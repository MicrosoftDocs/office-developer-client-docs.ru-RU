---
title: HideText Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251323
localization_priority: Normal
ms.assetid: 3d23647a-e567-da71-50df-336a0f2f4071
description: Скрывает текст фигуры. Вы можете просматривать текст, изменять свойства и применять стили к тексту в текстовом блоке, хотя изменения не будут отображаться, пока не будет сброшено состояние HideText в false (0).
ms.openlocfilehash: 3e1be814984ed15247c451f5cd86d0f7a6dba71a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425486"
---
# <a name="hidetext-cell-miscellaneous-section"></a><span data-ttu-id="3937d-104">HideText Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="3937d-104">HideText Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="3937d-105">Скрывает текст фигуры.</span><span class="sxs-lookup"><span data-stu-id="3937d-105">Hides the text for a shape.</span></span> <span data-ttu-id="3937d-106">Вы можете просматривать текст, изменять свойства и применять стили к тексту в текстовом блоке, хотя изменения не будут отображаться, пока не будет сброшено состояние HideText в false (0).</span><span class="sxs-lookup"><span data-stu-id="3937d-106">You can view text, edit properties, and apply styles to the text in the text block, although the changes will not appear until you reset HideText to FALSE (0).</span></span>
  
|<span data-ttu-id="3937d-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="3937d-107">**Value**</span></span>|<span data-ttu-id="3937d-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3937d-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3937d-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="3937d-109">TRUE</span></span>  <br/> | <span data-ttu-id="3937d-110">Текст скрыт и не печатается.</span><span class="sxs-lookup"><span data-stu-id="3937d-110">Text is hidden and does not print.</span></span>  <br/> |
| <span data-ttu-id="3937d-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="3937d-111">FALSE</span></span>  <br/> | <span data-ttu-id="3937d-112">Текст не скрыт.</span><span class="sxs-lookup"><span data-stu-id="3937d-112">Text is not hidden.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3937d-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="3937d-113">Remarks</span></span>

<span data-ttu-id="3937d-114">Чтобы получить ссылку на ячейку HideText по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="3937d-114">To get a reference to the HideText cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3937d-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="3937d-115">Cell name:</span></span>  <br/> | <span data-ttu-id="3937d-116">HideText</span><span class="sxs-lookup"><span data-stu-id="3937d-116">HideText</span></span>  <br/> |
   
<span data-ttu-id="3937d-117">Чтобы получить ссылку на ячейку HideText по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="3937d-117">To get a reference to the HideText cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3937d-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="3937d-118">Section index:</span></span>  <br/> |<span data-ttu-id="3937d-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3937d-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3937d-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="3937d-120">Row index:</span></span>  <br/> |<span data-ttu-id="3937d-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="3937d-121">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="3937d-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="3937d-122">Cell index:</span></span>  <br/> |<span data-ttu-id="3937d-123">**visHideText**</span><span class="sxs-lookup"><span data-stu-id="3937d-123">**visHideText**</span></span> <br/> |
   

