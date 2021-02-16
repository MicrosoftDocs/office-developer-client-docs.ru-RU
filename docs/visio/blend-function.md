---
title: Функция BLEND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Смешивает два цвета в пропорции, указанной параметром float.
ms.openlocfilehash: 0a231954370416be201183026424c79942204e12
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432788"
---
# <a name="blend-function"></a><span data-ttu-id="e777d-103">Функция BLEND</span><span class="sxs-lookup"><span data-stu-id="e777d-103">BLEND Function</span></span>

<span data-ttu-id="e777d-104">Смешивает два цвета в пропорции, указанной _параметром float._</span><span class="sxs-lookup"><span data-stu-id="e777d-104">Blends two colors in the proportion specified by the  _float_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e777d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e777d-105">Syntax</span></span>

<span data-ttu-id="e777d-106">BLEND(\*\* *color1* \*\*, \*\* *color2* \*\*, \*\* *float[0,1]* \*\* )</span><span class="sxs-lookup"><span data-stu-id="e777d-106">BLEND(\*\* *color1* \*\*, \*\* *color2* \*\*, \*\* *float[0,1]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e777d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e777d-107">Parameters</span></span>

|<span data-ttu-id="e777d-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="e777d-108">**Name**</span></span>|<span data-ttu-id="e777d-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="e777d-109">**Required/Optional**</span></span>|<span data-ttu-id="e777d-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="e777d-110">**Data Type**</span></span>|<span data-ttu-id="e777d-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e777d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e777d-112">_color1_</span><span class="sxs-lookup"><span data-stu-id="e777d-112">_color1_</span></span> <br/> |<span data-ttu-id="e777d-113">Обязательна</span><span class="sxs-lookup"><span data-stu-id="e777d-113">Required</span></span>  <br/> |<span data-ttu-id="e777d-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="e777d-114">**Numeric**</span></span> <br/> |<span data-ttu-id="e777d-115">Индекс цвета Visio или значение RGB первого цвета.</span><span class="sxs-lookup"><span data-stu-id="e777d-115">The Visio color index or RGB value of the first color.</span></span>  <br/> |
| <span data-ttu-id="e777d-116">_color2_</span><span class="sxs-lookup"><span data-stu-id="e777d-116">_color2_</span></span> <br/> |<span data-ttu-id="e777d-117">Обязательна</span><span class="sxs-lookup"><span data-stu-id="e777d-117">Required</span></span>  <br/> |<span data-ttu-id="e777d-118">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="e777d-118">**Numeric**</span></span> <br/> |<span data-ttu-id="e777d-119">Индекс цвета Visio или значение RGB второго цвета.</span><span class="sxs-lookup"><span data-stu-id="e777d-119">The Visio color index or RGB value of the second color.</span></span>  <br/> |
| <span data-ttu-id="e777d-120">_float[0,1]_</span><span class="sxs-lookup"><span data-stu-id="e777d-120">_float[0,1]_</span></span> <br/> |<span data-ttu-id="e777d-121">Обязательна</span><span class="sxs-lookup"><span data-stu-id="e777d-121">Required</span></span>  <br/> |<span data-ttu-id="e777d-122">**Double**</span><span class="sxs-lookup"><span data-stu-id="e777d-122">**Float**</span></span> <br/> |<span data-ttu-id="e777d-123">Пропорции для смешивания  _цветов2_  _и color1_ соответственно.</span><span class="sxs-lookup"><span data-stu-id="e777d-123">The proportion in which to blend  _color2_ and  _color1_, respectively.</span></span> <span data-ttu-id="e777d-124">Реальное число от 0 до 1 включительно.</span><span class="sxs-lookup"><span data-stu-id="e777d-124">A real number from 0 to 1 inclusive.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e777d-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e777d-125">Return value</span></span>

 <span data-ttu-id="e777d-126">**RGB**</span><span class="sxs-lookup"><span data-stu-id="e777d-126">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e777d-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="e777d-127">Remarks</span></span>

<span data-ttu-id="e777d-128">Возвращаемый цвет определяется относительным соотношением, в котором необходимо смешивать _color2_ и _color1_ соответственно, как указано в _параметре float._</span><span class="sxs-lookup"><span data-stu-id="e777d-128">The color returned is determined by the relative proportions in which to blend  _color2_ and  _color1_, respectively, as specified by the  _float_ parameter.</span></span> <span data-ttu-id="e777d-129">Например, если  _float_ составляет 0,25, возвращаемого цвета составляет 75 %  _от color1_ и 25 %  _цвета2_.</span><span class="sxs-lookup"><span data-stu-id="e777d-129">For example, if  _float_ is 0.25, the color returned is composed 75% of  _color1_ and 25% of  _color2_.</span></span> 
  
<span data-ttu-id="e777d-130">Другой способ продумать, что  значение с плавающей точкой соответствует точке спектра цветов _от color1_ до _color2._</span><span class="sxs-lookup"><span data-stu-id="e777d-130">Another way to think about it is that the  _float_ value corresponds to the point along the color spectrum from  _color1_ to  _color2_.</span></span> <span data-ttu-id="e777d-131">Таким образом, меньшие числа (ближе к нулю) для с плавающей заготовки создают смешение ближе _к color1,_ а большие числа (ближе к 1) создают смешение ближе _к color2._ </span><span class="sxs-lookup"><span data-stu-id="e777d-131">Therefore, smaller numbers (closer to zero) for  _float_ produce blends closer to  _color1_, while larger numbers (closer to 1) produce blends closer to  _color2_.</span></span>
  

