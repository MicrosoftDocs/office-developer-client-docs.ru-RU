---
title: Description Cell (Action Tags Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60037
localization_priority: Normal
ms.assetid: feb29b91-0f6e-6353-3dd0-7a280843a517
description: Содержит строку, описываемую тегом действия, который отображается в качестве подсказки, когда пользователь нанося указатель на тег.
ms.openlocfilehash: 00c7a4c1547927b8d1a979b8ae074f96f26dc17c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415763"
---
# <a name="description-cell-action-tags-section"></a><span data-ttu-id="0affb-103">Description Cell (Action Tags Section)</span><span class="sxs-lookup"><span data-stu-id="0affb-103">Description Cell (Action Tags Section)</span></span>

<span data-ttu-id="0affb-104">Содержит строку, описываемую тегом действия, который отображается в качестве подсказки, когда пользователь нанося указатель на тег.</span><span class="sxs-lookup"><span data-stu-id="0affb-104">Contains a string that describes the action tag, which appears as a tool tip when users place their pointer over the tag.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0affb-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="0affb-105">Remarks</span></span>

<span data-ttu-id="0affb-106">Чтобы получить ссылку на ячейку Description по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="0affb-106">To get a reference to the Description cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0affb-107">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="0affb-107">Cell name:</span></span>  <br/> | <span data-ttu-id="0affb-108">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="0affb-108">SmartTags.</span></span>  <span data-ttu-id="0affb-109">*name*  . Описание, где smartTags.</span><span class="sxs-lookup"><span data-stu-id="0affb-109">*name*  .Description           where SmartTags.</span></span> <span data-ttu-id="0affb-110">*имя* — название строки тегов действий.</span><span class="sxs-lookup"><span data-stu-id="0affb-110">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="0affb-111">Чтобы получить ссылку на ячейку Description по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="0affb-111">To get a reference to the Description cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0affb-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0affb-112">Section index:</span></span>  <br/> |<span data-ttu-id="0affb-113">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="0affb-113">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="0affb-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0affb-114">Row index:</span></span>  <br/> |<span data-ttu-id="0affb-115">**visRowSmartTag** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="0affb-115">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="0affb-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0affb-116">Cell index:</span></span>  <br/> |<span data-ttu-id="0affb-117">**visSmartTagDescription**</span><span class="sxs-lookup"><span data-stu-id="0affb-117">**visSmartTagDescription**</span></span> <br/> |
   

