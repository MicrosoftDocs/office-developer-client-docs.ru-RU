---
title: Объект Level (ADO MD)
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
# <a name="level-object-ado-md"></a><span data-ttu-id="75224-102">Объект Level (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="75224-102">Level object (ADO MD)</span></span>


<span data-ttu-id="75224-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="75224-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="75224-104">Содержит набор элементов, каждый из которых имеет одинаковый ранг в иерархии.</span><span class="sxs-lookup"><span data-stu-id="75224-104">Contains a set of members, each of which has the same rank within a hierarchy.</span></span>

## <a name="remarks"></a><span data-ttu-id="75224-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="75224-105">Remarks</span></span>

<span data-ttu-id="75224-106">С помощью коллекций и свойств объекта **Level** можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="75224-106">With the collections and properties of a **Level** object, you can do the following:</span></span>

  - <span data-ttu-id="75224-107">Определите **уровень** с помощью свойств [Name](name-property-ado-md.md) и [UniqueName](uniquename-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="75224-107">Identify the **Level** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="75224-108">Возвращает строку, используемую при отображении **уровня** со свойством [Caption](caption-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="75224-108">Return a string to use when displaying the **Level** with the [Caption](caption-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="75224-109">Возвращает осмысленную строку, описывающую **уровень** с помощью свойства [Description](description-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="75224-109">Return a meaningful string that describes the **Level** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="75224-110">Возвращает объекты [member](member-object-ado-md.md) , составляющие **уровень** , с коллекцией [Members](members-collection-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="75224-110">Return the [Member](member-object-ado-md.md) objects that make up the **Level** with the [Members](members-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="75224-111">Возвращает количество уровней из корня **уровня** со свойством [Depth](depth-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="75224-111">Return the number of levels from the root of the **Level** with the [Depth](depth-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="75224-112">Используйте стандартную коллекцию [свойств](properties-collection-ado.md) ADO для получения дополнительных сведений об объекте **Level** .</span><span class="sxs-lookup"><span data-stu-id="75224-112">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Level** object.</span></span>

<span data-ttu-id="75224-113">Коллекция **Properties** содержит свойства, предоставляемые поставщиком.</span><span class="sxs-lookup"><span data-stu-id="75224-113">The **Properties** collection contains provider-supplied properties.</span></span> <span data-ttu-id="75224-114">В следующей таблице перечислены свойства, которые могут быть доступны.</span><span class="sxs-lookup"><span data-stu-id="75224-114">The following table lists properties that might be available.</span></span> <span data-ttu-id="75224-115">Фактический список свойств может различаться в зависимости от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="75224-115">The actual property list may differ depending upon the implementation of the provider.</span></span> <span data-ttu-id="75224-116">Просмотрите документацию для своего поставщика, чтобы получить полный список доступных свойств.</span><span class="sxs-lookup"><span data-stu-id="75224-116">See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="75224-117">Имя</span><span class="sxs-lookup"><span data-stu-id="75224-117">Name</span></span></p></th>
<th><p><span data-ttu-id="75224-118">Описание</span><span class="sxs-lookup"><span data-stu-id="75224-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75224-119">каталогнаме</span><span class="sxs-lookup"><span data-stu-id="75224-119">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="75224-120">Имя каталога, к которому принадлежит куб.</span><span class="sxs-lookup"><span data-stu-id="75224-120">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75224-121">кубенаме</span><span class="sxs-lookup"><span data-stu-id="75224-121">CubeName</span></span></p></td>
<td><p><span data-ttu-id="75224-122">Имя куба.</span><span class="sxs-lookup"><span data-stu-id="75224-122">The name of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75224-123">Описание</span><span class="sxs-lookup"><span data-stu-id="75224-123">Description</span></span></p></td>
<td><p><span data-ttu-id="75224-124">Понятное описание уровня.</span><span class="sxs-lookup"><span data-stu-id="75224-124">A meaningful description of the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75224-125">дименсионуникуенаме</span><span class="sxs-lookup"><span data-stu-id="75224-125">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="75224-126">Неоднозначное имя <a href="dimension-object-ado-md.md">измерения</a>.</span><span class="sxs-lookup"><span data-stu-id="75224-126">The unambiguous name of the <a href="dimension-object-ado-md.md">dimension</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75224-127">хиерарчюникуенаме</span><span class="sxs-lookup"><span data-stu-id="75224-127">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="75224-128">Неоднозначное имя иерархии.</span><span class="sxs-lookup"><span data-stu-id="75224-128">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75224-129">левелкаптион</span><span class="sxs-lookup"><span data-stu-id="75224-129">LevelCaption</span></span></p></td>
<td><p><span data-ttu-id="75224-130">Метка или заголовок, связанные с уровнем.</span><span class="sxs-lookup"><span data-stu-id="75224-130">A label or caption associated with the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75224-131">левелкардиналити</span><span class="sxs-lookup"><span data-stu-id="75224-131">LevelCardinality</span></span></p></td>
<td><p><span data-ttu-id="75224-132">Количество элементов на уровне.</span><span class="sxs-lookup"><span data-stu-id="75224-132">The number of members in the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75224-133">левелгуид</span><span class="sxs-lookup"><span data-stu-id="75224-133">LevelGUID</span></span></p></td>
<td><p><span data-ttu-id="75224-134">GUID уровня.</span><span class="sxs-lookup"><span data-stu-id="75224-134">The GUID of the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75224-135">LevelName</span><span class="sxs-lookup"><span data-stu-id="75224-135">LevelName</span></span></p></td>
<td><p><span data-ttu-id="75224-136">Имя уровня.</span><span class="sxs-lookup"><span data-stu-id="75224-136">Name of the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75224-137">левелнумбер</span><span class="sxs-lookup"><span data-stu-id="75224-137">LevelNumber</span></span></p></td>
<td><p><span data-ttu-id="75224-138">Расстояние между уровнем и корнем иерархии.</span><span class="sxs-lookup"><span data-stu-id="75224-138">The distance between the level and the root of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75224-139">левелтипе</span><span class="sxs-lookup"><span data-stu-id="75224-139">LevelType</span></span></p></td>
<td><p><span data-ttu-id="75224-140">Тип уровня.</span><span class="sxs-lookup"><span data-stu-id="75224-140">The type of level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75224-141">левелуникуенаме</span><span class="sxs-lookup"><span data-stu-id="75224-141">LevelUniqueName</span></span></p></td>
<td><p><span data-ttu-id="75224-142">Неоднозначное имя уровня.</span><span class="sxs-lookup"><span data-stu-id="75224-142">The unambiguous name of the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75224-143">SchemaName</span><span class="sxs-lookup"><span data-stu-id="75224-143">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="75224-144">Имя схемы, к которой принадлежит куб.</span><span class="sxs-lookup"><span data-stu-id="75224-144">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

