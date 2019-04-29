---
title: ReplaceLockText Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: Указывает, перезаписывает ли значения заданных ячеек в главной фигуре значения (включая локальные значения) фигуры, которые заменяются во время операции замены фигуры. ReplaceLockText определяет, перезаписывает ли текст, отображаемый на образце, текст заменяемой фигуры.
ms.openlocfilehash: 299bd571ad935886879abb11108c3d0bd28e3183
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411920"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a><span data-ttu-id="33eea-104">ReplaceLockText Cell (Change Shape Behavior Section)</span><span class="sxs-lookup"><span data-stu-id="33eea-104">ReplaceLockText Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="33eea-105">Указывает, перезаписывает ли значения заданных ячеек в главной фигуре значения (включая локальные значения) фигуры, которые заменяются во время операции замены фигуры.</span><span class="sxs-lookup"><span data-stu-id="33eea-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="33eea-106">**ReplaceLockText** определяет, перезаписывает ли текст, отображаемый на образце, текст заменяемой фигуры.</span><span class="sxs-lookup"><span data-stu-id="33eea-106">The **ReplaceLockText** determines whether the text displayed on the Master overwrites the text of the shape being replaced.</span></span> 
  
|<span data-ttu-id="33eea-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="33eea-107">**Value**</span></span>|<span data-ttu-id="33eea-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="33eea-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="33eea-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="33eea-109">TRUE</span></span>  <br/> | <span data-ttu-id="33eea-110">Текст в фигуре образца перезаписывает текст на старой фигуре.</span><span class="sxs-lookup"><span data-stu-id="33eea-110">The text on the master shape overwrites the text on the old shape.</span></span> <span data-ttu-id="33eea-111">Кроме того, образец фигуры перезаписывает значения ячеек в следующих разделах во время операции замены фигуры:</span><span class="sxs-lookup"><span data-stu-id="33eea-111">In addition, the master shape overwrites the values of the cells in the following sections during a shape replacement operation:</span></span>  <br/> <span data-ttu-id="33eea-112">Раздел " **текстовые поля** "</span><span class="sxs-lookup"><span data-stu-id="33eea-112">**Text Fields** section</span></span>  <br/> <span data-ttu-id="33eea-113">Раздел " **Формат текстового блока** "</span><span class="sxs-lookup"><span data-stu-id="33eea-113">**Text Block Format** section</span></span>  <br/> |
|<span data-ttu-id="33eea-114">FALSE</span><span class="sxs-lookup"><span data-stu-id="33eea-114">FALSE</span></span>  <br/> |<span data-ttu-id="33eea-115">Замещающая фигура содержит любой текст, текстовые поля или другие свойства текста из старой фигуры, добавленной к фигуре.</span><span class="sxs-lookup"><span data-stu-id="33eea-115">The replacement shape contains any text, text fields, or other text properties from the old shape that have been added to the shape.</span></span>  <br/> <span data-ttu-id="33eea-116">Когда фигура замены содержит свойства текста из старой фигуры, замещающая фигура также имеет значения из разделов **знаков** и абзацев старой \*\*\*\* фигуры, если у них есть несколько строк.</span><span class="sxs-lookup"><span data-stu-id="33eea-116">When the replacement shape contains text properties from the old shape, the replacement shape also has the values from the **Character** and **Paragraph** sections of the old shape if they have more than one row.</span></span>  <br/> |
   
<span data-ttu-id="33eea-117">Если для этого параметра задано значение TRUE (1), значения образца фигуры заменят значения следующих параметров на заменяемую фигуру:</span><span class="sxs-lookup"><span data-stu-id="33eea-117">If set to TRUE (1), the values of the shape Master replaces the values of the following on the shape being replaced:</span></span>
  
- [<span data-ttu-id="33eea-118">TheText Cell (Events Section)</span><span class="sxs-lookup"><span data-stu-id="33eea-118">TheText Cell (Events Section)</span></span>](thetext-cell-events-section.md)
    
- <span data-ttu-id="33eea-119">Ячейки в [разделе "символ](character-section.md) "</span><span class="sxs-lookup"><span data-stu-id="33eea-119">Cells in the [Character Section](character-section.md)</span></span>
    
- <span data-ttu-id="33eea-120">Ячейки в [разделе абзаца](paragraph-section.md)</span><span class="sxs-lookup"><span data-stu-id="33eea-120">Cells in the [Paragraph Section](paragraph-section.md)</span></span>
    
- <span data-ttu-id="33eea-121">Ячейки в [разделе "вкладки](tabs-section.md) "</span><span class="sxs-lookup"><span data-stu-id="33eea-121">Cells in the [Tabs Section](tabs-section.md)</span></span>
    
## <a name="remarks"></a><span data-ttu-id="33eea-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="33eea-122">Remarks</span></span>

<span data-ttu-id="33eea-123">Чтобы получить ссылку на ячейку **ReplaceLockText** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="33eea-123">To get a reference to the **ReplaceLockText** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="33eea-124">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="33eea-124">Cell name:</span></span>  <br/> | <span data-ttu-id="33eea-125">ReplaceLockText</span><span class="sxs-lookup"><span data-stu-id="33eea-125">ReplaceLockText</span></span>  <br/> |
   
<span data-ttu-id="33eea-126">Чтобы получить ссылку на ячейку **ReplaceLockText** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="33eea-126">To get a reference to the **ReplaceLockText** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="33eea-127">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="33eea-127">Section index:</span></span>  <br/> |<span data-ttu-id="33eea-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="33eea-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="33eea-129">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="33eea-129">Row index:</span></span>  <br/> |<span data-ttu-id="33eea-130">**Висровреплацебехавиорс**</span><span class="sxs-lookup"><span data-stu-id="33eea-130">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="33eea-131">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="33eea-131">Cell index:</span></span>  <br/> |<span data-ttu-id="33eea-132">**Висреплацелокктекст**</span><span class="sxs-lookup"><span data-stu-id="33eea-132">**visReplaceLockText**</span></span> <br/> |
   

