---
title: Раздел "Вспомогательный"
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm2125
localization_priority: Normal
ms.assetid: 144dd06f-7225-57db-fd19-a58d6bccf0e1
description: Рабочая область для ввода и проверки формул, которые могут использоваться в других ячеек.
ms.openlocfilehash: 16f0bac8f139c0b03d7826ac377a964d15296dd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814730"
---
# <a name="scratch-section"></a><span data-ttu-id="ef17c-103">Раздел "Вспомогательный"</span><span class="sxs-lookup"><span data-stu-id="ef17c-103">Scratch Section</span></span>

<span data-ttu-id="ef17c-104">Рабочая область для ввода и проверки формул, которые могут использоваться в других ячеек.</span><span class="sxs-lookup"><span data-stu-id="ef17c-104">A work area for entering and testing formulas that can be referred to by other cells.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ef17c-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="ef17c-105">Remarks</span></span>

<span data-ttu-id="ef17c-106">В этом разделе можно добавить с помощью диалогового окна **Вставить раздел** .</span><span class="sxs-lookup"><span data-stu-id="ef17c-106">You can add this section by using the **Insert Section** dialog box.</span></span> <span data-ttu-id="ef17c-107">Щелкните правой кнопкой мыши в окне таблицы свойств фигуры и нажмите кнопку **Вставить раздел**.</span><span class="sxs-lookup"><span data-stu-id="ef17c-107">Right-click in the ShapeSheet window, and then click **Insert Section**.</span></span>
  
<span data-ttu-id="ef17c-108">В разделе **рабочие** обычно используется для изолирования повторяющиеся сложные вычисления.</span><span class="sxs-lookup"><span data-stu-id="ef17c-108">The **Scratch** section is typically used to isolate repeated complex calculations.</span></span> <span data-ttu-id="ef17c-109">Если решение должно четко определенные цели, приходить использовать ячейки в разделе **Пользовательские ячейки** для ясности, так как ячейки пользователь может с именем.</span><span class="sxs-lookup"><span data-stu-id="ef17c-109">If your solution has a well-defined purpose, it's wiser to use a cell in the **User-Defined Cells** section for clarity because User cells can be named.</span></span> 
  
<span data-ttu-id="ef17c-110">Ячейки в разделе **рабочие** используют единиц измерения двумя способами.</span><span class="sxs-lookup"><span data-stu-id="ef17c-110">Cells in the **Scratch** section use units in two different ways.</span></span> <span data-ttu-id="ef17c-111">X и Y ячеек используйте рисунка единиц измерения; До D ячеек не используйте единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="ef17c-111">X and Y cells use drawing units; A through D cells don't use units.</span></span> <span data-ttu-id="ef17c-112">(В жаргон программистов C ячейки X и Y «вводятся» и ячейки с A по D «void».) Ячейки **Вспомогательный X** и **Y рабочие** часто используются для извлечения координаты *x* и *y* , такие как **PinX** и **PinY**или X и Y ячеек, найденные в ячейке раздел **геометрии** .</span><span class="sxs-lookup"><span data-stu-id="ef17c-112">(In C programmers' jargon, X and Y cells are "typed," and cells A through D are "void.") The **Scratch X** and **Scratch Y** cells are often used for deriving  *x-*  and  *y-*  coordinates, such as **PinX** and **PinY**, or the X and Y cells found in a **Geometry** section cell.</span></span> <span data-ttu-id="ef17c-113">Вспомогательный буквы от A до D можно отобразить независимо от устройства, можно указать ячеек.</span><span class="sxs-lookup"><span data-stu-id="ef17c-113">Scratch cells A through D can display whatever units you specify.</span></span> 
  
<span data-ttu-id="ef17c-114">Дальнейший разницы способ таких ячеек хранения значения точек.</span><span class="sxs-lookup"><span data-stu-id="ef17c-114">A further difference is the way these cells store point values.</span></span> <span data-ttu-id="ef17c-115">Точка в Visio — это пакет данных single для координаты ( *x, y*).</span><span class="sxs-lookup"><span data-stu-id="ef17c-115">A point in Visio is a single data package for an ( *x,y*) coordinate.</span></span> <span data-ttu-id="ef17c-116">Если формула возвращает значение точки, это значение интерпретируется в одном из трех следующих способов в зависимости от формула находится в ячейке таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="ef17c-116">When a formula returns a point value, that value is interpreted in one of three ways, depending on the ShapeSheet cell the formula is in.</span></span> <span data-ttu-id="ef17c-117">Ячейки, которые относятся к *x* -координаты (например, **PinX**или ячеек в столбце X раздел **геометрии** ) извлекать только что *x* -координации значение точки.</span><span class="sxs-lookup"><span data-stu-id="ef17c-117">Cells that relate to  *x*  -coordinates (for example, **PinX**, or cells in the X column of a **Geometry** section) extract just the  *x*  -coordinate part of a point value.</span></span> <span data-ttu-id="ef17c-118">Ячейки, которые относятся к *y* -координаты извлекать только что *y* -координации значение точки.</span><span class="sxs-lookup"><span data-stu-id="ef17c-118">Cells that relate to  *y*  -coordinates extract just the  *y*  -coordinate part of a point value.</span></span> 
  
<span data-ttu-id="ef17c-119">Например, для Visio извлекает формулу `PNT(3,4)` следующими тремя способами.</span><span class="sxs-lookup"><span data-stu-id="ef17c-119">For example, Visio extracts the formula  `PNT(3,4)` in these three ways.</span></span> 
  
|<span data-ttu-id="ef17c-120">**Cell**</span><span class="sxs-lookup"><span data-stu-id="ef17c-120">**Cell**</span></span>|<span data-ttu-id="ef17c-121">**Если ввести**</span><span class="sxs-lookup"><span data-stu-id="ef17c-121">**If you enter**</span></span>|<span data-ttu-id="ef17c-122">**Visio обрабатывает ее как**</span><span class="sxs-lookup"><span data-stu-id="ef17c-122">**Visio treats it as**</span></span>|<span data-ttu-id="ef17c-123">**Результат**</span><span class="sxs-lookup"><span data-stu-id="ef17c-123">**Result**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ef17c-124">X </span><span class="sxs-lookup"><span data-stu-id="ef17c-124">X</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTX(PNT(3,4))` <br/> | <span data-ttu-id="ef17c-125">3.0000 in.</span><span class="sxs-lookup"><span data-stu-id="ef17c-125">3.0000 in.</span></span>  <br/> |
| <span data-ttu-id="ef17c-126">Да</span><span class="sxs-lookup"><span data-stu-id="ef17c-126">Y</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTY(PNT(3,4))` <br/> | <span data-ttu-id="ef17c-127">4.0000 in.</span><span class="sxs-lookup"><span data-stu-id="ef17c-127">4.0000 in.</span></span>  <br/> |
| <span data-ttu-id="ef17c-128">A-D</span><span class="sxs-lookup"><span data-stu-id="ef17c-128">A-D</span></span>  <br/> | `PNT(3,4)` <br/> | `PNT(3,4)` <br/> | <span data-ttu-id="ef17c-129">Раздела PNT (3.0000 дюймов, 4.0000 in.)</span><span class="sxs-lookup"><span data-stu-id="ef17c-129">PNT(3.0000 in., 4.0000 in.)</span></span>  <br/> |
   

