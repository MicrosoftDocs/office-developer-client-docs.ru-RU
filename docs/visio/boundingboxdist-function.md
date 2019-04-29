---
title: Функция BOUNDINGBOXDIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: Возвращает единицу измерения указанной части ограничительной рамки фигуры.
ms.openlocfilehash: a62d5b82c310e7b99e16b70982b75a68172b7fd8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428279"
---
# <a name="boundingboxdist-function"></a><span data-ttu-id="8ed42-103">Функция BOUNDINGBOXDIST</span><span class="sxs-lookup"><span data-stu-id="8ed42-103">BOUNDINGBOXDIST Function</span></span>

<span data-ttu-id="8ed42-104">Возвращает единицу измерения указанной части ограничительной рамки фигуры.</span><span class="sxs-lookup"><span data-stu-id="8ed42-104">Returns the measurement of the specified part of the shape's bounding box.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="8ed42-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="8ed42-105">Version Information</span></span>

<span data-ttu-id="8ed42-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="8ed42-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8ed42-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ed42-107">Syntax</span></span>

<span data-ttu-id="8ed42-108">BOUNDINGBOXDIST (\* \* *index* \* \*)</span><span class="sxs-lookup"><span data-stu-id="8ed42-108">BOUNDINGBOXDIST(\*\* *Index* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8ed42-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ed42-109">Parameters</span></span>

|<span data-ttu-id="8ed42-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="8ed42-110">**Name**</span></span>|<span data-ttu-id="8ed42-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="8ed42-111">**Required/Optional**</span></span>|<span data-ttu-id="8ed42-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="8ed42-112">**Data Type**</span></span>|<span data-ttu-id="8ed42-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8ed42-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8ed42-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="8ed42-114">_Index_</span></span> <br/> |<span data-ttu-id="8ed42-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8ed42-115">Required</span></span>  <br/> |<span data-ttu-id="8ed42-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="8ed42-116">**Number**</span></span> <br/> |<span data-ttu-id="8ed42-117">Часть ограничительной рамки фигуры для измерения и возврата.</span><span class="sxs-lookup"><span data-stu-id="8ed42-117">The part of the shape's bounding box to measure and return.</span></span> <span data-ttu-id="8ed42-118">Возможные значения приведены в разделе reMarks.</span><span class="sxs-lookup"><span data-stu-id="8ed42-118">See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8ed42-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ed42-119">Return value</span></span>

 <span data-ttu-id="8ed42-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="8ed42-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8ed42-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="8ed42-121">Remarks</span></span>

 <span data-ttu-id="8ed42-122">*Индекс* может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="8ed42-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="8ed42-123">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="8ed42-123">**Item**</span></span>|<span data-ttu-id="8ed42-124">**Значение**</span><span class="sxs-lookup"><span data-stu-id="8ed42-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8ed42-125">Width</span><span class="sxs-lookup"><span data-stu-id="8ed42-125">Width</span></span>  <br/> |<span data-ttu-id="8ed42-126">нуль</span><span class="sxs-lookup"><span data-stu-id="8ed42-126">0</span></span>  <br/> |
|<span data-ttu-id="8ed42-127">Height</span><span class="sxs-lookup"><span data-stu-id="8ed42-127">Height</span></span>  <br/> |<span data-ttu-id="8ed42-128">1,1</span><span class="sxs-lookup"><span data-stu-id="8ed42-128">1</span></span>  <br/> |
|<span data-ttu-id="8ed42-129">Закрепление левого края до фигуры</span><span class="sxs-lookup"><span data-stu-id="8ed42-129">Left edge to shape pin</span></span>  <br/> |<span data-ttu-id="8ed42-130">2</span><span class="sxs-lookup"><span data-stu-id="8ed42-130">2</span></span>  <br/> |
|<span data-ttu-id="8ed42-131">Прикрепление фигуры к правому краю</span><span class="sxs-lookup"><span data-stu-id="8ed42-131">Shape pin to right edge</span></span>  <br/> |<span data-ttu-id="8ed42-132">4</span><span class="sxs-lookup"><span data-stu-id="8ed42-132">3</span></span>  <br/> |
|<span data-ttu-id="8ed42-133">Прикрепление фигуры к верхнему краю</span><span class="sxs-lookup"><span data-stu-id="8ed42-133">Shape pin to top edge</span></span>  <br/> |<span data-ttu-id="8ed42-134">SP4</span><span class="sxs-lookup"><span data-stu-id="8ed42-134">4</span></span>  <br/> |
|<span data-ttu-id="8ed42-135">По нижнему краю до фигуры контакта</span><span class="sxs-lookup"><span data-stu-id="8ed42-135">Bottom edge to shape pin</span></span>  <br/> |<span data-ttu-id="8ed42-136">17:00</span><span class="sxs-lookup"><span data-stu-id="8ed42-136">5</span></span>  <br/> |
|<span data-ttu-id="8ed42-137">Центр ограничительной рамки для PinX</span><span class="sxs-lookup"><span data-stu-id="8ed42-137">Center of bounding box to PinX</span></span>  <br/> |<span data-ttu-id="8ed42-138">ICMPv6</span><span class="sxs-lookup"><span data-stu-id="8ed42-138">6</span></span>  <br/> |
|<span data-ttu-id="8ed42-139">Центр ограничительной рамки для PinY</span><span class="sxs-lookup"><span data-stu-id="8ed42-139">Center of bounding box to PinY</span></span>  <br/> |<span data-ttu-id="8ed42-140">см</span><span class="sxs-lookup"><span data-stu-id="8ed42-140">7</span></span>  <br/> |
   

