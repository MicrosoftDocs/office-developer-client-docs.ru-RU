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
description: Рабочая область для ввода и тестирования формул, на которые можно ссылаться по другим ячейкам.
ms.openlocfilehash: a7d2c6762e96fc19986521c2ba164666b925c928
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344529"
---
# <a name="scratch-section"></a><span data-ttu-id="6a571-103">Scratch Section</span><span class="sxs-lookup"><span data-stu-id="6a571-103">Scratch Section</span></span>

<span data-ttu-id="6a571-104">Рабочая область для ввода и тестирования формул, на которые можно ссылаться по другим ячейкам.</span><span class="sxs-lookup"><span data-stu-id="6a571-104">A work area for entering and testing formulas that can be referred to by other cells.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6a571-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6a571-105">Remarks</span></span>

<span data-ttu-id="6a571-106">Этот раздел можно добавить с помощью диалогового окна " **Вставить раздел** ".</span><span class="sxs-lookup"><span data-stu-id="6a571-106">You can add this section by using the **Insert Section** dialog box.</span></span> <span data-ttu-id="6a571-107">Щелкните правой кнопкой мыши в окне таблицы свойств фигуры и выберите команду **Вставить раздел**.</span><span class="sxs-lookup"><span data-stu-id="6a571-107">Right-click in the ShapeSheet window, and then click **Insert Section**.</span></span>
  
<span data-ttu-id="6a571-108">Раздел **"Рабочая область"** обычно используется для изоляции повторяющихся сложных вычислений.</span><span class="sxs-lookup"><span data-stu-id="6a571-108">The **Scratch** section is typically used to isolate repeated complex calculations.</span></span> <span data-ttu-id="6a571-109">Если ваше решение имеет хорошо определенное назначение, разумно использовать ячейку в разделе " **пользовательские ячейки** " для ясности, так как пользовательские ячейки могут называться.</span><span class="sxs-lookup"><span data-stu-id="6a571-109">If your solution has a well-defined purpose, it's wiser to use a cell in the **User-Defined Cells** section for clarity because User cells can be named.</span></span> 
  
<span data-ttu-id="6a571-110">В ячейках \*\*\*\* во вспомогательном разделе единицы используются с двумя различными способами.</span><span class="sxs-lookup"><span data-stu-id="6a571-110">Cells in the **Scratch** section use units in two different ways.</span></span> <span data-ttu-id="6a571-111">Ячейки X и Y используются для рисования единиц измерения; В ячейках С A по D не используются единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="6a571-111">X and Y cells use drawing units; A through D cells don't use units.</span></span> <span data-ttu-id="6a571-112">(В C программистами жаргон ячейки X и Y — "типизированные", а В ячейках "A" и "D" — "void".) Ячейки **"** фрагменты x" и **"с нуля"** часто используются для получения координат *x* и *y* , таких как **PinX** и **PinY**, или ячеек X и Y, обнаруженных в ячейке раздела **геометрии** .</span><span class="sxs-lookup"><span data-stu-id="6a571-112">(In C programmers' jargon, X and Y cells are "typed," and cells A through D are "void.") The **Scratch X** and **Scratch Y** cells are often used for deriving  *x-*  and  *y-*  coordinates, such as **PinX** and **PinY**, or the X and Y cells found in a **Geometry** section cell.</span></span> <span data-ttu-id="6a571-113">В пошаговых ячейках С A по D могут отображаться любые указанные единицы.</span><span class="sxs-lookup"><span data-stu-id="6a571-113">Scratch cells A through D can display whatever units you specify.</span></span> 
  
<span data-ttu-id="6a571-114">Дальнейшая разница — это способ хранения значений точек в этих ячейках.</span><span class="sxs-lookup"><span data-stu-id="6a571-114">A further difference is the way these cells store point values.</span></span> <span data-ttu-id="6a571-115">Точка в Visio — это один пакет данных для координат ( *x, y*).</span><span class="sxs-lookup"><span data-stu-id="6a571-115">A point in Visio is a single data package for an ( *x,y*) coordinate.</span></span> <span data-ttu-id="6a571-116">Когда формула возвращает значение точки, это значение интерпретируется одним из трех способов в зависимости от ячейки таблицы свойств фигуры, в которой находится формула.</span><span class="sxs-lookup"><span data-stu-id="6a571-116">When a formula returns a point value, that value is interpreted in one of three ways, depending on the ShapeSheet cell the formula is in.</span></span> <span data-ttu-id="6a571-117">Ячейки, связанные с координатами *x* (например, **PinX**или ячейки в столбце x в **геометрическом** разделе), извлекают только часть координат *x* значения точки.</span><span class="sxs-lookup"><span data-stu-id="6a571-117">Cells that relate to  *x*  -coordinates (for example, **PinX**, or cells in the X column of a **Geometry** section) extract just the  *x*  -coordinate part of a point value.</span></span> <span data-ttu-id="6a571-118">Ячейки, которые относятся к координатам *y* , извлекают только часть координат *y* значения точки.</span><span class="sxs-lookup"><span data-stu-id="6a571-118">Cells that relate to  *y*  -coordinates extract just the  *y*  -coordinate part of a point value.</span></span> 
  
<span data-ttu-id="6a571-119">Например, Visio извлекает формулу `PNT(3,4)` тремя способами.</span><span class="sxs-lookup"><span data-stu-id="6a571-119">For example, Visio extracts the formula  `PNT(3,4)` in these three ways.</span></span> 
  
|<span data-ttu-id="6a571-120">**Cell**</span><span class="sxs-lookup"><span data-stu-id="6a571-120">**Cell**</span></span>|<span data-ttu-id="6a571-121">**Если ввести**</span><span class="sxs-lookup"><span data-stu-id="6a571-121">**If you enter**</span></span>|<span data-ttu-id="6a571-122">**Visio рассматривает его как**</span><span class="sxs-lookup"><span data-stu-id="6a571-122">**Visio treats it as**</span></span>|<span data-ttu-id="6a571-123">**Result**</span><span class="sxs-lookup"><span data-stu-id="6a571-123">**Result**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6a571-124">X</span><span class="sxs-lookup"><span data-stu-id="6a571-124">X</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTX(PNT(3,4))` <br/> | <span data-ttu-id="6a571-125">3,0000.</span><span class="sxs-lookup"><span data-stu-id="6a571-125">3.0000 in.</span></span>  <br/> |
| <span data-ttu-id="6a571-126">Да</span><span class="sxs-lookup"><span data-stu-id="6a571-126">Y</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTY(PNT(3,4))` <br/> | <span data-ttu-id="6a571-127">4,0000.</span><span class="sxs-lookup"><span data-stu-id="6a571-127">4.0000 in.</span></span>  <br/> |
| <span data-ttu-id="6a571-128">A – D</span><span class="sxs-lookup"><span data-stu-id="6a571-128">A-D</span></span>  <br/> | `PNT(3,4)` <br/> | `PNT(3,4)` <br/> | <span data-ttu-id="6a571-129">PNT (3.0000 в., 4,0000)</span><span class="sxs-lookup"><span data-stu-id="6a571-129">PNT(3.0000 in., 4.0000 in.)</span></span>  <br/> |
   

