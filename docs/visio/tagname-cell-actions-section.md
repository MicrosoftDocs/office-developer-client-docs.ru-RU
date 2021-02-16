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
description: Содержит имя тега действия, с помощью которого связано это действие.
ms.openlocfilehash: e7bf5db940934d168ac2adb86d05b0374b0fd265
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412718"
---
# <a name="tagname-cell-actions-section"></a><span data-ttu-id="7ce12-103">TagName Cell (Actions Section)</span><span class="sxs-lookup"><span data-stu-id="7ce12-103">TagName Cell (Actions Section)</span></span>

<span data-ttu-id="7ce12-104">Содержит имя тега действия, с помощью которого связано это действие.</span><span class="sxs-lookup"><span data-stu-id="7ce12-104">Contains the name of the action tag that this action is associated with.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7ce12-105">В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами.</span><span class="sxs-lookup"><span data-stu-id="7ce12-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7ce12-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="7ce12-106">Remarks</span></span>

<span data-ttu-id="7ce12-107">Ячейка TagName в разделе "Действия" работает вместе с ячейкой TagName в разделе "Теги действий", чтобы связать тег действия с его действиями.</span><span class="sxs-lookup"><span data-stu-id="7ce12-107">The TagName cell in the Actions section works together with the TagName cell in the Action Tags section to associate an action tag with its actions.</span></span> 
  
- <span data-ttu-id="7ce12-108">Если ячейка TagName в строке "Действия" пуста, действие отображается в меню ярлыка, а не в меню тегов действий.</span><span class="sxs-lookup"><span data-stu-id="7ce12-108">If the TagName cell in an Actions row is blank, the action appears on a shortcut menu, not on an action tag menu.</span></span>
    
- <span data-ttu-id="7ce12-109">Если значение ячейки TagName в строке Actions совпадает со значением ячейки TagName в строке смарт-тегов, действие отображается в меню тегов действий.</span><span class="sxs-lookup"><span data-stu-id="7ce12-109">If a TagName cell value in the Actions row matches the TagName cell value in a Smart Tags row, the action appears on the action tag menu.</span></span>
    
- <span data-ttu-id="7ce12-110">Если ячейка TagName действия имеет значение, но не соответствует значению TagName ни в одной строке тегов фигуры, это действие не появляется ни в каких меню тегов действий или в сочетаниях клавиш.</span><span class="sxs-lookup"><span data-stu-id="7ce12-110">If an action's TagName cell has a value but it does not match the TagName value in any shape tag row, that action does not appear on any action tag menus or shortcut menus.</span></span>
    
- <span data-ttu-id="7ce12-111">Если несколько строк смарт-тегов имеют одинаковое значение TagName, все они будут показывать одинаковые действия.</span><span class="sxs-lookup"><span data-stu-id="7ce12-111">If several smart tag rows have the same TagName value, they will all show the same actions.</span></span>
    
<span data-ttu-id="7ce12-112">Чтобы получить ссылку на ячейку TagName по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="7ce12-112">To get a reference to the TagName cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7ce12-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="7ce12-113">Cell name:</span></span>  <br/> |<span data-ttu-id="7ce12-114">Действия.</span><span class="sxs-lookup"><span data-stu-id="7ce12-114">Actions.</span></span> <span data-ttu-id="7ce12-115">*name*  . Действия TagNamewhere.</span><span class="sxs-lookup"><span data-stu-id="7ce12-115">*name*  .TagNamewhere Actions.</span></span>  <span data-ttu-id="7ce12-116">*имя*  — это имя строки "Действия"</span><span class="sxs-lookup"><span data-stu-id="7ce12-116">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="7ce12-117">Чтобы получить ссылку на ячейку TagName по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="7ce12-117">To get a reference to the TagName cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7ce12-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="7ce12-118">Section index:</span></span>  <br/> |<span data-ttu-id="7ce12-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="7ce12-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="7ce12-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="7ce12-120">Row index:</span></span>  <br/> |<span data-ttu-id="7ce12-121">**visRowAction**  +   *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7ce12-121">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="7ce12-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="7ce12-122">Cell index:</span></span>  <br/> |<span data-ttu-id="7ce12-123">**visActionTagName**</span><span class="sxs-lookup"><span data-stu-id="7ce12-123">**visActionTagName**</span></span> <br/> |
   

