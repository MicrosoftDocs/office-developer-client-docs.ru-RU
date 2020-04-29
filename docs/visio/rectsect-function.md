---
title: Функция RECTSECT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251486
localization_priority: Normal
ms.assetid: e83343c5-df5f-bf74-f854-6380176693a2
description: Вычисляет сектор прямоугольника, связанный с x и y, и возвращает целое число от 0 до 4, обозначающее сектор.
ms.openlocfilehash: fb7ed37ac498765e21c62d7180413cdbcb932502
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360035"
---
# <a name="rectsect-function"></a><span data-ttu-id="b35d3-103">Функция RECTSECT</span><span class="sxs-lookup"><span data-stu-id="b35d3-103">RECTSECT Function</span></span>

<span data-ttu-id="b35d3-104">Вычисляет сектор прямоугольника, связанный с *x* и *y* , и возвращает целое число от 0 до 4, обозначающее сектор.</span><span class="sxs-lookup"><span data-stu-id="b35d3-104">Calculates the sector of a rectangle associated with  *x*  and  *y*  and returns an integer 0 to 4, indicating the sector.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b35d3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b35d3-105">Syntax</span></span>

<span data-ttu-id="b35d3-106">RECTSECT (\* \* *Ширина* \* \*, \* \* *Высота* \* \*, \* \* *x* \* \*, \* \* *y* \* \*, \* \* *параметр* \* \*)</span><span class="sxs-lookup"><span data-stu-id="b35d3-106">RECTSECT(\*\* *width* \*\*, \*\* *height* \*\*, \*\* *x* \*\*, \*\* *y* \*\*, \*\* *option* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b35d3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b35d3-107">Parameters</span></span>

|<span data-ttu-id="b35d3-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="b35d3-108">**Name**</span></span>|<span data-ttu-id="b35d3-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="b35d3-109">**Required/Optional**</span></span>|<span data-ttu-id="b35d3-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="b35d3-110">**Data Type**</span></span>|<span data-ttu-id="b35d3-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b35d3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b35d3-112">_width_</span><span class="sxs-lookup"><span data-stu-id="b35d3-112">_width_</span></span> <br/> |<span data-ttu-id="b35d3-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b35d3-113">Required</span></span>  <br/> |<span data-ttu-id="b35d3-114">**String**</span><span class="sxs-lookup"><span data-stu-id="b35d3-114">**String**</span></span> <br/> |<span data-ttu-id="b35d3-115">Ширина прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="b35d3-115">Width of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="b35d3-116">_height_</span><span class="sxs-lookup"><span data-stu-id="b35d3-116">_height_</span></span> <br/> |<span data-ttu-id="b35d3-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b35d3-117">Required</span></span>  <br/> |<span data-ttu-id="b35d3-118">**String**</span><span class="sxs-lookup"><span data-stu-id="b35d3-118">**String**</span></span> <br/> |<span data-ttu-id="b35d3-119">Высота прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="b35d3-119">Height of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="b35d3-120">_x_</span><span class="sxs-lookup"><span data-stu-id="b35d3-120">_x_</span></span> <br/> |<span data-ttu-id="b35d3-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b35d3-121">Required</span></span>  <br/> |<span data-ttu-id="b35d3-122">**String**</span><span class="sxs-lookup"><span data-stu-id="b35d3-122">**String**</span></span> <br/> |<span data-ttu-id="b35d3-123">Координата x.</span><span class="sxs-lookup"><span data-stu-id="b35d3-123">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="b35d3-124">_y_</span><span class="sxs-lookup"><span data-stu-id="b35d3-124">_y_</span></span> <br/> |<span data-ttu-id="b35d3-125">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b35d3-125">Required</span></span>  <br/> |<span data-ttu-id="b35d3-126">**String**</span><span class="sxs-lookup"><span data-stu-id="b35d3-126">**String**</span></span> <br/> |<span data-ttu-id="b35d3-127">Координата y.</span><span class="sxs-lookup"><span data-stu-id="b35d3-127">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="b35d3-128">_)_</span><span class="sxs-lookup"><span data-stu-id="b35d3-128">_option_</span></span> <br/> |<span data-ttu-id="b35d3-129">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b35d3-129">Required</span></span>  <br/> |<span data-ttu-id="b35d3-130">**Логический**</span><span class="sxs-lookup"><span data-stu-id="b35d3-130">**Boolean**</span></span> <br/> |<span data-ttu-id="b35d3-131">Указывает, как обрабатываются точки, которые попадают на диагонали.</span><span class="sxs-lookup"><span data-stu-id="b35d3-131">Specifies how points that fall on the diagonals are treated.</span></span> <span data-ttu-id="b35d3-132">Задайте для параметра значение 0, чтобы использовать левые и правые сектора для точек по диагонали.</span><span class="sxs-lookup"><span data-stu-id="b35d3-132">Set the value to 0 to use the left and right sectors for points on a diagonal.</span></span> <span data-ttu-id="b35d3-133">Присвойте этому параметру значение 1, чтобы использовать верхние и нижние сектора для точек по диагонали.</span><span class="sxs-lookup"><span data-stu-id="b35d3-133">Set the value to 1 to use the top and bottom sectors for points on a diagonal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b35d3-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="b35d3-134">Remarks</span></span>

<span data-ttu-id="b35d3-135">Рассмотрим прямоугольник с *шириной* и *высотой* , а также точку (*x, y*) от центральной точки прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="b35d3-135">Consider a rectangle that has a  *width*  and a  *height*  , and a point (*x,y*) from the center point of the rectangle.</span></span> <span data-ttu-id="b35d3-136">Нарисуйте диагональные линии через углы прямоугольника, чтобы разделить его на четыре сектора и центральную точку.</span><span class="sxs-lookup"><span data-stu-id="b35d3-136">Draw diagonal lines through the corners of the rectangle to divide it into four sectors and a center point.</span></span> <span data-ttu-id="b35d3-137">Сектора от 0 до 4 представляют центральную, правую, верхнюю, левую и нижнюю границу соответственно.</span><span class="sxs-lookup"><span data-stu-id="b35d3-137">The sectors 0 through 4 represent the center-point, right, top, left, and bottom respectively.</span></span> 
  
![Секторы от 0 до 4 представляют центральную, правую, верхнюю, левую и нижнюю соответственно](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a><span data-ttu-id="b35d3-139">Пример</span><span class="sxs-lookup"><span data-stu-id="b35d3-139">Example</span></span>

<span data-ttu-id="b35d3-140">RECTSECT (1 в, 2 в, 1 в,-7, 0)</span><span class="sxs-lookup"><span data-stu-id="b35d3-140">RECTSECT(1 in, 2 in, 1 in, -7 in, 0)</span></span> 
  
<span data-ttu-id="b35d3-141">Возвращает 4.</span><span class="sxs-lookup"><span data-stu-id="b35d3-141">Returns 4.</span></span> 
  

