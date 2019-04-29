---
title: Функция FLOOR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251423
localization_priority: Normal
ms.assetid: 6788bc96-cc86-5f21-781f-67274e7f605a
description: Округляет число в сторону 0 (ноль), на следующее целое число или на следующий экземпляр множителя.
ms.openlocfilehash: 7a16a77a990180f34dd7a5706c24ec3232438467
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439900"
---
# <a name="floor-function"></a><span data-ttu-id="8d57d-103">Функция FLOOR</span><span class="sxs-lookup"><span data-stu-id="8d57d-103">FLOOR Function</span></span>

<span data-ttu-id="8d57d-104">Округляет число в сторону 0 (ноль), на следующее целое число или на следующий экземпляр _множителя_.</span><span class="sxs-lookup"><span data-stu-id="8d57d-104">Rounds a number toward 0 (zero), to the next integer, or to the next instance of  _multiple_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="8d57d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d57d-105">Syntax</span></span>

<span data-ttu-id="8d57d-106">FLOOR (\* \* *число* \* \*, \* \* *несколько* \* \*)</span><span class="sxs-lookup"><span data-stu-id="8d57d-106">FLOOR(\*\* *number* \*\*, \*\* *multiple* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8d57d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d57d-107">Parameters</span></span>

|<span data-ttu-id="8d57d-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="8d57d-108">**Name**</span></span>|<span data-ttu-id="8d57d-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="8d57d-109">**Required/Optional**</span></span>|<span data-ttu-id="8d57d-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="8d57d-110">**Data Type**</span></span>|<span data-ttu-id="8d57d-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8d57d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8d57d-112">_число_</span><span class="sxs-lookup"><span data-stu-id="8d57d-112">_number_</span></span> <br/> |<span data-ttu-id="8d57d-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8d57d-113">Required</span></span>  <br/> |<span data-ttu-id="8d57d-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="8d57d-114">**Number**</span></span> <br/> |<span data-ttu-id="8d57d-115">Округляемое число.</span><span class="sxs-lookup"><span data-stu-id="8d57d-115">The number to round.</span></span>  <br/> |
| <span data-ttu-id="8d57d-116">_сразу_</span><span class="sxs-lookup"><span data-stu-id="8d57d-116">_multiple_</span></span> <br/> |<span data-ttu-id="8d57d-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8d57d-117">Required</span></span>  <br/> |<span data-ttu-id="8d57d-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="8d57d-118">**Number**</span></span> <br/> |<span data-ttu-id="8d57d-119">Точность, с которой округляется.</span><span class="sxs-lookup"><span data-stu-id="8d57d-119">The multiple to which to round.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8d57d-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d57d-120">Return value</span></span>

<span data-ttu-id="8d57d-121">Число</span><span class="sxs-lookup"><span data-stu-id="8d57d-121">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8d57d-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="8d57d-122">Remarks</span></span>

<span data-ttu-id="8d57d-123">Если не указано значение _Multiple_ , число округляется до 0 до следующего целого числа.</span><span class="sxs-lookup"><span data-stu-id="8d57d-123">If  _multiple_ is not specified, the number rounds toward 0 to the next integer.</span></span> 
  
 <span data-ttu-id="8d57d-124">_Число_ и _множество_ должны иметь одинаковые знаки или #NUM!</span><span class="sxs-lookup"><span data-stu-id="8d57d-124">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="8d57d-125">возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="8d57d-125">error is returned.</span></span> <span data-ttu-id="8d57d-126">Если один или _несколько_ _чисел_ не могут быть преобразованы в значение, то #VALUE!</span><span class="sxs-lookup"><span data-stu-id="8d57d-126">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="8d57d-127">возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="8d57d-127">error is returned.</span></span> <span data-ttu-id="8d57d-128">Если один или _несколько_ _чисел_ имеют значение 0, результат равен 0.</span><span class="sxs-lookup"><span data-stu-id="8d57d-128">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="8d57d-129">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8d57d-129">Example 1</span></span>

<span data-ttu-id="8d57d-130">ПОЛ (3.7)</span><span class="sxs-lookup"><span data-stu-id="8d57d-130">FLOOR(3.7)</span></span>
  
<span data-ttu-id="8d57d-131">Возвращает значение 3.</span><span class="sxs-lookup"><span data-stu-id="8d57d-131">Returns 3.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="8d57d-132">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8d57d-132">Example 2</span></span>

<span data-ttu-id="8d57d-133">FLOOR (-3,7)</span><span class="sxs-lookup"><span data-stu-id="8d57d-133">FLOOR(-3.7)</span></span>
  
<span data-ttu-id="8d57d-134">Возвращает значение 3.</span><span class="sxs-lookup"><span data-stu-id="8d57d-134">Returns -3.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="8d57d-135">Пример 3</span><span class="sxs-lookup"><span data-stu-id="8d57d-135">Example 3</span></span>

<span data-ttu-id="8d57d-136">FLOOR (3.7, 0,5)</span><span class="sxs-lookup"><span data-stu-id="8d57d-136">FLOOR(3.7, 0.5)</span></span>
  
<span data-ttu-id="8d57d-137">Возвращает 3,5.</span><span class="sxs-lookup"><span data-stu-id="8d57d-137">Returns 3.5.</span></span>
  

