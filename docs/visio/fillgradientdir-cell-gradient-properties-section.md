---
title: Ячейка FillGradientDir (градиента Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: Определяет направление градиентной заливки. Градиент линейно, Радиальное, прямоугольный, или выполните путь.
ms.openlocfilehash: 9b4226892e70fcffe7a78d109bd852e6d4f93838
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813753"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a><span data-ttu-id="419a4-104">Ячейка FillGradientDir (градиента Properties Section)</span><span class="sxs-lookup"><span data-stu-id="419a4-104">FillGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="419a4-105">Определяет направление градиентной заливки.</span><span class="sxs-lookup"><span data-stu-id="419a4-105">Determines the direction of the fill gradient.</span></span> <span data-ttu-id="419a4-106">Градиент линейно, Радиальное, прямоугольный, или выполните путь.</span><span class="sxs-lookup"><span data-stu-id="419a4-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="419a4-107">Линейный градиент — это единственный градиент, который принимает значения дополнительных угол (в зависимости от **FillGradientDir** ячейки).</span><span class="sxs-lookup"><span data-stu-id="419a4-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **FillGradientDir** cell).</span></span> <span data-ttu-id="419a4-108">Все другие градиента инструкции по панелям предварительно перечисления.</span><span class="sxs-lookup"><span data-stu-id="419a4-108">All other gradient directions have preset enumerations.</span></span> 
  
****

|<span data-ttu-id="419a4-109">**Значение**</span><span class="sxs-lookup"><span data-stu-id="419a4-109">**Value**</span></span>|<span data-ttu-id="419a4-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="419a4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="419a4-111">0</span><span class="sxs-lookup"><span data-stu-id="419a4-111">0</span></span>  <br/> |<span data-ttu-id="419a4-112">Линейный градиент.</span><span class="sxs-lookup"><span data-stu-id="419a4-112">Linear gradient.</span></span> <span data-ttu-id="419a4-113">Ячейка **FillGradientAngle** определяет направление градиента.</span><span class="sxs-lookup"><span data-stu-id="419a4-113">The **FillGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="419a4-114">1-7</span><span class="sxs-lookup"><span data-stu-id="419a4-114">1-7</span></span>  <br/> |<span data-ttu-id="419a4-115">Радиальное градиентом.</span><span class="sxs-lookup"><span data-stu-id="419a4-115">Radial gradients.</span></span> <span data-ttu-id="419a4-116">Градиента расширяет возможности outwards в круг из центральной точки.</span><span class="sxs-lookup"><span data-stu-id="419a4-116">The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="419a4-117">8-12</span><span class="sxs-lookup"><span data-stu-id="419a4-117">8-12</span></span>  <br/> |<span data-ttu-id="419a4-118">Прямоугольный градиентом.</span><span class="sxs-lookup"><span data-stu-id="419a4-118">Rectangular gradients.</span></span> <span data-ttu-id="419a4-119">Расширяет возможности градиента направления строке с происхождения с появления прямоугольной формы.</span><span class="sxs-lookup"><span data-stu-id="419a4-119">The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="419a4-120">13</span><span class="sxs-lookup"><span data-stu-id="419a4-120">13</span></span>  <br/> |<span data-ttu-id="419a4-121">Градиентные путь.</span><span class="sxs-lookup"><span data-stu-id="419a4-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="419a4-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="419a4-122">Remarks</span></span>

<span data-ttu-id="419a4-123">Для получения ссылки на ячейки **FillGradientDir** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="419a4-123">To get a reference to the **FillGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="419a4-124">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="419a4-124">Cell name:</span></span>  <br/> | <span data-ttu-id="419a4-125">FillGradientDir</span><span class="sxs-lookup"><span data-stu-id="419a4-125">FillGradientDir</span></span>  <br/> |
   
<span data-ttu-id="419a4-126">Для получения ссылки на ячейки **FillGradientDir** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="419a4-126">To get a reference to the **FillGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="419a4-127">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="419a4-127">Section index:</span></span>  <br/> |<span data-ttu-id="419a4-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="419a4-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="419a4-129">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="419a4-129">Row index:</span></span>  <br/> |<span data-ttu-id="419a4-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="419a4-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="419a4-131">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="419a4-131">Cell index:</span></span>  <br/> |<span data-ttu-id="419a4-132">**visFillGradientDir**</span><span class="sxs-lookup"><span data-stu-id="419a4-132">**visFillGradientDir**</span></span> <br/> |
   

