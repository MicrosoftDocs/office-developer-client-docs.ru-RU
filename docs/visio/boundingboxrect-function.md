---
title: Функция BOUNDINGBOXRECT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: Возвращает координату указанного края границ границ фигуры.
ms.openlocfilehash: 0018118eb0991fe9dc1da0eb000566b69d8a4b4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418073"
---
# <a name="boundingboxrect-function"></a><span data-ttu-id="aa46a-103">Функция BOUNDINGBOXRECT</span><span class="sxs-lookup"><span data-stu-id="aa46a-103">BOUNDINGBOXRECT Function</span></span>

<span data-ttu-id="aa46a-104">Возвращает координату указанного края границ границ фигуры.</span><span class="sxs-lookup"><span data-stu-id="aa46a-104">Returns the coordinate of the specified edge of the shape's bounding box.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="aa46a-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="aa46a-105">Version Information</span></span>

<span data-ttu-id="aa46a-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="aa46a-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="aa46a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aa46a-107">Syntax</span></span>

<span data-ttu-id="aa46a-108">BOUNDINGBOXRECT(\*\* *Index* \*\* )</span><span class="sxs-lookup"><span data-stu-id="aa46a-108">BOUNDINGBOXRECT(\*\* *Index* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="aa46a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="aa46a-109">Parameters</span></span>

|<span data-ttu-id="aa46a-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="aa46a-110">**Name**</span></span>|<span data-ttu-id="aa46a-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="aa46a-111">**Required/Optional**</span></span>|<span data-ttu-id="aa46a-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="aa46a-112">**Data Type**</span></span>|<span data-ttu-id="aa46a-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="aa46a-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="aa46a-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="aa46a-114">_Index_</span></span> <br/> |<span data-ttu-id="aa46a-115">Обязательна</span><span class="sxs-lookup"><span data-stu-id="aa46a-115">Required</span></span>  <br/> |<span data-ttu-id="aa46a-116">64-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="aa46a-116">**Integer**</span></span> <br/> |<span data-ttu-id="aa46a-117">Край границ границ фигуры, для которого необходимо получить координату.</span><span class="sxs-lookup"><span data-stu-id="aa46a-117">The edge of the shape's bounding box for which to get the coordinate.</span></span> <span data-ttu-id="aa46a-118">Возможные значения см. в примечаиях.</span><span class="sxs-lookup"><span data-stu-id="aa46a-118">See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="aa46a-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aa46a-119">Return value</span></span>

 <span data-ttu-id="aa46a-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="aa46a-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aa46a-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="aa46a-121">Remarks</span></span>

 <span data-ttu-id="aa46a-122">*Индекс*  может быть одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="aa46a-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="aa46a-123">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="aa46a-123">**Item**</span></span>|<span data-ttu-id="aa46a-124">**Значение**</span><span class="sxs-lookup"><span data-stu-id="aa46a-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="aa46a-125">Левый край</span><span class="sxs-lookup"><span data-stu-id="aa46a-125">Left edge</span></span>  <br/> |<span data-ttu-id="aa46a-126">0</span><span class="sxs-lookup"><span data-stu-id="aa46a-126">0</span></span>  <br/> |
|<span data-ttu-id="aa46a-127">Правый край</span><span class="sxs-lookup"><span data-stu-id="aa46a-127">Right edge</span></span>  <br/> |<span data-ttu-id="aa46a-128">1 </span><span class="sxs-lookup"><span data-stu-id="aa46a-128">1</span></span>  <br/> |
|<span data-ttu-id="aa46a-129">Верхний край</span><span class="sxs-lookup"><span data-stu-id="aa46a-129">Top edge</span></span>  <br/> |<span data-ttu-id="aa46a-130">2 </span><span class="sxs-lookup"><span data-stu-id="aa46a-130">2</span></span>  <br/> |
|<span data-ttu-id="aa46a-131">Нижний край</span><span class="sxs-lookup"><span data-stu-id="aa46a-131">Bottom edge</span></span>  <br/> |<span data-ttu-id="aa46a-132">3 </span><span class="sxs-lookup"><span data-stu-id="aa46a-132">3</span></span>  <br/> |
   
<span data-ttu-id="aa46a-133">Если фигура имеет родительский, возвращаемая величина находится в системе координат этого родительского.</span><span class="sxs-lookup"><span data-stu-id="aa46a-133">If the shape has a parent, the return value is in the coordinate system of that parent.</span></span>
  

