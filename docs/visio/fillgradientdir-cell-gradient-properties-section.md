---
title: FillGradientDir Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: Определяет направление градиентной заливки. Градиент может быть линейным, радиальным, прямоугольным или следовать по пути.
ms.openlocfilehash: 53aad056c7fc1674e00e142fd72a10134103b390
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322465"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a><span data-ttu-id="1fa95-104">FillGradientDir Cell (Gradient Properties Section)</span><span class="sxs-lookup"><span data-stu-id="1fa95-104">FillGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="1fa95-105">Определяет направление градиентной заливки.</span><span class="sxs-lookup"><span data-stu-id="1fa95-105">Determines the direction of the fill gradient.</span></span> <span data-ttu-id="1fa95-106">Градиент может быть линейным, радиальным, прямоугольным или следовать по пути.</span><span class="sxs-lookup"><span data-stu-id="1fa95-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1fa95-107">Линейный градиент — это единственный градиент, принимающий дополнительное значение угла (как определено в ячейке **FillGradientDir** ).</span><span class="sxs-lookup"><span data-stu-id="1fa95-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **FillGradientDir** cell).</span></span> <span data-ttu-id="1fa95-108">Все остальные направления градиента имеют предварительно заданные перечисления.</span><span class="sxs-lookup"><span data-stu-id="1fa95-108">All other gradient directions have preset enumerations.</span></span> 
  
****

|<span data-ttu-id="1fa95-109">**Value**</span><span class="sxs-lookup"><span data-stu-id="1fa95-109">**Value**</span></span>|<span data-ttu-id="1fa95-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1fa95-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1fa95-111">нуль</span><span class="sxs-lookup"><span data-stu-id="1fa95-111">0</span></span>  <br/> |<span data-ttu-id="1fa95-112">Линейный градиент.</span><span class="sxs-lookup"><span data-stu-id="1fa95-112">Linear gradient.</span></span> <span data-ttu-id="1fa95-113">Ячейка **FillGradientAngle** определяет направление градиента.</span><span class="sxs-lookup"><span data-stu-id="1fa95-113">The **FillGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="1fa95-114">1-7</span><span class="sxs-lookup"><span data-stu-id="1fa95-114">1-7</span></span>  <br/> |<span data-ttu-id="1fa95-115">Радиальные градиенты.</span><span class="sxs-lookup"><span data-stu-id="1fa95-115">Radial gradients.</span></span> <span data-ttu-id="1fa95-116">Градиент расширяется по кругу от центральной точки.</span><span class="sxs-lookup"><span data-stu-id="1fa95-116">The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="1fa95-117">8-12</span><span class="sxs-lookup"><span data-stu-id="1fa95-117">8-12</span></span>  <br/> |<span data-ttu-id="1fa95-118">Прямоугольные градиенты.</span><span class="sxs-lookup"><span data-stu-id="1fa95-118">Rectangular gradients.</span></span> <span data-ttu-id="1fa95-119">Градиент распространяется в виде направленной линии из источника с выцветанием прямоугольной формы.</span><span class="sxs-lookup"><span data-stu-id="1fa95-119">The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="1fa95-120">13</span><span class="sxs-lookup"><span data-stu-id="1fa95-120">13</span></span>  <br/> |<span data-ttu-id="1fa95-121">Градиентный путь.</span><span class="sxs-lookup"><span data-stu-id="1fa95-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1fa95-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="1fa95-122">Remarks</span></span>

<span data-ttu-id="1fa95-123">Чтобы получить ссылку на ячейку **FillGradientDir** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="1fa95-123">To get a reference to the **FillGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1fa95-124">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="1fa95-124">Cell name:</span></span>  <br/> | <span data-ttu-id="1fa95-125">FillGradientDir</span><span class="sxs-lookup"><span data-stu-id="1fa95-125">FillGradientDir</span></span>  <br/> |
   
<span data-ttu-id="1fa95-126">Чтобы получить ссылку на ячейку **FillGradientDir** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="1fa95-126">To get a reference to the **FillGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1fa95-127">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="1fa95-127">Section index:</span></span>  <br/> |<span data-ttu-id="1fa95-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1fa95-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1fa95-129">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="1fa95-129">Row index:</span></span>  <br/> |<span data-ttu-id="1fa95-130">**Висровградиентпропертиес**</span><span class="sxs-lookup"><span data-stu-id="1fa95-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="1fa95-131">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="1fa95-131">Cell index:</span></span>  <br/> |<span data-ttu-id="1fa95-132">**Висфиллградиентдир**</span><span class="sxs-lookup"><span data-stu-id="1fa95-132">**visFillGradientDir**</span></span> <br/> |
   

