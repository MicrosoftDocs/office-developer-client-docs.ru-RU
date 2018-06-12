---
title: Ячейка PageTopMargin (печати Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033785
localization_priority: Normal
ms.assetid: 2ba0fd22-65a6-6cb6-da00-08f391705544
description: Задает поле в верхней части страницы принтера.
ms.openlocfilehash: 1b7be63e3f21365231120c602d8edfe1dc727f88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814346"
---
# <a name="pagetopmargin-cell-print-properties-section"></a><span data-ttu-id="16a6d-103">Ячейка PageTopMargin (печати Properties Section)</span><span class="sxs-lookup"><span data-stu-id="16a6d-103">PageTopMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="16a6d-104">Задает поле в верхней части страницы принтера.</span><span class="sxs-lookup"><span data-stu-id="16a6d-104">Specifies the margin at the top of the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="16a6d-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="16a6d-105">Remarks</span></span>

<span data-ttu-id="16a6d-106">Это значение представляет физические единицы и не влияет на масштаб или рисования единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="16a6d-106">This value represents physical units and is unaffected by scale or drawing units.</span></span> <span data-ttu-id="16a6d-107">Например если эта ячейка имеет значение 0,25 дюйма, это поле будет 0,25 дюйма даже в том случае, если страница указываются футов.</span><span class="sxs-lookup"><span data-stu-id="16a6d-107">For example, if this cell has a value of 0.25 in., this margin is 0.25 inch even if page units are feet.</span></span> <span data-ttu-id="16a6d-108">Если единицы не указан явно, это значение по умолчанию единицах страницы.</span><span class="sxs-lookup"><span data-stu-id="16a6d-108">If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="16a6d-109">Чтобы получить ссылку на ячейку PageTopMargin по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="16a6d-109">To get a reference to the PageTopMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="16a6d-110">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="16a6d-110">Cell name:</span></span>  <br/> | <span data-ttu-id="16a6d-111">PageTopMargin</span><span class="sxs-lookup"><span data-stu-id="16a6d-111">PageTopMargin</span></span>  <br/> |
   
<span data-ttu-id="16a6d-112">Для получения ссылки на ячейки PageTopMargin по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="16a6d-112">To get a reference to the PageTopMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="16a6d-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="16a6d-113">Section index:</span></span>  <br/> |<span data-ttu-id="16a6d-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="16a6d-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="16a6d-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="16a6d-115">Row index:</span></span>  <br/> |<span data-ttu-id="16a6d-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="16a6d-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="16a6d-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="16a6d-117">Cell index:</span></span>  <br/> |<span data-ttu-id="16a6d-118">**visPrintPropertiesTopMargin**</span><span class="sxs-lookup"><span data-stu-id="16a6d-118">**visPrintPropertiesTopMargin**</span></span> <br/> |
   

