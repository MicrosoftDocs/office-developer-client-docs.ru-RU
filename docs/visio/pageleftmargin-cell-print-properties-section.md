---
title: Ячейка PageLeftMargin (раздел "Свойства печати")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60061
localization_priority: Normal
ms.assetid: 7ecdfc37-c9d4-2fde-ed3e-be81657c24e2
description: Задает поле в левой части печатной страницы.
ms.openlocfilehash: 5fd2c8cd5b18a4baedd355627005b7c5c2df3252
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814330"
---
# <a name="pageleftmargin-cell-print-properties-section"></a><span data-ttu-id="76dd2-103">Ячейка PageLeftMargin (раздел "Свойства печати")</span><span class="sxs-lookup"><span data-stu-id="76dd2-103">PageLeftMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="76dd2-104">Задает поле в левой части печатной страницы.</span><span class="sxs-lookup"><span data-stu-id="76dd2-104">Specifies the margin on the left of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="76dd2-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="76dd2-105">Remarks</span></span>

<span data-ttu-id="76dd2-106">Это значение представляет физические единицы и не влияет на масштаб или рисования единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="76dd2-106">This value represents physical units and is unaffected by scale or drawing units.</span></span> <span data-ttu-id="76dd2-107">Например если эта ячейка имеет значение 0,25 дюйма, это поле будет 0,25 дюйма даже в том случае, если страница указываются футов.</span><span class="sxs-lookup"><span data-stu-id="76dd2-107">For example, if this cell has a value of 0.25 in., this margin is 0.25 inch even if page units are feet.</span></span> <span data-ttu-id="76dd2-108">Если единицы не указан явно, это значение по умолчанию единицах страницы.</span><span class="sxs-lookup"><span data-stu-id="76dd2-108">If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="76dd2-109">Чтобы получить ссылку на ячейку PageLeftMargin по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="76dd2-109">To get a reference to the PageLeftMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="76dd2-110">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="76dd2-110">Cell name:</span></span>  <br/> | <span data-ttu-id="76dd2-111">PageLeftMargin</span><span class="sxs-lookup"><span data-stu-id="76dd2-111">PageLeftMargin</span></span>  <br/> |
   
<span data-ttu-id="76dd2-112">Для получения ссылки на ячейки PageLeftMargin по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="76dd2-112">To get a reference to the PageLeftMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="76dd2-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="76dd2-113">Section index:</span></span>  <br/> |<span data-ttu-id="76dd2-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="76dd2-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="76dd2-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="76dd2-115">Row index:</span></span>  <br/> |<span data-ttu-id="76dd2-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="76dd2-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="76dd2-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="76dd2-117">Cell index:</span></span>  <br/> |<span data-ttu-id="76dd2-118">**visPrintPropertiesLeftMargin**</span><span class="sxs-lookup"><span data-stu-id="76dd2-118">**visPrintPropertiesLeftMargin**</span></span> <br/> |
   

