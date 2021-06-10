---
title: ExecuteOptionEnum (Ссылка на настольные базы данных)
TOCTitle: ExecuteOptionEnum
ms:assetid: bd6d44a3-e471-7aa0-3e65-6775334de2ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249915(v=office.15)
ms:contentKeyID: 48547438
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: febeb3b52eb579647c995b01d6723a5c1f1b0c1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293247"
---
# <a name="executeoptionenum"></a>ExecuteOptionEnum

**Область применения**: Access 2013, Office 2013

Указывает, как поставщик должен выполнять команду.

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
<td><p><strong>adAsyncExecute</strong></p></td>
<td><p>0x10</p></td>
<td><p>Указывает, что команда должна выполняться асинхронно. Это значение нельзя сочетать с <a href="commandtypeenum.md">значением CommandTypeEnum</a> <strong>adCmdTableDirect.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>adAsyncFetch</strong></p></td>
<td><p>0x20</p></td>
<td><p>Указывает, что оставшиеся строки после первоначального количества, указанного в свойстве <a href="cachesize-property-ado.md">CacheSize,</a> должны быть извлечены асинхронно.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adAsyncFetchNonBlocking</strong></p></td>
<td><p>0x40</p></td>
<td><p>Указывает, что основной поток никогда не блокируется при ирисовке. Если запрашиваемая строка не была извлечена, текущая строка автоматически перемещается в конец файла.</p><p>Если открыть набор <a href="recordset-object-ado.md">записей</a> из <a href="stream-object-ado.md">потока,</a> содержащего постоянно хранимый <strong>Recordset,</strong> <strong>adAsyncFetchNonBlocking</strong> не будет иметь эффекта; операция будет синхронной и блокирующей. <strong>adAsynchFetchNonBlocking</strong> не влияет, когда для открытия <strong>recordset</strong>используется параметр <a href="commandtypeenum.md">adCmdTableDirect.</a></p></td>
</tr>
<tr class="even">
<td><p><strong>adExecuteNoRecords</strong></p></td>
<td><p>0x80</p></td>
<td><p>Указывает, что командный текст является командной или сохраненной процедурой, которая не возвращает строки (например, команду, которая вставляет только данные). Если какие-либо строки извлекаются, они отбрасываются и не возвращаются. <strong>adExecuteNoRecords</strong> может передаваться только в качестве необязательных параметров <strong>методу Командное</strong> или <strong>Выполнение</strong> <strong>подключения.</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>adExecuteStream</strong></p></td>
<td><p>0x400</p></td>
<td><p>Указывает, что результаты выполнения команд должны возвращаться в качестве потока. <strong>adExecuteStream</strong> может передаваться только в качестве необязательных параметров <strong>методу Командное</strong> <strong>выполнение.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>adExecuteRecord</strong></p></td>
<td><p><br />
</p></td>
<td><p>Указывает, что <strong>CommandText</strong> является командной или сохраненной процедурой, возвращаемой одной строкой, которая должна быть возвращена в качестве объекта <strong>Record.</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>adOptionUnspecified</strong></p></td>
<td><p>–1</p></td>
<td><p>Указывает, что команда не указана.</p></td>
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
<td><p>AdoEnums.ExeOption.ASYNCEXECUTE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ExeOption.ASYNCFETCH</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ExeOption.ASYNCFETCHNONBLOCKING</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ExeOption.NORECORDS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ExeCuteOption.UNSPECIFIED</p></td>
</tr>
</tbody>
</table>

