---
title: Функция GRAVITY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251433
localization_priority: Normal
ms.assetid: db80f147-71a0-0b23-bc7e-fe1915dfdd21
description: Вычисляет правильный угол поворота текстового блока для показанного поворота фигуры, чтобы не допустить поворота текста вниз.
ms.openlocfilehash: 77c944d954292e231f8bacbe3c8a4433aad5d689
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429287"
---
# <a name="gravity-function"></a><span data-ttu-id="de7eb-103">Функция GRAVITY</span><span class="sxs-lookup"><span data-stu-id="de7eb-103">GRAVITY Function</span></span>

<span data-ttu-id="de7eb-104">Вычисляет правильный угол поворота текстового блока для показанного поворота фигуры, чтобы не допустить поворота текста вниз.</span><span class="sxs-lookup"><span data-stu-id="de7eb-104">Calculates a text block's correct angle of rotation for the indicated shape rotation to prevent the text from turning upside down.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="de7eb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de7eb-105">Syntax</span></span>

<span data-ttu-id="de7eb-106">GRAVITY(\*\* *angle* \*\*,[ \*\* *limit1* \*\* ],[ \*\* *limit2* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="de7eb-106">GRAVITY(\*\* *angle* \*\*,[ \*\* *limit1* \*\* ],[ \*\* *limit2* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="de7eb-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="de7eb-107">Parameters</span></span>

|<span data-ttu-id="de7eb-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="de7eb-108">**Name**</span></span>|<span data-ttu-id="de7eb-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="de7eb-109">**Required/Optional**</span></span>|<span data-ttu-id="de7eb-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="de7eb-110">**Data Type**</span></span>|<span data-ttu-id="de7eb-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="de7eb-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="de7eb-112">_angle_</span><span class="sxs-lookup"><span data-stu-id="de7eb-112">_angle_</span></span> <br/> |<span data-ttu-id="de7eb-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="de7eb-113">Required</span></span>  <br/> |<span data-ttu-id="de7eb-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="de7eb-114">**String**</span></span> <br/> | <span data-ttu-id="de7eb-115">Угол фигуры.</span><span class="sxs-lookup"><span data-stu-id="de7eb-115">The shape's angle.</span></span>  <br/> |
| <span data-ttu-id="de7eb-116">_limit1_</span><span class="sxs-lookup"><span data-stu-id="de7eb-116">_limit1_</span></span> <br/> |<span data-ttu-id="de7eb-117">Необязательна</span><span class="sxs-lookup"><span data-stu-id="de7eb-117">Optional</span></span>  <br/> |<span data-ttu-id="de7eb-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="de7eb-118">**String**</span></span> <br/> |<span data-ttu-id="de7eb-119">Первое ограничение поворота.</span><span class="sxs-lookup"><span data-stu-id="de7eb-119">First limit of rotation.</span></span> <span data-ttu-id="de7eb-120">Значение по умолчанию — 90 градусов.</span><span class="sxs-lookup"><span data-stu-id="de7eb-120">Default is 90 degrees.</span></span>  <br/> |
| <span data-ttu-id="de7eb-121">_limit2_</span><span class="sxs-lookup"><span data-stu-id="de7eb-121">_limit2_</span></span> <br/> |<span data-ttu-id="de7eb-122">Необязательна</span><span class="sxs-lookup"><span data-stu-id="de7eb-122">Optional</span></span>  <br/> |<span data-ttu-id="de7eb-123">**Строка**</span><span class="sxs-lookup"><span data-stu-id="de7eb-123">**String**</span></span> <br/> |<span data-ttu-id="de7eb-124">Второе ограничение поворота.</span><span class="sxs-lookup"><span data-stu-id="de7eb-124">Second limit of rotation.</span></span> <span data-ttu-id="de7eb-125">Значение по умолчанию — 270 градусов.</span><span class="sxs-lookup"><span data-stu-id="de7eb-125">Default is 270 degrees.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="de7eb-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de7eb-126">Return value</span></span>

<span data-ttu-id="de7eb-127">String</span><span class="sxs-lookup"><span data-stu-id="de7eb-127">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="de7eb-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="de7eb-128">Remarks</span></span>

<span data-ttu-id="de7eb-129">Функция GRAVITY обычно используется в ячейке TxtAngle.</span><span class="sxs-lookup"><span data-stu-id="de7eb-129">The GRAVITY function is usually used in the TxtAngle cell.</span></span> 
  
<span data-ttu-id="de7eb-130">Возвращаемая величина составляет 180  _градусов,_ если угол находится между значениями, указанными  _в limit1_ и  _limit2;_ в противном случае возвращается значение 0 градусов.</span><span class="sxs-lookup"><span data-stu-id="de7eb-130">The value returned is 180 degrees if  _angle_ is between the values specified by  _limit1_ and  _limit2_; otherwise the value returned is 0 degrees.</span></span>
  
<span data-ttu-id="de7eb-131">Все аргументы автоматически нормализуются функцией от 0 до 360 градусов.</span><span class="sxs-lookup"><span data-stu-id="de7eb-131">All of the arguments are automatically normalized between 0 and 360 degrees by the function.</span></span> <span data-ttu-id="de7eb-132">Если аргумент не указывает единицы, предполагается, что радианы.</span><span class="sxs-lookup"><span data-stu-id="de7eb-132">If an argument does not specify units, radians are assumed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="de7eb-133">Пример 1</span><span class="sxs-lookup"><span data-stu-id="de7eb-133">Example 1</span></span>

<span data-ttu-id="de7eb-134">GRAVITY(Angle)</span><span class="sxs-lookup"><span data-stu-id="de7eb-134">GRAVITY(Angle)</span></span>
  
<span data-ttu-id="de7eb-135">Возвращает 180 градусов, если  *угол*  находится от 90 до 270 градусов; в противном случае возвращается 0 градусов.</span><span class="sxs-lookup"><span data-stu-id="de7eb-135">Returns 180 degrees if  *angle*  is between 90 and 270 degrees; otherwise, returns 0 degrees.</span></span> 
  
## <a name="example-2"></a><span data-ttu-id="de7eb-136">Пример 2</span><span class="sxs-lookup"><span data-stu-id="de7eb-136">Example 2</span></span>

<span data-ttu-id="de7eb-137">GRAVITY(2)</span><span class="sxs-lookup"><span data-stu-id="de7eb-137">GRAVITY(2)</span></span>
  
<span data-ttu-id="de7eb-138">Возвращает 180 градусов, так как 2 радиана — от 90 до 270 градусов.</span><span class="sxs-lookup"><span data-stu-id="de7eb-138">Returns 180 degrees, because 2 radians is between 90 and 270 degrees.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="de7eb-139">Пример 3</span><span class="sxs-lookup"><span data-stu-id="de7eb-139">Example 3</span></span>

<span data-ttu-id="de7eb-140">GRAVITY(100 deg, 110 deg, 290 deg)</span><span class="sxs-lookup"><span data-stu-id="de7eb-140">GRAVITY(100 deg, 110 deg, 290 deg)</span></span>
  
<span data-ttu-id="de7eb-141">Возвращает 0 градусов.</span><span class="sxs-lookup"><span data-stu-id="de7eb-141">Returns 0 degrees.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="de7eb-142">Пример 4</span><span class="sxs-lookup"><span data-stu-id="de7eb-142">Example 4</span></span>

<span data-ttu-id="de7eb-143">GRAVITY(100 deg, 290 deg, 110 deg)</span><span class="sxs-lookup"><span data-stu-id="de7eb-143">GRAVITY(100 deg, 290 deg, 110 deg)</span></span>
  
<span data-ttu-id="de7eb-144">Возвращает 0 градусов.</span><span class="sxs-lookup"><span data-stu-id="de7eb-144">Returns 0 degrees.</span></span>
  

