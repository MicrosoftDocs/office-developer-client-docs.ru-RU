---
title: Brightness Cell (Image Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251608
localization_priority: Normal
ms.assetid: 5bb1cc81-f3fd-a835-1449-233dbd1a62b6
description: Регулирует яркость изображения bitmap. Уменьшение яркости изображения путем ввода значения от 0% до 49% или увеличения яркости путем ввода значения от 51% до 100%. Значение по умолчанию — 50%.
ms.openlocfilehash: ae1390d2db3adad86a8afcbeaff88172a841d030
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424793"
---
# <a name="brightness-cell-image-properties-section"></a><span data-ttu-id="9943b-105">Brightness Cell (Image Properties Section)</span><span class="sxs-lookup"><span data-stu-id="9943b-105">Brightness Cell (Image Properties Section)</span></span>

<span data-ttu-id="9943b-106">Регулирует яркость изображения bitmap.</span><span class="sxs-lookup"><span data-stu-id="9943b-106">Adjusts the brightness of a bitmap image.</span></span> <span data-ttu-id="9943b-107">Уменьшение яркости изображения путем ввода значения от 0% до 49% или увеличения яркости путем ввода значения от 51% до 100%.</span><span class="sxs-lookup"><span data-stu-id="9943b-107">Decrease brightness of an image by entering a value between 0% and 49%, or increase brightness by entering a value between 51% and 100%.</span></span> <span data-ttu-id="9943b-108">Значение по умолчанию — 50%.</span><span class="sxs-lookup"><span data-stu-id="9943b-108">The default value is 50%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9943b-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="9943b-109">Remarks</span></span>

<span data-ttu-id="9943b-110">Чтобы получить ссылку на ячейку Brightness по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="9943b-110">To get a reference to the Brightness cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9943b-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="9943b-111">Cell name:</span></span>  <br/> | <span data-ttu-id="9943b-112">Яркость</span><span class="sxs-lookup"><span data-stu-id="9943b-112">Brightness</span></span>  <br/> |
   
<span data-ttu-id="9943b-113">Чтобы получить ссылку на ячейку Brightness по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="9943b-113">To get a reference to the Brightness cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9943b-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="9943b-114">Section index:</span></span>  <br/> |<span data-ttu-id="9943b-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9943b-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9943b-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="9943b-116">Row index:</span></span>  <br/> |<span data-ttu-id="9943b-117">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="9943b-117">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="9943b-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="9943b-118">Cell index:</span></span>  <br/> |<span data-ttu-id="9943b-119">**visImageBrightness**</span><span class="sxs-lookup"><span data-stu-id="9943b-119">**visImageBrightness**</span></span> <br/> |
   

