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
# <a name="overview-of-multidimensional-schemas-and-data"></a><span data-ttu-id="71a19-102">Обзор многомерных схем и данных</span><span class="sxs-lookup"><span data-stu-id="71a19-102">Overview of multidimensional schemas and data</span></span>

<span data-ttu-id="71a19-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="71a19-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="understanding-multidimensional-schemas"></a><span data-ttu-id="71a19-104">Understanding Multidimensional Schemas</span><span class="sxs-lookup"><span data-stu-id="71a19-104">Understanding Multidimensional Schemas</span></span>

<span data-ttu-id="71a19-105">Центральный объект метаданных в ADO MD — это *куб,* который состоит из структурированного набора связанных измерений, иерархий, уровней и членов.</span><span class="sxs-lookup"><span data-stu-id="71a19-105">The central metadata object in ADO MD is the *cube*, which consists of a structured set of related dimensions, hierarchies, levels, and members.</span></span>

<span data-ttu-id="71a19-106">Измерение *—* это независимая категория данных из многомерной базы данных, производная от бизнес-сущностями.</span><span class="sxs-lookup"><span data-stu-id="71a19-106">A *dimension* is an independent category of data from your multidimensional database, derived from your business entities.</span></span> <span data-ttu-id="71a19-107">Измерение обычно содержит элементы, используемые в качестве критериев запроса для мер базы данных.</span><span class="sxs-lookup"><span data-stu-id="71a19-107">A dimension typically contains items to be used as query criteria for the measures of the database.</span></span>

<span data-ttu-id="71a19-108">Иерархия *—* это путь агрегации измерения.</span><span class="sxs-lookup"><span data-stu-id="71a19-108">A *hierarchy* is a path of aggregation of a dimension.</span></span> <span data-ttu-id="71a19-109">Измерение может иметь несколько уровней детализации с родительскими и родительскими отношениями.</span><span class="sxs-lookup"><span data-stu-id="71a19-109">A dimension may have multiple levels of granularity, which have parent-child relationships.</span></span> <span data-ttu-id="71a19-110">Иерархия определяет, как эти уровни связаны.</span><span class="sxs-lookup"><span data-stu-id="71a19-110">A hierarchy defines how these levels are related.</span></span>

<span data-ttu-id="71a19-111">Уровень *—* это этап агрегации в иерархии.</span><span class="sxs-lookup"><span data-stu-id="71a19-111">A *level* is a step of aggregation in a hierarchy.</span></span> <span data-ttu-id="71a19-112">Для измерений с несколькими уровнями информации каждый уровень является уровнем.</span><span class="sxs-lookup"><span data-stu-id="71a19-112">For dimensions with multiple layers of information, each layer is a level.</span></span>

<span data-ttu-id="71a19-113">Элемент *—* это элемент данных в измерении.</span><span class="sxs-lookup"><span data-stu-id="71a19-113">A *member* is a data item in a dimension.</span></span> <span data-ttu-id="71a19-114">Как правило, вы создаете заголовок или описываете меру базы данных с помощью членов.</span><span class="sxs-lookup"><span data-stu-id="71a19-114">Typically, you create a caption or describe a measure of the database using members.</span></span>

<span data-ttu-id="71a19-115">Кубы представлены объектами [CubeDef](cubedef-object-ado-md.md) в ADO MD.</span><span class="sxs-lookup"><span data-stu-id="71a19-115">Cubes are represented by [CubeDef](cubedef-object-ado-md.md) objects in ADO MD.</span></span> <span data-ttu-id="71a19-116">Измерения, иерархии, уровни и члены также представлены соответствующими объектами ADO MD: [Dimension,](dimension-object-ado-md.md) [Hierarchy,](hierarchy-object-ado-md.md) [Level](level-object-ado-md.md)и [Member.](member-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="71a19-116">Dimensions, hierarchies, levels, and members are also represented by their corresponding ADO MD objects: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md).</span></span>

## <a name="dimensions"></a><span data-ttu-id="71a19-117">Dimensions</span><span class="sxs-lookup"><span data-stu-id="71a19-117">Dimensions</span></span>

<span data-ttu-id="71a19-118">Размеры куба зависят от бизнес-сущностями и типами данных, которые будут моделироваться в базе данных.</span><span class="sxs-lookup"><span data-stu-id="71a19-118">The dimensions of a cube depend on your business entities and types of data to be modeled in the database.</span></span> <span data-ttu-id="71a19-119">Как правило, каждое измерение является независимой точкой входа или механизмом для выбора данных.</span><span class="sxs-lookup"><span data-stu-id="71a19-119">Typically, each dimension is an independent entry point or mechanism for selecting data.</span></span>

<span data-ttu-id="71a19-120">Например, куб, содержащий данные о продажах, имеет следующие пять измерений: Salesperson, Geography, Time, Products, and Measures.</span><span class="sxs-lookup"><span data-stu-id="71a19-120">For example, a cube containing sales data has the following five dimensions: Salesperson, Geography, Time, Products, and Measures.</span></span> <span data-ttu-id="71a19-121">Измерение "Меры" содержит фактические значения данных о продажах, а другие измерения представляют способы классификации и группировки значений данных о продажах.</span><span class="sxs-lookup"><span data-stu-id="71a19-121">The Measures dimension contains actual sales data values, while the other dimensions represent ways to categorize and group the sales data values.</span></span>

<span data-ttu-id="71a19-122">Измерение "География" имеет следующий набор членов:</span><span class="sxs-lookup"><span data-stu-id="71a19-122">The Geography dimension has the following set of members:</span></span>

```text
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a><span data-ttu-id="71a19-123">Hierarchies</span><span class="sxs-lookup"><span data-stu-id="71a19-123">Hierarchies</span></span>

<span data-ttu-id="71a19-124">Иерархии определяют способы,которыми можно "свернуть" или сгруппить уровни измерения.</span><span class="sxs-lookup"><span data-stu-id="71a19-124">Hierarchies define the ways in which the levels of a dimension can be "rolled up" or grouped.</span></span> <span data-ttu-id="71a19-125">Измерение может иметь несколько иерархий.</span><span class="sxs-lookup"><span data-stu-id="71a19-125">A dimension can have more than one hierarchy.</span></span>

## <a name="levels"></a><span data-ttu-id="71a19-126">Levels</span><span class="sxs-lookup"><span data-stu-id="71a19-126">Levels</span></span>

<span data-ttu-id="71a19-127">В примере измерения "География", изображенном на предыдущем рисунке, каждое поле представляет уровень в иерархии.</span><span class="sxs-lookup"><span data-stu-id="71a19-127">In the example Geography dimension pictured in the previous figure, each box represents a level in the hierarchy.</span></span>

<span data-ttu-id="71a19-128">Каждый уровень имеет набор членов, как поется ниже.</span><span class="sxs-lookup"><span data-stu-id="71a19-128">Each level has a set of members, as follows:</span></span>

  - <span data-ttu-id="71a19-129">The World = {All}</span><span class="sxs-lookup"><span data-stu-id="71a19-129">The World = {All}</span></span>

  - <span data-ttu-id="71a19-130">Континенты = {Северная Америка, Европа}</span><span class="sxs-lookup"><span data-stu-id="71a19-130">Continents = {North America, Europe}</span></span>

  - <span data-ttu-id="71a19-131">Страны = {Канада, США, Соединенное Королевство, Германия}</span><span class="sxs-lookup"><span data-stu-id="71a19-131">Countries = {Canada, USA, UK, Germany}</span></span>

  - <span data-ttu-id="71a19-132">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span><span class="sxs-lookup"><span data-stu-id="71a19-132">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span></span>

  - <span data-ttu-id="71a19-133">Города = {Ottawa, Vancouver, Vancouver, Vancouver, Seattle, Boise, Los Seattle Seattle, Los Seattle, Shreveport, Meve, Meve, Los, New York, London, Dover, Seattleh, Cardiff, Pembroke, Losfast, London, Hamburg, Hamburg, Stuttgart}</span><span class="sxs-lookup"><span data-stu-id="71a19-133">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}</span></span>

## <a name="members"></a><span data-ttu-id="71a19-134">"Участники"</span><span class="sxs-lookup"><span data-stu-id="71a19-134">Members</span></span>

<span data-ttu-id="71a19-135">Члены на конечном уровне иерархии не имеют потомка, а члены на корневом уровне не имеют родительских.</span><span class="sxs-lookup"><span data-stu-id="71a19-135">Members at the leaf level of a hierarchy have no children, and members at the root level have no parent.</span></span> <span data-ttu-id="71a19-136">Все остальные члены имеют по крайней мере один родительский и по крайней мере один потомок.</span><span class="sxs-lookup"><span data-stu-id="71a19-136">All other members have at least one parent and at least one child.</span></span> <span data-ttu-id="71a19-137">Например, частичный обход дерева иерархии в измерении "География" дает следующие родительские и родительские отношения:</span><span class="sxs-lookup"><span data-stu-id="71a19-137">For example, a partial traversal of the hierarchy tree in the Geography dimension yields the following parent-child relationships:</span></span>

- <span data-ttu-id="71a19-138">{All} (родительский) {Europe, North America}</span><span class="sxs-lookup"><span data-stu-id="71a19-138">{All} (parent of) {Europe, North America}</span></span>
- <span data-ttu-id="71a19-139">{Северная Америка} (родительский) {Канада, США}</span><span class="sxs-lookup"><span data-stu-id="71a19-139">{North America} (parent of) {Canada, USA}</span></span>
- <span data-ttu-id="71a19-140">{USA} (родительский) {USA-NE, USA-NW, USA-SE, USA-SW}</span><span class="sxs-lookup"><span data-stu-id="71a19-140">{USA} (parent of) {USA-NE, USA-NW, USA-SE, USA-SW}</span></span>
- <span data-ttu-id="71a19-141">{USA-NW} (родительский) {Boise, Seattle}</span><span class="sxs-lookup"><span data-stu-id="71a19-141">{USA-NW} (parent of) {Boise, Seattle}</span></span>

<span data-ttu-id="71a19-142">Члены могут быть объединены в одну или несколько иерархий на измерение.</span><span class="sxs-lookup"><span data-stu-id="71a19-142">Members can be consolidated along one or more hierarchies per dimension.</span></span>

<span data-ttu-id="71a19-143">В этом примере также иллюстрируется другая характеристика: некоторые члены уровня недели иерархии Year-Week не отображаются ни на одном уровне иерархии Year-Quarter иерархии.</span><span class="sxs-lookup"><span data-stu-id="71a19-143">This example also illustrates another characteristic: some members of the Week level of the Year-Week hierarchy do not appear in any level of the Year-Quarter hierarchy.</span></span> <span data-ttu-id="71a19-144">Таким образом, иерархия не должна включать все члены измерения.</span><span class="sxs-lookup"><span data-stu-id="71a19-144">Thus, a hierarchy need not include all members of a dimension.</span></span>

## <a name="understanding-multidimensional-schemas"></a><span data-ttu-id="71a19-145">Understanding Multidimensional Schemas</span><span class="sxs-lookup"><span data-stu-id="71a19-145">Understanding Multidimensional Schemas</span></span>

<span data-ttu-id="71a19-146">Центральный объект метаданных в ADO MD — это *куб,* который состоит из структурированного набора связанных измерений, иерархий, уровней и членов.</span><span class="sxs-lookup"><span data-stu-id="71a19-146">The central metadata object in ADO MD is the *cube*, which consists of a structured set of related dimensions, hierarchies, levels, and members.</span></span>

<span data-ttu-id="71a19-147">Измерение *—* это независимая категория данных из многомерной базы данных, производная от бизнес-сущностями.</span><span class="sxs-lookup"><span data-stu-id="71a19-147">A *dimension* is an independent category of data from your multidimensional database, derived from your business entities.</span></span> <span data-ttu-id="71a19-148">Измерение обычно содержит элементы, используемые в качестве критериев запроса для мер базы данных.</span><span class="sxs-lookup"><span data-stu-id="71a19-148">A dimension typically contains items to be used as query criteria for the measures of the database.</span></span>

<span data-ttu-id="71a19-149">Иерархия *—* это путь агрегации измерения.</span><span class="sxs-lookup"><span data-stu-id="71a19-149">A *hierarchy* is a path of aggregation of a dimension.</span></span> <span data-ttu-id="71a19-150">Измерение может иметь несколько уровней детализации с родительскими и родительскими отношениями.</span><span class="sxs-lookup"><span data-stu-id="71a19-150">A dimension may have multiple levels of granularity, which have parent-child relationships.</span></span> <span data-ttu-id="71a19-151">Иерархия определяет, как эти уровни связаны.</span><span class="sxs-lookup"><span data-stu-id="71a19-151">A hierarchy defines how these levels are related.</span></span>

<span data-ttu-id="71a19-152">Уровень *—* это этап агрегации в иерархии.</span><span class="sxs-lookup"><span data-stu-id="71a19-152">A *level* is a step of aggregation in a hierarchy.</span></span> <span data-ttu-id="71a19-153">Для измерений с несколькими уровнями информации каждый уровень является уровнем.</span><span class="sxs-lookup"><span data-stu-id="71a19-153">For dimensions with multiple layers of information, each layer is a level.</span></span>

<span data-ttu-id="71a19-154">Элемент *—* это элемент данных в измерении.</span><span class="sxs-lookup"><span data-stu-id="71a19-154">A *member* is a data item in a dimension.</span></span> <span data-ttu-id="71a19-155">Как правило, вы создаете заголовок или описываете меру базы данных с помощью членов.</span><span class="sxs-lookup"><span data-stu-id="71a19-155">Typically, you create a caption or describe a measure of the database using members.</span></span>

<span data-ttu-id="71a19-156">Кубы представлены объектами [CubeDef](cubedef-object-ado-md.md) в ADO MD.</span><span class="sxs-lookup"><span data-stu-id="71a19-156">Cubes are represented by [CubeDef](cubedef-object-ado-md.md) objects in ADO MD.</span></span> <span data-ttu-id="71a19-157">Измерения, иерархии, уровни и члены также представлены соответствующими объектами ADO MD: [Dimension,](dimension-object-ado-md.md) [Hierarchy,](hierarchy-object-ado-md.md) [Level](level-object-ado-md.md)и [Member.](member-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="71a19-157">Dimensions, hierarchies, levels, and members are also represented by their corresponding ADO MD objects: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md).</span></span>

## <a name="dimensions"></a><span data-ttu-id="71a19-158">Dimensions</span><span class="sxs-lookup"><span data-stu-id="71a19-158">Dimensions</span></span>

<span data-ttu-id="71a19-159">Размеры куба зависят от бизнес-сущностями и типами данных, которые будут моделироваться в базе данных.</span><span class="sxs-lookup"><span data-stu-id="71a19-159">The dimensions of a cube depend on your business entities and types of data to be modeled in the database.</span></span> <span data-ttu-id="71a19-160">Как правило, каждое измерение является независимой точкой входа или механизмом для выбора данных.</span><span class="sxs-lookup"><span data-stu-id="71a19-160">Typically, each dimension is an independent entry point or mechanism for selecting data.</span></span>

<span data-ttu-id="71a19-161">Например, куб, содержащий данные о продажах, имеет следующие пять измерений: Salesperson, Geography, Time, Products, and Measures.</span><span class="sxs-lookup"><span data-stu-id="71a19-161">For example, a cube containing sales data has the following five dimensions: Salesperson, Geography, Time, Products, and Measures.</span></span> <span data-ttu-id="71a19-162">Измерение "Меры" содержит фактические значения данных о продажах, а другие измерения представляют способы классификации и группировки значений данных о продажах.</span><span class="sxs-lookup"><span data-stu-id="71a19-162">The Measures dimension contains actual sales data values, while the other dimensions represent ways to categorize and group the sales data values.</span></span>

<span data-ttu-id="71a19-163">Измерение "География" имеет следующий набор членов:</span><span class="sxs-lookup"><span data-stu-id="71a19-163">The Geography dimension has the following set of members:</span></span>

```text 
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a><span data-ttu-id="71a19-164">Hierarchies</span><span class="sxs-lookup"><span data-stu-id="71a19-164">Hierarchies</span></span>

<span data-ttu-id="71a19-165">Иерархии определяют способы,которыми можно "свернуть" или сгруппить уровни измерения.</span><span class="sxs-lookup"><span data-stu-id="71a19-165">Hierarchies define the ways in which the levels of a dimension can be "rolled up" or grouped.</span></span> <span data-ttu-id="71a19-166">Измерение может иметь несколько иерархий.</span><span class="sxs-lookup"><span data-stu-id="71a19-166">A dimension can have more than one hierarchy.</span></span>

## <a name="levels"></a><span data-ttu-id="71a19-167">Levels</span><span class="sxs-lookup"><span data-stu-id="71a19-167">Levels</span></span>

<span data-ttu-id="71a19-168">В примере измерения "География", изображенном на предыдущем рисунке, каждое поле представляет уровень в иерархии.</span><span class="sxs-lookup"><span data-stu-id="71a19-168">In the example Geography dimension pictured in the previous figure, each box represents a level in the hierarchy.</span></span>

<span data-ttu-id="71a19-169">Каждый уровень имеет набор членов, как поется ниже.</span><span class="sxs-lookup"><span data-stu-id="71a19-169">Each level has a set of members, as follows:</span></span>

- <span data-ttu-id="71a19-170">The World = {All}</span><span class="sxs-lookup"><span data-stu-id="71a19-170">The World = {All}</span></span>

- <span data-ttu-id="71a19-171">Континенты = {Северная Америка, Европа}</span><span class="sxs-lookup"><span data-stu-id="71a19-171">Continents = {North America, Europe}</span></span>

- <span data-ttu-id="71a19-172">Страны = {Канада, США, Соединенное Королевство, Германия}</span><span class="sxs-lookup"><span data-stu-id="71a19-172">Countries = {Canada, USA, UK, Germany}</span></span>

- <span data-ttu-id="71a19-173">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span><span class="sxs-lookup"><span data-stu-id="71a19-173">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span></span>

- <span data-ttu-id="71a19-174">Города = {Ottawa, Vancouver, Vancouver, Vancouver, Seattle, Boise, Los Seattle Seattle, Los Seattle, Shreveport, Meve, Meve, Los, New York, London, Dover, Seattleh, Cardiff, Pembroke, Losfast, London, Hamburg, Hamburg, Stuttgart}</span><span class="sxs-lookup"><span data-stu-id="71a19-174">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}</span></span>

## <a name="members"></a><span data-ttu-id="71a19-175">"Участники"</span><span class="sxs-lookup"><span data-stu-id="71a19-175">Members</span></span>

<span data-ttu-id="71a19-176">Члены на конечном уровне иерархии не имеют потомка, а члены на корневом уровне не имеют родительских.</span><span class="sxs-lookup"><span data-stu-id="71a19-176">Members at the leaf level of a hierarchy have no children, and members at the root level have no parent.</span></span> <span data-ttu-id="71a19-177">Все остальные члены имеют по крайней мере один родительский и по крайней мере один потомок.</span><span class="sxs-lookup"><span data-stu-id="71a19-177">All other members have at least one parent and at least one child.</span></span> <span data-ttu-id="71a19-178">Например, частичный обход дерева иерархии в измерении "География" дает следующие родительские и родительские отношения:</span><span class="sxs-lookup"><span data-stu-id="71a19-178">For example, a partial traversal of the hierarchy tree in the Geography dimension yields the following parent-child relationships:</span></span>

- <span data-ttu-id="71a19-179">{All} (родительский) {Europe, North America}</span><span class="sxs-lookup"><span data-stu-id="71a19-179">{All} (parent of) {Europe, North America}</span></span>

- <span data-ttu-id="71a19-180">{Северная Америка} (родительский) {Канада, США}</span><span class="sxs-lookup"><span data-stu-id="71a19-180">{North America} (parent of) {Canada, USA}</span></span>

- <span data-ttu-id="71a19-181">{USA} (родительский) {USA-NE, USA-NW, USA-SE, USA-SW}</span><span class="sxs-lookup"><span data-stu-id="71a19-181">{USA} (parent of) {USA-NE, USA-NW, USA-SE, USA-SW}</span></span>

- <span data-ttu-id="71a19-182">{USA-NW} (родительский) {Boise, Seattle}</span><span class="sxs-lookup"><span data-stu-id="71a19-182">{USA-NW} (parent of) {Boise, Seattle}</span></span>

<span data-ttu-id="71a19-183">Члены могут быть объединены в одну или несколько иерархий на измерение.</span><span class="sxs-lookup"><span data-stu-id="71a19-183">Members can be consolidated along one or more hierarchies per dimension.</span></span>

<span data-ttu-id="71a19-184">В этом примере также иллюстрируется другая характеристика: некоторые члены уровня недели иерархии Year-Week не отображаются ни на одном уровне иерархии Year-Quarter иерархии.</span><span class="sxs-lookup"><span data-stu-id="71a19-184">This example also illustrates another characteristic: some members of the Week level of the Year-Week hierarchy do not appear in any level of the Year-Quarter hierarchy.</span></span> <span data-ttu-id="71a19-185">Таким образом, иерархия не должна включать все члены измерения.</span><span class="sxs-lookup"><span data-stu-id="71a19-185">Thus, a hierarchy need not include all members of a dimension.</span></span>

