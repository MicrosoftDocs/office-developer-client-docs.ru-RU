---
title: DropOnPageScale Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60042
localization_priority: Normal
ms.assetid: 8927f811-7d8e-ed54-9eec-b86a781168dd
ms.openlocfilehash: 17c597df3d9e7e741d902fd566cc9a5de1f31ea0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359663"
---
# <a name="droponpagescale-cell-miscellaneous-section"></a><span data-ttu-id="fa499-102">DropOnPageScale Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="fa499-102">DropOnPageScale Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="fa499-103">Содержит процентное значение, на которое масштабирована фигура при удалении на странице документа.</span><span class="sxs-lookup"><span data-stu-id="fa499-103">Contains the percentage by which a shape is scaled when dropped on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fa499-104">Примечания</span><span class="sxs-lookup"><span data-stu-id="fa499-104">Remarks</span></span>

<span data-ttu-id="fa499-105">В следующих двух случаях Visio масштабирует фигуры таким образом, чтобы они правильно отображались на странице документа:</span><span class="sxs-lookup"><span data-stu-id="fa499-105">In the following two cases, Visio scales shapes so that they appear appropriately on the drawing page:</span></span>
  
- <span data-ttu-id="fa499-106">При перетаскивании неизмеренных фигур на масштабируемые рисунки.</span><span class="sxs-lookup"><span data-stu-id="fa499-106">When unmeasured shapes are dropped onto scaled drawings.</span></span>
    
- <span data-ttu-id="fa499-107">При отбрасывания измерений фигуры отправляются на немасштабированные рисунки.</span><span class="sxs-lookup"><span data-stu-id="fa499-107">When measured shapes are dropped onto unscaled drawings.</span></span>
    
<span data-ttu-id="fa499-108">Процент в ячейке DropOnPageScale указывает коэффициент, на который Visio Масштабирует фигуру (\>100) или вниз (\<100).</span><span class="sxs-lookup"><span data-stu-id="fa499-108">The percentage in the DropOnPageScale cell indicates the factor by which Visio scaled the shape, either up (\>100) or down (\<100).</span></span> <span data-ttu-id="fa499-109">Этот номер можно использовать как фактор при расчете жестко запрограммированных значений.</span><span class="sxs-lookup"><span data-stu-id="fa499-109">You can use this number as a factor when calculating hard-coded values.</span></span> 
  
<span data-ttu-id="fa499-110">Это значение равно 100% для измеренных фигур на масштабированных рисунках или неизмеренных фигур на немасштабированных рисунках.</span><span class="sxs-lookup"><span data-stu-id="fa499-110">This value is 100% for measured shapes on scaled drawings or unmeasured shapes on unscaled drawings.</span></span> 
  
<span data-ttu-id="fa499-111">Чтобы получить ссылку на ячейку DropOnPageScale по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="fa499-111">To get a reference to the DropOnPageScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fa499-112">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="fa499-112">Cell name:</span></span>  <br/> | <span data-ttu-id="fa499-113">DropOnPageScale</span><span class="sxs-lookup"><span data-stu-id="fa499-113">DropOnPageScale</span></span>  <br/> |
   
<span data-ttu-id="fa499-114">Чтобы получить ссылку на ячейку DropOnPageScale по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="fa499-114">To get a reference to the DropOnPageScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fa499-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="fa499-115">Section index:</span></span>  <br/> |<span data-ttu-id="fa499-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fa499-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fa499-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="fa499-117">Row index:</span></span>  <br/> |<span data-ttu-id="fa499-118">**Висровмиск**</span><span class="sxs-lookup"><span data-stu-id="fa499-118">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="fa499-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="fa499-119">Cell index:</span></span>  <br/> |<span data-ttu-id="fa499-120">**Висобждропонпажескале**</span><span class="sxs-lookup"><span data-stu-id="fa499-120">**visObjDropOnPageScale**</span></span> <br/> |
   

