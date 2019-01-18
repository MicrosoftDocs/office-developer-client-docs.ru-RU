---
title: CommandTypeEnum (Справочник по для настольных баз данных Access)
TOCTitle: CommandTypeEnum
ms:assetid: 9ad8f155-88a0-00eb-2855-1e1a2a677437
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249700(v=office.15)
ms:contentKeyID: 48546549
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a9114128771d4753265208dada763ac0c9f796d1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714278"
---
# <a name="commandtypeenum"></a>CommandTypeEnum

**Применимо к**: Access 2013, Office 2013

Указывает, как интерпретировать аргумент команды.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adCmdUnspecified</strong></p></td>
<td><p>–1</p></td>
<td><p>Не указан аргумент типа команды.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCmdText</strong></p></td>
<td><p>1</p></td>
<td><p>Оценивает <a href="commandtext-property-ado.md">CommandText</a> как текстовое определения вызова команды или хранимой процедуры.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCmdTable</strong></p></td>
<td><p>2</p></td>
<td><p>Оценивает <strong>CommandText</strong> как имя таблицы, столбцы возвращаются с внутренними запрос SQL.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCmdStoredProc</strong></p></td>
<td><p>4</p></td>
<td><p>Оценивает <strong>CommandText</strong> как имя хранимой процедуры.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCmdUnknown</strong></p></td>
<td><p>8</p></td>
<td><p>Значение, используемое по умолчанию. Указывает, что тип команды в свойстве <strong>CommandText</strong> не известен.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCmdFile</strong></p></td>
<td><p>256</p></td>
<td><p>Оценивает <strong>CommandText</strong> как имя файла постоянно хранимых <a href="recordset-object-ado.md">набора записей</a>. Используется с <strong>набора записей.</strong> <a href="open-method-ado-recordset.md">Open</a> или только <a href="requery-method-ado.md">повторный запрос</a> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCmdTableDirect</strong></p></td>
<td><p>512</p></td>
<td><p>Оценивает <strong>CommandText</strong> как имя таблицы, столбцы возвращаются все. Используется только с <strong>Recordset.Open</strong> или <strong>повторный запрос</strong> . Использование метода <a href="seek-method-ado.md">Seek</a> , необходимо открыть <strong>набора записей</strong> с <strong>adCmdTableDirect</strong>. Это значение не может быть вместе с значение <a href="executeoptionenum.md">ExecuteOptionEnum</a> <strong>adAsyncExecute</strong>.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Пакет: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.CommandType.UNSPECIFIED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CommandType.TEXT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CommandType.TABLE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CommandType.STOREDPROC</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CommandType.UNKNOWN</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CommandType.FILE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CommandType.TABLEDIRECT</p></td>
</tr>
</tbody>
</table>

