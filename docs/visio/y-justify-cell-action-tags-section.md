---
title: Y выровнять ячейки (действие помечает раздел)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026937
localization_priority: Normal
ms.assetid: 27042b62-7623-95d7-7e10-f589d74605c7
description: Y — смещение кнопки тега действия относительно точки, заданной ячейками X и Y.
ms.openlocfilehash: 8f8323d1f392654bf118ece2f78890f2a1b860ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815219"
---
# <a name="y-justify-cell-action-tags-section"></a><span data-ttu-id="667f2-103">Y выровнять ячейки (действие помечает раздел)</span><span class="sxs-lookup"><span data-stu-id="667f2-103">Y Justify Cell (Action Tags Section)</span></span>

<span data-ttu-id="667f2-104">*Y* — смещение кнопки тега действия относительно точки, заданной ячейками X и Y.</span><span class="sxs-lookup"><span data-stu-id="667f2-104">The  *y*  -offset of the action tag button relative to the point defined by the X and Y cells.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="667f2-105">В предыдущих версиях Microsoft Visio теги действий, называются смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="667f2-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="667f2-106">**Значение**</span><span class="sxs-lookup"><span data-stu-id="667f2-106">**Value**</span></span>|<span data-ttu-id="667f2-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="667f2-107">**Description**</span></span>|<span data-ttu-id="667f2-108">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="667f2-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="667f2-109">0</span><span class="sxs-lookup"><span data-stu-id="667f2-109">0</span></span>  <br/> | <span data-ttu-id="667f2-110">По верхнему краю (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="667f2-110">Top justified (the default).</span></span>  <br/> |<span data-ttu-id="667f2-111">**visSmartTagYJustifyTop**</span><span class="sxs-lookup"><span data-stu-id="667f2-111">**visSmartTagYJustifyTop**</span></span> <br/> |
| <span data-ttu-id="667f2-112">1</span><span class="sxs-lookup"><span data-stu-id="667f2-112">1</span></span>  <br/> | <span data-ttu-id="667f2-113">По центру.</span><span class="sxs-lookup"><span data-stu-id="667f2-113">Centered.</span></span>  <br/> |<span data-ttu-id="667f2-114">**visSmartTagYJustifyMiddle**</span><span class="sxs-lookup"><span data-stu-id="667f2-114">**visSmartTagYJustifyMiddle**</span></span> <br/> |
| <span data-ttu-id="667f2-115">2</span><span class="sxs-lookup"><span data-stu-id="667f2-115">2</span></span>  <br/> | <span data-ttu-id="667f2-116">По нижнему краю.</span><span class="sxs-lookup"><span data-stu-id="667f2-116">Bottom justified.</span></span>  <br/> |<span data-ttu-id="667f2-117">**visSmartTagYJustifyBottom**</span><span class="sxs-lookup"><span data-stu-id="667f2-117">**visSmartTagYJustifyBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="667f2-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="667f2-118">Remarks</span></span>

<span data-ttu-id="667f2-119">Выровнять X и Y ширине ячеек определить размещение кнопки тега действия при использовании точки, заданной в ячейках X и Y.</span><span class="sxs-lookup"><span data-stu-id="667f2-119">The X Justify and Y Justify cells determine where the action tag button is placed in relation to the point defined in the X and Y cells.</span></span>
  
<span data-ttu-id="667f2-120">Для получения ссылки на ячейки ширине Y по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="667f2-120">To get a reference to the Y Justify cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="667f2-121">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="667f2-121">Cell name:</span></span>  <br/> | <span data-ttu-id="667f2-122">Смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="667f2-122">SmartTags.</span></span>  <span data-ttu-id="667f2-123">*имя* . YJustify где смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="667f2-123">*name*  .YJustify           where SmartTags.</span></span> <span data-ttu-id="667f2-124">*имя* — это имя строки тега действия</span><span class="sxs-lookup"><span data-stu-id="667f2-124">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="667f2-125">Для получения ссылки на ячейки ширине Y по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="667f2-125">To get a reference to the Y Justify cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="667f2-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="667f2-126">Section index:</span></span>  <br/> |<span data-ttu-id="667f2-127">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="667f2-127">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="667f2-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="667f2-128">Row index:</span></span>  <br/> |<span data-ttu-id="667f2-129">**visRowSmartTag** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="667f2-129">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="667f2-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="667f2-130">Cell index:</span></span>  <br/> |<span data-ttu-id="667f2-131">**visSmartTagYJustify**</span><span class="sxs-lookup"><span data-stu-id="667f2-131">**visSmartTagYJustify**</span></span> <br/> |
   

