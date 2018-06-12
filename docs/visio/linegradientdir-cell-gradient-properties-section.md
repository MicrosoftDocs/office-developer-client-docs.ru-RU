---
title: Ячейка LineGradientDir (градиента Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c603f9a5-f887-47ce-90bb-d41ec2d1a6a1
description: Определяет направление градиента строки. Градиент линейно, Радиальное, прямоугольный, или выполните путь.
ms.openlocfilehash: 6243d7a6b470db0915ba6fc462f05b72a9814f66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814089"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a><span data-ttu-id="3e56f-104">Ячейка LineGradientDir (градиента Properties Section)</span><span class="sxs-lookup"><span data-stu-id="3e56f-104">LineGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="3e56f-105">Определяет направление градиента строки.</span><span class="sxs-lookup"><span data-stu-id="3e56f-105">Determines the direction of the line gradient.</span></span> <span data-ttu-id="3e56f-106">Градиент линейно, Радиальное, прямоугольный, или выполните путь.</span><span class="sxs-lookup"><span data-stu-id="3e56f-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3e56f-107">Линейный градиент — это единственный градиент, который принимает значения дополнительных угол (в зависимости от **LineGradientDir** ячейки).</span><span class="sxs-lookup"><span data-stu-id="3e56f-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **LineGradientDir** cell).</span></span> <span data-ttu-id="3e56f-108">Все другие градиента инструкции по панелям предварительно перечисления.</span><span class="sxs-lookup"><span data-stu-id="3e56f-108">All other gradient directions have preset enumerations.</span></span> 
  
|<span data-ttu-id="3e56f-109">**Значение**</span><span class="sxs-lookup"><span data-stu-id="3e56f-109">**Value**</span></span>|<span data-ttu-id="3e56f-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3e56f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3e56f-111">0</span><span class="sxs-lookup"><span data-stu-id="3e56f-111">0</span></span>  <br/> |<span data-ttu-id="3e56f-112">Линейный градиент.</span><span class="sxs-lookup"><span data-stu-id="3e56f-112">Linear gradient.</span></span> <span data-ttu-id="3e56f-113">Ячейка **LineGradientAngle** определяет направление градиента.</span><span class="sxs-lookup"><span data-stu-id="3e56f-113">The **LineGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="3e56f-114">1-7</span><span class="sxs-lookup"><span data-stu-id="3e56f-114">1-7</span></span>  <br/> |<span data-ttu-id="3e56f-115">Радиальное градиентом.</span><span class="sxs-lookup"><span data-stu-id="3e56f-115">Radial gradients.</span></span> <span data-ttu-id="3e56f-116">Градиента расширяет возможности outwards в круг из центральной точки.</span><span class="sxs-lookup"><span data-stu-id="3e56f-116">The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="3e56f-117">8-12</span><span class="sxs-lookup"><span data-stu-id="3e56f-117">8-12</span></span>  <br/> |<span data-ttu-id="3e56f-118">Прямоугольный градиентом.</span><span class="sxs-lookup"><span data-stu-id="3e56f-118">Rectangular gradients.</span></span> <span data-ttu-id="3e56f-119">Расширяет возможности градиента направления строке с происхождения с появления прямоугольной формы.</span><span class="sxs-lookup"><span data-stu-id="3e56f-119">The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="3e56f-120">13</span><span class="sxs-lookup"><span data-stu-id="3e56f-120">13</span></span>  <br/> |<span data-ttu-id="3e56f-121">Градиентные путь.</span><span class="sxs-lookup"><span data-stu-id="3e56f-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e56f-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="3e56f-122">Remarks</span></span>

<span data-ttu-id="3e56f-123">Для получения ссылки на ячейки **LineGradientDir** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="3e56f-123">To get a reference to the **LineGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3e56f-124">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="3e56f-124">Cell name:</span></span>  <br/> | <span data-ttu-id="3e56f-125">LineGradientDir</span><span class="sxs-lookup"><span data-stu-id="3e56f-125">LineGradientDir</span></span>  <br/> |
   
<span data-ttu-id="3e56f-126">Для получения ссылки на ячейки **LineGradientDir** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="3e56f-126">To get a reference to the **LineGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3e56f-127">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="3e56f-127">Section index:</span></span>  <br/> |<span data-ttu-id="3e56f-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3e56f-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3e56f-129">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="3e56f-129">Row index:</span></span>  <br/> |<span data-ttu-id="3e56f-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="3e56f-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="3e56f-131">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="3e56f-131">Cell index:</span></span>  <br/> |<span data-ttu-id="3e56f-132">**visLineGradientDir**</span><span class="sxs-lookup"><span data-stu-id="3e56f-132">**visLineGradientDir**</span></span> <br/> |
   

