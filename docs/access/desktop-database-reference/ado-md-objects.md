---
title: ADO MD objects (Access desktop database reference)
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
# <a name="ado-md-objects"></a><span data-ttu-id="688d2-102">Объекты ADO MD</span><span class="sxs-lookup"><span data-stu-id="688d2-102">ADO MD objects</span></span>

<span data-ttu-id="688d2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="688d2-103">**Applies to**: Access 2013, Office 2013</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="688d2-104">Объект</span><span class="sxs-lookup"><span data-stu-id="688d2-104">Object</span></span></th>
<th><span data-ttu-id="688d2-105">Описание</span><span class="sxs-lookup"><span data-stu-id="688d2-105">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="688d2-106"><a href="axis-object-ado-md.md">Axis</a></span><span class="sxs-lookup"><span data-stu-id="688d2-106"><a href="axis-object-ado-md.md">Axis</a></span></span></p></td>
<td><p><span data-ttu-id="688d2-107">Представляет позиционную или фильтровую ось ячейки, содержащую выбранные элементы одного или более измерений.</span><span class="sxs-lookup"><span data-stu-id="688d2-107">Represents a positional or filter axis of a cellset, containing selected members of one or more dimensions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="688d2-108"><a href="catalog-object-ado-md.md">Каталог</a></span><span class="sxs-lookup"><span data-stu-id="688d2-108"><a href="catalog-object-ado-md.md">Catalog</a></span></span></p></td>
<td><p><span data-ttu-id="688d2-109">Содержит сведения о многомерной схеме (то есть кубы и ее измерения, иерархии, уровни и члены), специфичность для многомерного поставщика данных (MDP).</span><span class="sxs-lookup"><span data-stu-id="688d2-109">Contains multidimensional schema information (that is, cubes and underlying dimensions, hierarchies, levels, and members) specific to a multidimensional data provider (MDP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="688d2-110"><a href="cell-object-ado-md.md">Cell</a></span><span class="sxs-lookup"><span data-stu-id="688d2-110"><a href="cell-object-ado-md.md">Cell</a></span></span></p></td>
<td><p><span data-ttu-id="688d2-111">Представляет данные на пересечении координат оси, содержащихся в ячейках.</span><span class="sxs-lookup"><span data-stu-id="688d2-111">Represents the data at the intersection of axis coordinates, contained in a cellset.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="688d2-112"><a href="cellset-object-ado-md.md">Cellset</a></span><span class="sxs-lookup"><span data-stu-id="688d2-112"><a href="cellset-object-ado-md.md">Cellset</a></span></span></p></td>
<td><p><span data-ttu-id="688d2-113">Представляет результаты многомерного запроса.</span><span class="sxs-lookup"><span data-stu-id="688d2-113">Represents the results of a multidimensional query.</span></span> <span data-ttu-id="688d2-114">Это коллекция ячеек, выбранных из кубов или других ячеек.</span><span class="sxs-lookup"><span data-stu-id="688d2-114">It is a collection of cells selected from cubes or other cellsets.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="688d2-115"><a href="cubedef-object-ado-md.md">CubeDef</a></span><span class="sxs-lookup"><span data-stu-id="688d2-115"><a href="cubedef-object-ado-md.md">CubeDef</a></span></span></p></td>
<td><p><span data-ttu-id="688d2-116">Представляет куб из многомерной схемы, содержащий набор связанных измерений.</span><span class="sxs-lookup"><span data-stu-id="688d2-116">Represents a cube from a multidimensional schema, containing a set of related dimensions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="688d2-117"><a href="dimension-object-ado-md.md">Dimension</a></span><span class="sxs-lookup"><span data-stu-id="688d2-117"><a href="dimension-object-ado-md.md">Dimension</a></span></span></p></td>
<td><p><span data-ttu-id="688d2-118">Представляет одно из измерений многомерного куба, содержащего одну или несколько иерархий членов.</span><span class="sxs-lookup"><span data-stu-id="688d2-118">Represents one of the dimensions of a multidimensional cube, containing one or more hierarchies of members.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="688d2-119"><a href="hierarchy-object-ado-md.md">Hierarchy</a></span><span class="sxs-lookup"><span data-stu-id="688d2-119"><a href="hierarchy-object-ado-md.md">Hierarchy</a></span></span></p></td>
<td><p><span data-ttu-id="688d2-120">Представляет один из способов агрегировать или свернуть члены &quot; измерения. &quot; Измерение можно агрегировать по одной или более иерархиям.</span><span class="sxs-lookup"><span data-stu-id="688d2-120">Represents one way in which the members of a dimension can be aggregated or &quot;rolled up.&quot; A dimension can be aggregated along one or more hierarchies.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="688d2-121"><a href="level-object-ado-md.md">Level</a></span><span class="sxs-lookup"><span data-stu-id="688d2-121"><a href="level-object-ado-md.md">Level</a></span></span></p></td>
<td><p><span data-ttu-id="688d2-122">Содержит набор членов, каждый из которых имеет одинаковый ранг в иерархии.</span><span class="sxs-lookup"><span data-stu-id="688d2-122">Contains a set of members, each of which has the same rank within a hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="688d2-123"><a href="member-object-ado-md.md">Элемент</a></span><span class="sxs-lookup"><span data-stu-id="688d2-123"><a href="member-object-ado-md.md">Member</a></span></span></p></td>
<td><p><span data-ttu-id="688d2-124">Представляет элемент уровня в кубе, его детей или позицию вдоль оси ячеек.</span><span class="sxs-lookup"><span data-stu-id="688d2-124">Represents a member of a level in a cube, the children of a member of a level, or a member of a position along an axis of a cellset.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="688d2-125"><a href="position-object-ado-md.md">Position</a></span><span class="sxs-lookup"><span data-stu-id="688d2-125"><a href="position-object-ado-md.md">Position</a></span></span></p></td>
<td><p><span data-ttu-id="688d2-126">Представляет набор из одного или более членов различных измерений, определяющей точку вдоль оси.</span><span class="sxs-lookup"><span data-stu-id="688d2-126">Represents a set of one or more members of different dimensions that defines a point along an axis.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="688d2-127">Кроме того, **объект Catalog** подключен к объекту подключения **ADO,** который входит в стандартную библиотеку ADO:</span><span class="sxs-lookup"><span data-stu-id="688d2-127">Also, the **Catalog** object is connected to an ADO **Connection** object, which is included with the standard ADO library:</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="688d2-128">Объект</span><span class="sxs-lookup"><span data-stu-id="688d2-128">Object</span></span></p></th>
<th><p><span data-ttu-id="688d2-129">Описание</span><span class="sxs-lookup"><span data-stu-id="688d2-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="688d2-130"><a href="connection-object-ado.md">Connection</a></span><span class="sxs-lookup"><span data-stu-id="688d2-130"><a href="connection-object-ado.md">Connection</a></span></span></p></td>
<td><p><span data-ttu-id="688d2-131">Представляет открытое подключение к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="688d2-131">Represents an open connection to a data source.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="688d2-132">Многие объекты ADO MD могут содержаться в соответствующей коллекции.</span><span class="sxs-lookup"><span data-stu-id="688d2-132">Many ADO MD objects can be contained in a corresponding collection.</span></span> <span data-ttu-id="688d2-133">Например, объект [CubeDef](cubedef-object-ado-md.md) может содержаться в коллекции [CubeDefs](cubedefs-collection-ado-md.md) **каталога.**</span><span class="sxs-lookup"><span data-stu-id="688d2-133">For example, a [CubeDef](cubedef-object-ado-md.md) object can be contained in a [CubeDefs](cubedefs-collection-ado-md.md) collection of a **Catalog**.</span></span> <span data-ttu-id="688d2-134">Дополнительные сведения [см. в коллекциях ADO MD.](ado-md-collections.md)</span><span class="sxs-lookup"><span data-stu-id="688d2-134">For more information, see [ADO MD Collections](ado-md-collections.md).</span></span>

