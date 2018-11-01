---
title: Объекты ADO MD (Справочник по для настольных баз данных Access)
TOCTitle: ADO MD Objects
ms:assetid: 13501e44-70b6-1036-a8b7-c276f187e4f4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248907(v=office.15)
ms:contentKeyID: 48543366
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e09676b222e7199b7f2f9f7520ebf3d5436f9a3c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875135"
---
# <a name="ado-md-objects"></a><span data-ttu-id="b88b1-102">Объекты ADO MD</span><span class="sxs-lookup"><span data-stu-id="b88b1-102">ADO MD Objects</span></span>


<span data-ttu-id="b88b1-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b88b1-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b88b1-104"><a href="axis-object-ado-md.md">Ось</a></span><span class="sxs-lookup"><span data-stu-id="b88b1-104"><a href="axis-object-ado-md.md">Axis</a></span></span></p></td>
<td><p><span data-ttu-id="b88b1-105">Представляет позиционные или оси фильтра набора ячеек, содержащий выбранные элементы из одного или нескольких измерений.</span><span class="sxs-lookup"><span data-stu-id="b88b1-105">Represents a positional or filter axis of a cellset, containing selected members of one or more dimensions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b88b1-106"><a href="catalog-object-ado-md.md">Каталог</a></span><span class="sxs-lookup"><span data-stu-id="b88b1-106"><a href="catalog-object-ado-md.md">Catalog</a></span></span></p></td>
<td><p><span data-ttu-id="b88b1-107">Содержит многомерные сведения о схеме (то есть, кубов и базовым измерений, иерархии, уровни и элементы) определенного поставщика многомерных данных (MDP).</span><span class="sxs-lookup"><span data-stu-id="b88b1-107">Contains multidimensional schema information (that is, cubes and underlying dimensions, hierarchies, levels, and members) specific to a multidimensional data provider (MDP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b88b1-108"><a href="cell-object-ado-md.md">Cell</a></span><span class="sxs-lookup"><span data-stu-id="b88b1-108"><a href="cell-object-ado-md.md">Cell</a></span></span></p></td>
<td><p><span data-ttu-id="b88b1-109">Представляет данные на пересечении ось координат, содержащихся в набор ячеек.</span><span class="sxs-lookup"><span data-stu-id="b88b1-109">Represents the data at the intersection of axis coordinates, contained in a cellset.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b88b1-110"><a href="cellset-object-ado-md.md">Набор ячеек</a></span><span class="sxs-lookup"><span data-stu-id="b88b1-110"><a href="cellset-object-ado-md.md">Cellset</a></span></span></p></td>
<td><p><span data-ttu-id="b88b1-111">Представляет результаты запроса многомерных.</span><span class="sxs-lookup"><span data-stu-id="b88b1-111">Represents the results of a multidimensional query.</span></span> <span data-ttu-id="b88b1-112">Это коллекция ячеек, выбранные из кубов или других наборов ячеек.</span><span class="sxs-lookup"><span data-stu-id="b88b1-112">It is a collection of cells selected from cubes or other cellsets.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b88b1-113"><a href="cubedef-object-ado-md.md">CubeDef</a></span><span class="sxs-lookup"><span data-stu-id="b88b1-113"><a href="cubedef-object-ado-md.md">CubeDef</a></span></span></p></td>
<td><p><span data-ttu-id="b88b1-114">Представляет куб из многомерных схемы, содержащая набор связанных измерений.</span><span class="sxs-lookup"><span data-stu-id="b88b1-114">Represents a cube from a multidimensional schema, containing a set of related dimensions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b88b1-115"><a href="dimension-object-ado-md.md">Измерения</a></span><span class="sxs-lookup"><span data-stu-id="b88b1-115"><a href="dimension-object-ado-md.md">Dimension</a></span></span></p></td>
<td><p><span data-ttu-id="b88b1-116">Представляет один из измерения многомерного куба, содержащего иерархии один или несколько элементов.</span><span class="sxs-lookup"><span data-stu-id="b88b1-116">Represents one of the dimensions of a multidimensional cube, containing one or more hierarchies of members.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b88b1-117"><a href="hierarchy-object-ado-md.md">Иерархия</a></span><span class="sxs-lookup"><span data-stu-id="b88b1-117"><a href="hierarchy-object-ado-md.md">Hierarchy</a></span></span></p></td>
<td><p><span data-ttu-id="b88b1-118">Представляет один способ которого можно объединить элементов измерения или &quot;суммируются. &quot; Измерения можно объединить вместе один или несколько иерархий.</span><span class="sxs-lookup"><span data-stu-id="b88b1-118">Represents one way in which the members of a dimension can be aggregated or &quot;rolled up.&quot; A dimension can be aggregated along one or more hierarchies.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b88b1-119"><a href="level-object-ado-md.md">Уровень</a></span><span class="sxs-lookup"><span data-stu-id="b88b1-119"><a href="level-object-ado-md.md">Level</a></span></span></p></td>
<td><p><span data-ttu-id="b88b1-120">Содержит набор элементов, каждый из которых содержит один и тот же ранг в иерархии.</span><span class="sxs-lookup"><span data-stu-id="b88b1-120">Contains a set of members, each of which has the same rank within a hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b88b1-121"><a href="member-object-ado-md.md">Элемент</a></span><span class="sxs-lookup"><span data-stu-id="b88b1-121"><a href="member-object-ado-md.md">Member</a></span></span></p></td>
<td><p><span data-ttu-id="b88b1-122">Представляет элемент уровень в кубе, дочерние элементы элемента уровня или членом положение оси набора ячеек.</span><span class="sxs-lookup"><span data-stu-id="b88b1-122">Represents a member of a level in a cube, the children of a member of a level, or a member of a position along an axis of a cellset.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b88b1-123"><a href="position-object-ado-md.md">Position</a></span><span class="sxs-lookup"><span data-stu-id="b88b1-123"><a href="position-object-ado-md.md">Position</a></span></span></p></td>
<td><p><span data-ttu-id="b88b1-124">Представляет набор одного или нескольких элементов различных измерений, который определяет точку оси.</span><span class="sxs-lookup"><span data-stu-id="b88b1-124">Represents a set of one or more members of different dimensions that defines a point along an axis.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b88b1-125">Кроме того объект **каталога** подключен объект ADO- **подключения** , который входит в состав стандартной библиотеки ADO:</span><span class="sxs-lookup"><span data-stu-id="b88b1-125">Also, the **Catalog** object is connected to an ADO **Connection** object, which is included with the standard ADO library:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b88b1-126">Объект</span><span class="sxs-lookup"><span data-stu-id="b88b1-126">Object</span></span></p></th>
<th><p><span data-ttu-id="b88b1-127">Описание</span><span class="sxs-lookup"><span data-stu-id="b88b1-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b88b1-128"><a href="connection-object-ado.md">Подключение</a></span><span class="sxs-lookup"><span data-stu-id="b88b1-128"><a href="connection-object-ado.md">Connection</a></span></span></p></td>
<td><p><span data-ttu-id="b88b1-129">Представляет открытое подключение к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="b88b1-129">Represents an open connection to a data source.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b88b1-130">Многие объекты ADO MD может содержаться в соответствующие коллекции.</span><span class="sxs-lookup"><span data-stu-id="b88b1-130">Many ADO MD objects can be contained in a corresponding collection.</span></span> <span data-ttu-id="b88b1-131">Например объект [CubeDef](cubedef-object-ado-md.md) может содержаться в коллекцию [CubeDefs](cubedefs-collection-ado-md.md) **каталога**.</span><span class="sxs-lookup"><span data-stu-id="b88b1-131">For example, a [CubeDef](cubedef-object-ado-md.md) object can be contained in a [CubeDefs](cubedefs-collection-ado-md.md) collection of a **Catalog**.</span></span> <span data-ttu-id="b88b1-132">Для получения дополнительных сведений см [ADO MD семейств сайтов](ado-md-collections.md).</span><span class="sxs-lookup"><span data-stu-id="b88b1-132">For more information, see [ADO MD Collections](ado-md-collections.md).</span></span>

