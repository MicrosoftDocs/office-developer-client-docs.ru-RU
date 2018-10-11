---
title: StreamOpenOptionsEnum
TOCTitle: StreamOpenOptionsEnum
ms:assetid: d4bbd6be-41f1-cdf2-9d8f-b77ce83fb88e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250069(v=office.15)
ms:contentKeyID: 48547951
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3998f41c1400a2870633f19228cbf73189e9527a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481907"
---
# <a name="streamopenoptionsenum"></a>StreamOpenOptionsEnum


**Применимо к**: Access 2013 | Office 2013

Задает параметры открытия объект [Stream](stream-object-ado.md) . Значения может использоваться совместно с операция OR.

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
<td><p><strong>adOpenStreamAsync</strong></p></td>
<td><p>1</p></td>
<td><p>Открывает объект <strong>Stream</strong> в асинхронном режиме.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStreamFromRecord</strong></p></td>
<td><p>4</p></td>
<td><p>Определяет содержимое параметра <em>источника</em> в уже открытой объекта <a href="record-object-ado.md">записи</a> . Поведение по умолчанию — это следует считать <em>исходный</em> URL-адрес, который указывает узел в древовидной структуре. Открывается поток по умолчанию, связанные с этим узлом.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenStreamUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Значение, используемое по умолчанию. Указывает, открыв объект <strong>Stream</strong> с параметрами по умолчанию.</p></td>
</tr>
</tbody>
</table>


**Эквивалент ADO/WFC**

Эти константы нет ADO/WFC эквивалентами.

