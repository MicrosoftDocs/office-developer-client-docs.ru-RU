---
title: Ячейка ReplaceLockText (раздел "Изменение поведения фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: Указывает ли значений указанного ячеек в основной фигуры перезаписи значений (в том числе локального значения) во время операции замены фигуры в процессе замены фигуры. ReplaceLockText определяет ли текст, отображаемый в образце перезаписывает текст фигура.
ms.openlocfilehash: 75fb0831e7361345f04d7912eb0a55959d9417cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814612"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a><span data-ttu-id="0e979-104">Ячейка ReplaceLockText (раздел "Изменение поведения фигуры")</span><span class="sxs-lookup"><span data-stu-id="0e979-104">ReplaceLockText Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="0e979-105">Указывает ли значений указанного ячеек в основной фигуры перезаписи значений (в том числе локального значения) во время операции замены фигуры в процессе замены фигуры.</span><span class="sxs-lookup"><span data-stu-id="0e979-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="0e979-106">**ReplaceLockText** определяет ли текст, отображаемый в образце перезаписывает текст фигура.</span><span class="sxs-lookup"><span data-stu-id="0e979-106">The **ReplaceLockText** determines whether the text displayed on the Master overwrites the text of the shape being replaced.</span></span> 
  
|<span data-ttu-id="0e979-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="0e979-107">**Value**</span></span>|<span data-ttu-id="0e979-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0e979-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0e979-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="0e979-109">TRUE</span></span>  <br/> | <span data-ttu-id="0e979-110">Текст в фигуру образца перезаписывает текст на старой фигуры.</span><span class="sxs-lookup"><span data-stu-id="0e979-110">The text on the master shape overwrites the text on the old shape.</span></span> <span data-ttu-id="0e979-111">Кроме того основной фигуры перезаписывает значений ячеек в следующих разделах во время операции замены фигуры:</span><span class="sxs-lookup"><span data-stu-id="0e979-111">In addition, the master shape overwrites the values of the cells in the following sections during a shape replacement operation:</span></span>  <br/> <span data-ttu-id="0e979-112">Раздел **Текстовых полей**</span><span class="sxs-lookup"><span data-stu-id="0e979-112">**Text Fields** section</span></span>  <br/> <span data-ttu-id="0e979-113">Раздел **Формат блока текста**</span><span class="sxs-lookup"><span data-stu-id="0e979-113">**Text Block Format** section</span></span>  <br/> |
|<span data-ttu-id="0e979-114">FALSE</span><span class="sxs-lookup"><span data-stu-id="0e979-114">FALSE</span></span>  <br/> |<span data-ttu-id="0e979-115">Фигура замены содержит текст, текстовые поля или другие свойства текст из старого фигуры, которые были добавлены в форму.</span><span class="sxs-lookup"><span data-stu-id="0e979-115">The replacement shape contains any text, text fields, or other text properties from the old shape that have been added to the shape.</span></span>  <br/> <span data-ttu-id="0e979-116">Если фигуры замещения содержит свойства текст из старого фигуры, фигуры замещения также имеет значения из **символов** и **абзацев** разделах старых фигуры при наличии более одного ряда.</span><span class="sxs-lookup"><span data-stu-id="0e979-116">When the replacement shape contains text properties from the old shape, the replacement shape also has the values from the **Character** and **Paragraph** sections of the old shape if they have more than one row.</span></span>  <br/> |
   
<span data-ttu-id="0e979-117">Если задано значение TRUE (1), значения основной фигуры заменяет значения следующих на фигура:</span><span class="sxs-lookup"><span data-stu-id="0e979-117">If set to TRUE (1), the values of the shape Master replaces the values of the following on the shape being replaced:</span></span>
  
- [<span data-ttu-id="0e979-118">Ячейка TheText (раздел "События")</span><span class="sxs-lookup"><span data-stu-id="0e979-118">TheText Cell (Events Section)</span></span>](thetext-cell-events-section.md)
    
- <span data-ttu-id="0e979-119">Ячеек в [раздел знаков](character-section.md)</span><span class="sxs-lookup"><span data-stu-id="0e979-119">Cells in the [Character Section](character-section.md)</span></span>
    
- <span data-ttu-id="0e979-120">Ячеек в [разделе абзаца](paragraph-section.md)</span><span class="sxs-lookup"><span data-stu-id="0e979-120">Cells in the [Paragraph Section](paragraph-section.md)</span></span>
    
- <span data-ttu-id="0e979-121">Ячеек [Tabs раздел](tabs-section.md)</span><span class="sxs-lookup"><span data-stu-id="0e979-121">Cells in the [Tabs Section](tabs-section.md)</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0e979-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="0e979-122">Remarks</span></span>

<span data-ttu-id="0e979-123">Для получения ссылки на ячейки **ReplaceLockText** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="0e979-123">To get a reference to the **ReplaceLockText** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0e979-124">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="0e979-124">Cell name:</span></span>  <br/> | <span data-ttu-id="0e979-125">ReplaceLockText</span><span class="sxs-lookup"><span data-stu-id="0e979-125">ReplaceLockText</span></span>  <br/> |
   
<span data-ttu-id="0e979-126">Для получения ссылки на ячейки **ReplaceLockText** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="0e979-126">To get a reference to the **ReplaceLockText** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0e979-127">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0e979-127">Section index:</span></span>  <br/> |<span data-ttu-id="0e979-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0e979-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0e979-129">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0e979-129">Row index:</span></span>  <br/> |<span data-ttu-id="0e979-130">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="0e979-130">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="0e979-131">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0e979-131">Cell index:</span></span>  <br/> |<span data-ttu-id="0e979-132">**visReplaceLockText**</span><span class="sxs-lookup"><span data-stu-id="0e979-132">**visReplaceLockText**</span></span> <br/> |
   

