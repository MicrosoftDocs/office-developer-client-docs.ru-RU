---
title: Функция ROUND (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251491
localization_priority: Normal
ms.assetid: a374fe7d-7302-5365-81ab-64f5474d9d5c
description: Округляет число до точности, представленное усеченное.
ms.openlocfilehash: 2457bdf6b46a2bb44b203497f02cc9b2ff034847
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/21/2018
ms.locfileid: "19814637"
---
# <a name="round-function-visioshapesheet"></a><span data-ttu-id="d759a-103">Функция ROUND (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="d759a-103">ROUND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="d759a-104">Округляет число до точности, представленное *усеченное* .</span><span class="sxs-lookup"><span data-stu-id="d759a-104">Rounds a number to the precision represented by  *numberofdigits*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d759a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d759a-105">Syntax</span></span>

<span data-ttu-id="d759a-106">ROUND (** *номер* **, ** *усеченное* **)</span><span class="sxs-lookup"><span data-stu-id="d759a-106">ROUND(** *number* **, ** *numberofdigits* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d759a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d759a-107">Parameters</span></span>

|<span data-ttu-id="d759a-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="d759a-108">**Name**</span></span>|<span data-ttu-id="d759a-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="d759a-109">**Required/Optional**</span></span>|<span data-ttu-id="d759a-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="d759a-110">**Data Type**</span></span>|<span data-ttu-id="d759a-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d759a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d759a-112">_number_</span><span class="sxs-lookup"><span data-stu-id="d759a-112">_number_</span></span> <br/> |<span data-ttu-id="d759a-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d759a-113">Required</span></span>  <br/> |<span data-ttu-id="d759a-114">**Число**</span><span class="sxs-lookup"><span data-stu-id="d759a-114">**Number**</span></span> <br/> |<span data-ttu-id="d759a-115">Номер для округления.</span><span class="sxs-lookup"><span data-stu-id="d759a-115">The number to round off.</span></span>  <br/> |
| <span data-ttu-id="d759a-116">_усеченное_</span><span class="sxs-lookup"><span data-stu-id="d759a-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="d759a-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d759a-117">Required</span></span>  <br/> |<span data-ttu-id="d759a-118">**Число**</span><span class="sxs-lookup"><span data-stu-id="d759a-118">**Number**</span></span> <br/> |<span data-ttu-id="d759a-119">Число десятичных разрядов точности.</span><span class="sxs-lookup"><span data-stu-id="d759a-119">The number of decimal places of precision.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d759a-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="d759a-120">Remarks</span></span>

<span data-ttu-id="d759a-121">Если _усеченное_ больше 0, _число_ округляется с _усеченное_ справа от десятичной запятой.</span><span class="sxs-lookup"><span data-stu-id="d759a-121">If  _numberofdigits_ is greater than 0,  _number_ is rounded by  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="d759a-122">Если _усеченное_ равно 0, _число_ округляется до целого числа.</span><span class="sxs-lookup"><span data-stu-id="d759a-122">If  _numberofdigits_ is 0,  _number_ is rounded to an integer.</span></span> <span data-ttu-id="d759a-123">Если _усеченное_ меньше 0, _число_ округляется с _усеченное_ слева от десятичной запятой.</span><span class="sxs-lookup"><span data-stu-id="d759a-123">If  _numberofdigits_ is less than 0,  _number_ is rounded by  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="d759a-124">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d759a-124">Example 1</span></span>

<span data-ttu-id="d759a-125">ROUND(123.654,2)</span><span class="sxs-lookup"><span data-stu-id="d759a-125">ROUND(123.654,2)</span></span>
  
<span data-ttu-id="d759a-126">Возвращает 123.65.</span><span class="sxs-lookup"><span data-stu-id="d759a-126">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d759a-127">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d759a-127">Example 2</span></span>

<span data-ttu-id="d759a-128">ROUND(123.654,0)</span><span class="sxs-lookup"><span data-stu-id="d759a-128">ROUND(123.654,0)</span></span>
  
<span data-ttu-id="d759a-129">Возвращает 124.</span><span class="sxs-lookup"><span data-stu-id="d759a-129">Returns 124.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="d759a-130">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d759a-130">Example 3</span></span>

<span data-ttu-id="d759a-131">ROUND(123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="d759a-131">ROUND(123.654,-1)</span></span>
  
<span data-ttu-id="d759a-132">Возвращает 120.</span><span class="sxs-lookup"><span data-stu-id="d759a-132">Returns 120.</span></span>
  

