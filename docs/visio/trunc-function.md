---
title: Функция ОТБР
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251508
localization_priority: Normal
ms.assetid: 62f074ef-5bf8-df1e-d826-fc1027a36501
description: Возвращает число сокращается до указанного количества десятичных разрядов.
ms.openlocfilehash: 8f6a9798391d308a234469d93bc8f481de5fc8da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815065"
---
# <a name="trunc-function"></a><span data-ttu-id="9448a-103">Функция ОТБР</span><span class="sxs-lookup"><span data-stu-id="9448a-103">TRUNC Function</span></span>

<span data-ttu-id="9448a-104">Возвращает число сокращается до указанного количества десятичных разрядов.</span><span class="sxs-lookup"><span data-stu-id="9448a-104">Returns a number truncated to the specified number of digits.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="9448a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9448a-105">Syntax</span></span>

<span data-ttu-id="9448a-106">ОТБР (** *номер* **, ** *усеченное* **)</span><span class="sxs-lookup"><span data-stu-id="9448a-106">TRUNC(** *number* **, ** *numberofdigits* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9448a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9448a-107">Parameters</span></span>

|<span data-ttu-id="9448a-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="9448a-108">**Name**</span></span>|<span data-ttu-id="9448a-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="9448a-109">**Required/Optional**</span></span>|<span data-ttu-id="9448a-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="9448a-110">**Data Type**</span></span>|<span data-ttu-id="9448a-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9448a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9448a-112">_number_</span><span class="sxs-lookup"><span data-stu-id="9448a-112">_number_</span></span> <br/> |<span data-ttu-id="9448a-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9448a-113">Required</span></span>  <br/> |<span data-ttu-id="9448a-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="9448a-114">**Numeric**</span></span> <br/> |<span data-ttu-id="9448a-115">Номер для усечения.</span><span class="sxs-lookup"><span data-stu-id="9448a-115">The number to truncate.</span></span>  <br/> |
| <span data-ttu-id="9448a-116">_усеченное_</span><span class="sxs-lookup"><span data-stu-id="9448a-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="9448a-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9448a-117">Required</span></span>  <br/> |<span data-ttu-id="9448a-118">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="9448a-118">**Numeric**</span></span> <br/> |<span data-ttu-id="9448a-119">Количество цифр, к которому следует усекать _номер_.</span><span class="sxs-lookup"><span data-stu-id="9448a-119">The number of digits to which to truncate  _number_.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="9448a-120">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="9448a-120">Return value</span></span>

<span data-ttu-id="9448a-121">Числовой.</span><span class="sxs-lookup"><span data-stu-id="9448a-121">Numeric.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9448a-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="9448a-122">Remarks</span></span>

<span data-ttu-id="9448a-123">_Если _усеченное_ больше 0, оно округляется в _усеченное_ справа от десятичной запятой._</span><span class="sxs-lookup"><span data-stu-id="9448a-123">If  _numberofdigits_ is greater than 0,  _number_ is truncated to  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="9448a-124">Если _усеченное_ равно 0, _число_ усекается до целого числа.</span><span class="sxs-lookup"><span data-stu-id="9448a-124">If  _numberofdigits_ is 0,  _number_ is truncated to an integer.</span></span> <span data-ttu-id="9448a-125">_Если _усеченное_ меньше 0, оно округляется в _усеченное_ слева от десятичной запятой._</span><span class="sxs-lookup"><span data-stu-id="9448a-125">If  _numberofdigits_ is less than 0,  _number_ is truncated to  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="9448a-126">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9448a-126">Example 1</span></span>

<span data-ttu-id="9448a-127">TRUNC(123.654,2)</span><span class="sxs-lookup"><span data-stu-id="9448a-127">TRUNC(123.654,2)</span></span>
  
<span data-ttu-id="9448a-128">Возвращает 123.65.</span><span class="sxs-lookup"><span data-stu-id="9448a-128">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="9448a-129">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9448a-129">Example 2</span></span>

<span data-ttu-id="9448a-130">TRUNC(123.654,0)</span><span class="sxs-lookup"><span data-stu-id="9448a-130">TRUNC(123.654,0)</span></span>
  
<span data-ttu-id="9448a-131">Возвращает 123.</span><span class="sxs-lookup"><span data-stu-id="9448a-131">Returns 123.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="9448a-132">Пример 3</span><span class="sxs-lookup"><span data-stu-id="9448a-132">Example 3</span></span>

<span data-ttu-id="9448a-133">TRUNC(123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="9448a-133">TRUNC(123.654,-1)</span></span>
  
<span data-ttu-id="9448a-134">Возвращает 120.</span><span class="sxs-lookup"><span data-stu-id="9448a-134">Returns 120.</span></span>
  

