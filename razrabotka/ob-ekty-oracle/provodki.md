# Проводки

  
Для написание проводок документа, нужно написать процедуру

**Например** \(в конце имени процедуры рекомендуется добавлять  **\_gfc** \) ****

```sql
procedure temp_gfc(p_nrdoc number)  is  // в процедуру передаем номер документа
 insert into vmdb_cmi                                  // Проводки пишем во вьюху vmdb_cmi, а читаем из vmdb_cmr
 (nrdoc,                                                // указываем номер документа   
 dt,                                                       // дебетовая часть проводки , сначала указывается счет (счет или Дт)
 dt1,                                                     // субчсет (счет1 или Дт1) 
 dtsc,                                                   // Аналитика Дт
 dtdep,                                                // Цент затрат Дт
 dtsc1,                                               //  Субконто Дт
 ct, ct1, ctdep,ctsc, ctsc1,                  // кредитовая часть указывается аналогичным образом
 cant,                                                 // количество
 suma,                                               // сумма  
 sumavaldt,                                       // по необходимости можно указать сумму в валюте Дт  
 valutadt,                                          // тип валюты Дт (аналогично можно указать Кт часть)     
 dtnrdoc, ctnrdoc,                            // если у дебиты и кредита разные nrdoc (по необходимости)
 dtstrsc
 ,sumagaap)      
select * // перечисляете нужные поля
from таблица;
end; // конец процедуры         
```

Для генерации проводок с использование таблиц tms\_201m, tms\_201d - можно использовать стандартную процедуру gfc201

**\(рекомендуется для проводок писать отдельные процедуры\).**

Например:  

```sql
BEGIN
Gfc_Util.gfc201(
  :nrdoc
  ,vSuma=>'d.suma'
  ,vSumaGaap=>''
  ,vCtDep=>'d.DtDep'
);
END;
```

vCtDep=&gt;'d.DtDep' – не срабатывает если в справочнике счетов не проставлены значения полей:

Аналитика2 и СубАналитика2

