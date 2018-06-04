# Создание формы справочника SysS

В конфигураторе выбираем узел Forms -&gt;Forms group -&gt; Формы-Тест

![](../../.gitbook/assets/fs1.jpg)

В этот узел добавим новый узел, форму которая будет отображать данные из справочника SysS.

Выделяем узел Формы-Тест  и в меню выбираем  Add subnode , в открывшемся окне выбираем Forms

![](../../.gitbook/assets/fs2.jpg)

нажимаем Ок

и вводим имя: Форма SysS.

В конфигураторе видно, что в узел дерева Формы-Тест добавился под узел.

Настройка свойств формы.

| **Название свойства** | **Тип** | **Описание**  | **Значение для примера**  |
| --- | --- | --- | --- | --- | --- | --- |
| Active | Boolean | действующий объект | true |
| Caption | Boolean | подпись формы | Маршруты |
| DLL FormName | String | тип формы | SysS |
| DLL ID | Integer | идентификационный номер DLL | 0 |
| TIP | String | тип справочника SysS | S |
| TIP.COD | String | подгруппа справочника GR1 | 79 |

 В конфигураторе: 

![](../../.gitbook/assets/fs3.jpg)

И обязательно нужно нажать Commit \(красную галочку\).

В Une нажимаем F5 \(Обновить\).

В меню формы добавится наш справочник Форма SysS.

![](../../.gitbook/assets/fs4.jpg)

Выбрав Форма SysS откроется справочник S 79, который можно дальше настраивать.

Примечание:

Если не работает привязка справочника в уне к унивЛисту в конфигураторе, то причиной может быть пустое свойство Active или его отсутствие

```sql
[ZZZ]
Active=true
.type.Active=Boolean
```
