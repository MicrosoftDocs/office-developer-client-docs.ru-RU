---
title: Функция BOUNDINGBOXDIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: Возвращает измерения указанную часть фигуры, ограничивающего поля.
ms.openlocfilehash: 94cad37c4a0d2c6c7e7c69d997af09a9d7f1d651
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813310"
---
# <a name="boundingboxdist-function"></a><span data-ttu-id="6d190-103">Функция BOUNDINGBOXDIST</span><span class="sxs-lookup"><span data-stu-id="6d190-103">BOUNDINGBOXDIST Function</span></span>

<span data-ttu-id="6d190-104">Возвращает измерения указанную часть фигуры, ограничивающего поля.</span><span class="sxs-lookup"><span data-stu-id="6d190-104">Returns the measurement of the specified part of the shape's bounding box.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="6d190-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="6d190-105">Version Information</span></span>

<span data-ttu-id="6d190-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="6d190-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6d190-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d190-107">Syntax</span></span>

<span data-ttu-id="6d190-108">BOUNDINGBOXDIST (** *индекса* **)</span><span class="sxs-lookup"><span data-stu-id="6d190-108">BOUNDINGBOXDIST(** *Index* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6d190-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d190-109">Parameters</span></span>

|<span data-ttu-id="6d190-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="6d190-110">**Name**</span></span>|<span data-ttu-id="6d190-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="6d190-111">**Required/Optional**</span></span>|<span data-ttu-id="6d190-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="6d190-112">**Data Type**</span></span>|<span data-ttu-id="6d190-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6d190-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6d190-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="6d190-114">_Index_</span></span> <br/> |<span data-ttu-id="6d190-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6d190-115">Required</span></span>  <br/> |<span data-ttu-id="6d190-116">**Число**</span><span class="sxs-lookup"><span data-stu-id="6d190-116">**Number**</span></span> <br/> |<span data-ttu-id="6d190-117">Части фигуры ограничивающего прямоугольника измерения и возврата.</span><span class="sxs-lookup"><span data-stu-id="6d190-117">The part of the shape's bounding box to measure and return.</span></span> <span data-ttu-id="6d190-118">Возможные значения см.</span><span class="sxs-lookup"><span data-stu-id="6d190-118">See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="6d190-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9">Return value</span></span>

 <span data-ttu-id="6d190-120">**Число**</span><span class="sxs-lookup"><span data-stu-id="6d190-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6d190-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="6d190-121">Remarks</span></span>

 <span data-ttu-id="6d190-122">*Индекс* может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6d190-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="6d190-123">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="6d190-123">**Item**</span></span>|<span data-ttu-id="6d190-124">**Значение**</span><span class="sxs-lookup"><span data-stu-id="6d190-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6d190-125">Width</span><span class="sxs-lookup"><span data-stu-id="6d190-125">Width</span></span>  <br/> |<span data-ttu-id="6d190-126">0</span><span class="sxs-lookup"><span data-stu-id="6d190-126">0</span></span>  <br/> |
|<span data-ttu-id="6d190-127">Height</span><span class="sxs-lookup"><span data-stu-id="6d190-127">Height</span></span>  <br/> |<span data-ttu-id="6d190-128">1</span><span class="sxs-lookup"><span data-stu-id="6d190-128">1</span></span>  <br/> |
|<span data-ttu-id="6d190-129">Левая граница для фигуры</span><span class="sxs-lookup"><span data-stu-id="6d190-129">Left edge to shape pin</span></span>  <br/> |<span data-ttu-id="6d190-130">2</span><span class="sxs-lookup"><span data-stu-id="6d190-130">2</span></span>  <br/> |
|<span data-ttu-id="6d190-131">Фигура прикрепить к правому краю</span><span class="sxs-lookup"><span data-stu-id="6d190-131">Shape pin to right edge</span></span>  <br/> |<span data-ttu-id="6d190-132">3</span><span class="sxs-lookup"><span data-stu-id="6d190-132">3</span></span>  <br/> |
|<span data-ttu-id="6d190-133">Фигура прикрепить к верхнему краю</span><span class="sxs-lookup"><span data-stu-id="6d190-133">Shape pin to top edge</span></span>  <br/> |<span data-ttu-id="6d190-134">4</span><span class="sxs-lookup"><span data-stu-id="6d190-134">4</span></span>  <br/> |
|<span data-ttu-id="6d190-135">Нижняя граница для фигуры</span><span class="sxs-lookup"><span data-stu-id="6d190-135">Bottom edge to shape pin</span></span>  <br/> |<span data-ttu-id="6d190-136">5</span><span class="sxs-lookup"><span data-stu-id="6d190-136">5</span></span>  <br/> |
|<span data-ttu-id="6d190-137">Центр ограничивающих поле PinX</span><span class="sxs-lookup"><span data-stu-id="6d190-137">Center of bounding box to PinX</span></span>  <br/> |<span data-ttu-id="6d190-138">6</span><span class="sxs-lookup"><span data-stu-id="6d190-138">6</span></span>  <br/> |
|<span data-ttu-id="6d190-139">Центр ограничивающих поле PinY</span><span class="sxs-lookup"><span data-stu-id="6d190-139">Center of bounding box to PinY</span></span>  <br/> |<span data-ttu-id="6d190-140">7</span><span class="sxs-lookup"><span data-stu-id="6d190-140">7</span></span>  <br/> |
   

