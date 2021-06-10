---
title: Объект Dimension (ADO MD)
TOCTitle: Dimension object (ADO MD)
ms:assetid: 12f43cfc-c74e-a2e8-7f6e-75fc68472c4b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248902(v=office.15)
ms:contentKeyID: 48543355
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: afea442aa535660b5bb618297640db8fbd546dec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293898"
---
# <a name="dimension-object-ado-md"></a><span data-ttu-id="7db95-102">Объект Dimension (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="7db95-102">Dimension object (ADO MD)</span></span>


<span data-ttu-id="7db95-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7db95-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7db95-104">Представляет одно из измерений многомерного куба, содержащего одну или несколько иерархий участников.</span><span class="sxs-lookup"><span data-stu-id="7db95-104">Represents one of the dimensions of a multidimensional cube, containing one or more hierarchies of members.</span></span>

## <a name="remarks"></a><span data-ttu-id="7db95-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="7db95-105">Remarks</span></span>

<span data-ttu-id="7db95-106">С помощью коллекций и свойств объекта **Dimension** можно сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="7db95-106">With the collections and properties of a **Dimension** object, you can do the following:</span></span>

  - <span data-ttu-id="7db95-107">Определите **измерение** с [свойствами Name](name-property-ado-md.md) и [UniqueName.](uniquename-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="7db95-107">Identify the **Dimension** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="7db95-108">Возвращаем значимую строку, описываемую **измерение** с [свойством Description.](description-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="7db95-108">Return a meaningful string that describes the **Dimension** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="7db95-109">Возвращаем [объекты Иерархия,](hierarchy-object-ado-md.md) которые составляют **Измерение** с [коллекцией Иерархии.](hierarchies-collection-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="7db95-109">Return the [Hierarchy](hierarchy-object-ado-md.md) objects that make up the **Dimension** with the [Hierarchies](hierarchies-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="7db95-110">Используйте стандартную коллекцию свойств ADO [для](properties-collection-ado.md) получения дополнительных сведений об **объекте Dimension.**</span><span class="sxs-lookup"><span data-stu-id="7db95-110">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Dimension** object.</span></span>

<span data-ttu-id="7db95-111">Коллекция **свойств** содержит свойства, предоставленные поставщиком.</span><span class="sxs-lookup"><span data-stu-id="7db95-111">The **Properties** collection contains provider-supplied properties.</span></span> <span data-ttu-id="7db95-112">В следующей таблице перечислены свойства, которые могут быть доступны.</span><span class="sxs-lookup"><span data-stu-id="7db95-112">The following table lists properties that might be available.</span></span> <span data-ttu-id="7db95-113">Фактический список свойств может отличаться в зависимости от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="7db95-113">The actual property list may differ depending upon the implementation of the provider.</span></span> <span data-ttu-id="7db95-114">Дополнительный список доступных свойств см. в документации для поставщика.</span><span class="sxs-lookup"><span data-stu-id="7db95-114">See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7db95-115">Имя</span><span class="sxs-lookup"><span data-stu-id="7db95-115">Name</span></span></p></th>
<th><p><span data-ttu-id="7db95-116">Описание</span><span class="sxs-lookup"><span data-stu-id="7db95-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7db95-117">CatalogName</span><span class="sxs-lookup"><span data-stu-id="7db95-117">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="7db95-118">Имя каталога, к которому принадлежит этот куб.</span><span class="sxs-lookup"><span data-stu-id="7db95-118">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7db95-119">CubeName</span><span class="sxs-lookup"><span data-stu-id="7db95-119">CubeName</span></span></p></td>
<td><p><span data-ttu-id="7db95-120">Имя куба.</span><span class="sxs-lookup"><span data-stu-id="7db95-120">The name of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7db95-121">DefaultHierarchy</span><span class="sxs-lookup"><span data-stu-id="7db95-121">DefaultHierarchy</span></span></p></td>
<td><p><span data-ttu-id="7db95-122">Уникальное имя иерархии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7db95-122">The unique name of the default hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7db95-123">Description</span><span class="sxs-lookup"><span data-stu-id="7db95-123">Description</span></span></p></td>
<td><p><span data-ttu-id="7db95-124">Содержательное описание куба.</span><span class="sxs-lookup"><span data-stu-id="7db95-124">A meaningful description of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7db95-125">DimensionCaption</span><span class="sxs-lookup"><span data-stu-id="7db95-125">DimensionCaption</span></span></p></td>
<td><p><span data-ttu-id="7db95-126">Метка или подпись, связанные с измерением.</span><span class="sxs-lookup"><span data-stu-id="7db95-126">A label or caption associated with the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7db95-127">DimensionCardinality</span><span class="sxs-lookup"><span data-stu-id="7db95-127">DimensionCardinality</span></span></p></td>
<td><p><span data-ttu-id="7db95-128">Количество участников в измерении.</span><span class="sxs-lookup"><span data-stu-id="7db95-128">The number of members in the dimension.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7db95-129">DimensionGUID</span><span class="sxs-lookup"><span data-stu-id="7db95-129">DimensionGUID</span></span></p></td>
<td><p><span data-ttu-id="7db95-130">GUID измерения.</span><span class="sxs-lookup"><span data-stu-id="7db95-130">The GUID of the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7db95-131">DimensionName</span><span class="sxs-lookup"><span data-stu-id="7db95-131">DimensionName</span></span></p></td>
<td><p><span data-ttu-id="7db95-132">Имя измерения.</span><span class="sxs-lookup"><span data-stu-id="7db95-132">The name of the dimension.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7db95-133">DimensionOrdinal</span><span class="sxs-lookup"><span data-stu-id="7db95-133">DimensionOrdinal</span></span></p></td>
<td><p><span data-ttu-id="7db95-134">Ordinal number of the dimension among the group of dimensions that form the cube.</span><span class="sxs-lookup"><span data-stu-id="7db95-134">The ordinal number of the dimension among the group of dimensions that form the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7db95-135">DimensionType</span><span class="sxs-lookup"><span data-stu-id="7db95-135">DimensionType</span></span></p></td>
<td><p><span data-ttu-id="7db95-136">Тип измерения.</span><span class="sxs-lookup"><span data-stu-id="7db95-136">The dimension type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7db95-137">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="7db95-137">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="7db95-138">Однозначное имя измерения.</span><span class="sxs-lookup"><span data-stu-id="7db95-138">The unambiguous name of the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7db95-139">SchemaName</span><span class="sxs-lookup"><span data-stu-id="7db95-139">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="7db95-140">Имя схемы, к которой принадлежит этот куб.</span><span class="sxs-lookup"><span data-stu-id="7db95-140">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

