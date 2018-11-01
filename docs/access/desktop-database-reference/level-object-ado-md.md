---
title: Объект уровня (ADO MD)
TOCTitle: Level Object (ADO MD)
ms:assetid: ddbcabce-8777-1068-98a3-be209084f497
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250121(v=office.15)
ms:contentKeyID: 48548160
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d6137e35d43153d7d9d36f23e1bdbe9fc80a442d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881442"
---
# <a name="level-object-ado-md"></a><span data-ttu-id="74128-102">Объект уровня (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="74128-102">Level Object (ADO MD)</span></span>


<span data-ttu-id="74128-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="74128-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="74128-104">Содержит набор элементов, каждый из которых содержит один и тот же ранг в иерархии.</span><span class="sxs-lookup"><span data-stu-id="74128-104">Contains a set of members, each of which has the same rank within a hierarchy.</span></span>

## <a name="remarks"></a><span data-ttu-id="74128-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="74128-105">Remarks</span></span>

<span data-ttu-id="74128-106">Со свойствами объекта **уровень** и семейств сайтов выполните следующее:</span><span class="sxs-lookup"><span data-stu-id="74128-106">With the collections and properties of a **Level** object, you can do the following:</span></span>

  - <span data-ttu-id="74128-107">Определите **уровень** с помощью свойства [Name](name-property-ado-md.md) и [уникального имени](uniquename-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="74128-107">Identify the **Level** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="74128-108">Возвращает строку, используемую при отображении **уровень** с свойство [Caption](caption-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="74128-108">Return a string to use when displaying the **Level** with the [Caption](caption-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="74128-109">Возвращает удобной для восприятия строку, которая описывает **уровень** с помощью свойства [Description](description-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="74128-109">Return a meaningful string that describes the **Level** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="74128-110">Возвращают объекты [элементов](member-object-ado-md.md) , которые составляют **уровня** в коллекции [элементов](members-collection-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="74128-110">Return the [Member](member-object-ado-md.md) objects that make up the **Level** with the [Members](members-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="74128-111">Возвращает число уровней из корневой папки **уровень** со свойством [глубины](depth-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="74128-111">Return the number of levels from the root of the **Level** with the [Depth](depth-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="74128-112">Используйте коллекцию стандартный ADO [Свойства](properties-collection-ado.md) для получения дополнительных сведений об объекте **уровень** .</span><span class="sxs-lookup"><span data-stu-id="74128-112">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Level** object.</span></span>

<span data-ttu-id="74128-113">Коллекции **свойств** содержит свойства, предоставленных поставщиком.</span><span class="sxs-lookup"><span data-stu-id="74128-113">The **Properties** collection contains provider-supplied properties.</span></span> <span data-ttu-id="74128-114">В следующей таблице перечислены свойства, которые могут быть недоступны.</span><span class="sxs-lookup"><span data-stu-id="74128-114">The following table lists properties that might be available.</span></span> <span data-ttu-id="74128-115">Список свойств фактический может различаться в зависимости от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="74128-115">The actual property list may differ depending upon the implementation of the provider.</span></span> <span data-ttu-id="74128-116">Обратитесь к документации вашего поставщика для получения более полного списка доступных свойств.</span><span class="sxs-lookup"><span data-stu-id="74128-116">See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="74128-117">Имя</span><span class="sxs-lookup"><span data-stu-id="74128-117">Name</span></span></p></th>
<th><p><span data-ttu-id="74128-118">Описание</span><span class="sxs-lookup"><span data-stu-id="74128-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="74128-119">ИмяКаталога</span><span class="sxs-lookup"><span data-stu-id="74128-119">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="74128-120">Имя каталога, к которому принадлежит этот куб.</span><span class="sxs-lookup"><span data-stu-id="74128-120">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74128-121">Имя куба</span><span class="sxs-lookup"><span data-stu-id="74128-121">CubeName</span></span></p></td>
<td><p><span data-ttu-id="74128-122">Имя куба.</span><span class="sxs-lookup"><span data-stu-id="74128-122">The name of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74128-123">Описание</span><span class="sxs-lookup"><span data-stu-id="74128-123">Description</span></span></p></td>
<td><p><span data-ttu-id="74128-124">Понятное описание уровня.</span><span class="sxs-lookup"><span data-stu-id="74128-124">A meaningful description of the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74128-125">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="74128-125">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="74128-126">Однозначное имя <a href="dimension-object-ado-md.md">измерения</a>.</span><span class="sxs-lookup"><span data-stu-id="74128-126">The unambiguous name of the <a href="dimension-object-ado-md.md">dimension</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74128-127">HierarchyUniqueName</span><span class="sxs-lookup"><span data-stu-id="74128-127">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="74128-128">Однозначное имя иерархии.</span><span class="sxs-lookup"><span data-stu-id="74128-128">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74128-129">LevelCaption</span><span class="sxs-lookup"><span data-stu-id="74128-129">LevelCaption</span></span></p></td>
<td><p><span data-ttu-id="74128-130">Метка или заголовок, связанный с уровнем.</span><span class="sxs-lookup"><span data-stu-id="74128-130">A label or caption associated with the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74128-131">LevelCardinality</span><span class="sxs-lookup"><span data-stu-id="74128-131">LevelCardinality</span></span></p></td>
<td><p><span data-ttu-id="74128-132">Количество элементов на этом уровне.</span><span class="sxs-lookup"><span data-stu-id="74128-132">The number of members in the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74128-133">LevelGUID</span><span class="sxs-lookup"><span data-stu-id="74128-133">LevelGUID</span></span></p></td>
<td><p><span data-ttu-id="74128-134">Идентификатор GUID уровня.</span><span class="sxs-lookup"><span data-stu-id="74128-134">The GUID of the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74128-135">LevelName</span><span class="sxs-lookup"><span data-stu-id="74128-135">LevelName</span></span></p></td>
<td><p><span data-ttu-id="74128-136">Имя уровня.</span><span class="sxs-lookup"><span data-stu-id="74128-136">Name of the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74128-137">LevelNumber</span><span class="sxs-lookup"><span data-stu-id="74128-137">LevelNumber</span></span></p></td>
<td><p><span data-ttu-id="74128-138">Расстояние между на уровне и корень иерархии.</span><span class="sxs-lookup"><span data-stu-id="74128-138">The distance between the level and the root of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74128-139">LevelType</span><span class="sxs-lookup"><span data-stu-id="74128-139">LevelType</span></span></p></td>
<td><p><span data-ttu-id="74128-140">Тип уровня.</span><span class="sxs-lookup"><span data-stu-id="74128-140">The type of level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74128-141">LevelUniqueName</span><span class="sxs-lookup"><span data-stu-id="74128-141">LevelUniqueName</span></span></p></td>
<td><p><span data-ttu-id="74128-142">Однозначное имя уровня.</span><span class="sxs-lookup"><span data-stu-id="74128-142">The unambiguous name of the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74128-143">SchemaName</span><span class="sxs-lookup"><span data-stu-id="74128-143">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="74128-144">Имя схемы, к которой принадлежит этот куб.</span><span class="sxs-lookup"><span data-stu-id="74128-144">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

