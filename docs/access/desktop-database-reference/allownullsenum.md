---
title: AllowNullsEnum (Справочник по для настольных баз данных Access)
TOCTitle: AllowNullsEnum
ms:assetid: 7bb42b38-6b3b-5930-b1d7-16323a3bdf37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249515(v=office.15)
ms:contentKeyID: 48545819
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c184253551fa3f974de1840d47654af597881cb8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701433"
---
# <a name="allownullsenum"></a>AllowNullsEnum

**Применимо к**: Access 2013, Office 2013

Указывает, индексированные записи с пустым значением.

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
<td><p><strong>adIndexNullsAllow</strong></p></td>
<td><p>0</p></td>
<td><p>Индекс разрешает записей, в которых ключевые столбцы имеют значение null. Нулевое значение, введенное в столбце ключа, запись вставляется в индексе.</p></td>
</tr>
<tr class="even">
<td><p><strong>adIndexNullsDisallow</strong></p></td>
<td><p>1</p></td>
<td><p>Значение, используемое по умолчанию. Индекс не разрешает записей, в которых ключевые столбцы имеют значение null. Нулевое значение, введенное в столбце ключа, произойдет ошибка.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adIndexNullsIgnore</strong></p></td>
<td><p>2</p></td>
<td><p>Индекс не вставляет операции, содержащие значение null, ключи. Нулевое значение, введенное в столбце ключа, операция обрабатывается и ошибка не происходит.</p></td>
</tr>
<tr class="even">
<td><p><strong>adIndexNullsIgnoreAny</strong></p></td>
<td><p>4</p></td>
<td><p>Индекс не вставляет записей, где некоторые ключевые столбец имеет значение null. Для индекса с несколькими столбцами ключей и нулевое значение, введенное в несколько столбцов, операция учитывается, и ошибка не происходит.</p></td>
</tr>
</tbody>
</table>

