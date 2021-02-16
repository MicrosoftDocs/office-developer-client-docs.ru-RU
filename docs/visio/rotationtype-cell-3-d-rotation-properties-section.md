---
title: RotationType Cell (3-D Rotation Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Определяет, следует ли фигура параллельному повороту, повороту перспективы или повороту косой точки в виде одного или того же друг другу в виде 0–6.
ms.openlocfilehash: 676f8a15185242aacc1affb9f1bd200ff3df454d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422945"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a><span data-ttu-id="60053-103">RotationType Cell (3-D Rotation Properties Section)</span><span class="sxs-lookup"><span data-stu-id="60053-103">RotationType Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="60053-104">Определяет, следует ли фигура параллельному повороту, повороту перспективы или повороту косой точки в виде одного или того же друг другу в виде 0–6.</span><span class="sxs-lookup"><span data-stu-id="60053-104">Determines whether the shape follows a parallel rotation, a perspective rotation, or an oblique rotation, as an integer from 0 to 6.</span></span> 
  
|<span data-ttu-id="60053-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="60053-105">**Value**</span></span>|<span data-ttu-id="60053-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="60053-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="60053-107">0</span><span class="sxs-lookup"><span data-stu-id="60053-107">0</span></span>  <br/> |<span data-ttu-id="60053-108">Фигура не имеет поворота.</span><span class="sxs-lookup"><span data-stu-id="60053-108">The shape does not have any rotation.</span></span>  <br/> |
|<span data-ttu-id="60053-109">1 </span><span class="sxs-lookup"><span data-stu-id="60053-109">1</span></span>  <br/> |<span data-ttu-id="60053-110">Фигура имеет параллельный поворот.</span><span class="sxs-lookup"><span data-stu-id="60053-110">The shape has a parallel rotation.</span></span>  <br/> |
|<span data-ttu-id="60053-111">2 </span><span class="sxs-lookup"><span data-stu-id="60053-111">2</span></span>  <br/> |<span data-ttu-id="60053-112">Фигура имеет поворот перспективы.</span><span class="sxs-lookup"><span data-stu-id="60053-112">The shape has a perspective rotation.</span></span>  <br/> |
|<span data-ttu-id="60053-113">3 </span><span class="sxs-lookup"><span data-stu-id="60053-113">3</span></span>  <br/> |<span data-ttu-id="60053-114">Фигура имеет левый верхний поворот косой оси.</span><span class="sxs-lookup"><span data-stu-id="60053-114">The shape has a top left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="60053-115">4 </span><span class="sxs-lookup"><span data-stu-id="60053-115">4</span></span>  <br/> |<span data-ttu-id="60053-116">Фигура имеет правый верхний поворот косой оси.</span><span class="sxs-lookup"><span data-stu-id="60053-116">The shape has a top right oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="60053-117">5 </span><span class="sxs-lookup"><span data-stu-id="60053-117">5</span></span>  <br/> |<span data-ttu-id="60053-118">Фигура имеет левый нижний поворот косой оси.</span><span class="sxs-lookup"><span data-stu-id="60053-118">The shape has a bottom left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="60053-119">6 </span><span class="sxs-lookup"><span data-stu-id="60053-119">6</span></span>  <br/> |<span data-ttu-id="60053-120">Фигура имеет правый нижний поворот косой оси.</span><span class="sxs-lookup"><span data-stu-id="60053-120">The shape has a bottom right oblique rotation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="60053-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="60053-121">Remarks</span></span>

<span data-ttu-id="60053-122">Чтобы получить ссылку на ячейку **RotationType** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="60053-122">To get a reference to the **RotationType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="60053-123">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="60053-123">Cell name:</span></span>  <br/> |<span data-ttu-id="60053-124">RotationType</span><span class="sxs-lookup"><span data-stu-id="60053-124">RotationType</span></span>  <br/> |
   
<span data-ttu-id="60053-125">Чтобы получить ссылку на ячейку **RotationType** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="60053-125">To get a reference to the **RotationType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="60053-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="60053-126">Section index:</span></span>  <br/> |<span data-ttu-id="60053-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="60053-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="60053-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="60053-128">Row index:</span></span>  <br/> |<span data-ttu-id="60053-129">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="60053-129">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="60053-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="60053-130">Cell index:</span></span>  <br/> |<span data-ttu-id="60053-131">**visRotationType**</span><span class="sxs-lookup"><span data-stu-id="60053-131">**visRotationType**</span></span> <br/> |
   

