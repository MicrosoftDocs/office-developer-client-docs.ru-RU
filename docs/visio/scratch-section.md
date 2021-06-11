---
title: Scratch Section
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm2125
localization_priority: Normal
ms.assetid: 144dd06f-7225-57db-fd19-a58d6bccf0e1
description: Область работы для ввода и тестирования формул, на которые можно ссылаться другими ячейками.
ms.openlocfilehash: a7d2c6762e96fc19986521c2ba164666b925c928
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411605"
---
# <a name="scratch-section"></a><span data-ttu-id="6f677-103">Scratch Section</span><span class="sxs-lookup"><span data-stu-id="6f677-103">Scratch Section</span></span>

<span data-ttu-id="6f677-104">Область работы для ввода и тестирования формул, на которые можно ссылаться другими ячейками.</span><span class="sxs-lookup"><span data-stu-id="6f677-104">A work area for entering and testing formulas that can be referred to by other cells.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6f677-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="6f677-105">Remarks</span></span>

<span data-ttu-id="6f677-106">Этот раздел можно добавить с помощью диалоговое окно **Insert Section.**</span><span class="sxs-lookup"><span data-stu-id="6f677-106">You can add this section by using the **Insert Section** dialog box.</span></span> <span data-ttu-id="6f677-107">Щелкните правой кнопкой мыши в окне ShapeSheet и нажмите **кнопку Вставить раздел**.</span><span class="sxs-lookup"><span data-stu-id="6f677-107">Right-click in the ShapeSheet window, and then click **Insert Section**.</span></span>
  
<span data-ttu-id="6f677-108">Раздел **Scratch** обычно используется для изоляции повторных сложных вычислений.</span><span class="sxs-lookup"><span data-stu-id="6f677-108">The **Scratch** section is typically used to isolate repeated complex calculations.</span></span> <span data-ttu-id="6f677-109">Если ваше решение имеет четко определенное назначение, для ясности целесообразно использовать ячейку в разделе **Пользовательские** определенные ячейки, так как ячейки пользователей можно назвать.</span><span class="sxs-lookup"><span data-stu-id="6f677-109">If your solution has a well-defined purpose, it's wiser to use a cell in the **User-Defined Cells** section for clarity because User cells can be named.</span></span> 
  
<span data-ttu-id="6f677-110">Ячейки в **разделе Scratch** используют единицы двумя способами.</span><span class="sxs-lookup"><span data-stu-id="6f677-110">Cells in the **Scratch** section use units in two different ways.</span></span> <span data-ttu-id="6f677-111">Ячейки X и Y используют единицы рисования; Ячейки через D не используют единицы.</span><span class="sxs-lookup"><span data-stu-id="6f677-111">X and Y cells use drawing units; A through D cells don't use units.</span></span> <span data-ttu-id="6f677-112">(В жаргоне программистов C ячейки X и Y "введите", а ячейки A через D являются "недействительными".) Ячейки **Scratch X** и Scratch Y часто используются для производных *x-* и *y-координат,* таких как **PinX** и **PinY,** или ячеек X и **Y,** найденных в ячейке раздела **Геометрия.**</span><span class="sxs-lookup"><span data-stu-id="6f677-112">(In C programmers' jargon, X and Y cells are "typed," and cells A through D are "void.") The **Scratch X** and **Scratch Y** cells are often used for deriving  *x-*  and  *y-*  coordinates, such as **PinX** and **PinY**, or the X and Y cells found in a **Geometry** section cell.</span></span> <span data-ttu-id="6f677-113">Scratch cells A through D can display whatever units you specify.</span><span class="sxs-lookup"><span data-stu-id="6f677-113">Scratch cells A through D can display whatever units you specify.</span></span> 
  
<span data-ttu-id="6f677-114">Еще одно отличие состоит в том, как эти ячейки хранят значения точечные.</span><span class="sxs-lookup"><span data-stu-id="6f677-114">A further difference is the way these cells store point values.</span></span> <span data-ttu-id="6f677-115">Точкой в Visio является единый пакет данных для координат *(x,y).*</span><span class="sxs-lookup"><span data-stu-id="6f677-115">A point in Visio is a single data package for an ( *x,y*) coordinate.</span></span> <span data-ttu-id="6f677-116">Когда формула возвращает значение точки, это значение интерпретируется одним из трех способов, в зависимости от ячейки ShapeSheet, в которую находится формула.</span><span class="sxs-lookup"><span data-stu-id="6f677-116">When a formula returns a point value, that value is interpreted in one of three ways, depending on the ShapeSheet cell the formula is in.</span></span> <span data-ttu-id="6f677-117">Ячейки,  которые относятся к x-координатам (например, **PinX** или ячейкам в X-столбце раздела **Геометрия),** извлекают только *x-coordinate* часть значения точки.</span><span class="sxs-lookup"><span data-stu-id="6f677-117">Cells that relate to  *x*  -coordinates (for example, **PinX**, or cells in the X column of a **Geometry** section) extract just the  *x*  -coordinate part of a point value.</span></span> <span data-ttu-id="6f677-118">Ячейки, которые относятся к y-координатам, извлекают только *часть y-coordinate* значения точки. </span><span class="sxs-lookup"><span data-stu-id="6f677-118">Cells that relate to  *y*  -coordinates extract just the  *y*  -coordinate part of a point value.</span></span> 
  
<span data-ttu-id="6f677-119">Например, Visio извлекает формулу `PNT(3,4)` тремя способами.</span><span class="sxs-lookup"><span data-stu-id="6f677-119">For example, Visio extracts the formula  `PNT(3,4)` in these three ways.</span></span> 
  
|<span data-ttu-id="6f677-120">**Cell**</span><span class="sxs-lookup"><span data-stu-id="6f677-120">**Cell**</span></span>|<span data-ttu-id="6f677-121">**Если ввести**</span><span class="sxs-lookup"><span data-stu-id="6f677-121">**If you enter**</span></span>|<span data-ttu-id="6f677-122">**Visio относится к нему как к**</span><span class="sxs-lookup"><span data-stu-id="6f677-122">**Visio treats it as**</span></span>|<span data-ttu-id="6f677-123">**Результат**</span><span class="sxs-lookup"><span data-stu-id="6f677-123">**Result**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6f677-124">X</span><span class="sxs-lookup"><span data-stu-id="6f677-124">X</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTX(PNT(3,4))` <br/> | <span data-ttu-id="6f677-125">3.0000 в.</span><span class="sxs-lookup"><span data-stu-id="6f677-125">3.0000 in.</span></span>  <br/> |
| <span data-ttu-id="6f677-126">Да</span><span class="sxs-lookup"><span data-stu-id="6f677-126">Y</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTY(PNT(3,4))` <br/> | <span data-ttu-id="6f677-127">4.0000 в.</span><span class="sxs-lookup"><span data-stu-id="6f677-127">4.0000 in.</span></span>  <br/> |
| <span data-ttu-id="6f677-128">A-D</span><span class="sxs-lookup"><span data-stu-id="6f677-128">A-D</span></span>  <br/> | `PNT(3,4)` <br/> | `PNT(3,4)` <br/> | <span data-ttu-id="6f677-129">PNT (3.0000 in., 4.0000 in.)</span><span class="sxs-lookup"><span data-stu-id="6f677-129">PNT(3.0000 in., 4.0000 in.)</span></span>  <br/> |
   

