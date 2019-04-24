---
title: CompoundType Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: Определяет составной тип линии фигуры.
ms.openlocfilehash: 120975e419656234266cb8151b2fa37ef19602e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359374"
---
# <a name="compoundtype-cell-line-format-section"></a><span data-ttu-id="ac217-103">CompoundType Cell (Line Format Section)</span><span class="sxs-lookup"><span data-stu-id="ac217-103">CompoundType Cell (Line Format Section)</span></span>

<span data-ttu-id="ac217-104">Определяет составной тип линии фигуры.</span><span class="sxs-lookup"><span data-stu-id="ac217-104">Determines the compound type of the line of a shape.</span></span> 
  
|<span data-ttu-id="ac217-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="ac217-105">**Value**</span></span>|<span data-ttu-id="ac217-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ac217-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ac217-107">нуль</span><span class="sxs-lookup"><span data-stu-id="ac217-107">0</span></span>  <br/> |<span data-ttu-id="ac217-108">Simple (Простая)</span><span class="sxs-lookup"><span data-stu-id="ac217-108">Simple</span></span>  <br/> |
|<span data-ttu-id="ac217-109">1,1</span><span class="sxs-lookup"><span data-stu-id="ac217-109">1</span></span>  <br/> |<span data-ttu-id="ac217-110">Двойное с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="ac217-110">Double</span></span>  <br/> |
|<span data-ttu-id="ac217-111">2</span><span class="sxs-lookup"><span data-stu-id="ac217-111">2</span></span>  <br/> |<span data-ttu-id="ac217-112">Толстая тонкая</span><span class="sxs-lookup"><span data-stu-id="ac217-112">Thick thin</span></span>  <br/> |
|<span data-ttu-id="ac217-113">4</span><span class="sxs-lookup"><span data-stu-id="ac217-113">3</span></span>  <br/> |<span data-ttu-id="ac217-114">Тонкие плотности</span><span class="sxs-lookup"><span data-stu-id="ac217-114">Thin thick</span></span>  <br/> |
|<span data-ttu-id="ac217-115">SP4</span><span class="sxs-lookup"><span data-stu-id="ac217-115">4</span></span>  <br/> |<span data-ttu-id="ac217-116">Triple</span><span class="sxs-lookup"><span data-stu-id="ac217-116">Triple</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac217-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="ac217-117">Remarks</span></span>

<span data-ttu-id="ac217-118">Чтобы получить ссылку на ячейку **CompoundType** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="ac217-118">To get a reference to the **CompoundType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ac217-119">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="ac217-119">Cell name:</span></span>  <br/> | <span data-ttu-id="ac217-120">CompoundType</span><span class="sxs-lookup"><span data-stu-id="ac217-120">CompoundType</span></span>  <br/> |
   
<span data-ttu-id="ac217-121">Чтобы получить ссылку на ячейку **CompoundType** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="ac217-121">To get a reference to the **CompoundType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ac217-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ac217-122">Section index:</span></span>  <br/> |<span data-ttu-id="ac217-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ac217-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ac217-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ac217-124">Row index:</span></span>  <br/> |<span data-ttu-id="ac217-125">**Висровлине**</span><span class="sxs-lookup"><span data-stu-id="ac217-125">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="ac217-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ac217-126">Cell index:</span></span>  <br/> |<span data-ttu-id="ac217-127">**Вискомпаундтипе**</span><span class="sxs-lookup"><span data-stu-id="ac217-127">**visCompoundType**</span></span> <br/> |
   

