---
title: Объект Hierarchy (ADO MD)
TOCTitle: Hierarchy object (ADO MD)
ms:assetid: 26e4e690-59ad-fb87-66b0-f3310df42d0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249031(v=office.15)
ms:contentKeyID: 48543825
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c6668dfd40f7d0d26bcfa2ca4149acdc713e14c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291931"
---
# <a name="hierarchy-object-ado-md"></a><span data-ttu-id="e9387-102">Объект Hierarchy (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="e9387-102">Hierarchy object (ADO MD)</span></span>


<span data-ttu-id="e9387-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e9387-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e9387-104">Представляет один из способов агрегировать или "свернуть" члены измерения. [](dimension-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="e9387-104">Represents one way in which the members of a [dimension](dimension-object-ado-md.md) can be aggregated or "rolled up."</span></span> <span data-ttu-id="e9387-105">Измерение можно агрегировать по одной или более иерархиям.</span><span class="sxs-lookup"><span data-stu-id="e9387-105">A dimension can be aggregated along one or more hierarchies.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9387-106">Заметки</span><span class="sxs-lookup"><span data-stu-id="e9387-106">Remarks</span></span>

<span data-ttu-id="e9387-107">С помощью коллекций и свойств объекта **Hierarchy** можно сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="e9387-107">With the collections and properties of a **Hierarchy** object, you can do the following:</span></span>

  - <span data-ttu-id="e9387-108">Определите **иерархию** со [свойствами Name](name-property-ado-md.md) и [UniqueName.](uniquename-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="e9387-108">Identify the **Hierarchy** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="e9387-109">Возвращает осмысленные строки, описывая **иерархию** со [свойством Description.](description-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="e9387-109">Return a meaningful string that describes the **Hierarchy** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="e9387-110">Возвращает [объекты level,](level-object-ado-md.md) которые составляют **иерархию** с [коллекцией Levels.](levels-collection-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="e9387-110">Return the [Level](level-object-ado-md.md) objects that make up the **Hierarchy** with the [Levels](levels-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="e9387-111">Используйте стандартную коллекцию [свойств](properties-collection-ado.md) ADO для получения дополнительных сведений об **объекте Hierarchy.**</span><span class="sxs-lookup"><span data-stu-id="e9387-111">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Hierarchy** object.</span></span>

<span data-ttu-id="e9387-112">Коллекция **Properties** содержит свойства, предоставленные поставщиком.</span><span class="sxs-lookup"><span data-stu-id="e9387-112">The **Properties** collection contains provider-supplied properties.</span></span> <span data-ttu-id="e9387-113">В следующей таблице перечислены свойства, которые могут быть доступны.</span><span class="sxs-lookup"><span data-stu-id="e9387-113">The following table lists properties that might be available.</span></span> <span data-ttu-id="e9387-114">Фактический список свойств может отличаться в зависимости от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="e9387-114">The actual property list may differ depending upon the implementation of the provider.</span></span> <span data-ttu-id="e9387-115">Более полный список доступных свойств см. в документации к поставщику.</span><span class="sxs-lookup"><span data-stu-id="e9387-115">See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e9387-116">Имя</span><span class="sxs-lookup"><span data-stu-id="e9387-116">Name</span></span></p></th>
<th><p><span data-ttu-id="e9387-117">Описание</span><span class="sxs-lookup"><span data-stu-id="e9387-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9387-118">AllMember</span><span class="sxs-lookup"><span data-stu-id="e9387-118">AllMember</span></span></p></td>
<td><p><span data-ttu-id="e9387-119">Член на самом высоком уровне ската в иерархии.</span><span class="sxs-lookup"><span data-stu-id="e9387-119">The member at the highest level of rollup in the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9387-120">CatalogName</span><span class="sxs-lookup"><span data-stu-id="e9387-120">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="e9387-121">Имя каталога, к которому принадлежит этот куб.</span><span class="sxs-lookup"><span data-stu-id="e9387-121">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9387-122">CubeName</span><span class="sxs-lookup"><span data-stu-id="e9387-122">CubeName</span></span></p></td>
<td><p><span data-ttu-id="e9387-123">Имя куба.</span><span class="sxs-lookup"><span data-stu-id="e9387-123">The name of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9387-124">DefaultMember</span><span class="sxs-lookup"><span data-stu-id="e9387-124">DefaultMember</span></span></p></td>
<td><p><span data-ttu-id="e9387-125">Уникальное имя члена по умолчанию для этой иерархии.</span><span class="sxs-lookup"><span data-stu-id="e9387-125">The unique name of the default member for this hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9387-126">Описание</span><span class="sxs-lookup"><span data-stu-id="e9387-126">Description</span></span></p></td>
<td><p><span data-ttu-id="e9387-127">Осмысленное описание иерархии.</span><span class="sxs-lookup"><span data-stu-id="e9387-127">A meaningful description of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9387-128">DimensionType</span><span class="sxs-lookup"><span data-stu-id="e9387-128">DimensionType</span></span></p></td>
<td><p><span data-ttu-id="e9387-129">Тип измерения, к которому принадлежит эта иерархия.</span><span class="sxs-lookup"><span data-stu-id="e9387-129">The type of dimension to which this hierarchy belongs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9387-130">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="e9387-130">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="e9387-131">Однозначное имя измерения.</span><span class="sxs-lookup"><span data-stu-id="e9387-131">The unambiguous name of the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9387-132">HierarchyCaption</span><span class="sxs-lookup"><span data-stu-id="e9387-132">HierarchyCaption</span></span></p></td>
<td><p><span data-ttu-id="e9387-133">Метка или заголовок, связанные с иерархией.</span><span class="sxs-lookup"><span data-stu-id="e9387-133">A label or caption associated with the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9387-134">HierarchyCardinality</span><span class="sxs-lookup"><span data-stu-id="e9387-134">HierarchyCardinality</span></span></p></td>
<td><p><span data-ttu-id="e9387-135">Количество членов в иерархии.</span><span class="sxs-lookup"><span data-stu-id="e9387-135">The number of members in the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9387-136">HierarchyGUID</span><span class="sxs-lookup"><span data-stu-id="e9387-136">HierarchyGUID</span></span></p></td>
<td><p><span data-ttu-id="e9387-137">GUID иерархии.</span><span class="sxs-lookup"><span data-stu-id="e9387-137">The GUID of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9387-138">HierarchyName</span><span class="sxs-lookup"><span data-stu-id="e9387-138">HierarchyName</span></span></p></td>
<td><p><span data-ttu-id="e9387-139">Имя иерархии.</span><span class="sxs-lookup"><span data-stu-id="e9387-139">The name of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9387-140">HierarchyUniqueName</span><span class="sxs-lookup"><span data-stu-id="e9387-140">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="e9387-141">Однозначное имя иерархии.</span><span class="sxs-lookup"><span data-stu-id="e9387-141">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9387-142">SchemaName</span><span class="sxs-lookup"><span data-stu-id="e9387-142">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="e9387-143">Имя схемы, к которой принадлежит этот куб.</span><span class="sxs-lookup"><span data-stu-id="e9387-143">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

