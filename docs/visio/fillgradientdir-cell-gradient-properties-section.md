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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406719"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a><span data-ttu-id="0e64d-104">FillGradientDir Cell (Gradient Properties Section)</span><span class="sxs-lookup"><span data-stu-id="0e64d-104">FillGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="0e64d-105">Определяет направление градиентной заливки.</span><span class="sxs-lookup"><span data-stu-id="0e64d-105">Determines the direction of the fill gradient.</span></span> <span data-ttu-id="0e64d-106">Градиент может быть линейным, радиальным, прямоугольным или следовать по пути.</span><span class="sxs-lookup"><span data-stu-id="0e64d-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0e64d-107">Линейный градиент — это единственный градиент, принимающий дополнительное значение угла (как определено в ячейке **FillGradientDir** ).</span><span class="sxs-lookup"><span data-stu-id="0e64d-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **FillGradientDir** cell).</span></span> <span data-ttu-id="0e64d-108">Все остальные направления градиента имеют предварительно заданные перечисления.</span><span class="sxs-lookup"><span data-stu-id="0e64d-108">All other gradient directions have preset enumerations.</span></span> 
  
****

|<span data-ttu-id="0e64d-109">**Значение**</span><span class="sxs-lookup"><span data-stu-id="0e64d-109">**Value**</span></span>|<span data-ttu-id="0e64d-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0e64d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0e64d-111">нуль</span><span class="sxs-lookup"><span data-stu-id="0e64d-111">0</span></span>  <br/> |<span data-ttu-id="0e64d-112">Линейный градиент.</span><span class="sxs-lookup"><span data-stu-id="0e64d-112">Linear gradient.</span></span> <span data-ttu-id="0e64d-113">Ячейка **FillGradientAngle** определяет направление градиента.</span><span class="sxs-lookup"><span data-stu-id="0e64d-113">The **FillGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="0e64d-114">1-7</span><span class="sxs-lookup"><span data-stu-id="0e64d-114">1-7</span></span>  <br/> |<span data-ttu-id="0e64d-115">Радиальные градиенты.</span><span class="sxs-lookup"><span data-stu-id="0e64d-115">Radial gradients.</span></span> <span data-ttu-id="0e64d-116">Градиент расширяется по кругу от центральной точки.</span><span class="sxs-lookup"><span data-stu-id="0e64d-116">The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="0e64d-117">8-12</span><span class="sxs-lookup"><span data-stu-id="0e64d-117">8-12</span></span>  <br/> |<span data-ttu-id="0e64d-118">Прямоугольные градиенты.</span><span class="sxs-lookup"><span data-stu-id="0e64d-118">Rectangular gradients.</span></span> <span data-ttu-id="0e64d-119">Градиент распространяется в виде направленной линии из источника с выцветанием прямоугольной формы.</span><span class="sxs-lookup"><span data-stu-id="0e64d-119">The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="0e64d-120">13 </span><span class="sxs-lookup"><span data-stu-id="0e64d-120">13</span></span>  <br/> |<span data-ttu-id="0e64d-121">Градиентный путь.</span><span class="sxs-lookup"><span data-stu-id="0e64d-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e64d-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="0e64d-122">Remarks</span></span>

<span data-ttu-id="0e64d-123">Чтобы получить ссылку на ячейку **FillGradientDir** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="0e64d-123">To get a reference to the **FillGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0e64d-124">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="0e64d-124">Cell name:</span></span>  <br/> | <span data-ttu-id="0e64d-125">FillGradientDir</span><span class="sxs-lookup"><span data-stu-id="0e64d-125">FillGradientDir</span></span>  <br/> |
   
<span data-ttu-id="0e64d-126">Чтобы получить ссылку на ячейку **FillGradientDir** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="0e64d-126">To get a reference to the **FillGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0e64d-127">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0e64d-127">Section index:</span></span>  <br/> |<span data-ttu-id="0e64d-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0e64d-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0e64d-129">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0e64d-129">Row index:</span></span>  <br/> |<span data-ttu-id="0e64d-130">**Висровградиентпропертиес**</span><span class="sxs-lookup"><span data-stu-id="0e64d-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="0e64d-131">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0e64d-131">Cell index:</span></span>  <br/> |<span data-ttu-id="0e64d-132">**Висфиллградиентдир**</span><span class="sxs-lookup"><span data-stu-id="0e64d-132">**visFillGradientDir**</span></span> <br/> |
   

