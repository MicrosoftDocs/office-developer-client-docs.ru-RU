---
title: LineGradientDir Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c603f9a5-f887-47ce-90bb-d41ec2d1a6a1
description: Определяет направление градиента линии. Градиент может быть линейным, радиальным, прямоугольным или следовать по пути.
ms.openlocfilehash: 05dcc6904a4e67d97c632dba44635936b1c14049
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417989"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a><span data-ttu-id="c5146-104">LineGradientDir Cell (Gradient Properties Section)</span><span class="sxs-lookup"><span data-stu-id="c5146-104">LineGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="c5146-105">Определяет направление градиента линии.</span><span class="sxs-lookup"><span data-stu-id="c5146-105">Determines the direction of the line gradient.</span></span> <span data-ttu-id="c5146-106">Градиент может быть линейным, радиальным, прямоугольным или следовать по пути.</span><span class="sxs-lookup"><span data-stu-id="c5146-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c5146-107">Линейный градиент — это единственный градиент, который принимает дополнительное значение угла (определяется ячейкой **LineGradientDir).**</span><span class="sxs-lookup"><span data-stu-id="c5146-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **LineGradientDir** cell).</span></span> <span data-ttu-id="c5146-108">Все остальные направления градиента имеют предустановленные enumerations.</span><span class="sxs-lookup"><span data-stu-id="c5146-108">All other gradient directions have preset enumerations.</span></span> 
  
|<span data-ttu-id="c5146-109">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c5146-109">**Value**</span></span>|<span data-ttu-id="c5146-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c5146-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c5146-111">0</span><span class="sxs-lookup"><span data-stu-id="c5146-111">0</span></span>  <br/> |<span data-ttu-id="c5146-112">Линейный градиент.</span><span class="sxs-lookup"><span data-stu-id="c5146-112">Linear gradient.</span></span> <span data-ttu-id="c5146-113">Ячейка **LineGradientAngle** определяет направление градиента.</span><span class="sxs-lookup"><span data-stu-id="c5146-113">The **LineGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="c5146-114">1-7</span><span class="sxs-lookup"><span data-stu-id="c5146-114">1-7</span></span>  <br/> |<span data-ttu-id="c5146-115">Радиальные градиенты.</span><span class="sxs-lookup"><span data-stu-id="c5146-115">Radial gradients.</span></span> <span data-ttu-id="c5146-116">Градиент расширяется по кругу от центральной точки.</span><span class="sxs-lookup"><span data-stu-id="c5146-116">The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="c5146-117">8-12</span><span class="sxs-lookup"><span data-stu-id="c5146-117">8-12</span></span>  <br/> |<span data-ttu-id="c5146-118">Прямоугольные градиенты.</span><span class="sxs-lookup"><span data-stu-id="c5146-118">Rectangular gradients.</span></span> <span data-ttu-id="c5146-119">Градиент расширяется как направленная линия от начала с прямоугольным исчезаемым цветом.</span><span class="sxs-lookup"><span data-stu-id="c5146-119">The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="c5146-120">13 </span><span class="sxs-lookup"><span data-stu-id="c5146-120">13</span></span>  <br/> |<span data-ttu-id="c5146-121">Градиент пути.</span><span class="sxs-lookup"><span data-stu-id="c5146-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5146-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="c5146-122">Remarks</span></span>

<span data-ttu-id="c5146-123">Чтобы получить ссылку на ячейку **LineGradientDir** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="c5146-123">To get a reference to the **LineGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c5146-124">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="c5146-124">Cell name:</span></span>  <br/> | <span data-ttu-id="c5146-125">LineGradientDir</span><span class="sxs-lookup"><span data-stu-id="c5146-125">LineGradientDir</span></span>  <br/> |
   
<span data-ttu-id="c5146-126">Чтобы получить ссылку на ячейку **LineGradientDir** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="c5146-126">To get a reference to the **LineGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c5146-127">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c5146-127">Section index:</span></span>  <br/> |<span data-ttu-id="c5146-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c5146-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c5146-129">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c5146-129">Row index:</span></span>  <br/> |<span data-ttu-id="c5146-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="c5146-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="c5146-131">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c5146-131">Cell index:</span></span>  <br/> |<span data-ttu-id="c5146-132">**visLineGradientDir**</span><span class="sxs-lookup"><span data-stu-id="c5146-132">**visLineGradientDir**</span></span> <br/> |
   

