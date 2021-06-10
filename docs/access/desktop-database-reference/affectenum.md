---
title: AffectEnum (Ссылка на настольные базы данных)
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
<td><p>3</p></td>
<td><p>Если фильтр не <a href="filter-property-ado.md">применяется</a> к <strong>Набору записей,</strong>влияет на все записи. Если свойство <strong>Filter</strong> заданной для строки (например, Author='Smith), операция влияет на видимые записи &quot; в текущей &quot; главе. Если свойство <strong>Filter</strong> установлено для члена <a href="filtergroupenum.md">FilterGroupEnum</a> или массива закладок, операция затронет все строки <strong>набора записей.</strong></p><p><strong>ПРИМЕЧАНИЕ.</strong>adAffectAll скрыт в браузере Visual Basic объекта.</p>
</td>
</tr>
<tr class="even">
<td><p><strong>adAffectAllChapters</strong></p></td>
<td><p>4 </p></td>
<td><p>Влияет на все записи во всех главах <strong>наборов</strong>записей, включая записи, которые не видны с помощью фильтра, <strong>который</strong> применяется в настоящее время.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adAffectCurrent</strong></p></td>
<td><p>1</p></td>
<td><p>Влияет только на текущую запись.</p></td>
</tr>
<tr class="even">
<td><p><strong>adAffectGroup</strong></p></td>
<td><p>2</p></td>
<td><p>Влияет только на записи, удовлетворяющие текущему <a href="filter-property-ado.md">параметру свойства Filter.</a> Для использования <strong>этого</strong> параметра необходимо указать свойство Filter <strong></strong> значение <strong>FilterGroupEnum</strong> или массив закладок.</p></td>
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

