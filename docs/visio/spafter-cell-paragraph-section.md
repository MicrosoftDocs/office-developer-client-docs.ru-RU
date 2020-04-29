---
title: SpAfter Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm960
localization_priority: Normal
ms.assetid: 2dd56ae5-300e-ba09-a73a-83c2b6c2a0ef
description: Определяет объем пространства, вставленного после каждого абзаца в блоке текста фигуры, в дополнение к любому пробелу из ячейки сплайна и, если это последний абзац в текстовом блоке, ячейка BottomMargin.
ms.openlocfilehash: 2b8fe7e2b0df09561d0db4367f917c8f4b71335d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439837"
---
# <a name="spafter-cell-paragraph-section"></a><span data-ttu-id="adb0a-103">SpAfter Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="adb0a-103">SpAfter Cell (Paragraph Section)</span></span>

<span data-ttu-id="adb0a-104">Определяет объем пространства, вставленного после каждого абзаца в блоке текста фигуры, в дополнение к любому пробелу из ячейки сплайна и, если это последний абзац в текстовом блоке, ячейка BottomMargin.</span><span class="sxs-lookup"><span data-stu-id="adb0a-104">Determines the amount of space inserted after each paragraph in the shape's text block, in addition to any space from the SpLine cell and, if it is the last paragraph in a text block, the BottomMargin cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="adb0a-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="adb0a-105">Remarks</span></span>

<span data-ttu-id="adb0a-106">Это значение не зависит от масштаба рисунка.</span><span class="sxs-lookup"><span data-stu-id="adb0a-106">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="adb0a-107">Если масштаб документа изменяется, пробел после параметра остается прежним.</span><span class="sxs-lookup"><span data-stu-id="adb0a-107">If the drawing is scaled, the Space After setting remains the same.</span></span>
  
<span data-ttu-id="adb0a-108">Чтобы получить ссылку на ячейку CellsU по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="adb0a-108">To get a reference to the SpAfter cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="adb0a-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="adb0a-109">Cell name:</span></span>  <br/> | <span data-ttu-id="adb0a-110">Para. "после [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="adb0a-110">Para.SpAfter[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="adb0a-111">Чтобы получить ссылку на ячейку CellsSRC по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="adb0a-111">To get a reference to the SpAfter cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="adb0a-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="adb0a-112">Section index:</span></span>  <br/> |<span data-ttu-id="adb0a-113">**виссектионпараграф**</span><span class="sxs-lookup"><span data-stu-id="adb0a-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="adb0a-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="adb0a-114">Row index:</span></span>  <br/> |<span data-ttu-id="adb0a-115">**висровпараграф** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="adb0a-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="adb0a-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="adb0a-116">Cell index:</span></span>  <br/> |<span data-ttu-id="adb0a-117">**висспацеафтер**</span><span class="sxs-lookup"><span data-stu-id="adb0a-117">**visSpaceAfter**</span></span> <br/> |
   

