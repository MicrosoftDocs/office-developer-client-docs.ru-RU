---
title: BeginArrow Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51105
localization_priority: Normal
ms.assetid: 0ab4044e-2d77-1fbe-ef20-5d029bc064ba
description: Указывает, имеет ли строка стрелку или другой формат конца линии на первой вершине. Введите число от 0 до 45 или функцию USE с именем пользовательского конца строки или используйте диалоговое окно "Строка".
ms.openlocfilehash: cf5a512dabd0e6296b83fa7bfd2a2a6134143d50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410296"
---
# <a name="beginarrow-cell-line-format-section"></a><span data-ttu-id="c0c00-104">BeginArrow Cell (Line Format Section)</span><span class="sxs-lookup"><span data-stu-id="c0c00-104">BeginArrow Cell (Line Format Section)</span></span>

<span data-ttu-id="c0c00-105">Указывает, имеет ли строка стрелку или другой формат конца линии на первой вершине.</span><span class="sxs-lookup"><span data-stu-id="c0c00-105">Indicates whether a line has an arrowhead or other line end format at its first vertex.</span></span> <span data-ttu-id="c0c00-106">Введите число от 0 до 45 или функцию USE с именем пользовательского конца строки или используйте диалоговое окно "Строка". </span><span class="sxs-lookup"><span data-stu-id="c0c00-106">Enter a number from 0 to 45 or the USE function with the name of a custom line end, or use the **Line** dialog box.</span></span> 
  
|<span data-ttu-id="c0c00-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c0c00-107">**Value**</span></span>|<span data-ttu-id="c0c00-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c0c00-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c0c00-109">0</span><span class="sxs-lookup"><span data-stu-id="c0c00-109">0</span></span>  <br/> | <span data-ttu-id="c0c00-110">Нет наконечник.</span><span class="sxs-lookup"><span data-stu-id="c0c00-110">No arrowhead.</span></span>  <br/> |
| <span data-ttu-id="c0c00-111">1 - 45</span><span class="sxs-lookup"><span data-stu-id="c0c00-111">1 - 45</span></span>  <br/> | <span data-ttu-id="c0c00-112">Различные стили со стрелками, соответствующие индексным записям в **диалоговом** окне "Строка".</span><span class="sxs-lookup"><span data-stu-id="c0c00-112">Assorted arrowhead styles that correspond to indexed entries in the **Line** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0c00-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="c0c00-113">Remarks</span></span>

<span data-ttu-id="c0c00-114">Размер стрелки устанавливается в ячейке BeginArrowSize.</span><span class="sxs-lookup"><span data-stu-id="c0c00-114">The size of the arrowhead is set in the BeginArrowSize cell.</span></span>
  
<span data-ttu-id="c0c00-115">Чтобы получить ссылку на ячейку BeginArrow по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="c0c00-115">To get a reference to the BeginArrow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c0c00-116">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="c0c00-116">Cell name:</span></span>  <br/> | <span data-ttu-id="c0c00-117">BeginArrow</span><span class="sxs-lookup"><span data-stu-id="c0c00-117">BeginArrow</span></span>  <br/> |
   
<span data-ttu-id="c0c00-118">Чтобы получить ссылку на ячейку BeginArrow по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="c0c00-118">To get a reference to the BeginArrow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c0c00-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c0c00-119">Section index:</span></span>  <br/> |<span data-ttu-id="c0c00-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c0c00-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c0c00-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c0c00-121">Row index:</span></span>  <br/> |<span data-ttu-id="c0c00-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="c0c00-122">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="c0c00-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c0c00-123">Cell index:</span></span>  <br/> |<span data-ttu-id="c0c00-124">**visLineBeginArrow**</span><span class="sxs-lookup"><span data-stu-id="c0c00-124">**visLineBeginArrow**</span></span> <br/> |
   

