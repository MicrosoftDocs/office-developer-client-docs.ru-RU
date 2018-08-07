---
title: Ячейка SpBefore (раздел "Абзац")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm965
localization_priority: Normal
ms.assetid: a7d5b0a1-3657-8211-f0e0-eaed588fa0bc
description: Определяет объем пространства, перед каждым абзацем в блоке текста фигуры пробелов из ячейки сплайн, если это первый абзац в блоке текста в ячейку TopMargin.
ms.openlocfilehash: d33a10220499020ba1a1acedf5782fdb78925c07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814927"
---
# <a name="spbefore-cell-paragraph-section"></a><span data-ttu-id="d816f-103">Ячейка SpBefore (раздел "Абзац")</span><span class="sxs-lookup"><span data-stu-id="d816f-103">SpBefore Cell (Paragraph Section)</span></span>

<span data-ttu-id="d816f-104">Определяет объем пространства, перед каждым абзацем в блоке текста фигуры пробелов из ячейки сплайн, если это первый абзац в блоке текста в ячейку TopMargin.</span><span class="sxs-lookup"><span data-stu-id="d816f-104">Determines the amount of space inserted before each paragraph in the shape's text block, in addition to any space from the SpLine cell if it is the first paragraph in a text block, the TopMargin cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d816f-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="d816f-105">Remarks</span></span>

<span data-ttu-id="d816f-106">Это значение не зависит от масштаба документа.</span><span class="sxs-lookup"><span data-stu-id="d816f-106">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="d816f-107">Если документа изменяется, пространство перед параметр остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="d816f-107">If the drawing is scaled, the Space Before setting remains the same.</span></span>
  
<span data-ttu-id="d816f-108">Чтобы получить ссылку на ячейку SpBefore по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d816f-108">To get a reference to the SpBefore cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d816f-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="d816f-109">Cell name:</span></span>  <br/> | <span data-ttu-id="d816f-110">Para.SpBefore [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d816f-110">Para.SpBefore[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d816f-111">Для получения ссылки на ячейки SpBefore по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="d816f-111">To get a reference to the SpBefore cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d816f-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d816f-112">Section index:</span></span>  <br/> |<span data-ttu-id="d816f-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="d816f-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="d816f-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d816f-114">Row index:</span></span>  <br/> |<span data-ttu-id="d816f-115">**visRowParagraph** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d816f-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d816f-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d816f-116">Cell index:</span></span>  <br/> |<span data-ttu-id="d816f-117">**visSpaceBefore**</span><span class="sxs-lookup"><span data-stu-id="d816f-117">**visSpaceBefore**</span></span> <br/> |
   

