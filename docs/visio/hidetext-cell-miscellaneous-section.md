---
title: Ячейка HideText (раздел "Прочее")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251323
localization_priority: Normal
ms.assetid: 3d23647a-e567-da71-50df-336a0f2f4071
description: Скрывает текст фигуры. Можно просматривать текст, измените свойства и применить стили для текста в блоке текста, несмотря на то, что изменения не будут отображаться, пока не будет сброшен HideText значение FALSE (0).
ms.openlocfilehash: e2d220e9d7874382f2aaeade5488bd4809f3a9dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813913"
---
# <a name="hidetext-cell-miscellaneous-section"></a><span data-ttu-id="fca5a-104">Ячейка HideText (раздел "Прочее")</span><span class="sxs-lookup"><span data-stu-id="fca5a-104">HideText Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="fca5a-105">Скрывает текст фигуры.</span><span class="sxs-lookup"><span data-stu-id="fca5a-105">Hides the text for a shape.</span></span> <span data-ttu-id="fca5a-106">Можно просматривать текст, измените свойства и применить стили для текста в блоке текста, несмотря на то, что изменения не будут отображаться, пока не будет сброшен HideText значение FALSE (0).</span><span class="sxs-lookup"><span data-stu-id="fca5a-106">You can view text, edit properties, and apply styles to the text in the text block, although the changes will not appear until you reset HideText to FALSE (0).</span></span>
  
|<span data-ttu-id="fca5a-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="fca5a-107">**Value**</span></span>|<span data-ttu-id="fca5a-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fca5a-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="fca5a-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="fca5a-109">TRUE</span></span>  <br/> | <span data-ttu-id="fca5a-110">Текст скрыто и не печатается.</span><span class="sxs-lookup"><span data-stu-id="fca5a-110">Text is hidden and does not print.</span></span>  <br/> |
| <span data-ttu-id="fca5a-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="fca5a-111">FALSE</span></span>  <br/> | <span data-ttu-id="fca5a-112">Текст не скрывается.</span><span class="sxs-lookup"><span data-stu-id="fca5a-112">Text is not hidden.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fca5a-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="fca5a-113">Remarks</span></span>

<span data-ttu-id="fca5a-114">Для получения ссылки на ячейки HideText по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="fca5a-114">To get a reference to the HideText cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fca5a-115">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="fca5a-115">Cell name:</span></span>  <br/> | <span data-ttu-id="fca5a-116">HideText</span><span class="sxs-lookup"><span data-stu-id="fca5a-116">HideText</span></span>  <br/> |
   
<span data-ttu-id="fca5a-117">Для получения ссылки на ячейки HideText по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="fca5a-117">To get a reference to the HideText cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fca5a-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="fca5a-118">Section index:</span></span>  <br/> |<span data-ttu-id="fca5a-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fca5a-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fca5a-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="fca5a-120">Row index:</span></span>  <br/> |<span data-ttu-id="fca5a-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="fca5a-121">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="fca5a-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="fca5a-122">Cell index:</span></span>  <br/> |<span data-ttu-id="fca5a-123">**visHideText**</span><span class="sxs-lookup"><span data-stu-id="fca5a-123">**visHideText**</span></span> <br/> |
   

