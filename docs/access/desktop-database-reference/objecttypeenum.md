---
title: ObjectTypeEnum (справочник по базе данных Access для настольных ПК)
TOCTitle: ObjectTypeEnum
ms:assetid: b0ee2113-dea9-912d-3442-e54885397310
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249842(v=office.15)
ms:contentKeyID: 48547132
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6e3b470c8c0d0c3f04b59bd382b66117bd79c188
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288534"
---
# <a name="objecttypeenum"></a>ObjectTypeEnum

**Область применения**: Access 2013, Office 2013

Указывает тип объекта базы данных, для которого необходимо установить разрешения или права владельца.

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
<td><p><strong>adPermObjColumn</strong></p></td>
<td><p>2 </p></td>
<td><p>Объект является столбцом.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPermObjDatabase</strong></p></td>
<td><p>3 </p></td>
<td><p>Объект является базой данных.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPermObjProcedure</strong></p></td>
<td><p>4 </p></td>
<td><p>Объект является процедурой.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPermObjProviderSpecific</strong></p></td>
<td><p>–1</p></td>
<td><p>Объект — это тип, определенный поставщиком. Если параметр <em>ObjectType</em> имеет тип <strong>adPermObjProviderSpecific</strong> и <em>ObjectTypeId</em> не задан, произойдет ошибка.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPermObjTable</strong></p></td>
<td><p>1 </p></td>
<td><p>Объект является таблицей.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPermObjView</strong></p></td>
<td><p>5 </p></td>
<td><p>Объект — это представление.</p></td>
</tr>
</tbody>
</table>

