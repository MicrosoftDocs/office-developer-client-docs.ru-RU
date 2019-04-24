---
title: LineGradientDir Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c603f9a5-f887-47ce-90bb-d41ec2d1a6a1
description: Определяет направление линии градиента. Градиент может быть линейным, радиальным, прямоугольным или следовать по пути.
ms.openlocfilehash: 05dcc6904a4e67d97c632dba44635936b1c14049
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350962"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a><span data-ttu-id="2efce-104">LineGradientDir Cell (Gradient Properties Section)</span><span class="sxs-lookup"><span data-stu-id="2efce-104">LineGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="2efce-105">Определяет направление линии градиента.</span><span class="sxs-lookup"><span data-stu-id="2efce-105">Determines the direction of the line gradient.</span></span> <span data-ttu-id="2efce-106">Градиент может быть линейным, радиальным, прямоугольным или следовать по пути.</span><span class="sxs-lookup"><span data-stu-id="2efce-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2efce-107">Линейный градиент — это единственный градиент, принимающий дополнительное значение угла (как определено в ячейке **LineGradientDir** ).</span><span class="sxs-lookup"><span data-stu-id="2efce-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **LineGradientDir** cell).</span></span> <span data-ttu-id="2efce-108">Все остальные направления градиента имеют предварительно заданные перечисления.</span><span class="sxs-lookup"><span data-stu-id="2efce-108">All other gradient directions have preset enumerations.</span></span> 
  
|<span data-ttu-id="2efce-109">**Value**</span><span class="sxs-lookup"><span data-stu-id="2efce-109">**Value**</span></span>|<span data-ttu-id="2efce-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2efce-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2efce-111">нуль</span><span class="sxs-lookup"><span data-stu-id="2efce-111">0</span></span>  <br/> |<span data-ttu-id="2efce-112">Линейный градиент.</span><span class="sxs-lookup"><span data-stu-id="2efce-112">Linear gradient.</span></span> <span data-ttu-id="2efce-113">Ячейка **LineGradientAngle** определяет направление градиента.</span><span class="sxs-lookup"><span data-stu-id="2efce-113">The **LineGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="2efce-114">1-7</span><span class="sxs-lookup"><span data-stu-id="2efce-114">1-7</span></span>  <br/> |<span data-ttu-id="2efce-115">Радиальные градиенты.</span><span class="sxs-lookup"><span data-stu-id="2efce-115">Radial gradients.</span></span> <span data-ttu-id="2efce-116">Градиент расширяется по кругу от центральной точки.</span><span class="sxs-lookup"><span data-stu-id="2efce-116">The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="2efce-117">8-12</span><span class="sxs-lookup"><span data-stu-id="2efce-117">8-12</span></span>  <br/> |<span data-ttu-id="2efce-118">Прямоугольные градиенты.</span><span class="sxs-lookup"><span data-stu-id="2efce-118">Rectangular gradients.</span></span> <span data-ttu-id="2efce-119">Градиент распространяется в виде направленной линии из источника с выцветанием прямоугольной формы.</span><span class="sxs-lookup"><span data-stu-id="2efce-119">The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="2efce-120">13</span><span class="sxs-lookup"><span data-stu-id="2efce-120">13</span></span>  <br/> |<span data-ttu-id="2efce-121">Градиентный путь.</span><span class="sxs-lookup"><span data-stu-id="2efce-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2efce-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="2efce-122">Remarks</span></span>

<span data-ttu-id="2efce-123">Чтобы получить ссылку на ячейку **LineGradientDir** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="2efce-123">To get a reference to the **LineGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2efce-124">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="2efce-124">Cell name:</span></span>  <br/> | <span data-ttu-id="2efce-125">LineGradientDir</span><span class="sxs-lookup"><span data-stu-id="2efce-125">LineGradientDir</span></span>  <br/> |
   
<span data-ttu-id="2efce-126">Чтобы получить ссылку на ячейку **LineGradientDir** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="2efce-126">To get a reference to the **LineGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2efce-127">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="2efce-127">Section index:</span></span>  <br/> |<span data-ttu-id="2efce-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2efce-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2efce-129">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="2efce-129">Row index:</span></span>  <br/> |<span data-ttu-id="2efce-130">**Висровградиентпропертиес**</span><span class="sxs-lookup"><span data-stu-id="2efce-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="2efce-131">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="2efce-131">Cell index:</span></span>  <br/> |<span data-ttu-id="2efce-132">**Вислинеградиентдир**</span><span class="sxs-lookup"><span data-stu-id="2efce-132">**visLineGradientDir**</span></span> <br/> |
   

