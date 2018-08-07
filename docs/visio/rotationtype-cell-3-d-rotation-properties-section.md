---
title: Ячейка RotationType (раздел "Свойства поворота объемной фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Определяет, следует ли фигуры параллельный цикл, перспективы поворот или наклон вращение, как целое число от 0 до 6.
ms.openlocfilehash: 85effcef3969d7b7c57551ec88710ba84b3fc163
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814663"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a><span data-ttu-id="a949c-103">Ячейка RotationType (раздел "Свойства поворота объемной фигуры")</span><span class="sxs-lookup"><span data-stu-id="a949c-103">RotationType Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="a949c-104">Определяет, следует ли фигуры параллельный цикл, перспективы поворот или наклон вращение, как целое число от 0 до 6.</span><span class="sxs-lookup"><span data-stu-id="a949c-104">Determines whether the shape follows a parallel rotation, a perspective rotation, or an oblique rotation, as an integer from 0 to 6.</span></span> 
  
|<span data-ttu-id="a949c-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="a949c-105">**Value**</span></span>|<span data-ttu-id="a949c-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a949c-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a949c-107">0</span><span class="sxs-lookup"><span data-stu-id="a949c-107">0</span></span>  <br/> |<span data-ttu-id="a949c-108">Фигура не имеет любое вращение.</span><span class="sxs-lookup"><span data-stu-id="a949c-108">The shape does not have any rotation.</span></span>  <br/> |
|<span data-ttu-id="a949c-109">1</span><span class="sxs-lookup"><span data-stu-id="a949c-109">1</span></span>  <br/> |<span data-ttu-id="a949c-110">Фигура имеет параллельный цикл.</span><span class="sxs-lookup"><span data-stu-id="a949c-110">The shape has a parallel rotation.</span></span>  <br/> |
|<span data-ttu-id="a949c-111">2</span><span class="sxs-lookup"><span data-stu-id="a949c-111">2</span></span>  <br/> |<span data-ttu-id="a949c-112">Фигура имеет вращение Перспектива.</span><span class="sxs-lookup"><span data-stu-id="a949c-112">The shape has a perspective rotation.</span></span>  <br/> |
|<span data-ttu-id="a949c-113">3</span><span class="sxs-lookup"><span data-stu-id="a949c-113">3</span></span>  <br/> |<span data-ttu-id="a949c-114">Фигура имеет верхней левой наклон вращение.</span><span class="sxs-lookup"><span data-stu-id="a949c-114">The shape has a top left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="a949c-115">4</span><span class="sxs-lookup"><span data-stu-id="a949c-115">4</span></span>  <br/> |<span data-ttu-id="a949c-116">Фигура имеет верхней прямо наклон вращение.</span><span class="sxs-lookup"><span data-stu-id="a949c-116">The shape has a top right oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="a949c-117">5</span><span class="sxs-lookup"><span data-stu-id="a949c-117">5</span></span>  <br/> |<span data-ttu-id="a949c-118">Фигура имеет наклонный вращение нижней левой.</span><span class="sxs-lookup"><span data-stu-id="a949c-118">The shape has a bottom left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="a949c-119">6</span><span class="sxs-lookup"><span data-stu-id="a949c-119">6</span></span>  <br/> |<span data-ttu-id="a949c-120">Фигура имеет нижней правой кнопкой наклон вращение.</span><span class="sxs-lookup"><span data-stu-id="a949c-120">The shape has a bottom right oblique rotation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a949c-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="a949c-121">Remarks</span></span>

<span data-ttu-id="a949c-122">Для получения ссылки на ячейки **RotationType** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="a949c-122">To get a reference to the **RotationType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a949c-123">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="a949c-123">Cell name:</span></span>  <br/> |<span data-ttu-id="a949c-124">RotationType</span><span class="sxs-lookup"><span data-stu-id="a949c-124">RotationType</span></span>  <br/> |
   
<span data-ttu-id="a949c-125">Для получения ссылки на ячейки **RotationType** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="a949c-125">To get a reference to the **RotationType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a949c-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a949c-126">Section index:</span></span>  <br/> |<span data-ttu-id="a949c-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a949c-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a949c-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a949c-128">Row index:</span></span>  <br/> |<span data-ttu-id="a949c-129">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="a949c-129">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="a949c-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a949c-130">Cell index:</span></span>  <br/> |<span data-ttu-id="a949c-131">**visRotationType**</span><span class="sxs-lookup"><span data-stu-id="a949c-131">**visRotationType**</span></span> <br/> |
   

