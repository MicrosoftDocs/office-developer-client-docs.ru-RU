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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423764"
---
# <a name="droponpagescale-cell-miscellaneous-section"></a><span data-ttu-id="a783a-102">DropOnPageScale Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="a783a-102">DropOnPageScale Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="a783a-103">Содержит процент масштабирования фигуры при сброшении на страницу рисования.</span><span class="sxs-lookup"><span data-stu-id="a783a-103">Contains the percentage by which a shape is scaled when dropped on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a783a-104">Примечания</span><span class="sxs-lookup"><span data-stu-id="a783a-104">Remarks</span></span>

<span data-ttu-id="a783a-105">В следующих двух случаях Visio масштабировать фигуры таким образом, чтобы они надлежащим образом появлялись на странице рисования:</span><span class="sxs-lookup"><span data-stu-id="a783a-105">In the following two cases, Visio scales shapes so that they appear appropriately on the drawing page:</span></span>
  
- <span data-ttu-id="a783a-106">Если неизмеряемые фигуры сброшены на масштабные рисунки.</span><span class="sxs-lookup"><span data-stu-id="a783a-106">When unmeasured shapes are dropped onto scaled drawings.</span></span>
    
- <span data-ttu-id="a783a-107">Когда измеренные фигуры сброшены на немасштабные рисунки.</span><span class="sxs-lookup"><span data-stu-id="a783a-107">When measured shapes are dropped onto unscaled drawings.</span></span>
    
<span data-ttu-id="a783a-108">Процент в ячейке DropOnPageScale указывает на фактор, с помощью которого Visio масштабировать фигуру вверх \> (100) или вниз \< (100).</span><span class="sxs-lookup"><span data-stu-id="a783a-108">The percentage in the DropOnPageScale cell indicates the factor by which Visio scaled the shape, either up (\>100) or down (\<100).</span></span> <span data-ttu-id="a783a-109">Этот номер можно использовать в качестве фактора при вычислении значений с жесткой кодией.</span><span class="sxs-lookup"><span data-stu-id="a783a-109">You can use this number as a factor when calculating hard-coded values.</span></span> 
  
<span data-ttu-id="a783a-110">Это значение составляет 100% для измеренных фигур на масштабных рисунках или необмерных фигур на немасштабных рисунках.</span><span class="sxs-lookup"><span data-stu-id="a783a-110">This value is 100% for measured shapes on scaled drawings or unmeasured shapes on unscaled drawings.</span></span> 
  
<span data-ttu-id="a783a-111">Чтобы получить ссылку на ячейку DropOnPageScale по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="a783a-111">To get a reference to the DropOnPageScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a783a-112">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="a783a-112">Cell name:</span></span>  <br/> | <span data-ttu-id="a783a-113">DropOnPageScale</span><span class="sxs-lookup"><span data-stu-id="a783a-113">DropOnPageScale</span></span>  <br/> |
   
<span data-ttu-id="a783a-114">Чтобы получить ссылку на ячейку DropOnPageScale по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="a783a-114">To get a reference to the DropOnPageScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a783a-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a783a-115">Section index:</span></span>  <br/> |<span data-ttu-id="a783a-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a783a-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a783a-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a783a-117">Row index:</span></span>  <br/> |<span data-ttu-id="a783a-118">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="a783a-118">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="a783a-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a783a-119">Cell index:</span></span>  <br/> |<span data-ttu-id="a783a-120">**visObjDropOnPageScale**</span><span class="sxs-lookup"><span data-stu-id="a783a-120">**visObjDropOnPageScale**</span></span> <br/> |
   

