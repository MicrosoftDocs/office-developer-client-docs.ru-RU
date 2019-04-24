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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315577"
---
# <a name="round-function-visioshapesheet"></a><span data-ttu-id="b385b-103">ROUND Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="b385b-103">ROUND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="b385b-104">Округляет число до точности, представленной *нумберофдигитс* .</span><span class="sxs-lookup"><span data-stu-id="b385b-104">Rounds a number to the precision represented by  *numberofdigits*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b385b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b385b-105">Syntax</span></span>

<span data-ttu-id="b385b-106">ROUND (\* \* *число* \* \*, \* \* *нумберофдигитс* \* \*)</span><span class="sxs-lookup"><span data-stu-id="b385b-106">ROUND(\*\* *number* \*\*, \*\* *numberofdigits* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b385b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b385b-107">Parameters</span></span>

|<span data-ttu-id="b385b-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="b385b-108">**Name**</span></span>|<span data-ttu-id="b385b-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="b385b-109">**Required/Optional**</span></span>|<span data-ttu-id="b385b-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="b385b-110">**Data Type**</span></span>|<span data-ttu-id="b385b-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b385b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b385b-112">_число_</span><span class="sxs-lookup"><span data-stu-id="b385b-112">_number_</span></span> <br/> |<span data-ttu-id="b385b-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b385b-113">Required</span></span>  <br/> |<span data-ttu-id="b385b-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="b385b-114">**Number**</span></span> <br/> |<span data-ttu-id="b385b-115">Число, которое требуется округлить.</span><span class="sxs-lookup"><span data-stu-id="b385b-115">The number to round off.</span></span>  <br/> |
| <span data-ttu-id="b385b-116">_нумберофдигитс_</span><span class="sxs-lookup"><span data-stu-id="b385b-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="b385b-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b385b-117">Required</span></span>  <br/> |<span data-ttu-id="b385b-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="b385b-118">**Number**</span></span> <br/> |<span data-ttu-id="b385b-119">Число десятичных разрядов точности.</span><span class="sxs-lookup"><span data-stu-id="b385b-119">The number of decimal places of precision.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b385b-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="b385b-120">Remarks</span></span>

<span data-ttu-id="b385b-121">Если _нумберофдигитс_ больше 0, _число_ округляется на _нумберофдигитс_ справа от десятичного разделителя.</span><span class="sxs-lookup"><span data-stu-id="b385b-121">If  _numberofdigits_ is greater than 0,  _number_ is rounded by  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="b385b-122">Если значение _нумберофдигитс_ равно 0, то _число_ округляется до целого числа.</span><span class="sxs-lookup"><span data-stu-id="b385b-122">If  _numberofdigits_ is 0,  _number_ is rounded to an integer.</span></span> <span data-ttu-id="b385b-123">Если _нумберофдигитс_ меньше 0, _число_ округляется с _нумберофдигитс_ слева от десятичного разделителя.</span><span class="sxs-lookup"><span data-stu-id="b385b-123">If  _numberofdigits_ is less than 0,  _number_ is rounded by  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="b385b-124">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b385b-124">Example 1</span></span>

<span data-ttu-id="b385b-125">ROUND (123.654, 2)</span><span class="sxs-lookup"><span data-stu-id="b385b-125">ROUND(123.654,2)</span></span>
  
<span data-ttu-id="b385b-126">Возвращает 123,65.</span><span class="sxs-lookup"><span data-stu-id="b385b-126">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="b385b-127">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b385b-127">Example 2</span></span>

<span data-ttu-id="b385b-128">ROUND (123.654, 0)</span><span class="sxs-lookup"><span data-stu-id="b385b-128">ROUND(123.654,0)</span></span>
  
<span data-ttu-id="b385b-129">Возвращает 124.</span><span class="sxs-lookup"><span data-stu-id="b385b-129">Returns 124.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="b385b-130">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b385b-130">Example 3</span></span>

<span data-ttu-id="b385b-131">ROUND (123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="b385b-131">ROUND(123.654,-1)</span></span>
  
<span data-ttu-id="b385b-132">Возвращает 120.</span><span class="sxs-lookup"><span data-stu-id="b385b-132">Returns 120.</span></span>
  

