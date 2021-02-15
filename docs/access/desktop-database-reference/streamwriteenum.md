---
title: StreamWriteEnum (справочник по базе данных Access для настольных ПК)
TOCTitle: StreamWriteEnum
ms:assetid: b4356999-d7a8-abfa-f6a8-6c2dd04b9257
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249861(v=office.15)
ms:contentKeyID: 48547216
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 87144e5409fb54cf0cb8f59ad4d593ab05d694a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308479"
---
# <a name="streamwriteenum"></a>StreamWriteEnum

**Область применения**: Access 2013, Office 2013

Указывает, будет ли к строке, записанной в объект Stream, будет ли к строке, записанной в [объект Stream, будет ли сепаратор строки.](stream-object-ado.md)

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
<td><p>Значение, используемое по умолчанию. Записывает указанную текстовую строку (заданную параметром <em>Data)</em> в <strong>объект Stream.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>adWriteLine</strong></p></td>
<td><p>1 </p></td>
<td><p>Записывает текстовую строку и знак сепаратора строк в объект <strong>Stream.</strong> Если свойство <a href="lineseparator-property-ado.md">LineSeparator</a> не определено, возвращается ошибка времени запуска.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Эти константы не имеют эквивалентов ADO/WFC.

