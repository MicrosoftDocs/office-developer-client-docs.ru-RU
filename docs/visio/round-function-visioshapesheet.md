---
title: ROUND Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251491
localization_priority: Normal
ms.assetid: a374fe7d-7302-5365-81ab-64f5474d9d5c
description: Округляет число до точности, представленной нумберофдигитс.
ms.openlocfilehash: 6795cbc4d99e293da06c0ec369d2cefb84f9f5b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439970"
---
# <a name="round-function-visioshapesheet"></a><span data-ttu-id="7d250-103">ROUND Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="7d250-103">ROUND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="7d250-104">Округляет число до точности, представленной *нумберофдигитс* .</span><span class="sxs-lookup"><span data-stu-id="7d250-104">Rounds a number to the precision represented by  *numberofdigits*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7d250-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d250-105">Syntax</span></span>

<span data-ttu-id="7d250-106">ROUND (\* \* *число* \* \*, \* \* *нумберофдигитс* \* \*)</span><span class="sxs-lookup"><span data-stu-id="7d250-106">ROUND(\*\* *number* \*\*, \*\* *numberofdigits* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7d250-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d250-107">Parameters</span></span>

|<span data-ttu-id="7d250-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="7d250-108">**Name**</span></span>|<span data-ttu-id="7d250-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="7d250-109">**Required/Optional**</span></span>|<span data-ttu-id="7d250-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="7d250-110">**Data Type**</span></span>|<span data-ttu-id="7d250-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7d250-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7d250-112">_число_</span><span class="sxs-lookup"><span data-stu-id="7d250-112">_number_</span></span> <br/> |<span data-ttu-id="7d250-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7d250-113">Required</span></span>  <br/> |<span data-ttu-id="7d250-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="7d250-114">**Number**</span></span> <br/> |<span data-ttu-id="7d250-115">Число, которое требуется округлить.</span><span class="sxs-lookup"><span data-stu-id="7d250-115">The number to round off.</span></span>  <br/> |
| <span data-ttu-id="7d250-116">_нумберофдигитс_</span><span class="sxs-lookup"><span data-stu-id="7d250-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="7d250-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7d250-117">Required</span></span>  <br/> |<span data-ttu-id="7d250-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="7d250-118">**Number**</span></span> <br/> |<span data-ttu-id="7d250-119">Число десятичных разрядов точности.</span><span class="sxs-lookup"><span data-stu-id="7d250-119">The number of decimal places of precision.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d250-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="7d250-120">Remarks</span></span>

<span data-ttu-id="7d250-121">Если _нумберофдигитс_ больше 0, _число_ округляется на _нумберофдигитс_ справа от десятичного разделителя.</span><span class="sxs-lookup"><span data-stu-id="7d250-121">If  _numberofdigits_ is greater than 0,  _number_ is rounded by  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="7d250-122">Если значение _нумберофдигитс_ равно 0, то _число_ округляется до целого числа.</span><span class="sxs-lookup"><span data-stu-id="7d250-122">If  _numberofdigits_ is 0,  _number_ is rounded to an integer.</span></span> <span data-ttu-id="7d250-123">Если _нумберофдигитс_ меньше 0, _число_ округляется с _нумберофдигитс_ слева от десятичного разделителя.</span><span class="sxs-lookup"><span data-stu-id="7d250-123">If  _numberofdigits_ is less than 0,  _number_ is rounded by  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="7d250-124">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7d250-124">Example 1</span></span>

<span data-ttu-id="7d250-125">ROUND (123.654, 2)</span><span class="sxs-lookup"><span data-stu-id="7d250-125">ROUND(123.654,2)</span></span>
  
<span data-ttu-id="7d250-126">Возвращает 123,65.</span><span class="sxs-lookup"><span data-stu-id="7d250-126">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="7d250-127">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7d250-127">Example 2</span></span>

<span data-ttu-id="7d250-128">ROUND (123.654, 0)</span><span class="sxs-lookup"><span data-stu-id="7d250-128">ROUND(123.654,0)</span></span>
  
<span data-ttu-id="7d250-129">Возвращает 124.</span><span class="sxs-lookup"><span data-stu-id="7d250-129">Returns 124.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="7d250-130">Пример 3</span><span class="sxs-lookup"><span data-stu-id="7d250-130">Example 3</span></span>

<span data-ttu-id="7d250-131">ROUND (123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="7d250-131">ROUND(123.654,-1)</span></span>
  
<span data-ttu-id="7d250-132">Возвращает 120.</span><span class="sxs-lookup"><span data-stu-id="7d250-132">Returns 120.</span></span>
  

