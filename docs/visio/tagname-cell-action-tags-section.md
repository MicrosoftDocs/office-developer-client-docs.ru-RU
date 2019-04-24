---
title: TagName Cell (Action Tags Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60088
localization_priority: Normal
ms.assetid: 28d1cd60-4fb6-9feb-1a13-0962798ac1ad
description: Имя тега действия, используемого в качестве ключа для сопоставления тега действия с его действиями.
ms.openlocfilehash: 777d6c1098888c9835c1ad367bb70926b835180b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332398"
---
# <a name="tagname-cell-action-tags-section"></a><span data-ttu-id="38a34-103">TagName Cell (Action Tags Section)</span><span class="sxs-lookup"><span data-stu-id="38a34-103">TagName Cell (Action Tags Section)</span></span>

<span data-ttu-id="38a34-104">Имя тега действия, используемого в качестве ключа для сопоставления тега действия с его действиями.</span><span class="sxs-lookup"><span data-stu-id="38a34-104">Name of the action tag that is used as a key to associate the action tag with its actions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="38a34-105">В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами.</span><span class="sxs-lookup"><span data-stu-id="38a34-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="38a34-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="38a34-106">Remarks</span></span>

 <span data-ttu-id="38a34-107">Ячейка TagName в разделе "теги действий" работает вместе с ячейкой TagName в разделе "действия", чтобы связать тег действия с его действиями.</span><span class="sxs-lookup"><span data-stu-id="38a34-107">The TagName cell in the Action Tags section works together with the TagName cell in the Actions section to associate an action tag with its actions.</span></span> <span data-ttu-id="38a34-108">В строках раздела Actions также есть ячейка TagName, и эти строки с одинаковым значением ячейки TagName в этой ячейке определяют действия, выполняемые для этого тега действия.</span><span class="sxs-lookup"><span data-stu-id="38a34-108">Rows in the Actions section also have a TagName cell, and those rows with the same TagName cell value as this cell define actions to take for this action tag.</span></span> 
  
<span data-ttu-id="38a34-109">Чтобы получить ссылку на ячейку TagName по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="38a34-109">To get a reference to the TagName cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="38a34-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="38a34-110">Cell name:</span></span>  <br/> | <span data-ttu-id="38a34-111">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="38a34-111">SmartTags.</span></span>  <span data-ttu-id="38a34-112">*Name (имя* ). TagName, где SmartTags.</span><span class="sxs-lookup"><span data-stu-id="38a34-112">*name*  .TagName           where SmartTags.</span></span> <span data-ttu-id="38a34-113">*имя* — название строки тегов действий.</span><span class="sxs-lookup"><span data-stu-id="38a34-113">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="38a34-114">Чтобы получить ссылку на ячейку TagName по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="38a34-114">To get a reference to the TagName cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="38a34-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="38a34-115">Section index:</span></span>  <br/> |<span data-ttu-id="38a34-116">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="38a34-116">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="38a34-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="38a34-117">Row index:</span></span>  <br/> |<span data-ttu-id="38a34-118">**visRowSmartTag** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="38a34-118">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="38a34-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="38a34-119">Cell index:</span></span>  <br/> |<span data-ttu-id="38a34-120">**Виссмарттагнаме**</span><span class="sxs-lookup"><span data-stu-id="38a34-120">**visSmartTagName**</span></span> <br/> |
   

