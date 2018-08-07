---
title: Ячейка TagName (раздел "Действия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60087
localization_priority: Normal
ms.assetid: e593e95d-f975-481d-69cd-619049d4427d
description: Содержит имя тега действия, с которым связана это действие.
ms.openlocfilehash: e1495a34769cbcfdd687491855d1f9c761de2b4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814996"
---
# <a name="tagname-cell-actions-section"></a><span data-ttu-id="fe479-103">Ячейка TagName (раздел "Действия")</span><span class="sxs-lookup"><span data-stu-id="fe479-103">TagName Cell (Actions Section)</span></span>

<span data-ttu-id="fe479-104">Содержит имя тега действия, с которым связана это действие.</span><span class="sxs-lookup"><span data-stu-id="fe479-104">Contains the name of the action tag that this action is associated with.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fe479-105">В предыдущих версиях Microsoft Visio теги действий, называются смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="fe479-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fe479-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="fe479-106">Remarks</span></span>

<span data-ttu-id="fe479-107">Ячейка TagName в разделе действия работает вместе с TagName ячейки в разделе теги действий, чтобы связать тег действия с его действиями.</span><span class="sxs-lookup"><span data-stu-id="fe479-107">The TagName cell in the Actions section works together with the TagName cell in the Action Tags section to associate an action tag with its actions.</span></span> 
  
- <span data-ttu-id="fe479-108">Если ячейка TagName в строки действий не задан, отображается действие в контекстном меню выберите не в меню Действие тега.</span><span class="sxs-lookup"><span data-stu-id="fe479-108">If the TagName cell in an Actions row is blank, the action appears on a shortcut menu, not on an action tag menu.</span></span>
    
- <span data-ttu-id="fe479-109">Если значение ячейки TagName в строке действия совпадает со значением TagName ячейки в строке смарт-тегов, тегов в меню Действие отображается действие.</span><span class="sxs-lookup"><span data-stu-id="fe479-109">If a TagName cell value in the Actions row matches the TagName cell value in a Smart Tags row, the action appears on the action tag menu.</span></span>
    
- <span data-ttu-id="fe479-110">Если ячейка TagName действия имеет значение, но не соответствует значение TagName в любой строке тег фигуры, это действие не отображается на любой тег действие или контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="fe479-110">If an action's TagName cell has a value but it does not match the TagName value in any shape tag row, that action does not appear on any action tag menus or shortcut menus.</span></span>
    
- <span data-ttu-id="fe479-111">Если несколько строк смарт-тег с таким же TagName значением, они будут отображать те же действия.</span><span class="sxs-lookup"><span data-stu-id="fe479-111">If several smart tag rows have the same TagName value, they will all show the same actions.</span></span>
    
<span data-ttu-id="fe479-112">Для получения ссылки на ячейки TagName по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="fe479-112">To get a reference to the TagName cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fe479-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="fe479-113">Cell name:</span></span>  <br/> |<span data-ttu-id="fe479-114">Действия.</span><span class="sxs-lookup"><span data-stu-id="fe479-114">Actions.</span></span> <span data-ttu-id="fe479-115">*имя* . TagNamewhere действия.</span><span class="sxs-lookup"><span data-stu-id="fe479-115">*name*  .TagNamewhere Actions.</span></span>  <span data-ttu-id="fe479-116">*имя* — это имя строки действий</span><span class="sxs-lookup"><span data-stu-id="fe479-116">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="fe479-117">Для получения ссылки на ячейки TagName по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="fe479-117">To get a reference to the TagName cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fe479-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="fe479-118">Section index:</span></span>  <br/> |<span data-ttu-id="fe479-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="fe479-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="fe479-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="fe479-120">Row index:</span></span>  <br/> |<span data-ttu-id="fe479-121">**visRowAction** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="fe479-121">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="fe479-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="fe479-122">Cell index:</span></span>  <br/> |<span data-ttu-id="fe479-123">**visActionTagName**</span><span class="sxs-lookup"><span data-stu-id="fe479-123">**visActionTagName**</span></span> <br/> |
   

