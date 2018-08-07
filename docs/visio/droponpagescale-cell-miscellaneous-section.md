---
title: Ячейка DropOnPageScale (раздел "Прочее")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60042
localization_priority: Normal
ms.assetid: 8927f811-7d8e-ed54-9eec-b86a781168dd
ms.openlocfilehash: a586cca497e1ba04848142917a84c3aa8a25d081
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813649"
---
# <a name="droponpagescale-cell-miscellaneous-section"></a><span data-ttu-id="0e197-102">Ячейка DropOnPageScale (раздел "Прочее")</span><span class="sxs-lookup"><span data-stu-id="0e197-102">DropOnPageScale Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="0e197-103">Содержит процентную долю, с помощью которого масштабирования фигуры при удаленной на странице документа.</span><span class="sxs-lookup"><span data-stu-id="0e197-103">Contains the percentage by which a shape is scaled when dropped on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0e197-104">Замечания</span><span class="sxs-lookup"><span data-stu-id="0e197-104">Remarks</span></span>

<span data-ttu-id="0e197-105">В следующих двух случаях Visio масштабов фигур, чтобы они отображаются должным образом на странице документа:</span><span class="sxs-lookup"><span data-stu-id="0e197-105">In the following two cases, Visio scales shapes so that they appear appropriately on the drawing page:</span></span>
  
- <span data-ttu-id="0e197-106">При перетаскивании Ненормированный фигур в масштабируемого документы.</span><span class="sxs-lookup"><span data-stu-id="0e197-106">When unmeasured shapes are dropped onto scaled drawings.</span></span>
    
- <span data-ttu-id="0e197-107">При перетаскивании измеренное фигур в зависимым документы.</span><span class="sxs-lookup"><span data-stu-id="0e197-107">When measured shapes are dropped onto unscaled drawings.</span></span>
    
<span data-ttu-id="0e197-108">Процент в ячейке DropOnPageScale указывает коэффициент, с помощью которого Visio масштабируемая фигуры, либо копирование (\>100) или вниз (\<100).</span><span class="sxs-lookup"><span data-stu-id="0e197-108">The percentage in the DropOnPageScale cell indicates the factor by which Visio scaled the shape, either up (\>100) or down (\<100).</span></span> <span data-ttu-id="0e197-109">Можно использовать этот номер как коэффициент при расчете фиксированными значениями.</span><span class="sxs-lookup"><span data-stu-id="0e197-109">You can use this number as a factor when calculating hard-coded values.</span></span> 
  
<span data-ttu-id="0e197-110">Это значение равно 100% для измеренное фигур на масштабируемого документы или Ненормированный фигур на зависимым документы.</span><span class="sxs-lookup"><span data-stu-id="0e197-110">This value is 100% for measured shapes on scaled drawings or unmeasured shapes on unscaled drawings.</span></span> 
  
<span data-ttu-id="0e197-111">Чтобы получить ссылку на ячейку DropOnPageScale по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0e197-111">To get a reference to the DropOnPageScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0e197-112">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="0e197-112">Cell name:</span></span>  <br/> | <span data-ttu-id="0e197-113">DropOnPageScale</span><span class="sxs-lookup"><span data-stu-id="0e197-113">DropOnPageScale</span></span>  <br/> |
   
<span data-ttu-id="0e197-114">Для получения ссылки на ячейки DropOnPageScale по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="0e197-114">To get a reference to the DropOnPageScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0e197-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0e197-115">Section index:</span></span>  <br/> |<span data-ttu-id="0e197-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0e197-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0e197-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0e197-117">Row index:</span></span>  <br/> |<span data-ttu-id="0e197-118">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="0e197-118">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="0e197-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0e197-119">Cell index:</span></span>  <br/> |<span data-ttu-id="0e197-120">**visObjDropOnPageScale**</span><span class="sxs-lookup"><span data-stu-id="0e197-120">**visObjDropOnPageScale**</span></span> <br/> |
   

