# Контексты сессии

  
**Установка контекста в пространстве имен EnvUn4:**

```sql
begin
EnvUn4.EnvSetValue('KADR_PLC_CALCD','1=0');
end;
```

**Получение значения контекста из пространства имен EnvUn4:**

```sql
select SYS_CONTEXT('EnvUn4','KADR_PLC_CALCD') from dual;
```

 **Посмотреть ВСЕ контексты сессии \(разные пространства имен\) в UNA можно следующим запросом:**

```sql
select attribute, value from session_context order by attribute;
```

В результате получаем список контекстов и их значений:

ATTRIBUTE,VALUE

A$BASE,PMR

-- Инициализируются на основе данных из секции конфигуратора Settings - AFIX

AFIX$COMIS1,4787

AFIX$COMIS2,4783

AFIX$COMIS3,4802

AFIX$COMIS4,4796

AFIX$CONT\_ACUMULATOR,2516

AFIX$CONT\_AF,123

AFIX$CONT\_ALTE\_ANTICIPATE,2510

AFIX$CONT\_ANVELOPE,2515

AFIX$CONT\_ARENDA\_CONSUM,9120

AFIX$CONT\_ARENDA\_PRESTARE,9122

AFIX$CONT\_AUTOMOB,1234

AFIX$CONT\_BEFORE\_AFIX,121 112

AFIX$CONT\_COST,7 8

AFIX$CONT\_FF,123 111

AFIX$CONT\_FF\_UZ,124 113

AFIX$CONT\_FILT\_ANTICIPATE,251 !2513

AFIX$CONT\_MET\_PRETIOS,9125

AFIX$CONT\_MF,123

AFIX$CONT\_MF\_UZ,124

AFIX$CONT\_SF,9123

AFIX$CONT\_TEREN,122

AFIX$CONT\_TVA,5349

AFIX$CONT1\_COMPLET\_UZAT,11

AFIX$CONT1\_CONSERV,17

AFIX$CONT1\_CORECTARE,12

AFIX$CONT1\_DECONSERV,6

AFIX$CONT1\_DONARE,15

AFIX$CONT1\_LIST\_IN,3,4,5,6,7

AFIX$CONT1\_LIST\_OUT,14,15,16,17,18,19

AFIX$CONT1\_REPAIR\_CAPITAL,51

AFIX$CONT1\_REPAIR\_LIMIT,9

AFIX$CONT1\_SLD,23

AFIX$DONT\_USE\_RUBRICA,true

AFIX$FILT\_SLD\_BEFORE\_AFIX,ABCDE12

AFIX$FILTSLD\_FF,ACDE

AFIX$FILTSLD\_FF\_UZ,AC

AFIX$GFC\_ZABALANS,false

AFIX$GR3\_CUMULATIV,40

AFIX$GR3\_LINIAR,1

AFIX$GR3\_NEUZURABIL,99

AFIX$GR3\_PROBEG,5

AFIX$GR3\_PRODUCERE,10

AFIX$GR3\_SLD\_ANUAL,30

AFIX$GR3\_SLD\_LUNAR,20

AFIX$GR3\_TERMEN,9

AFIX$GR4\_AUTOMOB\_LIMIT,4

AFIX$GR5\_NEPRODUCTIVE,6

AFIX$GR6\_IESIRE,4

AFIX$IMOB\_CONT,1231 1232

AFIX$IMOB\_CT\_IMP,5345

AFIX$IMOB\_CTSC\_IMP,917

AFIX$IMOB\_DT\_IMP,7134

AFIX$IMOB\_DTSC\_IMP,1299

AFIX$IMOB\_IMP\_K1,0.00025

AFIX$IMOB\_IMP\_K2,0.0005

AFIX$IMOB\_IMP\_K3,0.00075

AFIX$IMOB\_IMP\_K4,0.001

AFIX$K\_REPAIR\_LIMIT,0.15

AFIX$LIQ\_CONT6,6128

AFIX$LIQ\_CONT6MAT,6128

AFIX$LIQ\_CONT7,7141

AFIX$LIQ\_SC6,52785

AFIX$LIQ\_SC6MAT,52785

AFIX$LIQ\_SC7,52788

AFIX$PREDCOM,5298

AFIX$RAISE\_ERR,1

AFIX$REEVAL\_CONT,3411

AFIX$REEVAL\_CONT6,6216

AFIX$REEVAL\_CONT7,7214

AFIX$ROUND\_COEF\_UZ,9

AFIX$SALE\_CONT6,6128

AFIX$SALE\_CONT7,7141

AFIX$SALE\_SC6,52785

AFIX$SALE\_SC7,5269

AFIX$SC\_GRSF2,52096

AFIX$SC\_GRSF3,52097

AFIX$SC\_GRSF4,52098

AFIX$SC\_GRSF5,52099

AFIX$SCHEMA\_SEQ,0

AFIX$SC\_REPAIR\_CURRENT\_FILT,T4:34

AFIX$SUMA\_AUTOMOB\_LIMIT,200000

AFIX$UZ\_AN\_SC,1299

AFIX$UZ\_MF\_SC,1299

AFX$SCHEMA\_SEQ,1

A$UTIL.USER.OBJ\_ID,4314

-- Контексты, связанные с фильтром по филиалам

BG\_COMPANY,COMPANY1\_

BG\_COMPANY\_ID,1

BG\_POLICY\_NRSET\_TREE,ID IN \(2,4\)

BG\_POLICYPOLICYLEVEL,-1

BG\_POLICYSTP\_CALCD,trunc\(NRSET,-3\) IN\(SELECT trunc\(ID,-3\) FROM XNRSET\)

BG\_POLICYSTP\_CONT,NRCM IN\(SELECT ID FROM XNRSET\)

BG\_POLICYSTP\_DOCS,NRSET IN\(SELECT ID FROM XNRSET\)

BG\_POLICYSTP\_DTCT,DTNRCM IN\(SELECT ID FROM XNRSET\)OR CTNRCM  IN\(SELECT ID FROM XNRSET\)

CHANGE\_REG,REGM,REGD

-- Инициализируются на основе данных из секции конфигуратора Settings - COMPANY1

COMPANY\_ACTIVITY,1

COMPANY\_ADRESA,г.Тирасполь

COMPANY\_BANCA,Бенд. ф-ал № 6706 ЗАО "Приднестровский Сбербанк" г.Бендеры

COMPANY\_CASIR,ФИО кассира

COMPANY\_CODCASIR,4781

COMPANY\_CODDIRECTOR,4801

COMPANY\_CODECONOMIST,5348

COMPANY\_CODFISCAL,0200007751

COMPANY\_CODKADRY,4793

COMPANY\_CODTVA,N

COMPANY\_COD\_UNIV,5352

COMPANY\_COMPANYID,0

COMPANY\_CONTBANCAR,222615000001255

COMPANY\_CONTCOR,22262854

COMPANY\_CONT\_SEF,Сидорова Ф.Ю.

COMPANY\_DIRECTOR,ФИО директора

COMPANY\_GFOSS,045123

COMPANY\_GLOBALPERIODFINISH,31.12.3000

COMPANY\_GLOBALPERIODSTART,01.01.2012

COMPANY\_MFO,38

COMPANY\_NAME,ООО "Организация"

COMPANY\_NODETYPE,Company

COMPANY\_OKFS,16

COMPANY\_OKNH,51121

COMPANY\_OKOPF,49

COMPANY\_OKPO,37486514

COMPANY\_REGNUM,Т00011111

COMPANY\_SOATO,2826

COMPANY\_SOOGU,7774

COMPANY\_TELEFON,0/373-552/55555

--

DEFNRSET\_MAX,1

DEP\_PEREV\_COST,4651

DOCS\_ALT\_COLOR\_ENABLED,true

DOLJN\_CONSULT,33

F\_RECALC\_TVA,1

INIPARAM\_ADMINLEVEL,1

METOD\_UCETA,1

NRSET\_VALUTA\_LEN,1

NRSET\_VALUTA\_POS,1

-- Параметры по умолчанию, которые можно переопределить в секции конфигуратора USERS на группе польз. или на узле пользователь

PARAM\_DEFVALGAAP,USD

PARAM\_DEFVALM,RUB

PARAM\_NRSETDEFAULT,201

PARAM\_NRSETLENGTH,2

PARAM\_NRSETLEVELACCESS,1

PARAM\_PDCACC,1

PARAM\_PERIODBEG,01.11.2004

PARAM\_PERIODEND,31.12.3000

PARAM\_UNIVACC,1a

PARAM\_UNIVELACC,1

PARAM\_USERID,7

PARAM\_USERNAME,VBereza

PARAM\_USER\_SC,478800

--

REGNORM\_BLOCK\_RIGHTS,BLOCK

SCALES\_LNG,2

-- параметры, которые в основном инициализируются из таблицы a$env

PEREV\_ARENDA\_TO\_COST,4

SC\_DOPL\_PRAZDNIK,5639

SC\_DOPL\_VYHODNOI,5634

SC\_PEREV\_COST\_BAGAJ,4477

SC\_PEREV\_COST\_BILET,4477

SC\_PEREV\_COST\_INCAS,4477

SC\_ZP\_GPH,5236

SC\_ZP\_MROT\_ADD,5235

SC\_ZP\_MROT\_BAZE,5224

SC\_ZP\_NOCI,5152

SC\_ZP\_OSN,5091

SC\_ZP\_OSN\_OKLAD,5091

SC\_ZP\_PN\_MV,5234

SC\_ZP\_PRAZDNIK,5599

SC\_ZP\_SVERH,5670

SC\_ZP\_TS,5193

SC\_ZP\_VYHODNOI,5623

SYSFID\_GFC,1209

SYSFID\_PAYMENT,1113

SYSFID\_PEREV\_ARENDA,50020

SYSFID\_PEREV\_ARENDA\_OTP,50024

SYSFID\_PEREV\_ARENDA\_ZP,50022

SYSFID\_PEREV\_ARENDA\_ZP\_PER,50023

SYSFID\_PEREV\_CASSA,1159

SYSFID\_PEREV\_OPER\_CALC,50015

V\_SC\_ARENDA\_SAL\_ZP\_PER,4871

-- параметры, которые инициализируются из секции Settings - SLR

SL\_COD\_NEREZIDENT,2

SL\_COD\_REZIDENT,1

SL\_COD\_TEMPORARI,-1

SL\_COD\_UVOLEN,5046

SL\_CONCBUL\_SPLIT\_AUTO,1

SL\_CONC\_DONT\_RECALC\_PTRIMESTR,0

SL\_CONC\_KALEND\_ZILE\_TIP,1

SL\_CONC\_MM\_TIP,0

SL\_CONT\_AVANS,2277

SL\_CONT\_DEPONENT,5312

SL\_CONT\_KASSA,2411

SL\_CONT2272SF,2275

SL\_CONT5311,5311

SL\_CONT5311\_CONT,5311

SL\_CONT5311\_CONT1,0

SL\_CONT5313,5311

SL\_CONT5313\_CONT,5311

SL\_CONT5313\_CONT1,0

SL\_CONT5313\_9531,5311,9531

SL\_CONT5319,5319

SL\_CONT5331,5331

SL\_CONT5331\_29,5331

SL\_CONT5347,5347

SL\_CONT5393MP,5393

SL\_CONT9531,9531

SL\_CONT9532,9532

SL\_COUNT\_LUNI\_SCUTIRI\_ELIB,12

SL\_DOCS\_ZIMA\_AVTO,1551

SL\_DONT\_CALC\_CFSTAJ,0

SL\_DONT\_CALC\_ZILE\_CONCBUL,0

SL\_DONT\_EXCEED\_CONC\_DATAEND,0

SL\_EXTRAS\_CNT\_PAGE,0

SL\_FILTR\_COD\_ZILE\_CONCBUL,5091

SL\_GET\_GRAFIC\_FROM\_TP,0

SL\_ISBUGET,0

SL\_K\_NOCI,1.5

SL\_K\_ODIHNA,2

SL\_K\_PRAZDN,2

SL\_K\_SVERH\_UR1,1.5

SL\_K\_SVERH\_UR2,2

SL\_K\_VECER,0.2

SL\_LUNI\_BULETIN,6

SL\_LUNI\_CONCEDIU,3

SL\_SALARIU\_MINIMAL,18

SL\_SC\_AVANS,1293

SL\_SC\_CONCBUL,5398

SL\_SC\_FLUX,4021

SL\_SC\_GRAD,0

SL\_SC\_MATRIMONIALE,-1

SL\_SC\_MED\_STRAH\_PERS,1258

SL\_SCPF,0

SL\_SCSF,5198

SL\_SCSF\_ON5331,5198

SL\_SCSF29,5061

SL\_SCSF29\_ON5331,5198

SL\_SC\_TARIF,0

SL\_SC\_TARIF\_ORE,0

SL\_SC\_VECHIMEA,0

SL\_SC5347,1251

SL\_SFPROCENT,1

SL\_SOCFOND\_S\_VYPLAT,0

SL\_SUMA\_ZELODNEV\_PROSTOI,400

SL\_SYSFID\_AUTO\_CALC,0

SL\_SYSFID\_AUTO\_RETIN,0

SL\_SYSFID\_BULETIN,0

SL\_SYSFID\_CONCEDIU,0

SL\_SYSFID\_INDREPTARE,0

SL\_SYSFID\_LIPSURI,0

SL\_SYSFID\_LISTA\_DE\_PLATA,0

SL\_SYSFIDS2EXCLUDE\_SL\_AVTO,0

SL\_SYSFID\_TABEL\_CALC,0

SL\_SYSFID\_UVOLEN,327

SL\_TARIF\_VRED,0

SL\_TIP\_CALC\_CONC,1

SL\_TP\_USED,1

SL\_TRY\_GUESS\_ZILE\_LUCR,1

SL\_USE\_AVANS,1

SL\_USE\_NRSET\_CALCD,0

SL\_USE\_TMP\_CM\_NRSET\_INCLUDE,1

SL\_USE\_VSLRPRM\_CALCD9,1

SL\_VSLRPRM\_CALCD\_ACT\_DATA,20.01.2013

SL\_ZILE\_ORE,1

-- Текущая дата \(исп. как дата по умолчанию при создании документов\) 

-- Эту дату можно изменить в Uniacc Client - параметр "Сегодня" на панели "Период"

UN$DATACURENT,20.01.2013

-- Даты, которые можно изменить в Uniacc Client - Дата начала и конца просмотра

DOCS$BEG

DOCS$END

--

UNLANG,2

UNP1DEF\_NRSET,201

YIMC\_SCALES\_EXPORT\_SEPARATOR,.

