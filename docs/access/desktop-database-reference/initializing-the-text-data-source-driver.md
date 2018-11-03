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
ms.openlocfilehash: f87c8e45cbc719ee50c017abd45a8950dc6ec7ed
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945448"
---
# <a name="initializing-the-text-data-source-driver"></a>Инициализация драйвера источника текстовых данных


**Применимо к**: Access 2013, Office 2013


Для обоих источников данных и источники данных HTML, используется один и тот же драйвер базы данных.

При установке драйвера базы данных источника данных текста программа установки записывает набор значений по умолчанию реестра Microsoft Windows в подразделы обработчики и ISAM Formats. Не изменяйте эти параметры напрямую; для добавления, удаления или изменения этих параметров с помощью программы установки для приложения. В следующих разделах инициализации и параметров ISAM Format драйвера базы данных источника данных текста.

## <a name="text-data-source-initialization-settings"></a>Параметры инициализации источника данных текста

**Модуль подключения к Access\\ISAM Formats\\текст папка** содержит параметры инициализации драйвера Acetxt.dll, который используется для внешнего доступа к файлам текстовых данных. В следующем примере приведены типичные параметры записей в этой папке.

```vb
    win32=<path>\ ACETXT.DLL 
    
    MaxScanRows=25 
    
    FirstRowHasNames=True 
    
    CharacterSet= ANSI 
    
    Format=CSVDelimited 
    
    Extensions= txt,csv,tab,asc 
    
    ExportCurrencySymbols=Yes
```

Ядро базы данных Microsoft Access использует записи в папке Text следующим образом.

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
<td><p>Win32</p></td>
<td><p>Расположение Acetxt.dll. Полный путь определяется во время установки. Значения — типа REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>MaxScanRows</p></td>
<td><p>Количество строк, просматриваемых при распознавании типы столбцов. Если задано значение 0, весь файл будет осуществляться. Значение по умолчанию равно 25. Значения — типа REG_DWORD.</p></td>
</tr>
<tr class="odd">
<td><p>FirstRowHasNames</p></td>
<td><p>Двоичное значение, указывающее, содержит ли имена столбцов первой строки в таблице. Значение 01 показывает, что во время импорта, имена столбцов берутся из первой строки.</p></td>
</tr>
<tr class="even">
<td><p>CharacterSet</p></td>
<td><p>Указывает, как хранятся страницы текста. Имеются следующие параметры:</p>
<p></p>
<ul>
<li><p>ANSI — Кодовая страница ANSI компьютера. AnsiToUnicode и UnicodeToAnsi преобразований.</p></li>
<li><p>OEM — Кодовая страница OEM компьютера. OemToUnicode и UnicodeToOem преобразований.</p></li>
<li><p>Unicode — преобразования кодовой страницы не выполняется.</p></li>
<li><p>&lt;Преобразование десятичного числа&gt; — номер кодовой страницы заданного набора знаков. Будет выполнено преобразование в Юникод и обратно.</p></li>
</ul>
<p></p>
<p>Значение по умолчанию — ANSI. Значения — типа REG_SZ.</p></td>
</tr>
<tr class="odd">
<td><p>Format</p></td>
<td><p>Может быть любым из следующих значений: TabDelimited, CSVDelimited, с разделителями (&lt;отдельный знак&gt;). Знаком разделителя в формате с разделителями может быть любой отдельный знак, за исключением двойные кавычки (&quot;). Значение по умолчанию — CSVDelimited. Значения — типа REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>Расширения</p></td>
<td><p>Расширения файлов, для просмотра при поиске текстовых данных. Значение по умолчанию — txt, csv, вкладка, asc. Значения — типа REG_SZ.</p></td>
</tr>
<tr class="odd">
<td><p>ExportCurrencySymbols</p></td>
<td><p>Двоичное значение, указывающее, является ли символ валюты соответствующие при экспорте поля валюты. Значение 01 указывает, что включен символ. Значение 00 указывает, что только числовые данные экспортировать. Значение по умолчанию — 01. Значения — типа REG_BINARY.</p></td>
</tr>
</tbody>
</table>


## <a name="text-data-source-isam-formats"></a>Текстовые форматы ISAM источника данных

**Модуль подключения к Access\\ISAM Formats\\текст** папка содержит следующие записи.

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
<td><p>Модуль</p></td>
<td><p>REG_SZ</p></td>
<td><p>Текст</p></td>
</tr>
<tr class="even">
<td><p>ExportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Текстовые файлы (*.txt; *.csv; * .tab; *.asc)</p></td>
</tr>
<tr class="odd">
<td><p>ImportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Текстовые файлы (*.txt; *.csv; * .tab; *.asc)</p></td>
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
<td><p>Импорт данных из внешнего файла в текущей базе данных. Изменение данных в текущей базе данных остаются без изменений данных во внешнем файле.</p></td>
</tr>
<tr class="even">
<td><p>ResultTextLink</p></td>
<td><p>REG_SZ</p></td>
<td><p>Создайте таблицу в текущей базе данных, которая связана с внешним файлом. Изменение данных в текущей базе данных будет изменять данные во внешнем файле.</p></td>
</tr>
<tr class="odd">
<td><p>ResultTextExport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Экспорт данных из текущей базы данных в текстовый файл. В этом будут перезаписаны данные при экспорте в существующий файл.</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P>При изменении параметров реестра Windows, необходимо выйти из и перезапустить ядро базы данных для новых параметров вступили в силу.</P>



## <a name="html-import-isam-formats"></a>Форматы ISAM импорта HTML

**Модуль подключения к Access\\ISAM Formats\\импорта HTML** папка содержит следующие записи.

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
<td><p>Модуль</p></td>
<td><p>REG_SZ</p></td>
<td><p>Текст</p></td>
</tr>
<tr class="even">
<td><p>ImportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>HTML-файлы (*.ht*)</p></td>
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
<td><p>Импорт данных из внешнего файла в текущей базе данных. Изменение данных в текущей базе данных остаются без изменений данных во внешнем файле.</p></td>
</tr>
<tr class="odd">
<td><p>ResultTextLink</p></td>
<td><p>REG_SZ</p></td>
<td><p>Создайте таблицу в текущей базе данных, которая связана с внешним файлом. Изменение данных в текущей базе данных будет изменять данные во внешнем файле.</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P>При изменении параметров реестра Windows, необходимо выйти из и перезапустить ядро базы данных для новых параметров вступили в силу.</P>



## <a name="html-export-isam-formats"></a>Форматы ISAM экспорта HTML

**Модуль подключения к Access\\ISAM Formats\\экспорта HTML** папка содержит следующие записи.

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
<td><p>Модуль</p></td>
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
<td><p>Экспорт данных из текущей базы данных в текстовый файл. В этом будут перезаписаны данные при экспорте в существующий файл.</p></td>
</tr>
<tr class="odd">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P>При изменении параметров реестра Windows, необходимо выйти из и перезапустить ядро базы данных для новых параметров вступили в силу.</P>



## <a name="customizing-the-schemaini-file-for-text-and-html-data"></a>Настройка файла Schema.ini для текста и данных HTML

Для чтения, импорта, или экспорта текстовых данных и данных HTML, необходимо создать файл Schema.ini Кроме включения сведений Text ISAM в INI-файле. Этот файл содержит особенности источника данных: формат текстового файла, как она считывается во время импорта и экспорта формат по умолчанию — для файлов. В следующих примерах показано макета для файла фиксированной ширины Filename.txt:

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

Аналогично формат для файла с разделителями задается следующим образом:

```text
    [Delimit.txt] 
    
    ColNameHeader=True 
    
    Format=Delimited() 
    
    MaxScanRows=0 
    
    CharacterSet=OEM 
    
    Col1=username char width 50 
    
    Col2=dateofbirth Date width 9
```

Если данные экспортируются в файл с разделителями, укажите формат для этого файла:

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

В примере Мой Экспорт относится к определенным экспорте; можно указать любые изменения параметров экспорта во время подключения. Этот пример также соответствует имени источника данных (DSN), который может быть передан при необходимости во время подключения. Все три раздела может быть включен в одном INI-файла.

Ядро базы данных Microsoft Access использует записи Schema.ini следующим образом.

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
<td><p>Может быть присвоено значение <strong>True</strong> (это означает, что первая запись данных задает имена столбцов) или <strong>False</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Format</p></td>
<td><p>Может быть установлено одно из следующих значений: TabDelimited, CSVDelimited, с разделителями (&lt;отдельный знак&gt;), или FixedLength. Разделитель, указанный для формата файла с разделителями может быть любой отдельный знак, за исключением двойные кавычки (&quot;).</p></td>
</tr>
<tr class="odd">
<td><p>FixedFormat</p></td>
<td><p>Только для использования при FixedLength имеет формат, это может быть установлено одно из следующих значений: значение RaggedEdge или TrueFixedLength. Значение RaggedEdge позволяет прерывать символом возврата каретки строки. Значение TrueFixedLength каждую строку, чтобы быть точное количество символов и знаков возврата каретки не в конце строки предполагается, что внедрены в поле. Если этот параметр не указан, значением по умолчанию является значение RaggedEdge.</p></td>
</tr>
<tr class="even">
<td><p>MaxScanRows</p></td>
<td><p>Указывает число строк, просматриваемых при распознавании в столбце типов данных. Если это имеет значение 0, выполняется весь файл.</p></td>
</tr>
<tr class="odd">
<td><p>CharacterSet</p></td>
<td><p>Можно задать OEM, ANSI, UNICODE или десятичное число допустимый код страницы и указывает набор знаков исходного файла.</p></td>
</tr>
<tr class="even">
<td><p>DateTimeFormat</p></td>
<td><p>Можно задать строку формата даты и времени. Если все поля даты/времени в тот же формат обрабатываются импорта и экспорта должны быть указаны в этой записи. Поддерживаются все форматы ядра базы данных Microsoft Jet за исключением AM и PM. В случае отсутствия строку формата используются параметры изображения и время краткий формат даты панели управления Windows.</p></td>
</tr>
<tr class="odd">
<td><p>CurrencySymbol</p></td>
<td><p>Указывает символ валюты, которое будет использоваться для денежных значений в текстовый файл. Примеры включают доллара ($) и интеллектуальный анализ данных. Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</p></td>
</tr>
<tr class="even">
<td><p>CurrencyPosFormat</p></td>
<td><p>Может быть установлено любое из следующих значений: символ денежной единицы перед без пробела ($1) суффикс символ валюты без пробела (1$) символ денежной единицы перед суффикс символ валюты один символ пробела ($ 1) с одним пробелом (1 $) Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</p></td>
</tr>
<tr class="odd">
<td><p>CurrencyDigits</p></td>
<td><p>Указывает количество знаков, используемых для дробной части денежной суммы. Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</p></td>
</tr>
<tr class="even">
<td><p>CurrencyNegFormat</p></td>
<td><p>Может иметь одно из следующих значений: (1) — $1 $– 1 $1 — (1$) -1$ $ 1 – $ 1 – – 1 $ – $ 1 1 – $ 1 – $ 1-1 – $ ($ 1) (1 $) знак доллара отображается для этого примера, но оно должно быть заменено соответствующим значением качестве в самой программы. Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</p></td>
</tr>
<tr class="odd">
<td><p>CurrencyThousandSymbol</p></td>
<td><p>Символ одного знака, используемый для разделения денежных значений тысячи людей в текстовый файл. Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</p></td>
</tr>
<tr class="even">
<td><p>CurrencyDecimalSymbol</p></td>
<td><p>Можно задать для любой отдельный знак, используемый для разделения целой дробная часть денежной суммы. Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</p></td>
</tr>
<tr class="odd">
<td><p>DecimalSymbol</p></td>
<td><p>Можно задать для любой отдельный знак, используемый для отделения целое число от дробная часть числа. Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</p></td>
</tr>
<tr class="even">
<td><p>NumberDigits</p></td>
<td><p>Указывает число десятичных знаков в дробной части числа. Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</p></td>
</tr>
<tr class="odd">
<td><p>NumberLeadingZeros</p></td>
<td><p>Определяет, содержат ли десятичное значение меньше 1 и больше -1 нулей; Это значение может быть False (отсутствие нуля) или True.</p></td>
</tr>
<tr class="even">
<td><p>Столбец1 Col2...</p></td>
<td><p>Список столбцов в текстовый файл для чтения. Формат этой записи должны быть: <em>Coln</em>=<em>columnName</em> тип [Width <em> #</em>] <em>columnName</em>: имена столбцов с внедренным пробелов должно заключаться в кавычки. <em>Тип</em>: бит, Byte, Short, Long, знаков после запятой, Currency, Single, Double, даты и времени. Двоичный OLE, текст или заметка. Кроме того, поддерживаются следующие типы текстовых драйверов ODBC: символ (то же, как текст) с плавающей запятой (то же, что Double) Integer (то же, что Short) LongChar (то же, что Memo) даты <em>формата даты</em> в случае типа Memo может быть маркер дополнительные формат [атрибут гиперссылка] используется для указания столбцов, которые должны быть активные URL-адреса в Microsoft Access. В случае тип Decimal введите дополнительные формат маркеры [масштабировать #] точности #] следует использовать.</p></td>
</tr>
<tr class="odd">
<td><p>TextDelimiter</p></td>
<td><p>Можно задать для любой отдельный знак, используемый для выделения строки, содержащие любое из специальных символов. Пример: &quot;ABC&quot;,&quot;xyz, компании pqr&quot;,&quot;hij&quot; при этом нет разделителем по умолчанию является двойные кавычки. Если эта запись — это строка &quot;нет&quot; затем символы не будут рассматриваться в качестве разделителей.</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> При изменении параметров файла Schema.ini необходимо выйти из и перезапустить ядро базы данных для новых параметров вступили в силу.


