---
title: Ячейка ShapeShdwShow (раздел "Формат заливки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Определяет, будет ли фигуры тени, как целое число от 0 до 2.
ms.openlocfilehash: 72077e60089acd3cd3f8a9349691e1468f6b1f9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814798"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a><span data-ttu-id="5cdfa-103">Ячейка ShapeShdwShow (раздел "Формат заливки")</span><span class="sxs-lookup"><span data-stu-id="5cdfa-103">ShapeShdwShow Cell (Fill Format Section)</span></span>

<span data-ttu-id="5cdfa-104">Определяет, будет ли фигуры тени, как целое число от 0 до 2.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-104">Determines whether the shape displays a shadow, as an integer from 0 to 2.</span></span>
  
|<span data-ttu-id="5cdfa-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="5cdfa-105">**Value**</span></span>|<span data-ttu-id="5cdfa-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5cdfa-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5cdfa-107">0</span><span class="sxs-lookup"><span data-stu-id="5cdfa-107">0</span></span>  <br/> |<span data-ttu-id="5cdfa-108">Всегда отображать тени, если указан тени.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-108">Always display the shadow if a shadow is specified.</span></span> <span data-ttu-id="5cdfa-109">Теней в вложенные фигуры, не отображаются.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-109">The shadows for sub-shapes are not displayed.</span></span>  <br/> |
|<span data-ttu-id="5cdfa-110">1</span><span class="sxs-lookup"><span data-stu-id="5cdfa-110">1</span></span>  <br/> |<span data-ttu-id="5cdfa-111">Не отображать тени, пока не имеет родительского узла фигуры.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-111">Do not render a shadow unless the shape does not have a parent.</span></span> <span data-ttu-id="5cdfa-112">Используйте подменю фигура тени, если объединять.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-112">Use sub-shape shadows if grouped together.</span></span>  <br/> |
|<span data-ttu-id="5cdfa-113">2</span><span class="sxs-lookup"><span data-stu-id="5cdfa-113">2</span></span>  <br/> |<span data-ttu-id="5cdfa-114">Всегда отображать тень Если указан тени.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-114">Always display a shadow if a shadow is specified.</span></span> <span data-ttu-id="5cdfa-115">Отображаются теней в вложенные фигуры.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-115">The shadows for sub-shapes are displayed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5cdfa-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="5cdfa-116">Remarks</span></span>

<span data-ttu-id="5cdfa-117">Для получения ссылки на ячейки **ShapeShdwShow** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="5cdfa-117">To get a reference to the **ShapeShdwShow** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5cdfa-118">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-118">Cell name:</span></span>  <br/> | <span data-ttu-id="5cdfa-119">ShapeShdwShow</span><span class="sxs-lookup"><span data-stu-id="5cdfa-119">ShapeShdwShow</span></span>  <br/> |
   
<span data-ttu-id="5cdfa-120">Для получения ссылки на ячейки **ShapeShdwShow** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="5cdfa-120">To get a reference to the **ShapeShdwShow** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5cdfa-121">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5cdfa-121">Section index:</span></span>  <br/> |<span data-ttu-id="5cdfa-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5cdfa-122">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5cdfa-123">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5cdfa-123">Row index:</span></span>  <br/> |<span data-ttu-id="5cdfa-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="5cdfa-124">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="5cdfa-125">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5cdfa-125">Cell index:</span></span>  <br/> |<span data-ttu-id="5cdfa-126">**visFillShdwShow**</span><span class="sxs-lookup"><span data-stu-id="5cdfa-126">**visFillShdwShow**</span></span> <br/> |
   

