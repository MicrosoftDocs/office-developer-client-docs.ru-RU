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
description: Округлит число до точности, представленной числомofdigits.
ms.openlocfilehash: 6795cbc4d99e293da06c0ec369d2cefb84f9f5b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439970"
---
# <a name="round-function-visioshapesheet"></a><span data-ttu-id="0a516-103">ROUND Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="0a516-103">ROUND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="0a516-104">Округлит число до точности, представленной *числомofdigits.*</span><span class="sxs-lookup"><span data-stu-id="0a516-104">Rounds a number to the precision represented by  *numberofdigits*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0a516-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a516-105">Syntax</span></span>

<span data-ttu-id="0a516-106">ROUND(\*\* *number* \*\*, \*\* *numberofdigits* \*\* )</span><span class="sxs-lookup"><span data-stu-id="0a516-106">ROUND(\*\* *number* \*\*, \*\* *numberofdigits* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0a516-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0a516-107">Parameters</span></span>

|<span data-ttu-id="0a516-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="0a516-108">**Name**</span></span>|<span data-ttu-id="0a516-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="0a516-109">**Required/Optional**</span></span>|<span data-ttu-id="0a516-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="0a516-110">**Data Type**</span></span>|<span data-ttu-id="0a516-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0a516-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0a516-112">_число_</span><span class="sxs-lookup"><span data-stu-id="0a516-112">_number_</span></span> <br/> |<span data-ttu-id="0a516-113">Обязательна</span><span class="sxs-lookup"><span data-stu-id="0a516-113">Required</span></span>  <br/> |<span data-ttu-id="0a516-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="0a516-114">**Number**</span></span> <br/> |<span data-ttu-id="0a516-115">Номер, который необходимо округить.</span><span class="sxs-lookup"><span data-stu-id="0a516-115">The number to round off.</span></span>  <br/> |
| <span data-ttu-id="0a516-116">_numberofdigits_</span><span class="sxs-lookup"><span data-stu-id="0a516-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="0a516-117">Обязательна</span><span class="sxs-lookup"><span data-stu-id="0a516-117">Required</span></span>  <br/> |<span data-ttu-id="0a516-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="0a516-118">**Number**</span></span> <br/> |<span data-ttu-id="0a516-119">Количество десятичных мест точности.</span><span class="sxs-lookup"><span data-stu-id="0a516-119">The number of decimal places of precision.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a516-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="0a516-120">Remarks</span></span>

<span data-ttu-id="0a516-121">Если _числоofdigits_ больше 0,  число округляется _числомofdigits_ справа от десятичной заголовки.</span><span class="sxs-lookup"><span data-stu-id="0a516-121">If  _numberofdigits_ is greater than 0,  _number_ is rounded by  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="0a516-122">Если  _numberofdigits_ имеет 0,  _число_ округлится до integer.</span><span class="sxs-lookup"><span data-stu-id="0a516-122">If  _numberofdigits_ is 0,  _number_ is rounded to an integer.</span></span> <span data-ttu-id="0a516-123">Если _числоofdigits_ меньше 0,  число округляется _числомofdigits_ слева от десятичной заголовки.</span><span class="sxs-lookup"><span data-stu-id="0a516-123">If  _numberofdigits_ is less than 0,  _number_ is rounded by  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="0a516-124">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0a516-124">Example 1</span></span>

<span data-ttu-id="0a516-125">ROUND(123.654,2)</span><span class="sxs-lookup"><span data-stu-id="0a516-125">ROUND(123.654,2)</span></span>
  
<span data-ttu-id="0a516-126">Возвращает 123,65.</span><span class="sxs-lookup"><span data-stu-id="0a516-126">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="0a516-127">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0a516-127">Example 2</span></span>

<span data-ttu-id="0a516-128">ROUND(123.654,0)</span><span class="sxs-lookup"><span data-stu-id="0a516-128">ROUND(123.654,0)</span></span>
  
<span data-ttu-id="0a516-129">Возвращает 124.</span><span class="sxs-lookup"><span data-stu-id="0a516-129">Returns 124.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="0a516-130">Пример 3</span><span class="sxs-lookup"><span data-stu-id="0a516-130">Example 3</span></span>

<span data-ttu-id="0a516-131">ROUND(123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="0a516-131">ROUND(123.654,-1)</span></span>
  
<span data-ttu-id="0a516-132">Возвращает 120.</span><span class="sxs-lookup"><span data-stu-id="0a516-132">Returns 120.</span></span>
  

