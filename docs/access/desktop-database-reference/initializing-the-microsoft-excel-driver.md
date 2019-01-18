---
title: Инициализация драйвера Microsoft Excel
TOCTitle: Initializing the Microsoft Excel driver
ms:assetid: 06c7f823-8e74-0811-cc00-e6b32075ef11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844939(v=office.15)
ms:contentKeyID: 48543054
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032159
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 12fb79f459024ed113007e6f764945ca9564cb3c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712934"
---
# <a name="initializing-the-microsoft-excel-driver"></a>Инициализация драйвера Microsoft Excel

**Применимо к**: Access 2013 | Office 2013

При установке драйвера Excel, программа установки записывает набор значений по умолчанию в реестре Windows в подразделах обработчики и ISAM Formats. Не изменяйте эти параметры напрямую; для добавления, удаления или изменения этих параметров с помощью программы установки для приложения. В следующих разделах инициализации и параметров ISAM Format драйвера базы данных Microsoft Excel.

## <a name="excel-initialization-settings"></a>Параметры инициализации Excel

**Модуль подключения к Access\\обработчики\\Excel** папка содержит параметры инициализации драйвера Aceexcl.dll, который используется для внешнего доступа к лист Microsoft Excel. В следующем примере приведены типичные параметры записей в этой папке.

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

Ядро базы данных Microsoft Access записи папки Excel используются следующим образом.

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
<td><p>Расположение msexcl40.dll. Полный путь определяется во время установки. Значения — типа REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>TypeGuessRows</p></td>
<td><p>Количество строк для проверки типа данных. Тип данных определяется максимальное количество типов данных. Если имеется набор функций, тип данных определяется в следующем порядке: номер, валюта, дата, текст, логическое значение. Если обнаружены данные, которые не соответствует типу данных, указанному для столбца, он возвращается как значение <strong>Null</strong> . При импорте Если столбец имеет смешанный тип данных, столбец целиком приводится в соответствии с параметром ImportMixedTypes. По умолчанию число строк для проверки — 8. Значения — типа REG_DWORD.</p></td>
</tr>
<tr class="odd">
<td><p>ImportMixedTypes</p></td>
<td><p>Может иметь значение MajorityType или текст. Если параметр имеет значение MajorityType, столбцы смешанный типы данных приводится к типу данных основной при импорте. Если установлено значение Text, столбцы mixed типы данных приводится в текст при импорте. Значение по умолчанию — текст. Значения — типа REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>Значение параметра AppendBlankRows</p></td>
<td><p>Добавлен номер пустые строки для добавления в конец версии 3.5 или листа версии 4.0 перед новыми данными. Например, если значение параметра AppendBlankRows равно 4, Microsoft Jet добавляет 4 пустые строки в конец рабочего листа перед добавлением строки, содержащие данные. Целые значения для этого параметра можно в диапазоне от 0 до 16; значение по умолчанию — 01 (добавляется один дополнительный ряд). Значения — типа REG_DWORD.</p></td>
</tr>
<tr class="odd">
<td><p>FirstRowHasNames</p></td>
<td><p>Двоичное значение, указывающее, содержит ли имена столбцов первой строки в таблице. Значение 01 показывает, что во время импорта, имена столбцов берутся из первой строки. Значение 00 указывает не имена столбцов в первой строке; имена столбцов отображаются в виде F1, F2, F3 и т. д. Значение по умолчанию — 01. Значения — типа REG_BINARY.</p></td>
</tr>
</tbody>
</table>

<br/>

**Модуль подключения к Access\\обработчики\\Excel 8.0** папка содержит следующие записи, которые применяются к Microsoft Excel 97.

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
<td><p>Excel</p></td>
</tr>
<tr class="even">
<td><p>ExportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Microsoft Excel 97-2000 (*.xls)</p></td>
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
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>ResultTextExport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Экспорт данных из текущей базы данных в файл Microsoft Excel 97. В этом будут перезаписаны данные при экспорте в существующий файл.</p></td>
</tr>
<tr class="odd">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> При изменении параметров реестра Windows, необходимо выйти из и перезапустить ядро базы данных для новых параметров вступили в силу.

## <a name="see-also"></a>См. также

- [С помощью параметра TypeGuessRows драйвера Excel](https://support.office.com/en-us/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b?ui=en-US&rs=en-US&ad=US)
