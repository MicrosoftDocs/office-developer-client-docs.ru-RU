---
title: Ячейка DisplayMode (раздел "Теги действий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60039
localization_priority: Normal
ms.assetid: 0dfad40b-f97e-0c4a-2102-7344d1317b82
description: Определяет, отображается ли тег действия при наведении указателя мыши на тег, при выборе фигуры или все время.
ms.openlocfilehash: 4cb0666ca8de28247309de4fc0d2ff23e8b37d8a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813596"
---
# <a name="displaymode-cell-action-tags-section"></a><span data-ttu-id="7af49-103">Ячейка DisplayMode (раздел "Теги действий")</span><span class="sxs-lookup"><span data-stu-id="7af49-103">DisplayMode Cell (Action Tags Section)</span></span>

<span data-ttu-id="7af49-104">Определяет, отображается ли тег действия при наведении указателя мыши на тег, при выборе фигуры или все время.</span><span class="sxs-lookup"><span data-stu-id="7af49-104">Determines whether the action tag appears when the user moves the pointer over the tag, when the shape is selected, or all the time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7af49-105">В предыдущих версиях Microsoft Visio теги действий, называются смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="7af49-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="7af49-106">**Значение**</span><span class="sxs-lookup"><span data-stu-id="7af49-106">**Value**</span></span>|<span data-ttu-id="7af49-107">**Режим отображения**</span><span class="sxs-lookup"><span data-stu-id="7af49-107">**Display Mode**</span></span>|<span data-ttu-id="7af49-108">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="7af49-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="7af49-109">0</span><span class="sxs-lookup"><span data-stu-id="7af49-109">0</span></span>  <br/> | <span data-ttu-id="7af49-110">Отображается при наведении курсора на тег (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="7af49-110">Appears when the mouse is paused over the tag (the default).</span></span>  <br/> |<span data-ttu-id="7af49-111">**visSmartTagDispModeMouseOver**</span><span class="sxs-lookup"><span data-stu-id="7af49-111">**visSmartTagDispModeMouseOver**</span></span> <br/> |
| <span data-ttu-id="7af49-112">1</span><span class="sxs-lookup"><span data-stu-id="7af49-112">1</span></span>  <br/> | <span data-ttu-id="7af49-113">Появляется при выбранной фигуре.</span><span class="sxs-lookup"><span data-stu-id="7af49-113">Appears while the shape is selected.</span></span>  <br/> |<span data-ttu-id="7af49-114">**visSmartTagDispModeShapeSelected**</span><span class="sxs-lookup"><span data-stu-id="7af49-114">**visSmartTagDispModeShapeSelected**</span></span> <br/> |
| <span data-ttu-id="7af49-115">2</span><span class="sxs-lookup"><span data-stu-id="7af49-115">2</span></span>  <br/> | <span data-ttu-id="7af49-116">Появляется при запуске.</span><span class="sxs-lookup"><span data-stu-id="7af49-116">Appears all the time.</span></span>  <br/> |<span data-ttu-id="7af49-117">**visSmartTagDispModeAlways**</span><span class="sxs-lookup"><span data-stu-id="7af49-117">**visSmartTagDispModeAlways**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7af49-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="7af49-118">Remarks</span></span>

<span data-ttu-id="7af49-119">Теги действий не отображаются на печати и опубликованные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="7af49-119">Action tags do not appear on printed or published output.</span></span> 
  
<span data-ttu-id="7af49-120">Если тег действие определенные на странице, и эта ячейка содержит значение 1, тега никогда не отображается, поскольку страница не может быть выбран.</span><span class="sxs-lookup"><span data-stu-id="7af49-120">If an action tag is defined for a page, and this cell contains a value of 1, the tag never appears because a page cannot be selected.</span></span> 
  
<span data-ttu-id="7af49-121">Чтобы получить ссылку на ячейку DisplayMode по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="7af49-121">To get a reference to the DisplayMode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7af49-122">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="7af49-122">Cell name:</span></span>  <br/> | <span data-ttu-id="7af49-123">Смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="7af49-123">SmartTags.</span></span>  <span data-ttu-id="7af49-124">*имя* . DisplayMode где смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="7af49-124">*name*  .DisplayMode           where SmartTags.</span></span> <span data-ttu-id="7af49-125">*имя* — это имя строки тега действия</span><span class="sxs-lookup"><span data-stu-id="7af49-125">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="7af49-126">Для получения ссылки на ячейки DisplayMode по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="7af49-126">To get a reference to the DisplayMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7af49-127">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="7af49-127">Section index:</span></span>  <br/> |<span data-ttu-id="7af49-128">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="7af49-128">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="7af49-129">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="7af49-129">Row index:</span></span>  <br/> |<span data-ttu-id="7af49-130">**visRowSmartTag** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7af49-130">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="7af49-131">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="7af49-131">Cell index:</span></span>  <br/> |<span data-ttu-id="7af49-132">**visSmartTagDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="7af49-132">**visSmartTagDisplayMode**</span></span> <br/> |
   

