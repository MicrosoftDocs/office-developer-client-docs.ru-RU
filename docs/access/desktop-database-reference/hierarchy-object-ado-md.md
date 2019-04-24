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
# <a name="hierarchy-object-ado-md"></a><span data-ttu-id="79aec-102">Объект Hierarchy (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="79aec-102">Hierarchy object (ADO MD)</span></span>


<span data-ttu-id="79aec-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="79aec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="79aec-104">Представляет один из способов, с помощью которого можно выполнить статистическую настройку элементов [измерения](dimension-object-ado-md.md) или выполнить их сведение.</span><span class="sxs-lookup"><span data-stu-id="79aec-104">Represents one way in which the members of a [dimension](dimension-object-ado-md.md) can be aggregated or "rolled up."</span></span> <span data-ttu-id="79aec-105">Измерение можно объединить вдоль одной или нескольких иерархий.</span><span class="sxs-lookup"><span data-stu-id="79aec-105">A dimension can be aggregated along one or more hierarchies.</span></span>

## <a name="remarks"></a><span data-ttu-id="79aec-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="79aec-106">Remarks</span></span>

<span data-ttu-id="79aec-107">С помощью коллекций и свойств объекта **иерархии** можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="79aec-107">With the collections and properties of a **Hierarchy** object, you can do the following:</span></span>

  - <span data-ttu-id="79aec-108">Определите **иерархию** с помощью свойств [Name](name-property-ado-md.md) и [UniqueName](uniquename-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="79aec-108">Identify the **Hierarchy** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="79aec-109">Возвращает осмысленную строку, которая описывает **иерархию** со свойством [Description](description-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="79aec-109">Return a meaningful string that describes the **Hierarchy** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="79aec-110">Возвращает объекты [уровня](level-object-ado-md.md) , составляющие иерархию, \*\*\*\* с коллекцией [Levels](levels-collection-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="79aec-110">Return the [Level](level-object-ado-md.md) objects that make up the **Hierarchy** with the [Levels](levels-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="79aec-111">Используйте стандартную коллекцию [свойств](properties-collection-ado.md) ADO для получения дополнительных сведений об объекте **иерархии** .</span><span class="sxs-lookup"><span data-stu-id="79aec-111">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Hierarchy** object.</span></span>

<span data-ttu-id="79aec-112">Коллекция **Properties** содержит свойства, предоставляемые поставщиком.</span><span class="sxs-lookup"><span data-stu-id="79aec-112">The **Properties** collection contains provider-supplied properties.</span></span> <span data-ttu-id="79aec-113">В следующей таблице перечислены свойства, которые могут быть доступны.</span><span class="sxs-lookup"><span data-stu-id="79aec-113">The following table lists properties that might be available.</span></span> <span data-ttu-id="79aec-114">Фактический список свойств может различаться в зависимости от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="79aec-114">The actual property list may differ depending upon the implementation of the provider.</span></span> <span data-ttu-id="79aec-115">Просмотрите документацию для своего поставщика, чтобы получить полный список доступных свойств.</span><span class="sxs-lookup"><span data-stu-id="79aec-115">See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="79aec-116">Имя</span><span class="sxs-lookup"><span data-stu-id="79aec-116">Name</span></span></p></th>
<th><p><span data-ttu-id="79aec-117">Описание</span><span class="sxs-lookup"><span data-stu-id="79aec-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="79aec-118">Аллмембер</span><span class="sxs-lookup"><span data-stu-id="79aec-118">AllMember</span></span></p></td>
<td><p><span data-ttu-id="79aec-119">Элемент на высшем уровне свертки в иерархии.</span><span class="sxs-lookup"><span data-stu-id="79aec-119">The member at the highest level of rollup in the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79aec-120">Каталогнаме</span><span class="sxs-lookup"><span data-stu-id="79aec-120">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="79aec-121">Имя каталога, к которому принадлежит куб.</span><span class="sxs-lookup"><span data-stu-id="79aec-121">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79aec-122">Кубенаме</span><span class="sxs-lookup"><span data-stu-id="79aec-122">CubeName</span></span></p></td>
<td><p><span data-ttu-id="79aec-123">Имя куба.</span><span class="sxs-lookup"><span data-stu-id="79aec-123">The name of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79aec-124">DefaultMember</span><span class="sxs-lookup"><span data-stu-id="79aec-124">DefaultMember</span></span></p></td>
<td><p><span data-ttu-id="79aec-125">Уникальное имя элемента по умолчанию для этой иерархии.</span><span class="sxs-lookup"><span data-stu-id="79aec-125">The unique name of the default member for this hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79aec-126">Описание</span><span class="sxs-lookup"><span data-stu-id="79aec-126">Description</span></span></p></td>
<td><p><span data-ttu-id="79aec-127">Понятное описание иерархии.</span><span class="sxs-lookup"><span data-stu-id="79aec-127">A meaningful description of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79aec-128">Дименсионтипе</span><span class="sxs-lookup"><span data-stu-id="79aec-128">DimensionType</span></span></p></td>
<td><p><span data-ttu-id="79aec-129">Тип измерения, к которому относится данная иерархия.</span><span class="sxs-lookup"><span data-stu-id="79aec-129">The type of dimension to which this hierarchy belongs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79aec-130">Дименсионуникуенаме</span><span class="sxs-lookup"><span data-stu-id="79aec-130">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="79aec-131">Неоднозначное имя измерения.</span><span class="sxs-lookup"><span data-stu-id="79aec-131">The unambiguous name of the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79aec-132">Хиерарчикаптион</span><span class="sxs-lookup"><span data-stu-id="79aec-132">HierarchyCaption</span></span></p></td>
<td><p><span data-ttu-id="79aec-133">Метка или заголовок, связанные с иерархией.</span><span class="sxs-lookup"><span data-stu-id="79aec-133">A label or caption associated with the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79aec-134">Хиерарчикардиналити</span><span class="sxs-lookup"><span data-stu-id="79aec-134">HierarchyCardinality</span></span></p></td>
<td><p><span data-ttu-id="79aec-135">Число элементов в иерархии.</span><span class="sxs-lookup"><span data-stu-id="79aec-135">The number of members in the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79aec-136">Хиерарчигуид</span><span class="sxs-lookup"><span data-stu-id="79aec-136">HierarchyGUID</span></span></p></td>
<td><p><span data-ttu-id="79aec-137">GUID иерархии.</span><span class="sxs-lookup"><span data-stu-id="79aec-137">The GUID of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79aec-138">Хиерарчинаме</span><span class="sxs-lookup"><span data-stu-id="79aec-138">HierarchyName</span></span></p></td>
<td><p><span data-ttu-id="79aec-139">Имя иерархии.</span><span class="sxs-lookup"><span data-stu-id="79aec-139">The name of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79aec-140">Хиерарчюникуенаме</span><span class="sxs-lookup"><span data-stu-id="79aec-140">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="79aec-141">Неоднозначное имя иерархии.</span><span class="sxs-lookup"><span data-stu-id="79aec-141">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79aec-142">SchemaName</span><span class="sxs-lookup"><span data-stu-id="79aec-142">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="79aec-143">Имя схемы, к которой принадлежит куб.</span><span class="sxs-lookup"><span data-stu-id="79aec-143">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

