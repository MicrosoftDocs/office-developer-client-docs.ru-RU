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
description: Возвращает числа, возведенного в степень экспоненты.
ms.openlocfilehash: 48870c679251a666a5756b2b684d262fe059eee0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814478"
---
# <a name="pow-function"></a><span data-ttu-id="51449-103">Функция POW</span><span class="sxs-lookup"><span data-stu-id="51449-103">POW Function</span></span>

<span data-ttu-id="51449-104">Возвращает числа, возведенного в степень экспоненты.</span><span class="sxs-lookup"><span data-stu-id="51449-104">Returns a number raised to the power of an exponent.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="51449-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51449-105">Syntax</span></span>

<span data-ttu-id="51449-106">POW (** *номер* **, ** *степени* **)</span><span class="sxs-lookup"><span data-stu-id="51449-106">POW(** *number* **, ** *exponent* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="51449-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="51449-107">Parameters</span></span>

|<span data-ttu-id="51449-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="51449-108">**Name**</span></span>|<span data-ttu-id="51449-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="51449-109">**Required/Optional**</span></span>|<span data-ttu-id="51449-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="51449-110">**Data Type**</span></span>|<span data-ttu-id="51449-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="51449-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="51449-112">_number_</span><span class="sxs-lookup"><span data-stu-id="51449-112">_number_</span></span> <br/> |<span data-ttu-id="51449-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="51449-113">Required</span></span>  <br/> |<span data-ttu-id="51449-114">**Число**</span><span class="sxs-lookup"><span data-stu-id="51449-114">**Number**</span></span> <br/> |<span data-ttu-id="51449-115">Номер для возведения в степень экспоненты.</span><span class="sxs-lookup"><span data-stu-id="51449-115">The number to raise to the power of an exponent.</span></span>  <br/> |
| <span data-ttu-id="51449-116">_exponent_</span><span class="sxs-lookup"><span data-stu-id="51449-116">_exponent_</span></span> <br/> |<span data-ttu-id="51449-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="51449-117">Required</span></span>  <br/> |<span data-ttu-id="51449-118">**Число**</span><span class="sxs-lookup"><span data-stu-id="51449-118">**Number**</span></span> <br/> |<span data-ttu-id="51449-119">Степень.</span><span class="sxs-lookup"><span data-stu-id="51449-119">The exponent.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51449-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="51449-120">Remarks</span></span>

<span data-ttu-id="51449-121">_Номер_ и _степени_ может быть не целые числа и может быть отрицательным.</span><span class="sxs-lookup"><span data-stu-id="51449-121">Both  _number_ and  _exponent_ may be non-integers, and they may be negative.</span></span> <span data-ttu-id="51449-122">Если _номер_ не 0 и _степени_ равно 0, эта функция возвращает 1.</span><span class="sxs-lookup"><span data-stu-id="51449-122">If  _number_ is not 0 and  _exponent_ is 0, this function returns 1.</span></span> <span data-ttu-id="51449-123">Если _число_ равняется 0 и _степени_ является отрицательным, эта функция возвращает 0,0.</span><span class="sxs-lookup"><span data-stu-id="51449-123">If  _number_ is 0 and  _exponent_ is negative, this function returns 0.0.</span></span> <span data-ttu-id="51449-124">Если _номер_ и _степень_ , 0 или _число_ является отрицательным и _степени_ не является целым числом, эта функция возвращает 0,0.</span><span class="sxs-lookup"><span data-stu-id="51449-124">If both  _number_ and  _exponent_ are 0, or if  _number_ is negative and  _exponent_ is not an integer, this function returns 0.0.</span></span> <span data-ttu-id="51449-125">Если отрицательные _числа_ и _степень_ , эта функция возвращает значение -1. #IND.</span><span class="sxs-lookup"><span data-stu-id="51449-125">If both  _number_ and  _exponent_ are negative, this function returns -1.#IND.</span></span> 
  
## <a name="example"></a><span data-ttu-id="51449-126">Пример</span><span class="sxs-lookup"><span data-stu-id="51449-126">Example</span></span>

<span data-ttu-id="51449-127">POW(5,2)</span><span class="sxs-lookup"><span data-stu-id="51449-127">POW(5,2)</span></span> 
  
<span data-ttu-id="51449-128">Возвращает 25.</span><span class="sxs-lookup"><span data-stu-id="51449-128">Returns 25.</span></span> 
  

