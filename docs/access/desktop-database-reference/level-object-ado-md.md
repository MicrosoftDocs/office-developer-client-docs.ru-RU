---
title: Level object (ADO MD)
TOCTitle: Level object (ADO MD)
ms:assetid: ddbcabce-8777-1068-98a3-be209084f497
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250121(v=office.15)
ms:contentKeyID: 48548160
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 70fb359aa4faa0bcfc99f0b1700b0eb51f665bc0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290116"
---
# <a name="level-object-ado-md"></a><span data-ttu-id="2a63a-102">Level object (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="2a63a-102">Level object (ADO MD)</span></span>


<span data-ttu-id="2a63a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2a63a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2a63a-104">Содержит набор членов, каждый из которых имеет одинаковый ранг в иерархии.</span><span class="sxs-lookup"><span data-stu-id="2a63a-104">Contains a set of members, each of which has the same rank within a hierarchy.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a63a-105">Заметки</span><span class="sxs-lookup"><span data-stu-id="2a63a-105">Remarks</span></span>

<span data-ttu-id="2a63a-106">С помощью коллекций и свойств объекта **Level** можно сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="2a63a-106">With the collections and properties of a **Level** object, you can do the following:</span></span>

  - <span data-ttu-id="2a63a-107">Определите **уровень** со [свойствами Name](name-property-ado-md.md) и [UniqueName.](uniquename-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="2a63a-107">Identify the **Level** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="2a63a-108">Возвращает строку, которая будет применяться при отобраке **уровня** со [свойством Caption.](caption-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="2a63a-108">Return a string to use when displaying the **Level** with the [Caption](caption-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="2a63a-109">Возвращает осмысленные строки, описывая **уровень** со [свойством Description.](description-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="2a63a-109">Return a meaningful string that describes the **Level** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="2a63a-110">Возвращает [объекты Member,](member-object-ado-md.md) которые составляют **уровень** с [коллекцией Members.](members-collection-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="2a63a-110">Return the [Member](member-object-ado-md.md) objects that make up the **Level** with the [Members](members-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="2a63a-111">Возвращает количество уровней из корневого объекта **Level** со [свойством Depth.](depth-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="2a63a-111">Return the number of levels from the root of the **Level** with the [Depth](depth-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="2a63a-112">Используйте стандартную коллекцию [свойств](properties-collection-ado.md) ADO для получения дополнительных сведений об **объекте Level.**</span><span class="sxs-lookup"><span data-stu-id="2a63a-112">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Level** object.</span></span>

<span data-ttu-id="2a63a-113">Коллекция **Properties** содержит свойства, предоставленные поставщиком.</span><span class="sxs-lookup"><span data-stu-id="2a63a-113">The **Properties** collection contains provider-supplied properties.</span></span> <span data-ttu-id="2a63a-114">В следующей таблице перечислены свойства, которые могут быть доступны.</span><span class="sxs-lookup"><span data-stu-id="2a63a-114">The following table lists properties that might be available.</span></span> <span data-ttu-id="2a63a-115">Фактический список свойств может отличаться в зависимости от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="2a63a-115">The actual property list may differ depending upon the implementation of the provider.</span></span> <span data-ttu-id="2a63a-116">Более полный список доступных свойств см. в документации к поставщику.</span><span class="sxs-lookup"><span data-stu-id="2a63a-116">See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2a63a-117">Имя</span><span class="sxs-lookup"><span data-stu-id="2a63a-117">Name</span></span></p></th>
<th><p><span data-ttu-id="2a63a-118">Описание</span><span class="sxs-lookup"><span data-stu-id="2a63a-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a63a-119">CatalogName</span><span class="sxs-lookup"><span data-stu-id="2a63a-119">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="2a63a-120">Имя каталога, к которому принадлежит этот куб.</span><span class="sxs-lookup"><span data-stu-id="2a63a-120">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a63a-121">CubeName</span><span class="sxs-lookup"><span data-stu-id="2a63a-121">CubeName</span></span></p></td>
<td><p><span data-ttu-id="2a63a-122">Имя куба.</span><span class="sxs-lookup"><span data-stu-id="2a63a-122">The name of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a63a-123">Описание</span><span class="sxs-lookup"><span data-stu-id="2a63a-123">Description</span></span></p></td>
<td><p><span data-ttu-id="2a63a-124">Осмысленное описание уровня.</span><span class="sxs-lookup"><span data-stu-id="2a63a-124">A meaningful description of the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a63a-125">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="2a63a-125">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="2a63a-126">Однозначное имя <a href="dimension-object-ado-md.md">измерения.</a></span><span class="sxs-lookup"><span data-stu-id="2a63a-126">The unambiguous name of the <a href="dimension-object-ado-md.md">dimension</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a63a-127">HierarchyUniqueName</span><span class="sxs-lookup"><span data-stu-id="2a63a-127">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="2a63a-128">Однозначное имя иерархии.</span><span class="sxs-lookup"><span data-stu-id="2a63a-128">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a63a-129">LevelCaption</span><span class="sxs-lookup"><span data-stu-id="2a63a-129">LevelCaption</span></span></p></td>
<td><p><span data-ttu-id="2a63a-130">Метка или заголовок, связанный с уровнем.</span><span class="sxs-lookup"><span data-stu-id="2a63a-130">A label or caption associated with the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a63a-131">LevelCardinality</span><span class="sxs-lookup"><span data-stu-id="2a63a-131">LevelCardinality</span></span></p></td>
<td><p><span data-ttu-id="2a63a-132">Количество участников на уровне.</span><span class="sxs-lookup"><span data-stu-id="2a63a-132">The number of members in the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a63a-133">LevelGUID</span><span class="sxs-lookup"><span data-stu-id="2a63a-133">LevelGUID</span></span></p></td>
<td><p><span data-ttu-id="2a63a-134">GUID уровня.</span><span class="sxs-lookup"><span data-stu-id="2a63a-134">The GUID of the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a63a-135">LevelName</span><span class="sxs-lookup"><span data-stu-id="2a63a-135">LevelName</span></span></p></td>
<td><p><span data-ttu-id="2a63a-136">Имя уровня.</span><span class="sxs-lookup"><span data-stu-id="2a63a-136">Name of the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a63a-137">LevelNumber</span><span class="sxs-lookup"><span data-stu-id="2a63a-137">LevelNumber</span></span></p></td>
<td><p><span data-ttu-id="2a63a-138">Расстояние между уровнем и корнем иерархии.</span><span class="sxs-lookup"><span data-stu-id="2a63a-138">The distance between the level and the root of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a63a-139">LevelType</span><span class="sxs-lookup"><span data-stu-id="2a63a-139">LevelType</span></span></p></td>
<td><p><span data-ttu-id="2a63a-140">Тип уровня.</span><span class="sxs-lookup"><span data-stu-id="2a63a-140">The type of level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a63a-141">LevelUniqueName</span><span class="sxs-lookup"><span data-stu-id="2a63a-141">LevelUniqueName</span></span></p></td>
<td><p><span data-ttu-id="2a63a-142">Однозначное имя уровня.</span><span class="sxs-lookup"><span data-stu-id="2a63a-142">The unambiguous name of the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a63a-143">SchemaName</span><span class="sxs-lookup"><span data-stu-id="2a63a-143">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="2a63a-144">Имя схемы, к которой принадлежит этот куб.</span><span class="sxs-lookup"><span data-stu-id="2a63a-144">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

