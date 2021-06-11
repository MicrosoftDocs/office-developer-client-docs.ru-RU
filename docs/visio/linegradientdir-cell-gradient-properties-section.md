---
title: LineGradientDir Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c603f9a5-f887-47ce-90bb-d41ec2d1a6a1
description: Определяет направление градиента строки. Градиент может быть линейным, радиальным, прямоугольным или следовать по пути.
ms.openlocfilehash: 05dcc6904a4e67d97c632dba44635936b1c14049
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417989"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a><span data-ttu-id="bf1a1-104">LineGradientDir Cell (Gradient Properties Section)</span><span class="sxs-lookup"><span data-stu-id="bf1a1-104">LineGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="bf1a1-105">Определяет направление градиента строки.</span><span class="sxs-lookup"><span data-stu-id="bf1a1-105">Determines the direction of the line gradient.</span></span> <span data-ttu-id="bf1a1-106">Градиент может быть линейным, радиальным, прямоугольным или следовать по пути.</span><span class="sxs-lookup"><span data-stu-id="bf1a1-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="bf1a1-107">Линейный градиент — это единственный градиент, который принимает дополнительное значение угла (как определяется **ячейкой LineGradientDir).**</span><span class="sxs-lookup"><span data-stu-id="bf1a1-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **LineGradientDir** cell).</span></span> <span data-ttu-id="bf1a1-108">Все остальные направления градиента имеют заранее.</span><span class="sxs-lookup"><span data-stu-id="bf1a1-108">All other gradient directions have preset enumerations.</span></span> 
  
|<span data-ttu-id="bf1a1-109">**Значение**</span><span class="sxs-lookup"><span data-stu-id="bf1a1-109">**Value**</span></span>|<span data-ttu-id="bf1a1-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bf1a1-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bf1a1-111">0</span><span class="sxs-lookup"><span data-stu-id="bf1a1-111">0</span></span>  <br/> |<span data-ttu-id="bf1a1-112">Линейный градиент.</span><span class="sxs-lookup"><span data-stu-id="bf1a1-112">Linear gradient.</span></span> <span data-ttu-id="bf1a1-113">Ячейка **LineGradientAngle** определяет направление градиента.</span><span class="sxs-lookup"><span data-stu-id="bf1a1-113">The **LineGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="bf1a1-114">1-7</span><span class="sxs-lookup"><span data-stu-id="bf1a1-114">1-7</span></span>  <br/> |<span data-ttu-id="bf1a1-115">Радиальные градиенты.</span><span class="sxs-lookup"><span data-stu-id="bf1a1-115">Radial gradients.</span></span> <span data-ttu-id="bf1a1-116">Градиент простирается наружу по кругу из центральной точки.</span><span class="sxs-lookup"><span data-stu-id="bf1a1-116">The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="bf1a1-117">8-12</span><span class="sxs-lookup"><span data-stu-id="bf1a1-117">8-12</span></span>  <br/> |<span data-ttu-id="bf1a1-118">Прямоугольные градиенты.</span><span class="sxs-lookup"><span data-stu-id="bf1a1-118">Rectangular gradients.</span></span> <span data-ttu-id="bf1a1-119">Градиент расширяется в виде направления от начала с прямоугольной формой.</span><span class="sxs-lookup"><span data-stu-id="bf1a1-119">The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="bf1a1-120">13</span><span class="sxs-lookup"><span data-stu-id="bf1a1-120">13</span></span>  <br/> |<span data-ttu-id="bf1a1-121">Градиент пути.</span><span class="sxs-lookup"><span data-stu-id="bf1a1-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf1a1-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="bf1a1-122">Remarks</span></span>

<span data-ttu-id="bf1a1-123">Чтобы получить ссылку на **ячейку LineGradientDir** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы с использованием свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="bf1a1-123">To get a reference to the **LineGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bf1a1-124">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="bf1a1-124">Cell name:</span></span>  <br/> | <span data-ttu-id="bf1a1-125">LineGradientDir</span><span class="sxs-lookup"><span data-stu-id="bf1a1-125">LineGradientDir</span></span>  <br/> |
   
<span data-ttu-id="bf1a1-126">Чтобы получить ссылку на **ячейку LineGradientDir** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="bf1a1-126">To get a reference to the **LineGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bf1a1-127">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="bf1a1-127">Section index:</span></span>  <br/> |<span data-ttu-id="bf1a1-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bf1a1-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bf1a1-129">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="bf1a1-129">Row index:</span></span>  <br/> |<span data-ttu-id="bf1a1-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="bf1a1-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="bf1a1-131">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="bf1a1-131">Cell index:</span></span>  <br/> |<span data-ttu-id="bf1a1-132">**visLineGradientDir**</span><span class="sxs-lookup"><span data-stu-id="bf1a1-132">**visLineGradientDir**</span></span> <br/> |
   

