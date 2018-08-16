---
title: Ячейка Y Justify (раздел "Теги действий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026937
localization_priority: Normal
ms.assetid: 27042b62-7623-95d7-7e10-f589d74605c7
description: Смещение по оси Y для кнопки тега действия, связанной с точкой, которая определена ячейками X и Y.
ms.openlocfilehash: 8f8323d1f392654bf118ece2f78890f2a1b860ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815219"
---
# <a name="y-justify-cell-action-tags-section"></a><span data-ttu-id="23e7d-103">Ячейка Y Justify (раздел "Теги действий")</span><span class="sxs-lookup"><span data-stu-id="23e7d-103">Y Justify Cell (Action Tags Section)</span></span>

<span data-ttu-id="23e7d-104">Смещение по оси *y* для кнопки тега действия, связанной с точкой, которая определена ячейками X и Y.</span><span class="sxs-lookup"><span data-stu-id="23e7d-104">The  *y*  -offset of the action tag button relative to the point defined by the X and Y cells.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="23e7d-105">В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами.</span><span class="sxs-lookup"><span data-stu-id="23e7d-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="23e7d-106">**Значение**</span><span class="sxs-lookup"><span data-stu-id="23e7d-106">**Value**</span></span>|<span data-ttu-id="23e7d-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="23e7d-107">**Description**</span></span>|<span data-ttu-id="23e7d-108">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="23e7d-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="23e7d-109">0</span><span class="sxs-lookup"><span data-stu-id="23e7d-109">0%</span></span>  <br/> | <span data-ttu-id="23e7d-110">Выравнивание по верхнему краю (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="23e7d-110">Top justified (the default).</span></span>  <br/> |<span data-ttu-id="23e7d-111">**visSmartTagYJustifyTop**</span><span class="sxs-lookup"><span data-stu-id="23e7d-111">**visSmartTagYJustifyTop**</span></span> <br/> |
| <span data-ttu-id="23e7d-112">1</span><span class="sxs-lookup"><span data-stu-id="23e7d-112">1</span></span>  <br/> | <span data-ttu-id="23e7d-113">Выравнивание по центру.</span><span class="sxs-lookup"><span data-stu-id="23e7d-113">Centered</span></span>  <br/> |<span data-ttu-id="23e7d-114">**visSmartTagYJustifyMiddle**</span><span class="sxs-lookup"><span data-stu-id="23e7d-114">**visSmartTagYJustifyMiddle**</span></span> <br/> |
| <span data-ttu-id="23e7d-115">2</span><span class="sxs-lookup"><span data-stu-id="23e7d-115">2</span></span>  <br/> | <span data-ttu-id="23e7d-116">Выравнивание по нижнему краю.</span><span class="sxs-lookup"><span data-stu-id="23e7d-116">Bottom justified.</span></span>  <br/> |<span data-ttu-id="23e7d-117">**visSmartTagYJustifyBottom**</span><span class="sxs-lookup"><span data-stu-id="23e7d-117">**visSmartTagYJustifyBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23e7d-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="23e7d-118">Remarks</span></span>

<span data-ttu-id="23e7d-119">Ячейки X Justify и Y Justify указывают, где размещается кнопка тега действия по отношению к точке, определенной в ячейках X и Y.</span><span class="sxs-lookup"><span data-stu-id="23e7d-119">The X Justify and Y Justify cells determine where the action tag button is placed in relation to the point defined in the X and Y cells.</span></span>
  
<span data-ttu-id="23e7d-120">Чтобы получить ссылку на ячейку Y Justify по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="23e7d-120">To get a reference to the Y Justify cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="23e7d-121">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="23e7d-121">Cell name:</span></span>  <br/> | <span data-ttu-id="23e7d-122">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="23e7d-122">SmartTags Property</span></span>  <span data-ttu-id="23e7d-123">*имя* .YJustify, где SmartTags.</span><span class="sxs-lookup"><span data-stu-id="23e7d-123">*name*  .YJustify           where SmartTags.</span></span> <span data-ttu-id="23e7d-124">*имя* — название строки тегов действий.</span><span class="sxs-lookup"><span data-stu-id="23e7d-124">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="23e7d-125">Чтобы получить ссылку на ячейку Y Justify по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="23e7d-125">To get a reference to the Y Justify cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="23e7d-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="23e7d-126">Section index:</span></span>  <br/> |<span data-ttu-id="23e7d-127">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="23e7d-127">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="23e7d-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="23e7d-128">Row index:</span></span>  <br/> |<span data-ttu-id="23e7d-129">**visRowSmartTag** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="23e7d-129">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="23e7d-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="23e7d-130">Cell index:</span></span>  <br/> |<span data-ttu-id="23e7d-131">**visSmartTagYJustify**</span><span class="sxs-lookup"><span data-stu-id="23e7d-131">**visSmartTagYJustify**</span></span> <br/> |
   

