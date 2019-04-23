---
title: Обзор многомерных схем и данных
TOCTitle: Overview of multidimensional schemas and data
ms:assetid: a963e993-b7bf-eeb4-ecd5-d6fe43cf4bb5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249784(v=office.15)
ms:contentKeyID: 48546923
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d65378bf964ad8c6e81a08cb653f09bf00a8431c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288156"
---
# <a name="overview-of-multidimensional-schemas-and-data"></a><span data-ttu-id="7f74f-102">Обзор многомерных схем и данных</span><span class="sxs-lookup"><span data-stu-id="7f74f-102">Overview of multidimensional schemas and data</span></span>

<span data-ttu-id="7f74f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7f74f-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="understanding-multidimensional-schemas"></a><span data-ttu-id="7f74f-104">Общие сведения о многомерных схемах</span><span class="sxs-lookup"><span data-stu-id="7f74f-104">Understanding Multidimensional Schemas</span></span>

<span data-ttu-id="7f74f-105">Центральным объектом метаданных в ADO MD является *куб*, состоящий из структурированного набора связанных измерений, иерархий, уровней и элементов.</span><span class="sxs-lookup"><span data-stu-id="7f74f-105">The central metadata object in ADO MD is the *cube*, which consists of a structured set of related dimensions, hierarchies, levels, and members.</span></span>

<span data-ttu-id="7f74f-106">*Измерение* — это независимая категория данных из многомерной базы данных, которая является производной от ваших бизнес-сущностей.</span><span class="sxs-lookup"><span data-stu-id="7f74f-106">A *dimension* is an independent category of data from your multidimensional database, derived from your business entities.</span></span> <span data-ttu-id="7f74f-107">Измерение обычно содержит элементы, которые будут использоваться в качестве критериев запроса для мер базы данных.</span><span class="sxs-lookup"><span data-stu-id="7f74f-107">A dimension typically contains items to be used as query criteria for the measures of the database.</span></span>

<span data-ttu-id="7f74f-108">*Иерархия* это путь статистической обработки измерения.</span><span class="sxs-lookup"><span data-stu-id="7f74f-108">A *hierarchy* is a path of aggregation of a dimension.</span></span> <span data-ttu-id="7f74f-109">Измерение может иметь несколько уровней гранулярности, которые имеют отношения "родители — потомки".</span><span class="sxs-lookup"><span data-stu-id="7f74f-109">A dimension may have multiple levels of granularity, which have parent-child relationships.</span></span> <span data-ttu-id="7f74f-110">Иерархия определяет способ связи этих уровней.</span><span class="sxs-lookup"><span data-stu-id="7f74f-110">A hierarchy defines how these levels are related.</span></span>

<span data-ttu-id="7f74f-111">*Уровень* — это шаг статистической обработки в иерархии.</span><span class="sxs-lookup"><span data-stu-id="7f74f-111">A *level* is a step of aggregation in a hierarchy.</span></span> <span data-ttu-id="7f74f-112">Для измерений с несколькими уровнями информации каждый уровень является уровнем.</span><span class="sxs-lookup"><span data-stu-id="7f74f-112">For dimensions with multiple layers of information, each layer is a level.</span></span>

<span data-ttu-id="7f74f-113">Элемент \*\* — это элемент данных в измерении.</span><span class="sxs-lookup"><span data-stu-id="7f74f-113">A *member* is a data item in a dimension.</span></span> <span data-ttu-id="7f74f-114">Как правило, при создании заголовка или описания меры базы данных используются члены.</span><span class="sxs-lookup"><span data-stu-id="7f74f-114">Typically, you create a caption or describe a measure of the database using members.</span></span>

<span data-ttu-id="7f74f-115">Кубы представлены объектами [CubeDef](cubedef-object-ado-md.md) в ADO MD.</span><span class="sxs-lookup"><span data-stu-id="7f74f-115">Cubes are represented by [CubeDef](cubedef-object-ado-md.md) objects in ADO MD.</span></span> <span data-ttu-id="7f74f-116">Измерения, иерархии, уровни и элементы также представлены соответствующими объектами ADO MD: [измерение](dimension-object-ado-md.md), иерархия, [уровень](level-object-ado-md.md)и [](hierarchy-object-ado-md.md) [элемент](member-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="7f74f-116">Dimensions, hierarchies, levels, and members are also represented by their corresponding ADO MD objects: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md).</span></span>

## <a name="dimensions"></a><span data-ttu-id="7f74f-117">Dimensions</span><span class="sxs-lookup"><span data-stu-id="7f74f-117">Dimensions</span></span>

<span data-ttu-id="7f74f-118">Измерения куба зависят от бизнес-сущностей и типов данных, которые необходимо моделировать в базе данных.</span><span class="sxs-lookup"><span data-stu-id="7f74f-118">The dimensions of a cube depend on your business entities and types of data to be modeled in the database.</span></span> <span data-ttu-id="7f74f-119">Как правило, каждое измерение — это независимая точка входа или механизм для выбора данных.</span><span class="sxs-lookup"><span data-stu-id="7f74f-119">Typically, each dimension is an independent entry point or mechanism for selecting data.</span></span>

<span data-ttu-id="7f74f-120">Например, куб с данными продаж имеет следующие пять измерений: продавец, геоГрафия, время, продукты и меры.</span><span class="sxs-lookup"><span data-stu-id="7f74f-120">For example, a cube containing sales data has the following five dimensions: Salesperson, Geography, Time, Products, and Measures.</span></span> <span data-ttu-id="7f74f-121">Измерение Measures содержит фактические значения данных продаж, а другие измерения представляют способы категоризации и группировки значений данных продаж.</span><span class="sxs-lookup"><span data-stu-id="7f74f-121">The Measures dimension contains actual sales data values, while the other dimensions represent ways to categorize and group the sales data values.</span></span>

<span data-ttu-id="7f74f-122">Измерение Geography имеет следующий набор элементов:</span><span class="sxs-lookup"><span data-stu-id="7f74f-122">The Geography dimension has the following set of members:</span></span>

```text
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a><span data-ttu-id="7f74f-123">Hierarchies</span><span class="sxs-lookup"><span data-stu-id="7f74f-123">Hierarchies</span></span>

<span data-ttu-id="7f74f-124">Иерархии определяют способы, с помощью которых уровни измерения могут быть сведены или сгруппированы.</span><span class="sxs-lookup"><span data-stu-id="7f74f-124">Hierarchies define the ways in which the levels of a dimension can be "rolled up" or grouped.</span></span> <span data-ttu-id="7f74f-125">Измерение может иметь несколько иерархий.</span><span class="sxs-lookup"><span data-stu-id="7f74f-125">A dimension can have more than one hierarchy.</span></span>

## <a name="levels"></a><span data-ttu-id="7f74f-126">Levels</span><span class="sxs-lookup"><span data-stu-id="7f74f-126">Levels</span></span>

<span data-ttu-id="7f74f-127">В примере измерения геоГрафия, изображенного на предыдущем рисунке, каждое поле представляет уровень в иерархии.</span><span class="sxs-lookup"><span data-stu-id="7f74f-127">In the example Geography dimension pictured in the previous figure, each box represents a level in the hierarchy.</span></span>

<span data-ttu-id="7f74f-128">Каждый уровень имеет набор элементов следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7f74f-128">Each level has a set of members, as follows:</span></span>

  - <span data-ttu-id="7f74f-129">Мир = {ALL}</span><span class="sxs-lookup"><span data-stu-id="7f74f-129">The World = {All}</span></span>

  - <span data-ttu-id="7f74f-130">Континенты = {Северная Америка, Европа}</span><span class="sxs-lookup"><span data-stu-id="7f74f-130">Continents = {North America, Europe}</span></span>

  - <span data-ttu-id="7f74f-131">Страны = {Канада, США, Великобритания, Германия}</span><span class="sxs-lookup"><span data-stu-id="7f74f-131">Countries = {Canada, USA, UK, Germany}</span></span>

  - <span data-ttu-id="7f74f-132">Регионы = {Канада-Восток, Канада-Запад, США-NE, США-NW, США-SE, USA-SW, Англия, Ирландия, Шотландии, Красноярск, Германия-север, Германия-Южный}</span><span class="sxs-lookup"><span data-stu-id="7f74f-132">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span></span>

  - <span data-ttu-id="7f74f-133">Города = {Ottawa, Торонто, Vancouver, Калгари, Сиэтл, Бойсе, Лос, Хьюстон, Шревепорт, Майами, Бостон, Нью Йорк, Лондон, Довер, Гласгов, Эдинбург, Кардифф, Пемброке, Белфаст, Берлин, Хамбург, Мунич, Штутгарте, Берлин,,,, Берлин,,,</span><span class="sxs-lookup"><span data-stu-id="7f74f-133">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}</span></span>

## <a name="members"></a><span data-ttu-id="7f74f-134">Members</span><span class="sxs-lookup"><span data-stu-id="7f74f-134">Members</span></span>

<span data-ttu-id="7f74f-135">Элементы на конечном уровне иерархии не имеют дочерних элементов, а элементы на уровне корня не имеют родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="7f74f-135">Members at the leaf level of a hierarchy have no children, and members at the root level have no parent.</span></span> <span data-ttu-id="7f74f-136">Все остальные члены имеют по крайней мере один родительский элемент и по крайней мере один дочерний элемент.</span><span class="sxs-lookup"><span data-stu-id="7f74f-136">All other members have at least one parent and at least one child.</span></span> <span data-ttu-id="7f74f-137">Например, частичное прохождение дерева иерархии в измерении Geography дает следующие связи между родительскими и дочерними узлами:</span><span class="sxs-lookup"><span data-stu-id="7f74f-137">For example, a partial traversal of the hierarchy tree in the Geography dimension yields the following parent-child relationships:</span></span>

- <span data-ttu-id="7f74f-138">Ко (родительский объект) {Европа, Северная Америка}</span><span class="sxs-lookup"><span data-stu-id="7f74f-138">{All} (parent of) {Europe, North America}</span></span>
- <span data-ttu-id="7f74f-139">{Северная Америка} (родительский объект) {Канада, США}</span><span class="sxs-lookup"><span data-stu-id="7f74f-139">{North America} (parent of) {Canada, USA}</span></span>
- <span data-ttu-id="7f74f-140">ЗАКАЗЧИКА (родительский объект) {USA — NE, США – NW, США – SE, США/SW}</span><span class="sxs-lookup"><span data-stu-id="7f74f-140">{USA} (parent of) {USA-NE, USA-NW, USA-SE, USA-SW}</span></span>
- <span data-ttu-id="7f74f-141">{USA — NW} (родительский объект) {Бойсе, Сиэтл}</span><span class="sxs-lookup"><span data-stu-id="7f74f-141">{USA-NW} (parent of) {Boise, Seattle}</span></span>

<span data-ttu-id="7f74f-142">Элементы можно консолидировать по одной или нескольким иерархиям для каждого измерения.</span><span class="sxs-lookup"><span data-stu-id="7f74f-142">Members can be consolidated along one or more hierarchies per dimension.</span></span>

<span data-ttu-id="7f74f-143">В этом примере также показана другая характеристика: некоторые элементы уровня "Неделя" в иерархии "год за год" не отображаются ни на одном уровне иерархии "год за квартал".</span><span class="sxs-lookup"><span data-stu-id="7f74f-143">This example also illustrates another characteristic: some members of the Week level of the Year-Week hierarchy do not appear in any level of the Year-Quarter hierarchy.</span></span> <span data-ttu-id="7f74f-144">Таким образом, иерархия не требуется включать все элементы измерения.</span><span class="sxs-lookup"><span data-stu-id="7f74f-144">Thus, a hierarchy need not include all members of a dimension.</span></span>

## <a name="understanding-multidimensional-schemas"></a><span data-ttu-id="7f74f-145">Общие сведения о многомерных схемах</span><span class="sxs-lookup"><span data-stu-id="7f74f-145">Understanding Multidimensional Schemas</span></span>

<span data-ttu-id="7f74f-146">Центральным объектом метаданных в ADO MD является *куб*, состоящий из структурированного набора связанных измерений, иерархий, уровней и элементов.</span><span class="sxs-lookup"><span data-stu-id="7f74f-146">The central metadata object in ADO MD is the *cube*, which consists of a structured set of related dimensions, hierarchies, levels, and members.</span></span>

<span data-ttu-id="7f74f-147">*Измерение* — это независимая категория данных из многомерной базы данных, которая является производной от ваших бизнес-сущностей.</span><span class="sxs-lookup"><span data-stu-id="7f74f-147">A *dimension* is an independent category of data from your multidimensional database, derived from your business entities.</span></span> <span data-ttu-id="7f74f-148">Измерение обычно содержит элементы, которые будут использоваться в качестве критериев запроса для мер базы данных.</span><span class="sxs-lookup"><span data-stu-id="7f74f-148">A dimension typically contains items to be used as query criteria for the measures of the database.</span></span>

<span data-ttu-id="7f74f-149">*Иерархия* это путь статистической обработки измерения.</span><span class="sxs-lookup"><span data-stu-id="7f74f-149">A *hierarchy* is a path of aggregation of a dimension.</span></span> <span data-ttu-id="7f74f-150">Измерение может иметь несколько уровней гранулярности, которые имеют отношения "родители — потомки".</span><span class="sxs-lookup"><span data-stu-id="7f74f-150">A dimension may have multiple levels of granularity, which have parent-child relationships.</span></span> <span data-ttu-id="7f74f-151">Иерархия определяет способ связи этих уровней.</span><span class="sxs-lookup"><span data-stu-id="7f74f-151">A hierarchy defines how these levels are related.</span></span>

<span data-ttu-id="7f74f-152">*Уровень* — это шаг статистической обработки в иерархии.</span><span class="sxs-lookup"><span data-stu-id="7f74f-152">A *level* is a step of aggregation in a hierarchy.</span></span> <span data-ttu-id="7f74f-153">Для измерений с несколькими уровнями информации каждый уровень является уровнем.</span><span class="sxs-lookup"><span data-stu-id="7f74f-153">For dimensions with multiple layers of information, each layer is a level.</span></span>

<span data-ttu-id="7f74f-154">Элемент \*\* — это элемент данных в измерении.</span><span class="sxs-lookup"><span data-stu-id="7f74f-154">A *member* is a data item in a dimension.</span></span> <span data-ttu-id="7f74f-155">Как правило, при создании заголовка или описания меры базы данных используются члены.</span><span class="sxs-lookup"><span data-stu-id="7f74f-155">Typically, you create a caption or describe a measure of the database using members.</span></span>

<span data-ttu-id="7f74f-156">Кубы представлены объектами [CubeDef](cubedef-object-ado-md.md) в ADO MD.</span><span class="sxs-lookup"><span data-stu-id="7f74f-156">Cubes are represented by [CubeDef](cubedef-object-ado-md.md) objects in ADO MD.</span></span> <span data-ttu-id="7f74f-157">Измерения, иерархии, уровни и элементы также представлены соответствующими объектами ADO MD: [измерение](dimension-object-ado-md.md), иерархия, [уровень](level-object-ado-md.md)и [](hierarchy-object-ado-md.md) [элемент](member-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="7f74f-157">Dimensions, hierarchies, levels, and members are also represented by their corresponding ADO MD objects: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md).</span></span>

## <a name="dimensions"></a><span data-ttu-id="7f74f-158">Dimensions</span><span class="sxs-lookup"><span data-stu-id="7f74f-158">Dimensions</span></span>

<span data-ttu-id="7f74f-159">Измерения куба зависят от бизнес-сущностей и типов данных, которые необходимо моделировать в базе данных.</span><span class="sxs-lookup"><span data-stu-id="7f74f-159">The dimensions of a cube depend on your business entities and types of data to be modeled in the database.</span></span> <span data-ttu-id="7f74f-160">Как правило, каждое измерение — это независимая точка входа или механизм для выбора данных.</span><span class="sxs-lookup"><span data-stu-id="7f74f-160">Typically, each dimension is an independent entry point or mechanism for selecting data.</span></span>

<span data-ttu-id="7f74f-161">Например, куб с данными продаж имеет следующие пять измерений: продавец, геоГрафия, время, продукты и меры.</span><span class="sxs-lookup"><span data-stu-id="7f74f-161">For example, a cube containing sales data has the following five dimensions: Salesperson, Geography, Time, Products, and Measures.</span></span> <span data-ttu-id="7f74f-162">Измерение Measures содержит фактические значения данных продаж, а другие измерения представляют способы категоризации и группировки значений данных продаж.</span><span class="sxs-lookup"><span data-stu-id="7f74f-162">The Measures dimension contains actual sales data values, while the other dimensions represent ways to categorize and group the sales data values.</span></span>

<span data-ttu-id="7f74f-163">Измерение Geography имеет следующий набор элементов:</span><span class="sxs-lookup"><span data-stu-id="7f74f-163">The Geography dimension has the following set of members:</span></span>

```text 
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a><span data-ttu-id="7f74f-164">Hierarchies</span><span class="sxs-lookup"><span data-stu-id="7f74f-164">Hierarchies</span></span>

<span data-ttu-id="7f74f-165">Иерархии определяют способы, с помощью которых уровни измерения могут быть сведены или сгруппированы.</span><span class="sxs-lookup"><span data-stu-id="7f74f-165">Hierarchies define the ways in which the levels of a dimension can be "rolled up" or grouped.</span></span> <span data-ttu-id="7f74f-166">Измерение может иметь несколько иерархий.</span><span class="sxs-lookup"><span data-stu-id="7f74f-166">A dimension can have more than one hierarchy.</span></span>

## <a name="levels"></a><span data-ttu-id="7f74f-167">Levels</span><span class="sxs-lookup"><span data-stu-id="7f74f-167">Levels</span></span>

<span data-ttu-id="7f74f-168">В примере измерения геоГрафия, изображенного на предыдущем рисунке, каждое поле представляет уровень в иерархии.</span><span class="sxs-lookup"><span data-stu-id="7f74f-168">In the example Geography dimension pictured in the previous figure, each box represents a level in the hierarchy.</span></span>

<span data-ttu-id="7f74f-169">Каждый уровень имеет набор элементов следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7f74f-169">Each level has a set of members, as follows:</span></span>

- <span data-ttu-id="7f74f-170">Мир = {ALL}</span><span class="sxs-lookup"><span data-stu-id="7f74f-170">The World = {All}</span></span>

- <span data-ttu-id="7f74f-171">Континенты = {Северная Америка, Европа}</span><span class="sxs-lookup"><span data-stu-id="7f74f-171">Continents = {North America, Europe}</span></span>

- <span data-ttu-id="7f74f-172">Страны = {Канада, США, Великобритания, Германия}</span><span class="sxs-lookup"><span data-stu-id="7f74f-172">Countries = {Canada, USA, UK, Germany}</span></span>

- <span data-ttu-id="7f74f-173">Регионы = {Канада-Восток, Канада-Запад, США-NE, США-NW, США-SE, USA-SW, Англия, Ирландия, Шотландии, Красноярск, Германия-север, Германия-Южный}</span><span class="sxs-lookup"><span data-stu-id="7f74f-173">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span></span>

- <span data-ttu-id="7f74f-174">Города = {Ottawa, Торонто, Vancouver, Калгари, Сиэтл, Бойсе, Лос, Хьюстон, Шревепорт, Майами, Бостон, Нью Йорк, Лондон, Довер, Гласгов, Эдинбург, Кардифф, Пемброке, Белфаст, Берлин, Хамбург, Мунич, Штутгарте, Берлин,,,, Берлин,,,</span><span class="sxs-lookup"><span data-stu-id="7f74f-174">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}</span></span>

## <a name="members"></a><span data-ttu-id="7f74f-175">Members</span><span class="sxs-lookup"><span data-stu-id="7f74f-175">Members</span></span>

<span data-ttu-id="7f74f-176">Элементы на конечном уровне иерархии не имеют дочерних элементов, а элементы на уровне корня не имеют родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="7f74f-176">Members at the leaf level of a hierarchy have no children, and members at the root level have no parent.</span></span> <span data-ttu-id="7f74f-177">Все остальные члены имеют по крайней мере один родительский элемент и по крайней мере один дочерний элемент.</span><span class="sxs-lookup"><span data-stu-id="7f74f-177">All other members have at least one parent and at least one child.</span></span> <span data-ttu-id="7f74f-178">Например, частичное прохождение дерева иерархии в измерении Geography дает следующие связи между родительскими и дочерними узлами:</span><span class="sxs-lookup"><span data-stu-id="7f74f-178">For example, a partial traversal of the hierarchy tree in the Geography dimension yields the following parent-child relationships:</span></span>

- <span data-ttu-id="7f74f-179">Ко (родительский объект) {Европа, Северная Америка}</span><span class="sxs-lookup"><span data-stu-id="7f74f-179">{All} (parent of) {Europe, North America}</span></span>

- <span data-ttu-id="7f74f-180">{Северная Америка} (родительский объект) {Канада, США}</span><span class="sxs-lookup"><span data-stu-id="7f74f-180">{North America} (parent of) {Canada, USA}</span></span>

- <span data-ttu-id="7f74f-181">ЗАКАЗЧИКА (родительский объект) {USA — NE, США – NW, США – SE, США/SW}</span><span class="sxs-lookup"><span data-stu-id="7f74f-181">{USA} (parent of) {USA-NE, USA-NW, USA-SE, USA-SW}</span></span>

- <span data-ttu-id="7f74f-182">{USA — NW} (родительский объект) {Бойсе, Сиэтл}</span><span class="sxs-lookup"><span data-stu-id="7f74f-182">{USA-NW} (parent of) {Boise, Seattle}</span></span>

<span data-ttu-id="7f74f-183">Элементы можно консолидировать по одной или нескольким иерархиям для каждого измерения.</span><span class="sxs-lookup"><span data-stu-id="7f74f-183">Members can be consolidated along one or more hierarchies per dimension.</span></span>

<span data-ttu-id="7f74f-184">В этом примере также показана другая характеристика: некоторые элементы уровня "Неделя" в иерархии "год за год" не отображаются ни на одном уровне иерархии "год за квартал".</span><span class="sxs-lookup"><span data-stu-id="7f74f-184">This example also illustrates another characteristic: some members of the Week level of the Year-Week hierarchy do not appear in any level of the Year-Quarter hierarchy.</span></span> <span data-ttu-id="7f74f-185">Таким образом, иерархия не требуется включать все элементы измерения.</span><span class="sxs-lookup"><span data-stu-id="7f74f-185">Thus, a hierarchy need not include all members of a dimension.</span></span>

