---
title: Функция POW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251483
localization_priority: Normal
ms.assetid: c6519c55-5f98-ed0d-95b1-5443d0d23c0b
description: Возвращает число, поднятые в силу экспонента.
ms.openlocfilehash: 7a1102aa13f54d7e323247b83af3732ebb63acf4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406313"
---
# <a name="pow-function"></a><span data-ttu-id="2b208-103">Функция POW</span><span class="sxs-lookup"><span data-stu-id="2b208-103">POW Function</span></span>

<span data-ttu-id="2b208-104">Возвращает число, поднятые в силу экспонента.</span><span class="sxs-lookup"><span data-stu-id="2b208-104">Returns a number raised to the power of an exponent.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="2b208-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b208-105">Syntax</span></span>

<span data-ttu-id="2b208-106">POW(\*\* *number* \*\*, \*\* *exponent* \*\* )</span><span class="sxs-lookup"><span data-stu-id="2b208-106">POW(\*\* *number* \*\*, \*\* *exponent* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2b208-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b208-107">Parameters</span></span>

|<span data-ttu-id="2b208-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="2b208-108">**Name**</span></span>|<span data-ttu-id="2b208-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="2b208-109">**Required/Optional**</span></span>|<span data-ttu-id="2b208-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="2b208-110">**Data Type**</span></span>|<span data-ttu-id="2b208-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2b208-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2b208-112">_число_</span><span class="sxs-lookup"><span data-stu-id="2b208-112">_number_</span></span> <br/> |<span data-ttu-id="2b208-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="2b208-113">Required</span></span>  <br/> |<span data-ttu-id="2b208-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="2b208-114">**Number**</span></span> <br/> |<span data-ttu-id="2b208-115">Число, необходимое для повышения до мощности экспонента.</span><span class="sxs-lookup"><span data-stu-id="2b208-115">The number to raise to the power of an exponent.</span></span>  <br/> |
| <span data-ttu-id="2b208-116">_exponent_</span><span class="sxs-lookup"><span data-stu-id="2b208-116">_exponent_</span></span> <br/> |<span data-ttu-id="2b208-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="2b208-117">Required</span></span>  <br/> |<span data-ttu-id="2b208-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="2b208-118">**Number**</span></span> <br/> |<span data-ttu-id="2b208-119">Экспонент.</span><span class="sxs-lookup"><span data-stu-id="2b208-119">The exponent.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b208-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="2b208-120">Remarks</span></span>

<span data-ttu-id="2b208-121">Число  _и_  _показатель могут_ быть неинтеграционными, и они могут быть отрицательными.</span><span class="sxs-lookup"><span data-stu-id="2b208-121">Both  _number_ and  _exponent_ may be non-integers, and they may be negative.</span></span> <span data-ttu-id="2b208-122">Если  _число_ не 0,  _а показатель_ 0, эта функция возвращает 1.</span><span class="sxs-lookup"><span data-stu-id="2b208-122">If  _number_ is not 0 and  _exponent_ is 0, this function returns 1.</span></span> <span data-ttu-id="2b208-123">Если  _число_ 0 и  _показатель_ отрицательный, эта функция возвращает 0.0.</span><span class="sxs-lookup"><span data-stu-id="2b208-123">If  _number_ is 0 and  _exponent_ is negative, this function returns 0.0.</span></span> <span data-ttu-id="2b208-124">Если и _число,_ и _показатель_ 0, или  если число отрицательное и показатель не является integer, эта функция возвращает 0.0. </span><span class="sxs-lookup"><span data-stu-id="2b208-124">If both  _number_ and  _exponent_ are 0, or if  _number_ is negative and  _exponent_ is not an integer, this function returns 0.0.</span></span> <span data-ttu-id="2b208-125">Если и  _число,_ и  _показатель_ отрицательные, эта функция возвращает -1.#IND.</span><span class="sxs-lookup"><span data-stu-id="2b208-125">If both  _number_ and  _exponent_ are negative, this function returns -1.#IND.</span></span> 
  
## <a name="example"></a><span data-ttu-id="2b208-126">Пример</span><span class="sxs-lookup"><span data-stu-id="2b208-126">Example</span></span>

<span data-ttu-id="2b208-127">POW (5,2)</span><span class="sxs-lookup"><span data-stu-id="2b208-127">POW(5,2)</span></span> 
  
<span data-ttu-id="2b208-128">Возвращает 25.</span><span class="sxs-lookup"><span data-stu-id="2b208-128">Returns 25.</span></span> 
  

