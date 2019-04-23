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
# <a name="member-object-ado-md"></a><span data-ttu-id="b24a9-102">Объект Member (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="b24a9-102">Member object (ADO MD)</span></span>


<span data-ttu-id="b24a9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b24a9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b24a9-104">Представляет элемент уровня в Кубе, дочерние элементы элемента уровня или элемента положения на оси в наборе ячеек.</span><span class="sxs-lookup"><span data-stu-id="b24a9-104">Represents a member of a level in a cube, the children of a member of a level, or a member of a position along an axis of a cellset.</span></span>

## <a name="remarks"></a><span data-ttu-id="b24a9-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="b24a9-105">Remarks</span></span>

<span data-ttu-id="b24a9-106">Свойства **элемента** различаются в зависимости от контекста, в котором он используется.</span><span class="sxs-lookup"><span data-stu-id="b24a9-106">The properties of a **Member** differ depending on the context in which it is used.</span></span> <span data-ttu-id="b24a9-107">**Элемент** [уровня](level-object-ado-md.md) в [CubeDef](cubedef-object-ado-md.md) имеет свойство [Children](children-property-ado-md.md) , возвращающее **элементы** следующего нижнего уровня в иерархии от текущего **элемента**.</span><span class="sxs-lookup"><span data-stu-id="b24a9-107">A **Member** of a [Level](level-object-ado-md.md) in a [CubeDef](cubedef-object-ado-md.md) has a [Children](children-property-ado-md.md) property that returns the **Members** on the next lower level in the hierarchy from the current **Member**.</span></span> <span data-ttu-id="b24a9-108">Для **элемента** [position](position-object-ado-md.md)коллекция **Children** всегда пуста.</span><span class="sxs-lookup"><span data-stu-id="b24a9-108">For a **Member** of a [Position](position-object-ado-md.md), the **Children** collection is always empty.</span></span> <span data-ttu-id="b24a9-109">Кроме того, свойство [Type](type-property-ado-md.md) применяется только к **членам** **уровня**.</span><span class="sxs-lookup"><span data-stu-id="b24a9-109">Also, the [Type](type-property-ado-md.md) property applies only to **Members** of a **Level**.</span></span>

<span data-ttu-id="b24a9-110">Элемент **position** имеет два свойства — [DrilledDown](drilleddown-property-ado-md.md) и [ParentSameAsPrev](parentsameasprev-property-ado-md.md) , которые удобно использовать при отображении **набора** [ячеек](cellset-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="b24a9-110">A **Member** of **Position** has two properties — [DrilledDown](drilleddown-property-ado-md.md) and [ParentSameAsPrev](parentsameasprev-property-ado-md.md) — that are useful when displaying the [Cellset](cellset-object-ado-md.md).</span></span> <span data-ttu-id="b24a9-111">Если к этим свойствам обращаются по **элементу** **уровня**, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="b24a9-111">An error will occur if these properties are accessed on a **Member** of a **Level**.</span></span>

<span data-ttu-id="b24a9-112">С помощью коллекций и свойств объекта **member** **уровня**можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="b24a9-112">With the collections and properties of a **Member** object of a **Level**, you can do the following:</span></span>

  - <span data-ttu-id="b24a9-113">Идентифицируйте **члена** с помощью свойств [Name](name-property-ado-md.md) и [UniqueName](uniquename-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="b24a9-113">Identify the **Member** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="b24a9-114">Возвращает строку, используемую при отображении **элемента** со свойством [Caption](caption-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="b24a9-114">Return a string to use when displaying the **Member** with the [Caption](caption-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="b24a9-115">Возвращает осмысленную строку, описывающую меру или **элемент** формулы, с помощью свойства [Description](description-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="b24a9-115">Return a meaningful string that describes a measure or formula **Member** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="b24a9-116">Определите природу **элемента** с помощью свойства [Type](type-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="b24a9-116">Determine the nature of the **Member** with the [Type](type-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="b24a9-117">Получение сведений о **уровне** **элемента** с помощью свойств [LevelDepth](leveldepth-property-ado-md.md) и [LevelName](levelname-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="b24a9-117">Obtain information about the **Level** of the **Member** with the [LevelDepth](leveldepth-property-ado-md.md) and [LevelName](levelname-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="b24a9-118">Получение связанных **членов** в [иерархии](hierarchy-object-ado-md.md) с родительскими [](parent-property-ado-md.md) свойствами и свойствами [дочерних элементов](children-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="b24a9-118">Obtain related **Members** in a [Hierarchy](hierarchy-object-ado-md.md) with the [Parent](parent-property-ado-md.md) and [Children](children-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="b24a9-119">ПодСчитайте дочерние элементы **элемента** с помощью свойства [ChildCount](childcount-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="b24a9-119">Count the children of a **Member** with the [ChildCount](childcount-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="b24a9-120">Используйте стандартную коллекцию [свойств](properties-collection-ado.md) ADO для получения дополнительных сведений об объекте **Level** .</span><span class="sxs-lookup"><span data-stu-id="b24a9-120">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Level** object.</span></span>

<span data-ttu-id="b24a9-121">С помощью коллекций и свойств **члена** **позиции** вдоль [оси](axis-object-ado-md.md)можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="b24a9-121">With the collections and properties of a **Member** of a **Position** along an [Axis](axis-object-ado-md.md), you can do the following:</span></span>

  - <span data-ttu-id="b24a9-122">Идентифицируйте **члена** с помощью свойств [Name](name-property-ado-md.md) и [UniqueName](uniquename-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="b24a9-122">Identify the **Member** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="b24a9-123">Возвращает строку, используемую при отображении **элемента** со свойством [Caption](caption-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="b24a9-123">Return a string to use when displaying the **Member** with the [Caption](caption-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="b24a9-124">Возвращает осмысленную строку, описывающую меру или **элемент** формулы, с помощью свойства [Description](description-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="b24a9-124">Return a meaningful string that describes a measure or formula **Member** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="b24a9-125">Получение сведений о **уровне** **элемента** с помощью свойств [LevelDepth](leveldepth-property-ado-md.md) и [LevelName](levelname-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="b24a9-125">Obtain information about the **Level** of the **Member** with the [LevelDepth](leveldepth-property-ado-md.md) and [LevelName](levelname-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="b24a9-126">ПодСчитайте дочерние элементы **элемента** с помощью свойства [ChildCount](childcount-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="b24a9-126">Count the children of a **Member** with the [ChildCount](childcount-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="b24a9-127">Используйте свойство [DrilledDown](drilleddown-property-ado-md.md) , чтобы определить, есть ли по крайней мере один дочерний элемент на **оси** , которая сразу после этого **элемента**.</span><span class="sxs-lookup"><span data-stu-id="b24a9-127">Use the [DrilledDown](drilleddown-property-ado-md.md) property to determine whether there is at least one child on the **Axis** immediately following this **Member**.</span></span>

  - <span data-ttu-id="b24a9-128">Используйте свойство [ParentSameAsPrev](parentsameasprev-property-ado-md.md) , чтобы определить, совпадает ли родительский **элемент этого члена** со родителем непосредственно предыдущего **члена**.</span><span class="sxs-lookup"><span data-stu-id="b24a9-128">Use the [ParentSameAsPrev](parentsameasprev-property-ado-md.md) property to determine whether the parent of this **Member** is the same as the parent of the immediately preceding **Member**.</span></span>

  - <span data-ttu-id="b24a9-129">Используйте стандартную коллекцию [свойств](properties-collection-ado.md) ADO для получения дополнительных сведений об объекте **Level** .</span><span class="sxs-lookup"><span data-stu-id="b24a9-129">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Level** object.</span></span>

<span data-ttu-id="b24a9-130">Коллекция **Properties** содержит свойства, предоставляемые поставщиком.</span><span class="sxs-lookup"><span data-stu-id="b24a9-130">The **Properties** collection contains provider-supplied properties.</span></span> <span data-ttu-id="b24a9-131">В следующей таблице перечислены свойства, которые могут быть доступны.</span><span class="sxs-lookup"><span data-stu-id="b24a9-131">The following table lists properties that might be available.</span></span> <span data-ttu-id="b24a9-132">Фактический список свойств может различаться в зависимости от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="b24a9-132">The actual property list may differ depending upon the implementation of the provider.</span></span> <span data-ttu-id="b24a9-133">Просмотрите документацию для своего поставщика, чтобы получить полный список доступных свойств.</span><span class="sxs-lookup"><span data-stu-id="b24a9-133">See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b24a9-134">Имя</span><span class="sxs-lookup"><span data-stu-id="b24a9-134">Name</span></span></p></th>
<th><p><span data-ttu-id="b24a9-135">Описание</span><span class="sxs-lookup"><span data-stu-id="b24a9-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b24a9-136">Каталогнаме</span><span class="sxs-lookup"><span data-stu-id="b24a9-136">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="b24a9-137">Имя каталога, к которому принадлежит куб.</span><span class="sxs-lookup"><span data-stu-id="b24a9-137">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b24a9-138">Чилдренкардиналити</span><span class="sxs-lookup"><span data-stu-id="b24a9-138">ChildrenCardinality</span></span></p></td>
<td><p><span data-ttu-id="b24a9-139">Количество дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="b24a9-139">The number of children that the member has.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b24a9-140">Кубенаме</span><span class="sxs-lookup"><span data-stu-id="b24a9-140">CubeName</span></span></p></td>
<td><p><span data-ttu-id="b24a9-141">Имя куба.</span><span class="sxs-lookup"><span data-stu-id="b24a9-141">The name of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b24a9-142">Описание</span><span class="sxs-lookup"><span data-stu-id="b24a9-142">Description</span></span></p></td>
<td><p><span data-ttu-id="b24a9-143">Понятное описание члена.</span><span class="sxs-lookup"><span data-stu-id="b24a9-143">A meaningful description of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b24a9-144">Дименсионуникуенаме</span><span class="sxs-lookup"><span data-stu-id="b24a9-144">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="b24a9-145">Неоднозначное имя <a href="dimension-object-ado-md.md">измерения</a>.</span><span class="sxs-lookup"><span data-stu-id="b24a9-145">The unambiguous name of the <a href="dimension-object-ado-md.md">dimension</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b24a9-146">Хиерарчюникуенаме</span><span class="sxs-lookup"><span data-stu-id="b24a9-146">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="b24a9-147">Неоднозначное имя иерархии.</span><span class="sxs-lookup"><span data-stu-id="b24a9-147">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b24a9-148">Левелнумбер</span><span class="sxs-lookup"><span data-stu-id="b24a9-148">LevelNumber</span></span></p></td>
<td><p><span data-ttu-id="b24a9-149">Расстояние между уровнем и корнем иерархии.</span><span class="sxs-lookup"><span data-stu-id="b24a9-149">The distance between the level and the root of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b24a9-150">Левелуникуенаме</span><span class="sxs-lookup"><span data-stu-id="b24a9-150">LevelUniqueName</span></span></p></td>
<td><p><span data-ttu-id="b24a9-151">Неоднозначное имя уровня.</span><span class="sxs-lookup"><span data-stu-id="b24a9-151">The unambiguous name of the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b24a9-152">Мемберкаптион</span><span class="sxs-lookup"><span data-stu-id="b24a9-152">MemberCaption</span></span></p></td>
<td><p><span data-ttu-id="b24a9-153">Метка или заголовок, связанные с элементом.</span><span class="sxs-lookup"><span data-stu-id="b24a9-153">A label or caption associated with the member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b24a9-154">Мембергуид</span><span class="sxs-lookup"><span data-stu-id="b24a9-154">MemberGUID</span></span></p></td>
<td><p><span data-ttu-id="b24a9-155">GUID члена.</span><span class="sxs-lookup"><span data-stu-id="b24a9-155">The GUID of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b24a9-156">MemberName</span><span class="sxs-lookup"><span data-stu-id="b24a9-156">MemberName</span></span></p></td>
<td><p><span data-ttu-id="b24a9-157">Имя элемента.</span><span class="sxs-lookup"><span data-stu-id="b24a9-157">The name of the member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b24a9-158">Мемберординал</span><span class="sxs-lookup"><span data-stu-id="b24a9-158">MemberOrdinal</span></span></p></td>
<td><p><span data-ttu-id="b24a9-159">Порядковый номер элемента.</span><span class="sxs-lookup"><span data-stu-id="b24a9-159">The ordinal number of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b24a9-160">Мембертипе</span><span class="sxs-lookup"><span data-stu-id="b24a9-160">MemberType</span></span></p></td>
<td><p><span data-ttu-id="b24a9-161">Тип элемента.</span><span class="sxs-lookup"><span data-stu-id="b24a9-161">The type of the member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b24a9-162">Мемберуникуенаме</span><span class="sxs-lookup"><span data-stu-id="b24a9-162">MemberUniqueName</span></span></p></td>
<td><p><span data-ttu-id="b24a9-163">Неоднозначное имя элемента.</span><span class="sxs-lookup"><span data-stu-id="b24a9-163">The unambiguous name of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b24a9-164">Паренткаунт</span><span class="sxs-lookup"><span data-stu-id="b24a9-164">ParentCount</span></span></p></td>
<td><p><span data-ttu-id="b24a9-165">Количество родительских элементов.</span><span class="sxs-lookup"><span data-stu-id="b24a9-165">The count of the number of parents that this member has.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b24a9-166">Парентлевел</span><span class="sxs-lookup"><span data-stu-id="b24a9-166">ParentLevel</span></span></p></td>
<td><p><span data-ttu-id="b24a9-167">Номер уровня родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="b24a9-167">The level number of the member's parent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b24a9-168">Парентуникуенаме</span><span class="sxs-lookup"><span data-stu-id="b24a9-168">ParentUniqueName</span></span></p></td>
<td><p><span data-ttu-id="b24a9-169">Неоднозначное имя родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="b24a9-169">The unambiguous name of the member's parent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b24a9-170">SchemaName</span><span class="sxs-lookup"><span data-stu-id="b24a9-170">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="b24a9-171">Имя схемы, к которой принадлежит куб.</span><span class="sxs-lookup"><span data-stu-id="b24a9-171">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

