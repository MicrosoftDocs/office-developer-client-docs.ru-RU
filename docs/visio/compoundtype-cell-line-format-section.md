---
title: Ячейка CompoundType (раздел "Формат линий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: Определяет тип составные строки фигуры.
ms.openlocfilehash: 663b683030251c8b57324f1d2bdf492463c50eef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813431"
---
# <a name="compoundtype-cell-line-format-section"></a><span data-ttu-id="07d65-103">Ячейка CompoundType (раздел "Формат линий")</span><span class="sxs-lookup"><span data-stu-id="07d65-103">CompoundType Cell (Line Format Section)</span></span>

<span data-ttu-id="07d65-104">Определяет тип составные строки фигуры.</span><span class="sxs-lookup"><span data-stu-id="07d65-104">Determines the compound type of the line of a shape.</span></span> 
  
|<span data-ttu-id="07d65-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="07d65-105">**Value**</span></span>|<span data-ttu-id="07d65-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="07d65-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="07d65-107">0</span><span class="sxs-lookup"><span data-stu-id="07d65-107">0</span></span>  <br/> |<span data-ttu-id="07d65-108">Простое</span><span class="sxs-lookup"><span data-stu-id="07d65-108">Simple</span></span>  <br/> |
|<span data-ttu-id="07d65-109">1</span><span class="sxs-lookup"><span data-stu-id="07d65-109">1</span></span>  <br/> |<span data-ttu-id="07d65-110">Double</span><span class="sxs-lookup"><span data-stu-id="07d65-110">Double</span></span>  <br/> |
|<span data-ttu-id="07d65-111">2</span><span class="sxs-lookup"><span data-stu-id="07d65-111">2</span></span>  <br/> |<span data-ttu-id="07d65-112">Жирная тонкая</span><span class="sxs-lookup"><span data-stu-id="07d65-112">Thick thin</span></span>  <br/> |
|<span data-ttu-id="07d65-113">3</span><span class="sxs-lookup"><span data-stu-id="07d65-113">3</span></span>  <br/> |<span data-ttu-id="07d65-114">Тонкая Жирная</span><span class="sxs-lookup"><span data-stu-id="07d65-114">Thin thick</span></span>  <br/> |
|<span data-ttu-id="07d65-115">4</span><span class="sxs-lookup"><span data-stu-id="07d65-115">4</span></span>  <br/> |<span data-ttu-id="07d65-116">Triple</span><span class="sxs-lookup"><span data-stu-id="07d65-116">Triple</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07d65-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="07d65-117">Remarks</span></span>

<span data-ttu-id="07d65-118">Для получения ссылки на ячейки **CompoundType** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="07d65-118">To get a reference to the **CompoundType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="07d65-119">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="07d65-119">Cell name:</span></span>  <br/> | <span data-ttu-id="07d65-120">CompoundType</span><span class="sxs-lookup"><span data-stu-id="07d65-120">CompoundType</span></span>  <br/> |
   
<span data-ttu-id="07d65-121">Для получения ссылки на ячейки **CompoundType** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="07d65-121">To get a reference to the **CompoundType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="07d65-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="07d65-122">Section index:</span></span>  <br/> |<span data-ttu-id="07d65-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="07d65-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="07d65-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="07d65-124">Row index:</span></span>  <br/> |<span data-ttu-id="07d65-125">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="07d65-125">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="07d65-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="07d65-126">Cell index:</span></span>  <br/> |<span data-ttu-id="07d65-127">**visCompoundType**</span><span class="sxs-lookup"><span data-stu-id="07d65-127">**visCompoundType**</span></span> <br/> |
   

