---
title: ReplaceLockText Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: Указывает, переоценили ли значения указанных ячеек в фигуре хозяина значения (включая локальные значения) фигуры, заменяемой во время операции замены фигуры. ReplaceLockText определяет, переопределяется ли текст, отображаемого на мастере, текст заменяемой фигуры.
ms.openlocfilehash: 299bd571ad935886879abb11108c3d0bd28e3183
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411920"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a><span data-ttu-id="c2f0e-104">ReplaceLockText Cell (Change Shape Behavior Section)</span><span class="sxs-lookup"><span data-stu-id="c2f0e-104">ReplaceLockText Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="c2f0e-105">Указывает, переоценили ли значения указанных ячеек в фигуре хозяина значения (включая локальные значения) фигуры, заменяемой во время операции замены фигуры.</span><span class="sxs-lookup"><span data-stu-id="c2f0e-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="c2f0e-106">**ReplaceLockText** определяет, переопределяется ли текст, отображаемого на мастере, текст заменяемой фигуры.</span><span class="sxs-lookup"><span data-stu-id="c2f0e-106">The **ReplaceLockText** determines whether the text displayed on the Master overwrites the text of the shape being replaced.</span></span> 
  
|<span data-ttu-id="c2f0e-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c2f0e-107">**Value**</span></span>|<span data-ttu-id="c2f0e-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c2f0e-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c2f0e-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="c2f0e-109">TRUE</span></span>  <br/> | <span data-ttu-id="c2f0e-110">Текст в фигуре хозяина переописает текст старой фигуры.</span><span class="sxs-lookup"><span data-stu-id="c2f0e-110">The text on the master shape overwrites the text on the old shape.</span></span> <span data-ttu-id="c2f0e-111">Кроме того, во время операции замены фигур основной фигуры переоценка значений ячеек в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="c2f0e-111">In addition, the master shape overwrites the values of the cells in the following sections during a shape replacement operation:</span></span>  <br/> <span data-ttu-id="c2f0e-112">**Раздел "Текстовые поля"**</span><span class="sxs-lookup"><span data-stu-id="c2f0e-112">**Text Fields** section</span></span>  <br/> <span data-ttu-id="c2f0e-113">**Раздел "Формат текстового блока"**</span><span class="sxs-lookup"><span data-stu-id="c2f0e-113">**Text Block Format** section</span></span>  <br/> |
|<span data-ttu-id="c2f0e-114">FALSE</span><span class="sxs-lookup"><span data-stu-id="c2f0e-114">FALSE</span></span>  <br/> |<span data-ttu-id="c2f0e-115">Фигура замены содержит текст, текстовые поля или другие свойства текста из старой фигуры, которые были добавлены в фигуру.</span><span class="sxs-lookup"><span data-stu-id="c2f0e-115">The replacement shape contains any text, text fields, or other text properties from the old shape that have been added to the shape.</span></span>  <br/> <span data-ttu-id="c2f0e-116">Если фигура замены содержит свойства текста из старой фигуры, она  также имеет значения из разделов **"Символ"** и "Абзац" старой фигуры, если их несколько строк.</span><span class="sxs-lookup"><span data-stu-id="c2f0e-116">When the replacement shape contains text properties from the old shape, the replacement shape also has the values from the **Character** and **Paragraph** sections of the old shape if they have more than one row.</span></span>  <br/> |
   
<span data-ttu-id="c2f0e-117">Если установлено значение TRUE (1), значения хозяина фигуры заменяют следующие значения для заменяемой фигуры:</span><span class="sxs-lookup"><span data-stu-id="c2f0e-117">If set to TRUE (1), the values of the shape Master replaces the values of the following on the shape being replaced:</span></span>
  
- [<span data-ttu-id="c2f0e-118">TheText Cell (Events Section)</span><span class="sxs-lookup"><span data-stu-id="c2f0e-118">TheText Cell (Events Section)</span></span>](thetext-cell-events-section.md)
    
- <span data-ttu-id="c2f0e-119">Ячейки в [разделе символов](character-section.md)</span><span class="sxs-lookup"><span data-stu-id="c2f0e-119">Cells in the [Character Section](character-section.md)</span></span>
    
- <span data-ttu-id="c2f0e-120">Ячейки в разделе ["Абзац"](paragraph-section.md)</span><span class="sxs-lookup"><span data-stu-id="c2f0e-120">Cells in the [Paragraph Section](paragraph-section.md)</span></span>
    
- <span data-ttu-id="c2f0e-121">Ячейки в [разделе вкладок](tabs-section.md)</span><span class="sxs-lookup"><span data-stu-id="c2f0e-121">Cells in the [Tabs Section](tabs-section.md)</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c2f0e-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="c2f0e-122">Remarks</span></span>

<span data-ttu-id="c2f0e-123">Чтобы получить ссылку на ячейку **ReplaceLockText** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="c2f0e-123">To get a reference to the **ReplaceLockText** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c2f0e-124">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="c2f0e-124">Cell name:</span></span>  <br/> | <span data-ttu-id="c2f0e-125">ReplaceLockText</span><span class="sxs-lookup"><span data-stu-id="c2f0e-125">ReplaceLockText</span></span>  <br/> |
   
<span data-ttu-id="c2f0e-126">Чтобы получить ссылку на ячейку **ReplaceLockText** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="c2f0e-126">To get a reference to the **ReplaceLockText** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c2f0e-127">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c2f0e-127">Section index:</span></span>  <br/> |<span data-ttu-id="c2f0e-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c2f0e-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c2f0e-129">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c2f0e-129">Row index:</span></span>  <br/> |<span data-ttu-id="c2f0e-130">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="c2f0e-130">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="c2f0e-131">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c2f0e-131">Cell index:</span></span>  <br/> |<span data-ttu-id="c2f0e-132">**visReplaceLockText**</span><span class="sxs-lookup"><span data-stu-id="c2f0e-132">**visReplaceLockText**</span></span> <br/> |
   

