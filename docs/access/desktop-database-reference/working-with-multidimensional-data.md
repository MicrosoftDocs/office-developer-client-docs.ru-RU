---
title: Работа с многомерных данных
TOCTitle: Working with multidimensional data
ms:assetid: a0c9ac73-04da-cfdd-8787-15c8a53ff819
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249740(v=office.15)
ms:contentKeyID: 48546717
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1fc86aa61b9dda9db2246b7b5720eed31a595ea0
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998695"
---
# <a name="working-with-multidimensional-data"></a><span data-ttu-id="d0e2b-102">Работа с многомерных данных</span><span class="sxs-lookup"><span data-stu-id="d0e2b-102">Working with multidimensional data</span></span>

<span data-ttu-id="d0e2b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d0e2b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d0e2b-104">*Набор ячеек* производится в результате запроса на многомерные данные.</span><span class="sxs-lookup"><span data-stu-id="d0e2b-104">A *cellset* is the result of a query on multidimensional data.</span></span> <span data-ttu-id="d0e2b-105">Он состоит из коллекции осей, обычно не более четырех осей и обычно только два или три.</span><span class="sxs-lookup"><span data-stu-id="d0e2b-105">It consists of a collection of axes, usually no more than four axes and typically only two or three.</span></span> <span data-ttu-id="d0e2b-106">*Ось* — это коллекцию элементов из одного или нескольких измерений, который используется для поиска или фильтрации определенных значений в кубе.</span><span class="sxs-lookup"><span data-stu-id="d0e2b-106">An *axis* is a collection of members from one or more dimensions, which is used to locate or filter specific values in a cube.</span></span>

<span data-ttu-id="d0e2b-107">*Положение* — точка оси.</span><span class="sxs-lookup"><span data-stu-id="d0e2b-107">A *position* is a point along an axis.</span></span> <span data-ttu-id="d0e2b-108">Для оси, состоящий из одного измерения эти положения могут подмножества элементов измерения.</span><span class="sxs-lookup"><span data-stu-id="d0e2b-108">For an axis consisting of a single dimension, these positions are a subset of the dimension members.</span></span> <span data-ttu-id="d0e2b-109">Если оси состоит из нескольких измерений, каждом положении является составной лицо, которое состоит из частей *n* , где *n* — число измерений, ориентированные на этой оси.</span><span class="sxs-lookup"><span data-stu-id="d0e2b-109">If an axis consists of more than one dimension, then each position is a compound entity, which has *n* parts where *n* is the number of dimensions oriented along that axis.</span></span> <span data-ttu-id="d0e2b-110">Каждая часть положение является участником из одного целостные измерения.</span><span class="sxs-lookup"><span data-stu-id="d0e2b-110">Each part of the position is a member from one constituent dimension.</span></span>

<span data-ttu-id="d0e2b-111">Например измерений Geography и продукта из куба, содержащего данные о продажах располагается по оси набора ячеек, положение этой оси могут содержать элементы «США» и «Computers».</span><span class="sxs-lookup"><span data-stu-id="d0e2b-111">For example, if the Geography and Product dimensions from a cube containing sales data are oriented along the x-axis of a cellset, a position along this axis may contain the members "USA" and "Computers."</span></span> <span data-ttu-id="d0e2b-112">В этом примере определение положение по оси требуется, что элементы каждого измерения ориентированного на оси.</span><span class="sxs-lookup"><span data-stu-id="d0e2b-112">In this example, determining a position along the x-axis requires that members from each dimension are oriented along the axis.</span></span>

<span data-ttu-id="d0e2b-113">*Ячейка* — это объект, размещенный на пересечении ось координат.</span><span class="sxs-lookup"><span data-stu-id="d0e2b-113">A *cell* is an object positioned at the intersection of axis coordinates.</span></span> <span data-ttu-id="d0e2b-114">Каждой ячейки имеет несколько элементов данных, связанных с ним, включая сами данные, форматированные строки (отображаемом виде данные ячеек) и порядковый номер ячейки.</span><span class="sxs-lookup"><span data-stu-id="d0e2b-114">Each cell has multiple pieces of information associated with it, including the data itself, a formatted string (the displayable form of cell data), and the cell ordinal value.</span></span> <span data-ttu-id="d0e2b-115">(Каждой ячейки является значением уникальный порядковый номер в наборе ячеек.</span><span class="sxs-lookup"><span data-stu-id="d0e2b-115">(Each cell is a unique ordinal value in the cellset.</span></span> <span data-ttu-id="d0e2b-116">Порядковый номер первой ячейки в наборе ячеек равно нулю, а самые левые ячейки во второй строке ячеек с восемь столбцов порядковый номер восьми.)</span><span class="sxs-lookup"><span data-stu-id="d0e2b-116">The ordinal value of the first cell in the cellset is zero, while the leftmost cell in the second row of a cellset with eight columns would have an ordinal value of eight.)</span></span>

<span data-ttu-id="d0e2b-117">Например куб имеет следующие шесть измерений (Обратите внимание, что эта схема куба незначительно отличается от пример, заданный в [Обзор многомерные схемы и данных](overview-of-multidimensional-schemas-and-data.md)):</span><span class="sxs-lookup"><span data-stu-id="d0e2b-117">For example, a cube has the following six dimensions (note that this cube schema differs slightly from the example given in [Overview of Multidimensional Schemas and Data](overview-of-multidimensional-schemas-and-data.md)):</span></span>

- <span data-ttu-id="d0e2b-118">Менеджер</span><span class="sxs-lookup"><span data-stu-id="d0e2b-118">Salesperson</span></span>
- <span data-ttu-id="d0e2b-119">География (естественной иерархии) — разных странах, странах, состояния и т. п.</span><span class="sxs-lookup"><span data-stu-id="d0e2b-119">Geography (natural hierarchy) — Continents, Countries, States, and so on</span></span>
- <span data-ttu-id="d0e2b-120">Кварталов, Кварталов, месяцев, дней</span><span class="sxs-lookup"><span data-stu-id="d0e2b-120">Quarters — Quarters, Months, Days</span></span>
- <span data-ttu-id="d0e2b-121">Лет</span><span class="sxs-lookup"><span data-stu-id="d0e2b-121">Years</span></span>
- <span data-ttu-id="d0e2b-122">Меры — Продажи, PercentChange, BudgetedSales</span><span class="sxs-lookup"><span data-stu-id="d0e2b-122">Measures — Sales, PercentChange, BudgetedSales</span></span>
- <span data-ttu-id="d0e2b-123">Продукты</span><span class="sxs-lookup"><span data-stu-id="d0e2b-123">Products</span></span>

> [!NOTE]
> <span data-ttu-id="d0e2b-124">Значений ячеек в примере можно рассматривать как упорядоченный пары определенного положения ось, где первая цифра представляет секунды положение оси y и должности оси x.</span><span class="sxs-lookup"><span data-stu-id="d0e2b-124">The cell values in the example can be viewed as ordered pairs of axis position ordinals where the first digit represents the x-axis position and the second digit the y-axis position.</span></span>

<span data-ttu-id="d0e2b-125">Характеристики этот набор ячеек, следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d0e2b-125">The characteristics of this cellset are as follows:</span></span>

- <span data-ttu-id="d0e2b-126">Ось измерениями: кварталов, менеджер, Geography</span><span class="sxs-lookup"><span data-stu-id="d0e2b-126">Axis dimensions: Quarters, Salesperson, Geography</span></span>

- <span data-ttu-id="d0e2b-127">Фильтрация измерениями: меры, годы, продуктов</span><span class="sxs-lookup"><span data-stu-id="d0e2b-127">Filter dimensions: Measures, Years, Products</span></span>

- <span data-ttu-id="d0e2b-128">Две оси: СТОЛБЦОВ (x или оси 0) и СТРОК (y или ось 1)</span><span class="sxs-lookup"><span data-stu-id="d0e2b-128">Two axes: COLUMN (x, or Axis 0) and ROW (y, or Axis 1)</span></span>

- <span data-ttu-id="d0e2b-129">ось x: два вложенных измерений, Продавец и Geography</span><span class="sxs-lookup"><span data-stu-id="d0e2b-129">x-axis: two nested dimensions, Salesperson and Geography</span></span>

- <span data-ttu-id="d0e2b-130">ось y: кварталов измерения</span><span class="sxs-lookup"><span data-stu-id="d0e2b-130">y-axis: Quarters dimension</span></span>

<span data-ttu-id="d0e2b-131">Ось x имеет два вложенных измерения: продавца и География.</span><span class="sxs-lookup"><span data-stu-id="d0e2b-131">The x-axis has two nested dimensions: Salesperson and Geography.</span></span> <span data-ttu-id="d0e2b-132">Из расположения, выбираются элементы четыре: Сиэтл, может, Южная США и Японии.</span><span class="sxs-lookup"><span data-stu-id="d0e2b-132">From Geography, four members are selected: Seattle, Boston, USA-South, and Japan.</span></span> <span data-ttu-id="d0e2b-133">Два элемента, выбранные продавца: любимая и Нэшем.</span><span class="sxs-lookup"><span data-stu-id="d0e2b-133">Two members are selected from Salesperson: Valentine and Nash.</span></span> <span data-ttu-id="d0e2b-134">Это дает восемь положения на этой оси (8 = 4\*2).</span><span class="sxs-lookup"><span data-stu-id="d0e2b-134">This yields a total of eight positions on this axis (8 = 4\*2).</span></span>

<span data-ttu-id="d0e2b-135">Каждый координата представлен как положение с двумя участниками — одно из измерений менеджера по продажам и другой из измерения География:</span><span class="sxs-lookup"><span data-stu-id="d0e2b-135">Each coordinate is represented as a position with two members — one from the Salesperson dimension and another from the Geography dimension:</span></span>

```vb 
 
(Valentine, Seattle), (Valentine, Boston), (Valentine, USA_North), 
(Valentine, Japan), (Nash, Seattle), (Nash, Boston), (Nash, USA_North), 
(Nash, Japan) 
```

<span data-ttu-id="d0e2b-136">Ось y имеет только одно измерение, содержащее следующие восемь положения:</span><span class="sxs-lookup"><span data-stu-id="d0e2b-136">The y-axis has only one dimension, containing the following eight positions:</span></span>

```vb 
 
Jan, Feb, Mar, Qtr2, Qtr3, Oct, Nov, Dec 
```

<span data-ttu-id="d0e2b-137">Наборов ячеек, ячеек, осей и положения все представлены в ADO MD с соответствующими объектами: [ячеек](cellset-object-ado-md.md), [ячейки](cell-object-ado-md.md), [ось](axis-object-ado-md.md)и [положение](position-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d0e2b-137">Cellsets, cells, axes, and positions are all represented in ADO MD by corresponding objects: [Cellset](cellset-object-ado-md.md), [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md), and [Position](position-object-ado-md.md).</span></span>

