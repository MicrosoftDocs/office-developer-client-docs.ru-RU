---
title: ReplaceLockFormat Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: Указывает, перезаписывает ли значения заданных ячеек в главной фигуре значения (включая локальные значения) фигуры, которые заменяются во время операции замены фигуры. Если ячейка ReplaceLockFormat главной фигуры имеет значение TRUE (1), то значения форматирования образца перезапишу все соответствующие значения фигуры, замещенной образцом.
ms.openlocfilehash: 88af22accb7a80640e7553338dae1af48934f246
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329892"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a><span data-ttu-id="df8e7-104">ReplaceLockFormat Cell (Change Shape Behavior Section)</span><span class="sxs-lookup"><span data-stu-id="df8e7-104">ReplaceLockFormat Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="df8e7-105">Указывает, перезаписывает ли значения заданных ячеек в главной фигуре значения (включая локальные значения) фигуры, которые заменяются во время операции замены фигуры.</span><span class="sxs-lookup"><span data-stu-id="df8e7-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="df8e7-106">Если ячейка **ReplaceLockFormat** главной фигуры имеет значение true (1), то значения форматирования образца перезапишу все соответствующие значения фигуры, замещенной образцом.</span><span class="sxs-lookup"><span data-stu-id="df8e7-106">If the **ReplaceLockFormat** cell of a master shape is set to TRUE (1), the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span> 
  
|<span data-ttu-id="df8e7-107">**Value**</span><span class="sxs-lookup"><span data-stu-id="df8e7-107">**Value**</span></span>|<span data-ttu-id="df8e7-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="df8e7-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="df8e7-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="df8e7-109">TRUE</span></span>  <br/> |<span data-ttu-id="df8e7-110">Если ячейка **ReplaceLockFormat** главной фигуры имеет значение true, то значения форматирования образца перезапишу все соответствующие значения фигуры, замещенной образцом.</span><span class="sxs-lookup"><span data-stu-id="df8e7-110">If the **ReplaceLockFormat** cell of a master shape is set to TRUE, the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span>  <br/> |
|<span data-ttu-id="df8e7-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="df8e7-111">FALSE</span></span>  <br/> |<span data-ttu-id="df8e7-112">Если ячейка **ReplaceLockFormat** главной фигуры имеет значение false, фигура замещения содержит локальные значения форматирования из старой фигуры после операции замены.</span><span class="sxs-lookup"><span data-stu-id="df8e7-112">If the **ReplaceLockFormat** cell of a master shape is set to FALSE, the replacement shape contains the local formatting values from the old shape after the replacement operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df8e7-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df8e7-113">Remarks</span></span>

<span data-ttu-id="df8e7-114">Ячейка **ReplaceLockFormat** определяет, перезаписывает ли Главная фигура локальные значения форматирования ячеек в следующих разделах во время операции замены фигуры:</span><span class="sxs-lookup"><span data-stu-id="df8e7-114">The **ReplaceLockFormat** cell determines whether the master shape overwrites the local formatting values of the cells in the following sections during a shape replacement operation:</span></span> 
  
- <span data-ttu-id="df8e7-115">Раздел " **Формат заливки** "</span><span class="sxs-lookup"><span data-stu-id="df8e7-115">**Fill Format** section</span></span> 
    
- <span data-ttu-id="df8e7-116">Раздел " **Формат линий** "</span><span class="sxs-lookup"><span data-stu-id="df8e7-116">**Line Format** section</span></span> 
    
- <span data-ttu-id="df8e7-117">Раздел " **экспресс — стиль** "</span><span class="sxs-lookup"><span data-stu-id="df8e7-117">**Quick Style** section</span></span> 
    
- <span data-ttu-id="df8e7-118">Раздел " **свойства темы** "</span><span class="sxs-lookup"><span data-stu-id="df8e7-118">**Theme Properties** section</span></span> 
    
- <span data-ttu-id="df8e7-119">Раздел " **Свойства градиента** "</span><span class="sxs-lookup"><span data-stu-id="df8e7-119">**Gradient Properties** section</span></span> 
    
- <span data-ttu-id="df8e7-120">Раздел " **Свойства багетНой рамки** "</span><span class="sxs-lookup"><span data-stu-id="df8e7-120">**Bevel Properties** section</span></span> 
    
- <span data-ttu-id="df8e7-121">Раздел " **Дополнительные свойства эффекты** "</span><span class="sxs-lookup"><span data-stu-id="df8e7-121">**Additional Effect Properties** section</span></span> 
    
- <span data-ttu-id="df8e7-122">Раздел " **позиции градиента линий** "</span><span class="sxs-lookup"><span data-stu-id="df8e7-122">**Line Gradient Stops** section</span></span> 
    
- <span data-ttu-id="df8e7-123">Раздел " **позиции градиента заполнения** "</span><span class="sxs-lookup"><span data-stu-id="df8e7-123">**Fill Gradient Stops** section</span></span> 
    
<span data-ttu-id="df8e7-124">Чтобы получить ссылку на ячейку **ReplaceLockFormat** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="df8e7-124">To get a reference to the **ReplaceLockFormat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="df8e7-125">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="df8e7-125">Cell name:</span></span>  <br/> | <span data-ttu-id="df8e7-126">ReplaceLockFormat</span><span class="sxs-lookup"><span data-stu-id="df8e7-126">ReplaceLockFormat</span></span>  <br/> |
   
<span data-ttu-id="df8e7-127">Чтобы получить ссылку на ячейку **ReplaceLockFormat** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="df8e7-127">To get a reference to the **ReplaceLockFormat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="df8e7-128">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="df8e7-128">Section index:</span></span>  <br/> |<span data-ttu-id="df8e7-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="df8e7-129">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="df8e7-130">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="df8e7-130">Row index:</span></span>  <br/> |<span data-ttu-id="df8e7-131">**Висровреплацебехавиорс**</span><span class="sxs-lookup"><span data-stu-id="df8e7-131">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="df8e7-132">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="df8e7-132">Cell index:</span></span>  <br/> |<span data-ttu-id="df8e7-133">**Висреплацелоккформат**</span><span class="sxs-lookup"><span data-stu-id="df8e7-133">**visReplaceLockFormat**</span></span> <br/> |
   

