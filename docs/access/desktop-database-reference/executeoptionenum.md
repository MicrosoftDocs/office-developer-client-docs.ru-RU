---
title: ExecuteOptionEnum (Справочник по для настольных баз данных Access)
TOCTitle: ExecuteOptionEnum
ms:assetid: bd6d44a3-e471-7aa0-3e65-6775334de2ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249915(v=office.15)
ms:contentKeyID: 48547438
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 51c5ab78c4ea49ade7fd2b6972aa3753b0c6df09
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862312"
---
# <a name="executeoptionenum"></a>ExecuteOptionEnum

**Применимо к**: Access 2013 | Office 2013

Указывает, как поставщик должен выполнить команду.

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
<td><p>Указывает, что будет выполняться асинхронно. Это значение не может быть вместе с значение <a href="commandtypeenum.md">CommandTypeEnum</a> <strong>adCmdTableDirect</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adAsyncFetch</strong></p></td>
<td><p>0x20</p></td>
<td><p>Указывает, что оставшиеся строки после начального количества, указанных в свойстве <a href="cachesize-property-ado.md">CacheSize</a> должны быть получены асинхронно.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adAsyncFetchNonBlocking</strong></p></td>
<td><p>0x40</p></td>
<td><p>Указывает, что основной поток не блокируется при получении. Если не был получен запрашиваемый строку, текущей строки автоматически перемещается в конец файла.</p><p>При открытии <a href="recordset-object-ado.md">набора записей</a> из <a href="stream-object-ado.md">потока</a> , содержащий постоянно сохраненных <strong>записей</strong> <strong>adAsyncFetchNonBlocking</strong> не будет иметь эффекта. Операция будет синхронная и блокировки. <strong>adAsynchFetchNonBlocking</strong> не оказывает влияния при использовании параметра <a href="commandtypeenum.md">adCmdTableDirect</a> для открытия <strong>набора записей</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adExecuteNoRecords</strong></p></td>
<td><p>0x80</p></td>
<td><p>Указывает, что текст команды команду или хранимую процедуру, которая не возвращает строки (например, команды, только вставляет данные). Если извлекаются все строки, они удалены и не возвращается. <strong>adExecuteNoRecords</strong> можно только передаваться как необязательный параметр <strong>команда</strong> или метод <strong>Execute</strong> <strong>подключения</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>adExecuteStream</strong></p></td>
<td><p>0x400</p></td>
<td><p>Указывает, что результаты выполнения команды должны возвращаться в виде потока. <strong>adExecuteStream</strong> могут передаваться только как необязательный параметр для метода <strong>Execute</strong> <strong>команды</strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong>adExecuteRecord</strong></p></td>
<td><p><br />
</p></td>
<td><p>Указывает, что <strong>CommandText</strong> команду или хранимую процедуру, возвращающую одной строки, которые должны быть возвращены как объект <strong>записи</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOptionUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Указывает, что команда не определено.</p></td>
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
<th><p>Constant</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.ExecuteOption.ASYNCEXECUTE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ExecuteOption.ASYNCFETCH</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ExecuteOption.ASYNCFETCHNONBLOCKING</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ExecuteOption.NORECORDS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ExecuteOption.UNSPECIFIED</p></td>
</tr>
</tbody>
</table>

