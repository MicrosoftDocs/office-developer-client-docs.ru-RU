---
title: Ячейка ReplaceLockFormat (раздел "Изменение поведения фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: Указывает ли значений указанного ячеек в основной фигуры перезаписи значений (в том числе локального значения) во время операции замены фигуры в процессе замены фигуры. Если ячейка ReplaceLockFormat основной фигуры задано значение TRUE (1), форматирования значения хозяином перезаписать все соответствующие значения заменяется основной фигуры.
ms.openlocfilehash: bf1e28353cc1e2d737a7d7a6dcd90caf14e19dc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814579"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a><span data-ttu-id="a47f8-104">Ячейка ReplaceLockFormat (раздел "Изменение поведения фигуры")</span><span class="sxs-lookup"><span data-stu-id="a47f8-104">ReplaceLockFormat Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="a47f8-105">Указывает ли значений указанного ячеек в основной фигуры перезаписи значений (в том числе локального значения) во время операции замены фигуры в процессе замены фигуры.</span><span class="sxs-lookup"><span data-stu-id="a47f8-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="a47f8-106">Если ячейка **ReplaceLockFormat** основной фигуры задано значение TRUE (1), форматирования значения хозяином перезаписать все соответствующие значения заменяется основной фигуры.</span><span class="sxs-lookup"><span data-stu-id="a47f8-106">If the **ReplaceLockFormat** cell of a master shape is set to TRUE (1), the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span> 
  
|<span data-ttu-id="a47f8-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="a47f8-107">**Value**</span></span>|<span data-ttu-id="a47f8-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a47f8-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a47f8-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="a47f8-109">TRUE</span></span>  <br/> |<span data-ttu-id="a47f8-110">Если ячейка **ReplaceLockFormat** основной фигуры задано значение TRUE, форматирования значения хозяином перезаписать все соответствующие значения заменяется основной фигуры.</span><span class="sxs-lookup"><span data-stu-id="a47f8-110">If the **ReplaceLockFormat** cell of a master shape is set to TRUE, the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span>  <br/> |
|<span data-ttu-id="a47f8-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="a47f8-111">FALSE</span></span>  <br/> |<span data-ttu-id="a47f8-112">Если ячейка **ReplaceLockFormat** основной фигуры задано значение FALSE, фигуры замещения содержит локального форматирования значения из старого фигуры после выполнения операции замены.</span><span class="sxs-lookup"><span data-stu-id="a47f8-112">If the **ReplaceLockFormat** cell of a master shape is set to FALSE, the replacement shape contains the local formatting values from the old shape after the replacement operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a47f8-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="a47f8-113">Remarks</span></span>

<span data-ttu-id="a47f8-114">Ячейки **ReplaceLockFormat** определяет ли образца фигуры перезаписывает во время операции замены фигуры локального форматирования значений ячеек в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="a47f8-114">The **ReplaceLockFormat** cell determines whether the master shape overwrites the local formatting values of the cells in the following sections during a shape replacement operation:</span></span> 
  
- <span data-ttu-id="a47f8-115">**Заполните поля формат** раздела</span><span class="sxs-lookup"><span data-stu-id="a47f8-115">**Fill Format** section</span></span> 
    
- <span data-ttu-id="a47f8-116">Раздел **Формат строки**</span><span class="sxs-lookup"><span data-stu-id="a47f8-116">**Line Format** section</span></span> 
    
- <span data-ttu-id="a47f8-117">Раздел **Экспресс-стилей**</span><span class="sxs-lookup"><span data-stu-id="a47f8-117">**Quick Style** section</span></span> 
    
- <span data-ttu-id="a47f8-118">Раздел **Свойства темы**</span><span class="sxs-lookup"><span data-stu-id="a47f8-118">**Theme Properties** section</span></span> 
    
- <span data-ttu-id="a47f8-119">В разделе **Градиента свойств**</span><span class="sxs-lookup"><span data-stu-id="a47f8-119">**Gradient Properties** section</span></span> 
    
- <span data-ttu-id="a47f8-120">В разделе **Свойств рельефов**</span><span class="sxs-lookup"><span data-stu-id="a47f8-120">**Bevel Properties** section</span></span> 
    
- <span data-ttu-id="a47f8-121">В разделе **Дополнительных свойств влияние**</span><span class="sxs-lookup"><span data-stu-id="a47f8-121">**Additional Effect Properties** section</span></span> 
    
- <span data-ttu-id="a47f8-122">Раздел **Строки градиента**</span><span class="sxs-lookup"><span data-stu-id="a47f8-122">**Line Gradient Stops** section</span></span> 
    
- <span data-ttu-id="a47f8-123">**Заполните поля градиента** раздел</span><span class="sxs-lookup"><span data-stu-id="a47f8-123">**Fill Gradient Stops** section</span></span> 
    
<span data-ttu-id="a47f8-124">Для получения ссылки на ячейки **ReplaceLockFormat** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="a47f8-124">To get a reference to the **ReplaceLockFormat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a47f8-125">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="a47f8-125">Cell name:</span></span>  <br/> | <span data-ttu-id="a47f8-126">ReplaceLockFormat</span><span class="sxs-lookup"><span data-stu-id="a47f8-126">ReplaceLockFormat</span></span>  <br/> |
   
<span data-ttu-id="a47f8-127">Для получения ссылки на ячейки **ReplaceLockFormat** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="a47f8-127">To get a reference to the **ReplaceLockFormat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a47f8-128">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a47f8-128">Section index:</span></span>  <br/> |<span data-ttu-id="a47f8-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a47f8-129">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a47f8-130">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a47f8-130">Row index:</span></span>  <br/> |<span data-ttu-id="a47f8-131">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="a47f8-131">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="a47f8-132">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a47f8-132">Cell index:</span></span>  <br/> |<span data-ttu-id="a47f8-133">**visReplaceLockFormat**</span><span class="sxs-lookup"><span data-stu-id="a47f8-133">**visReplaceLockFormat**</span></span> <br/> |
   

