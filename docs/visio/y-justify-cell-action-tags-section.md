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
ms.openlocfilehash: d7a1f5c1feda3624c9f96039e7247c737a91a813
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419984"
---
# <a name="y-justify-cell-action-tags-section"></a><span data-ttu-id="6d56b-103">Ячейка Y Justify (раздел "Теги действий")</span><span class="sxs-lookup"><span data-stu-id="6d56b-103">Y Justify Cell (Action Tags Section)</span></span>

<span data-ttu-id="6d56b-104">Смещение по оси *y* для кнопки тега действия, связанной с точкой, которая определена ячейками X и Y.</span><span class="sxs-lookup"><span data-stu-id="6d56b-104">The  *y*  -offset of the action tag button relative to the point defined by the X and Y cells.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6d56b-105">В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами.</span><span class="sxs-lookup"><span data-stu-id="6d56b-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="6d56b-106">**Значение**</span><span class="sxs-lookup"><span data-stu-id="6d56b-106">**Value**</span></span>|<span data-ttu-id="6d56b-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6d56b-107">**Description**</span></span>|<span data-ttu-id="6d56b-108">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="6d56b-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="6d56b-109">нуль</span><span class="sxs-lookup"><span data-stu-id="6d56b-109">0</span></span>  <br/> | <span data-ttu-id="6d56b-110">Выравнивание по верхнему краю (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="6d56b-110">Top justified (the default).</span></span>  <br/> |<span data-ttu-id="6d56b-111">**visSmartTagYJustifyTop**</span><span class="sxs-lookup"><span data-stu-id="6d56b-111">**visSmartTagYJustifyTop**</span></span> <br/> |
| <span data-ttu-id="6d56b-112">1,1</span><span class="sxs-lookup"><span data-stu-id="6d56b-112">1</span></span>  <br/> | <span data-ttu-id="6d56b-113">Выравнивание по центру.</span><span class="sxs-lookup"><span data-stu-id="6d56b-113">Centered.</span></span>  <br/> |<span data-ttu-id="6d56b-114">**visSmartTagYJustifyMiddle**</span><span class="sxs-lookup"><span data-stu-id="6d56b-114">**visSmartTagYJustifyMiddle**</span></span> <br/> |
| <span data-ttu-id="6d56b-115">2</span><span class="sxs-lookup"><span data-stu-id="6d56b-115">2</span></span>  <br/> | <span data-ttu-id="6d56b-116">Выравнивание по нижнему краю.</span><span class="sxs-lookup"><span data-stu-id="6d56b-116">Bottom justified.</span></span>  <br/> |<span data-ttu-id="6d56b-117">**visSmartTagYJustifyBottom**</span><span class="sxs-lookup"><span data-stu-id="6d56b-117">**visSmartTagYJustifyBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d56b-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="6d56b-118">Remarks</span></span>

<span data-ttu-id="6d56b-119">Ячейки X Justify и Y Justify указывают, где размещается кнопка тега действия по отношению к точке, определенной в ячейках X и Y.</span><span class="sxs-lookup"><span data-stu-id="6d56b-119">The X Justify and Y Justify cells determine where the action tag button is placed in relation to the point defined in the X and Y cells.</span></span>
  
<span data-ttu-id="6d56b-120">Чтобы получить ссылку на ячейку Y Justify по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="6d56b-120">To get a reference to the Y Justify cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6d56b-121">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="6d56b-121">Cell name:</span></span>  <br/> | <span data-ttu-id="6d56b-122">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="6d56b-122">SmartTags.</span></span>  <span data-ttu-id="6d56b-123">*имя* .YJustify, где SmartTags.</span><span class="sxs-lookup"><span data-stu-id="6d56b-123">*name*  .YJustify           where SmartTags.</span></span> <span data-ttu-id="6d56b-124">*имя* — название строки тегов действий.</span><span class="sxs-lookup"><span data-stu-id="6d56b-124">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="6d56b-125">Чтобы получить ссылку на ячейку Y Justify по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="6d56b-125">To get a reference to the Y Justify cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6d56b-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="6d56b-126">Section index:</span></span>  <br/> |<span data-ttu-id="6d56b-127">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="6d56b-127">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="6d56b-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="6d56b-128">Row index:</span></span>  <br/> |<span data-ttu-id="6d56b-129">**visRowSmartTag** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="6d56b-129">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="6d56b-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="6d56b-130">Cell index:</span></span>  <br/> |<span data-ttu-id="6d56b-131">**visSmartTagYJustify**</span><span class="sxs-lookup"><span data-stu-id="6d56b-131">**visSmartTagYJustify**</span></span> <br/> |
   

