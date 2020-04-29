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
description: Задает поле справа от печатной страницы.
ms.openlocfilehash: d30669626fe07379521d61554010ae1bd7b0e83a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33440012"
---
# <a name="pagerightmargin-cell-print-properties-section"></a><span data-ttu-id="b5ec1-103">PageRightMargin Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="b5ec1-103">PageRightMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="b5ec1-104">Задает поле справа от печатной страницы.</span><span class="sxs-lookup"><span data-stu-id="b5ec1-104">Specifies the margin on the right of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b5ec1-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="b5ec1-105">Remarks</span></span>

<span data-ttu-id="b5ec1-106">Это значение представляет физические единицы и не затронет единицы масштабирования или рисования.</span><span class="sxs-lookup"><span data-stu-id="b5ec1-106">This value represents physical units and is unaffected by scale or drawing units.</span></span> <span data-ttu-id="b5ec1-107">Например, если ячейка имеет значение 0,25 в., это поле составляет 0,25 дюйма, даже если единицы страницы — футы.</span><span class="sxs-lookup"><span data-stu-id="b5ec1-107">For example, if this cell has a value of 0.25 in., this margin is 0.25 inch even if page units are feet.</span></span> <span data-ttu-id="b5ec1-108">Если единицы измерения не заданы явным образом, значение по умолчанию равно единицам страницы.</span><span class="sxs-lookup"><span data-stu-id="b5ec1-108">If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="b5ec1-109">Чтобы получить ссылку на ячейку PageRightMargin по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="b5ec1-109">To get a reference to the PageRightMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b5ec1-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="b5ec1-110">Cell name:</span></span>  <br/> | <span data-ttu-id="b5ec1-111">PageRightMargin</span><span class="sxs-lookup"><span data-stu-id="b5ec1-111">PageRightMargin</span></span>  <br/> |
   
<span data-ttu-id="b5ec1-112">Чтобы получить ссылку на ячейку PageRightMargin по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="b5ec1-112">To get a reference to the PageRightMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b5ec1-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b5ec1-113">Section index:</span></span>  <br/> |<span data-ttu-id="b5ec1-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b5ec1-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b5ec1-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b5ec1-115">Row index:</span></span>  <br/> |<span data-ttu-id="b5ec1-116">**висровпринтпропертиес**</span><span class="sxs-lookup"><span data-stu-id="b5ec1-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="b5ec1-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b5ec1-117">Cell index:</span></span>  <br/> |<span data-ttu-id="b5ec1-118">**виспринтпропертиесригхтмаргин**</span><span class="sxs-lookup"><span data-stu-id="b5ec1-118">**visPrintPropertiesRightMargin**</span></span> <br/> |
   

