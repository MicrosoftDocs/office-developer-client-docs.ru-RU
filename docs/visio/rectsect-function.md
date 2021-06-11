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
description: Вычисляет сектор прямоугольника, связанный с x и y, и возвращает 0 на 4, указав сектор.
ms.openlocfilehash: 442ec0d614589c709a097ba314abad044d470df6
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160274"
---
# <a name="rectsect-function"></a><span data-ttu-id="d8736-103">Функция RECTSECT</span><span class="sxs-lookup"><span data-stu-id="d8736-103">RECTSECT Function</span></span>

<span data-ttu-id="d8736-104">Вычисляет сектор прямоугольника, связанный с  *x*  и  *y,*  и возвращает 0 на 4, указав сектор.</span><span class="sxs-lookup"><span data-stu-id="d8736-104">Calculates the sector of a rectangle associated with  *x*  and  *y*  and returns an integer 0 to 4, indicating the sector.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d8736-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8736-105">Syntax</span></span>

<span data-ttu-id="d8736-106">RECTSECT ***(ширина,*** ***высота***, ***x***, ***y***, ***вариант*** )</span><span class="sxs-lookup"><span data-stu-id="d8736-106">RECTSECT(***width***, ***height***, ***x***, ***y***, ***option*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d8736-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8736-107">Parameters</span></span>

|<span data-ttu-id="d8736-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="d8736-108">**Name**</span></span>|<span data-ttu-id="d8736-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="d8736-109">**Required/Optional**</span></span>|<span data-ttu-id="d8736-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="d8736-110">**Data Type**</span></span>|<span data-ttu-id="d8736-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d8736-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d8736-112">_width_</span><span class="sxs-lookup"><span data-stu-id="d8736-112">_width_</span></span> <br/> |<span data-ttu-id="d8736-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d8736-113">Required</span></span>  <br/> |<span data-ttu-id="d8736-114">**String**</span><span class="sxs-lookup"><span data-stu-id="d8736-114">**String**</span></span> <br/> |<span data-ttu-id="d8736-115">Ширина прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="d8736-115">Width of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="d8736-116">_height_</span><span class="sxs-lookup"><span data-stu-id="d8736-116">_height_</span></span> <br/> |<span data-ttu-id="d8736-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d8736-117">Required</span></span>  <br/> |<span data-ttu-id="d8736-118">**String**</span><span class="sxs-lookup"><span data-stu-id="d8736-118">**String**</span></span> <br/> |<span data-ttu-id="d8736-119">Высота прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="d8736-119">Height of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="d8736-120">_x_</span><span class="sxs-lookup"><span data-stu-id="d8736-120">_x_</span></span> <br/> |<span data-ttu-id="d8736-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d8736-121">Required</span></span>  <br/> |<span data-ttu-id="d8736-122">**String**</span><span class="sxs-lookup"><span data-stu-id="d8736-122">**String**</span></span> <br/> |<span data-ttu-id="d8736-123">X-coordinate.</span><span class="sxs-lookup"><span data-stu-id="d8736-123">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="d8736-124">_y_</span><span class="sxs-lookup"><span data-stu-id="d8736-124">_y_</span></span> <br/> |<span data-ttu-id="d8736-125">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d8736-125">Required</span></span>  <br/> |<span data-ttu-id="d8736-126">**String**</span><span class="sxs-lookup"><span data-stu-id="d8736-126">**String**</span></span> <br/> |<span data-ttu-id="d8736-127">y-coordinate.</span><span class="sxs-lookup"><span data-stu-id="d8736-127">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="d8736-128">_параметр_</span><span class="sxs-lookup"><span data-stu-id="d8736-128">_option_</span></span> <br/> |<span data-ttu-id="d8736-129">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d8736-129">Required</span></span>  <br/> |<span data-ttu-id="d8736-130">**Логический**</span><span class="sxs-lookup"><span data-stu-id="d8736-130">**Boolean**</span></span> <br/> |<span data-ttu-id="d8736-131">Указывает, как обрабатываются точки, которые попадают на диагонали.</span><span class="sxs-lookup"><span data-stu-id="d8736-131">Specifies how points that fall on the diagonals are treated.</span></span> <span data-ttu-id="d8736-132">Установите значение 0 для использования левого и правого секторов для точек на диагонали.</span><span class="sxs-lookup"><span data-stu-id="d8736-132">Set the value to 0 to use the left and right sectors for points on a diagonal.</span></span> <span data-ttu-id="d8736-133">Установите значение 1 для использования верхних и нижних секторов для точек на диагонали.</span><span class="sxs-lookup"><span data-stu-id="d8736-133">Set the value to 1 to use the top and bottom sectors for points on a diagonal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d8736-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="d8736-134">Remarks</span></span>

<span data-ttu-id="d8736-135">Рассмотрим прямоугольник, который  имеет ширину и высоту,  и точку *(x,y)* от центральной точки прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="d8736-135">Consider a rectangle that has a  *width*  and a  *height*  , and a point (*x,y*) from the center point of the rectangle.</span></span> <span data-ttu-id="d8736-136">Нарисуйте диагональные линии по углам прямоугольника, чтобы разделить его на четыре сектора и центрную точку.</span><span class="sxs-lookup"><span data-stu-id="d8736-136">Draw diagonal lines through the corners of the rectangle to divide it into four sectors and a center point.</span></span> <span data-ttu-id="d8736-137">Сектора от 0 до 4 представляют центр- точку, правую, верхнюю, левую и нижнюю соответственно.</span><span class="sxs-lookup"><span data-stu-id="d8736-137">The sectors 0 through 4 represent the center-point, right, top, left, and bottom respectively.</span></span> 
  
![Секторы от 0 до 4 представляют центр, правую, верхнюю, левую и нижнюю области соответственно](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a><span data-ttu-id="d8736-139">Пример</span><span class="sxs-lookup"><span data-stu-id="d8736-139">Example</span></span>

<span data-ttu-id="d8736-140">RECTSECT (1 в, 2 в, 1 в, -7 в, 0)</span><span class="sxs-lookup"><span data-stu-id="d8736-140">RECTSECT(1 in, 2 in, 1 in, -7 in, 0)</span></span> 
  
<span data-ttu-id="d8736-141">Возвращает 4.</span><span class="sxs-lookup"><span data-stu-id="d8736-141">Returns 4.</span></span> 
  

