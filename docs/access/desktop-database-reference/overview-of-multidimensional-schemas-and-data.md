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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720221"
---
# <a name="overview-of-multidimensional-schemas-and-data"></a><span data-ttu-id="0aec0-102">Обзор многомерных схем и данных</span><span class="sxs-lookup"><span data-stu-id="0aec0-102">Overview of multidimensional schemas and data</span></span>

<span data-ttu-id="0aec0-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0aec0-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="understanding-multidimensional-schemas"></a><span data-ttu-id="0aec0-104">Общие сведения о многомерных схем</span><span class="sxs-lookup"><span data-stu-id="0aec0-104">Understanding Multidimensional Schemas</span></span>

<span data-ttu-id="0aec0-105">Объект центра метаданных в ADO MD является *куба*, которое состоит из структурированный набор связанных измерений, иерархии, уровни и элементы.</span><span class="sxs-lookup"><span data-stu-id="0aec0-105">The central metadata object in ADO MD is the *cube*, which consists of a structured set of related dimensions, hierarchies, levels, and members.</span></span>

<span data-ttu-id="0aec0-106">*Измерение* является независимой категории данных из многомерной базы данных, производные от бизнес-сущности.</span><span class="sxs-lookup"><span data-stu-id="0aec0-106">A *dimension* is an independent category of data from your multidimensional database, derived from your business entities.</span></span> <span data-ttu-id="0aec0-107">Измерения обычно содержит элементы для использования в качестве условия запроса для меры базы данных.</span><span class="sxs-lookup"><span data-stu-id="0aec0-107">A dimension typically contains items to be used as query criteria for the measures of the database.</span></span>

<span data-ttu-id="0aec0-108">*Иерархия* — это путь статистической обработки измерения.</span><span class="sxs-lookup"><span data-stu-id="0aec0-108">A *hierarchy* is a path of aggregation of a dimension.</span></span> <span data-ttu-id="0aec0-109">Измерение может иметь несколько уровни детализации, имеющие родительских и дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="0aec0-109">A dimension may have multiple levels of granularity, which have parent-child relationships.</span></span> <span data-ttu-id="0aec0-110">Иерархия определяет, как взаимосвязаны эти уровни.</span><span class="sxs-lookup"><span data-stu-id="0aec0-110">A hierarchy defines how these levels are related.</span></span>

<span data-ttu-id="0aec0-111">*Уровень* — шаг статистической обработки в иерархии.</span><span class="sxs-lookup"><span data-stu-id="0aec0-111">A *level* is a step of aggregation in a hierarchy.</span></span> <span data-ttu-id="0aec0-112">Для измерений несколько уровней сведения о каждом уровне находится на уровне.</span><span class="sxs-lookup"><span data-stu-id="0aec0-112">For dimensions with multiple layers of information, each layer is a level.</span></span>

<span data-ttu-id="0aec0-113">*Участник* — это элемент данных в измерении.</span><span class="sxs-lookup"><span data-stu-id="0aec0-113">A *member* is a data item in a dimension.</span></span> <span data-ttu-id="0aec0-114">Как правило создайте заголовка или описания величин базы данных с помощью элементов.</span><span class="sxs-lookup"><span data-stu-id="0aec0-114">Typically, you create a caption or describe a measure of the database using members.</span></span>

<span data-ttu-id="0aec0-115">Кубы, представленные объектами [CubeDef](cubedef-object-ado-md.md) в ADO MD.</span><span class="sxs-lookup"><span data-stu-id="0aec0-115">Cubes are represented by [CubeDef](cubedef-object-ado-md.md) objects in ADO MD.</span></span> <span data-ttu-id="0aec0-116">Измерения, иерархии, уровни и элементы также представлены их соответствующими объектами ADO MD: [ [измерений](dimension-object-ado-md.md), [иерархии](hierarchy-object-ado-md.md)и [член](member-object-ado-md.md)](level-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="0aec0-116">Dimensions, hierarchies, levels, and members are also represented by their corresponding ADO MD objects: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md).</span></span>

## <a name="dimensions"></a><span data-ttu-id="0aec0-117">Dimensions</span><span class="sxs-lookup"><span data-stu-id="0aec0-117">Dimensions</span></span>

<span data-ttu-id="0aec0-118">Измерения куба зависят от бизнес-сущности и типы данных по моделированию в базе данных.</span><span class="sxs-lookup"><span data-stu-id="0aec0-118">The dimensions of a cube depend on your business entities and types of data to be modeled in the database.</span></span> <span data-ttu-id="0aec0-119">Как правило каждого измерения — независимые Начальная точка для входа или механизм выбора данных.</span><span class="sxs-lookup"><span data-stu-id="0aec0-119">Typically, each dimension is an independent entry point or mechanism for selecting data.</span></span>

<span data-ttu-id="0aec0-120">Например, куб, содержащий данные о продажах имеет следующие пять размеры: продавца, Geography, время, продукты и меры.</span><span class="sxs-lookup"><span data-stu-id="0aec0-120">For example, a cube containing sales data has the following five dimensions: Salesperson, Geography, Time, Products, and Measures.</span></span> <span data-ttu-id="0aec0-121">Измерение мер содержит значения фактические данные о продажах, тогда как другие измерения представляют собой способы распределения по категориям и значений данные о продажах.</span><span class="sxs-lookup"><span data-stu-id="0aec0-121">The Measures dimension contains actual sales data values, while the other dimensions represent ways to categorize and group the sales data values.</span></span>

<span data-ttu-id="0aec0-122">Измерение Geography имеет следующий набор элементов:</span><span class="sxs-lookup"><span data-stu-id="0aec0-122">The Geography dimension has the following set of members:</span></span>

```text
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a><span data-ttu-id="0aec0-123">Hierarchies</span><span class="sxs-lookup"><span data-stu-id="0aec0-123">Hierarchies</span></span>

<span data-ttu-id="0aec0-124">Иерархии определить способы, в котором можно «сведения» или сгруппированные уровней измерения.</span><span class="sxs-lookup"><span data-stu-id="0aec0-124">Hierarchies define the ways in which the levels of a dimension can be "rolled up" or grouped.</span></span> <span data-ttu-id="0aec0-125">Измерение может иметь более одной иерархии.</span><span class="sxs-lookup"><span data-stu-id="0aec0-125">A dimension can have more than one hierarchy.</span></span>

## <a name="levels"></a><span data-ttu-id="0aec0-126">Levels</span><span class="sxs-lookup"><span data-stu-id="0aec0-126">Levels</span></span>

<span data-ttu-id="0aec0-127">В измерении Geography примере, представлены на предыдущем рисунке каждое поле представляет уровень в иерархии.</span><span class="sxs-lookup"><span data-stu-id="0aec0-127">In the example Geography dimension pictured in the previous figure, each box represents a level in the hierarchy.</span></span>

<span data-ttu-id="0aec0-128">Каждый уровень содержит набор элементов, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="0aec0-128">Each level has a set of members, as follows:</span></span>

  - <span data-ttu-id="0aec0-129">World = {All}</span><span class="sxs-lookup"><span data-stu-id="0aec0-129">The World = {All}</span></span>

  - <span data-ttu-id="0aec0-130">Континентах = {Северная Америка, Европа}</span><span class="sxs-lookup"><span data-stu-id="0aec0-130">Continents = {North America, Europe}</span></span>

  - <span data-ttu-id="0aec0-131">Странах = {Канада, США, Великобритания, Германия}</span><span class="sxs-lookup"><span data-stu-id="0aec0-131">Countries = {Canada, USA, UK, Germany}</span></span>

  - <span data-ttu-id="0aec0-132">Областей = {East Канада, Канада-Запад США NE, США-NW США-SE (en), США-SW, Англия, Ирландия, Шотландии, Уэльс, Германия-Северной, Южная Германия}</span><span class="sxs-lookup"><span data-stu-id="0aec0-132">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span></span>

  - <span data-ttu-id="0aec0-133">Cities (города) = {Ottawa, Торонто, Vancouver, Калгари, Сиэтл, Буаз, Лос-Анджелес, Хьюстоне, Shreveport, Майами, может, Нью-Йорк, Лондон, Dover, Глазго, Эдинбург, Cardiff, Pembroke, Белфаст, Берлин, Hamburg, Мюнхен, Штутгартский}</span><span class="sxs-lookup"><span data-stu-id="0aec0-133">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}</span></span>

## <a name="members"></a><span data-ttu-id="0aec0-134">Members</span><span class="sxs-lookup"><span data-stu-id="0aec0-134">Members</span></span>

<span data-ttu-id="0aec0-135">Элементы на конечном уровне иерархии не имеющие дочерних элементов и нет родительского имеют члены на корневом уровне.</span><span class="sxs-lookup"><span data-stu-id="0aec0-135">Members at the leaf level of a hierarchy have no children, and members at the root level have no parent.</span></span> <span data-ttu-id="0aec0-136">Другие участники имеют по крайней мере один родительских и дочерних по крайней мере один.</span><span class="sxs-lookup"><span data-stu-id="0aec0-136">All other members have at least one parent and at least one child.</span></span> <span data-ttu-id="0aec0-137">Например частичное обход дерева иерархии в измерении Geography дает следующие отношения родительских и дочерних:</span><span class="sxs-lookup"><span data-stu-id="0aec0-137">For example, a partial traversal of the hierarchy tree in the Geography dimension yields the following parent-child relationships:</span></span>

- <span data-ttu-id="0aec0-138">{All} (родительский) {Европы, Северной Америки}</span><span class="sxs-lookup"><span data-stu-id="0aec0-138">{All} (parent of) {Europe, North America}</span></span>
- <span data-ttu-id="0aec0-139">{Северная Америка} (родительский) {Канада США}</span><span class="sxs-lookup"><span data-stu-id="0aec0-139">{North America} (parent of) {Canada, USA}</span></span>
- <span data-ttu-id="0aec0-140">{США} (родительский) {США NE, США-NW США-SE (EN), США-SW}</span><span class="sxs-lookup"><span data-stu-id="0aec0-140">{USA} (parent of) {USA-NE, USA-NW, USA-SE, USA-SW}</span></span>
- <span data-ttu-id="0aec0-141">{США NW} (родительский) {Буаз Сиэтл}</span><span class="sxs-lookup"><span data-stu-id="0aec0-141">{USA-NW} (parent of) {Boise, Seattle}</span></span>

<span data-ttu-id="0aec0-142">Члены можно объединить вместе один или несколько иерархий на аналитику.</span><span class="sxs-lookup"><span data-stu-id="0aec0-142">Members can be consolidated along one or more hierarchies per dimension.</span></span>

<span data-ttu-id="0aec0-143">В этом примере также показано другой характеристика: некоторые элементы недели уровня иерархии недели года не отображаются на любой уровень иерархии квартал года.</span><span class="sxs-lookup"><span data-stu-id="0aec0-143">This example also illustrates another characteristic: some members of the Week level of the Year-Week hierarchy do not appear in any level of the Year-Quarter hierarchy.</span></span> <span data-ttu-id="0aec0-144">Таким образом иерархии не обязательно должны включать все элементы измерения.</span><span class="sxs-lookup"><span data-stu-id="0aec0-144">Thus, a hierarchy need not include all members of a dimension.</span></span>

## <a name="understanding-multidimensional-schemas"></a><span data-ttu-id="0aec0-145">Общие сведения о многомерных схем</span><span class="sxs-lookup"><span data-stu-id="0aec0-145">Understanding Multidimensional Schemas</span></span>

<span data-ttu-id="0aec0-146">Объект центра метаданных в ADO MD является *куба*, которое состоит из структурированный набор связанных измерений, иерархии, уровни и элементы.</span><span class="sxs-lookup"><span data-stu-id="0aec0-146">The central metadata object in ADO MD is the *cube*, which consists of a structured set of related dimensions, hierarchies, levels, and members.</span></span>

<span data-ttu-id="0aec0-147">*Измерение* является независимой категории данных из многомерной базы данных, производные от бизнес-сущности.</span><span class="sxs-lookup"><span data-stu-id="0aec0-147">A *dimension* is an independent category of data from your multidimensional database, derived from your business entities.</span></span> <span data-ttu-id="0aec0-148">Измерения обычно содержит элементы для использования в качестве условия запроса для меры базы данных.</span><span class="sxs-lookup"><span data-stu-id="0aec0-148">A dimension typically contains items to be used as query criteria for the measures of the database.</span></span>

<span data-ttu-id="0aec0-149">*Иерархия* — это путь статистической обработки измерения.</span><span class="sxs-lookup"><span data-stu-id="0aec0-149">A *hierarchy* is a path of aggregation of a dimension.</span></span> <span data-ttu-id="0aec0-150">Измерение может иметь несколько уровни детализации, имеющие родительских и дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="0aec0-150">A dimension may have multiple levels of granularity, which have parent-child relationships.</span></span> <span data-ttu-id="0aec0-151">Иерархия определяет, как взаимосвязаны эти уровни.</span><span class="sxs-lookup"><span data-stu-id="0aec0-151">A hierarchy defines how these levels are related.</span></span>

<span data-ttu-id="0aec0-152">*Уровень* — шаг статистической обработки в иерархии.</span><span class="sxs-lookup"><span data-stu-id="0aec0-152">A *level* is a step of aggregation in a hierarchy.</span></span> <span data-ttu-id="0aec0-153">Для измерений несколько уровней сведения о каждом уровне находится на уровне.</span><span class="sxs-lookup"><span data-stu-id="0aec0-153">For dimensions with multiple layers of information, each layer is a level.</span></span>

<span data-ttu-id="0aec0-154">*Участник* — это элемент данных в измерении.</span><span class="sxs-lookup"><span data-stu-id="0aec0-154">A *member* is a data item in a dimension.</span></span> <span data-ttu-id="0aec0-155">Как правило создайте заголовка или описания величин базы данных с помощью элементов.</span><span class="sxs-lookup"><span data-stu-id="0aec0-155">Typically, you create a caption or describe a measure of the database using members.</span></span>

<span data-ttu-id="0aec0-156">Кубы, представленные объектами [CubeDef](cubedef-object-ado-md.md) в ADO MD.</span><span class="sxs-lookup"><span data-stu-id="0aec0-156">Cubes are represented by [CubeDef](cubedef-object-ado-md.md) objects in ADO MD.</span></span> <span data-ttu-id="0aec0-157">Измерения, иерархии, уровни и элементы также представлены их соответствующими объектами ADO MD: [ [измерений](dimension-object-ado-md.md), [иерархии](hierarchy-object-ado-md.md)и [член](member-object-ado-md.md)](level-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="0aec0-157">Dimensions, hierarchies, levels, and members are also represented by their corresponding ADO MD objects: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md).</span></span>

## <a name="dimensions"></a><span data-ttu-id="0aec0-158">Dimensions</span><span class="sxs-lookup"><span data-stu-id="0aec0-158">Dimensions</span></span>

<span data-ttu-id="0aec0-159">Измерения куба зависят от бизнес-сущности и типы данных по моделированию в базе данных.</span><span class="sxs-lookup"><span data-stu-id="0aec0-159">The dimensions of a cube depend on your business entities and types of data to be modeled in the database.</span></span> <span data-ttu-id="0aec0-160">Как правило каждого измерения — независимые Начальная точка для входа или механизм выбора данных.</span><span class="sxs-lookup"><span data-stu-id="0aec0-160">Typically, each dimension is an independent entry point or mechanism for selecting data.</span></span>

<span data-ttu-id="0aec0-161">Например, куб, содержащий данные о продажах имеет следующие пять размеры: продавца, Geography, время, продукты и меры.</span><span class="sxs-lookup"><span data-stu-id="0aec0-161">For example, a cube containing sales data has the following five dimensions: Salesperson, Geography, Time, Products, and Measures.</span></span> <span data-ttu-id="0aec0-162">Измерение мер содержит значения фактические данные о продажах, тогда как другие измерения представляют собой способы распределения по категориям и значений данные о продажах.</span><span class="sxs-lookup"><span data-stu-id="0aec0-162">The Measures dimension contains actual sales data values, while the other dimensions represent ways to categorize and group the sales data values.</span></span>

<span data-ttu-id="0aec0-163">Измерение Geography имеет следующий набор элементов:</span><span class="sxs-lookup"><span data-stu-id="0aec0-163">The Geography dimension has the following set of members:</span></span>

```text 
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a><span data-ttu-id="0aec0-164">Hierarchies</span><span class="sxs-lookup"><span data-stu-id="0aec0-164">Hierarchies</span></span>

<span data-ttu-id="0aec0-165">Иерархии определить способы, в котором можно «сведения» или сгруппированные уровней измерения.</span><span class="sxs-lookup"><span data-stu-id="0aec0-165">Hierarchies define the ways in which the levels of a dimension can be "rolled up" or grouped.</span></span> <span data-ttu-id="0aec0-166">Измерение может иметь более одной иерархии.</span><span class="sxs-lookup"><span data-stu-id="0aec0-166">A dimension can have more than one hierarchy.</span></span>

## <a name="levels"></a><span data-ttu-id="0aec0-167">Levels</span><span class="sxs-lookup"><span data-stu-id="0aec0-167">Levels</span></span>

<span data-ttu-id="0aec0-168">В измерении Geography примере, представлены на предыдущем рисунке каждое поле представляет уровень в иерархии.</span><span class="sxs-lookup"><span data-stu-id="0aec0-168">In the example Geography dimension pictured in the previous figure, each box represents a level in the hierarchy.</span></span>

<span data-ttu-id="0aec0-169">Каждый уровень содержит набор элементов, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="0aec0-169">Each level has a set of members, as follows:</span></span>

- <span data-ttu-id="0aec0-170">World = {All}</span><span class="sxs-lookup"><span data-stu-id="0aec0-170">The World = {All}</span></span>

- <span data-ttu-id="0aec0-171">Континентах = {Северная Америка, Европа}</span><span class="sxs-lookup"><span data-stu-id="0aec0-171">Continents = {North America, Europe}</span></span>

- <span data-ttu-id="0aec0-172">Странах = {Канада, США, Великобритания, Германия}</span><span class="sxs-lookup"><span data-stu-id="0aec0-172">Countries = {Canada, USA, UK, Germany}</span></span>

- <span data-ttu-id="0aec0-173">Областей = {East Канада, Канада-Запад США NE, США-NW США-SE (en), США-SW, Англия, Ирландия, Шотландии, Уэльс, Германия-Северной, Южная Германия}</span><span class="sxs-lookup"><span data-stu-id="0aec0-173">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span></span>

- <span data-ttu-id="0aec0-174">Cities (города) = {Ottawa, Торонто, Vancouver, Калгари, Сиэтл, Буаз, Лос-Анджелес, Хьюстоне, Shreveport, Майами, может, Нью-Йорк, Лондон, Dover, Глазго, Эдинбург, Cardiff, Pembroke, Белфаст, Берлин, Hamburg, Мюнхен, Штутгартский}</span><span class="sxs-lookup"><span data-stu-id="0aec0-174">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}</span></span>

## <a name="members"></a><span data-ttu-id="0aec0-175">Members</span><span class="sxs-lookup"><span data-stu-id="0aec0-175">Members</span></span>

<span data-ttu-id="0aec0-176">Элементы на конечном уровне иерархии не имеющие дочерних элементов и нет родительского имеют члены на корневом уровне.</span><span class="sxs-lookup"><span data-stu-id="0aec0-176">Members at the leaf level of a hierarchy have no children, and members at the root level have no parent.</span></span> <span data-ttu-id="0aec0-177">Другие участники имеют по крайней мере один родительских и дочерних по крайней мере один.</span><span class="sxs-lookup"><span data-stu-id="0aec0-177">All other members have at least one parent and at least one child.</span></span> <span data-ttu-id="0aec0-178">Например частичное обход дерева иерархии в измерении Geography дает следующие отношения родительских и дочерних:</span><span class="sxs-lookup"><span data-stu-id="0aec0-178">For example, a partial traversal of the hierarchy tree in the Geography dimension yields the following parent-child relationships:</span></span>

- <span data-ttu-id="0aec0-179">{All} (родительский) {Европы, Северной Америки}</span><span class="sxs-lookup"><span data-stu-id="0aec0-179">{All} (parent of) {Europe, North America}</span></span>

- <span data-ttu-id="0aec0-180">{Северная Америка} (родительский) {Канада США}</span><span class="sxs-lookup"><span data-stu-id="0aec0-180">{North America} (parent of) {Canada, USA}</span></span>

- <span data-ttu-id="0aec0-181">{США} (родительский) {США NE, США-NW США-SE (EN), США-SW}</span><span class="sxs-lookup"><span data-stu-id="0aec0-181">{USA} (parent of) {USA-NE, USA-NW, USA-SE, USA-SW}</span></span>

- <span data-ttu-id="0aec0-182">{США NW} (родительский) {Буаз Сиэтл}</span><span class="sxs-lookup"><span data-stu-id="0aec0-182">{USA-NW} (parent of) {Boise, Seattle}</span></span>

<span data-ttu-id="0aec0-183">Члены можно объединить вместе один или несколько иерархий на аналитику.</span><span class="sxs-lookup"><span data-stu-id="0aec0-183">Members can be consolidated along one or more hierarchies per dimension.</span></span>

<span data-ttu-id="0aec0-184">В этом примере также показано другой характеристика: некоторые элементы недели уровня иерархии недели года не отображаются на любой уровень иерархии квартал года.</span><span class="sxs-lookup"><span data-stu-id="0aec0-184">This example also illustrates another characteristic: some members of the Week level of the Year-Week hierarchy do not appear in any level of the Year-Quarter hierarchy.</span></span> <span data-ttu-id="0aec0-185">Таким образом иерархии не обязательно должны включать все элементы измерения.</span><span class="sxs-lookup"><span data-stu-id="0aec0-185">Thus, a hierarchy need not include all members of a dimension.</span></span>

