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
ms.openlocfilehash: 442ec0d614589c709a097ba314abad044d470df6
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160274"
---
# <a name="rectsect-function"></a><span data-ttu-id="4611c-103">Функция RECTSECT</span><span class="sxs-lookup"><span data-stu-id="4611c-103">RECTSECT Function</span></span>

<span data-ttu-id="4611c-104">Вычисляет сектор прямоугольника, связанный с *x* и *y* , и возвращает целое число от 0 до 4, обозначающее сектор.</span><span class="sxs-lookup"><span data-stu-id="4611c-104">Calculates the sector of a rectangle associated with  *x*  and  *y*  and returns an integer 0 to 4, indicating the sector.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4611c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4611c-105">Syntax</span></span>

<span data-ttu-id="4611c-106">RECTSECT (***Ширина***, ***Высота***, ***x***, ***y***, ***параметр*** )</span><span class="sxs-lookup"><span data-stu-id="4611c-106">RECTSECT(***width***, ***height***, ***x***, ***y***, ***option*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4611c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4611c-107">Parameters</span></span>

|<span data-ttu-id="4611c-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="4611c-108">**Name**</span></span>|<span data-ttu-id="4611c-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="4611c-109">**Required/Optional**</span></span>|<span data-ttu-id="4611c-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="4611c-110">**Data Type**</span></span>|<span data-ttu-id="4611c-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4611c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4611c-112">_width_</span><span class="sxs-lookup"><span data-stu-id="4611c-112">_width_</span></span> <br/> |<span data-ttu-id="4611c-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4611c-113">Required</span></span>  <br/> |<span data-ttu-id="4611c-114">**String**</span><span class="sxs-lookup"><span data-stu-id="4611c-114">**String**</span></span> <br/> |<span data-ttu-id="4611c-115">Ширина прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4611c-115">Width of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="4611c-116">_height_</span><span class="sxs-lookup"><span data-stu-id="4611c-116">_height_</span></span> <br/> |<span data-ttu-id="4611c-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4611c-117">Required</span></span>  <br/> |<span data-ttu-id="4611c-118">**String**</span><span class="sxs-lookup"><span data-stu-id="4611c-118">**String**</span></span> <br/> |<span data-ttu-id="4611c-119">Высота прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4611c-119">Height of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="4611c-120">_x_</span><span class="sxs-lookup"><span data-stu-id="4611c-120">_x_</span></span> <br/> |<span data-ttu-id="4611c-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4611c-121">Required</span></span>  <br/> |<span data-ttu-id="4611c-122">**String**</span><span class="sxs-lookup"><span data-stu-id="4611c-122">**String**</span></span> <br/> |<span data-ttu-id="4611c-123">Координата x.</span><span class="sxs-lookup"><span data-stu-id="4611c-123">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="4611c-124">_y_</span><span class="sxs-lookup"><span data-stu-id="4611c-124">_y_</span></span> <br/> |<span data-ttu-id="4611c-125">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4611c-125">Required</span></span>  <br/> |<span data-ttu-id="4611c-126">**String**</span><span class="sxs-lookup"><span data-stu-id="4611c-126">**String**</span></span> <br/> |<span data-ttu-id="4611c-127">Координата y.</span><span class="sxs-lookup"><span data-stu-id="4611c-127">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="4611c-128">_)_</span><span class="sxs-lookup"><span data-stu-id="4611c-128">_option_</span></span> <br/> |<span data-ttu-id="4611c-129">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4611c-129">Required</span></span>  <br/> |<span data-ttu-id="4611c-130">**Логический**</span><span class="sxs-lookup"><span data-stu-id="4611c-130">**Boolean**</span></span> <br/> |<span data-ttu-id="4611c-131">Указывает, как обрабатываются точки, которые попадают на диагонали.</span><span class="sxs-lookup"><span data-stu-id="4611c-131">Specifies how points that fall on the diagonals are treated.</span></span> <span data-ttu-id="4611c-132">Задайте для параметра значение 0, чтобы использовать левые и правые сектора для точек по диагонали.</span><span class="sxs-lookup"><span data-stu-id="4611c-132">Set the value to 0 to use the left and right sectors for points on a diagonal.</span></span> <span data-ttu-id="4611c-133">Присвойте этому параметру значение 1, чтобы использовать верхние и нижние сектора для точек по диагонали.</span><span class="sxs-lookup"><span data-stu-id="4611c-133">Set the value to 1 to use the top and bottom sectors for points on a diagonal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4611c-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="4611c-134">Remarks</span></span>

<span data-ttu-id="4611c-135">Рассмотрим прямоугольник с *шириной* и *высотой* , а также точку (*x, y*) от центральной точки прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4611c-135">Consider a rectangle that has a  *width*  and a  *height*  , and a point (*x,y*) from the center point of the rectangle.</span></span> <span data-ttu-id="4611c-136">Нарисуйте диагональные линии через углы прямоугольника, чтобы разделить его на четыре сектора и центральную точку.</span><span class="sxs-lookup"><span data-stu-id="4611c-136">Draw diagonal lines through the corners of the rectangle to divide it into four sectors and a center point.</span></span> <span data-ttu-id="4611c-137">Сектора от 0 до 4 представляют центральную, правую, верхнюю, левую и нижнюю границу соответственно.</span><span class="sxs-lookup"><span data-stu-id="4611c-137">The sectors 0 through 4 represent the center-point, right, top, left, and bottom respectively.</span></span> 
  
![Секторы от 0 до 4 представляют центральную, правую, верхнюю, левую и нижнюю соответственно](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a><span data-ttu-id="4611c-139">Пример</span><span class="sxs-lookup"><span data-stu-id="4611c-139">Example</span></span>

<span data-ttu-id="4611c-140">RECTSECT (1 в, 2 в, 1 в,-7, 0)</span><span class="sxs-lookup"><span data-stu-id="4611c-140">RECTSECT(1 in, 2 in, 1 in, -7 in, 0)</span></span> 
  
<span data-ttu-id="4611c-141">Возвращает 4.</span><span class="sxs-lookup"><span data-stu-id="4611c-141">Returns 4.</span></span> 
  

