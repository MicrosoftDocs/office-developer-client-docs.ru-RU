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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709581"
---
# <a name="member-object-ado-md"></a><span data-ttu-id="469ee-102">Объект Member (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="469ee-102">Member object (ADO MD)</span></span>


<span data-ttu-id="469ee-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="469ee-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="469ee-104">Представляет элемент уровень в кубе, дочерние элементы элемента уровня или членом положение оси набора ячеек.</span><span class="sxs-lookup"><span data-stu-id="469ee-104">Represents a member of a level in a cube, the children of a member of a level, or a member of a position along an axis of a cellset.</span></span>

## <a name="remarks"></a><span data-ttu-id="469ee-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="469ee-105">Remarks</span></span>

<span data-ttu-id="469ee-106">Свойства **члена** отличаются в зависимости от контекста, в котором она используется.</span><span class="sxs-lookup"><span data-stu-id="469ee-106">The properties of a **Member** differ depending on the context in which it is used.</span></span> <span data-ttu-id="469ee-107">**Член** [уровень](level-object-ado-md.md) [CubeDef](cubedef-object-ado-md.md) имеет свойство [дочерних элементов](children-property-ado-md.md) , которое возвращает **члены** на уровень ниже в иерархии из текущего **элемента**.</span><span class="sxs-lookup"><span data-stu-id="469ee-107">A **Member** of a [Level](level-object-ado-md.md) in a [CubeDef](cubedef-object-ado-md.md) has a [Children](children-property-ado-md.md) property that returns the **Members** on the next lower level in the hierarchy from the current **Member**.</span></span> <span data-ttu-id="469ee-108">Для **члена** [позицию](position-object-ado-md.md) **дочерней** коллекции всегда будет пустым.</span><span class="sxs-lookup"><span data-stu-id="469ee-108">For a **Member** of a [Position](position-object-ado-md.md), the **Children** collection is always empty.</span></span> <span data-ttu-id="469ee-109">Кроме того свойство [Type](type-property-ado-md.md) применяется только к **члены** **уровня**.</span><span class="sxs-lookup"><span data-stu-id="469ee-109">Also, the [Type](type-property-ado-md.md) property applies only to **Members** of a **Level**.</span></span>

<span data-ttu-id="469ee-110">**Член** **положение** имеет два свойства — [DrilledDown](drilleddown-property-ado-md.md) и [ParentSameAsPrev](parentsameasprev-property-ado-md.md) —, могут быть полезны при отображении [ячеек](cellset-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="469ee-110">A **Member** of **Position** has two properties — [DrilledDown](drilleddown-property-ado-md.md) and [ParentSameAsPrev](parentsameasprev-property-ado-md.md) — that are useful when displaying the [Cellset](cellset-object-ado-md.md).</span></span> <span data-ttu-id="469ee-111">Если эти свойства доступны на **уровень** **член** , произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="469ee-111">An error will occur if these properties are accessed on a **Member** of a **Level**.</span></span>

<span data-ttu-id="469ee-112">Со свойствами объекта **члена** **уровень**и семейств сайтов выполните следующее:</span><span class="sxs-lookup"><span data-stu-id="469ee-112">With the collections and properties of a **Member** object of a **Level**, you can do the following:</span></span>

  - <span data-ttu-id="469ee-113">Определите с помощью свойства [Name](name-property-ado-md.md) и [уникального имени](uniquename-property-ado-md.md) **члена** .</span><span class="sxs-lookup"><span data-stu-id="469ee-113">Identify the **Member** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="469ee-114">Возвращает строку, используемую при отображении **элемента** с помощью свойства [Caption](caption-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="469ee-114">Return a string to use when displaying the **Member** with the [Caption](caption-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="469ee-115">Возвращает удобной для восприятия строка, описывающая измерения или формулу **элемента** с помощью свойства [Description](description-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="469ee-115">Return a meaningful string that describes a measure or formula **Member** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="469ee-116">Определите характер **член** со свойством [типа](type-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="469ee-116">Determine the nature of the **Member** with the [Type](type-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="469ee-117">Получите информацию о **уровень** **член** с помощью свойства [LevelDepth](leveldepth-property-ado-md.md) и [LevelName](levelname-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="469ee-117">Obtain information about the **Level** of the **Member** with the [LevelDepth](leveldepth-property-ado-md.md) and [LevelName](levelname-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="469ee-118">Получение связанных **элементов** в [иерархии](hierarchy-object-ado-md.md) с помощью свойства [родительских](parent-property-ado-md.md) и [дочерних элементов](children-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="469ee-118">Obtain related **Members** in a [Hierarchy](hierarchy-object-ado-md.md) with the [Parent](parent-property-ado-md.md) and [Children](children-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="469ee-119">Счетчик потомков **члена** со свойством [ChildCount](childcount-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="469ee-119">Count the children of a **Member** with the [ChildCount](childcount-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="469ee-120">Используйте коллекцию стандартный ADO [Свойства](properties-collection-ado.md) для получения дополнительных сведений об объекте **уровень** .</span><span class="sxs-lookup"><span data-stu-id="469ee-120">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Level** object.</span></span>

<span data-ttu-id="469ee-121">Со свойствами **члена** **положение** по [оси](axis-object-ado-md.md)и семейств сайтов выполните следующее:</span><span class="sxs-lookup"><span data-stu-id="469ee-121">With the collections and properties of a **Member** of a **Position** along an [Axis](axis-object-ado-md.md), you can do the following:</span></span>

  - <span data-ttu-id="469ee-122">Определите с помощью свойства [Name](name-property-ado-md.md) и [уникального имени](uniquename-property-ado-md.md) **члена** .</span><span class="sxs-lookup"><span data-stu-id="469ee-122">Identify the **Member** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="469ee-123">Возвращает строку, используемую при отображении **элемента** с помощью свойства [Caption](caption-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="469ee-123">Return a string to use when displaying the **Member** with the [Caption](caption-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="469ee-124">Возвращает удобной для восприятия строка, описывающая измерения или формулу **элемента** с помощью свойства [Description](description-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="469ee-124">Return a meaningful string that describes a measure or formula **Member** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="469ee-125">Получите информацию о **уровень** **член** с помощью свойства [LevelDepth](leveldepth-property-ado-md.md) и [LevelName](levelname-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="469ee-125">Obtain information about the **Level** of the **Member** with the [LevelDepth](leveldepth-property-ado-md.md) and [LevelName](levelname-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="469ee-126">Счетчик потомков **члена** со свойством [ChildCount](childcount-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="469ee-126">Count the children of a **Member** with the [ChildCount](childcount-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="469ee-127">Свойство [DrilledDown](drilleddown-property-ado-md.md) используется для определения, является ли на **оси** сразу после этот **член**по крайней мере один дочерний элемент.</span><span class="sxs-lookup"><span data-stu-id="469ee-127">Use the [DrilledDown](drilleddown-property-ado-md.md) property to determine whether there is at least one child on the **Axis** immediately following this **Member**.</span></span>

  - <span data-ttu-id="469ee-128">Свойство [ParentSameAsPrev](parentsameasprev-property-ado-md.md) используется для определения, совпадает ли родительский этот **член** родительской предыдущего **элемента**.</span><span class="sxs-lookup"><span data-stu-id="469ee-128">Use the [ParentSameAsPrev](parentsameasprev-property-ado-md.md) property to determine whether the parent of this **Member** is the same as the parent of the immediately preceding **Member**.</span></span>

  - <span data-ttu-id="469ee-129">Используйте коллекцию стандартный ADO [Свойства](properties-collection-ado.md) для получения дополнительных сведений об объекте **уровень** .</span><span class="sxs-lookup"><span data-stu-id="469ee-129">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Level** object.</span></span>

<span data-ttu-id="469ee-130">Коллекции **свойств** содержит свойства, предоставленных поставщиком.</span><span class="sxs-lookup"><span data-stu-id="469ee-130">The **Properties** collection contains provider-supplied properties.</span></span> <span data-ttu-id="469ee-131">В следующей таблице перечислены свойства, которые могут быть недоступны.</span><span class="sxs-lookup"><span data-stu-id="469ee-131">The following table lists properties that might be available.</span></span> <span data-ttu-id="469ee-132">Список свойств фактический может различаться в зависимости от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="469ee-132">The actual property list may differ depending upon the implementation of the provider.</span></span> <span data-ttu-id="469ee-133">Обратитесь к документации вашего поставщика для получения более полного списка доступных свойств.</span><span class="sxs-lookup"><span data-stu-id="469ee-133">See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="469ee-134">Имя</span><span class="sxs-lookup"><span data-stu-id="469ee-134">Name</span></span></p></th>
<th><p><span data-ttu-id="469ee-135">Описание</span><span class="sxs-lookup"><span data-stu-id="469ee-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="469ee-136">ИмяКаталога</span><span class="sxs-lookup"><span data-stu-id="469ee-136">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="469ee-137">Имя каталога, к которому принадлежит этот куб.</span><span class="sxs-lookup"><span data-stu-id="469ee-137">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="469ee-138">ChildrenCardinality</span><span class="sxs-lookup"><span data-stu-id="469ee-138">ChildrenCardinality</span></span></p></td>
<td><p><span data-ttu-id="469ee-139">Число дочерних элементов элемента.</span><span class="sxs-lookup"><span data-stu-id="469ee-139">The number of children that the member has.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="469ee-140">Имя куба</span><span class="sxs-lookup"><span data-stu-id="469ee-140">CubeName</span></span></p></td>
<td><p><span data-ttu-id="469ee-141">Имя куба.</span><span class="sxs-lookup"><span data-stu-id="469ee-141">The name of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="469ee-142">Описание</span><span class="sxs-lookup"><span data-stu-id="469ee-142">Description</span></span></p></td>
<td><p><span data-ttu-id="469ee-143">Понятное описание элемента.</span><span class="sxs-lookup"><span data-stu-id="469ee-143">A meaningful description of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="469ee-144">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="469ee-144">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="469ee-145">Однозначное имя <a href="dimension-object-ado-md.md">измерения</a>.</span><span class="sxs-lookup"><span data-stu-id="469ee-145">The unambiguous name of the <a href="dimension-object-ado-md.md">dimension</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="469ee-146">HierarchyUniqueName</span><span class="sxs-lookup"><span data-stu-id="469ee-146">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="469ee-147">Однозначное имя иерархии.</span><span class="sxs-lookup"><span data-stu-id="469ee-147">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="469ee-148">LevelNumber</span><span class="sxs-lookup"><span data-stu-id="469ee-148">LevelNumber</span></span></p></td>
<td><p><span data-ttu-id="469ee-149">Расстояние между на уровне и корень иерархии.</span><span class="sxs-lookup"><span data-stu-id="469ee-149">The distance between the level and the root of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="469ee-150">LevelUniqueName</span><span class="sxs-lookup"><span data-stu-id="469ee-150">LevelUniqueName</span></span></p></td>
<td><p><span data-ttu-id="469ee-151">Однозначное имя уровня.</span><span class="sxs-lookup"><span data-stu-id="469ee-151">The unambiguous name of the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="469ee-152">MemberCaption</span><span class="sxs-lookup"><span data-stu-id="469ee-152">MemberCaption</span></span></p></td>
<td><p><span data-ttu-id="469ee-153">Метка или заголовок, связанный с элементом.</span><span class="sxs-lookup"><span data-stu-id="469ee-153">A label or caption associated with the member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="469ee-154">MemberGUID</span><span class="sxs-lookup"><span data-stu-id="469ee-154">MemberGUID</span></span></p></td>
<td><p><span data-ttu-id="469ee-155">Идентификатор GUID члена.</span><span class="sxs-lookup"><span data-stu-id="469ee-155">The GUID of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="469ee-156">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="469ee-156">MemberName</span></span></p></td>
<td><p><span data-ttu-id="469ee-157">Имя участника.</span><span class="sxs-lookup"><span data-stu-id="469ee-157">The name of the member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="469ee-158">MemberOrdinal</span><span class="sxs-lookup"><span data-stu-id="469ee-158">MemberOrdinal</span></span></p></td>
<td><p><span data-ttu-id="469ee-159">Порядковый номер элемента.</span><span class="sxs-lookup"><span data-stu-id="469ee-159">The ordinal number of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="469ee-160">MemberType</span><span class="sxs-lookup"><span data-stu-id="469ee-160">MemberType</span></span></p></td>
<td><p><span data-ttu-id="469ee-161">Тип элемента.</span><span class="sxs-lookup"><span data-stu-id="469ee-161">The type of the member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="469ee-162">MemberUniqueName</span><span class="sxs-lookup"><span data-stu-id="469ee-162">MemberUniqueName</span></span></p></td>
<td><p><span data-ttu-id="469ee-163">Однозначное имя участника.</span><span class="sxs-lookup"><span data-stu-id="469ee-163">The unambiguous name of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="469ee-164">ParentCount</span><span class="sxs-lookup"><span data-stu-id="469ee-164">ParentCount</span></span></p></td>
<td><p><span data-ttu-id="469ee-165">Счетчик количество родительских элементов данного элемента.</span><span class="sxs-lookup"><span data-stu-id="469ee-165">The count of the number of parents that this member has.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="469ee-166">ParentLevel</span><span class="sxs-lookup"><span data-stu-id="469ee-166">ParentLevel</span></span></p></td>
<td><p><span data-ttu-id="469ee-167">Номер уровня родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="469ee-167">The level number of the member's parent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="469ee-168">ParentUniqueName</span><span class="sxs-lookup"><span data-stu-id="469ee-168">ParentUniqueName</span></span></p></td>
<td><p><span data-ttu-id="469ee-169">Однозначное имя родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="469ee-169">The unambiguous name of the member's parent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="469ee-170">SchemaName</span><span class="sxs-lookup"><span data-stu-id="469ee-170">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="469ee-171">Имя схемы, к которой принадлежит этот куб.</span><span class="sxs-lookup"><span data-stu-id="469ee-171">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

