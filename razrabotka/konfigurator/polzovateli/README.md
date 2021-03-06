# Пользователи

**Права пользователей**

В программе существует несколько групп пользователей с разными правами доступа, которые можно редактировать. В зависимости от того, в какой группе находится пользователь, тем набором прав он и обладает. Данную функцию выполняет системный администратор либо программист, заранее согласовав список групп пользователей и права доступа с администрацией компании-клиента. 

Администратор в программе имеет доступ ко всем разделам, может изменять настройки программы и так далее. Он может также создавать новых пользователей, назначать права доступа, изменять их свойства и удалять ненужных пользователей. 

В представленной ниже таблице описаны свойства, необходимые для создания пользователей. Таблица свойства разделена на  две части, обязательные являются важными для создания учетной записи пользователя.

| **Название свойства** | **Тип** | **Описание**  | **Значение для примера**  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|   |   | Обязательные свойства: |   |
| Enabled | Boolean | Значение true говорит о том, что учетная запись пользователя активна.  \(Если True, настройки пользователя видимы для приложения Universal Accounting, если False – объект игнорируется\) | true |
| ID | Integer | Идентификационный номер пользователя \(соответствует значению поля \[UserID\]  таблицы документов для записей документов пользователя\) | 1001 |
| UserName | String | Логин пользователя.  \(Имя пользователя. Вводится в поле UserID при запуске приложения Universal Accounting\) | petrov |
| Encoded | Integer | \(Авто\) Закодированный пароль пользователя. |   |
| PassDate | Date | \(Авто\) После определения пароля автоматически проставляется дата.  |   |
|   |   |  Дополнительные свойства: |   |
| Admin  | String  | Если значение=1, то пользователь обладает правами администратора.   | 1 |
| AllowGridDesign  | Boolean  | Разрешить изменение дизайнов \(применяется для пользователей, у которых нет прав администратора, но которым нужно разрешить изменение дизайнов\).  | true  |
| AutoFreeMemory   | Boolean  | Выгружать неисп. DLL. Выгружать из памяти неиспользуемые динамические библиотеки \(DLL и BPL\).   | true   |
| Familia Numele Prenumele  | String  | Фамилия, имя, отчество пользователя.  \(информативное поле\)  | Петров Иван Сергеевич  |
| ConfirmExit  | Boolean  |   | false  |
| InitSQL  | Memo  | Права, прописанные программно в коде программы.  | begin:res:=2; envun4.EnvSetValue                                  \('restricted\_syss\_tip','tip in \(''R''\)                                                                    and cod in \(502,18,61\)'\); envun4.            EnvSetValue\('restricted\_syss\_tip',                                                                        'tip in \(''S''\) and cod in \(14\)'\);end; |
| LACSetupBlockSections  | String  | Список всех журналов, справочников, находящихся на верхней функциональной панели.  Используется для облегченного интерфейса. Список объектов Формы \(имена соответствующих узлов\), не доступных группе пользователей. \(Список секций форм и справочников, которые пользователю видеть запрещено\).   | J\_MATERIAL ,J\_CONFIRMARE, J\_CLASIFICATOARE,                                                        F\_CLASIFICATOARE, J\_RAPOARTE,F\_FORME, cl\_tms\_order\_inf\_supliment,                                                  J\_CONFIRMARF |
| LACSetupBlockSections\_old  | String  |   | 0:0:ActeOrdere,0:1:ActeOrdere,                             f\_ruta\_agent,f\_ruta\_client  |
| PeriodStart  | String  | Период, с которого пользователь имеет право видеть документы. Частная дата начала периода редактирования документов. Допускается SQL-выражение. Если значение параметра отсутствует, вместо него используется значение параметра GlobalPeriodStart. | 01.01.2012  |
| PeriodEnd  | String   | Частная дата окончания периода редактирования документов. Допускается SQL-выражение. Если значение параметра отсутствует, вместо него используется значение параметра GlobalPeriodEnd  |  01.12.2012 |
| PeriodFinish  | String  | Период окончания, с которого пользователь не имеет право видеть документы.  | 01.12.2012  |
| PassAttempts  | Integer  |  Количество попыток ввода неправильного пароля | 5  |
| LACReportsSelectedOnly  | Boolean  | Интерпретировать параметр  LacSetupBlockReports как список разрешенных секций. | true |
| LACSetupBlockReports  | String   | Список секций отчетов, которые пользователю видеть запрещено. | R\_MATERIAL  |
| LACSetupBlockObjects  | String  | Список объектов, с которыми пользователю работать запрещено.  | NRSET  |
| LACSectionsSelectedOnly  | Boolean   | Интерпретировать параметр LacSetupBlockSections  как список разрешенных секций.   | true  |
| LACObjectsSelectedOnly  | Boolean  | Интерпретировать параметр LACSetupBlockObjects как список разрешенных секций.  | true  |
| Language  | String  | Язык интерфейса.  Значения:  0-англ.яз.  1-рум.яз.  2-русский  По умолчанию стоит 1-рум.яз.   | 2  |
| DataEmpty  | Boolean  | Если True, игнорируется значение по умолчанию поля \[Дата\] таблицы документов при вводе документов пользователем  | false  |
| DesignGroup  | Integer  | Номер группы дизайнов \(ненулевое значение позволяет пользователю иметь персональные дизайны, переводы, схемы отчетов и т.п.\). Администратор может менять себе этот номер во время выполнения программы \(через интерфейс меню\).  |   |
| Password  | String  | Пароль пользователя. Вводится в поле Password при запуске приложения Universal Accounting  |   |
| seqNRMANDisableChanges  | Boolean  | Запретить пользователю изменять поле NRMANUAL.  | true  |
| DEF\_JOURNAL  | String  | Журнал \(фильтр на документы\), устанавливаемый по умолчанию при запуске приложения Universal Accounting  | J\_BANK  |
| Docs View Mode  | String  | 0- All documents – пользователям доступны все документы 1- All group documents – пользователям доступны только документы пользователей группы 2- Private documents – пользователям доступны только личные документы  | 2  |
| Docs edit mode  | Integer  | 0 - All documents - все документы   1 - All group documents - документы группы  2 -Private documents-документы пользователя \(только свои\)  Если выбран режим 1 - документы группы, то необходимо на группе создать свойство - UserGroupList  | 2  |
| DivVisible  | Boolean  |   | false  |
| GridPropCacheLimit   | Integer   | Размер кеша дизайнов. Максимальный размер кеша дизайнов в памяти.  За единицу берется один тип  документа, один узел дерева отчетов, одна форма или справочник.  | 100 |
| GridDisableNumberSearch   | Boolean   | Запрет числового поиска. Режим текстового поиска даже в числовых полях грида \(вместо числового поиска\).  | true   |
| RepairGridDesign   | Boolean   | Исправление ошибок. Режим автокоррекции загружаемых дизайнов \(бывает нужен при работе с ORACLE 9i\).   | true  |
| RepDataStart  | String  | Дата начала периода просмотра данных в отчетах. Допускается SQL-выражение. Если значение параметра отсутствует, вместо него используется значение параметра PeriodStart. |   |
| RepDataEnd  | String  | Дата окончания периода просмотра данных в отчетах. Допускается SQL-выражение. Если значение параметра отсутствует, вместо него используется значение параметра PeriodEnd.  |   |
| ReportTreeSorting   | Boolean   | Сортировка узлов. Режим сортировки узлов дерева отчетов по алфавиту.   | true   |
| StartupReportNode   | String   | Стартовый узел. Имя секции отчета, на котором позиционировать дерево отчетов сразу после открытия  окна менеджера отчетов.  |   |
| RepTestRecordCount  | Boolean   | Проверять к-во записей. Режим проверки количества записей в наборе данных отчета \(для F1Reports\):   при очень большом количестве записей выдается предупреждающее сообщение, имеется возможность  отменить построение отчета или вручную ограничить количество выводимых записей.  Предельное количество записей для отчетов Master/Detail - 1000, только Master - 10000.  | true    |
| RepDeleteTempTables   | Boolean   | Удалять врем. таблицы. Режим удаления временных таблиц ORACLE после построения отчета \(можно выключить\).   | true     |
| LangDontLoad   | Boolean   | Не загружать переводы. Не пытаться загружать тексты переводов из ORACLE \(для уменьшения  траффика\).  | true  |
| LoadCaptionsSep   | Boolean   | Заголовки отдельно. Режим раздельной загрузки переводов заголовков столбцов и дизайнов  \(для совместимости с переводами заголовков столбцов, сохраненными в предыдущих версиях SL\).  | true  |
| UserGroupList  | String  | Список кодов пользователей \(через запятую\), составляющих группу, используемую в параметрах Docs View Mode и Docs edit mode. Этот параметр удобно заводить на уровне секции группы пользователей.В таком случае пользователи будут видеть документы пользователей, входящих в группу.  | 1,2,3,4,7,15  |
| UseDotInCont   | Boolean   | Точка в счете. Использовать точку в значении счета \(формат 99.99\) - удобно для ПМР.  | true   |
| UseSmartTab   | Boolean   | "Умный" &lt;Tab&gt;. Режим интеллектуального поведения клавиши &lt;Tab&gt;: переход от поля к полю по всему  активному окну.  | true  |
| UseSpeedSearch   | Boolean  | Быстрый поиск в справ.. Режим быстрого поиска в выпадающих справочниках.   | true   |
| UseSmartEnter   | Boolean   | "Умный" &lt;Enter&gt;. Режим интеллектуального поведения клавиши &lt;Enter&gt; на дополнительной \(цифровой\)  клавиатуре:  при редактировании таблиц - переход к следующему полю или \(из последнего столбца\)  завершение редактирования и вставка новой записи.  | true   |
| UseSmartEnterNotebook | Boolea  |   | true  |
| UnivListReadOnly | Boolean |   | false  |
| SmartEnterLikeTab  | Boolean |   | true  |
| USER\_SC  | Integer  | Код пользователя из универс. Чтобы получить этот код в клиенте  \(добавляем приставку param\_\):sys\_context\('envun4','param\_user\_sc'\)  | 25820  |
| UseCMX  | Boolean |   | false  |
| PassUnique  | Boolean | Пользователю/ям можно повторять пароль   | false  |
| ToolBarFormSections  | String   | Пример 2-х уровневого меню форм \(даже с переводами: см. "Cliente,Клиенты"\)   | \*Producte,F\_PROD\_GR,F\_PRODUCTS,                            \*"Cliente,Клиенты", F\_CLIENTS,F\_AGENTS,                              \*Rute,F\_ROUTES,F\_RUTE\_DESF,\*, F\_UM,F\_TT,F\_PRICE,F\_INF\_SUPLIMENT,                                       F\_TIP\_DOC, F\_CAUZA\_RETUR,F\_BANKS,\*"Facture",                        F\_DEBLOCAREA\_NN, F\_STRICTPAPER\_DOCS  |
| ToolBarFormSections\_  | String  |   | \*Producte,F\_PROD\_GR,F\_PRODUCTS,                           \*"Cliente,Клиенты", F\_CLIENTS,F\_AGENTS,\*Rute,F\_ROUTES,                               F\_RUTE\_DESF,\*, F\_UM,F\_TT,F\_PRICE,F\_INF\_SUPLIMENT,                                      F\_TIP\_DOC, F\_CAUZA\_RETUR,F\_BANKS,\*"Facture",                         F\_DEBLOCAREA\_NN, F\_STRICTPAPER\_DOCS  |
| ToolBarFormSections\_\_  | String   |   | F\_PROD\_GR,F\_PRODUCTS,F\_CLIENTS,                      F\_AGENTS,F\_ROUTES, F\_RUTE\_DESF,F\_UM,F\_TT,  F\_PRICE,F\_INF\_SUPLIMENT, F\_BANKS,F\_CERT  |
| TBDocCmd  | Boolean |   | true  |
| TBForms  | Boolean |   | false  |
| HideErrorLevel   | Integer  | 2 =&gt; все ошибки показываются в статус баре; 1 =&gt; в статус баре показываются все ошибки, кроме msg.  Меню Сервис-&gt;журнал ошибок. \(DblClick по статус-бару\)  | 2  |
| HideMenuDict   | Boolean | Меню справочников. Отображение меню "Справочники" \(по умолчанию включено\).  | true   |
| HideMenuReps   | Boolean | Меню отчетов. Отображение меню "Отчеты" \(по умолчанию включено\).   | true   |
| HideMenuForms   | Boolean | Меню форм. Отображение меню "Формы" \(по умолчанию включено\).   | true   |
| ViewFromToday   | Integer   | Ограничение периода. Ограничение периода отображаемых документов  как смещение на указанное  число дней назад от текущей даты.  |   |
| ViewBegin   | String   | Ограничение снизу. Минимальная дата отображаемых документов |   |
| ViewEnd   | String    | Ограничение сверху. Максимальная дата отображаемых документов   |   |
| LastRecord  | Boolean | К последнему документу. При открытии журнала документов переходить на последний видимый  документ.  | true  |
| ORDER BY   | String   | Порядок сортировки. Порядок сортировки документов \(список имен полей, разделенных запятыми\).   |   |
| OraLoaderModeDML  | Boolean | Режим загрузки данных. Использование DML при загрузке данных из текстового файла или таблицы BDE.  Этот режим снижает скорость загрузки, но позволяет обойти некоторые ограничения.  | true   |
| DataAutomat  | Boolean | DATAMANUAL как в пред.. Автозаполнение даты документов при вводе на основании даты предыдущего документа.  | true  |
| DataCurrent  | Boolean | DATAMANUAL сегодня. Автозаполнение даты документов при вводе на основании текущей даты.   | true   |
| DataEmpty   | Boolean | Пустая DATAMANUAL. Отменить для пользователя автозаполнение поля DATAMANUAL  \(отмена глобальных параметров DataAutomat и DataCurrent\).  | true  |
| PXCMSimpleEditing   | Boolean | Режим быстрой правки. Режим быстрой правки проводок документов версии PX.   | true  |
| Backup   | Boolean | Архив документов. Режим сохранения документов в архиве перед их удалением.  | true   |
| XDEF\_BGFILTER  | String   | Фильтр по умолчанию. Начальное значение фильтра по NrSet: здесь нужно перечислить  через запятую коды тех позиций фильтра, которые должны быть изначально включены.  \(Имеются в виду коды, которые можно увидеть в последнем столбце верхней таблицы в  окне установки фильтра по NrSet - колонка "№"\). Вместо списка кодов можно ввести символ "\*", что означает "включить все".  |  1,2,3,1226 |
| XDEF\_NRSET   | String   | NrSet по умолчанию. Начальное значение NrSet по умолчанию.  |   |
| XDEF\_NRSET\_VIEW   | String   | Ограничение по NrSet. Список кодов NrSet, которыми ограничиваются права пользователя.   |   |
| HideNrsetFilter   | Boolean | Скрыть фильтр по NrSet. Не отображать установленный фильтр по NrSet.   | true   |
| \_\_XDEF\_NRSET  | Integer  |   | 201  |
|   |   |  Панели инструментов: |   |
| TBIconStyle  | Integer   | Расположение значков. Число от 0 до 3 означает положение значка относительно пункта главного меню: 0 - Значки не выводятся на экран \(в меню - только надписи\);  1 - Надписи не выводятся на экран \(в меню - только значки\);   2 - Значки выводятся на экран слева от соответствующих надписей;  3 - Значки выводятся на экран над соответствующими надписями.  | 3   |
| TBIconSize   | Integer    | Размер значков. Число от 0 до 2 означает размер значков в главного меню:  0 - Мелкие значки;  1 - Средние значки;  2 - Крупные значки.   | 2  |
| TBPeriod  | Boolean | Панель периодов. Отображать на экране панель ввода периодов.   | true   |
| TBWindowList   | Boolean | Панель открытых окон. Отображать на экране панель открытых окон.   | true   |
| HideDocPreview | Boolean |   | true  |
| HideDocsActive | Boolean |   | false |
| HideDocsBarCode | Boolean |   | true   |
| HideDocsDesign  | Boolean |   | true    |
| HideDocsDublare  | Boolean |   | true     |
| HideDocsEditare  | Boolean  |   | true  |
| HideDocsFact  | Boolean   |   | true   |
| HideDocsHeadLine  | Boolean  |   | true    |
| HideDocsLang  | Boolean   |   | true     |
| HideDocsLich  | Boolean  |   | true  |
| HideDocsPeriod | Boolean   |   | true  |
| HideDocsSalvare | Boolean  |   | true  |
| HideDocsSold  | Boolean   |   | true   |
| HideDocsSpec  | Boolean    |   | true    |
| HideDocsSwitch  | Boolean   |   | true  |
| HideDocsTabAdd  | Boolean    |   | true   |
| HideDocsTabCM  | Boolean   |   | true    |
| HideDocsTabLog  | Boolean    |   | true     |
| HideDocsTabMain  | Boolean   |   | true      |
| HideDocsTabObj  | Boolean    |   | true       |
| HideDocsTabXL  | Boolean   |   | true  |
| HideDocsToolBar  | Boolean    |   | true   |
| HideDocsTotals  | Boolean    |   | true    |
| HideDocsWizard  | Boolean  |   | true  |
| HideF1Buttons  | Boolean   |   | true   |
| HideMemory  | Boolean  |   | true    |
| HideMenuDoc  | Boolean   |   | true  |
| HideMenuHelp  | Boolean    |   | true   |
| HideMenuUtil  | Boolean  |   | true  |
| HideMenuWindow | Boolean   |   | true   |
| HideNaviPDC  | Boolean    |   | true  |
| HideNaviSQL  | Boolean    |   | true   |
| HideNaviSysS  | Boolean   |   | true    |
| HideNaviUniv  | Boolean    |   | true     |
| HideStatusBar  | Boolean  |   | true      |
| HideToolCalc  | Boolean   |   | true       |
| HideToolInf  | Boolean    |   | true        |
| HideToolLang  | Boolean     |   | true         |
| HideToolMsg  | Boolean    |   | true          |
| HideToolNavi  | Boolean     |   | true           |
| HideToolSet  | Boolean  |   | true  |
| HideToolSys  | Boolean   |   | true   |
| GotoDocumentEditing  | Boolean    |   | true    |
|   |   | Скрытие пункта меню "Журналы"  |   |
| HideMenu   | Boolean  |   | true   |
| HideMenuJrnlStd  | Boolean  |   | true |
| TBJournals  | Boolean  |   | true  |
|   |   | Включение кнопки SubSet в EasyInterface | Примечание: в LACSetupBlockObjects не должно быть NRSET  \(если при этом LACObjectsSelectedOnly не объявлено или =false\)  \(если на нашем уровне LACSetupBlockObjects пустой, тогда возьмется с уровня выше. так что вместо пустого надо задать значение: -\)  |
| BG\_FILTER\_SECTION  | String   |   | 1  |
| HideDocGrid  | Boolean   |   | false   |
| HideNrsetFilte  | Boolean  |   | false   |
| HideToolbar  | Boolean   |   | false   |
| InitSQL  | Memo   |   | begin  :res:=2; Bg\_Policy.INITFILTER\_NRSET\_TREE    \('ID IN \(1,2,3\)'\);end;  |



Действия над учетными записями в конфигураторе UniConf:**Свойства, установленные для группы пользователей, распространяются на всех пользователей группы.**

1\) [Создание учетной записи пользователя](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5+%D1%83%D1%87%D0%B5%D1%82%D0%BD%D0%BE%D0%B9+%D0%B7%D0%B0%D0%BF%D0%B8%D1%81%D0%B8+%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D0%B5%D0%BB%D1%8F)

2\) [Смена пароля](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%A1%D0%BC%D0%B5%D0%BD%D0%B0+%D0%BF%D0%B0%D1%80%D0%BE%D0%BB%D1%8F)

3\) [Удаление учетной записи пользователя](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%A3%D0%B4%D0%B0%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5+%D1%83%D1%87%D0%B5%D1%82%D0%BD%D0%BE%D0%B9+%D0%B7%D0%B0%D0%BF%D0%B8%D1%81%D0%B8+%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D0%B5%D0%BB%D1%8F)

Иногда полезно временно получить права админа под текущим пользователем. Для этого можно использовать комбинацию клавиш Ctrl+F12. Запрашиваемый пароль настраивается в Settings-&gt;General следующим свойством:

| **Название свойства** | **Тип** | **Описание** | **Значение для примера** |
| --- | --- |
| Tmpadminpass | String | временные права админа под текущим пользователем | aaa |

[Настройка ограничения доступа на изменение универсального справочника](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%9D%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0+%D0%BE%D0%B3%D1%80%D0%B0%D0%BD%D0%B8%D1%87%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B4%D0%BE%D1%81%D1%82%D1%83%D0%BF%D0%B0+%D0%BD%D0%B0+%D0%B8%D0%B7%D0%BC%D0%B5%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5+%D1%83%D0%BD%D0%B8%D0%B2%D0%B5%D1%80%D1%81%D0%B0%D0%BB%D1%8C%D0%BD%D0%BE%D0%B3%D0%BE+%D1%81%D0%BF%D1%80%D0%B0%D0%B2%D0%BE%D1%87%D0%BD%D0%B8%D0%BA%D0%B0)

[Настройка ограничения доступа к проводкам \(tmdb\_cm\)](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%9D%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0+%D0%BE%D0%B3%D1%80%D0%B0%D0%BD%D0%B8%D1%87%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B4%D0%BE%D1%81%D1%82%D1%83%D0%BF%D0%B0+%D0%BA+%D0%BF%D1%80%D0%BE%D0%B2%D0%BE%D0%B4%D0%BA%D0%B0%D0%BC+%28tmdb_cm%29)

_Подсказка:_

[Как скрыть пароль](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%9A%D0%B0%D0%BA+%D1%81%D0%BA%D1%80%D1%8B%D1%82%D1%8C+%D0%BF%D0%B0%D1%80%D0%BE%D0%BB%D1%8C)

[Настройка прав на редактирование справочников UNIVERS](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%9D%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0+%D0%BE%D0%B3%D1%80%D0%B0%D0%BD%D0%B8%D1%87%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B4%D0%BE%D1%81%D1%82%D1%83%D0%BF%D0%B0+%D0%BD%D0%B0+%D0%B8%D0%B7%D0%BC%D0%B5%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5+%D1%83%D0%BD%D0%B8%D0%B2%D0%B5%D1%80%D1%81%D0%B0%D0%BB%D1%8C%D0%BD%D0%BE%D0%B3%D0%BE+%D1%81%D0%BF%D1%80%D0%B0%D0%B2%D0%BE%D1%87%D0%BD%D0%B8%D0%BA%D0%B0)

[Настройка прав на редактирование справочников SYSS](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%9D%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0+%D0%BF%D1%80%D0%B0%D0%B2+%D0%BD%D0%B0+%D1%80%D0%B5%D0%B4%D0%B0%D0%BA%D1%82%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5+%28tms_syss_unlock%29)

[Интерфейс](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%98%D0%BD%D1%82%D0%B5%D1%80%D1%84%D0%B5%D0%B9%D1%81)

Новые возможности по [ограничению паролей пользователей](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%9E%D0%B3%D1%80%D0%B0%D0%BD%D0%B8%D1%87%D0%B5%D0%BD%D0%B8%D0%B5+%D0%BF%D0%B0%D1%80%D0%BE%D0%BB%D0%B5%D0%B9+%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D0%B5%D0%BB%D0%B5%D0%B9)

