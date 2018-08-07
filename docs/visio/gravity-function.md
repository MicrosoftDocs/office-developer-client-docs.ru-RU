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
description: Вычисляет блок текста правильный угол вращения для вращение указанного фигуры для предотвращения текст и включение сверху вниз.
ms.openlocfilehash: 0d8b0160c7e7d63fb5a272219a2694d35e6e6b61
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19813864"
---
# <a name="gravity-function"></a><span data-ttu-id="ce714-103">Функция GRAVITY</span><span class="sxs-lookup"><span data-stu-id="ce714-103">GRAVITY Function</span></span>

<span data-ttu-id="ce714-104">Вычисляет блок текста правильный угол вращения для вращение указанного фигуры для предотвращения текст и включение сверху вниз.</span><span class="sxs-lookup"><span data-stu-id="ce714-104">Calculates a text block's correct angle of rotation for the indicated shape rotation to prevent the text from turning upside down.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ce714-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce714-105">Syntax</span></span>

<span data-ttu-id="ce714-106">ВЕС (** *угол* **, [** *limit1* **], [** *limit2* **])</span><span class="sxs-lookup"><span data-stu-id="ce714-106">GRAVITY(** *angle* **,[ ** *limit1* ** ],[ ** *limit2* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ce714-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce714-107">Parameters</span></span>

|<span data-ttu-id="ce714-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="ce714-108">**Name**</span></span>|<span data-ttu-id="ce714-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="ce714-109">**Required/Optional**</span></span>|<span data-ttu-id="ce714-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="ce714-110">**Data Type**</span></span>|<span data-ttu-id="ce714-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ce714-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ce714-112">_угол_</span><span class="sxs-lookup"><span data-stu-id="ce714-112">_angle_</span></span> <br/> |<span data-ttu-id="ce714-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ce714-113">Required</span></span>  <br/> |<span data-ttu-id="ce714-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="ce714-114">**String**</span></span> <br/> | <span data-ttu-id="ce714-115">Угол фигуры.</span><span class="sxs-lookup"><span data-stu-id="ce714-115">The shape's angle.</span></span>  <br/> |
| <span data-ttu-id="ce714-116">_limit1_</span><span class="sxs-lookup"><span data-stu-id="ce714-116">_limit1_</span></span> <br/> |<span data-ttu-id="ce714-117">Optional</span><span class="sxs-lookup"><span data-stu-id="ce714-117">Optional</span></span>  <br/> |<span data-ttu-id="ce714-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="ce714-118">**String**</span></span> <br/> |<span data-ttu-id="ce714-119">Первое ограничение вращение.</span><span class="sxs-lookup"><span data-stu-id="ce714-119">First limit of rotation.</span></span> <span data-ttu-id="ce714-120">Значение по умолчанию — 90 градусов.</span><span class="sxs-lookup"><span data-stu-id="ce714-120">Default is 90 degrees.</span></span>  <br/> |
| <span data-ttu-id="ce714-121">_limit2_</span><span class="sxs-lookup"><span data-stu-id="ce714-121">_limit2_</span></span> <br/> |<span data-ttu-id="ce714-122">Optional</span><span class="sxs-lookup"><span data-stu-id="ce714-122">Optional</span></span>  <br/> |<span data-ttu-id="ce714-123">**Строка**</span><span class="sxs-lookup"><span data-stu-id="ce714-123">**String**</span></span> <br/> |<span data-ttu-id="ce714-124">Второй ограничение вращение.</span><span class="sxs-lookup"><span data-stu-id="ce714-124">Second limit of rotation.</span></span> <span data-ttu-id="ce714-125">Значение по умолчанию — на 270 градусов.</span><span class="sxs-lookup"><span data-stu-id="ce714-125">Default is 270 degrees.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ce714-126">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="ce714-126">Return value</span></span>

<span data-ttu-id="ce714-127">Строка</span><span class="sxs-lookup"><span data-stu-id="ce714-127">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ce714-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="ce714-128">Remarks</span></span>

<span data-ttu-id="ce714-129">Функция ВЕСА обычно используются в ячейке TxtAngle.</span><span class="sxs-lookup"><span data-stu-id="ce714-129">The GRAVITY function is usually used in the TxtAngle cell.</span></span> 
  
<span data-ttu-id="ce714-130">Возвращаемое значение 180 градусов при _угловая_ между значениями, указанными с _limit1_ и _limit2_; в противном случае — значение, возвращаемое — 0 градусов.</span><span class="sxs-lookup"><span data-stu-id="ce714-130">The value returned is 180 degrees if  _angle_ is between the values specified by  _limit1_ and  _limit2_; otherwise the value returned is 0 degrees.</span></span>
  
<span data-ttu-id="ce714-131">Все аргументы автоматически нормализации в диапазоне от 0 до 360 градусов с помощью функции.</span><span class="sxs-lookup"><span data-stu-id="ce714-131">All of the arguments are automatically normalized between 0 and 360 degrees by the function.</span></span> <span data-ttu-id="ce714-132">Если аргумент не указан единиц измерения, считаются радианах.</span><span class="sxs-lookup"><span data-stu-id="ce714-132">If an argument does not specify units, radians are assumed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="ce714-133">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ce714-133">Example 1</span></span>

<span data-ttu-id="ce714-134">GRAVITY(angle)</span><span class="sxs-lookup"><span data-stu-id="ce714-134">GRAVITY(Angle)</span></span>
  
<span data-ttu-id="ce714-135">Возвращает 180 градусов, если *угол* между 90 и 270 градусов; в противном случае возвращает 0 градусов.</span><span class="sxs-lookup"><span data-stu-id="ce714-135">Returns 180 degrees if  *angle*  is between 90 and 270 degrees; otherwise, returns 0 degrees.</span></span> 
  
## <a name="example-2"></a><span data-ttu-id="ce714-136">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ce714-136">Example 2</span></span>

<span data-ttu-id="ce714-137">GRAVITY(2)</span><span class="sxs-lookup"><span data-stu-id="ce714-137">GRAVITY(2)</span></span>
  
<span data-ttu-id="ce714-138">Возвращает 180 градусов, так как 2 радианах находится в пределах 90 и 270 градусов.</span><span class="sxs-lookup"><span data-stu-id="ce714-138">Returns 180 degrees, because 2 radians is between 90 and 270 degrees.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ce714-139">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ce714-139">Example 3</span></span>

<span data-ttu-id="ce714-140">ВЕС (100 градусов, 110 градусов, 290 градусов)</span><span class="sxs-lookup"><span data-stu-id="ce714-140">GRAVITY(100 deg, 110 deg, 290 deg)</span></span>
  
<span data-ttu-id="ce714-141">Возвращает 0 градусов.</span><span class="sxs-lookup"><span data-stu-id="ce714-141">Returns 0 degrees.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="ce714-142">Пример 4</span><span class="sxs-lookup"><span data-stu-id="ce714-142">Example 4</span></span>

<span data-ttu-id="ce714-143">ВЕС (100 градусов, 290 градусов, 110 градусов)</span><span class="sxs-lookup"><span data-stu-id="ce714-143">GRAVITY(100 deg, 290 deg, 110 deg)</span></span>
  
<span data-ttu-id="ce714-144">Возвращает 0 градусов.</span><span class="sxs-lookup"><span data-stu-id="ce714-144">Returns 0 degrees.</span></span>
  

