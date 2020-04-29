---
title: TagName Cell (Actions Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60087
localization_priority: Normal
ms.assetid: e593e95d-f975-481d-69cd-619049d4427d
description: Содержит имя тега действия, с которым связано это действие.
ms.openlocfilehash: e7bf5db940934d168ac2adb86d05b0374b0fd265
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412718"
---
# <a name="tagname-cell-actions-section"></a><span data-ttu-id="21479-103">TagName Cell (Actions Section)</span><span class="sxs-lookup"><span data-stu-id="21479-103">TagName Cell (Actions Section)</span></span>

<span data-ttu-id="21479-104">Содержит имя тега действия, с которым связано это действие.</span><span class="sxs-lookup"><span data-stu-id="21479-104">Contains the name of the action tag that this action is associated with.</span></span>
  
> [!NOTE]
> <span data-ttu-id="21479-105">В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами.</span><span class="sxs-lookup"><span data-stu-id="21479-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="21479-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="21479-106">Remarks</span></span>

<span data-ttu-id="21479-107">Ячейка TagName в разделе "действия" работает вместе с ячейкой TagName в разделе "теги действий", чтобы связать тег действия с его действиями.</span><span class="sxs-lookup"><span data-stu-id="21479-107">The TagName cell in the Actions section works together with the TagName cell in the Action Tags section to associate an action tag with its actions.</span></span> 
  
- <span data-ttu-id="21479-108">Если ячейка TagName в строке Actions пустая, действие отображается в контекстном меню, а не в меню тегов действий.</span><span class="sxs-lookup"><span data-stu-id="21479-108">If the TagName cell in an Actions row is blank, the action appears on a shortcut menu, not on an action tag menu.</span></span>
    
- <span data-ttu-id="21479-109">Если значение ячейки TagName в строке Actions соответствует значению ячейки TagName в строке смарт-тегов, действие будет отображаться в меню тегов действий.</span><span class="sxs-lookup"><span data-stu-id="21479-109">If a TagName cell value in the Actions row matches the TagName cell value in a Smart Tags row, the action appears on the action tag menu.</span></span>
    
- <span data-ttu-id="21479-110">Если ячейка TagName действия имеет значение, но не соответствует значению TagName в любой строке тега фигуры, это действие не отображается ни в одном меню тегов действий или контекстных меню.</span><span class="sxs-lookup"><span data-stu-id="21479-110">If an action's TagName cell has a value but it does not match the TagName value in any shape tag row, that action does not appear on any action tag menus or shortcut menus.</span></span>
    
- <span data-ttu-id="21479-111">Если несколько строк смарт-тегов имеют одинаковое значение TagName, все они будут отображать одни и те же действия.</span><span class="sxs-lookup"><span data-stu-id="21479-111">If several smart tag rows have the same TagName value, they will all show the same actions.</span></span>
    
<span data-ttu-id="21479-112">Чтобы получить ссылку на ячейку TagName по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="21479-112">To get a reference to the TagName cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="21479-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="21479-113">Cell name:</span></span>  <br/> |<span data-ttu-id="21479-114">Действия.</span><span class="sxs-lookup"><span data-stu-id="21479-114">Actions.</span></span> <span data-ttu-id="21479-115">*Name (имя* ). Действия Тагнамевхере.</span><span class="sxs-lookup"><span data-stu-id="21479-115">*name*  .TagNamewhere Actions.</span></span>  <span data-ttu-id="21479-116">*Name* — имя строки действий</span><span class="sxs-lookup"><span data-stu-id="21479-116">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="21479-117">Чтобы получить ссылку на ячейку TagName по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="21479-117">To get a reference to the TagName cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="21479-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="21479-118">Section index:</span></span>  <br/> |<span data-ttu-id="21479-119">**виссектионактион**</span><span class="sxs-lookup"><span data-stu-id="21479-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="21479-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="21479-120">Row index:</span></span>  <br/> |<span data-ttu-id="21479-121">**висровактион** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="21479-121">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="21479-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="21479-122">Cell index:</span></span>  <br/> |<span data-ttu-id="21479-123">**висактионтагнаме**</span><span class="sxs-lookup"><span data-stu-id="21479-123">**visActionTagName**</span></span> <br/> |
   

