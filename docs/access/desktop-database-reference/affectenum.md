---
title: AffectEnum (справочник по базе данных Access для настольных ПК)
TOCTitle: AffectEnum
ms:assetid: 15393398-d7eb-a685-1bfa-d6712d8e5015
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248916(v=office.15)
ms:contentKeyID: 48543404
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0183cde0862e947f686bed9821e447abc117d205
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297202"
---
# <a name="affectenum"></a>AffectEnum

**Область применения**: Access 2013, Office 2013

Указывает, на какие записи влияет операция.

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
<td><p><strong>adAffectAll</strong></p></td>
<td><p>3 </p></td>
<td><p>Если к набору <a href="filter-property-ado.md">записей не</a> применяется <strong>фильтр,</strong>это влияет на все записи. Если свойство <strong>Filter</strong> имеет строку условия (например, Author='Smith'), операция влияет на видимые записи &quot; &quot; в текущей главе. Если для <strong>свойства Filter</strong> установлено свойство <a href="filtergroupenum.md">FilterGroupEnum</a> или массив закладок, операция повлияет на все строки <strong>набора записей.</strong></p><p><strong>ПРИМЕЧАНИЕ.</strong>AdAffectAll скрыт в браузере Visual Basic объектов.</p>
</td>
</tr>
<tr class="even">
<td><p><strong>adAffectAllChapters</strong></p></td>
<td><p>4 </p></td>
<td><p>Влияет на все записи во всех <strong></strong>главах одного и того же раздела в наборе записей, включая те, которые не видны с помощью <strong>фильтра,</strong> который применяется в настоящее время.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adAffectCurrent</strong></p></td>
<td><p>1 </p></td>
<td><p>Влияет только на текущую запись.</p></td>
</tr>
<tr class="even">
<td><p><strong>adAffectGroup</strong></p></td>
<td><p>2 </p></td>
<td><p>Влияет только на записи, удовлетворяющие <a href="filter-property-ado.md">текущему параметру</a> свойства Filter. Чтобы использовать этот <strong>параметр,</strong> необходимо установить для свойства <strong></strong> <strong>Filter значение FilterGroupEnum</strong> или массив закладок.</p></td>
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
<td><p>AdoEnums.Affect.ALL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Affect.ALLCHAPTERS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Affect.CURRENT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Affect.GROUP</p></td>
</tr>
</tbody>
</table>

