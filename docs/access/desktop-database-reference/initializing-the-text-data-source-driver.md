---
title: Инициализация драйвера источника текстовых данных
TOCTitle: Initializing the Text Data Source driver
ms:assetid: cba0864e-5f94-bf43-4708-b1981e3acaff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834391(v=office.15)
ms:contentKeyID: 48547718
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032166
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2e76cc7d6b5254f2347e2264b0588ee1df643d05
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291423"
---
# <a name="initializing-the-text-data-source-driver"></a>Инициализация драйвера источника текстовых данных

**Область применения**: Access 2013, Office 2013

Один и тот же драйвер базы данных используется как для источников текстовых данных, так и для HTML-источников данных.

При установке драйвера базы данных Text Data Source программа установки записывает набор значений по умолчанию в реестр Microsoft Windows в подкайлах Engines и ISAM Formats. Не следует изменять эти параметры напрямую; используйте программу установки для приложения, чтобы добавить, удалить или изменить эти параметры. В следующих разделах описываются параметры инициализации и формата ISAM для драйвера базы данных Text Data Source.

## <a name="text-data-source-initialization-settings"></a>Параметры инициализации источника текстовых данных

Текстовая папка **Access Connectivity Engine \\ ISAM \\ Formats** включает параметры инициализации драйвера Acetxt.dll, используемой для внешнего доступа к текстовым файлам данных. Типичные параметры для записей в этой папке показаны в следующем примере.

```vb
    win32=<path>\ ACETXT.DLL 
    
    MaxScanRows=25 
    
    FirstRowHasNames=True 
    
    CharacterSet= ANSI 
    
    Format=CSVDelimited 
    
    Extensions= txt,csv,tab,asc 
    
    ExportCurrencySymbols=Yes
```

<br/>

В движке базы данных Microsoft Access используются записи текстовых папок следующим образом.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Запись</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>win32</p></td>
<td><p>Расположение Acetxt.dll. Полный путь определяется во время установки. Значения имеют тип REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>MaxScanRows</p></td>
<td><p>Количество строк, которые необходимо отсканировать при угадывке типов столбцов. Если установлено 0, весь файл будет искаться. По умолчанию — 25. Значения имеют тип REG_DWORD.</p></td>
</tr>
<tr class="odd">
<td><p>FirstRowHasNames</p></td>
<td><p>Двоичное значение, которое указывает, содержит ли первая строка таблицы имена столбцов. Значение 01 указывает, что во время импорта из первой строки будут взяты имена столбцов.</p></td>
</tr>
<tr class="even">
<td><p>CharacterSet</p></td>
<td><p>Индикатор хранения текстовых страниц. Возможные параметры:</p>
<p></p>
<ul>
<li><p>ANSI — страница кода ANSI компьютера. Преобразования AnsiToUnicode и UnicodeToAnsi сделаны.</p></li>
<li><p>OEM — страница кода OEM машины. Преобразования OemToUnicode и UnicodeToOem сделаны.</p></li>
<li><p>Unicode — преобразования кода не были сделаны.</p></li>
<li><p>&lt;десятичной номер &gt; — номер страницы кода определенного набора символов. Преобразования в Юникод и из него будут сделаны.</p></li>
</ul>
<p></p>
<p>По умолчанию — ANSI. Значения имеют тип REG_SZ.</p></td>
</tr>
<tr class="odd">
<td><p>Формат</p></td>
<td><p>Может быть любой из следующих: TabDelimited, CSVDelimited, Delimited &lt; (один &gt; символ). Делимитер с одним персонажем в формате Delimited может быть любым одним персонажем, за исключением двойной кавычка ( &quot; ). По умолчанию CSVDelimited. Значения имеют тип REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>Расширения</p></td>
<td><p>Расширение любых файлов, которые необходимо просмотреть при поиске текстовых данных. По умолчанию это txt, csv, tab, asc. Значения имеют тип REG_SZ.</p></td>
</tr>
<tr class="odd">
<td><p>ExportCurrencySymbols</p></td>
<td><p>Двоичное значение, которое указывает, включен ли соответствующий символ валюты при экспорте валютных полей. Значение 01 указывает, что символ включен. Значение 00 указывает, что экспортируются только числовая информация. Значение по умолчанию — 01. Значения имеют тип REG_BINARY.</p></td>
</tr>
</tbody>
</table>


## <a name="text-data-source-isam-formats"></a>Форматы ISAM источника текстовых данных

**Текстовая папка \\ IsAM \\ Formats IsAM Engine Access Connectivity Engine** содержит следующие записи.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя входа</p></th>
<th><p>Тип</p></th>
<th><p>Значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Двигатель</p></td>
<td><p>REG_SZ</p></td>
<td><p>Текст</p></td>
</tr>
<tr class="even">
<td><p>ExportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Текстовые файлы (*.txt; *.csv; *.tab; *.asc)</p></td>
</tr>
<tr class="odd">
<td><p>ImportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Текстовые файлы (*.txt; *.csv; *.tab; *.asc)</p></td>
</tr>
<tr class="even">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="odd">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>IsamType</p></td>
<td><p>REG_DWORD</p></td>
<td><p>2</p></td>
</tr>
<tr class="odd">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>ResultTextImport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Импорт данных из внешнего файла в текущую базу данных. Изменение данных в текущей базе данных не изменит данные во внешнем файле.</p></td>
</tr>
<tr class="even">
<td><p>ResultTextLink</p></td>
<td><p>REG_SZ</p></td>
<td><p>Создание таблицы в текущей базе данных, связанной с внешним файлом. Изменение данных в текущей базе данных изменит данные во внешнем файле.</p></td>
</tr>
<tr class="odd">
<td><p>ResultTextExport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Экспорт данных из текущей базы данных в текстовый файл. Этот процесс переопишет данные, если они будут экспортироваться в существующий файл.</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> При изменении параметров Windows реестра необходимо выйти и перезапустить двигатель базы данных, чтобы новые параметры вступили в силу.

## <a name="html-import-isam-formats"></a>Форматы HTML-импорта ISAM

Папка **\\ \\ HTML Import в** движке ISAM Для подключения к системе подключения к доступу содержит следующие записи.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя входа</p></th>
<th><p>Тип</p></th>
<th><p>Значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Двигатель</p></td>
<td><p>REG_SZ</p></td>
<td><p>Текст</p></td>
</tr>
<tr class="even">
<td><p>ImportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>HTML Files *(.ht)*</p></td>
</tr>
<tr class="odd">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>IsamType</p></td>
<td><p>REG_DWORD</p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>ResultTextImport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Импорт данных из внешнего файла в текущую базу данных. Изменение данных в текущей базе данных не изменит данные во внешнем файле.</p></td>
</tr>
<tr class="odd">
<td><p>ResultTextLink</p></td>
<td><p>REG_SZ</p></td>
<td><p>Создание таблицы в текущей базе данных, связанной с внешним файлом. Изменение данных в текущей базе данных изменит данные во внешнем файле.</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> При изменении параметров Windows реестра необходимо выйти и перезапустить двигатель базы данных, чтобы новые параметры вступили в силу.

## <a name="html-export-isam-formats"></a>Форматы HTML-экспорта ISAM

Папка **\\ \\ HTML Export в** движке ISAM Engine ISAM Для подключения к доступу содержит следующие записи.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя входа</p></th>
<th><p>Тип</p></th>
<th><p>Значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Двигатель</p></td>
<td><p>REG_SZ</p></td>
<td><p>Текст</p></td>
</tr>
<tr class="even">
<td><p>ExportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>HTML-файлы (*.htm)</p></td>
</tr>
<tr class="odd">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="odd">
<td><p>IsamType</p></td>
<td><p>REG_DWORD</p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>ResultTextExport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Экспорт данных из текущей базы данных в текстовый файл. Этот процесс переопишет данные, если они будут экспортироваться в существующий файл.</p></td>
</tr>
<tr class="odd">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> При изменении параметров Windows реестра необходимо выйти и перезапустить двигатель базы данных, чтобы новые параметры вступили в силу.

## <a name="customizing-the-schemaini-file-for-text-and-html-data"></a>Настройка файла Schema.ini для текстовых и HTML-данных

Чтобы читать, импортировать или экспортировать текстовые и HTML-данные, необходимо создать файл Schema.ini, а также включив в него сведения об ISAM text .ini файле. Schema.ini содержит особенности источника данных: форматирование текстового файла, его чтение во время импорта и формат экспорта по умолчанию для файлов. В следующих примерах покажите макет файла с фиксированной шириной, Filename.txt:

```text
    [Filename.txt] 
    
    ColNameHeader=False 
    
    Format=FixedLength 
    
    FixedFormat= RaggedEdge 
    
    MaxScanRows=25 
    
    CharacterSet=OEM 
    
    Col1=columnname Char Width 24 
    
    Col2=columnname2 Date Width 9 
    
    Col3=columnname7 Float Width 10 
    
    Col4=columnname8 Integer Width 10 
    Col5=columnname9 LongChar Width 10
```

<br/>

Кроме того, формат делимитного файла указывается следующим образом:

```text
    [Delimit.txt] 
    
    ColNameHeader=True 
    
    Format=Delimited() 
    
    MaxScanRows=0 
    
    CharacterSet=OEM 
    
    Col1=username char width 50 
    
    Col2=dateofbirth Date width 9
```

<br/>

Если вы экспортируете данные в делимитированный текстовый файл, укажите формат этого файла:

```text
    [Export: My Special Export] 
    
    ColNameHeader=True 
    
    Format=TabDelimited 
    
    MaxScanRows=25 
    
    CharacterSet=OEM 
    
    DateTimeFormat=mm.dd.yy.hh.mm.ss 
    
    CurrencySymbol=Dm 
    
    CurrencyPosFormat=0 
    
    CurrencyDigits=2 
    
    CurrencyNegFormat=0 
    
    CurrencyThousandSymbol=, 
    
    CurrencyDecimalSymbol=. 
    
    DecimalSymbol=, 
    
    NumberDigits=2 
    
    NumberLeadingZeros=0 
    
    TextDelimeter="
```

<br/>

Пример "Мой специальный экспорт" относится к определенному варианту экспорта; вы можете указать любые варианты экспорта во время подключения. Этот последний пример также соответствует имени источника данных (DSN), которое может быть дополнительно передано во время подключения. Все три раздела формата могут быть включены в один .ini файл.

Движок базы данных Microsoft Access использует Schema.ini записей следующим образом.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Запись</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ColNameHeader</p></td>
<td><p>Можно установить как <strong>True</strong> (указывая, что первая запись данных указывает имена столбцов), так и <strong>False</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Формат</p></td>
<td><p>Можно установить одно из следующих значений: TabDelimited, CSVDelimited, Delimited &lt; (один символ) или &gt; FixedLength. Делимитер, указанный для формата делимитированный файл, может быть любым одним персонажем, за исключением двойной кавычка ( &quot; ).</p></td>
</tr>
<tr class="odd">
<td><p>FixedFormat</p></td>
<td><p>Только если формат fixedLength, его можно установить к одному из следующих значений: RaggedEdGe или TrueFixedLength. RaggedEdge позволяет прекращать строки с помощью символа Carriage Return. TrueFixedLength требует, чтобы каждая строка была точным числом символов, и предполагается, что любые символы возвращения кареты, не на границе строки, будут встроены в поле. Если этого параметра нет, по умолчанию значение RaggedEdge.</p></td>
</tr>
<tr class="even">
<td><p>MaxScanRows</p></td>
<td><p>Указывает количество строк, которые необходимо отсканировать при угадывке типов данных столбцов. Если это установлено до 0, весь файл будет искаться.</p></td>
</tr>
<tr class="odd">
<td><p>CharacterSet</p></td>
<td><p>Можно установить OEM, ANSI, UNICODE или десятичной номер допустимой страницы кода и указать набор символов исходных файлов.</p></td>
</tr>
<tr class="even">
<td><p>DateTimeFormat</p></td>
<td><p>Можно установить строку формата, указывающее даты и время. Эта запись должна быть указана, если все поля даты и времени в импорте/экспорте обрабатываются в одном формате. Поддерживаются все форматы двигателей базы данных Microsoft Jet, кроме AM и PM. При отсутствии строки формата используется Windows панели управления краткое изображение даты и параметры времени.</p></td>
</tr>
<tr class="odd">
<td><p>CurrencySymbol</p></td>
<td><p>Указывает символ валюты, который будет использоваться для значений валюты в текстовом файле. Примеры включают знак доллара ($) и dm. Если эта запись отсутствует, используется значение по умолчанию Windows панели управления.</p></td>
</tr>
<tr class="even">
<td><p>CurrencyPosFormat</p></td>
<td><p>Можно установить любое из следующих значений: префикс символа валюты без разделения ($1) Суффикс символа валюты без префикса символа разделения (1$) с суффиксом символа разделения символа ($ 1) с разделением одного символа (1 $) Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</p></td>
</tr>
<tr class="odd">
<td><p>CurrencyDigits</p></td>
<td><p>Указывает количество цифр, используемых для дробной части суммы валюты. Если эта запись отсутствует, используется значение по умолчанию Windows панели управления.</p></td>
</tr>
<tr class="even">
<td><p>CurrencyNegFormat</p></td>
<td><p>Может быть одним из следующих значений: ($1) -$1 $-1 $1 - (1$) -1$1-$ 1$- -1 $-1 $- $1 - $1 - $1 - $1 ($1) Знак доллара показан для целей этого примера, но его следует заменить соответствующим значением CurrencySymbol в фактической программе. Если эта запись отсутствует, используется значение по умолчанию Windows панели управления.</p></td>
</tr>
<tr class="odd">
<td><p>CurrencyThousandSymbol</p></td>
<td><p>Указывает символ одного символа, который используется для разделения значений валюты на тысячи в текстовом файле. Если эта запись отсутствует, используется значение по умолчанию Windows панели управления.</p></td>
</tr>
<tr class="even">
<td><p>CurrencyDecimalSymbol</p></td>
<td><p>Можно установить для любого отдельного символа, который используется для отделить целое от дробной части суммы валюты. Если эта запись отсутствует, используется значение по умолчанию Windows панели управления.</p></td>
</tr>
<tr class="odd">
<td><p>DecimalSymbol</p></td>
<td><p>Можно установить для любого отдельного символа, который используется для отделить целый ряд от дробной части номера. Если эта запись отсутствует, используется значение по умолчанию Windows панели управления.</p></td>
</tr>
<tr class="even">
<td><p>NumberDigits</p></td>
<td><p>Указывает количество десятичных цифр в дробной части номера. Если эта запись отсутствует, используется значение по умолчанию Windows панели управления.</p></td>
</tr>
<tr class="odd">
<td><p>NumberLeadingZeros</p></td>
<td><p>Указывает, должно ли десятичная величина меньше 1 и больше -1 содержать ведущие нули; это значение может быть false (без ведущих нулей) или True.</p></td>
</tr>
<tr class="even">
<td><p>Col1, Col2, ...</p></td>
<td><p>Списки столбцов в текстовом файле для чтения. Формат этой записи должен быть: <em>тип coln</em> = columnName [Width ]<em>columnName:</em> Имена столбцов со встроенными пробелами должны быть заключены <em>#</em> в кавычках. <em></em> <em>тип:</em>Может быть Бит, Byte, Short, Long, Decimal, Currency, Single, Double, DateTime. Двоичный, OLE, текст или памятка. Кроме того, поддерживаются следующие типы текстовых драйверов ODBC: Для указания столбцов, которые должны быть активными URL-адресами в Microsoft Access, поддерживаются следующие типы текстовых драйверов ODBC: Char (такой же, как Text) Float (так же, как и Double) Формат даты LongChar (так же, как и формат Memo). Для указания столбцов, которые должны быть активными URL-адресами в Microsoft Access, можно использовать дополнительный маркер формата. <em></em> В случае десятичных типов необходимо использовать дополнительные маркеры формата [Scale #] Precision #]</p></td>
</tr>
<tr class="odd">
<td><p>TextDelimiter</p></td>
<td><p>Можно установить для любого отдельного символа, используемого для делимитации строк, содержащих любые другие специальные символы. Например, &quot;ABC, &quot; &quot; xyz, pqr, hij Если эта запись не представлена, делимитер по умолчанию &quot; является двойной &quot; &quot; цитатой. Если эта запись не является &quot; строкой, никакие символы не будут &quot; рассматриваться как делимитеры.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> При изменении Schema.ini параметров файла необходимо выйти и перезапустить двигатель базы данных, чтобы новые параметры вступили в силу.


