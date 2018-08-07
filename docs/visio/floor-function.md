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
description: Округляет число в сторону нуль (0), целого или до ближайшего нескольких.
ms.openlocfilehash: f66b993e3ab48fd1abc685b7db5889d5bf24fbfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813774"
---
# <a name="floor-function"></a><span data-ttu-id="0988c-103">Функция FLOOR</span><span class="sxs-lookup"><span data-stu-id="0988c-103">FLOOR Function</span></span>

<span data-ttu-id="0988c-104">Округляет число в сторону нуль (0), целого или до ближайшего из _нескольких_.</span><span class="sxs-lookup"><span data-stu-id="0988c-104">Rounds a number toward 0 (zero), to the next integer, or to the next instance of  _multiple_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="0988c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0988c-105">Syntax</span></span>

<span data-ttu-id="0988c-106">ЭТАЖА (** *номер* **, ** *несколько* **)</span><span class="sxs-lookup"><span data-stu-id="0988c-106">FLOOR(** *number* **, ** *multiple* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0988c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0988c-107">Parameters</span></span>

|<span data-ttu-id="0988c-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="0988c-108">**Name**</span></span>|<span data-ttu-id="0988c-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="0988c-109">**Required/Optional**</span></span>|<span data-ttu-id="0988c-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="0988c-110">**Data Type**</span></span>|<span data-ttu-id="0988c-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0988c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0988c-112">_number_</span><span class="sxs-lookup"><span data-stu-id="0988c-112">_number_</span></span> <br/> |<span data-ttu-id="0988c-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0988c-113">Required</span></span>  <br/> |<span data-ttu-id="0988c-114">**Число**</span><span class="sxs-lookup"><span data-stu-id="0988c-114">**Number**</span></span> <br/> |<span data-ttu-id="0988c-115">Чтобы округлить число.</span><span class="sxs-lookup"><span data-stu-id="0988c-115">The number to round.</span></span>  <br/> |
| <span data-ttu-id="0988c-116">_несколько_</span><span class="sxs-lookup"><span data-stu-id="0988c-116">_multiple_</span></span> <br/> |<span data-ttu-id="0988c-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0988c-117">Required</span></span>  <br/> |<span data-ttu-id="0988c-118">**Число**</span><span class="sxs-lookup"><span data-stu-id="0988c-118">**Number**</span></span> <br/> |<span data-ttu-id="0988c-119">Множитель, к которому следует округлить.</span><span class="sxs-lookup"><span data-stu-id="0988c-119">The multiple to which to round.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="0988c-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0">Return value</span></span>

<span data-ttu-id="0988c-121">Number</span><span class="sxs-lookup"><span data-stu-id="0988c-121">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0988c-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="0988c-122">Remarks</span></span>

<span data-ttu-id="0988c-123">Если _несколько_ не указан, число округляется к 0 до ближайшего целого числа.</span><span class="sxs-lookup"><span data-stu-id="0988c-123">If  _multiple_ is not specified, the number rounds toward 0 to the next integer.</span></span> 
  
 <span data-ttu-id="0988c-124">_Номер_ и _нескольких_ должны иметь одинаковые знаки или #NUM!</span><span class="sxs-lookup"><span data-stu-id="0988c-124">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="0988c-125">возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="0988c-125">error is returned.</span></span> <span data-ttu-id="0988c-126">Если _номер_ или _нескольких_ невозможно преобразовать в значение #VALUE!</span><span class="sxs-lookup"><span data-stu-id="0988c-126">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="0988c-127">возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="0988c-127">error is returned.</span></span> <span data-ttu-id="0988c-128">Если _номер_ или _нескольких_ равно 0, результатом будет 0.</span><span class="sxs-lookup"><span data-stu-id="0988c-128">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="0988c-129">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0988c-129">Example 1</span></span>

<span data-ttu-id="0988c-130">FLOOR(3.7)</span><span class="sxs-lookup"><span data-stu-id="0988c-130">FLOOR(3.7)</span></span>
  
<span data-ttu-id="0988c-131">Возврат значения 3.</span><span class="sxs-lookup"><span data-stu-id="0988c-131">Returns 3.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="0988c-132">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0988c-132">Example 2</span></span>

<span data-ttu-id="0988c-133">FLOOR(-3.7)</span><span class="sxs-lookup"><span data-stu-id="0988c-133">FLOOR(-3.7)</span></span>
  
<span data-ttu-id="0988c-134">Возвращает -3.</span><span class="sxs-lookup"><span data-stu-id="0988c-134">Returns -3.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="0988c-135">Пример 3</span><span class="sxs-lookup"><span data-stu-id="0988c-135">Example 3</span></span>

<span data-ttu-id="0988c-136">ЭТАЖА (3,7, 0,5)</span><span class="sxs-lookup"><span data-stu-id="0988c-136">FLOOR(3.7, 0.5)</span></span>
  
<span data-ttu-id="0988c-137">Возвращает 3.5.</span><span class="sxs-lookup"><span data-stu-id="0988c-137">Returns 3.5.</span></span>
  

