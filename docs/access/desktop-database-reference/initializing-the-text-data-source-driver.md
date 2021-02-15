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

Один и тот же драйвер базы данных используется как для текстовых источников данных, так и для источников данных HTML.

При установке драйвера базы данных источника текстовых данных программа установки записывает набор значений по умолчанию в реестр Microsoft Windows в подмайсах "Подпрограммы" и "Форматы ISAM". Не следует изменять эти параметры напрямую; используйте программу установки приложения для добавления, удаления или изменения этих параметров. В следующих разделах описаны параметры инициализации и формата ISAM для драйвера базы данных источника текстовых данных.

## <a name="text-data-source-initialization-settings"></a>Параметры инициализации источника текстовых данных

Текстовая папка **\\ ISAM \\** для средства подключения к Access включает параметры инициализации драйвера Acetxt.dll, используемой для внешнего доступа к текстовым файлам данных. Типичные параметры для записей в этой папке показаны в следующем примере.

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

Ядер баз данных Microsoft Access использует записи текстовых папок следующим образом.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Запись</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>win32</p></td>
<td><p>Расположение Acetxt.dll. Полный путь определяется во время установки. Значения имеют тип REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>MaxScanRows</p></td>
<td><p>Количество строк, сканированных при угадать типы столбцов. Если установлено 0, будет искаться весь файл. Значение по умолчанию — 25. Значения имеют тип REG_DWORD.</p></td>
</tr>
<tr class="odd">
<td><p>FirstRowHasNames</p></td>
<td><p>Двоичное значение, которое указывает, содержит ли первая строка таблицы имена столбцов. Значение 01 указывает, что во время импорта имена столбцов принимаются из первой строки.</p></td>
</tr>
<tr class="even">
<td><p>CharacterSet</p></td>
<td><p>Индикатор хранения текстовых страниц. Возможные параметры:</p>
<p></p>
<ul>
<li><p>ANSI — кодовая страница ANSI компьютера. Преобразования AnsiToUnicode и UnicodeToAnsi были сделаны.</p></li>
<li><p>OEM — кодовая страница OEM компьютера. Преобразования OemToUnicode и UnicodeToOem были сделаны.</p></li>
<li><p>Юникод — преобразования на странице кода не были сделаны.</p></li>
<li><p>&lt;десятичной номер &gt; — кодовая страница определенного набора символов. Преобразования в Юникод и из него будут сделаны.</p></li>
</ul>
<p></p>
<p>Значение по умолчанию — ANSI. Значения имеют тип REG_SZ.</p></td>
</tr>
<tr class="odd">
<td><p>Format</p></td>
<td><p>Может иметь одно из следующих символов: TabDelimited, CSVDelimited, Delimited ( &lt; single &gt; character). Односиматором в формате с делегированием может быть любой отдельный символ, кроме двойных кавычках ( &quot; ). Значение по умолчанию — CSVDelimited. Значения имеют тип REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>Расширения</p></td>
<td><p>Расширение любых файлов, которые необходимо просмотреть при поиске текстовых данных. Значение по умолчанию: txt, csv, tab, asc. Значения имеют тип REG_SZ.</p></td>
</tr>
<tr class="odd">
<td><p>ExportCurrencySymbols</p></td>
<td><p>Двоичное значение, которое указывает, включается ли соответствующий символ валюты при экспорте полей валюты. Значение 01 указывает, что символ включен. Значение 00 указывает, что экспортируются только числовая информация. Значение по умолчанию — 01. Значения имеют тип REG_BINARY.</p></td>
</tr>
</tbody>
</table>


## <a name="text-data-source-isam-formats"></a>Форматы ISAM источника текстовых данных

**Текстовая папка \\ "Форматы ISAM" \\** средства подключения Access содержит следующие записи.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя записи</p></th>
<th><p>Тип</p></th>
<th><p>Значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Engine</p></td>
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
<td><p>2 </p></td>
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
<td><p>Импорт данных из внешнего файла в текущую базу данных. Изменение данных в текущей базе данных не изменяет данные во внешнем файле.</p></td>
</tr>
<tr class="even">
<td><p>ResultTextLink</p></td>
<td><p>REG_SZ</p></td>
<td><p>Создайте таблицу в текущей базе данных, связанную с внешним файлом. Изменение данных в текущей базе данных изменит данные во внешнем файле.</p></td>
</tr>
<tr class="odd">
<td><p>ResultTextExport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Экспорт данных из текущей базы данных в текстовый файл. Этот процесс переопишет данные при экспорте в существующий файл.</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> При изменении параметров реестра Windows необходимо выйти из системы и перезапустить механизм баз данных, чтобы новые параметры вступили в силу.

## <a name="html-import-isam-formats"></a>Форматы ISAM для импорта HTML

HtmL-папка "Импорт" в формате **\\ \\ ISAM** средства подключения Access содержит следующие записи.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя записи</p></th>
<th><p>Тип</p></th>
<th><p>Значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Engine</p></td>
<td><p>REG_SZ</p></td>
<td><p>Текст</p></td>
</tr>
<tr class="even">
<td><p>ImportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>HTML-файлы (*HT)*</p></td>
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
<td><p>2 </p></td>
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
<td><p>Импорт данных из внешнего файла в текущую базу данных. Изменение данных в текущей базе данных не изменяет данные во внешнем файле.</p></td>
</tr>
<tr class="odd">
<td><p>ResultTextLink</p></td>
<td><p>REG_SZ</p></td>
<td><p>Создайте таблицу в текущей базе данных, связанную с внешним файлом. Изменение данных в текущей базе данных изменит данные во внешнем файле.</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> При изменении параметров реестра Windows необходимо выйти из системы и перезапустить механизм баз данных, чтобы новые параметры вступили в силу.

## <a name="html-export-isam-formats"></a>Форматы ISAM экспорта HTML

Папка **\\ \\ HTML Export** в формате ISAM средства подключения Access содержит следующие записи.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя записи</p></th>
<th><p>Тип</p></th>
<th><p>Значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Engine</p></td>
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
<td><p>2 </p></td>
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
<td><p>Экспорт данных из текущей базы данных в текстовый файл. Этот процесс переопишет данные при экспорте в существующий файл.</p></td>
</tr>
<tr class="odd">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> При изменении параметров реестра Windows необходимо выйти из системы и перезапустить механизм баз данных, чтобы новые параметры вступили в силу.

## <a name="customizing-the-schemaini-file-for-text-and-html-data"></a>Настройка Schema.ini для текстовых и HTML-данных

Чтобы читать, импортировать или экспортировать текст и HTML-данные, необходимо создать Schema.ini в дополнение к сведениям ISAM text в INI-файле. Schema.ini содержит особенности источника данных: форматирование текстового файла, его чтение во время импорта и формат экспорта по умолчанию для файлов. В следующих примерах покажите макет для файла фиксированной ширины, Filename.txt:

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

Аналогичным образом, формат файла с делегированием задан следующим образом:

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

Если вы экспортируете данные в текстовый файл с делениями, также укажите формат для этого файла:

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

В примере "Мой специальный экспорт" указывается определенный параметр экспорта; Вы можете указать любой вариант параметров экспорта во время подключения. Этот последний пример также соответствует имени источника данных (DSN), которое можно передать при подключении. Все три раздела формата можно включить в один INI-файл.

Яд баз данных Microsoft Access использует Schema.ini записи следующим образом.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Запись</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ColNameHeader</p></td>
<td><p>Может иметь либо <strong>true</strong> (указывая, что первая запись данных указывает имена столбцов) или <strong>False</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Format</p></td>
<td><p>Можно установить одно из следующих значений: TabDelimited, CSVDelimited, Delimited ( &lt; single &gt; character) или FixedLength. Для формата файлов с делегированием заданы отдельные знаки, кроме двойных кавычках ( &quot; ).</p></td>
</tr>
<tr class="odd">
<td><p>FixedFormat</p></td>
<td><p>Только если формат имеет значение FixedLength, можно установить одно из следующих значений: RaggedEdge или TrueFixedLength. RaggedEdge позволяет завершать строки символом возврата каретки. TrueFixedLength требует, чтобы каждая строка была точным количеством символов, а любые символы возврата каретки, не вложенные в границу строки, должны быть внедрены в поле. Если этого параметра нет, значение по умолчанию — RaggedEdge.</p></td>
</tr>
<tr class="even">
<td><p>MaxScanRows</p></td>
<td><p>Указывает количество строк, которые будут сканироваться при угадать типы данных столбцов. Если установлено 0, поиск будет искаться во всем файле.</p></td>
</tr>
<tr class="odd">
<td><p>CharacterSet</p></td>
<td><p>Можно указать OEM, ANSI, UNICODE или десятичной кодировку допустимой кодировки, а также указать кодировку для исходных файлов.</p></td>
</tr>
<tr class="even">
<td><p>DateTimeFormat</p></td>
<td><p>Можно установить строку формата, указывающее даты и время. Эта запись должна быть указана, если все поля даты и времени в импорте/экспорте обрабатываются в одном формате. Поддерживаются все форматы ядер ядер баз данных Microsoft Jet, кроме AM и PM. При отсутствии строки формата используются краткие параметры даты и времени панели управления Windows.</p></td>
</tr>
<tr class="odd">
<td><p>CurrencySymbol</p></td>
<td><p>Указывает символ валюты, используемый для значений валюты в текстовом файле. Примеры: знак доллара ($) и dm. Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</p></td>
</tr>
<tr class="even">
<td><p>CurrencyPosFormat</p></td>
<td><p>Можно установить любое из следующих значений: префикс символа валюты без суффикса символа разделения ($1) без префикса символа разделения (1$) валюты с одним символом разделения символов ($ 1) с одним разделением символов (1 $). Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</p></td>
</tr>
<tr class="odd">
<td><p>CurrencyDigits</p></td>
<td><p>Указывает количество цифр, используемых для дробной части валюты. Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</p></td>
</tr>
<tr class="even">
<td><p>CurrencyNegFormat</p></td>
<td><p>Может иметь одно из следующих значений: ($1) –$1 $–1 $1– (1$) –1$ 1–$ 1$– –1 $ 1 $– 1– $ –1– $ –1– $ ($ 1) ($ 1 $) Знак доллара отображается в этом примере, но его следует заменить соответствующим значением CurrencySymbol в фактической программе. Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</p></td>
</tr>
<tr class="odd">
<td><p>CurrencyThousandSymbol</p></td>
<td><p>Указывает символ, который будет использоваться для разделения значений валюты на тысячи в текстовом файле. Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</p></td>
</tr>
<tr class="even">
<td><p>CurrencyDecimalSymbol</p></td>
<td><p>Можно установить любой отдельный символ, используемый для отделения целого от дробной части валюты. Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</p></td>
</tr>
<tr class="odd">
<td><p>DecimalSymbol</p></td>
<td><p>Можно установить любой отдельный символ, используемый для отделять это число от дробной части числа. Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</p></td>
</tr>
<tr class="even">
<td><p>NumberDigits</p></td>
<td><p>Указывает количество десятичных цифр в дробной части числа. Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</p></td>
</tr>
<tr class="odd">
<td><p>NumberLeadingZeros</p></td>
<td><p>Указывает, должно ли десятичной заданное значение меньше 1 и больше –1 содержать нулей в 1; это значение может иметь значение False (без нулей в окнах в окнах) или True.</p></td>
</tr>
<tr class="even">
<td><p>Col1, Col2, ...</p></td>
<td><p>Перечисляет столбцы в текстовом файле для чтения. Формат этой записи: <em>Coln</em> = <em>columnName</em> type [Width <em>#</em> ] <em>columnName</em>: Column names with embedded spaces should be enclosed in quotation marks. <em>тип:</em>может быть бит, byte, short, Long, Decimal, Currency, Single, Double, DateTime. Двоичный файл, OLE, текст или memo. Кроме того, поддерживаются следующие типы текстовых драйверов ODBC: Char (такой же, как Text) Float (то же, что и Double) Integer (то же, что и Short) LongChar (то же, что и Memo) <em>Формат</em> даты даты В случае с memo-типом можно использовать дополнительный маркер формата [гиперссылка атрибута] для указания столбцов, которые должны быть активными URL-адресами в Microsoft Access. В случае десятичных знаков следует использовать дополнительные маркеры формата [Scale #] Precision #] (Точность).</p></td>
</tr>
<tr class="odd">
<td><p>TextDelimiter</p></td>
<td><p>Можно установить любой отдельный символ, используемый для разграничия строк, содержащих любые другие специальные символы. Например, &quot;abc &quot; , &quot; xyz,pqr &quot; , &quot; hij If this entry is not present &quot; the default delimiter is a double quote. Если эта запись не является строкой, никакие символы не будут рассматриваться &quot; &quot; как разлицы.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> При изменении Schema.ini файлов необходимо выйти из системы и перезапустить механизм баз данных, чтобы новые параметры вступили в силу.


