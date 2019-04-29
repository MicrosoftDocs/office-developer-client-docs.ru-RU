---
title: Disabled Cell (Action Tags Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60038
localization_priority: Normal
ms.assetid: bf0a80c9-0fdb-e2cf-3ab0-74cb6338fdce
description: Указывает, отображается ли тег действия в окне документа.
ms.openlocfilehash: 867d36e27cb890509b0687500caf719362a711fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439669"
---
# <a name="disabled-cell-action-tags-section"></a><span data-ttu-id="b4bff-103">Disabled Cell (Action Tags Section)</span><span class="sxs-lookup"><span data-stu-id="b4bff-103">Disabled Cell (Action Tags Section)</span></span>

<span data-ttu-id="b4bff-104">Указывает, отображается ли тег действия в окне документа.</span><span class="sxs-lookup"><span data-stu-id="b4bff-104">Indicates whether the action tag appears in the drawing window.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b4bff-105">В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами.</span><span class="sxs-lookup"><span data-stu-id="b4bff-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="b4bff-106">**Значение**</span><span class="sxs-lookup"><span data-stu-id="b4bff-106">**Value**</span></span>|<span data-ttu-id="b4bff-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b4bff-107">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b4bff-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="b4bff-108">TRUE</span></span>  <br/> | <span data-ttu-id="b4bff-109">Тег действия отключен.</span><span class="sxs-lookup"><span data-stu-id="b4bff-109">The action tag is disabled.</span></span>  <br/> |
| <span data-ttu-id="b4bff-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="b4bff-110">FALSE</span></span>  <br/> | <span data-ttu-id="b4bff-111">Тег действия включен (значение по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="b4bff-111">The action tag is enabled (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4bff-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="b4bff-112">Remarks</span></span>

<span data-ttu-id="b4bff-113">Если тег действия отключен, он не отображается, пока он не будет повторно включен.</span><span class="sxs-lookup"><span data-stu-id="b4bff-113">When an action tag is disabled, it does not appear at all until it is re-enabled.</span></span> 
  
<span data-ttu-id="b4bff-114">Чтобы получить ссылку на отключенную ячейку по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="b4bff-114">To get a reference to the Disabled cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b4bff-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="b4bff-115">Cell name:</span></span>  <br/> | <span data-ttu-id="b4bff-116">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="b4bff-116">SmartTags.</span></span>  <span data-ttu-id="b4bff-117">*Name (имя* ). Отключено, где SmartTags.</span><span class="sxs-lookup"><span data-stu-id="b4bff-117">*name*  .Disabled           where SmartTags.</span></span> <span data-ttu-id="b4bff-118">*имя* — название строки тегов действий.</span><span class="sxs-lookup"><span data-stu-id="b4bff-118">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="b4bff-119">Чтобы получить ссылку на отключенную ячейку по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="b4bff-119">To get a reference to the Disabled cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b4bff-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b4bff-120">Section index:</span></span>  <br/> |<span data-ttu-id="b4bff-121">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="b4bff-121">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="b4bff-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b4bff-122">Row index:</span></span>  <br/> |<span data-ttu-id="b4bff-123">**visRowSmartTag** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="b4bff-123">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b4bff-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b4bff-124">Cell index:</span></span>  <br/> |<span data-ttu-id="b4bff-125">**Виссмарттагдисаблед**</span><span class="sxs-lookup"><span data-stu-id="b4bff-125">**visSmartTagDisabled**</span></span> <br/> |
   

