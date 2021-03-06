# Настройка UnivList

[Создание СПРАВОЧНИКОВ.](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5+%D1%81%D0%BF%D1%80%D0%B0%D0%B2%D0%BE%D1%87%D0%BD%D0%B8%D0%BA%D0%B0+%D1%82%D0%B8%D0%BF%D0%B0+Univ+List)

[Настройка Формы, ссылающейся на Univers](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D1%81%D0%BF%D1%80%D0%B0%D0%B2%D0%BE%D1%87%D0%BD%D0%B8%D0%BA+Univers)

Чтобы действовало свойство в конфигураторе необходимо задать имя секции с «:».

Например: UNIVLIST:O:F. 

Для создания расширенного справочника необходимо включить в конфигураторе свойство:

**SagiEditQuery=true.**

И настроить справочник на другую вьюху через Alt+Q и Alt+D в конфигураторе. При этом фильтры на поля Tip и GR1 устанавливаются клиентом автоматически в зависимости от справочника.

Свойства справочников \(узел конф. Univ lists\)

| **Имя свойства** | **Тип** | **Описание** | **Значение для примера** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| StartField | String | Поле позиционирования по умолчанию | denumirea |
| SpeedSearchQuery | String | Запрос для быстрого поиска,  который выполняется по нажатию Enter | SELECT cod,\(SELECT denumirea\_\_1 FROM vms\_univers u WHERE u.cod=t.cod \)  denumirea\_\_1 FROM TMS\_MPT t WHERE |
| SagiEditQuery | Boolean | Разрешить изменение запросов \(Alt+Q\) справочника | true |
| AutoFilterTree | String | Открывать определенное дерево в справочнике | 1 |
| AutoTree | Integer |  дерево которое будет открываться в справочнике по умолчанию | 5 |
| Gr1 | String | Значение поля GR1 из vms\_univers | TVR |
| Active | Boolean | действующий объект | true |
| Caption | String | Подпись справочника | 1. Справочник товаров |
| DLL FormName | String |   |   |
| DLL ID | Integer | Идентификационный номер DLL |   |
| ID | String | Идентификационный номер | Marfuri |
| MainAttr | String |  основная карточка, которая открывается по F3 или кнопка 'A' внизу формы | ATTR\_BAR |
| MenuAttr | String |  список карточек, которые открываются по кнопке ^ | ATTR\_PRC,ATTR\_MINMAX, ATTR\_STRGRP |
| StartField | String | Поле позиционирования по умолчанию | STRIH1\_CODPRODUCER |
| MainAttrActive | Boolean  | При открытии справочника сразу открыта карточка  | true |

Справочник из нескольких типов нужно создавать в группе UNIV\_ALL.

Пример справочника: [univ\_p\_m.xml](http://wiki.biznesssoft.ru:8081/xwiki/bin/download/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/UnivList+%D0%B8%D0%B7+%D0%BD%D0%B5%D1%81%D0%BA%D0%BE%D0%BB%D1%8C%D0%BA%D0%B8%D1%85+%D1%82%D0%B8%D0%BF%D0%BE%D0%B2/univ_p_m.xml) tip=P,M gr1=TVR,2112

