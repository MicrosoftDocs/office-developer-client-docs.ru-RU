---
title: Работа с многомерными данными
TOCTitle: Working with multidimensional data
ms:assetid: a0c9ac73-04da-cfdd-8787-15c8a53ff819
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249740(v=office.15)
ms:contentKeyID: 48546717
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 67b22219fdbbec8bf518b7be0fabd9a6adfbcf7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306043"
---
# <a name="working-with-multidimensional-data"></a><span data-ttu-id="12825-102">Работа с многомерными данными</span><span class="sxs-lookup"><span data-stu-id="12825-102">Working with multidimensional data</span></span>

<span data-ttu-id="12825-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="12825-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="12825-104">Набор *ячеек* — это результат запроса в многомерных данных.</span><span class="sxs-lookup"><span data-stu-id="12825-104">A *cellset* is the result of a query on multidimensional data.</span></span> <span data-ttu-id="12825-105">Он состоит из коллекции осей, обычно не более четырех осей и обычно двух или трех.</span><span class="sxs-lookup"><span data-stu-id="12825-105">It consists of a collection of axes, usually no more than four axes and typically only two or three.</span></span> <span data-ttu-id="12825-106">*Ось* — это коллекция элементов из одного или нескольких измерений, которая используется для обнаружения или фильтрации определенных значений в Кубе.</span><span class="sxs-lookup"><span data-stu-id="12825-106">An *axis* is a collection of members from one or more dimensions, which is used to locate or filter specific values in a cube.</span></span>

<span data-ttu-id="12825-107">*Положение* — это точка вдоль оси.</span><span class="sxs-lookup"><span data-stu-id="12825-107">A *position* is a point along an axis.</span></span> <span data-ttu-id="12825-108">Для оси, состоящей из одного измерения, эти положения являются подмножеством элементов измерения.</span><span class="sxs-lookup"><span data-stu-id="12825-108">For an axis consisting of a single dimension, these positions are a subset of the dimension members.</span></span> <span data-ttu-id="12825-109">Если ось состоит из нескольких измерений, то каждое положение представляет собой составную сущность, которая содержит *n* частей, где *n* — количество измерений, ориентированных по этой оси.</span><span class="sxs-lookup"><span data-stu-id="12825-109">If an axis consists of more than one dimension, then each position is a compound entity, which has *n* parts where *n* is the number of dimensions oriented along that axis.</span></span> <span data-ttu-id="12825-110">Каждая часть положения является элементом из одного составного измерения.</span><span class="sxs-lookup"><span data-stu-id="12825-110">Each part of the position is a member from one constituent dimension.</span></span>

<span data-ttu-id="12825-111">Например, если измерения Geography и Product из Куба, содержащего данные продаж, ориентированы вдоль оси x набора ячеек, положение на этой оси может содержать элементы "USA" и "Computers".</span><span class="sxs-lookup"><span data-stu-id="12825-111">For example, if the Geography and Product dimensions from a cube containing sales data are oriented along the x-axis of a cellset, a position along this axis may contain the members "USA" and "Computers."</span></span> <span data-ttu-id="12825-112">В этом примере определение положения по оси x требует, чтобы элементы из каждого измерения были ориентированы вдоль оси.</span><span class="sxs-lookup"><span data-stu-id="12825-112">In this example, determining a position along the x-axis requires that members from each dimension are oriented along the axis.</span></span>

<span data-ttu-id="12825-113">*Ячейка* — это объект, расположенный на пересечении координат оси.</span><span class="sxs-lookup"><span data-stu-id="12825-113">A *cell* is an object positioned at the intersection of axis coordinates.</span></span> <span data-ttu-id="12825-114">Каждая ячейка содержит несколько связанных с ней частей информации, в том числе собственно данные, форматированную строку (отображаемая форма данных ячейки) и порядковый номер ячейки.</span><span class="sxs-lookup"><span data-stu-id="12825-114">Each cell has multiple pieces of information associated with it, including the data itself, a formatted string (the displayable form of cell data), and the cell ordinal value.</span></span> <span data-ttu-id="12825-115">(Каждая ячейка — это уникальное порядковое значение в наборе ячеек.</span><span class="sxs-lookup"><span data-stu-id="12825-115">(Each cell is a unique ordinal value in the cellset.</span></span> <span data-ttu-id="12825-116">Порядковое значение первой ячейки в наборе ячеек равно нулю, а крайняя левая ячейка во второй строке набора ячеек с восемью столбцами будет иметь порядковое значение восемь.)</span><span class="sxs-lookup"><span data-stu-id="12825-116">The ordinal value of the first cell in the cellset is zero, while the leftmost cell in the second row of a cellset with eight columns would have an ordinal value of eight.)</span></span>

<span data-ttu-id="12825-117">Например, куб имеет следующие шесть измерений (Обратите внимание, что эта схема куба немного отличается от примера, приведенного в разделе [Обзор многомерных схем и данных](overview-of-multidimensional-schemas-and-data.md)):</span><span class="sxs-lookup"><span data-stu-id="12825-117">For example, a cube has the following six dimensions (note that this cube schema differs slightly from the example given in [Overview of Multidimensional Schemas and Data](overview-of-multidimensional-schemas-and-data.md)):</span></span>

- <span data-ttu-id="12825-118">Этому</span><span class="sxs-lookup"><span data-stu-id="12825-118">Salesperson</span></span>
- <span data-ttu-id="12825-119">Geography (естественная иерархия) — континенты, страны, Штаты и т. д.</span><span class="sxs-lookup"><span data-stu-id="12825-119">Geography (natural hierarchy) — Continents, Countries, States, and so on</span></span>
- <span data-ttu-id="12825-120">Кварталы — кварталы, месяцы, дни</span><span class="sxs-lookup"><span data-stu-id="12825-120">Quarters — Quarters, Months, Days</span></span>
- <span data-ttu-id="12825-121">(в годах)</span><span class="sxs-lookup"><span data-stu-id="12825-121">Years</span></span>
- <span data-ttu-id="12825-122">Меры — Sales, Перцентчанже, Буджетедсалес</span><span class="sxs-lookup"><span data-stu-id="12825-122">Measures — Sales, PercentChange, BudgetedSales</span></span>
- <span data-ttu-id="12825-123">Продукты</span><span class="sxs-lookup"><span data-stu-id="12825-123">Products</span></span>

> [!NOTE]
> <span data-ttu-id="12825-124">Значения ячеек в примере можно просматривать в виде упорядоченных пар порядков, где первая цифра представляет положение по оси x, а вторая цифра относительно оси y.</span><span class="sxs-lookup"><span data-stu-id="12825-124">The cell values in the example can be viewed as ordered pairs of axis position ordinals where the first digit represents the x-axis position and the second digit the y-axis position.</span></span>

<span data-ttu-id="12825-125">Ниже приведены характеристики этого набора ячеек.</span><span class="sxs-lookup"><span data-stu-id="12825-125">The characteristics of this cellset are as follows:</span></span>

- <span data-ttu-id="12825-126">Измерения оси: кварталы, продавец, география</span><span class="sxs-lookup"><span data-stu-id="12825-126">Axis dimensions: Quarters, Salesperson, Geography</span></span>

- <span data-ttu-id="12825-127">Измерения фильтра: меры, годы, продукты</span><span class="sxs-lookup"><span data-stu-id="12825-127">Filter dimensions: Measures, Years, Products</span></span>

- <span data-ttu-id="12825-128">Две оси: столбец (x, ось 0) и строка (y или ось 1)</span><span class="sxs-lookup"><span data-stu-id="12825-128">Two axes: COLUMN (x, or Axis 0) and ROW (y, or Axis 1)</span></span>

- <span data-ttu-id="12825-129">ось x: два вложенных измерения, продавец и география</span><span class="sxs-lookup"><span data-stu-id="12825-129">x-axis: two nested dimensions, Salesperson and Geography</span></span>

- <span data-ttu-id="12825-130">ось y: размерность в кварталах</span><span class="sxs-lookup"><span data-stu-id="12825-130">y-axis: Quarters dimension</span></span>

<span data-ttu-id="12825-131">Ось x имеет два вложенных измерения: SalesPerson и geography.</span><span class="sxs-lookup"><span data-stu-id="12825-131">The x-axis has two nested dimensions: Salesperson and Geography.</span></span> <span data-ttu-id="12825-132">Из географии выбрано четыре члена: Сиэтл, Бостон, USA-Южный и Япония.</span><span class="sxs-lookup"><span data-stu-id="12825-132">From Geography, four members are selected: Seattle, Boston, USA-South, and Japan.</span></span> <span data-ttu-id="12825-133">В SalesPerson выбраны два элемента: любимая и наш.</span><span class="sxs-lookup"><span data-stu-id="12825-133">Two members are selected from Salesperson: Valentine and Nash.</span></span> <span data-ttu-id="12825-134">В результате получается всего восемь позиций на этой оси (8 = 4\*2).</span><span class="sxs-lookup"><span data-stu-id="12825-134">This yields a total of eight positions on this axis (8 = 4\*2).</span></span>

<span data-ttu-id="12825-135">Каждая координата представляется в виде позиции с двумя элементами (один из измерения "продавец") и другой из измерения "География":</span><span class="sxs-lookup"><span data-stu-id="12825-135">Each coordinate is represented as a position with two members — one from the Salesperson dimension and another from the Geography dimension:</span></span>

```vb 
 
(Valentine, Seattle), (Valentine, Boston), (Valentine, USA_North), 
(Valentine, Japan), (Nash, Seattle), (Nash, Boston), (Nash, USA_North), 
(Nash, Japan) 
```

<span data-ttu-id="12825-136">Ось y имеет только одно измерение, содержащее следующие восемь позиций:</span><span class="sxs-lookup"><span data-stu-id="12825-136">The y-axis has only one dimension, containing the following eight positions:</span></span>

```vb 
 
Jan, Feb, Mar, Qtr2, Qtr3, Oct, Nov, Dec 
```

<span data-ttu-id="12825-137">Целлсетс, Cells, осей и положения представлены в ADO MD с помощью соответствующих объектов: набора [ячеек](cellset-object-ado-md.md), [ячейки](cell-object-ado-md.md), [оси](axis-object-ado-md.md)и [позиции](position-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="12825-137">Cellsets, cells, axes, and positions are all represented in ADO MD by corresponding objects: [Cellset](cellset-object-ado-md.md), [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md), and [Position](position-object-ado-md.md).</span></span>

