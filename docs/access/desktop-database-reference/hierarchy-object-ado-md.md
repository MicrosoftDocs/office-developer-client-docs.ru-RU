---
title: Объект Hierarchy (ADO MD)
TOCTitle: Hierarchy object (ADO MD)
ms:assetid: 26e4e690-59ad-fb87-66b0-f3310df42d0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249031(v=office.15)
ms:contentKeyID: 48543825
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5005ffec000c8fecc1188f37fad75227385f9ee2
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928189"
---
# <a name="hierarchy-object-ado-md"></a><span data-ttu-id="3bbc0-102">Объект Hierarchy (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="3bbc0-102">Hierarchy object (ADO MD)</span></span>


<span data-ttu-id="3bbc0-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3bbc0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3bbc0-104">Представляет один из способов в котором элементов [измерения](dimension-object-ado-md.md) можно сгруппировать или «сведение.»</span><span class="sxs-lookup"><span data-stu-id="3bbc0-104">Represents one way in which the members of a [dimension](dimension-object-ado-md.md) can be aggregated or "rolled up."</span></span> <span data-ttu-id="3bbc0-105">Измерения можно объединить вместе один или несколько иерархий.</span><span class="sxs-lookup"><span data-stu-id="3bbc0-105">A dimension can be aggregated along one or more hierarchies.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bbc0-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="3bbc0-106">Remarks</span></span>

<span data-ttu-id="3bbc0-107">Со свойствами объекта **иерархии** и семейств сайтов выполните следующее:</span><span class="sxs-lookup"><span data-stu-id="3bbc0-107">With the collections and properties of a **Hierarchy** object, you can do the following:</span></span>

  - <span data-ttu-id="3bbc0-108">Определение **иерархии** с помощью свойства [Name](name-property-ado-md.md) и [уникального имени](uniquename-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="3bbc0-108">Identify the **Hierarchy** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="3bbc0-109">Возвращает удобной для восприятия строку, которая описывает **иерархии** с помощью свойства [Description](description-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="3bbc0-109">Return a meaningful string that describes the **Hierarchy** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="3bbc0-110">Возвращает объекты [уровня](level-object-ado-md.md) , которые будут включены в **иерархии** с коллекцией [уровней](levels-collection-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="3bbc0-110">Return the [Level](level-object-ado-md.md) objects that make up the **Hierarchy** with the [Levels](levels-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="3bbc0-111">Используйте коллекцию стандартный ADO [Свойства](properties-collection-ado.md) для получения дополнительных сведений об объекте **иерархии** .</span><span class="sxs-lookup"><span data-stu-id="3bbc0-111">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Hierarchy** object.</span></span>

<span data-ttu-id="3bbc0-112">Коллекции **свойств** содержит свойства, предоставленных поставщиком.</span><span class="sxs-lookup"><span data-stu-id="3bbc0-112">The **Properties** collection contains provider-supplied properties.</span></span> <span data-ttu-id="3bbc0-113">В следующей таблице перечислены свойства, которые могут быть недоступны.</span><span class="sxs-lookup"><span data-stu-id="3bbc0-113">The following table lists properties that might be available.</span></span> <span data-ttu-id="3bbc0-114">Список свойств фактический может различаться в зависимости от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="3bbc0-114">The actual property list may differ depending upon the implementation of the provider.</span></span> <span data-ttu-id="3bbc0-115">Обратитесь к документации вашего поставщика для получения более полного списка доступных свойств.</span><span class="sxs-lookup"><span data-stu-id="3bbc0-115">See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3bbc0-116">Имя</span><span class="sxs-lookup"><span data-stu-id="3bbc0-116">Name</span></span></p></th>
<th><p><span data-ttu-id="3bbc0-117">Описание</span><span class="sxs-lookup"><span data-stu-id="3bbc0-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3bbc0-118">AllMember</span><span class="sxs-lookup"><span data-stu-id="3bbc0-118">AllMember</span></span></p></td>
<td><p><span data-ttu-id="3bbc0-119">Член на верхнем уровне накопительный пакет обновления в иерархии.</span><span class="sxs-lookup"><span data-stu-id="3bbc0-119">The member at the highest level of rollup in the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bbc0-120">ИмяКаталога</span><span class="sxs-lookup"><span data-stu-id="3bbc0-120">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="3bbc0-121">Имя каталога, к которому принадлежит этот куб.</span><span class="sxs-lookup"><span data-stu-id="3bbc0-121">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bbc0-122">Имя куба</span><span class="sxs-lookup"><span data-stu-id="3bbc0-122">CubeName</span></span></p></td>
<td><p><span data-ttu-id="3bbc0-123">Имя куба.</span><span class="sxs-lookup"><span data-stu-id="3bbc0-123">The name of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bbc0-124">DefaultMember</span><span class="sxs-lookup"><span data-stu-id="3bbc0-124">DefaultMember</span></span></p></td>
<td><p><span data-ttu-id="3bbc0-125">Уникальное имя элемента по умолчанию для этой иерархии.</span><span class="sxs-lookup"><span data-stu-id="3bbc0-125">The unique name of the default member for this hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bbc0-126">Описание</span><span class="sxs-lookup"><span data-stu-id="3bbc0-126">Description</span></span></p></td>
<td><p><span data-ttu-id="3bbc0-127">Подробное описание иерархии.</span><span class="sxs-lookup"><span data-stu-id="3bbc0-127">A meaningful description of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bbc0-128">DimensionType</span><span class="sxs-lookup"><span data-stu-id="3bbc0-128">DimensionType</span></span></p></td>
<td><p><span data-ttu-id="3bbc0-129">Тип измерения, к которой принадлежит этой иерархии.</span><span class="sxs-lookup"><span data-stu-id="3bbc0-129">The type of dimension to which this hierarchy belongs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bbc0-130">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="3bbc0-130">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="3bbc0-131">Однозначное имя измерения.</span><span class="sxs-lookup"><span data-stu-id="3bbc0-131">The unambiguous name of the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bbc0-132">HierarchyCaption</span><span class="sxs-lookup"><span data-stu-id="3bbc0-132">HierarchyCaption</span></span></p></td>
<td><p><span data-ttu-id="3bbc0-133">Метка или заголовок, связанный с иерархией.</span><span class="sxs-lookup"><span data-stu-id="3bbc0-133">A label or caption associated with the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bbc0-134">HierarchyCardinality</span><span class="sxs-lookup"><span data-stu-id="3bbc0-134">HierarchyCardinality</span></span></p></td>
<td><p><span data-ttu-id="3bbc0-135">Число элементов в иерархии.</span><span class="sxs-lookup"><span data-stu-id="3bbc0-135">The number of members in the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bbc0-136">HierarchyGUID</span><span class="sxs-lookup"><span data-stu-id="3bbc0-136">HierarchyGUID</span></span></p></td>
<td><p><span data-ttu-id="3bbc0-137">GUID иерархии.</span><span class="sxs-lookup"><span data-stu-id="3bbc0-137">The GUID of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bbc0-138">HierarchyName</span><span class="sxs-lookup"><span data-stu-id="3bbc0-138">HierarchyName</span></span></p></td>
<td><p><span data-ttu-id="3bbc0-139">Имя иерархии.</span><span class="sxs-lookup"><span data-stu-id="3bbc0-139">The name of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bbc0-140">HierarchyUniqueName</span><span class="sxs-lookup"><span data-stu-id="3bbc0-140">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="3bbc0-141">Однозначное имя иерархии.</span><span class="sxs-lookup"><span data-stu-id="3bbc0-141">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bbc0-142">SchemaName</span><span class="sxs-lookup"><span data-stu-id="3bbc0-142">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="3bbc0-143">Имя схемы, к которой принадлежит этот куб.</span><span class="sxs-lookup"><span data-stu-id="3bbc0-143">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

