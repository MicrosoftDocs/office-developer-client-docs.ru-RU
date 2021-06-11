---
title: Функция BOUNDINGBOXDIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: Возвращает измерение указанной части окне границы фигуры.
ms.openlocfilehash: a62d5b82c310e7b99e16b70982b75a68172b7fd8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428279"
---
# <a name="boundingboxdist-function"></a><span data-ttu-id="bf5f7-103">Функция BOUNDINGBOXDIST</span><span class="sxs-lookup"><span data-stu-id="bf5f7-103">BOUNDINGBOXDIST Function</span></span>

<span data-ttu-id="bf5f7-104">Возвращает измерение указанной части окне границы фигуры.</span><span class="sxs-lookup"><span data-stu-id="bf5f7-104">Returns the measurement of the specified part of the shape's bounding box.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="bf5f7-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="bf5f7-105">Version Information</span></span>

<span data-ttu-id="bf5f7-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="bf5f7-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="bf5f7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf5f7-107">Syntax</span></span>

<span data-ttu-id="bf5f7-108">BOUNDINGBOXDIST(\*\* *Index* \*\* )</span><span class="sxs-lookup"><span data-stu-id="bf5f7-108">BOUNDINGBOXDIST(\*\* *Index* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="bf5f7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf5f7-109">Parameters</span></span>

|<span data-ttu-id="bf5f7-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="bf5f7-110">**Name**</span></span>|<span data-ttu-id="bf5f7-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="bf5f7-111">**Required/Optional**</span></span>|<span data-ttu-id="bf5f7-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="bf5f7-112">**Data Type**</span></span>|<span data-ttu-id="bf5f7-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bf5f7-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bf5f7-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="bf5f7-114">_Index_</span></span> <br/> |<span data-ttu-id="bf5f7-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bf5f7-115">Required</span></span>  <br/> |<span data-ttu-id="bf5f7-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="bf5f7-116">**Number**</span></span> <br/> |<span data-ttu-id="bf5f7-117">Часть связанного окна фигуры для измерения и возврата.</span><span class="sxs-lookup"><span data-stu-id="bf5f7-117">The part of the shape's bounding box to measure and return.</span></span> <span data-ttu-id="bf5f7-118">См. примечание для возможных значений.</span><span class="sxs-lookup"><span data-stu-id="bf5f7-118">See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="bf5f7-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf5f7-119">Return value</span></span>

 <span data-ttu-id="bf5f7-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="bf5f7-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bf5f7-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="bf5f7-121">Remarks</span></span>

 <span data-ttu-id="bf5f7-122">*Индекс*  может быть одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="bf5f7-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="bf5f7-123">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="bf5f7-123">**Item**</span></span>|<span data-ttu-id="bf5f7-124">**Значение**</span><span class="sxs-lookup"><span data-stu-id="bf5f7-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bf5f7-125">Width</span><span class="sxs-lookup"><span data-stu-id="bf5f7-125">Width</span></span>  <br/> |<span data-ttu-id="bf5f7-126">0</span><span class="sxs-lookup"><span data-stu-id="bf5f7-126">0</span></span>  <br/> |
|<span data-ttu-id="bf5f7-127">Height</span><span class="sxs-lookup"><span data-stu-id="bf5f7-127">Height</span></span>  <br/> |<span data-ttu-id="bf5f7-128">1</span><span class="sxs-lookup"><span data-stu-id="bf5f7-128">1</span></span>  <br/> |
|<span data-ttu-id="bf5f7-129">Левый край для фигуры пин-кода</span><span class="sxs-lookup"><span data-stu-id="bf5f7-129">Left edge to shape pin</span></span>  <br/> |<span data-ttu-id="bf5f7-130">2</span><span class="sxs-lookup"><span data-stu-id="bf5f7-130">2</span></span>  <br/> |
|<span data-ttu-id="bf5f7-131">Пин-код формы к правому краю</span><span class="sxs-lookup"><span data-stu-id="bf5f7-131">Shape pin to right edge</span></span>  <br/> |<span data-ttu-id="bf5f7-132">3</span><span class="sxs-lookup"><span data-stu-id="bf5f7-132">3</span></span>  <br/> |
|<span data-ttu-id="bf5f7-133">Пин-код формы до верхнего края</span><span class="sxs-lookup"><span data-stu-id="bf5f7-133">Shape pin to top edge</span></span>  <br/> |<span data-ttu-id="bf5f7-134">4 </span><span class="sxs-lookup"><span data-stu-id="bf5f7-134">4</span></span>  <br/> |
|<span data-ttu-id="bf5f7-135">Нижний край для фигуры пин-кода</span><span class="sxs-lookup"><span data-stu-id="bf5f7-135">Bottom edge to shape pin</span></span>  <br/> |<span data-ttu-id="bf5f7-136">5 </span><span class="sxs-lookup"><span data-stu-id="bf5f7-136">5</span></span>  <br/> |
|<span data-ttu-id="bf5f7-137">Центр связанного окна с PinX</span><span class="sxs-lookup"><span data-stu-id="bf5f7-137">Center of bounding box to PinX</span></span>  <br/> |<span data-ttu-id="bf5f7-138">6 </span><span class="sxs-lookup"><span data-stu-id="bf5f7-138">6</span></span>  <br/> |
|<span data-ttu-id="bf5f7-139">Центр связанного окна с PinY</span><span class="sxs-lookup"><span data-stu-id="bf5f7-139">Center of bounding box to PinY</span></span>  <br/> |<span data-ttu-id="bf5f7-140">7 </span><span class="sxs-lookup"><span data-stu-id="bf5f7-140">7</span></span>  <br/> |
   

