---
title: TextPosAfterBullet Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60089
localization_priority: Normal
ms.assetid: 08958abb-9d66-5a83-dac3-4cbfd1f6d85e
description: Представляет расстояние между первой строкой абзаца и маркером.
ms.openlocfilehash: a98967cb5f9541434745c3b3d6afafde0878074a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422154"
---
# <a name="textposafterbullet-cell-paragraph-section"></a><span data-ttu-id="4d5aa-103">TextPosAfterBullet Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="4d5aa-103">TextPosAfterBullet Cell (Paragraph Section)</span></span>

<span data-ttu-id="4d5aa-104">Представляет расстояние между первой строкой абзаца и маркером.</span><span class="sxs-lookup"><span data-stu-id="4d5aa-104">Represents the distance between the first line of the paragraph and the bullet.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4d5aa-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="4d5aa-105">Remarks</span></span>

<span data-ttu-id="4d5aa-106">Это расстояние добавляется к расстоянию, которое хранится в ячейке Индфирст по умолчанию в левом отступе.</span><span class="sxs-lookup"><span data-stu-id="4d5aa-106">This distance is added to the distance contained in the IndFirst cell, which is the default left indent.</span></span> <span data-ttu-id="4d5aa-107">Это значение не зависит от масштаба рисунка.</span><span class="sxs-lookup"><span data-stu-id="4d5aa-107">This value is independent of the scale of the drawing.</span></span> 
  
<span data-ttu-id="4d5aa-108">Чтобы получить ссылку на ячейку TextPosAfterBullet по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="4d5aa-108">To get a reference to the TextPosAfterBullet cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4d5aa-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="4d5aa-109">Cell name:</span></span>  <br/> | <span data-ttu-id="4d5aa-110">Para. TextPosAfterBullet [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="4d5aa-110">Para.TextPosAfterBullet[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="4d5aa-111">Чтобы получить ссылку на ячейку TextPosAfterBullet по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="4d5aa-111">To get a reference to the TextPosAfterBullet cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4d5aa-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="4d5aa-112">Section index:</span></span>  <br/> |<span data-ttu-id="4d5aa-113">**виссектионпараграф**</span><span class="sxs-lookup"><span data-stu-id="4d5aa-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="4d5aa-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="4d5aa-114">Row index:</span></span>  <br/> |<span data-ttu-id="4d5aa-115">**висровпараграф** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4d5aa-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="4d5aa-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="4d5aa-116">Cell index:</span></span>  <br/> |<span data-ttu-id="4d5aa-117">**вистекстпосафтербуллет**</span><span class="sxs-lookup"><span data-stu-id="4d5aa-117">**visTextPosAfterBullet**</span></span> <br/> |
   

