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
ms.openlocfilehash: f8542d2f3a22b12794d999323d202d7a5bece20b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414125"
---
# <a name="x-justify-cell-action-tags-section"></a><span data-ttu-id="7c772-103">Ячейка X Justify (раздел "Теги действий")</span><span class="sxs-lookup"><span data-stu-id="7c772-103">X Justify Cell (Action Tags Section)</span></span>

<span data-ttu-id="7c772-104">Смещение по оси *x* для кнопки тега действия, связанной с точкой, которая определена ячейками X и Y.</span><span class="sxs-lookup"><span data-stu-id="7c772-104">The  *x*  -offset of the action tag button relative to the point defined by the X and Y cells.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7c772-105">В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами.</span><span class="sxs-lookup"><span data-stu-id="7c772-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="7c772-106">**Значение**</span><span class="sxs-lookup"><span data-stu-id="7c772-106">**Value**</span></span>|<span data-ttu-id="7c772-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7c772-107">**Description**</span></span>|<span data-ttu-id="7c772-108">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="7c772-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="7c772-109">нуль</span><span class="sxs-lookup"><span data-stu-id="7c772-109">0</span></span>  <br/> | <span data-ttu-id="7c772-110">Выравнивание по левому краю (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="7c772-110">Left justified (the default).</span></span>  <br/> |<span data-ttu-id="7c772-111">**visSmartTagXJustifyLeft**</span><span class="sxs-lookup"><span data-stu-id="7c772-111">**visSmartTagXJustifyLeft**</span></span> <br/> |
| <span data-ttu-id="7c772-112">1,1</span><span class="sxs-lookup"><span data-stu-id="7c772-112">1</span></span>  <br/> | <span data-ttu-id="7c772-113">Выравнивание по центру.</span><span class="sxs-lookup"><span data-stu-id="7c772-113">Centered.</span></span>  <br/> |<span data-ttu-id="7c772-114">**visSmartTagXJustifyCenter**</span><span class="sxs-lookup"><span data-stu-id="7c772-114">**visSmartTagXJustifyCenter**</span></span> <br/> |
| <span data-ttu-id="7c772-115">2</span><span class="sxs-lookup"><span data-stu-id="7c772-115">2</span></span>  <br/> | <span data-ttu-id="7c772-116">Выравнивание по правому краю.</span><span class="sxs-lookup"><span data-stu-id="7c772-116">Right justified.</span></span>  <br/> |<span data-ttu-id="7c772-117">**visSmartTagXJustifyRight**</span><span class="sxs-lookup"><span data-stu-id="7c772-117">**visSmartTagXJustifyRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c772-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="7c772-118">Remarks</span></span>

<span data-ttu-id="7c772-119">Ячейки X Justify и Y Justify указывают, где размещается кнопка тега действия по отношению к точке, определенной в ячейках X и Y.</span><span class="sxs-lookup"><span data-stu-id="7c772-119">The X Justify and Y Justify cells determine where the action tag button is placed in relation to the point defined in the X and Y cells.</span></span> 
  
<span data-ttu-id="7c772-120">Чтобы получить ссылку на ячейку X Justify по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="7c772-120">To get a reference to the X Justify cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7c772-121">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="7c772-121">Cell name:</span></span>  <br/> | <span data-ttu-id="7c772-122">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="7c772-122">SmartTags.</span></span>  <span data-ttu-id="7c772-123">*имя* .XJustify, где SmartTags.</span><span class="sxs-lookup"><span data-stu-id="7c772-123">*name*  .XJustify           where SmartTags.</span></span> <span data-ttu-id="7c772-124">*имя* — название строки тегов действий.</span><span class="sxs-lookup"><span data-stu-id="7c772-124">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="7c772-125">Чтобы получить ссылку на ячейку X Justify по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="7c772-125">To get a reference to the X Justify cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7c772-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="7c772-126">Section index:</span></span>  <br/> |<span data-ttu-id="7c772-127">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="7c772-127">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="7c772-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="7c772-128">Row index:</span></span>  <br/> |<span data-ttu-id="7c772-129">**visRowSmartTag** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="7c772-129">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="7c772-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="7c772-130">Cell index:</span></span>  <br/> |<span data-ttu-id="7c772-131">**visSmartTagXJustify**</span><span class="sxs-lookup"><span data-stu-id="7c772-131">**visSmartTagXJustify**</span></span> <br/> |
   

