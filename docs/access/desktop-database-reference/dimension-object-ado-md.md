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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712829"
---
# <a name="dimension-object-ado-md"></a><span data-ttu-id="69063-102">Объект Dimension (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="69063-102">Dimension object (ADO MD)</span></span>


<span data-ttu-id="69063-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="69063-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="69063-104">Представляет один из измерения многомерного куба, содержащего иерархии один или несколько элементов.</span><span class="sxs-lookup"><span data-stu-id="69063-104">Represents one of the dimensions of a multidimensional cube, containing one or more hierarchies of members.</span></span>

## <a name="remarks"></a><span data-ttu-id="69063-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="69063-105">Remarks</span></span>

<span data-ttu-id="69063-106">Со свойствами объекта **измерения** и семейств сайтов выполните следующее:</span><span class="sxs-lookup"><span data-stu-id="69063-106">With the collections and properties of a **Dimension** object, you can do the following:</span></span>

  - <span data-ttu-id="69063-107">Определение **измерения** с помощью свойства [Name](name-property-ado-md.md) и [уникального имени](uniquename-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="69063-107">Identify the **Dimension** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="69063-108">Возвращает удобной для восприятия строка, описывающая **измерения** с помощью свойства [Description](description-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="69063-108">Return a meaningful string that describes the **Dimension** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="69063-109">Возвращает объекты [иерархии](hierarchy-object-ado-md.md) , которые составляют **измерения** с коллекцией [иерархии](hierarchies-collection-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="69063-109">Return the [Hierarchy](hierarchy-object-ado-md.md) objects that make up the **Dimension** with the [Hierarchies](hierarchies-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="69063-110">Используйте коллекцию стандартный ADO [Свойства](properties-collection-ado.md) для получения дополнительных сведений об объекте **измерения** .</span><span class="sxs-lookup"><span data-stu-id="69063-110">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Dimension** object.</span></span>

<span data-ttu-id="69063-111">Коллекции **свойств** содержит свойства, предоставленных поставщиком.</span><span class="sxs-lookup"><span data-stu-id="69063-111">The **Properties** collection contains provider-supplied properties.</span></span> <span data-ttu-id="69063-112">В следующей таблице перечислены свойства, которые могут быть недоступны.</span><span class="sxs-lookup"><span data-stu-id="69063-112">The following table lists properties that might be available.</span></span> <span data-ttu-id="69063-113">Список свойств фактический может различаться в зависимости от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="69063-113">The actual property list may differ depending upon the implementation of the provider.</span></span> <span data-ttu-id="69063-114">Обратитесь к документации вашего поставщика для получения более полного списка доступных свойств.</span><span class="sxs-lookup"><span data-stu-id="69063-114">See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="69063-115">Имя</span><span class="sxs-lookup"><span data-stu-id="69063-115">Name</span></span></p></th>
<th><p><span data-ttu-id="69063-116">Описание</span><span class="sxs-lookup"><span data-stu-id="69063-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="69063-117">ИмяКаталога</span><span class="sxs-lookup"><span data-stu-id="69063-117">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="69063-118">Имя каталога, к которому принадлежит этот куб.</span><span class="sxs-lookup"><span data-stu-id="69063-118">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69063-119">Имя куба</span><span class="sxs-lookup"><span data-stu-id="69063-119">CubeName</span></span></p></td>
<td><p><span data-ttu-id="69063-120">Имя куба.</span><span class="sxs-lookup"><span data-stu-id="69063-120">The name of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69063-121">DefaultHierarchy</span><span class="sxs-lookup"><span data-stu-id="69063-121">DefaultHierarchy</span></span></p></td>
<td><p><span data-ttu-id="69063-122">Уникальное имя иерархии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="69063-122">The unique name of the default hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69063-123">Описание</span><span class="sxs-lookup"><span data-stu-id="69063-123">Description</span></span></p></td>
<td><p><span data-ttu-id="69063-124">Понятное описание куба.</span><span class="sxs-lookup"><span data-stu-id="69063-124">A meaningful description of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69063-125">DimensionCaption</span><span class="sxs-lookup"><span data-stu-id="69063-125">DimensionCaption</span></span></p></td>
<td><p><span data-ttu-id="69063-126">Метка или заголовок, связанный с измерения.</span><span class="sxs-lookup"><span data-stu-id="69063-126">A label or caption associated with the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69063-127">DimensionCardinality</span><span class="sxs-lookup"><span data-stu-id="69063-127">DimensionCardinality</span></span></p></td>
<td><p><span data-ttu-id="69063-128">Количество элементов измерения.</span><span class="sxs-lookup"><span data-stu-id="69063-128">The number of members in the dimension.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69063-129">DimensionGUID</span><span class="sxs-lookup"><span data-stu-id="69063-129">DimensionGUID</span></span></p></td>
<td><p><span data-ttu-id="69063-130">Идентификатор GUID, измерения.</span><span class="sxs-lookup"><span data-stu-id="69063-130">The GUID of the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69063-131">Имя измерения</span><span class="sxs-lookup"><span data-stu-id="69063-131">DimensionName</span></span></p></td>
<td><p><span data-ttu-id="69063-132">Имя измерения.</span><span class="sxs-lookup"><span data-stu-id="69063-132">The name of the dimension.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69063-133">DimensionOrdinal</span><span class="sxs-lookup"><span data-stu-id="69063-133">DimensionOrdinal</span></span></p></td>
<td><p><span data-ttu-id="69063-134">Порядковый номер измерения между группы измерений, формирующих куба.</span><span class="sxs-lookup"><span data-stu-id="69063-134">The ordinal number of the dimension among the group of dimensions that form the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69063-135">DimensionType</span><span class="sxs-lookup"><span data-stu-id="69063-135">DimensionType</span></span></p></td>
<td><p><span data-ttu-id="69063-136">Тип аналитики.</span><span class="sxs-lookup"><span data-stu-id="69063-136">The dimension type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69063-137">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="69063-137">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="69063-138">Однозначное имя измерения.</span><span class="sxs-lookup"><span data-stu-id="69063-138">The unambiguous name of the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69063-139">SchemaName</span><span class="sxs-lookup"><span data-stu-id="69063-139">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="69063-140">Имя схемы, к которой принадлежит этот куб.</span><span class="sxs-lookup"><span data-stu-id="69063-140">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

