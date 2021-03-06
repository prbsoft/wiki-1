# Установка Toad

 Установка программного обеспечения Toad производится на стенде виртуальной машины Oracle VM VirtualBox версии 4.2.16 r86992 на операционной системе Windows Server 2003\(установка только программы Toad\) и Windows Server 2003 SP2\(полная установка всех утилит\). Подключение Toad осуществляется к базе данных Oracle Database 11g версии 11.2.0.1. Для установки программного обеспечения Toad необходимо открыть папку Toad DBA Suite for Oracle 11.0 Commercial.

![](../.gitbook/assets/u-1.png)

 После чего кликнуть два раза по файлу Toad DBA Suite for Oracle 11.0 Commercial.

![](../.gitbook/assets/u-2.png)

 В результате чего выйдет главное меню установки, где необходимо согласиться с условиями лицензионного соглашения.

![](../.gitbook/assets/u-3.png)

 После чего нажать

![](../.gitbook/assets/next-1%20%282%29.png)

![](../.gitbook/assets/u-4.png)

Далее необходимо сделать выбор какие утилиты устанавливать, а какие нет. Обратите внимание на красные круги возле утилит Toad for Data Analyst Base Edition, Quest SQL Optimizer for Oracle, Benchmark Factory for Databases и Sroplight on Oracle. Так как используется операционная система Windows Server 2003, а программное обеспечение Toad требует продукты Net Framework 3.5 SP1 и Microsoft MSXML 4.20.9818.0.

Внизу расположен путь установки, который  при желании можно изменить.

![](../.gitbook/assets/u-5.png)

 При переходе по ссылке, можно скачать недостающие модули.

![](../.gitbook/assets/u-6.png)

![](../.gitbook/assets/u-7.png)

![](../.gitbook/assets/u-8.png)

 Или установить галочку только на Toad for Oracle и нажать

![](../.gitbook/assets/install.png)

![](../.gitbook/assets/u-9.png)

 На прогресс баре можно увидеть процесс установки.

![](../.gitbook/assets/u-10.png)

 По окончании которой будет запись "Installation complete!" после чего необходимо нажать 

![](../.gitbook/assets/next-1.png)

![](../.gitbook/assets/u-11.png)

 На этом выборочная установка продукта Toad for Oracle завершена. Необходимо нажать

![](../.gitbook/assets/finish%20%282%29.png)

![](../.gitbook/assets/u-12.png)

### **Полная установка.**

Полная установка производится на операционной системе Windows Server 2003 SP2, которая удовлетворяет все требования программного обеспечения Toad.

![](../.gitbook/assets/pu-1.png)

 У каждой утилиты показана версия, статус установки и статус бар. Ниже расположен общий статус бар.

![](../.gitbook/assets/pu-2.png)

![](../.gitbook/assets/pu-3.png)

 После достижения всех статус баров 100% установка завершится и выйдет сообщение "Installation completed!" после чего необходимо нажать

![](../.gitbook/assets/next.png)

![](../.gitbook/assets/pu-4.png)

 На этом полная установка завершена, для выхода необходимо нажать 

![](../.gitbook/assets/finish.png)

![](../.gitbook/assets/pu-5.png)

 В результате на рабочем столе появятся ярлыки программы Toad for Oracle, а так же её утилит.

![](../.gitbook/assets/pl-1.png)

###  **Процедура лечения.**

 Независимо от типа установки, программное обеспечение Toad необходимо активировать.

 После запуска ярлыка "Toad for Oracle 11" с рабочего стола

![](../.gitbook/assets/pl-2.png)

 выйдет сообщение о активации лицензии.

![](../.gitbook/assets/pl-3.png)

 Запустив файл keygen.exe

![](../.gitbook/assets/pl-4.png)

 выйдет окно Quest Keymaker.

![](../.gitbook/assets/pl-5.png)

 Далее из списка необходимо выбрать тип продукта "TOAD".

![](../.gitbook/assets/pl-6.png)

 В окно "Site Message" необходимо ввести "bs" и нажать на

![](../.gitbook/assets/generate.png)

 для генерации ключа.

![](../.gitbook/assets/pl-7.png)

 После чего в строку "Site message" ввести "bs", а в строку "Key" ввести полученный код и нажать на

![](../.gitbook/assets/apply.png)

![](../.gitbook/assets/pl-8.png)

 После чего мы увидим данные о регистрации.

![](../.gitbook/assets/pl-9.png)

###  **Запуск.**

 Запуск осуществляется с ярлыка

![](../.gitbook/assets/pl-2-1.png)

 Получаем сообщение об отсутствие модуля настройки SQL. \(При желании можно поставить галочку не показывать это сообщение снова\) и нажимаем 

![](../.gitbook/assets/ok.png)

![](../.gitbook/assets/z-1.png)

 В следующем окне появляется возможность копирования предыдущих файлов пользователя или выполнить чистую установку. Для продолжения необходимо нажать на кнопку

![](../.gitbook/assets/next-1%20%281%29.png)

![](../.gitbook/assets/z-3.png)

На следующих скриншотах показан выбор визуального стиля:

_Выпадающий стиль_.

![](../.gitbook/assets/z-4.png)

 _Однорядные вкладки._

![](../.gitbook/assets/z-5.png)

 _Многорядные вкладки._

![](../.gitbook/assets/z-6.png)

 _Древовидный стиль._

![](../.gitbook/assets/z-7.png)

 Так же можно включить иконки, поставив галочку на "_Show icons_" \(действует только в выпадающем стиле и в одно- и многорядных вкладках\).

![](../.gitbook/assets/z-8.png)

![](../.gitbook/assets/z-9.png)

 В следующем окне находятся общие настройки. Здесь можно настроить параметры запуска, выключения и визуального стиля. В параметрах запуска находятся настройки, позволяющие запускать несколько копий Toad, использовать сигнал Toad при запуске программы,  показывать окно входа в систему и открывать окно на новые соединения. В параметры выключения входит возможность подтверждения перед закрытием Toad. В параметрах визуального стиля можно настроить стиль панели инструментов и док- панели.

![](../.gitbook/assets/z-10.png)

В следующем окне можно настроить параметры Oracle. В частности в общих настройках:

o  возможность включения функции Commit \(завершение транзакции\) после каждого оператора.

o  возможность выполнения запросов в потоке\(создается отдельная сессия\).

o  возможность сохранения паролей при подключении к Oracle.

o возможность использования DataBase Administrator \(DBA\) просмотров \(если схема использует доступ к ним\).

o использования запросов только чтение.

Настройки сессий:

o  Основная сессия Toad.

o  Отдельная сессия.

Настройки при завершения соединения:

o Завершение транзакции \(Commit\)

o Откат изменений \(Rollback\)

o Запрос завершения транзакции/откат изменений когда изменения обнаружены или обнаружение не представляется возможным из-за отсутствия привилегий.

 После настройки всех опций необходимо нажать

![](../.gitbook/assets/next%20%282%29.png)

![](../.gitbook/assets/z-11.png)

В следующем окне доступны пакеты диагностики.

После выбора необходимо нажать

![](../.gitbook/assets/next%20%281%29.png)

![](../.gitbook/assets/z-12.png)

 После чего настройка завершится нажатием

![](../.gitbook/assets/finish%20%281%29.png)

![](../.gitbook/assets/z-18.png)

 В главном меню необходимо выбрать базу данных, тип подключения и цвет \(при желании\).

![](../.gitbook/assets/z-19.png)

 Созданная база данных называется ORCL, заполняем имя пользователя и пароль SYS. При нажатии на

![](../.gitbook/assets/connect.png)

 будет произведен вход под системным администратором базы данных \(DBA\).

![](../.gitbook/assets/z-20.png)

 Вход выполнен.

![](../.gitbook/assets/z-21.png)

