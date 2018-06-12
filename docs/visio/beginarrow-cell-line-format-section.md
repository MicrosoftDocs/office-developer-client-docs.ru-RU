---
title: Ячейка BeginArrow (раздел формат строки)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51105
localization_priority: Normal
ms.assetid: 0ab4044e-2d77-1fbe-ef20-5d029bc064ba
description: Указывает, будет ли линия стрелки или другой формат окончания строки в первой вершине. Введите число от 0 до 45 или использовать функцию с именем конец настраиваемой строки или используйте диалоговое окно строки.
ms.openlocfilehash: c6d5a66d76cfea61b1c9923c5b904dadec5495f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813172"
---
# <a name="beginarrow-cell-line-format-section"></a><span data-ttu-id="e5eae-104">Ячейка BeginArrow (раздел формат строки)</span><span class="sxs-lookup"><span data-stu-id="e5eae-104">BeginArrow Cell (Line Format Section)</span></span>

<span data-ttu-id="e5eae-105">Указывает, будет ли линия стрелки или другой формат окончания строки в первой вершине.</span><span class="sxs-lookup"><span data-stu-id="e5eae-105">Indicates whether a line has an arrowhead or other line end format at its first vertex.</span></span> <span data-ttu-id="e5eae-106">Введите число от 0 до 45 или использовать функцию с именем конец настраиваемой строки или используйте диалоговое окно **строки** .</span><span class="sxs-lookup"><span data-stu-id="e5eae-106">Enter a number from 0 to 45 or the USE function with the name of a custom line end, or use the **Line** dialog box.</span></span> 
  
|<span data-ttu-id="e5eae-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="e5eae-107">**Value**</span></span>|<span data-ttu-id="e5eae-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e5eae-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e5eae-109">0</span><span class="sxs-lookup"><span data-stu-id="e5eae-109">0</span></span>  <br/> | <span data-ttu-id="e5eae-110">Не стрелки.</span><span class="sxs-lookup"><span data-stu-id="e5eae-110">No arrowhead.</span></span>  <br/> |
| <span data-ttu-id="e5eae-111">1 - 45</span><span class="sxs-lookup"><span data-stu-id="e5eae-111">1 - 45</span></span>  <br/> | <span data-ttu-id="e5eae-112">Различные стрелки стили, которые соответствуют индексирование записей в диалоговом окне " **строка** ".</span><span class="sxs-lookup"><span data-stu-id="e5eae-112">Assorted arrowhead styles that correspond to indexed entries in the **Line** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5eae-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="e5eae-113">Remarks</span></span>

<span data-ttu-id="e5eae-114">Размер стрелки имеет значение в ячейке BeginArrowSize.</span><span class="sxs-lookup"><span data-stu-id="e5eae-114">The size of the arrowhead is set in the BeginArrowSize cell.</span></span>
  
<span data-ttu-id="e5eae-115">Чтобы получить ссылку на ячейку BeginArrow по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e5eae-115">To get a reference to the BeginArrow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e5eae-116">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="e5eae-116">Cell name:</span></span>  <br/> | <span data-ttu-id="e5eae-117">BeginArrow</span><span class="sxs-lookup"><span data-stu-id="e5eae-117">BeginArrow</span></span>  <br/> |
   
<span data-ttu-id="e5eae-118">Для получения ссылки на ячейки BeginArrow по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="e5eae-118">To get a reference to the BeginArrow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e5eae-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e5eae-119">Section index:</span></span>  <br/> |<span data-ttu-id="e5eae-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e5eae-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e5eae-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e5eae-121">Row index:</span></span>  <br/> |<span data-ttu-id="e5eae-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="e5eae-122">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="e5eae-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e5eae-123">Cell index:</span></span>  <br/> |<span data-ttu-id="e5eae-124">**visLineBeginArrow**</span><span class="sxs-lookup"><span data-stu-id="e5eae-124">**visLineBeginArrow**</span></span> <br/> |
   

