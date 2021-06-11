---
title: Функция BOUNDINGBOXRECT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: Возвращает координату указанного края окне границы фигуры.
ms.openlocfilehash: 0018118eb0991fe9dc1da0eb000566b69d8a4b4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418073"
---
# <a name="boundingboxrect-function"></a><span data-ttu-id="83e77-103">Функция BOUNDINGBOXRECT</span><span class="sxs-lookup"><span data-stu-id="83e77-103">BOUNDINGBOXRECT Function</span></span>

<span data-ttu-id="83e77-104">Возвращает координату указанного края окне границы фигуры.</span><span class="sxs-lookup"><span data-stu-id="83e77-104">Returns the coordinate of the specified edge of the shape's bounding box.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="83e77-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="83e77-105">Version Information</span></span>

<span data-ttu-id="83e77-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="83e77-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="83e77-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83e77-107">Syntax</span></span>

<span data-ttu-id="83e77-108">BOUNDINGBOXRECT(\*\* *Index* \*\* )</span><span class="sxs-lookup"><span data-stu-id="83e77-108">BOUNDINGBOXRECT(\*\* *Index* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="83e77-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="83e77-109">Parameters</span></span>

|<span data-ttu-id="83e77-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="83e77-110">**Name**</span></span>|<span data-ttu-id="83e77-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="83e77-111">**Required/Optional**</span></span>|<span data-ttu-id="83e77-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="83e77-112">**Data Type**</span></span>|<span data-ttu-id="83e77-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="83e77-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="83e77-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="83e77-114">_Index_</span></span> <br/> |<span data-ttu-id="83e77-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="83e77-115">Required</span></span>  <br/> |<span data-ttu-id="83e77-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="83e77-116">**Integer**</span></span> <br/> |<span data-ttu-id="83e77-117">Край окне границы фигуры, для которого нужно получить координаты.</span><span class="sxs-lookup"><span data-stu-id="83e77-117">The edge of the shape's bounding box for which to get the coordinate.</span></span> <span data-ttu-id="83e77-118">См. примечание для возможных значений.</span><span class="sxs-lookup"><span data-stu-id="83e77-118">See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="83e77-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83e77-119">Return value</span></span>

 <span data-ttu-id="83e77-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="83e77-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="83e77-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="83e77-121">Remarks</span></span>

 <span data-ttu-id="83e77-122">*Индекс*  может быть одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="83e77-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="83e77-123">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="83e77-123">**Item**</span></span>|<span data-ttu-id="83e77-124">**Значение**</span><span class="sxs-lookup"><span data-stu-id="83e77-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="83e77-125">Левый край</span><span class="sxs-lookup"><span data-stu-id="83e77-125">Left edge</span></span>  <br/> |<span data-ttu-id="83e77-126">0</span><span class="sxs-lookup"><span data-stu-id="83e77-126">0</span></span>  <br/> |
|<span data-ttu-id="83e77-127">Правый край</span><span class="sxs-lookup"><span data-stu-id="83e77-127">Right edge</span></span>  <br/> |<span data-ttu-id="83e77-128">1</span><span class="sxs-lookup"><span data-stu-id="83e77-128">1</span></span>  <br/> |
|<span data-ttu-id="83e77-129">Верхний край</span><span class="sxs-lookup"><span data-stu-id="83e77-129">Top edge</span></span>  <br/> |<span data-ttu-id="83e77-130">2</span><span class="sxs-lookup"><span data-stu-id="83e77-130">2</span></span>  <br/> |
|<span data-ttu-id="83e77-131">Нижний край</span><span class="sxs-lookup"><span data-stu-id="83e77-131">Bottom edge</span></span>  <br/> |<span data-ttu-id="83e77-132">3</span><span class="sxs-lookup"><span data-stu-id="83e77-132">3</span></span>  <br/> |
   
<span data-ttu-id="83e77-133">Если фигура имеет родительский, возвращаемая величина находится в системе координат этого родителя.</span><span class="sxs-lookup"><span data-stu-id="83e77-133">If the shape has a parent, the return value is in the coordinate system of that parent.</span></span>
  

