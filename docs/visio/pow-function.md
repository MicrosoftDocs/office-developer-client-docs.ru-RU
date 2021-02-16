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
description: Возвращает число, подавленное в силу экспонента.
ms.openlocfilehash: 7a1102aa13f54d7e323247b83af3732ebb63acf4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406313"
---
# <a name="pow-function"></a><span data-ttu-id="4a507-103">Функция POW</span><span class="sxs-lookup"><span data-stu-id="4a507-103">POW Function</span></span>

<span data-ttu-id="4a507-104">Возвращает число, подавленное в силу экспонента.</span><span class="sxs-lookup"><span data-stu-id="4a507-104">Returns a number raised to the power of an exponent.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="4a507-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a507-105">Syntax</span></span>

<span data-ttu-id="4a507-106">POW(\*\* *number* \*\*, \*\* *exponent* \*\* )</span><span class="sxs-lookup"><span data-stu-id="4a507-106">POW(\*\* *number* \*\*, \*\* *exponent* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4a507-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a507-107">Parameters</span></span>

|<span data-ttu-id="4a507-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="4a507-108">**Name**</span></span>|<span data-ttu-id="4a507-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="4a507-109">**Required/Optional**</span></span>|<span data-ttu-id="4a507-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="4a507-110">**Data Type**</span></span>|<span data-ttu-id="4a507-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4a507-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4a507-112">_число_</span><span class="sxs-lookup"><span data-stu-id="4a507-112">_number_</span></span> <br/> |<span data-ttu-id="4a507-113">Обязательна</span><span class="sxs-lookup"><span data-stu-id="4a507-113">Required</span></span>  <br/> |<span data-ttu-id="4a507-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="4a507-114">**Number**</span></span> <br/> |<span data-ttu-id="4a507-115">Число, поднимаемого до мощности экспонента.</span><span class="sxs-lookup"><span data-stu-id="4a507-115">The number to raise to the power of an exponent.</span></span>  <br/> |
| <span data-ttu-id="4a507-116">_exponent_</span><span class="sxs-lookup"><span data-stu-id="4a507-116">_exponent_</span></span> <br/> |<span data-ttu-id="4a507-117">Обязательна</span><span class="sxs-lookup"><span data-stu-id="4a507-117">Required</span></span>  <br/> |<span data-ttu-id="4a507-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="4a507-118">**Number**</span></span> <br/> |<span data-ttu-id="4a507-119">Экспонент.</span><span class="sxs-lookup"><span data-stu-id="4a507-119">The exponent.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a507-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="4a507-120">Remarks</span></span>

<span data-ttu-id="4a507-121">Число  _и_  _экспоненты_ могут быть неинтеграционными, а они могут быть отрицательными.</span><span class="sxs-lookup"><span data-stu-id="4a507-121">Both  _number_ and  _exponent_ may be non-integers, and they may be negative.</span></span> <span data-ttu-id="4a507-122">Если  _число_ не 0, а  _показатель exponent_ — 0, эта функция возвращает 1.</span><span class="sxs-lookup"><span data-stu-id="4a507-122">If  _number_ is not 0 and  _exponent_ is 0, this function returns 1.</span></span> <span data-ttu-id="4a507-123">Если  _число_ — 0,  _а показатель exponent_ отрицательный, эта функция возвращает 0,0.</span><span class="sxs-lookup"><span data-stu-id="4a507-123">If  _number_ is 0 and  _exponent_ is negative, this function returns 0.0.</span></span> <span data-ttu-id="4a507-124">Если и _число,_ и _экспоненты_  — 0, или если число отрицательное и _экспоненент_ не является числом, эта функция возвращает 0,0.</span><span class="sxs-lookup"><span data-stu-id="4a507-124">If both  _number_ and  _exponent_ are 0, or if  _number_ is negative and  _exponent_ is not an integer, this function returns 0.0.</span></span> <span data-ttu-id="4a507-125">Если и  _число,_ и  _экспоненты_ отрицательные, эта функция возвращает -1,#IND.</span><span class="sxs-lookup"><span data-stu-id="4a507-125">If both  _number_ and  _exponent_ are negative, this function returns -1.#IND.</span></span> 
  
## <a name="example"></a><span data-ttu-id="4a507-126">Пример</span><span class="sxs-lookup"><span data-stu-id="4a507-126">Example</span></span>

<span data-ttu-id="4a507-127">POW(5,2)</span><span class="sxs-lookup"><span data-stu-id="4a507-127">POW(5,2)</span></span> 
  
<span data-ttu-id="4a507-128">Возвращает 25.</span><span class="sxs-lookup"><span data-stu-id="4a507-128">Returns 25.</span></span> 
  

