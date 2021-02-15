---
title: Объект Member (ADO MD)
TOCTitle: Member object (ADO MD)
ms:assetid: d80c024a-07dc-7a35-f8f2-b4d5b19d89e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250088(v=office.15)
ms:contentKeyID: 48548025
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 380fdf6c15f6774e27221e8500100870d22350c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289424"
---
# <a name="member-object-ado-md"></a><span data-ttu-id="c3b6e-102">Объект Member (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="c3b6e-102">Member object (ADO MD)</span></span>


<span data-ttu-id="c3b6e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c3b6e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c3b6e-104">Представляет элемент уровня в кубе, его детей или позицию вдоль оси ячеек.</span><span class="sxs-lookup"><span data-stu-id="c3b6e-104">Represents a member of a level in a cube, the children of a member of a level, or a member of a position along an axis of a cellset.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3b6e-105">Заметки</span><span class="sxs-lookup"><span data-stu-id="c3b6e-105">Remarks</span></span>

<span data-ttu-id="c3b6e-106">Свойства члена отличаются **в** зависимости от контекста, в котором он используется.</span><span class="sxs-lookup"><span data-stu-id="c3b6e-106">The properties of a **Member** differ depending on the context in which it is used.</span></span> <span data-ttu-id="c3b6e-107">У **члена** [уровня](level-object-ado-md.md) в [CubeDef](cubedef-object-ado-md.md) есть свойство [Children,](children-property-ado-md.md) которое возвращает члены на следующем нижнем уровне иерархии от текущего **члена.** </span><span class="sxs-lookup"><span data-stu-id="c3b6e-107">A **Member** of a [Level](level-object-ado-md.md) in a [CubeDef](cubedef-object-ado-md.md) has a [Children](children-property-ado-md.md) property that returns the **Members** on the next lower level in the hierarchy from the current **Member**.</span></span> <span data-ttu-id="c3b6e-108">Для  члена позиции [коллекция](position-object-ado-md.md) **Children** всегда пуста.</span><span class="sxs-lookup"><span data-stu-id="c3b6e-108">For a **Member** of a [Position](position-object-ado-md.md), the **Children** collection is always empty.</span></span> <span data-ttu-id="c3b6e-109">Кроме того, свойство [Type](type-property-ado-md.md) применяется только к **членам** **уровня.**</span><span class="sxs-lookup"><span data-stu-id="c3b6e-109">Also, the [Type](type-property-ado-md.md) property applies only to **Members** of a **Level**.</span></span>

<span data-ttu-id="c3b6e-110">Элемент **Позиции** **имеет** два свойства ( [DrilledDown](drilleddown-property-ado-md.md) и [ParentSameAsPrev),](parentsameasprev-property-ado-md.md) которые полезны при отобралении [cellset](cellset-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="c3b6e-110">A **Member** of **Position** has two properties — [DrilledDown](drilleddown-property-ado-md.md) and [ParentSameAsPrev](parentsameasprev-property-ado-md.md) — that are useful when displaying the [Cellset](cellset-object-ado-md.md).</span></span> <span data-ttu-id="c3b6e-111">При доступе к этим свойствам на  члене уровня произойдет **ошибка.**</span><span class="sxs-lookup"><span data-stu-id="c3b6e-111">An error will occur if these properties are accessed on a **Member** of a **Level**.</span></span>

<span data-ttu-id="c3b6e-112">С помощью коллекций и свойств объекта  **Member** уровня можно сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="c3b6e-112">With the collections and properties of a **Member** object of a **Level**, you can do the following:</span></span>

  - <span data-ttu-id="c3b6e-113">Определите **участника** со [свойствами Name](name-property-ado-md.md) и [UniqueName.](uniquename-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="c3b6e-113">Identify the **Member** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="c3b6e-114">Возвращает строку, которая будет применяться при отобраке **объекта Member** со [свойством Caption.](caption-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="c3b6e-114">Return a string to use when displaying the **Member** with the [Caption](caption-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="c3b6e-115">Возвращает осмысленные строки, описывая меру или **формулу Member со** [свойством Description.](description-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="c3b6e-115">Return a meaningful string that describes a measure or formula **Member** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="c3b6e-116">Определите природу члена **с** помощью свойства [Type.](type-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="c3b6e-116">Determine the nature of the **Member** with the [Type](type-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="c3b6e-117">Получите сведения об **уровне участника** **со** свойствами [LevelDepth](leveldepth-property-ado-md.md) и [LevelName.](levelname-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="c3b6e-117">Obtain information about the **Level** of the **Member** with the [LevelDepth](leveldepth-property-ado-md.md) and [LevelName](levelname-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="c3b6e-118">Получение **связанных членов** в [иерархии со](hierarchy-object-ado-md.md) свойствами [Parent](parent-property-ado-md.md) и [Children.](children-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="c3b6e-118">Obtain related **Members** in a [Hierarchy](hierarchy-object-ado-md.md) with the [Parent](parent-property-ado-md.md) and [Children](children-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="c3b6e-119">Посчитайте количество детей **члена с** помощью свойства [ChildCount.](childcount-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="c3b6e-119">Count the children of a **Member** with the [ChildCount](childcount-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="c3b6e-120">Используйте стандартную коллекцию [свойств](properties-collection-ado.md) ADO для получения дополнительных сведений об **объекте Level.**</span><span class="sxs-lookup"><span data-stu-id="c3b6e-120">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Level** object.</span></span>

<span data-ttu-id="c3b6e-121">С помощью коллекций и  свойств члена  позиции вдоль оси [можно](axis-object-ado-md.md)сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="c3b6e-121">With the collections and properties of a **Member** of a **Position** along an [Axis](axis-object-ado-md.md), you can do the following:</span></span>

  - <span data-ttu-id="c3b6e-122">Определите **участника** со [свойствами Name](name-property-ado-md.md) и [UniqueName.](uniquename-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="c3b6e-122">Identify the **Member** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="c3b6e-123">Возвращает строку, которая будет применяться при отобраке **объекта Member** со [свойством Caption.](caption-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="c3b6e-123">Return a string to use when displaying the **Member** with the [Caption](caption-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="c3b6e-124">Возвращает осмысленные строки, описывая меру или **формулу Member со** [свойством Description.](description-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="c3b6e-124">Return a meaningful string that describes a measure or formula **Member** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="c3b6e-125">Получите сведения об **уровне участника** **со** свойствами [LevelDepth](leveldepth-property-ado-md.md) и [LevelName.](levelname-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="c3b6e-125">Obtain information about the **Level** of the **Member** with the [LevelDepth](leveldepth-property-ado-md.md) and [LevelName](levelname-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="c3b6e-126">Посчитайте количество детей **члена с** помощью свойства [ChildCount.](childcount-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="c3b6e-126">Count the children of a **Member** with the [ChildCount](childcount-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="c3b6e-127">Используйте свойство [DrilledDown,](drilleddown-property-ado-md.md) чтобы определить, есть ли по крайней мере один child на оси **сразу** после этого **члена**.</span><span class="sxs-lookup"><span data-stu-id="c3b6e-127">Use the [DrilledDown](drilleddown-property-ado-md.md) property to determine whether there is at least one child on the **Axis** immediately following this **Member**.</span></span>

  - <span data-ttu-id="c3b6e-128">Используйте свойство [ParentSameAsPrev,](parentsameasprev-property-ado-md.md) чтобы определить,  является ли родительский объект этого члена тем же, что и родительский объект предшествующего **члена.**</span><span class="sxs-lookup"><span data-stu-id="c3b6e-128">Use the [ParentSameAsPrev](parentsameasprev-property-ado-md.md) property to determine whether the parent of this **Member** is the same as the parent of the immediately preceding **Member**.</span></span>

  - <span data-ttu-id="c3b6e-129">Используйте стандартную коллекцию [свойств](properties-collection-ado.md) ADO для получения дополнительных сведений об **объекте Level.**</span><span class="sxs-lookup"><span data-stu-id="c3b6e-129">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Level** object.</span></span>

<span data-ttu-id="c3b6e-130">Коллекция **Properties** содержит свойства, предоставленные поставщиком.</span><span class="sxs-lookup"><span data-stu-id="c3b6e-130">The **Properties** collection contains provider-supplied properties.</span></span> <span data-ttu-id="c3b6e-131">В следующей таблице перечислены свойства, которые могут быть доступны.</span><span class="sxs-lookup"><span data-stu-id="c3b6e-131">The following table lists properties that might be available.</span></span> <span data-ttu-id="c3b6e-132">Фактический список свойств может отличаться в зависимости от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="c3b6e-132">The actual property list may differ depending upon the implementation of the provider.</span></span> <span data-ttu-id="c3b6e-133">Более полный список доступных свойств см. в документации к поставщику.</span><span class="sxs-lookup"><span data-stu-id="c3b6e-133">See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c3b6e-134">Имя</span><span class="sxs-lookup"><span data-stu-id="c3b6e-134">Name</span></span></p></th>
<th><p><span data-ttu-id="c3b6e-135">Описание</span><span class="sxs-lookup"><span data-stu-id="c3b6e-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3b6e-136">CatalogName</span><span class="sxs-lookup"><span data-stu-id="c3b6e-136">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="c3b6e-137">Имя каталога, к которому принадлежит этот куб.</span><span class="sxs-lookup"><span data-stu-id="c3b6e-137">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3b6e-138">ChildrenCardinality</span><span class="sxs-lookup"><span data-stu-id="c3b6e-138">ChildrenCardinality</span></span></p></td>
<td><p><span data-ttu-id="c3b6e-139">Количество детей, которые есть у участника.</span><span class="sxs-lookup"><span data-stu-id="c3b6e-139">The number of children that the member has.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3b6e-140">CubeName</span><span class="sxs-lookup"><span data-stu-id="c3b6e-140">CubeName</span></span></p></td>
<td><p><span data-ttu-id="c3b6e-141">Имя куба.</span><span class="sxs-lookup"><span data-stu-id="c3b6e-141">The name of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3b6e-142">Описание</span><span class="sxs-lookup"><span data-stu-id="c3b6e-142">Description</span></span></p></td>
<td><p><span data-ttu-id="c3b6e-143">Осмысленное описание участника.</span><span class="sxs-lookup"><span data-stu-id="c3b6e-143">A meaningful description of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3b6e-144">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="c3b6e-144">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="c3b6e-145">Однозначное имя <a href="dimension-object-ado-md.md">измерения.</a></span><span class="sxs-lookup"><span data-stu-id="c3b6e-145">The unambiguous name of the <a href="dimension-object-ado-md.md">dimension</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3b6e-146">HierarchyUniqueName</span><span class="sxs-lookup"><span data-stu-id="c3b6e-146">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="c3b6e-147">Однозначное имя иерархии.</span><span class="sxs-lookup"><span data-stu-id="c3b6e-147">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3b6e-148">LevelNumber</span><span class="sxs-lookup"><span data-stu-id="c3b6e-148">LevelNumber</span></span></p></td>
<td><p><span data-ttu-id="c3b6e-149">Расстояние между уровнем и корнем иерархии.</span><span class="sxs-lookup"><span data-stu-id="c3b6e-149">The distance between the level and the root of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3b6e-150">LevelUniqueName</span><span class="sxs-lookup"><span data-stu-id="c3b6e-150">LevelUniqueName</span></span></p></td>
<td><p><span data-ttu-id="c3b6e-151">Однозначное имя уровня.</span><span class="sxs-lookup"><span data-stu-id="c3b6e-151">The unambiguous name of the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3b6e-152">MemberCaption</span><span class="sxs-lookup"><span data-stu-id="c3b6e-152">MemberCaption</span></span></p></td>
<td><p><span data-ttu-id="c3b6e-153">Метка или подпись, связанная с участником.</span><span class="sxs-lookup"><span data-stu-id="c3b6e-153">A label or caption associated with the member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3b6e-154">MemberGUID</span><span class="sxs-lookup"><span data-stu-id="c3b6e-154">MemberGUID</span></span></p></td>
<td><p><span data-ttu-id="c3b6e-155">GUID участника.</span><span class="sxs-lookup"><span data-stu-id="c3b6e-155">The GUID of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3b6e-156">MemberName</span><span class="sxs-lookup"><span data-stu-id="c3b6e-156">MemberName</span></span></p></td>
<td><p><span data-ttu-id="c3b6e-157">Имя участника.</span><span class="sxs-lookup"><span data-stu-id="c3b6e-157">The name of the member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3b6e-158">MemberOrdinal</span><span class="sxs-lookup"><span data-stu-id="c3b6e-158">MemberOrdinal</span></span></p></td>
<td><p><span data-ttu-id="c3b6e-159">Порядковая номер участника.</span><span class="sxs-lookup"><span data-stu-id="c3b6e-159">The ordinal number of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3b6e-160">MemberType</span><span class="sxs-lookup"><span data-stu-id="c3b6e-160">MemberType</span></span></p></td>
<td><p><span data-ttu-id="c3b6e-161">Тип члена.</span><span class="sxs-lookup"><span data-stu-id="c3b6e-161">The type of the member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3b6e-162">MemberUniqueName</span><span class="sxs-lookup"><span data-stu-id="c3b6e-162">MemberUniqueName</span></span></p></td>
<td><p><span data-ttu-id="c3b6e-163">Однозначное имя члена.</span><span class="sxs-lookup"><span data-stu-id="c3b6e-163">The unambiguous name of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3b6e-164">ParentCount</span><span class="sxs-lookup"><span data-stu-id="c3b6e-164">ParentCount</span></span></p></td>
<td><p><span data-ttu-id="c3b6e-165">Количество родителей, которые есть у этого участника.</span><span class="sxs-lookup"><span data-stu-id="c3b6e-165">The count of the number of parents that this member has.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3b6e-166">ParentLevel</span><span class="sxs-lookup"><span data-stu-id="c3b6e-166">ParentLevel</span></span></p></td>
<td><p><span data-ttu-id="c3b6e-167">Номер уровня родительского члена.</span><span class="sxs-lookup"><span data-stu-id="c3b6e-167">The level number of the member's parent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3b6e-168">ParentUniqueName</span><span class="sxs-lookup"><span data-stu-id="c3b6e-168">ParentUniqueName</span></span></p></td>
<td><p><span data-ttu-id="c3b6e-169">Однозначное имя родительского члена.</span><span class="sxs-lookup"><span data-stu-id="c3b6e-169">The unambiguous name of the member's parent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3b6e-170">SchemaName</span><span class="sxs-lookup"><span data-stu-id="c3b6e-170">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="c3b6e-171">Имя схемы, к которой принадлежит этот куб.</span><span class="sxs-lookup"><span data-stu-id="c3b6e-171">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

