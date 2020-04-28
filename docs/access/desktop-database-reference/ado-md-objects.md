---
title: Объекты ADO MD (Справочник по базам данных Access на компьютере)
TOCTitle: ADO MD objects
ms:assetid: 13501e44-70b6-1036-a8b7-c276f187e4f4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248907(v=office.15)
ms:contentKeyID: 48543366
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a2d3acf1b236e23522da0143d577bbcbeacbb4b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283298"
---
# <a name="ado-md-objects"></a>Объекты ADO MD

**Область применения**: Access 2013, Office 2013

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>Объект</th>
<th>Описание</th>
</tr>
<tr class="odd">
<td><p><a href="axis-object-ado-md.md">Axis</a></p></td>
<td><p>Представляет положение или ось фильтра для набора ячеек, содержащего выбранные элементы одного или нескольких измерений.</p></td>
</tr>
<tr class="even">
<td><p><a href="catalog-object-ado-md.md">Каталог</a></p></td>
<td><p>Содержит сведения о многомерной схеме (то есть Кубы и базовые измерения, иерархии, уровни и элементы), характерные для поставщика многомерных данных (МДП).</p></td>
</tr>
<tr class="odd">
<td><p><a href="cell-object-ado-md.md">Cell</a></p></td>
<td><p>Представляет данные на пересечении координат оси, содержащегося в наборе ячеек.</p></td>
</tr>
<tr class="even">
<td><p><a href="cellset-object-ado-md.md">Cellset</a></p></td>
<td><p>Представляет результаты многомерного запроса. Это коллекция ячеек, выбранных из кубов или других целлсетс.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cubedef-object-ado-md.md">CubeDef</a></p></td>
<td><p>Представляет куб из многомерной схемы, содержащий набор связанных измерений.</p></td>
</tr>
<tr class="even">
<td><p><a href="dimension-object-ado-md.md">Dimension</a></p></td>
<td><p>Представляет один из измерений многомерного куба, содержащий одну или несколько иерархий элементов.</p></td>
</tr>
<tr class="odd">
<td><p><a href="hierarchy-object-ado-md.md">Hierarchy</a></p></td>
<td><p>Представляет один из способов, с помощью которого можно выполнить статистическую настройку или &quot;сведение элементов измерения. &quot; Измерение можно объединить вдоль одной или нескольких иерархий.</p></td>
</tr>
<tr class="even">
<td><p><a href="level-object-ado-md.md">Level</a></p></td>
<td><p>Содержит набор элементов, каждый из которых имеет одинаковый ранг в иерархии.</p></td>
</tr>
<tr class="odd">
<td><p><a href="member-object-ado-md.md">Элемент</a></p></td>
<td><p>Представляет элемент уровня в Кубе, дочерние элементы элемента уровня или элемента положения на оси в наборе ячеек.</p></td>
</tr>
<tr class="even">
<td><p><a href="position-object-ado-md.md">Position</a></p></td>
<td><p>Представляет набор из одного или нескольких элементов разных измерений, определяющих точку вдоль оси.</p></td>
</tr>
</tbody>
</table>

<br/>

Кроме того, объект **Catalog** подключается к объекту **подключения** ADO, который включен в стандартную библиотеку ADO:

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Объект</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="connection-object-ado.md">Connection</a></p></td>
<td><p>Представляет открытое подключение к источнику данных.</p></td>
</tr>
</tbody>
</table>

<br/>

В соответствующей коллекции может содержаться множество объектов ADO MD. Например, объект [CubeDef](cubedef-object-ado-md.md) может содержаться в коллекции [коллекция cubedefs](cubedefs-collection-ado-md.md) **каталога**. Более подробную информацию можно узнать в статье [ADO MD Collections](ado-md-collections.md).

