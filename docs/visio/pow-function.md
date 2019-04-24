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
description: Возвращает число, возведенное в степень экспоненты.
ms.openlocfilehash: 7a1102aa13f54d7e323247b83af3732ebb63acf4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356051"
---
# <a name="pow-function"></a><span data-ttu-id="c124b-103">Функция POW</span><span class="sxs-lookup"><span data-stu-id="c124b-103">POW Function</span></span>

<span data-ttu-id="c124b-104">Возвращает число, возведенное в степень экспоненты.</span><span class="sxs-lookup"><span data-stu-id="c124b-104">Returns a number raised to the power of an exponent.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c124b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c124b-105">Syntax</span></span>

<span data-ttu-id="c124b-106">POW (\* \* *число* \* \*, \* \* *экспонента* \* \*)</span><span class="sxs-lookup"><span data-stu-id="c124b-106">POW(\*\* *number* \*\*, \*\* *exponent* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c124b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c124b-107">Parameters</span></span>

|<span data-ttu-id="c124b-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="c124b-108">**Name**</span></span>|<span data-ttu-id="c124b-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="c124b-109">**Required/Optional**</span></span>|<span data-ttu-id="c124b-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="c124b-110">**Data Type**</span></span>|<span data-ttu-id="c124b-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c124b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c124b-112">_число_</span><span class="sxs-lookup"><span data-stu-id="c124b-112">_number_</span></span> <br/> |<span data-ttu-id="c124b-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c124b-113">Required</span></span>  <br/> |<span data-ttu-id="c124b-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="c124b-114">**Number**</span></span> <br/> |<span data-ttu-id="c124b-115">Число, которое возводится в степень возведения в степень.</span><span class="sxs-lookup"><span data-stu-id="c124b-115">The number to raise to the power of an exponent.</span></span>  <br/> |
| <span data-ttu-id="c124b-116">_exponent_</span><span class="sxs-lookup"><span data-stu-id="c124b-116">_exponent_</span></span> <br/> |<span data-ttu-id="c124b-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c124b-117">Required</span></span>  <br/> |<span data-ttu-id="c124b-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="c124b-118">**Number**</span></span> <br/> |<span data-ttu-id="c124b-119">Показатель степени.</span><span class="sxs-lookup"><span data-stu-id="c124b-119">The exponent.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c124b-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="c124b-120">Remarks</span></span>

<span data-ttu-id="c124b-121">_Число_ и _экспонента_ могут быть не целыми числами и могут быть отрицательными.</span><span class="sxs-lookup"><span data-stu-id="c124b-121">Both  _number_ and  _exponent_ may be non-integers, and they may be negative.</span></span> <span data-ttu-id="c124b-122">Если _число_ не равно 0 и __ значение экспоненты равно 0, эта функция возвращает 1.</span><span class="sxs-lookup"><span data-stu-id="c124b-122">If  _number_ is not 0 and  _exponent_ is 0, this function returns 1.</span></span> <span data-ttu-id="c124b-123">Если _число_ равно 0 и _экспонента_ отрицательна, эта функция возвращает 0,0.</span><span class="sxs-lookup"><span data-stu-id="c124b-123">If  _number_ is 0 and  _exponent_ is negative, this function returns 0.0.</span></span> <span data-ttu-id="c124b-124">Если _число_ и _экспонента_ равны 0 или _число_ отрицательно, а _экспонента_ не является целым числом, эта функция возвращает 0,0.</span><span class="sxs-lookup"><span data-stu-id="c124b-124">If both  _number_ and  _exponent_ are 0, or if  _number_ is negative and  _exponent_ is not an integer, this function returns 0.0.</span></span> <span data-ttu-id="c124b-125">Если _число_ и _показатель степени_ отрицательны, эта функция возвращает значение – 1. #IND.</span><span class="sxs-lookup"><span data-stu-id="c124b-125">If both  _number_ and  _exponent_ are negative, this function returns -1.#IND.</span></span> 
  
## <a name="example"></a><span data-ttu-id="c124b-126">Пример</span><span class="sxs-lookup"><span data-stu-id="c124b-126">Example</span></span>

<span data-ttu-id="c124b-127">POW (5, 2)</span><span class="sxs-lookup"><span data-stu-id="c124b-127">POW(5,2)</span></span> 
  
<span data-ttu-id="c124b-128">Возвращает 25.</span><span class="sxs-lookup"><span data-stu-id="c124b-128">Returns 25.</span></span> 
  

