# Диагностика

  
1. Если нет возможности выполнить команду alter session в диагностируемой сессии, то нужно определить sid и serial\# нужной сессии - по view v$session.

2. Включить трассировку:

2.1 Если есть возможность выполнить в диагностируемой сессии, то:

```sql
alter session set 
events '10046 trace name context forever, level 12'
```

Вместо 12 могут быть установлены другие уровни, подробности - по ссылке в конце описания.

2.2 Если включение выполняется из другой сессии, то:

 Вместо sid, serial\# - значения, найденные на первом шаге.

```sql
begin 
dbms_system.set_ev(sid,serial#,10046,12,''); 
end;
```

Трассировку желательно включить непосредственно перед выполнением проблемного действия, чтобы уменьшить объём не несущих пользы для диагностики данных.

2.3 STATISTICS\_LEVEL \(опционально\)

Значение по умолчанию для параметра statistics\_level = typical. При таком значении детальная статистика выполнения запроса \(row source execution statistics\) может содержать существенную погрешность. Если есть подозрения на ошибки подсчёта статистики       выполнения, можно повторить трассировку с включённым

```sql
alter session set statistics_level = all
```

При этом возможно и увеличение общего времени выполнения запроса из-за доп. нагрузки на более точный подсчёт статистики, особенно при большом количестве относительно быстрых операций \(nested loops\).

3. Выполнить проблемное действие в программе.

4. Дождаться окончания работы в приложении и закрыть программу \(завершить сессию\).

Если не завершить сессию \(не закрыть программу\), то часть необходимой информации не попадёт в трэйс-файл. Перед закрытием программы, из диагностируемой сессии нужно   выполнить \(если есть возможность\) следующие команды:   

```sql
alter session set session_cached_cursors = 0;
-- закрытие кэшированных курсоров
alter session set events '10046 trace name context off'; 
-- отключение трассировки
```

Именно при закрытии курсоров в трэйс файл попадает информация о плане выполнения запросов.

5. Проверить, сформировался ли трэйс-файл.

 - В обычной конфигурации трэйс-файлы формируются в папке udump.

  Найти путь к udump можно так:

```sql
 select value from v$parameter where name='user_dump_dest'
```

Если сервер работает в Shared Server Mode, а также если диагностируемая сессия - job или другой background процесс, то трэйс будет сформирован в папке bdump.

```sql
 select value from v$parameter 
 where name='background_dump_dest'
```

{% hint style="info" %}
 В 11g условия изменились
{% endhint %}

- Трэйс должен содержать строку вида:

\*\*\* SESSION ID:\(sid.serial\#\)  &lt;дата и время&gt;

где sid и serial\# - из первого пункта

- Если трэйс не сформировался, необходимо повторить процедуру.

Возможно, была некорректно идентифицирована нужная сессия.

6. Обработать полученный файл при помощи tkprof.

Необходимо получить 4 файла, обработанных tkprof - без сортировки, с сортировкой sort=prsela, sort=exeela, sort=fchela.

Пример: \(имя файла трассировки - catalog\_ora\_2384.trc\)

Вызов tkprof из командной строки:

При каждом вызове необходимо указывать новое имя файла, чтобы не перекрыть уже имеющиеся.

Удобно добавлять суффикс с первой буквой параметра сортировки.

1\) tkprof catalog\_ora\_2384.trc catalog\_ora\_2384.out sys=no

2\) tkprof catalog\_ora\_2384.trc catalog\_ora\_2384\_p.out sys=no sort=prsela

3\) tkprof catalog\_ora\_2384.trc catalog\_ora\_2384\_e.out sys=no sort=exeela

4\) tkprof catalog\_ora\_2384.trc catalog\_ora\_2384\_f.out sys=no sort=fchela

7. Для дальнейшего анализа нужны все полученные на выходе tkprof файлы и файл трассировки.

{% hint style="warning" %}
Доп. информация: [http://www.sql.ru/faq/faq\_topic.aspx?fid=389](http://www.sql.ru/faq/faq_topic.aspx?fid=389)
{% endhint %}



