---
title: Ячейка X Justify (раздел "Теги действий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026936
localization_priority: Normal
ms.assetid: a8995020-3eaa-2b2c-eca0-dd475de4d06f
description: Смещение по оси x для кнопки тега действия, связанной с точкой, которая определена ячейками X и Y.
ms.openlocfilehash: 043d7b198ae5a529c623545fb54ef5aa1d32217d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815189"
---
# <a name="x-justify-cell-action-tags-section"></a><span data-ttu-id="c2976-103">Ячейка X Justify (раздел "Теги действий")</span><span class="sxs-lookup"><span data-stu-id="c2976-103">X Justify Cell (Action Tags Section)</span></span>

<span data-ttu-id="c2976-104">Смещение по оси *x* для кнопки тега действия, связанной с точкой, которая определена ячейками X и Y.</span><span class="sxs-lookup"><span data-stu-id="c2976-104">The  *x*  -offset of the action tag button relative to the point defined by the X and Y cells.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c2976-105">В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами.</span><span class="sxs-lookup"><span data-stu-id="c2976-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="c2976-106">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c2976-106">**Value**</span></span>|<span data-ttu-id="c2976-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c2976-107">**Description**</span></span>|<span data-ttu-id="c2976-108">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="c2976-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="c2976-109">0</span><span class="sxs-lookup"><span data-stu-id="c2976-109">0%</span></span>  <br/> | <span data-ttu-id="c2976-110">Выравнивание по левому краю (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="c2976-110">Left justified (the default).</span></span>  <br/> |<span data-ttu-id="c2976-111">**visSmartTagXJustifyLeft**</span><span class="sxs-lookup"><span data-stu-id="c2976-111">**visSmartTagXJustifyLeft**</span></span> <br/> |
| <span data-ttu-id="c2976-112">1</span><span class="sxs-lookup"><span data-stu-id="c2976-112">1</span></span>  <br/> | <span data-ttu-id="c2976-113">Выравнивание по центру.</span><span class="sxs-lookup"><span data-stu-id="c2976-113">Centered</span></span>  <br/> |<span data-ttu-id="c2976-114">**visSmartTagXJustifyCenter**</span><span class="sxs-lookup"><span data-stu-id="c2976-114">**visSmartTagXJustifyCenter**</span></span> <br/> |
| <span data-ttu-id="c2976-115">2</span><span class="sxs-lookup"><span data-stu-id="c2976-115">2</span></span>  <br/> | <span data-ttu-id="c2976-116">Выравнивание по правому краю.</span><span class="sxs-lookup"><span data-stu-id="c2976-116">Right justified.</span></span>  <br/> |<span data-ttu-id="c2976-117">**visSmartTagXJustifyRight**</span><span class="sxs-lookup"><span data-stu-id="c2976-117">**visSmartTagXJustifyRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2976-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="c2976-118">Remarks</span></span>

<span data-ttu-id="c2976-119">Ячейки X Justify и Y Justify указывают, где размещается кнопка тега действия по отношению к точке, определенной в ячейках X и Y.</span><span class="sxs-lookup"><span data-stu-id="c2976-119">The X Justify and Y Justify cells determine where the action tag button is placed in relation to the point defined in the X and Y cells.</span></span> 
  
<span data-ttu-id="c2976-120">Чтобы получить ссылку на ячейку X Justify по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="c2976-120">To get a reference to the X Justify cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c2976-121">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="c2976-121">Cell name:</span></span>  <br/> | <span data-ttu-id="c2976-122">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="c2976-122">SmartTags Property</span></span>  <span data-ttu-id="c2976-123">*имя* .XJustify, где SmartTags.</span><span class="sxs-lookup"><span data-stu-id="c2976-123">*name*  .XJustify           where SmartTags.</span></span> <span data-ttu-id="c2976-124">*имя* — название строки тегов действий.</span><span class="sxs-lookup"><span data-stu-id="c2976-124">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="c2976-125">Чтобы получить ссылку на ячейку X Justify по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="c2976-125">To get a reference to the X Justify cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c2976-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c2976-126">Section index:</span></span>  <br/> |<span data-ttu-id="c2976-127">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="c2976-127">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="c2976-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c2976-128">Row index:</span></span>  <br/> |<span data-ttu-id="c2976-129">**visRowSmartTag** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="c2976-129">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c2976-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c2976-130">Cell index:</span></span>  <br/> |<span data-ttu-id="c2976-131">**visSmartTagXJustify**</span><span class="sxs-lookup"><span data-stu-id="c2976-131">**visSmartTagXJustify**</span></span> <br/> |
   

