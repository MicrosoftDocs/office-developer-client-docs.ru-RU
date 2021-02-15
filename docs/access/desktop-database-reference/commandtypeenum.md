---
title: CommandTypeEnum (справочник по базам данных Access для настольных ПК)
TOCTitle: CommandTypeEnum
ms:assetid: 9ad8f155-88a0-00eb-2855-1e1a2a677437
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249700(v=office.15)
ms:contentKeyID: 48546549
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a9114128771d4753265208dada763ac0c9f796d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296117"
---
# <a name="commandtypeenum"></a>CommandTypeEnum

**Область применения**: Access 2013, Office 2013

Указывает, как следует интерпретировать аргумент команды.

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
<td><p>Не указывает аргумент типа команды.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCmdText</strong></p></td>
<td><p>1 </p></td>
<td><p>Оценивает <a href="commandtext-property-ado.md">CommandText как</a> текстовое определение вызова команды или хранимой процедуры.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCmdTable</strong></p></td>
<td><p>2 </p></td>
<td><p>Оценивает <strong>CommandText как</strong> имя таблицы, столбцы которой возвращаются внутренним SQL запроса.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCmdStoredProc</strong></p></td>
<td><p>4 </p></td>
<td><p>Оценивает <strong>CommandText в качестве</strong> имени хранимой процедуры.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCmdUnknown</strong></p></td>
<td><p>8 </p></td>
<td><p>Значение, используемое по умолчанию. Указывает, что тип команды в свойстве <strong>CommandText</strong> неизвестна.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCmdFile</strong></p></td>
<td><p>256</p></td>
<td><p>Оценивает <strong>CommandText в</strong> качестве имени файла постоянно хранимого <a href="recordset-object-ado.md">наборов записей.</a> Используется с <strong>recordset.</strong> <a href="open-method-ado-recordset.md">Только open</a> или <a href="requery-method-ado.md">Requery.</a></p></td>
</tr>
<tr class="odd">
<td><p><strong>adCmdTableDirect</strong></p></td>
<td><p>512</p></td>
<td><p>Оценивает <strong>CommandText как</strong> имя таблицы, столбцы которой возвращаются. Используется только <strong>с Recordset.Open</strong> или <strong>Requery.</strong> Чтобы использовать метод <a href="seek-method-ado.md">Seek,</a> <strong>recordset</strong> необходимо открыть с <strong>помощью adCmdTableDirect.</strong> Это значение нельзя объединить со <a href="executeoptionenum.md">значением ExecuteOptionEnum</a> <strong>adAsyncExecute.</strong></p></td>
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

