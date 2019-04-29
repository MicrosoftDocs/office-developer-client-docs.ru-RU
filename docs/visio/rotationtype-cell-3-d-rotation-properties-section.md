---
title: RotationType Cell (3-D Rotation Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Определяет, соответствует ли фигура параллельному повороту, повороту перспективы или наклонному повороту в виде целого числа от 0 до 6.
ms.openlocfilehash: 676f8a15185242aacc1affb9f1bd200ff3df454d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422945"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a><span data-ttu-id="5bee6-103">RotationType Cell (3-D Rotation Properties Section)</span><span class="sxs-lookup"><span data-stu-id="5bee6-103">RotationType Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="5bee6-104">Определяет, соответствует ли фигура параллельному повороту, повороту перспективы или наклонному повороту в виде целого числа от 0 до 6.</span><span class="sxs-lookup"><span data-stu-id="5bee6-104">Determines whether the shape follows a parallel rotation, a perspective rotation, or an oblique rotation, as an integer from 0 to 6.</span></span> 
  
|<span data-ttu-id="5bee6-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="5bee6-105">**Value**</span></span>|<span data-ttu-id="5bee6-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5bee6-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5bee6-107">нуль</span><span class="sxs-lookup"><span data-stu-id="5bee6-107">0</span></span>  <br/> |<span data-ttu-id="5bee6-108">Фигура не имеет вращения.</span><span class="sxs-lookup"><span data-stu-id="5bee6-108">The shape does not have any rotation.</span></span>  <br/> |
|<span data-ttu-id="5bee6-109">1,1</span><span class="sxs-lookup"><span data-stu-id="5bee6-109">1</span></span>  <br/> |<span data-ttu-id="5bee6-110">Фигура имеет параллельный поворот.</span><span class="sxs-lookup"><span data-stu-id="5bee6-110">The shape has a parallel rotation.</span></span>  <br/> |
|<span data-ttu-id="5bee6-111">2</span><span class="sxs-lookup"><span data-stu-id="5bee6-111">2</span></span>  <br/> |<span data-ttu-id="5bee6-112">Фигура имеет перспективный поворот.</span><span class="sxs-lookup"><span data-stu-id="5bee6-112">The shape has a perspective rotation.</span></span>  <br/> |
|<span data-ttu-id="5bee6-113">4</span><span class="sxs-lookup"><span data-stu-id="5bee6-113">3</span></span>  <br/> |<span data-ttu-id="5bee6-114">Фигура имеет верхний левый наклонный поворот.</span><span class="sxs-lookup"><span data-stu-id="5bee6-114">The shape has a top left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="5bee6-115">SP4</span><span class="sxs-lookup"><span data-stu-id="5bee6-115">4</span></span>  <br/> |<span data-ttu-id="5bee6-116">Фигура имеет верхний правый наклонный угол.</span><span class="sxs-lookup"><span data-stu-id="5bee6-116">The shape has a top right oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="5bee6-117">17:00</span><span class="sxs-lookup"><span data-stu-id="5bee6-117">5</span></span>  <br/> |<span data-ttu-id="5bee6-118">Фигура имеет нижний поворот с наклоном влево.</span><span class="sxs-lookup"><span data-stu-id="5bee6-118">The shape has a bottom left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="5bee6-119">ICMPv6</span><span class="sxs-lookup"><span data-stu-id="5bee6-119">6</span></span>  <br/> |<span data-ttu-id="5bee6-120">Фигура имеет нижний правый наклонный угол.</span><span class="sxs-lookup"><span data-stu-id="5bee6-120">The shape has a bottom right oblique rotation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5bee6-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="5bee6-121">Remarks</span></span>

<span data-ttu-id="5bee6-122">Чтобы получить ссылку на ячейку **RotationType** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="5bee6-122">To get a reference to the **RotationType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5bee6-123">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="5bee6-123">Cell name:</span></span>  <br/> |<span data-ttu-id="5bee6-124">RotationType</span><span class="sxs-lookup"><span data-stu-id="5bee6-124">RotationType</span></span>  <br/> |
   
<span data-ttu-id="5bee6-125">Чтобы получить ссылку на ячейку **RotationType** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="5bee6-125">To get a reference to the **RotationType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5bee6-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5bee6-126">Section index:</span></span>  <br/> |<span data-ttu-id="5bee6-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5bee6-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="5bee6-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5bee6-128">Row index:</span></span>  <br/> |<span data-ttu-id="5bee6-129">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="5bee6-129">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="5bee6-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5bee6-130">Cell index:</span></span>  <br/> |<span data-ttu-id="5bee6-131">**Висротатионтипе**</span><span class="sxs-lookup"><span data-stu-id="5bee6-131">**visRotationType**</span></span> <br/> |
   

