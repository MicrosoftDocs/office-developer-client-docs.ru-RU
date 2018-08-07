---
title: Ячейка PageRightMargin (раздел "Свойства печати")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60062
localization_priority: Normal
ms.assetid: f864c759-ed94-8ab7-d664-cc04b3ed743e
description: Задает поле в правой части печатной страницы.
ms.openlocfilehash: 951a16ff20e294b68ed5447d330f4e7cbc100c82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814340"
---
# <a name="pagerightmargin-cell-print-properties-section"></a><span data-ttu-id="d83f3-103">Ячейка PageRightMargin (раздел "Свойства печати")</span><span class="sxs-lookup"><span data-stu-id="d83f3-103">PageRightMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="d83f3-104">Задает поле в правой части печатной страницы.</span><span class="sxs-lookup"><span data-stu-id="d83f3-104">Specifies the margin on the right of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d83f3-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="d83f3-105">Remarks</span></span>

<span data-ttu-id="d83f3-106">Это значение представляет физические единицы и не влияет на масштаб или рисования единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="d83f3-106">This value represents physical units and is unaffected by scale or drawing units.</span></span> <span data-ttu-id="d83f3-107">Например если эта ячейка имеет значение 0,25 дюйма, это поле будет 0,25 дюйма даже в том случае, если страница указываются футов.</span><span class="sxs-lookup"><span data-stu-id="d83f3-107">For example, if this cell has a value of 0.25 in., this margin is 0.25 inch even if page units are feet.</span></span> <span data-ttu-id="d83f3-108">Если единицы не указан явно, это значение по умолчанию единицах страницы.</span><span class="sxs-lookup"><span data-stu-id="d83f3-108">If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="d83f3-109">Чтобы получить ссылку на ячейку PageRightMargin по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d83f3-109">To get a reference to the PageRightMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d83f3-110">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="d83f3-110">Cell name:</span></span>  <br/> | <span data-ttu-id="d83f3-111">PageRightMargin</span><span class="sxs-lookup"><span data-stu-id="d83f3-111">PageRightMargin</span></span>  <br/> |
   
<span data-ttu-id="d83f3-112">Для получения ссылки на ячейки PageRightMargin по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="d83f3-112">To get a reference to the PageRightMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d83f3-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d83f3-113">Section index:</span></span>  <br/> |<span data-ttu-id="d83f3-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d83f3-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d83f3-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d83f3-115">Row index:</span></span>  <br/> |<span data-ttu-id="d83f3-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="d83f3-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="d83f3-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d83f3-117">Cell index:</span></span>  <br/> |<span data-ttu-id="d83f3-118">**visPrintPropertiesRightMargin**</span><span class="sxs-lookup"><span data-stu-id="d83f3-118">**visPrintPropertiesRightMargin**</span></span> <br/> |
   

