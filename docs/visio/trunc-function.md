---
title: Функция TRUNC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251508
localization_priority: Normal
ms.assetid: 62f074ef-5bf8-df1e-d826-fc1027a36501
description: Возвращает число, которое усекается до указанного количества цифр.
ms.openlocfilehash: 5b2138ff3091f70313344d5b38d8225d572d8e70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426501"
---
# <a name="trunc-function"></a><span data-ttu-id="0b6e3-103">Функция TRUNC</span><span class="sxs-lookup"><span data-stu-id="0b6e3-103">TRUNC Function</span></span>

<span data-ttu-id="0b6e3-104">Возвращает число, которое усекается до указанного количества цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-104">Returns a number truncated to the specified number of digits.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="0b6e3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b6e3-105">Syntax</span></span>

<span data-ttu-id="0b6e3-106">ОТБР (\* \* *число* \* \*, \* \* *нумберофдигитс* \* \*)</span><span class="sxs-lookup"><span data-stu-id="0b6e3-106">TRUNC(\*\* *number* \*\*, \*\* *numberofdigits* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0b6e3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0b6e3-107">Parameters</span></span>

|<span data-ttu-id="0b6e3-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="0b6e3-108">**Name**</span></span>|<span data-ttu-id="0b6e3-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="0b6e3-109">**Required/Optional**</span></span>|<span data-ttu-id="0b6e3-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="0b6e3-110">**Data Type**</span></span>|<span data-ttu-id="0b6e3-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0b6e3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0b6e3-112">_число_</span><span class="sxs-lookup"><span data-stu-id="0b6e3-112">_number_</span></span> <br/> |<span data-ttu-id="0b6e3-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0b6e3-113">Required</span></span>  <br/> |<span data-ttu-id="0b6e3-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="0b6e3-114">**Numeric**</span></span> <br/> |<span data-ttu-id="0b6e3-115">Число, которое необходимо усечь.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-115">The number to truncate.</span></span>  <br/> |
| <span data-ttu-id="0b6e3-116">_нумберофдигитс_</span><span class="sxs-lookup"><span data-stu-id="0b6e3-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="0b6e3-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0b6e3-117">Required</span></span>  <br/> |<span data-ttu-id="0b6e3-118">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="0b6e3-118">**Numeric**</span></span> <br/> |<span data-ttu-id="0b6e3-119">Количество цифр, на которые усекается _число_.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-119">The number of digits to which to truncate  _number_.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="0b6e3-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0b6e3-120">Return value</span></span>

<span data-ttu-id="0b6e3-121">Числовых.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-121">Numeric.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0b6e3-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="0b6e3-122">Remarks</span></span>

<span data-ttu-id="0b6e3-123">Если _нумберофдигитс_ больше 0, _число_ усекается до _нумберофдигитс_ справа от десятичного разделителя.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-123">If  _numberofdigits_ is greater than 0,  _number_ is truncated to  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="0b6e3-124">Если _нумберофдигитс_ имеет значение 0, _число_ усекается до целого.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-124">If  _numberofdigits_ is 0,  _number_ is truncated to an integer.</span></span> <span data-ttu-id="0b6e3-125">Если _нумберофдигитс_ меньше 0, _число_ усекается до _нумберофдигитс_ слева от десятичного разделителя.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-125">If  _numberofdigits_ is less than 0,  _number_ is truncated to  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="0b6e3-126">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0b6e3-126">Example 1</span></span>

<span data-ttu-id="0b6e3-127">ОТБР (123.654, 2)</span><span class="sxs-lookup"><span data-stu-id="0b6e3-127">TRUNC(123.654,2)</span></span>
  
<span data-ttu-id="0b6e3-128">Возвращает 123,65.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-128">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="0b6e3-129">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0b6e3-129">Example 2</span></span>

<span data-ttu-id="0b6e3-130">ОТБР (123.654, 0)</span><span class="sxs-lookup"><span data-stu-id="0b6e3-130">TRUNC(123.654,0)</span></span>
  
<span data-ttu-id="0b6e3-131">Возвращает 123.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-131">Returns 123.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="0b6e3-132">Пример 3</span><span class="sxs-lookup"><span data-stu-id="0b6e3-132">Example 3</span></span>

<span data-ttu-id="0b6e3-133">ОТБР (123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="0b6e3-133">TRUNC(123.654,-1)</span></span>
  
<span data-ttu-id="0b6e3-134">Возвращает 120.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-134">Returns 120.</span></span>
  

