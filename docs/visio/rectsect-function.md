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
description: Вычисляет сектор прямоугольника, связанного с x и y, и возвращает количество от 0 до 4, обозначающее сектор.
ms.openlocfilehash: 442ec0d614589c709a097ba314abad044d470df6
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160274"
---
# <a name="rectsect-function"></a><span data-ttu-id="0cd50-103">Функция RECTSECT</span><span class="sxs-lookup"><span data-stu-id="0cd50-103">RECTSECT Function</span></span>

<span data-ttu-id="0cd50-104">Вычисляет сектор прямоугольника, связанного с  *x*  и  *y,*  и возвращает количество от 0 до 4, обозначающее сектор.</span><span class="sxs-lookup"><span data-stu-id="0cd50-104">Calculates the sector of a rectangle associated with  *x*  and  *y*  and returns an integer 0 to 4, indicating the sector.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0cd50-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0cd50-105">Syntax</span></span>

<span data-ttu-id="0cd50-106">RECTSECT(width, ***height,*** ***x***, ***y***, ***option)***</span><span class="sxs-lookup"><span data-stu-id="0cd50-106">RECTSECT(***width***, ***height***, ***x***, ***y***, ***option*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0cd50-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0cd50-107">Parameters</span></span>

|<span data-ttu-id="0cd50-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="0cd50-108">**Name**</span></span>|<span data-ttu-id="0cd50-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="0cd50-109">**Required/Optional**</span></span>|<span data-ttu-id="0cd50-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="0cd50-110">**Data Type**</span></span>|<span data-ttu-id="0cd50-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0cd50-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0cd50-112">_width_</span><span class="sxs-lookup"><span data-stu-id="0cd50-112">_width_</span></span> <br/> |<span data-ttu-id="0cd50-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="0cd50-113">Required</span></span>  <br/> |<span data-ttu-id="0cd50-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="0cd50-114">**String**</span></span> <br/> |<span data-ttu-id="0cd50-115">Ширина прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="0cd50-115">Width of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="0cd50-116">_height_</span><span class="sxs-lookup"><span data-stu-id="0cd50-116">_height_</span></span> <br/> |<span data-ttu-id="0cd50-117">Обязательно</span><span class="sxs-lookup"><span data-stu-id="0cd50-117">Required</span></span>  <br/> |<span data-ttu-id="0cd50-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="0cd50-118">**String**</span></span> <br/> |<span data-ttu-id="0cd50-119">Высота прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="0cd50-119">Height of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="0cd50-120">_x_</span><span class="sxs-lookup"><span data-stu-id="0cd50-120">_x_</span></span> <br/> |<span data-ttu-id="0cd50-121">Обязательно</span><span class="sxs-lookup"><span data-stu-id="0cd50-121">Required</span></span>  <br/> |<span data-ttu-id="0cd50-122">**Строка**</span><span class="sxs-lookup"><span data-stu-id="0cd50-122">**String**</span></span> <br/> |<span data-ttu-id="0cd50-123">X-координата.</span><span class="sxs-lookup"><span data-stu-id="0cd50-123">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="0cd50-124">_y_</span><span class="sxs-lookup"><span data-stu-id="0cd50-124">_y_</span></span> <br/> |<span data-ttu-id="0cd50-125">Обязательно</span><span class="sxs-lookup"><span data-stu-id="0cd50-125">Required</span></span>  <br/> |<span data-ttu-id="0cd50-126">**Строка**</span><span class="sxs-lookup"><span data-stu-id="0cd50-126">**String**</span></span> <br/> |<span data-ttu-id="0cd50-127">Координата Y.</span><span class="sxs-lookup"><span data-stu-id="0cd50-127">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="0cd50-128">_option_</span><span class="sxs-lookup"><span data-stu-id="0cd50-128">_option_</span></span> <br/> |<span data-ttu-id="0cd50-129">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0cd50-129">Required</span></span>  <br/> |<span data-ttu-id="0cd50-130">**Логический**</span><span class="sxs-lookup"><span data-stu-id="0cd50-130">**Boolean**</span></span> <br/> |<span data-ttu-id="0cd50-131">Указывает, как обрабатываются точки, попадая на диагонали.</span><span class="sxs-lookup"><span data-stu-id="0cd50-131">Specifies how points that fall on the diagonals are treated.</span></span> <span data-ttu-id="0cd50-132">Установите значение 0, чтобы использовать левый и правый секторы для точек по диагонали.</span><span class="sxs-lookup"><span data-stu-id="0cd50-132">Set the value to 0 to use the left and right sectors for points on a diagonal.</span></span> <span data-ttu-id="0cd50-133">Установите значение 1, чтобы использовать верхний и нижний секторы для точек по диагонали.</span><span class="sxs-lookup"><span data-stu-id="0cd50-133">Set the value to 1 to use the top and bottom sectors for points on a diagonal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0cd50-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="0cd50-134">Remarks</span></span>

<span data-ttu-id="0cd50-135">Рассмотрим прямоугольник с шириной и высотой *и* точкой *(x,y)* от центральной точки прямоугольника. </span><span class="sxs-lookup"><span data-stu-id="0cd50-135">Consider a rectangle that has a  *width*  and a  *height*  , and a point (*x,y*) from the center point of the rectangle.</span></span> <span data-ttu-id="0cd50-136">Нарисуйте диагональные линии через углы прямоугольника, чтобы разделить его на четыре сектора и центр.</span><span class="sxs-lookup"><span data-stu-id="0cd50-136">Draw diagonal lines through the corners of the rectangle to divide it into four sectors and a center point.</span></span> <span data-ttu-id="0cd50-137">Секторы от 0 до 4 представляют собой центр, правую, верхнюю, левую и нижнюю соответственно.</span><span class="sxs-lookup"><span data-stu-id="0cd50-137">The sectors 0 through 4 represent the center-point, right, top, left, and bottom respectively.</span></span> 
  
![Секторы от 0 до 4 представляют собой центр, правую, верхнюю, левую и нижнюю соответственно](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a><span data-ttu-id="0cd50-139">Пример</span><span class="sxs-lookup"><span data-stu-id="0cd50-139">Example</span></span>

<span data-ttu-id="0cd50-140">RECTSECT(1 in, 2 in, 1 in, -7 in, 0)</span><span class="sxs-lookup"><span data-stu-id="0cd50-140">RECTSECT(1 in, 2 in, 1 in, -7 in, 0)</span></span> 
  
<span data-ttu-id="0cd50-141">Возвращает 4.</span><span class="sxs-lookup"><span data-stu-id="0cd50-141">Returns 4.</span></span> 
  

