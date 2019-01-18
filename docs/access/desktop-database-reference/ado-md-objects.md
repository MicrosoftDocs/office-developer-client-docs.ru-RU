---
title: Объекты ADO MD (Справочник по для настольных баз данных Access)
TOCTitle: ADO MD objects
ms:assetid: 13501e44-70b6-1036-a8b7-c276f187e4f4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248907(v=office.15)
ms:contentKeyID: 48543366
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a2d3acf1b236e23522da0143d577bbcbeacbb4b7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726213"
---
# <a name="ado-md-objects"></a>Объекты ADO MD

**Применимо к**: Access 2013, Office 2013

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
<td><p>Представляет позиционные или оси фильтра набора ячеек, содержащий выбранные элементы из одного или нескольких измерений.</p></td>
</tr>
<tr class="even">
<td><p><a href="catalog-object-ado-md.md">Каталог</a></p></td>
<td><p>Содержит многомерные сведения о схеме (то есть, кубов и базовым измерений, иерархии, уровни и элементы) определенного поставщика многомерных данных (MDP).</p></td>
</tr>
<tr class="odd">
<td><p><a href="cell-object-ado-md.md">Cell</a></p></td>
<td><p>Представляет данные на пересечении ось координат, содержащихся в набор ячеек.</p></td>
</tr>
<tr class="even">
<td><p><a href="cellset-object-ado-md.md">Cellset</a></p></td>
<td><p>Представляет результаты запроса многомерных. Это коллекция ячеек, выбранные из кубов или других наборов ячеек.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cubedef-object-ado-md.md">CubeDef</a></p></td>
<td><p>Представляет куб из многомерных схемы, содержащая набор связанных измерений.</p></td>
</tr>
<tr class="even">
<td><p><a href="dimension-object-ado-md.md">Dimension</a></p></td>
<td><p>Представляет один из измерения многомерного куба, содержащего иерархии один или несколько элементов.</p></td>
</tr>
<tr class="odd">
<td><p><a href="hierarchy-object-ado-md.md">Hierarchy</a></p></td>
<td><p>Представляет один способ которого можно объединить элементов измерения или &quot;суммируются. &quot; Измерения можно объединить вместе один или несколько иерархий.</p></td>
</tr>
<tr class="even">
<td><p><a href="level-object-ado-md.md">Level</a></p></td>
<td><p>Содержит набор элементов, каждый из которых содержит один и тот же ранг в иерархии.</p></td>
</tr>
<tr class="odd">
<td><p><a href="member-object-ado-md.md">Элемент</a></p></td>
<td><p>Представляет элемент уровень в кубе, дочерние элементы элемента уровня или членом положение оси набора ячеек.</p></td>
</tr>
<tr class="even">
<td><p><a href="position-object-ado-md.md">Position</a></p></td>
<td><p>Представляет набор одного или нескольких элементов различных измерений, который определяет точку оси.</p></td>
</tr>
</tbody>
</table>

<br/>

Кроме того объект **каталога** подключен объект ADO- **подключения** , который входит в состав стандартной библиотеки ADO:

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

Многие объекты ADO MD может содержаться в соответствующие коллекции. Например объект [CubeDef](cubedef-object-ado-md.md) может содержаться в коллекцию [CubeDefs](cubedefs-collection-ado-md.md) **каталога**. Для получения дополнительных сведений см [ADO MD семейств сайтов](ado-md-collections.md).

