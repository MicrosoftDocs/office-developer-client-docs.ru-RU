---
title: PageLeftMargin Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60061
localization_priority: Normal
ms.assetid: 7ecdfc37-c9d4-2fde-ed3e-be81657c24e2
description: Указывает поле слева от печатаемой страницы.
ms.openlocfilehash: 289bd0bf16c6dcd9b26ec1a8c7920a29dab724a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435672"
---
# <a name="pageleftmargin-cell-print-properties-section"></a><span data-ttu-id="ecbd1-103">PageLeftMargin Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="ecbd1-103">PageLeftMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="ecbd1-104">Указывает поле слева от печатаемой страницы.</span><span class="sxs-lookup"><span data-stu-id="ecbd1-104">Specifies the margin on the left of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ecbd1-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="ecbd1-105">Remarks</span></span>

<span data-ttu-id="ecbd1-106">Это значение представляет физические единицы и не влияет на масштаб или единицы рисования.</span><span class="sxs-lookup"><span data-stu-id="ecbd1-106">This value represents physical units and is unaffected by scale or drawing units.</span></span> <span data-ttu-id="ecbd1-107">Например, если значение этой ячейки составляет 0,25 дюйма, то это поле будет 0,25 дюйма, даже если единицы страниц находятся в метрах.</span><span class="sxs-lookup"><span data-stu-id="ecbd1-107">For example, if this cell has a value of 0.25 in., this margin is 0.25 inch even if page units are feet.</span></span> <span data-ttu-id="ecbd1-108">Если единицы не заявимы, это значение по умолчанию является единицами страниц.</span><span class="sxs-lookup"><span data-stu-id="ecbd1-108">If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="ecbd1-109">Чтобы получить ссылку на ячейку PageLeftMargin по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="ecbd1-109">To get a reference to the PageLeftMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ecbd1-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="ecbd1-110">Cell name:</span></span>  <br/> | <span data-ttu-id="ecbd1-111">PageLeftMargin</span><span class="sxs-lookup"><span data-stu-id="ecbd1-111">PageLeftMargin</span></span>  <br/> |
   
<span data-ttu-id="ecbd1-112">Чтобы получить ссылку на ячейку PageLeftMargin по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="ecbd1-112">To get a reference to the PageLeftMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ecbd1-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ecbd1-113">Section index:</span></span>  <br/> |<span data-ttu-id="ecbd1-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ecbd1-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ecbd1-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ecbd1-115">Row index:</span></span>  <br/> |<span data-ttu-id="ecbd1-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="ecbd1-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="ecbd1-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ecbd1-117">Cell index:</span></span>  <br/> |<span data-ttu-id="ecbd1-118">**visPrintPropertiesLeftMargin**</span><span class="sxs-lookup"><span data-stu-id="ecbd1-118">**visPrintPropertiesLeftMargin**</span></span> <br/> |
   

