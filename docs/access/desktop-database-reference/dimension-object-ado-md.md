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
# <a name="dimension-object-ado-md"></a><span data-ttu-id="17967-102">Объект Dimension (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="17967-102">Dimension object (ADO MD)</span></span>


<span data-ttu-id="17967-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="17967-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="17967-104">Представляет один из измерений многомерного куба, содержащий одну или несколько иерархий элементов.</span><span class="sxs-lookup"><span data-stu-id="17967-104">Represents one of the dimensions of a multidimensional cube, containing one or more hierarchies of members.</span></span>

## <a name="remarks"></a><span data-ttu-id="17967-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="17967-105">Remarks</span></span>

<span data-ttu-id="17967-106">Используя коллекции и свойства объекта **измерения** , можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="17967-106">With the collections and properties of a **Dimension** object, you can do the following:</span></span>

  - <span data-ttu-id="17967-107">Определите **размерность** с помощью свойств [Name](name-property-ado-md.md) и [UniqueName](uniquename-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="17967-107">Identify the **Dimension** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="17967-108">Возвращает осмысленную строку, описывающую **измерение** , с помощью свойства [Description](description-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="17967-108">Return a meaningful string that describes the **Dimension** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="17967-109">Возвращает объекты [иерархии](hierarchy-object-ado-md.md) , которые составляют **измерение** , с помощью коллекции [иерархий](hierarchies-collection-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="17967-109">Return the [Hierarchy](hierarchy-object-ado-md.md) objects that make up the **Dimension** with the [Hierarchies](hierarchies-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="17967-110">Используйте стандартные коллекции [свойств](properties-collection-ado.md) ADO для получения дополнительных сведений об объекте **измерения** .</span><span class="sxs-lookup"><span data-stu-id="17967-110">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Dimension** object.</span></span>

<span data-ttu-id="17967-111">Коллекция **Properties** содержит свойства, предоставляемые поставщиком.</span><span class="sxs-lookup"><span data-stu-id="17967-111">The **Properties** collection contains provider-supplied properties.</span></span> <span data-ttu-id="17967-112">В следующей таблице перечислены свойства, которые могут быть доступны.</span><span class="sxs-lookup"><span data-stu-id="17967-112">The following table lists properties that might be available.</span></span> <span data-ttu-id="17967-113">Фактический список свойств может различаться в зависимости от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="17967-113">The actual property list may differ depending upon the implementation of the provider.</span></span> <span data-ttu-id="17967-114">Просмотрите документацию для своего поставщика, чтобы получить полный список доступных свойств.</span><span class="sxs-lookup"><span data-stu-id="17967-114">See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="17967-115">Имя</span><span class="sxs-lookup"><span data-stu-id="17967-115">Name</span></span></p></th>
<th><p><span data-ttu-id="17967-116">Описание</span><span class="sxs-lookup"><span data-stu-id="17967-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17967-117">Каталогнаме</span><span class="sxs-lookup"><span data-stu-id="17967-117">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="17967-118">Имя каталога, к которому принадлежит куб.</span><span class="sxs-lookup"><span data-stu-id="17967-118">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17967-119">Кубенаме</span><span class="sxs-lookup"><span data-stu-id="17967-119">CubeName</span></span></p></td>
<td><p><span data-ttu-id="17967-120">Имя куба.</span><span class="sxs-lookup"><span data-stu-id="17967-120">The name of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17967-121">Дефаулсиерарчи</span><span class="sxs-lookup"><span data-stu-id="17967-121">DefaultHierarchy</span></span></p></td>
<td><p><span data-ttu-id="17967-122">Уникальное имя иерархии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="17967-122">The unique name of the default hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17967-123">Описание</span><span class="sxs-lookup"><span data-stu-id="17967-123">Description</span></span></p></td>
<td><p><span data-ttu-id="17967-124">Понятное описание Куба.</span><span class="sxs-lookup"><span data-stu-id="17967-124">A meaningful description of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17967-125">Дименсионкаптион</span><span class="sxs-lookup"><span data-stu-id="17967-125">DimensionCaption</span></span></p></td>
<td><p><span data-ttu-id="17967-126">Метка или подпись, связанная с измерением.</span><span class="sxs-lookup"><span data-stu-id="17967-126">A label or caption associated with the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17967-127">Дименсионкардиналити</span><span class="sxs-lookup"><span data-stu-id="17967-127">DimensionCardinality</span></span></p></td>
<td><p><span data-ttu-id="17967-128">Число элементов в измерении.</span><span class="sxs-lookup"><span data-stu-id="17967-128">The number of members in the dimension.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17967-129">Дименсионгуид</span><span class="sxs-lookup"><span data-stu-id="17967-129">DimensionGUID</span></span></p></td>
<td><p><span data-ttu-id="17967-130">GUID измерения.</span><span class="sxs-lookup"><span data-stu-id="17967-130">The GUID of the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17967-131">Дименсионнаме</span><span class="sxs-lookup"><span data-stu-id="17967-131">DimensionName</span></span></p></td>
<td><p><span data-ttu-id="17967-132">Имя измерения.</span><span class="sxs-lookup"><span data-stu-id="17967-132">The name of the dimension.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17967-133">Дименсионординал</span><span class="sxs-lookup"><span data-stu-id="17967-133">DimensionOrdinal</span></span></p></td>
<td><p><span data-ttu-id="17967-134">Порядковый номер измерения между группами измерений, которые формируют куб.</span><span class="sxs-lookup"><span data-stu-id="17967-134">The ordinal number of the dimension among the group of dimensions that form the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17967-135">Дименсионтипе</span><span class="sxs-lookup"><span data-stu-id="17967-135">DimensionType</span></span></p></td>
<td><p><span data-ttu-id="17967-136">Тип измерения.</span><span class="sxs-lookup"><span data-stu-id="17967-136">The dimension type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17967-137">Дименсионуникуенаме</span><span class="sxs-lookup"><span data-stu-id="17967-137">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="17967-138">Неоднозначное имя измерения.</span><span class="sxs-lookup"><span data-stu-id="17967-138">The unambiguous name of the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17967-139">SchemaName</span><span class="sxs-lookup"><span data-stu-id="17967-139">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="17967-140">Имя схемы, к которой принадлежит куб.</span><span class="sxs-lookup"><span data-stu-id="17967-140">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

