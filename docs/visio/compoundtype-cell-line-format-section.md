---
title: CompoundType Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: Определяет сложный тип линии фигуры.
ms.openlocfilehash: 120975e419656234266cb8151b2fa37ef19602e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407174"
---
# <a name="compoundtype-cell-line-format-section"></a><span data-ttu-id="4b6f1-103">CompoundType Cell (Line Format Section)</span><span class="sxs-lookup"><span data-stu-id="4b6f1-103">CompoundType Cell (Line Format Section)</span></span>

<span data-ttu-id="4b6f1-104">Определяет сложный тип линии фигуры.</span><span class="sxs-lookup"><span data-stu-id="4b6f1-104">Determines the compound type of the line of a shape.</span></span> 
  
|<span data-ttu-id="4b6f1-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="4b6f1-105">**Value**</span></span>|<span data-ttu-id="4b6f1-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4b6f1-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4b6f1-107">0</span><span class="sxs-lookup"><span data-stu-id="4b6f1-107">0</span></span>  <br/> |<span data-ttu-id="4b6f1-108">Простой</span><span class="sxs-lookup"><span data-stu-id="4b6f1-108">Simple</span></span>  <br/> |
|<span data-ttu-id="4b6f1-109">1</span><span class="sxs-lookup"><span data-stu-id="4b6f1-109">1</span></span>  <br/> |<span data-ttu-id="4b6f1-110">Двойное с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="4b6f1-110">Double</span></span>  <br/> |
|<span data-ttu-id="4b6f1-111">2</span><span class="sxs-lookup"><span data-stu-id="4b6f1-111">2</span></span>  <br/> |<span data-ttu-id="4b6f1-112">Толстый тонкий</span><span class="sxs-lookup"><span data-stu-id="4b6f1-112">Thick thin</span></span>  <br/> |
|<span data-ttu-id="4b6f1-113">3</span><span class="sxs-lookup"><span data-stu-id="4b6f1-113">3</span></span>  <br/> |<span data-ttu-id="4b6f1-114">Тонкий толстый</span><span class="sxs-lookup"><span data-stu-id="4b6f1-114">Thin thick</span></span>  <br/> |
|<span data-ttu-id="4b6f1-115">4 </span><span class="sxs-lookup"><span data-stu-id="4b6f1-115">4</span></span>  <br/> |<span data-ttu-id="4b6f1-116">Triple</span><span class="sxs-lookup"><span data-stu-id="4b6f1-116">Triple</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4b6f1-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="4b6f1-117">Remarks</span></span>

<span data-ttu-id="4b6f1-118">Чтобы получить ссылку на ячейку **CompoundType** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы с использованием свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="4b6f1-118">To get a reference to the **CompoundType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4b6f1-119">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="4b6f1-119">Cell name:</span></span>  <br/> | <span data-ttu-id="4b6f1-120">CompoundType</span><span class="sxs-lookup"><span data-stu-id="4b6f1-120">CompoundType</span></span>  <br/> |
   
<span data-ttu-id="4b6f1-121">Чтобы получить ссылку на ячейку **CompoundType** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="4b6f1-121">To get a reference to the **CompoundType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4b6f1-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="4b6f1-122">Section index:</span></span>  <br/> |<span data-ttu-id="4b6f1-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4b6f1-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4b6f1-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="4b6f1-124">Row index:</span></span>  <br/> |<span data-ttu-id="4b6f1-125">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="4b6f1-125">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="4b6f1-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="4b6f1-126">Cell index:</span></span>  <br/> |<span data-ttu-id="4b6f1-127">**visCompoundType**</span><span class="sxs-lookup"><span data-stu-id="4b6f1-127">**visCompoundType**</span></span> <br/> |
   

