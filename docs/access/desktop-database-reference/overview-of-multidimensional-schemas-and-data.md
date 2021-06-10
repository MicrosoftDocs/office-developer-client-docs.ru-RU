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
# <a name="overview-of-multidimensional-schemas-and-data"></a><span data-ttu-id="f4ac1-102">Обзор многомерных схем и данных</span><span class="sxs-lookup"><span data-stu-id="f4ac1-102">Overview of multidimensional schemas and data</span></span>

<span data-ttu-id="f4ac1-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f4ac1-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="understanding-multidimensional-schemas"></a><span data-ttu-id="f4ac1-104">Понимание многомерных схем</span><span class="sxs-lookup"><span data-stu-id="f4ac1-104">Understanding Multidimensional Schemas</span></span>

<span data-ttu-id="f4ac1-105">Центральным объектом метаданных в ADO MD является *куб,* состоящий из структурированного набора связанных измерений, иерархий, уровней и участников.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-105">The central metadata object in ADO MD is the *cube*, which consists of a structured set of related dimensions, hierarchies, levels, and members.</span></span>

<span data-ttu-id="f4ac1-106">Измерение *—* это независимая категория данных из многомерной базы данных, полученная из бизнес-сущностями.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-106">A *dimension* is an independent category of data from your multidimensional database, derived from your business entities.</span></span> <span data-ttu-id="f4ac1-107">Измерение обычно содержит элементы, которые будут использоваться в качестве критериев запроса для мер базы данных.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-107">A dimension typically contains items to be used as query criteria for the measures of the database.</span></span>

<span data-ttu-id="f4ac1-108">Иерархия *—* это путь агрегации измерения.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-108">A *hierarchy* is a path of aggregation of a dimension.</span></span> <span data-ttu-id="f4ac1-109">Измерение может иметь несколько уровней детализации, которые имеют родительские и детские отношения.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-109">A dimension may have multiple levels of granularity, which have parent-child relationships.</span></span> <span data-ttu-id="f4ac1-110">Иерархия определяет, как эти уровни связаны.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-110">A hierarchy defines how these levels are related.</span></span>

<span data-ttu-id="f4ac1-111">Уровень *—* это шаг агрегации в иерархии.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-111">A *level* is a step of aggregation in a hierarchy.</span></span> <span data-ttu-id="f4ac1-112">Для размеров с несколькими уровнями информации каждый слой является уровнем.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-112">For dimensions with multiple layers of information, each layer is a level.</span></span>

<span data-ttu-id="f4ac1-113">Член *—* это элемент данных в измерении.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-113">A *member* is a data item in a dimension.</span></span> <span data-ttu-id="f4ac1-114">Как правило, вы создаете подпись или описываете меру базы данных с помощью участников.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-114">Typically, you create a caption or describe a measure of the database using members.</span></span>

<span data-ttu-id="f4ac1-115">Куби представлены [объектами CubeDef](cubedef-object-ado-md.md) в ADO MD.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-115">Cubes are represented by [CubeDef](cubedef-object-ado-md.md) objects in ADO MD.</span></span> <span data-ttu-id="f4ac1-116">Размеры, иерархии, уровни и члены также представлены соответствующими объектами ADO MD: [Dimension,](dimension-object-ado-md.md) [Hierarchy,](hierarchy-object-ado-md.md) [Level](level-object-ado-md.md)и [Member](member-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="f4ac1-116">Dimensions, hierarchies, levels, and members are also represented by their corresponding ADO MD objects: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md).</span></span>

## <a name="dimensions"></a><span data-ttu-id="f4ac1-117">Dimensions</span><span class="sxs-lookup"><span data-stu-id="f4ac1-117">Dimensions</span></span>

<span data-ttu-id="f4ac1-118">Размеры куба зависят от бизнес-сущностями и типами данных, которые будут моделироваться в базе данных.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-118">The dimensions of a cube depend on your business entities and types of data to be modeled in the database.</span></span> <span data-ttu-id="f4ac1-119">Как правило, каждое измерение является независимой точкой входа или механизмом выбора данных.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-119">Typically, each dimension is an independent entry point or mechanism for selecting data.</span></span>

<span data-ttu-id="f4ac1-120">Например, куб, содержащий данные о продажах, имеет следующие пять измерений: Salesperson, Geography, Time, Products и Measures.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-120">For example, a cube containing sales data has the following five dimensions: Salesperson, Geography, Time, Products, and Measures.</span></span> <span data-ttu-id="f4ac1-121">Измерение Measures содержит фактические значения данных о продажах, в то время как другие измерения представляют способы классификации и группы значений данных о продажах.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-121">The Measures dimension contains actual sales data values, while the other dimensions represent ways to categorize and group the sales data values.</span></span>

<span data-ttu-id="f4ac1-122">Измерение Географии имеет следующий набор участников:</span><span class="sxs-lookup"><span data-stu-id="f4ac1-122">The Geography dimension has the following set of members:</span></span>

```text
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a><span data-ttu-id="f4ac1-123">Hierarchies</span><span class="sxs-lookup"><span data-stu-id="f4ac1-123">Hierarchies</span></span>

<span data-ttu-id="f4ac1-124">Иерархии определяют способы,которыми можно "свернуть" или сгруппить уровни измерения.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-124">Hierarchies define the ways in which the levels of a dimension can be "rolled up" or grouped.</span></span> <span data-ttu-id="f4ac1-125">Измерение может иметь несколько иерархий.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-125">A dimension can have more than one hierarchy.</span></span>

## <a name="levels"></a><span data-ttu-id="f4ac1-126">Levels</span><span class="sxs-lookup"><span data-stu-id="f4ac1-126">Levels</span></span>

<span data-ttu-id="f4ac1-127">В примере измерения географии, изображенном на предыдущем рисунке, каждое поле представляет уровень иерархии.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-127">In the example Geography dimension pictured in the previous figure, each box represents a level in the hierarchy.</span></span>

<span data-ttu-id="f4ac1-128">Каждый уровень имеет набор участников:</span><span class="sxs-lookup"><span data-stu-id="f4ac1-128">Each level has a set of members, as follows:</span></span>

  - <span data-ttu-id="f4ac1-129">Мир = {All}</span><span class="sxs-lookup"><span data-stu-id="f4ac1-129">The World = {All}</span></span>

  - <span data-ttu-id="f4ac1-130">Континенты = {Северная Америка, Европа}</span><span class="sxs-lookup"><span data-stu-id="f4ac1-130">Continents = {North America, Europe}</span></span>

  - <span data-ttu-id="f4ac1-131">Страны = {Канада, США, Великобритания, Германия}</span><span class="sxs-lookup"><span data-stu-id="f4ac1-131">Countries = {Canada, USA, UK, Germany}</span></span>

  - <span data-ttu-id="f4ac1-132">Регионы = {Canada-East, Canada-West, USA-NE, USA-NW, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span><span class="sxs-lookup"><span data-stu-id="f4ac1-132">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span></span>

  - <span data-ttu-id="f4ac1-133">Города = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}</span><span class="sxs-lookup"><span data-stu-id="f4ac1-133">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}</span></span>

## <a name="members"></a><span data-ttu-id="f4ac1-134">"Участники"</span><span class="sxs-lookup"><span data-stu-id="f4ac1-134">Members</span></span>

<span data-ttu-id="f4ac1-135">Члены на уровне листа иерархии не имеют детей, а члены на корневом уровне не имеют родителей.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-135">Members at the leaf level of a hierarchy have no children, and members at the root level have no parent.</span></span> <span data-ttu-id="f4ac1-136">Все остальные члены имеют по крайней мере одного родителя и по крайней мере одного ребенка.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-136">All other members have at least one parent and at least one child.</span></span> <span data-ttu-id="f4ac1-137">Например, частичный обход дерева иерархии в измерении География дает следующие отношения между родителем и ребенком:</span><span class="sxs-lookup"><span data-stu-id="f4ac1-137">For example, a partial traversal of the hierarchy tree in the Geography dimension yields the following parent-child relationships:</span></span>

- <span data-ttu-id="f4ac1-138">{All} (родитель) {Европа, Северная Америка}</span><span class="sxs-lookup"><span data-stu-id="f4ac1-138">{All} (parent of) {Europe, North America}</span></span>
- <span data-ttu-id="f4ac1-139">{Северная Америка} (родитель) {Канада, США}</span><span class="sxs-lookup"><span data-stu-id="f4ac1-139">{North America} (parent of) {Canada, USA}</span></span>
- <span data-ttu-id="f4ac1-140">{USA} (родитель) {USA-NE, USA-NW, USA-SE, USA-SW}</span><span class="sxs-lookup"><span data-stu-id="f4ac1-140">{USA} (parent of) {USA-NE, USA-NW, USA-SE, USA-SW}</span></span>
- <span data-ttu-id="f4ac1-141">{USA-NW} (родитель) {Boise, Seattle}</span><span class="sxs-lookup"><span data-stu-id="f4ac1-141">{USA-NW} (parent of) {Boise, Seattle}</span></span>

<span data-ttu-id="f4ac1-142">Участники могут быть консолидированы по одной или несколько иерархий на одно измерение.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-142">Members can be consolidated along one or more hierarchies per dimension.</span></span>

<span data-ttu-id="f4ac1-143">В этом примере также иллюстрируется другая характеристика: некоторые члены уровня недели иерархии Year-Week не отображаются ни на одном уровне иерархии Year-Quarter.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-143">This example also illustrates another characteristic: some members of the Week level of the Year-Week hierarchy do not appear in any level of the Year-Quarter hierarchy.</span></span> <span data-ttu-id="f4ac1-144">Таким образом, иерархия не должна включать все члены измерения.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-144">Thus, a hierarchy need not include all members of a dimension.</span></span>

## <a name="understanding-multidimensional-schemas"></a><span data-ttu-id="f4ac1-145">Понимание многомерных схем</span><span class="sxs-lookup"><span data-stu-id="f4ac1-145">Understanding Multidimensional Schemas</span></span>

<span data-ttu-id="f4ac1-146">Центральным объектом метаданных в ADO MD является *куб,* состоящий из структурированного набора связанных измерений, иерархий, уровней и участников.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-146">The central metadata object in ADO MD is the *cube*, which consists of a structured set of related dimensions, hierarchies, levels, and members.</span></span>

<span data-ttu-id="f4ac1-147">Измерение *—* это независимая категория данных из многомерной базы данных, полученная из бизнес-сущностями.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-147">A *dimension* is an independent category of data from your multidimensional database, derived from your business entities.</span></span> <span data-ttu-id="f4ac1-148">Измерение обычно содержит элементы, которые будут использоваться в качестве критериев запроса для мер базы данных.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-148">A dimension typically contains items to be used as query criteria for the measures of the database.</span></span>

<span data-ttu-id="f4ac1-149">Иерархия *—* это путь агрегации измерения.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-149">A *hierarchy* is a path of aggregation of a dimension.</span></span> <span data-ttu-id="f4ac1-150">Измерение может иметь несколько уровней детализации, которые имеют родительские и детские отношения.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-150">A dimension may have multiple levels of granularity, which have parent-child relationships.</span></span> <span data-ttu-id="f4ac1-151">Иерархия определяет, как эти уровни связаны.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-151">A hierarchy defines how these levels are related.</span></span>

<span data-ttu-id="f4ac1-152">Уровень *—* это шаг агрегации в иерархии.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-152">A *level* is a step of aggregation in a hierarchy.</span></span> <span data-ttu-id="f4ac1-153">Для размеров с несколькими уровнями информации каждый слой является уровнем.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-153">For dimensions with multiple layers of information, each layer is a level.</span></span>

<span data-ttu-id="f4ac1-154">Член *—* это элемент данных в измерении.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-154">A *member* is a data item in a dimension.</span></span> <span data-ttu-id="f4ac1-155">Как правило, вы создаете подпись или описываете меру базы данных с помощью участников.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-155">Typically, you create a caption or describe a measure of the database using members.</span></span>

<span data-ttu-id="f4ac1-156">Куби представлены [объектами CubeDef](cubedef-object-ado-md.md) в ADO MD.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-156">Cubes are represented by [CubeDef](cubedef-object-ado-md.md) objects in ADO MD.</span></span> <span data-ttu-id="f4ac1-157">Размеры, иерархии, уровни и члены также представлены соответствующими объектами ADO MD: [Dimension,](dimension-object-ado-md.md) [Hierarchy,](hierarchy-object-ado-md.md) [Level](level-object-ado-md.md)и [Member](member-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="f4ac1-157">Dimensions, hierarchies, levels, and members are also represented by their corresponding ADO MD objects: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md).</span></span>

## <a name="dimensions"></a><span data-ttu-id="f4ac1-158">Dimensions</span><span class="sxs-lookup"><span data-stu-id="f4ac1-158">Dimensions</span></span>

<span data-ttu-id="f4ac1-159">Размеры куба зависят от бизнес-сущностями и типами данных, которые будут моделироваться в базе данных.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-159">The dimensions of a cube depend on your business entities and types of data to be modeled in the database.</span></span> <span data-ttu-id="f4ac1-160">Как правило, каждое измерение является независимой точкой входа или механизмом выбора данных.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-160">Typically, each dimension is an independent entry point or mechanism for selecting data.</span></span>

<span data-ttu-id="f4ac1-161">Например, куб, содержащий данные о продажах, имеет следующие пять измерений: Salesperson, Geography, Time, Products и Measures.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-161">For example, a cube containing sales data has the following five dimensions: Salesperson, Geography, Time, Products, and Measures.</span></span> <span data-ttu-id="f4ac1-162">Измерение Measures содержит фактические значения данных о продажах, в то время как другие измерения представляют способы классификации и группы значений данных о продажах.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-162">The Measures dimension contains actual sales data values, while the other dimensions represent ways to categorize and group the sales data values.</span></span>

<span data-ttu-id="f4ac1-163">Измерение Географии имеет следующий набор участников:</span><span class="sxs-lookup"><span data-stu-id="f4ac1-163">The Geography dimension has the following set of members:</span></span>

```text 
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a><span data-ttu-id="f4ac1-164">Hierarchies</span><span class="sxs-lookup"><span data-stu-id="f4ac1-164">Hierarchies</span></span>

<span data-ttu-id="f4ac1-165">Иерархии определяют способы,которыми можно "свернуть" или сгруппить уровни измерения.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-165">Hierarchies define the ways in which the levels of a dimension can be "rolled up" or grouped.</span></span> <span data-ttu-id="f4ac1-166">Измерение может иметь несколько иерархий.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-166">A dimension can have more than one hierarchy.</span></span>

## <a name="levels"></a><span data-ttu-id="f4ac1-167">Levels</span><span class="sxs-lookup"><span data-stu-id="f4ac1-167">Levels</span></span>

<span data-ttu-id="f4ac1-168">В примере измерения географии, изображенном на предыдущем рисунке, каждое поле представляет уровень иерархии.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-168">In the example Geography dimension pictured in the previous figure, each box represents a level in the hierarchy.</span></span>

<span data-ttu-id="f4ac1-169">Каждый уровень имеет набор участников:</span><span class="sxs-lookup"><span data-stu-id="f4ac1-169">Each level has a set of members, as follows:</span></span>

- <span data-ttu-id="f4ac1-170">Мир = {All}</span><span class="sxs-lookup"><span data-stu-id="f4ac1-170">The World = {All}</span></span>

- <span data-ttu-id="f4ac1-171">Континенты = {Северная Америка, Европа}</span><span class="sxs-lookup"><span data-stu-id="f4ac1-171">Continents = {North America, Europe}</span></span>

- <span data-ttu-id="f4ac1-172">Страны = {Канада, США, Великобритания, Германия}</span><span class="sxs-lookup"><span data-stu-id="f4ac1-172">Countries = {Canada, USA, UK, Germany}</span></span>

- <span data-ttu-id="f4ac1-173">Регионы = {Canada-East, Canada-West, USA-NE, USA-NW, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span><span class="sxs-lookup"><span data-stu-id="f4ac1-173">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span></span>

- <span data-ttu-id="f4ac1-174">Города = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}</span><span class="sxs-lookup"><span data-stu-id="f4ac1-174">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}</span></span>

## <a name="members"></a><span data-ttu-id="f4ac1-175">"Участники"</span><span class="sxs-lookup"><span data-stu-id="f4ac1-175">Members</span></span>

<span data-ttu-id="f4ac1-176">Члены на уровне листа иерархии не имеют детей, а члены на корневом уровне не имеют родителей.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-176">Members at the leaf level of a hierarchy have no children, and members at the root level have no parent.</span></span> <span data-ttu-id="f4ac1-177">Все остальные члены имеют по крайней мере одного родителя и по крайней мере одного ребенка.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-177">All other members have at least one parent and at least one child.</span></span> <span data-ttu-id="f4ac1-178">Например, частичный обход дерева иерархии в измерении География дает следующие отношения между родителем и ребенком:</span><span class="sxs-lookup"><span data-stu-id="f4ac1-178">For example, a partial traversal of the hierarchy tree in the Geography dimension yields the following parent-child relationships:</span></span>

- <span data-ttu-id="f4ac1-179">{All} (родитель) {Европа, Северная Америка}</span><span class="sxs-lookup"><span data-stu-id="f4ac1-179">{All} (parent of) {Europe, North America}</span></span>

- <span data-ttu-id="f4ac1-180">{Северная Америка} (родитель) {Канада, США}</span><span class="sxs-lookup"><span data-stu-id="f4ac1-180">{North America} (parent of) {Canada, USA}</span></span>

- <span data-ttu-id="f4ac1-181">{USA} (родитель) {USA-NE, USA-NW, USA-SE, USA-SW}</span><span class="sxs-lookup"><span data-stu-id="f4ac1-181">{USA} (parent of) {USA-NE, USA-NW, USA-SE, USA-SW}</span></span>

- <span data-ttu-id="f4ac1-182">{USA-NW} (родитель) {Boise, Seattle}</span><span class="sxs-lookup"><span data-stu-id="f4ac1-182">{USA-NW} (parent of) {Boise, Seattle}</span></span>

<span data-ttu-id="f4ac1-183">Участники могут быть консолидированы по одной или несколько иерархий на одно измерение.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-183">Members can be consolidated along one or more hierarchies per dimension.</span></span>

<span data-ttu-id="f4ac1-184">В этом примере также иллюстрируется другая характеристика: некоторые члены уровня недели иерархии Year-Week не отображаются ни на одном уровне иерархии Year-Quarter.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-184">This example also illustrates another characteristic: some members of the Week level of the Year-Week hierarchy do not appear in any level of the Year-Quarter hierarchy.</span></span> <span data-ttu-id="f4ac1-185">Таким образом, иерархия не должна включать все члены измерения.</span><span class="sxs-lookup"><span data-stu-id="f4ac1-185">Thus, a hierarchy need not include all members of a dimension.</span></span>

