---
title: PageRightMargin Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60062
localization_priority: Normal
ms.assetid: f864c759-ed94-8ab7-d664-cc04b3ed743e
description: Указывает поле справа от печатной страницы.
ms.openlocfilehash: d30669626fe07379521d61554010ae1bd7b0e83a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33440012"
---
# <a name="pagerightmargin-cell-print-properties-section"></a><span data-ttu-id="ad998-103">PageRightMargin Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="ad998-103">PageRightMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="ad998-104">Указывает поле справа от печатной страницы.</span><span class="sxs-lookup"><span data-stu-id="ad998-104">Specifies the margin on the right of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ad998-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="ad998-105">Remarks</span></span>

<span data-ttu-id="ad998-106">Это значение представляет физические единицы и не влияет на масштаб или единицы рисования.</span><span class="sxs-lookup"><span data-stu-id="ad998-106">This value represents physical units and is unaffected by scale or drawing units.</span></span> <span data-ttu-id="ad998-107">Например, если значение этой ячейки составляет 0,25 дюйма, то это поле будет 0,25 дюйма, даже если единицы страниц находятся в метрах.</span><span class="sxs-lookup"><span data-stu-id="ad998-107">For example, if this cell has a value of 0.25 in., this margin is 0.25 inch even if page units are feet.</span></span> <span data-ttu-id="ad998-108">Если единицы не заявимы, это значение по умолчанию занося в единицы страниц.</span><span class="sxs-lookup"><span data-stu-id="ad998-108">If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="ad998-109">Чтобы получить ссылку на ячейку PageRightMargin по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="ad998-109">To get a reference to the PageRightMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ad998-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="ad998-110">Cell name:</span></span>  <br/> | <span data-ttu-id="ad998-111">PageRightMargin</span><span class="sxs-lookup"><span data-stu-id="ad998-111">PageRightMargin</span></span>  <br/> |
   
<span data-ttu-id="ad998-112">Чтобы получить ссылку на ячейку PageRightMargin по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="ad998-112">To get a reference to the PageRightMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ad998-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ad998-113">Section index:</span></span>  <br/> |<span data-ttu-id="ad998-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ad998-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ad998-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ad998-115">Row index:</span></span>  <br/> |<span data-ttu-id="ad998-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="ad998-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="ad998-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ad998-117">Cell index:</span></span>  <br/> |<span data-ttu-id="ad998-118">**visPrintPropertiesRightMargin**</span><span class="sxs-lookup"><span data-stu-id="ad998-118">**visPrintPropertiesRightMargin**</span></span> <br/> |
   

