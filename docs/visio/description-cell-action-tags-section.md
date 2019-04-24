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
description: Содержит строку, описывающую тег действия, который отображается как всплывающая подсказка, когда пользователь наводит указатель мыши на тег.
ms.openlocfilehash: 00c7a4c1547927b8d1a979b8ae074f96f26dc17c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360234"
---
# <a name="description-cell-action-tags-section"></a><span data-ttu-id="61a3f-103">Description Cell (Action Tags Section)</span><span class="sxs-lookup"><span data-stu-id="61a3f-103">Description Cell (Action Tags Section)</span></span>

<span data-ttu-id="61a3f-104">Содержит строку, описывающую тег действия, который отображается как всплывающая подсказка, когда пользователь наводит указатель мыши на тег.</span><span class="sxs-lookup"><span data-stu-id="61a3f-104">Contains a string that describes the action tag, which appears as a tool tip when users place their pointer over the tag.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="61a3f-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="61a3f-105">Remarks</span></span>

<span data-ttu-id="61a3f-106">Чтобы получить ссылку на ячейку Description по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="61a3f-106">To get a reference to the Description cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="61a3f-107">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="61a3f-107">Cell name:</span></span>  <br/> | <span data-ttu-id="61a3f-108">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="61a3f-108">SmartTags.</span></span>  <span data-ttu-id="61a3f-109">*Name (имя* ). Description, где SmartTags.</span><span class="sxs-lookup"><span data-stu-id="61a3f-109">*name*  .Description           where SmartTags.</span></span> <span data-ttu-id="61a3f-110">*имя* — название строки тегов действий.</span><span class="sxs-lookup"><span data-stu-id="61a3f-110">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="61a3f-111">Чтобы получить ссылку на ячейку Description по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="61a3f-111">To get a reference to the Description cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="61a3f-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="61a3f-112">Section index:</span></span>  <br/> |<span data-ttu-id="61a3f-113">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="61a3f-113">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="61a3f-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="61a3f-114">Row index:</span></span>  <br/> |<span data-ttu-id="61a3f-115">**visRowSmartTag** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="61a3f-115">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="61a3f-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="61a3f-116">Cell index:</span></span>  <br/> |<span data-ttu-id="61a3f-117">**Виссмарттагдескриптион**</span><span class="sxs-lookup"><span data-stu-id="61a3f-117">**visSmartTagDescription**</span></span> <br/> |
   

