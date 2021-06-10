---
title: Объекты ADO MD (Ссылка на настольные базы данных)
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
<td><p>Представляет позиционную или фильтровую ось ячейки, содержащую выбранные элементы одного или более измерений.</p></td>
</tr>
<tr class="even">
<td><p><a href="catalog-object-ado-md.md">Каталог</a></p></td>
<td><p>Содержит многомерные сведения о схеме (т. е. кубов и их ниже, иерархий, уровней и членов), специфичные для многомерного поставщика данных (MDP).</p></td>
</tr>
<tr class="odd">
<td><p><a href="cell-object-ado-md.md">Cell</a></p></td>
<td><p>Представляет данные на пересечении координат оси, содержащихся в ячейке.</p></td>
</tr>
<tr class="even">
<td><p><a href="cellset-object-ado-md.md">Cellset</a></p></td>
<td><p>Представляет результаты многомерного запроса. Это коллекция ячеек, выбранных из кубов или других ячеек.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cubedef-object-ado-md.md">CubeDef</a></p></td>
<td><p>Представляет куб из многомерной схемы, содержащей набор связанных измерений.</p></td>
</tr>
<tr class="even">
<td><p><a href="dimension-object-ado-md.md">Dimension</a></p></td>
<td><p>Представляет одно из измерений многомерного куба, содержащего одну или несколько иерархий участников.</p></td>
</tr>
<tr class="odd">
<td><p><a href="hierarchy-object-ado-md.md">Hierarchy</a></p></td>
<td><p>Представляет один из способов агрегировать или свернуть члены &quot; измерения. &quot; Измерение можно агрегировать по одной или несколько иерархий.</p></td>
</tr>
<tr class="even">
<td><p><a href="level-object-ado-md.md">Level</a></p></td>
<td><p>Содержит набор участников, каждый из которых имеет один и тот же ранг в иерархии.</p></td>
</tr>
<tr class="odd">
<td><p><a href="member-object-ado-md.md">Элемент</a></p></td>
<td><p>Представляет члена уровня в кубе, детей члена уровня или члена положения вдоль оси ячейки.</p></td>
</tr>
<tr class="even">
<td><p><a href="position-object-ado-md.md">Position</a></p></td>
<td><p>Представляет набор из одного или более членов разных размеров, определяющей точку вдоль оси.</p></td>
</tr>
</tbody>
</table>

<br/>

Кроме того, **объект Catalog** подключен к объекту ADO **Connection,** который входит в стандартную библиотеку ADO:

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

Многие объекты ADO MD могут содержаться в соответствующей коллекции. Например, объект [CubeDef](cubedef-object-ado-md.md) может содержаться в коллекции [CubeDefs](cubedefs-collection-ado-md.md) **каталога.** Дополнительные сведения см. в [подборке ADO MD Collections.](ado-md-collections.md)

