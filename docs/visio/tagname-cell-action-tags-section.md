---
title: Ячейка TagName (раздел "Теги действий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60088
localization_priority: Normal
ms.assetid: 28d1cd60-4fb6-9feb-1a13-0962798ac1ad
description: Имя тега действия, который используется в качестве ключа для связывания тега действия с его действиями.
ms.openlocfilehash: dbac3d4dff9d2ffd18bba75db56cafc08f5e0ee8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814980"
---
# <a name="tagname-cell-action-tags-section"></a><span data-ttu-id="a88fc-103">Ячейка TagName (раздел "Теги действий")</span><span class="sxs-lookup"><span data-stu-id="a88fc-103">TagName Cell (Action Tags Section)</span></span>

<span data-ttu-id="a88fc-104">Имя тега действия, который используется в качестве ключа для связывания тега действия с его действиями.</span><span class="sxs-lookup"><span data-stu-id="a88fc-104">Name of the action tag that is used as a key to associate the action tag with its actions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a88fc-105">В предыдущих версиях Microsoft Visio теги действий, называются смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="a88fc-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a88fc-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="a88fc-106">Remarks</span></span>

 <span data-ttu-id="a88fc-107">Ячейка TagName в разделе Действие тегов работает вместе с TagName ячейки в разделе действия, чтобы связать тег действия с его действиями.</span><span class="sxs-lookup"><span data-stu-id="a88fc-107">The TagName cell in the Action Tags section works together with the TagName cell in the Actions section to associate an action tag with its actions.</span></span> <span data-ttu-id="a88fc-108">Строки в разделе действия также TagName ячейки, и эти строки с тем же значением ячейки TagName как этой ячейке определения действий, выполняемых для этого тега действия.</span><span class="sxs-lookup"><span data-stu-id="a88fc-108">Rows in the Actions section also have a TagName cell, and those rows with the same TagName cell value as this cell define actions to take for this action tag.</span></span> 
  
<span data-ttu-id="a88fc-109">Чтобы получить ссылку на ячейку TagName по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="a88fc-109">To get a reference to the TagName cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a88fc-110">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="a88fc-110">Cell name:</span></span>  <br/> | <span data-ttu-id="a88fc-111">Смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="a88fc-111">SmartTags.</span></span>  <span data-ttu-id="a88fc-112">*имя* . TagName где смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="a88fc-112">*name*  .TagName           where SmartTags.</span></span> <span data-ttu-id="a88fc-113">*имя* — это имя строки тега действия</span><span class="sxs-lookup"><span data-stu-id="a88fc-113">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="a88fc-114">Для получения ссылки на ячейки TagName по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="a88fc-114">To get a reference to the TagName cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a88fc-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a88fc-115">Section index:</span></span>  <br/> |<span data-ttu-id="a88fc-116">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="a88fc-116">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="a88fc-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a88fc-117">Row index:</span></span>  <br/> |<span data-ttu-id="a88fc-118">**visRowSmartTag** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a88fc-118">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a88fc-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a88fc-119">Cell index:</span></span>  <br/> |<span data-ttu-id="a88fc-120">**visSmartTagName**</span><span class="sxs-lookup"><span data-stu-id="a88fc-120">**visSmartTagName**</span></span> <br/> |
   

