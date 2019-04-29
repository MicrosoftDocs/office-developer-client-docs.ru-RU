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
description: Вычисляет правильный угол вращения блока текста для указанного поворота фигуры, чтобы предотвратить переворачивание текста.
ms.openlocfilehash: 77c944d954292e231f8bacbe3c8a4433aad5d689
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429287"
---
# <a name="gravity-function"></a><span data-ttu-id="7f5e5-103">Функция GRAVITY</span><span class="sxs-lookup"><span data-stu-id="7f5e5-103">GRAVITY Function</span></span>

<span data-ttu-id="7f5e5-104">Вычисляет правильный угол вращения блока текста для указанного поворота фигуры, чтобы предотвратить переворачивание текста.</span><span class="sxs-lookup"><span data-stu-id="7f5e5-104">Calculates a text block's correct angle of rotation for the indicated shape rotation to prevent the text from turning upside down.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="7f5e5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f5e5-105">Syntax</span></span>

<span data-ttu-id="7f5e5-106">Сила притяжения (\* \* *угол* \* *, [* \* *ограничено1* \* *], [* \* *limit2* \* \*])</span><span class="sxs-lookup"><span data-stu-id="7f5e5-106">GRAVITY(\*\* *angle* \*\*,[ \*\* *limit1* \*\* ],[ \*\* *limit2* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7f5e5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f5e5-107">Parameters</span></span>

|<span data-ttu-id="7f5e5-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="7f5e5-108">**Name**</span></span>|<span data-ttu-id="7f5e5-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="7f5e5-109">**Required/Optional**</span></span>|<span data-ttu-id="7f5e5-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="7f5e5-110">**Data Type**</span></span>|<span data-ttu-id="7f5e5-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7f5e5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7f5e5-112">_градусов_</span><span class="sxs-lookup"><span data-stu-id="7f5e5-112">_angle_</span></span> <br/> |<span data-ttu-id="7f5e5-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7f5e5-113">Required</span></span>  <br/> |<span data-ttu-id="7f5e5-114">**String**</span><span class="sxs-lookup"><span data-stu-id="7f5e5-114">**String**</span></span> <br/> | <span data-ttu-id="7f5e5-115">Угол фигуры.</span><span class="sxs-lookup"><span data-stu-id="7f5e5-115">The shape's angle.</span></span>  <br/> |
| <span data-ttu-id="7f5e5-116">_ограничено1_</span><span class="sxs-lookup"><span data-stu-id="7f5e5-116">_limit1_</span></span> <br/> |<span data-ttu-id="7f5e5-117">Необязательный</span><span class="sxs-lookup"><span data-stu-id="7f5e5-117">Optional</span></span>  <br/> |<span data-ttu-id="7f5e5-118">**String**</span><span class="sxs-lookup"><span data-stu-id="7f5e5-118">**String**</span></span> <br/> |<span data-ttu-id="7f5e5-119">Первое предельное значение поворота.</span><span class="sxs-lookup"><span data-stu-id="7f5e5-119">First limit of rotation.</span></span> <span data-ttu-id="7f5e5-120">Значение по умолчанию — 90 градусов.</span><span class="sxs-lookup"><span data-stu-id="7f5e5-120">Default is 90 degrees.</span></span>  <br/> |
| <span data-ttu-id="7f5e5-121">_limit2_</span><span class="sxs-lookup"><span data-stu-id="7f5e5-121">_limit2_</span></span> <br/> |<span data-ttu-id="7f5e5-122">Необязательный</span><span class="sxs-lookup"><span data-stu-id="7f5e5-122">Optional</span></span>  <br/> |<span data-ttu-id="7f5e5-123">**String**</span><span class="sxs-lookup"><span data-stu-id="7f5e5-123">**String**</span></span> <br/> |<span data-ttu-id="7f5e5-124">Второй лимит вращения.</span><span class="sxs-lookup"><span data-stu-id="7f5e5-124">Second limit of rotation.</span></span> <span data-ttu-id="7f5e5-125">Значение по умолчанию — 270 градусов.</span><span class="sxs-lookup"><span data-stu-id="7f5e5-125">Default is 270 degrees.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="7f5e5-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f5e5-126">Return value</span></span>

<span data-ttu-id="7f5e5-127">String</span><span class="sxs-lookup"><span data-stu-id="7f5e5-127">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7f5e5-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="7f5e5-128">Remarks</span></span>

<span data-ttu-id="7f5e5-129">Функция сила ПРИТЯЖЕНИя обычно используется в ячейке TxtAngle.</span><span class="sxs-lookup"><span data-stu-id="7f5e5-129">The GRAVITY function is usually used in the TxtAngle cell.</span></span> 
  
<span data-ttu-id="7f5e5-130">Возвращаемое значение равно 180 градусов, если _угол_ между значениями, указанными в _ограничено1_ и _limit2_; в противном случае возвращаемое значение равно 0 градусов.</span><span class="sxs-lookup"><span data-stu-id="7f5e5-130">The value returned is 180 degrees if  _angle_ is between the values specified by  _limit1_ and  _limit2_; otherwise the value returned is 0 degrees.</span></span>
  
<span data-ttu-id="7f5e5-131">Все аргументы автоматически нормализованы в пределах от 0 до 360 градусов по функциям.</span><span class="sxs-lookup"><span data-stu-id="7f5e5-131">All of the arguments are automatically normalized between 0 and 360 degrees by the function.</span></span> <span data-ttu-id="7f5e5-132">Если аргумент не указывает единицы, предполагается, что используются радианы.</span><span class="sxs-lookup"><span data-stu-id="7f5e5-132">If an argument does not specify units, radians are assumed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="7f5e5-133">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7f5e5-133">Example 1</span></span>

<span data-ttu-id="7f5e5-134">СИЛА ПРИТЯЖЕНИя (угол)</span><span class="sxs-lookup"><span data-stu-id="7f5e5-134">GRAVITY(Angle)</span></span>
  
<span data-ttu-id="7f5e5-135">Возвращает 180 градусов, если *угол* находится в пределах от 90 до 270 градусов; в противном случае возвращает 0 градусов.</span><span class="sxs-lookup"><span data-stu-id="7f5e5-135">Returns 180 degrees if  *angle*  is between 90 and 270 degrees; otherwise, returns 0 degrees.</span></span> 
  
## <a name="example-2"></a><span data-ttu-id="7f5e5-136">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7f5e5-136">Example 2</span></span>

<span data-ttu-id="7f5e5-137">СИЛА ПРИТЯЖЕНИЯ (2)</span><span class="sxs-lookup"><span data-stu-id="7f5e5-137">GRAVITY(2)</span></span>
  
<span data-ttu-id="7f5e5-138">Возвращает значение 180 градусов, так как 2 радианы находятся в диапазоне от 90 до 270 градусов.</span><span class="sxs-lookup"><span data-stu-id="7f5e5-138">Returns 180 degrees, because 2 radians is between 90 and 270 degrees.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="7f5e5-139">Пример 3</span><span class="sxs-lookup"><span data-stu-id="7f5e5-139">Example 3</span></span>

<span data-ttu-id="7f5e5-140">СИЛА ПРИТЯЖЕНИя (100 градусов, 110 град, 290 градусов)</span><span class="sxs-lookup"><span data-stu-id="7f5e5-140">GRAVITY(100 deg, 110 deg, 290 deg)</span></span>
  
<span data-ttu-id="7f5e5-141">Возвращает 0 градусов.</span><span class="sxs-lookup"><span data-stu-id="7f5e5-141">Returns 0 degrees.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="7f5e5-142">Пример 4</span><span class="sxs-lookup"><span data-stu-id="7f5e5-142">Example 4</span></span>

<span data-ttu-id="7f5e5-143">СИЛА ПРИТЯЖЕНИя (100 градусов, 290 град, 110 градусов)</span><span class="sxs-lookup"><span data-stu-id="7f5e5-143">GRAVITY(100 deg, 290 deg, 110 deg)</span></span>
  
<span data-ttu-id="7f5e5-144">Возвращает 0 градусов.</span><span class="sxs-lookup"><span data-stu-id="7f5e5-144">Returns 0 degrees.</span></span>
  

