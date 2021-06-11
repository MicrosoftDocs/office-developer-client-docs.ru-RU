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
description: Округляет число от 0 (ноль) до следующего экземпляра из нескольких экземпляров. Если несколько не указано, число раундов от 0 до следующей очереди.
ms.openlocfilehash: 449f17d1b68c116cccb2635723a3f6277d0ac2a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404129"
---
# <a name="ceiling-function"></a><span data-ttu-id="f043b-104">Функция CEILING</span><span class="sxs-lookup"><span data-stu-id="f043b-104">CEILING Function</span></span>

<span data-ttu-id="f043b-105">Округляет число от 0 (ноль) до следующего экземпляра с _несколькими экземплярами._</span><span class="sxs-lookup"><span data-stu-id="f043b-105">Rounds a number away from 0 (zero) to the next instance of  _multiple_.</span></span> <span data-ttu-id="f043b-106">Если  _несколько_ не указано, число раундов от 0 до следующей очереди.</span><span class="sxs-lookup"><span data-stu-id="f043b-106">If  _multiple_ is not specified, the number rounds away from 0 to the next integer.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f043b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f043b-107">Syntax</span></span>

<span data-ttu-id="f043b-108">CEILING(\*\* *number* \*\*, \*\* *multiple* \*\* )</span><span class="sxs-lookup"><span data-stu-id="f043b-108">CEILING(\*\* *number* \*\*, \*\* *multiple* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f043b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f043b-109">Parameters</span></span>

|<span data-ttu-id="f043b-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="f043b-110">**Name**</span></span>|<span data-ttu-id="f043b-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="f043b-111">**Required/Optional**</span></span>|<span data-ttu-id="f043b-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="f043b-112">**Data Type**</span></span>|<span data-ttu-id="f043b-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f043b-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f043b-114">_число_</span><span class="sxs-lookup"><span data-stu-id="f043b-114">_number_</span></span> <br/> |<span data-ttu-id="f043b-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f043b-115">Required</span></span>  <br/> |<span data-ttu-id="f043b-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="f043b-116">**Number**</span></span> <br/> |<span data-ttu-id="f043b-117">Число к округлу.</span><span class="sxs-lookup"><span data-stu-id="f043b-117">The number to round.</span></span>  <br/> |
| <span data-ttu-id="f043b-118">_несколько_</span><span class="sxs-lookup"><span data-stu-id="f043b-118">_multiple_</span></span> <br/> |<span data-ttu-id="f043b-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f043b-119">Required</span></span>  <br/> |<span data-ttu-id="f043b-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="f043b-120">**Number**</span></span> <br/> |<span data-ttu-id="f043b-121">Несколько к округл.</span><span class="sxs-lookup"><span data-stu-id="f043b-121">The multiple to round to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f043b-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="f043b-122">Remarks</span></span>

 <span data-ttu-id="f043b-123">_Число_ и  _несколько_ должны иметь одинаковые знаки или #NUM!</span><span class="sxs-lookup"><span data-stu-id="f043b-123">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="f043b-124">возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="f043b-124">error is returned.</span></span> <span data-ttu-id="f043b-125">Если число  _или_  _несколько_ не могут быть преобразованы в значение, #VALUE!</span><span class="sxs-lookup"><span data-stu-id="f043b-125">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="f043b-126">возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="f043b-126">error is returned.</span></span> <span data-ttu-id="f043b-127">Если число  _или_  _несколько_ — 0, результат — 0.</span><span class="sxs-lookup"><span data-stu-id="f043b-127">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="f043b-128">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f043b-128">Example 1</span></span>

<span data-ttu-id="f043b-129">CEILING (3.7)</span><span class="sxs-lookup"><span data-stu-id="f043b-129">CEILING(3.7)</span></span>
  
<span data-ttu-id="f043b-130">Возвращает 4</span><span class="sxs-lookup"><span data-stu-id="f043b-130">Returns 4</span></span>
  
## <a name="example-2"></a><span data-ttu-id="f043b-131">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f043b-131">Example 2</span></span>

<span data-ttu-id="f043b-132">CEILING (-3.7)</span><span class="sxs-lookup"><span data-stu-id="f043b-132">CEILING(-3.7)</span></span>
  
<span data-ttu-id="f043b-133">Возвращает -4</span><span class="sxs-lookup"><span data-stu-id="f043b-133">Returns -4</span></span>
  
## <a name="example-3"></a><span data-ttu-id="f043b-134">Пример 3</span><span class="sxs-lookup"><span data-stu-id="f043b-134">Example 3</span></span>

<span data-ttu-id="f043b-135">CEILING (3.7, 0.25)</span><span class="sxs-lookup"><span data-stu-id="f043b-135">CEILING(3.7, 0.25)</span></span>
  
<span data-ttu-id="f043b-136">Возвращает 3.75</span><span class="sxs-lookup"><span data-stu-id="f043b-136">Returns 3.75</span></span>
  

