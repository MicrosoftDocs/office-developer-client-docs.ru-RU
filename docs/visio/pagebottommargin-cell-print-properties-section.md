---
title: Ячейка PageBottomMargin (раздел "Свойства печати")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60060
localization_priority: Normal
ms.assetid: 7a97e97c-278d-2e1e-6c4f-f5f32e2cdeb0
description: Задает поле в нижней части печатной страницы.
ms.openlocfilehash: fb67cf87f5e50719d24b0f354acc93209eed8811
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814329"
---
# <a name="pagebottommargin-cell-print-properties-section"></a><span data-ttu-id="16e2d-103">Ячейка PageBottomMargin (раздел "Свойства печати")</span><span class="sxs-lookup"><span data-stu-id="16e2d-103">PageBottomMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="16e2d-104">Задает поле в нижней части печатной страницы.</span><span class="sxs-lookup"><span data-stu-id="16e2d-104">Specifies the margin at the bottom of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="16e2d-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="16e2d-105">Remarks</span></span>

<span data-ttu-id="16e2d-106">Это значение представляет физические единицы и не влияет на масштаб или рисования единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="16e2d-106">This value represents physical units and is unaffected by scale or drawing units.</span></span> <span data-ttu-id="16e2d-107">Например если эта ячейка имеет значение 0,5 дюйма, это поле будет 0,5 дюйма даже в том случае, если страница указываются футов.</span><span class="sxs-lookup"><span data-stu-id="16e2d-107">For example, if this cell has a value of 0.5 in., this margin is 0.5 inch even if page units are feet.</span></span> <span data-ttu-id="16e2d-108">Если единицы не указан явно, это значение по умолчанию единицах страницы.</span><span class="sxs-lookup"><span data-stu-id="16e2d-108">If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="16e2d-109">Чтобы получить ссылку на ячейку PageBottomMargin по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="16e2d-109">To get a reference to the PageBottomMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="16e2d-110">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="16e2d-110">Cell name:</span></span>  <br/> | <span data-ttu-id="16e2d-111">PageBottomMargin</span><span class="sxs-lookup"><span data-stu-id="16e2d-111">PageBottomMargin</span></span>  <br/> |
   
<span data-ttu-id="16e2d-112">Для получения ссылки на ячейки PageBottomMargin по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="16e2d-112">To get a reference to the PageBottomMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="16e2d-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="16e2d-113">Section index:</span></span>  <br/> |<span data-ttu-id="16e2d-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="16e2d-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="16e2d-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="16e2d-115">Row index:</span></span>  <br/> |<span data-ttu-id="16e2d-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="16e2d-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="16e2d-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="16e2d-117">Cell index:</span></span>  <br/> |<span data-ttu-id="16e2d-118">**visPrintPropertiesBottomMargin**</span><span class="sxs-lookup"><span data-stu-id="16e2d-118">**visPrintPropertiesBottomMargin**</span></span> <br/> |
   

