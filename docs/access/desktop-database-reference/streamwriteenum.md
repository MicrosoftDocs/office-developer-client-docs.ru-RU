---
title: StreamWriteEnum (Справочник по для настольных баз данных Access)
TOCTitle: StreamWriteEnum
ms:assetid: b4356999-d7a8-abfa-f6a8-6c2dd04b9257
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249861(v=office.15)
ms:contentKeyID: 48547216
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 76286fcd09e5b92f19d8dbf0e8d0419ad4c600df
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861892"
---
# <a name="streamwriteenum"></a>StreamWriteEnum

**Применимо к**: Access 2013 | Office 2013

Указывает, добавлены ли разделитель к строке, записанные в объект [потока](stream-object-ado.md) .

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
<td><p><strong>adWriteChar</strong></p></td>
<td><p>0</p></td>
<td><p>Значение, используемое по умолчанию. Записывает заданную текстовую строку (указывается с помощью параметра <em>данных</em> ) на объект <strong>Stream</strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong>adWriteLine</strong></p></td>
<td><p>1</p></td>
<td><p>Записывает текстовую строку и символ разделителя строки в объект <strong>потока</strong> . Если свойство <a href="lineseparator-property-ado.md">LineSeparator</a> не определен, командлет возвращает ошибку времени выполнения.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Эти константы нет ADO/WFC эквивалентами.

