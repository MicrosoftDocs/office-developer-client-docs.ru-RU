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
# <a name="working-with-multidimensional-data"></a><span data-ttu-id="57257-102">Работа с многомерными данными</span><span class="sxs-lookup"><span data-stu-id="57257-102">Working with multidimensional data</span></span>

<span data-ttu-id="57257-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="57257-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="57257-104">Ячейки *—* это результат запроса многомерных данных.</span><span class="sxs-lookup"><span data-stu-id="57257-104">A *cellset* is the result of a query on multidimensional data.</span></span> <span data-ttu-id="57257-105">Он состоит из коллекции осей, обычно не более четырех осей и, как правило, только двух или трех.</span><span class="sxs-lookup"><span data-stu-id="57257-105">It consists of a collection of axes, usually no more than four axes and typically only two or three.</span></span> <span data-ttu-id="57257-106">*Ось* — это коллекция членов из одного или более измерений, которая используется для поиска или фильтрации определенных значений в кубе.</span><span class="sxs-lookup"><span data-stu-id="57257-106">An *axis* is a collection of members from one or more dimensions, which is used to locate or filter specific values in a cube.</span></span>

<span data-ttu-id="57257-107">Положение *—* это точка вдоль оси.</span><span class="sxs-lookup"><span data-stu-id="57257-107">A *position* is a point along an axis.</span></span> <span data-ttu-id="57257-108">Для оси, состоящей из одного измерения, эти позиции являются подмножество членов измерения.</span><span class="sxs-lookup"><span data-stu-id="57257-108">For an axis consisting of a single dimension, these positions are a subset of the dimension members.</span></span> <span data-ttu-id="57257-109">Если ось состоит из нескольких измерений, каждое положение является составной сущностью, которая имеет *n* частей, где *n* — это число измерений, ориентированных вдоль этой оси.</span><span class="sxs-lookup"><span data-stu-id="57257-109">If an axis consists of more than one dimension, then each position is a compound entity, which has *n* parts where *n* is the number of dimensions oriented along that axis.</span></span> <span data-ttu-id="57257-110">Каждая часть позиции является членом из одного составляющих измерения.</span><span class="sxs-lookup"><span data-stu-id="57257-110">Each part of the position is a member from one constituent dimension.</span></span>

<span data-ttu-id="57257-111">Например, если измерения "География" и "Продукт" куба, содержащего данные о продажах, ориентированы вдоль оси X ячеек, положение вдоль этой оси может содержать элементы "USA" и "Computers".</span><span class="sxs-lookup"><span data-stu-id="57257-111">For example, if the Geography and Product dimensions from a cube containing sales data are oriented along the x-axis of a cellset, a position along this axis may contain the members "USA" and "Computers."</span></span> <span data-ttu-id="57257-112">В этом примере определение положения вдоль оси x требует, чтобы члены из каждого измерения были ориентированы вдоль оси.</span><span class="sxs-lookup"><span data-stu-id="57257-112">In this example, determining a position along the x-axis requires that members from each dimension are oriented along the axis.</span></span>

<span data-ttu-id="57257-113">*Ячейка* — это объект, который находится на пересечении координат оси.</span><span class="sxs-lookup"><span data-stu-id="57257-113">A *cell* is an object positioned at the intersection of axis coordinates.</span></span> <span data-ttu-id="57257-114">Каждая ячейка имеет несколько элементов данных, связанных с ней, включая сами данные, форматированную строку (отображаемую форму данных ячейки) и порядковое значение ячейки.</span><span class="sxs-lookup"><span data-stu-id="57257-114">Each cell has multiple pieces of information associated with it, including the data itself, a formatted string (the displayable form of cell data), and the cell ordinal value.</span></span> <span data-ttu-id="57257-115">(Каждая ячейка — это уникальное порядковые значения в ячейках.</span><span class="sxs-lookup"><span data-stu-id="57257-115">(Each cell is a unique ordinal value in the cellset.</span></span> <span data-ttu-id="57257-116">Порядковые значения первой ячейки в ячейках — нуль, а самая левая ячейка во второй строке ячейки с восемью столбцами будет иметь порядковые значения 8.)</span><span class="sxs-lookup"><span data-stu-id="57257-116">The ordinal value of the first cell in the cellset is zero, while the leftmost cell in the second row of a cellset with eight columns would have an ordinal value of eight.)</span></span>

<span data-ttu-id="57257-117">Например, куб имеет следующие шесть измерений (обратите внимание, что эта схема куба немного отличается от примера, представленного в обзоре многомерных схем [и данных):](overview-of-multidimensional-schemas-and-data.md)</span><span class="sxs-lookup"><span data-stu-id="57257-117">For example, a cube has the following six dimensions (note that this cube schema differs slightly from the example given in [Overview of Multidimensional Schemas and Data](overview-of-multidimensional-schemas-and-data.md)):</span></span>

- <span data-ttu-id="57257-118">Salesperson</span><span class="sxs-lookup"><span data-stu-id="57257-118">Salesperson</span></span>
- <span data-ttu-id="57257-119">География (естественные иерархии) — континенты, страны, состояния и так далее</span><span class="sxs-lookup"><span data-stu-id="57257-119">Geography (natural hierarchy) — Continents, Countries, States, and so on</span></span>
- <span data-ttu-id="57257-120">Кварталы — кварталы, месяцы, дни</span><span class="sxs-lookup"><span data-stu-id="57257-120">Quarters — Quarters, Months, Days</span></span>
- <span data-ttu-id="57257-121">Годы</span><span class="sxs-lookup"><span data-stu-id="57257-121">Years</span></span>
- <span data-ttu-id="57257-122">Меры — продажи, PercentChange, BudgetedSales</span><span class="sxs-lookup"><span data-stu-id="57257-122">Measures — Sales, PercentChange, BudgetedSales</span></span>
- <span data-ttu-id="57257-123">Продукты</span><span class="sxs-lookup"><span data-stu-id="57257-123">Products</span></span>

> [!NOTE]
> <span data-ttu-id="57257-124">Значения ячеей в примере можно рассматривать как упорядоченные пары порядков положения оси, где первая цифра представляет положение оси X, а вторая — положение оси Y.</span><span class="sxs-lookup"><span data-stu-id="57257-124">The cell values in the example can be viewed as ordered pairs of axis position ordinals where the first digit represents the x-axis position and the second digit the y-axis position.</span></span>

<span data-ttu-id="57257-125">Характеристики этого ячеек:</span><span class="sxs-lookup"><span data-stu-id="57257-125">The characteristics of this cellset are as follows:</span></span>

- <span data-ttu-id="57257-126">Измерения оси: Кварталы, Salesperson, География</span><span class="sxs-lookup"><span data-stu-id="57257-126">Axis dimensions: Quarters, Salesperson, Geography</span></span>

- <span data-ttu-id="57257-127">Размеры фильтра: "Показатели", "Годы", "Продукты"</span><span class="sxs-lookup"><span data-stu-id="57257-127">Filter dimensions: Measures, Years, Products</span></span>

- <span data-ttu-id="57257-128">Две оси: COLUMN (x или Axis 0) и ROW (y или Axis 1)</span><span class="sxs-lookup"><span data-stu-id="57257-128">Two axes: COLUMN (x, or Axis 0) and ROW (y, or Axis 1)</span></span>

- <span data-ttu-id="57257-129">Ось x: два вложенных измерения: Salesperson и Geography</span><span class="sxs-lookup"><span data-stu-id="57257-129">x-axis: two nested dimensions, Salesperson and Geography</span></span>

- <span data-ttu-id="57257-130">Y-axis: измерение кварталов</span><span class="sxs-lookup"><span data-stu-id="57257-130">y-axis: Quarters dimension</span></span>

<span data-ttu-id="57257-131">Ось x имеет два вложенных измерения: Salesperson и Geography.</span><span class="sxs-lookup"><span data-stu-id="57257-131">The x-axis has two nested dimensions: Salesperson and Geography.</span></span> <span data-ttu-id="57257-132">В области "География" выбраны четыре члена: Сиэтл, Глоу, США-Южная и Япония.</span><span class="sxs-lookup"><span data-stu-id="57257-132">From Geography, four members are selected: Seattle, Boston, USA-South, and Japan.</span></span> <span data-ttu-id="57257-133">В salesperson выбраны два члена: "Иван" и "Вайс".</span><span class="sxs-lookup"><span data-stu-id="57257-133">Two members are selected from Salesperson: Valentine and Nash.</span></span> <span data-ttu-id="57257-134">Это дает в общей сложности восемь позиций на этой оси (8 = 4 \* 2).</span><span class="sxs-lookup"><span data-stu-id="57257-134">This yields a total of eight positions on this axis (8 = 4\*2).</span></span>

<span data-ttu-id="57257-135">Каждая координата представлена в качестве позиции с двумя членами : один из измерения Salesperson, а другой из измерения "География":</span><span class="sxs-lookup"><span data-stu-id="57257-135">Each coordinate is represented as a position with two members — one from the Salesperson dimension and another from the Geography dimension:</span></span>

```vb 
 
(Valentine, Seattle), (Valentine, Boston), (Valentine, USA_North), 
(Valentine, Japan), (Nash, Seattle), (Nash, Boston), (Nash, USA_North), 
(Nash, Japan) 
```

<span data-ttu-id="57257-136">Ось Y имеет только одно измерение, содержащее следующие восемь позиций:</span><span class="sxs-lookup"><span data-stu-id="57257-136">The y-axis has only one dimension, containing the following eight positions:</span></span>

```vb 
 
Jan, Feb, Mar, Qtr2, Qtr3, Oct, Nov, Dec 
```

<span data-ttu-id="57257-137">Ячейки, ячейки, оси и положения представлены в ADO MD соответствующими объектами: [Cellset,](cellset-object-ado-md.md) [Cell,](cell-object-ado-md.md) [Axis](axis-object-ado-md.md)и [Position.](position-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="57257-137">Cellsets, cells, axes, and positions are all represented in ADO MD by corresponding objects: [Cellset](cellset-object-ado-md.md), [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md), and [Position](position-object-ado-md.md).</span></span>

