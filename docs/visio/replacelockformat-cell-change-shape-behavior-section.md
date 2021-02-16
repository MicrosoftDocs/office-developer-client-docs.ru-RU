---
title: ReplaceLockFormat Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: Указывает, переоценили ли значения указанных ячеек в фигуре хозяина значения (включая локальные значения) фигуры, заменяемой во время операции замены фигуры. Если для ячейки ReplaceLockFormat в фигуре хозяина установлено значение TRUE (1), значения форматирования хозяина переоценят все соответствующие значения фигуры, заменяемой хозяином.
ms.openlocfilehash: 88af22accb7a80640e7553338dae1af48934f246
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427236"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a><span data-ttu-id="560c2-104">ReplaceLockFormat Cell (Change Shape Behavior Section)</span><span class="sxs-lookup"><span data-stu-id="560c2-104">ReplaceLockFormat Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="560c2-105">Указывает, переоценили ли значения указанных ячеек в фигуре хозяина значения (включая локальные значения) фигуры, заменяемой во время операции замены фигуры.</span><span class="sxs-lookup"><span data-stu-id="560c2-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="560c2-106">Если для ячейки **ReplaceLockFormat** в фигуре хозяина установлено значение TRUE (1), значения форматирования хозяина переоценят все соответствующие значения фигуры, заменяемой хозяином.</span><span class="sxs-lookup"><span data-stu-id="560c2-106">If the **ReplaceLockFormat** cell of a master shape is set to TRUE (1), the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span> 
  
|<span data-ttu-id="560c2-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="560c2-107">**Value**</span></span>|<span data-ttu-id="560c2-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="560c2-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="560c2-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="560c2-109">TRUE</span></span>  <br/> |<span data-ttu-id="560c2-110">Если для **ячейки ReplaceLockFormat** для фигуры-хозяина установлено значение TRUE, значения форматирования хозяина заменяют все соответствующие значения фигуры, заменяемой хозяином.</span><span class="sxs-lookup"><span data-stu-id="560c2-110">If the **ReplaceLockFormat** cell of a master shape is set to TRUE, the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span>  <br/> |
|<span data-ttu-id="560c2-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="560c2-111">FALSE</span></span>  <br/> |<span data-ttu-id="560c2-112">Если **ячейка ReplaceLockFormat** для фигуры-хозяина имеет значение FALSE, замена фигуры содержит локальные значения форматирования из старой фигуры после операции замены.</span><span class="sxs-lookup"><span data-stu-id="560c2-112">If the **ReplaceLockFormat** cell of a master shape is set to FALSE, the replacement shape contains the local formatting values from the old shape after the replacement operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="560c2-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="560c2-113">Remarks</span></span>

<span data-ttu-id="560c2-114">Ячейка **ReplaceLockFormat** определяет, переопределяется ли в ходе операции замены фигуры значения локального форматирования ячеек в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="560c2-114">The **ReplaceLockFormat** cell determines whether the master shape overwrites the local formatting values of the cells in the following sections during a shape replacement operation:</span></span> 
  
- <span data-ttu-id="560c2-115">**Раздел "Формат заливки"**</span><span class="sxs-lookup"><span data-stu-id="560c2-115">**Fill Format** section</span></span> 
    
- <span data-ttu-id="560c2-116">**Раздел "Формат строки"**</span><span class="sxs-lookup"><span data-stu-id="560c2-116">**Line Format** section</span></span> 
    
- <span data-ttu-id="560c2-117">**Раздел "Быстрый стиль"**</span><span class="sxs-lookup"><span data-stu-id="560c2-117">**Quick Style** section</span></span> 
    
- <span data-ttu-id="560c2-118">**Раздел "Свойства темы"**</span><span class="sxs-lookup"><span data-stu-id="560c2-118">**Theme Properties** section</span></span> 
    
- <span data-ttu-id="560c2-119">**Раздел "Свойства градиента"**</span><span class="sxs-lookup"><span data-stu-id="560c2-119">**Gradient Properties** section</span></span> 
    
- <span data-ttu-id="560c2-120">**Раздел "Свойства bevel"**</span><span class="sxs-lookup"><span data-stu-id="560c2-120">**Bevel Properties** section</span></span> 
    
- <span data-ttu-id="560c2-121">**Раздел "Дополнительные свойства эффекта"**</span><span class="sxs-lookup"><span data-stu-id="560c2-121">**Additional Effect Properties** section</span></span> 
    
- <span data-ttu-id="560c2-122">**Раздел "Остановки градиента линии"**</span><span class="sxs-lookup"><span data-stu-id="560c2-122">**Line Gradient Stops** section</span></span> 
    
- <span data-ttu-id="560c2-123">**Раздел "Остановки градиента заливки"**</span><span class="sxs-lookup"><span data-stu-id="560c2-123">**Fill Gradient Stops** section</span></span> 
    
<span data-ttu-id="560c2-124">Чтобы получить ссылку на ячейку **ReplaceLockFormat** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="560c2-124">To get a reference to the **ReplaceLockFormat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="560c2-125">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="560c2-125">Cell name:</span></span>  <br/> | <span data-ttu-id="560c2-126">ReplaceLockFormat</span><span class="sxs-lookup"><span data-stu-id="560c2-126">ReplaceLockFormat</span></span>  <br/> |
   
<span data-ttu-id="560c2-127">Чтобы получить ссылку на ячейку **ReplaceLockFormat** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="560c2-127">To get a reference to the **ReplaceLockFormat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="560c2-128">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="560c2-128">Section index:</span></span>  <br/> |<span data-ttu-id="560c2-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="560c2-129">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="560c2-130">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="560c2-130">Row index:</span></span>  <br/> |<span data-ttu-id="560c2-131">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="560c2-131">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="560c2-132">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="560c2-132">Cell index:</span></span>  <br/> |<span data-ttu-id="560c2-133">**visReplaceLockFormat**</span><span class="sxs-lookup"><span data-stu-id="560c2-133">**visReplaceLockFormat**</span></span> <br/> |
   

