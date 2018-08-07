---
title: Функция CEILING
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251405
localization_priority: Normal
ms.assetid: 1a8d6d48-7ae3-5483-28d2-5b1706088a53
description: Округляет число от 0 (ноль) до ближайшего нескольких. Если несколько не указан, число округляется от 0 до ближайшего целого числа.
ms.openlocfilehash: fa982b44ea4a73e7da614c49a52cd50efd612f20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813332"
---
# <a name="ceiling-function"></a><span data-ttu-id="00330-104">Функция CEILING</span><span class="sxs-lookup"><span data-stu-id="00330-104">CEILING Function</span></span>

<span data-ttu-id="00330-105">Округляет число от 0 (ноль) до ближайшего из _нескольких_.</span><span class="sxs-lookup"><span data-stu-id="00330-105">Rounds a number away from 0 (zero) to the next instance of  _multiple_.</span></span> <span data-ttu-id="00330-106">Если _несколько_ не указан, число округляется от 0 до ближайшего целого числа.</span><span class="sxs-lookup"><span data-stu-id="00330-106">If  _multiple_ is not specified, the number rounds away from 0 to the next integer.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="00330-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00330-107">Syntax</span></span>

<span data-ttu-id="00330-108">ПОТОЛОК (** *номер* **, ** *несколько* **)</span><span class="sxs-lookup"><span data-stu-id="00330-108">CEILING(** *number* **, ** *multiple* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="00330-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="00330-109">Parameters</span></span>

|<span data-ttu-id="00330-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="00330-110">**Name**</span></span>|<span data-ttu-id="00330-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="00330-111">**Required/Optional**</span></span>|<span data-ttu-id="00330-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="00330-112">**Data Type**</span></span>|<span data-ttu-id="00330-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="00330-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="00330-114">_number_</span><span class="sxs-lookup"><span data-stu-id="00330-114">_number_</span></span> <br/> |<span data-ttu-id="00330-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="00330-115">Required</span></span>  <br/> |<span data-ttu-id="00330-116">**Число**</span><span class="sxs-lookup"><span data-stu-id="00330-116">**Number**</span></span> <br/> |<span data-ttu-id="00330-117">Чтобы округлить число.</span><span class="sxs-lookup"><span data-stu-id="00330-117">The number to round.</span></span>  <br/> |
| <span data-ttu-id="00330-118">_несколько_</span><span class="sxs-lookup"><span data-stu-id="00330-118">_multiple_</span></span> <br/> |<span data-ttu-id="00330-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="00330-119">Required</span></span>  <br/> |<span data-ttu-id="00330-120">**Число**</span><span class="sxs-lookup"><span data-stu-id="00330-120">**Number**</span></span> <br/> |<span data-ttu-id="00330-121">Множитель для округления.</span><span class="sxs-lookup"><span data-stu-id="00330-121">The multiple to round to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00330-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="00330-122">Remarks</span></span>

 <span data-ttu-id="00330-123">_Номер_ и _нескольких_ должны иметь одинаковые знаки или #NUM!</span><span class="sxs-lookup"><span data-stu-id="00330-123">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="00330-124">возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="00330-124">error is returned.</span></span> <span data-ttu-id="00330-125">Если _номер_ или _нескольких_ невозможно преобразовать в значение #VALUE!</span><span class="sxs-lookup"><span data-stu-id="00330-125">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="00330-126">возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="00330-126">error is returned.</span></span> <span data-ttu-id="00330-127">Если _номер_ или _нескольких_ равно 0, результатом будет 0.</span><span class="sxs-lookup"><span data-stu-id="00330-127">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="00330-128">Пример 1</span><span class="sxs-lookup"><span data-stu-id="00330-128">Example 1</span></span>

<span data-ttu-id="00330-129">CEILING(3.7)</span><span class="sxs-lookup"><span data-stu-id="00330-129">CEILING(3.7)</span></span>
  
<span data-ttu-id="00330-130">Возвращает 4</span><span class="sxs-lookup"><span data-stu-id="00330-130">Returns 4</span></span>
  
## <a name="example-2"></a><span data-ttu-id="00330-131">Пример 2</span><span class="sxs-lookup"><span data-stu-id="00330-131">Example 2</span></span>

<span data-ttu-id="00330-132">CEILING(-3.7)</span><span class="sxs-lookup"><span data-stu-id="00330-132">CEILING(-3.7)</span></span>
  
<span data-ttu-id="00330-133">Возвращает -4</span><span class="sxs-lookup"><span data-stu-id="00330-133">Returns -4</span></span>
  
## <a name="example-3"></a><span data-ttu-id="00330-134">Пример 3</span><span class="sxs-lookup"><span data-stu-id="00330-134">Example 3</span></span>

<span data-ttu-id="00330-135">ПОТОЛОК (3,7, 0,25)</span><span class="sxs-lookup"><span data-stu-id="00330-135">CEILING(3.7, 0.25)</span></span>
  
<span data-ttu-id="00330-136">Возвращает 3,75</span><span class="sxs-lookup"><span data-stu-id="00330-136">Returns 3.75</span></span>
  

