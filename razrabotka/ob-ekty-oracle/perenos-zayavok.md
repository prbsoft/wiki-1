# Перенос заявок

**Для переноса заявок с un4@maconweb на рабочую схему нужно сделать следующее:**

1. Перенести данные из a$env.

2. Перенести данные из tms\_syss по tip=’Z’ and cod between 2001 and 2010.

3. Перенести секцию конфигуратора Settings-&gt;System settings-&gt;WEB\_ORDERS.

4. Перенести узел конфигуратора Documents-&gt;Заявки-&gt;Заявка клиента \(sysfid=48331\)

5. В tms\_mpt проставить единицы измерения \(cant\_id\_um\).

Даже после этого с заявками работать не получится, как минимум по двум причинам.

1. Справочник торговых точек и в документе в программе, и при работе через web будет пустым до тех пор, пока не будут настроены взаимосвязи: торговая точка-маршрут, агент-маршрут, агент-пользователь. Варианты выхода из ситуации:

 - менять текст пакета pg\_orders\_web и настройки документа в программе \(довольно сложно/трудоемко; так как пакет стандартный, то придется создать контекст и везде делать вилки: если контекст такой-то, то ориентироваться на эти привязки, иначе показывать всё\)

 - либо проставить напротив всех клиентов какой-то “липовый” маршрут, создать на каждого пользователя запись в справочнике агентов и настроить на каждого агента этот маршрут \(не очень хорошо, так как надо будет поддерживать актуальность этих “липовых” данных\).  


2. Чтобы заявки корректно заполнялись, нужно переписывать процедуру расчета цены \(дописывать свою вилку\), так как расчет, сделанный для митхауса/солвекса, не подходит и цены будут приходить нулевыми. Вилку нужно будет дописать в pkg\_orders\_docs.getpret\_sc вместо:

```sql
elsif v_tip=4 then
 ------------------------------------------
  vpret:=1;
 ------------------------------------------
 end if;
```



