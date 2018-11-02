---
title: Объект Dimension (ADO MD)
TOCTitle: Dimension object (ADO MD)
ms:assetid: 12f43cfc-c74e-a2e8-7f6e-75fc68472c4b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248902(v=office.15)
ms:contentKeyID: 48543355
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c3d42c01d1d9d4e77169f74afcc97d147d6f5d53
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921189"
---
# <a name="dimension-object-ado-md"></a><span data-ttu-id="45a12-102">Объект Dimension (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="45a12-102">Dimension object (ADO MD)</span></span>


<span data-ttu-id="45a12-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="45a12-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="45a12-104">Представляет один из измерения многомерного куба, содержащего иерархии один или несколько элементов.</span><span class="sxs-lookup"><span data-stu-id="45a12-104">Represents one of the dimensions of a multidimensional cube, containing one or more hierarchies of members.</span></span>

## <a name="remarks"></a><span data-ttu-id="45a12-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="45a12-105">Remarks</span></span>

<span data-ttu-id="45a12-106">Со свойствами объекта **измерения** и семейств сайтов выполните следующее:</span><span class="sxs-lookup"><span data-stu-id="45a12-106">With the collections and properties of a **Dimension** object, you can do the following:</span></span>

  - <span data-ttu-id="45a12-107">Определение **измерения** с помощью свойства [Name](name-property-ado-md.md) и [уникального имени](uniquename-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="45a12-107">Identify the **Dimension** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="45a12-108">Возвращает удобной для восприятия строка, описывающая **измерения** с помощью свойства [Description](description-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="45a12-108">Return a meaningful string that describes the **Dimension** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="45a12-109">Возвращает объекты [иерархии](hierarchy-object-ado-md.md) , которые составляют **измерения** с коллекцией [иерархии](hierarchies-collection-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="45a12-109">Return the [Hierarchy](hierarchy-object-ado-md.md) objects that make up the **Dimension** with the [Hierarchies](hierarchies-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="45a12-110">Используйте коллекцию стандартный ADO [Свойства](properties-collection-ado.md) для получения дополнительных сведений об объекте **измерения** .</span><span class="sxs-lookup"><span data-stu-id="45a12-110">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Dimension** object.</span></span>

<span data-ttu-id="45a12-111">Коллекции **свойств** содержит свойства, предоставленных поставщиком.</span><span class="sxs-lookup"><span data-stu-id="45a12-111">The **Properties** collection contains provider-supplied properties.</span></span> <span data-ttu-id="45a12-112">В следующей таблице перечислены свойства, которые могут быть недоступны.</span><span class="sxs-lookup"><span data-stu-id="45a12-112">The following table lists properties that might be available.</span></span> <span data-ttu-id="45a12-113">Список свойств фактический может различаться в зависимости от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="45a12-113">The actual property list may differ depending upon the implementation of the provider.</span></span> <span data-ttu-id="45a12-114">Обратитесь к документации вашего поставщика для получения более полного списка доступных свойств.</span><span class="sxs-lookup"><span data-stu-id="45a12-114">See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="45a12-115">Имя</span><span class="sxs-lookup"><span data-stu-id="45a12-115">Name</span></span></p></th>
<th><p><span data-ttu-id="45a12-116">Описание</span><span class="sxs-lookup"><span data-stu-id="45a12-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45a12-117">ИмяКаталога</span><span class="sxs-lookup"><span data-stu-id="45a12-117">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="45a12-118">Имя каталога, к которому принадлежит этот куб.</span><span class="sxs-lookup"><span data-stu-id="45a12-118">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45a12-119">Имя куба</span><span class="sxs-lookup"><span data-stu-id="45a12-119">CubeName</span></span></p></td>
<td><p><span data-ttu-id="45a12-120">Имя куба.</span><span class="sxs-lookup"><span data-stu-id="45a12-120">The name of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45a12-121">DefaultHierarchy</span><span class="sxs-lookup"><span data-stu-id="45a12-121">DefaultHierarchy</span></span></p></td>
<td><p><span data-ttu-id="45a12-122">Уникальное имя иерархии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="45a12-122">The unique name of the default hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45a12-123">Описание</span><span class="sxs-lookup"><span data-stu-id="45a12-123">Description</span></span></p></td>
<td><p><span data-ttu-id="45a12-124">Понятное описание куба.</span><span class="sxs-lookup"><span data-stu-id="45a12-124">A meaningful description of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45a12-125">DimensionCaption</span><span class="sxs-lookup"><span data-stu-id="45a12-125">DimensionCaption</span></span></p></td>
<td><p><span data-ttu-id="45a12-126">Метка или заголовок, связанный с измерения.</span><span class="sxs-lookup"><span data-stu-id="45a12-126">A label or caption associated with the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45a12-127">DimensionCardinality</span><span class="sxs-lookup"><span data-stu-id="45a12-127">DimensionCardinality</span></span></p></td>
<td><p><span data-ttu-id="45a12-128">Количество элементов измерения.</span><span class="sxs-lookup"><span data-stu-id="45a12-128">The number of members in the dimension.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45a12-129">DimensionGUID</span><span class="sxs-lookup"><span data-stu-id="45a12-129">DimensionGUID</span></span></p></td>
<td><p><span data-ttu-id="45a12-130">Идентификатор GUID, измерения.</span><span class="sxs-lookup"><span data-stu-id="45a12-130">The GUID of the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45a12-131">Имя измерения</span><span class="sxs-lookup"><span data-stu-id="45a12-131">DimensionName</span></span></p></td>
<td><p><span data-ttu-id="45a12-132">Имя измерения.</span><span class="sxs-lookup"><span data-stu-id="45a12-132">The name of the dimension.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45a12-133">DimensionOrdinal</span><span class="sxs-lookup"><span data-stu-id="45a12-133">DimensionOrdinal</span></span></p></td>
<td><p><span data-ttu-id="45a12-134">Порядковый номер измерения между группы измерений, формирующих куба.</span><span class="sxs-lookup"><span data-stu-id="45a12-134">The ordinal number of the dimension among the group of dimensions that form the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45a12-135">DimensionType</span><span class="sxs-lookup"><span data-stu-id="45a12-135">DimensionType</span></span></p></td>
<td><p><span data-ttu-id="45a12-136">Тип аналитики.</span><span class="sxs-lookup"><span data-stu-id="45a12-136">The dimension type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45a12-137">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="45a12-137">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="45a12-138">Однозначное имя измерения.</span><span class="sxs-lookup"><span data-stu-id="45a12-138">The unambiguous name of the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45a12-139">SchemaName</span><span class="sxs-lookup"><span data-stu-id="45a12-139">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="45a12-140">Имя схемы, к которой принадлежит этот куб.</span><span class="sxs-lookup"><span data-stu-id="45a12-140">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

