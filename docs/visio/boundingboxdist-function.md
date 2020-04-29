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
# <a name="boundingboxdist-function"></a><span data-ttu-id="fdb0e-103">Функция BOUNDINGBOXDIST</span><span class="sxs-lookup"><span data-stu-id="fdb0e-103">BOUNDINGBOXDIST Function</span></span>

<span data-ttu-id="fdb0e-104">Возвращает единицу измерения указанной части ограничительной рамки фигуры.</span><span class="sxs-lookup"><span data-stu-id="fdb0e-104">Returns the measurement of the specified part of the shape's bounding box.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="fdb0e-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="fdb0e-105">Version Information</span></span>

<span data-ttu-id="fdb0e-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="fdb0e-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fdb0e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fdb0e-107">Syntax</span></span>

<span data-ttu-id="fdb0e-108">BOUNDINGBOXDIST (\* \* *index* \* \*)</span><span class="sxs-lookup"><span data-stu-id="fdb0e-108">BOUNDINGBOXDIST(\*\* *Index* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fdb0e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fdb0e-109">Parameters</span></span>

|<span data-ttu-id="fdb0e-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="fdb0e-110">**Name**</span></span>|<span data-ttu-id="fdb0e-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="fdb0e-111">**Required/Optional**</span></span>|<span data-ttu-id="fdb0e-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="fdb0e-112">**Data Type**</span></span>|<span data-ttu-id="fdb0e-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fdb0e-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fdb0e-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="fdb0e-114">_Index_</span></span> <br/> |<span data-ttu-id="fdb0e-115">Обязательна</span><span class="sxs-lookup"><span data-stu-id="fdb0e-115">Required</span></span>  <br/> |<span data-ttu-id="fdb0e-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="fdb0e-116">**Number**</span></span> <br/> |<span data-ttu-id="fdb0e-117">Часть ограничительной рамки фигуры для измерения и возврата.</span><span class="sxs-lookup"><span data-stu-id="fdb0e-117">The part of the shape's bounding box to measure and return.</span></span> <span data-ttu-id="fdb0e-118">Возможные значения приведены в разделе remarks.</span><span class="sxs-lookup"><span data-stu-id="fdb0e-118">See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="fdb0e-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fdb0e-119">Return value</span></span>

 <span data-ttu-id="fdb0e-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="fdb0e-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fdb0e-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="fdb0e-121">Remarks</span></span>

 <span data-ttu-id="fdb0e-122">*Индекс* может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="fdb0e-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="fdb0e-123">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="fdb0e-123">**Item**</span></span>|<span data-ttu-id="fdb0e-124">**Значение**</span><span class="sxs-lookup"><span data-stu-id="fdb0e-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fdb0e-125">Width</span><span class="sxs-lookup"><span data-stu-id="fdb0e-125">Width</span></span>  <br/> |<span data-ttu-id="fdb0e-126">нуль</span><span class="sxs-lookup"><span data-stu-id="fdb0e-126">0</span></span>  <br/> |
|<span data-ttu-id="fdb0e-127">Height</span><span class="sxs-lookup"><span data-stu-id="fdb0e-127">Height</span></span>  <br/> |<span data-ttu-id="fdb0e-128">1,1</span><span class="sxs-lookup"><span data-stu-id="fdb0e-128">1</span></span>  <br/> |
|<span data-ttu-id="fdb0e-129">Закрепление левого края до фигуры</span><span class="sxs-lookup"><span data-stu-id="fdb0e-129">Left edge to shape pin</span></span>  <br/> |<span data-ttu-id="fdb0e-130">2</span><span class="sxs-lookup"><span data-stu-id="fdb0e-130">2</span></span>  <br/> |
|<span data-ttu-id="fdb0e-131">Прикрепление фигуры к правому краю</span><span class="sxs-lookup"><span data-stu-id="fdb0e-131">Shape pin to right edge</span></span>  <br/> |<span data-ttu-id="fdb0e-132">4</span><span class="sxs-lookup"><span data-stu-id="fdb0e-132">3</span></span>  <br/> |
|<span data-ttu-id="fdb0e-133">Прикрепление фигуры к верхнему краю</span><span class="sxs-lookup"><span data-stu-id="fdb0e-133">Shape pin to top edge</span></span>  <br/> |<span data-ttu-id="fdb0e-134">4 </span><span class="sxs-lookup"><span data-stu-id="fdb0e-134">4</span></span>  <br/> |
|<span data-ttu-id="fdb0e-135">По нижнему краю до фигуры контакта</span><span class="sxs-lookup"><span data-stu-id="fdb0e-135">Bottom edge to shape pin</span></span>  <br/> |<span data-ttu-id="fdb0e-136">5 </span><span class="sxs-lookup"><span data-stu-id="fdb0e-136">5</span></span>  <br/> |
|<span data-ttu-id="fdb0e-137">Центр ограничительной рамки для PinX</span><span class="sxs-lookup"><span data-stu-id="fdb0e-137">Center of bounding box to PinX</span></span>  <br/> |<span data-ttu-id="fdb0e-138">6 </span><span class="sxs-lookup"><span data-stu-id="fdb0e-138">6</span></span>  <br/> |
|<span data-ttu-id="fdb0e-139">Центр ограничительной рамки для PinY</span><span class="sxs-lookup"><span data-stu-id="fdb0e-139">Center of bounding box to PinY</span></span>  <br/> |<span data-ttu-id="fdb0e-140">7 </span><span class="sxs-lookup"><span data-stu-id="fdb0e-140">7</span></span>  <br/> |
   

