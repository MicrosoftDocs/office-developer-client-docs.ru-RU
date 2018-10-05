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
description: Вычисляет сектора прямоугольника, связанный с x и y и возвращает целое число 0 до 4, указывающее сектора.
ms.openlocfilehash: fb7ed37ac498765e21c62d7180413cdbcb932502
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395086"
---
# <a name="rectsect-function"></a><span data-ttu-id="6f05d-103">Функция RECTSECT</span><span class="sxs-lookup"><span data-stu-id="6f05d-103">RECTSECT Function</span></span>

<span data-ttu-id="6f05d-104">Вычисляет сектора прямоугольника, связанный с *x* и *y* и возвращает целое число 0 до 4, указывающее сектора.</span><span class="sxs-lookup"><span data-stu-id="6f05d-104">Calculates the sector of a rectangle associated with  *x*  and  *y*  and returns an integer 0 to 4, indicating the sector.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6f05d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f05d-105">Syntax</span></span>

<span data-ttu-id="6f05d-106">RECTSECT (\*\* *ширины* \*\*, \*\* *Высота* \*\*, \*\* *x* \*\*, \*\* *y* \*\*, \*\* *параметр* \*\*)</span><span class="sxs-lookup"><span data-stu-id="6f05d-106">RECTSECT(\*\* *width* \*\*, \*\* *height* \*\*, \*\* *x* \*\*, \*\* *y* \*\*, \*\* *option* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6f05d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f05d-107">Parameters</span></span>

|<span data-ttu-id="6f05d-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="6f05d-108">**Name**</span></span>|<span data-ttu-id="6f05d-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="6f05d-109">**Required/Optional**</span></span>|<span data-ttu-id="6f05d-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="6f05d-110">**Data Type**</span></span>|<span data-ttu-id="6f05d-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6f05d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6f05d-112">_width_</span><span class="sxs-lookup"><span data-stu-id="6f05d-112">_width_</span></span> <br/> |<span data-ttu-id="6f05d-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6f05d-113">Required</span></span>  <br/> |<span data-ttu-id="6f05d-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="6f05d-114">**String**</span></span> <br/> |<span data-ttu-id="6f05d-115">Ширина прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="6f05d-115">Width of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="6f05d-116">_height_</span><span class="sxs-lookup"><span data-stu-id="6f05d-116">_height_</span></span> <br/> |<span data-ttu-id="6f05d-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6f05d-117">Required</span></span>  <br/> |<span data-ttu-id="6f05d-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="6f05d-118">**String**</span></span> <br/> |<span data-ttu-id="6f05d-119">Высота прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="6f05d-119">Height of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="6f05d-120">_x_</span><span class="sxs-lookup"><span data-stu-id="6f05d-120">_x_</span></span> <br/> |<span data-ttu-id="6f05d-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6f05d-121">Required</span></span>  <br/> |<span data-ttu-id="6f05d-122">**Строка**</span><span class="sxs-lookup"><span data-stu-id="6f05d-122">**String**</span></span> <br/> |<span data-ttu-id="6f05d-123">X координата.</span><span class="sxs-lookup"><span data-stu-id="6f05d-123">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="6f05d-124">_y_</span><span class="sxs-lookup"><span data-stu-id="6f05d-124">_y_</span></span> <br/> |<span data-ttu-id="6f05d-125">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6f05d-125">Required</span></span>  <br/> |<span data-ttu-id="6f05d-126">**Строка**</span><span class="sxs-lookup"><span data-stu-id="6f05d-126">**String**</span></span> <br/> |<span data-ttu-id="6f05d-127">Координата.</span><span class="sxs-lookup"><span data-stu-id="6f05d-127">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="6f05d-128">_параметр_</span><span class="sxs-lookup"><span data-stu-id="6f05d-128">_option_</span></span> <br/> |<span data-ttu-id="6f05d-129">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6f05d-129">Required</span></span>  <br/> |<span data-ttu-id="6f05d-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="6f05d-130">**Boolean**</span></span> <br/> |<span data-ttu-id="6f05d-131">Указывает порядок обработки точек, которые могут быть разделены на диагоналей.</span><span class="sxs-lookup"><span data-stu-id="6f05d-131">Specifies how points that fall on the diagonals are treated.</span></span> <span data-ttu-id="6f05d-132">Задайте значение 0, чтобы использовать секторов влево и вправо для указывает на вправо.</span><span class="sxs-lookup"><span data-stu-id="6f05d-132">Set the value to 0 to use the left and right sectors for points on a diagonal.</span></span> <span data-ttu-id="6f05d-133">Задайте значение 1 для использования верхних и нижних секторов для указывает на вправо.</span><span class="sxs-lookup"><span data-stu-id="6f05d-133">Set the value to 1 to use the top and bottom sectors for points on a diagonal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f05d-134">Замечания</span><span class="sxs-lookup"><span data-stu-id="6f05d-134">Remarks</span></span>

<span data-ttu-id="6f05d-135">Рассмотрите возможность прямоугольник, который имеет *ширину* и *высоту* и точка (*x, y*) из центральной точки прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="6f05d-135">Consider a rectangle that has a  *width*  and a  *height*  , and a point (*x,y*) from the center point of the rectangle.</span></span> <span data-ttu-id="6f05d-136">Рисование диагональные линии через углов прямоугольника для отделения его в четырех секторов и центральной точки.</span><span class="sxs-lookup"><span data-stu-id="6f05d-136">Draw diagonal lines through the corners of the rectangle to divide it into four sectors and a center point.</span></span> <span data-ttu-id="6f05d-137">Цифры от 0 до 4 секторов представляют центральной точки, справа, сверху, слева и вниз соответственно.</span><span class="sxs-lookup"><span data-stu-id="6f05d-137">The sectors 0 through 4 represent the center-point, right, top, left, and bottom respectively.</span></span> 
  
![Секторов цифры от 0 до 4 представляют центральной точки, справа, сверху, слева и соответственно вниз](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a><span data-ttu-id="6f05d-139">Пример</span><span class="sxs-lookup"><span data-stu-id="6f05d-139">Example</span></span>

<span data-ttu-id="6f05d-140">RECTSECT (1, 2 в, 1 в, -7 в, 0)</span><span class="sxs-lookup"><span data-stu-id="6f05d-140">RECTSECT(1 in, 2 in, 1 in, -7 in, 0)</span></span> 
  
<span data-ttu-id="6f05d-141">Возвращает 4.</span><span class="sxs-lookup"><span data-stu-id="6f05d-141">Returns 4.</span></span> 
  

