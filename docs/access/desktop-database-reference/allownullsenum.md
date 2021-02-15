---
title: AllowNullsEnum (справочник по базам данных Access для настольных ПК)
TOCTitle: AllowNullsEnum
ms:assetid: 7bb42b38-6b3b-5930-b1d7-16323a3bdf37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249515(v=office.15)
ms:contentKeyID: 48545819
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c184253551fa3f974de1840d47654af597881cb8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297168"
---
# <a name="allownullsenum"></a>AllowNullsEnum

**Область применения**: Access 2013, Office 2013

Указывает, индексироваться ли записи со значениями NULL.

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
<td><p>Индекс разрешает записи, в которых ключевые столбцы имеют значение NULL. Если в ключевом столбце вводится значение null, запись вставляется в индекс.</p></td>
</tr>
<tr class="even">
<td><p><strong>adIndexNullsDisallow</strong></p></td>
<td><p>1 </p></td>
<td><p>Значение, используемое по умолчанию. В индексе не допускается использовать записи, в которых ключевые столбцы имеют значение NULL. Если в ключевом столбце ввели значение null, произойдет ошибка.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adIndexNullsIgnore</strong></p></td>
<td><p>2 </p></td>
<td><p>Индекс не вставляет записи, содержащие ключи NULL. Если в ключевом столбце ввели значение null, запись игнорируется, и ошибка не возникает.</p></td>
</tr>
<tr class="even">
<td><p><strong>adIndexNullsIgnoreAny</strong></p></td>
<td><p>4 </p></td>
<td><p>Индекс не вставляет записи, в которых для определенного ключевого столбца установлено значение null. Если в индексе с ключом с несколькими столбцами в какой-либо столбце ввели значение null, запись игнорируется и ошибки не возникают.</p></td>
</tr>
</tbody>
</table>

