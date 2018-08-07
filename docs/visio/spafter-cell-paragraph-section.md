---
title: Ячейка SpAfter (раздел "Абзац")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm960
localization_priority: Normal
ms.assetid: 2dd56ae5-300e-ba09-a73a-83c2b6c2a0ef
description: Определяет дискового пространства вставленный после каждого абзаца в блоке текста фигуры пробелов из ячейки сплайн и, если он установлен в последний абзац текстового заблокировать, BottomMargin ячейки.
ms.openlocfilehash: 93db93e58124b5f176fb57f843580eff6a3d4d3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814950"
---
# <a name="spafter-cell-paragraph-section"></a><span data-ttu-id="2b2b0-103">Ячейка SpAfter (раздел "Абзац")</span><span class="sxs-lookup"><span data-stu-id="2b2b0-103">SpAfter Cell (Paragraph Section)</span></span>

<span data-ttu-id="2b2b0-104">Определяет дискового пространства вставленный после каждого абзаца в блоке текста фигуры пробелов из ячейки сплайн и, если он установлен в последний абзац текстового заблокировать, BottomMargin ячейки.</span><span class="sxs-lookup"><span data-stu-id="2b2b0-104">Determines the amount of space inserted after each paragraph in the shape's text block, in addition to any space from the SpLine cell and, if it is the last paragraph in a text block, the BottomMargin cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2b2b0-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="2b2b0-105">Remarks</span></span>

<span data-ttu-id="2b2b0-106">Это значение не зависит от масштаба документа.</span><span class="sxs-lookup"><span data-stu-id="2b2b0-106">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="2b2b0-107">Если документа изменяется, пространство после параметр остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="2b2b0-107">If the drawing is scaled, the Space After setting remains the same.</span></span>
  
<span data-ttu-id="2b2b0-108">Чтобы получить ссылку на ячейку SpAfter по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="2b2b0-108">To get a reference to the SpAfter cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2b2b0-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="2b2b0-109">Cell name:</span></span>  <br/> | <span data-ttu-id="2b2b0-110">Para.SpAfter [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="2b2b0-110">Para.SpAfter[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="2b2b0-111">Для получения ссылки на ячейки SpAfter по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="2b2b0-111">To get a reference to the SpAfter cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2b2b0-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="2b2b0-112">Section index:</span></span>  <br/> |<span data-ttu-id="2b2b0-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="2b2b0-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="2b2b0-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="2b2b0-114">Row index:</span></span>  <br/> |<span data-ttu-id="2b2b0-115">**visRowParagraph** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2b2b0-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="2b2b0-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="2b2b0-116">Cell index:</span></span>  <br/> |<span data-ttu-id="2b2b0-117">**visSpaceAfter**</span><span class="sxs-lookup"><span data-stu-id="2b2b0-117">**visSpaceAfter**</span></span> <br/> |
   

