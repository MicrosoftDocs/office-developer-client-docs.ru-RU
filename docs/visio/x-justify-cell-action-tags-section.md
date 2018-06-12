---
title: X ширине ячейки (раздел теги действие)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026936
localization_priority: Normal
ms.assetid: a8995020-3eaa-2b2c-eca0-dd475de4d06f
description: X - смещение кнопки тега действия относительно точки, заданной ячейками X и Y.
ms.openlocfilehash: 043d7b198ae5a529c623545fb54ef5aa1d32217d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815189"
---
# <a name="x-justify-cell-action-tags-section"></a><span data-ttu-id="ec121-103">X ширине ячейки (раздел теги действие)</span><span class="sxs-lookup"><span data-stu-id="ec121-103">X Justify Cell (Action Tags Section)</span></span>

<span data-ttu-id="ec121-104">*X* -смещение кнопки тега действия относительно точки, заданной ячейками X и Y.</span><span class="sxs-lookup"><span data-stu-id="ec121-104">The  *x*  -offset of the action tag button relative to the point defined by the X and Y cells.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ec121-105">В предыдущих версиях Microsoft Visio теги действий, называются смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="ec121-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="ec121-106">**Значение**</span><span class="sxs-lookup"><span data-stu-id="ec121-106">**Value**</span></span>|<span data-ttu-id="ec121-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ec121-107">**Description**</span></span>|<span data-ttu-id="ec121-108">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="ec121-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="ec121-109">0</span><span class="sxs-lookup"><span data-stu-id="ec121-109">0</span></span>  <br/> | <span data-ttu-id="ec121-110">По левому краю (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="ec121-110">Left justified (the default).</span></span>  <br/> |<span data-ttu-id="ec121-111">**visSmartTagXJustifyLeft**</span><span class="sxs-lookup"><span data-stu-id="ec121-111">**visSmartTagXJustifyLeft**</span></span> <br/> |
| <span data-ttu-id="ec121-112">1</span><span class="sxs-lookup"><span data-stu-id="ec121-112">1</span></span>  <br/> | <span data-ttu-id="ec121-113">По центру.</span><span class="sxs-lookup"><span data-stu-id="ec121-113">Centered.</span></span>  <br/> |<span data-ttu-id="ec121-114">**visSmartTagXJustifyCenter**</span><span class="sxs-lookup"><span data-stu-id="ec121-114">**visSmartTagXJustifyCenter**</span></span> <br/> |
| <span data-ttu-id="ec121-115">2</span><span class="sxs-lookup"><span data-stu-id="ec121-115">2</span></span>  <br/> | <span data-ttu-id="ec121-116">По правому краю.</span><span class="sxs-lookup"><span data-stu-id="ec121-116">Right justified.</span></span>  <br/> |<span data-ttu-id="ec121-117">**visSmartTagXJustifyRight**</span><span class="sxs-lookup"><span data-stu-id="ec121-117">**visSmartTagXJustifyRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ec121-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="ec121-118">Remarks</span></span>

<span data-ttu-id="ec121-119">Выровнять X и Y ширине ячеек определить размещение кнопки тега действия при использовании точки, заданной в ячейках X и Y.</span><span class="sxs-lookup"><span data-stu-id="ec121-119">The X Justify and Y Justify cells determine where the action tag button is placed in relation to the point defined in the X and Y cells.</span></span> 
  
<span data-ttu-id="ec121-120">Для получения ссылки на ячейку обоснование X по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="ec121-120">To get a reference to the X Justify cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ec121-121">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="ec121-121">Cell name:</span></span>  <br/> | <span data-ttu-id="ec121-122">Смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="ec121-122">SmartTags.</span></span>  <span data-ttu-id="ec121-123">*имя* . XJustify где смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="ec121-123">*name*  .XJustify           where SmartTags.</span></span> <span data-ttu-id="ec121-124">*имя* — это имя строки тега действия</span><span class="sxs-lookup"><span data-stu-id="ec121-124">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="ec121-125">Для получения ссылки на ячейки обоснование X по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="ec121-125">To get a reference to the X Justify cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ec121-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ec121-126">Section index:</span></span>  <br/> |<span data-ttu-id="ec121-127">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="ec121-127">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="ec121-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ec121-128">Row index:</span></span>  <br/> |<span data-ttu-id="ec121-129">**visRowSmartTag** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ec121-129">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="ec121-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ec121-130">Cell index:</span></span>  <br/> |<span data-ttu-id="ec121-131">**visSmartTagXJustify**</span><span class="sxs-lookup"><span data-stu-id="ec121-131">**visSmartTagXJustify**</span></span> <br/> |
   

