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
description: Округлит число в сторону 0 (ноль), в следующий ряд или в следующий экземпляр из нескольких экземпляров.
ms.openlocfilehash: 7a16a77a990180f34dd7a5706c24ec3232438467
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439900"
---
# <a name="floor-function"></a><span data-ttu-id="01284-103">Функция FLOOR</span><span class="sxs-lookup"><span data-stu-id="01284-103">FLOOR Function</span></span>

<span data-ttu-id="01284-104">Округлит число к 0 (ноль), к следующему экземпляру или к следующему экземпляру _из нескольких экземпляров._</span><span class="sxs-lookup"><span data-stu-id="01284-104">Rounds a number toward 0 (zero), to the next integer, or to the next instance of  _multiple_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="01284-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01284-105">Syntax</span></span>

<span data-ttu-id="01284-106">FLOOR(\*\* *номер* \*\*, \*\* *несколько* \*\* )</span><span class="sxs-lookup"><span data-stu-id="01284-106">FLOOR(\*\* *number* \*\*, \*\* *multiple* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="01284-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="01284-107">Parameters</span></span>

|<span data-ttu-id="01284-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="01284-108">**Name**</span></span>|<span data-ttu-id="01284-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="01284-109">**Required/Optional**</span></span>|<span data-ttu-id="01284-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="01284-110">**Data Type**</span></span>|<span data-ttu-id="01284-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="01284-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="01284-112">_число_</span><span class="sxs-lookup"><span data-stu-id="01284-112">_number_</span></span> <br/> |<span data-ttu-id="01284-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="01284-113">Required</span></span>  <br/> |<span data-ttu-id="01284-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="01284-114">**Number**</span></span> <br/> |<span data-ttu-id="01284-115">Число к округлу.</span><span class="sxs-lookup"><span data-stu-id="01284-115">The number to round.</span></span>  <br/> |
| <span data-ttu-id="01284-116">_несколько_</span><span class="sxs-lookup"><span data-stu-id="01284-116">_multiple_</span></span> <br/> |<span data-ttu-id="01284-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="01284-117">Required</span></span>  <br/> |<span data-ttu-id="01284-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="01284-118">**Number**</span></span> <br/> |<span data-ttu-id="01284-119">Множестве, к которому можно округлиться.</span><span class="sxs-lookup"><span data-stu-id="01284-119">The multiple to which to round.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="01284-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01284-120">Return value</span></span>

<span data-ttu-id="01284-121">Номер</span><span class="sxs-lookup"><span data-stu-id="01284-121">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="01284-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="01284-122">Remarks</span></span>

<span data-ttu-id="01284-123">Если  _несколько_ не указано, число округлится до 0 к следующему ряду.</span><span class="sxs-lookup"><span data-stu-id="01284-123">If  _multiple_ is not specified, the number rounds toward 0 to the next integer.</span></span> 
  
 <span data-ttu-id="01284-124">_Число_ и  _несколько_ должны иметь одинаковые знаки или #NUM!</span><span class="sxs-lookup"><span data-stu-id="01284-124">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="01284-125">возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="01284-125">error is returned.</span></span> <span data-ttu-id="01284-126">Если число  _или_  _несколько_ не могут быть преобразованы в значение, #VALUE!</span><span class="sxs-lookup"><span data-stu-id="01284-126">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="01284-127">возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="01284-127">error is returned.</span></span> <span data-ttu-id="01284-128">Если число  _или_  _несколько_ — 0, результат — 0.</span><span class="sxs-lookup"><span data-stu-id="01284-128">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="01284-129">Пример 1</span><span class="sxs-lookup"><span data-stu-id="01284-129">Example 1</span></span>

<span data-ttu-id="01284-130">FLOOR (3.7)</span><span class="sxs-lookup"><span data-stu-id="01284-130">FLOOR(3.7)</span></span>
  
<span data-ttu-id="01284-131">Возвращает 3.</span><span class="sxs-lookup"><span data-stu-id="01284-131">Returns 3.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="01284-132">Пример 2</span><span class="sxs-lookup"><span data-stu-id="01284-132">Example 2</span></span>

<span data-ttu-id="01284-133">FLOOR (-3.7)</span><span class="sxs-lookup"><span data-stu-id="01284-133">FLOOR(-3.7)</span></span>
  
<span data-ttu-id="01284-134">Возвращает -3.</span><span class="sxs-lookup"><span data-stu-id="01284-134">Returns -3.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="01284-135">Пример 3</span><span class="sxs-lookup"><span data-stu-id="01284-135">Example 3</span></span>

<span data-ttu-id="01284-136">FLOOR (3.7, 0.5)</span><span class="sxs-lookup"><span data-stu-id="01284-136">FLOOR(3.7, 0.5)</span></span>
  
<span data-ttu-id="01284-137">Возвращает 3.5.</span><span class="sxs-lookup"><span data-stu-id="01284-137">Returns 3.5.</span></span>
  

