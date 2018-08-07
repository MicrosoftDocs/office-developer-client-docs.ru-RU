---
title: Функция BLEND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Сочетает двух цветов в пропорции, указанного с помощью параметра с плавающей запятой.
ms.openlocfilehash: 61993cea9eed6583d62004e1c756368b67c7bb33
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813276"
---
# <a name="blend-function"></a><span data-ttu-id="2d6c4-103">Функция BLEND</span><span class="sxs-lookup"><span data-stu-id="2d6c4-103">BLEND Function</span></span>

<span data-ttu-id="2d6c4-104">Сочетает двух цветов в пропорции, указанного с помощью параметра _с плавающей запятой_ .</span><span class="sxs-lookup"><span data-stu-id="2d6c4-104">Blends two colors in the proportion specified by the  _float_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2d6c4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d6c4-105">Syntax</span></span>

<span data-ttu-id="2d6c4-106">Переход (** *color1* **, ** *цвет2* **, ** *с плавающей запятой [0,1]* **)</span><span class="sxs-lookup"><span data-stu-id="2d6c4-106">BLEND(** *color1* **, ** *color2* **, ** *float[0,1]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2d6c4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2d6c4-107">Parameters</span></span>

|<span data-ttu-id="2d6c4-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="2d6c4-108">**Name**</span></span>|<span data-ttu-id="2d6c4-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="2d6c4-109">**Required/Optional**</span></span>|<span data-ttu-id="2d6c4-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="2d6c4-110">**Data Type**</span></span>|<span data-ttu-id="2d6c4-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2d6c4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2d6c4-112">_color1_</span><span class="sxs-lookup"><span data-stu-id="2d6c4-112">_color1_</span></span> <br/> |<span data-ttu-id="2d6c4-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="2d6c4-113">Required</span></span>  <br/> |<span data-ttu-id="2d6c4-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="2d6c4-114">**Numeric**</span></span> <br/> |<span data-ttu-id="2d6c4-115">Индекс цвет Visio или значение первого цвета RGB.</span><span class="sxs-lookup"><span data-stu-id="2d6c4-115">The Visio color index or RGB value of the first color.</span></span>  <br/> |
| <span data-ttu-id="2d6c4-116">_цвет2_</span><span class="sxs-lookup"><span data-stu-id="2d6c4-116">_color2_</span></span> <br/> |<span data-ttu-id="2d6c4-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="2d6c4-117">Required</span></span>  <br/> |<span data-ttu-id="2d6c4-118">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="2d6c4-118">**Numeric**</span></span> <br/> |<span data-ttu-id="2d6c4-119">Индекс цвет Visio или значение второй цвета RGB.</span><span class="sxs-lookup"><span data-stu-id="2d6c4-119">The Visio color index or RGB value of the second color.</span></span>  <br/> |
| <span data-ttu-id="2d6c4-120">_число с плавающей запятой [0,1]_</span><span class="sxs-lookup"><span data-stu-id="2d6c4-120">_float[0,1]_</span></span> <br/> |<span data-ttu-id="2d6c4-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="2d6c4-121">Required</span></span>  <br/> |<span data-ttu-id="2d6c4-122">**Double**</span><span class="sxs-lookup"><span data-stu-id="2d6c4-122">**Float**</span></span> <br/> |<span data-ttu-id="2d6c4-123">Размеры наложения _цвет2_ и _color1_соответственно.</span><span class="sxs-lookup"><span data-stu-id="2d6c4-123">The proportion in which to blend  _color2_ and  _color1_, respectively.</span></span> <span data-ttu-id="2d6c4-124">Действительное число от 0 до 1 включительно.</span><span class="sxs-lookup"><span data-stu-id="2d6c4-124">A real number from 0 to 1 inclusive.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="2d6c4-125">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="2d6c4-125">Return value</span></span>

 <span data-ttu-id="2d6c4-126">**RGB**</span><span class="sxs-lookup"><span data-stu-id="2d6c4-126">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2d6c4-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="2d6c4-127">Remarks</span></span>

<span data-ttu-id="2d6c4-128">Цвет возвращаемых определяется относительный пропорции, в котором следует наложения _цвет2_ и _color1_, соответственно, как указано в параметре _с плавающей запятой_ .</span><span class="sxs-lookup"><span data-stu-id="2d6c4-128">The color returned is determined by the relative proportions in which to blend  _color2_ and  _color1_, respectively, as specified by the  _float_ parameter.</span></span> <span data-ttu-id="2d6c4-129">Например если _число с плавающей запятой_ 0,25, возвращаемых цвет — составных 75% _color1_ и 25% _цвет2_.</span><span class="sxs-lookup"><span data-stu-id="2d6c4-129">For example, if  _float_ is 0.25, the color returned is composed 75% of  _color1_ and 25% of  _color2_.</span></span> 
  
<span data-ttu-id="2d6c4-130">Другим способом подумайте, он является, что значение _с плавающей запятой_ соответствует точка в спектре из _color1_ для _цвет2_.</span><span class="sxs-lookup"><span data-stu-id="2d6c4-130">Another way to think about it is that the  _float_ value corresponds to the point along the color spectrum from  _color1_ to  _color2_.</span></span> <span data-ttu-id="2d6c4-131">Таким образом меньшего числа (ближе к нулю) для переходов продукты _с плавающей запятой_ ближе к _color1_во время большего числа (ближе к 1) необходимо создать переходы ближе к _цвет2_.</span><span class="sxs-lookup"><span data-stu-id="2d6c4-131">Therefore, smaller numbers (closer to zero) for  _float_ produce blends closer to  _color1_, while larger numbers (closer to 1) produce blends closer to  _color2_.</span></span>
  

