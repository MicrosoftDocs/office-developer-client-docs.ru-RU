---
title: Функция BLEND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Смешивает два цвета в соответствии с пропорциями, указанными в параметре float.
ms.openlocfilehash: 0a231954370416be201183026424c79942204e12
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303299"
---
# <a name="blend-function"></a><span data-ttu-id="00658-103">Функция BLEND</span><span class="sxs-lookup"><span data-stu-id="00658-103">BLEND Function</span></span>

<span data-ttu-id="00658-104">Смешивает два цвета в соответствии с пропорциями, указанными в параметре _float_ .</span><span class="sxs-lookup"><span data-stu-id="00658-104">Blends two colors in the proportion specified by the  _float_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="00658-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00658-105">Syntax</span></span>

<span data-ttu-id="00658-106">BLEND (\* \* *color1* \* \*, \* \* *color2* \* \*, \* \* *float [0, 1]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="00658-106">BLEND(\*\* *color1* \*\*, \*\* *color2* \*\*, \*\* *float[0,1]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="00658-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="00658-107">Parameters</span></span>

|<span data-ttu-id="00658-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="00658-108">**Name**</span></span>|<span data-ttu-id="00658-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="00658-109">**Required/Optional**</span></span>|<span data-ttu-id="00658-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="00658-110">**Data Type**</span></span>|<span data-ttu-id="00658-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="00658-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="00658-112">_color1_</span><span class="sxs-lookup"><span data-stu-id="00658-112">_color1_</span></span> <br/> |<span data-ttu-id="00658-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="00658-113">Required</span></span>  <br/> |<span data-ttu-id="00658-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="00658-114">**Numeric**</span></span> <br/> |<span data-ttu-id="00658-115">Цветовой индекс Visio или значение RGB для первого цвета.</span><span class="sxs-lookup"><span data-stu-id="00658-115">The Visio color index or RGB value of the first color.</span></span>  <br/> |
| <span data-ttu-id="00658-116">_color2_</span><span class="sxs-lookup"><span data-stu-id="00658-116">_color2_</span></span> <br/> |<span data-ttu-id="00658-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="00658-117">Required</span></span>  <br/> |<span data-ttu-id="00658-118">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="00658-118">**Numeric**</span></span> <br/> |<span data-ttu-id="00658-119">Цветовой индекс Visio или значение RGB второго цвета.</span><span class="sxs-lookup"><span data-stu-id="00658-119">The Visio color index or RGB value of the second color.</span></span>  <br/> |
| <span data-ttu-id="00658-120">_float [0, 1]_</span><span class="sxs-lookup"><span data-stu-id="00658-120">_float[0,1]_</span></span> <br/> |<span data-ttu-id="00658-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="00658-121">Required</span></span>  <br/> |<span data-ttu-id="00658-122">**Double**</span><span class="sxs-lookup"><span data-stu-id="00658-122">**Float**</span></span> <br/> |<span data-ttu-id="00658-123">Пропорция, в которой накладываются _color2_ и _color1_соответственно.</span><span class="sxs-lookup"><span data-stu-id="00658-123">The proportion in which to blend  _color2_ and  _color1_, respectively.</span></span> <span data-ttu-id="00658-124">Вещественное число от 0 до 1 включительно.</span><span class="sxs-lookup"><span data-stu-id="00658-124">A real number from 0 to 1 inclusive.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="00658-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="00658-125">Return value</span></span>

 <span data-ttu-id="00658-126">**RGB**</span><span class="sxs-lookup"><span data-stu-id="00658-126">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="00658-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="00658-127">Remarks</span></span>

<span data-ttu-id="00658-128">Возвращаемый цвет определяется относительными пропорциями, в которых выполняется смешение _color2_ и _color1_, соответственно, как указано параметром _float_ .</span><span class="sxs-lookup"><span data-stu-id="00658-128">The color returned is determined by the relative proportions in which to blend  _color2_ and  _color1_, respectively, as specified by the  _float_ parameter.</span></span> <span data-ttu-id="00658-129">Например, если значение _float_ равно 0,25, возвращаемый цвет составляет 75% от _color1_ и 25% от _color2_.</span><span class="sxs-lookup"><span data-stu-id="00658-129">For example, if  _float_ is 0.25, the color returned is composed 75% of  _color1_ and 25% of  _color2_.</span></span> 
  
<span data-ttu-id="00658-130">Еще один способ обдумать то, что значение _float_ соответствует точке цветового спектра из _color1_ в _color2_.</span><span class="sxs-lookup"><span data-stu-id="00658-130">Another way to think about it is that the  _float_ value corresponds to the point along the color spectrum from  _color1_ to  _color2_.</span></span> <span data-ttu-id="00658-131">Таким образом, меньшее число (ближе к нулю __ ) для наложения накладывается ближе к _color1_, а большее число (ближе к 1) приводит к переходу ближе к _color2_.</span><span class="sxs-lookup"><span data-stu-id="00658-131">Therefore, smaller numbers (closer to zero) for  _float_ produce blends closer to  _color1_, while larger numbers (closer to 1) produce blends closer to  _color2_.</span></span>
  

