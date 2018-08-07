---
title: Функция BOUNDINGBOXRECT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: Возвращает координаты указанного краю фигуры, ограничивающего поля.
ms.openlocfilehash: 2c850cb213ec0093ead53cd860f92e38da46f27e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813305"
---
# <a name="boundingboxrect-function"></a><span data-ttu-id="c6cb0-103">Функция BOUNDINGBOXRECT</span><span class="sxs-lookup"><span data-stu-id="c6cb0-103">BOUNDINGBOXRECT Function</span></span>

<span data-ttu-id="c6cb0-104">Возвращает координаты указанного краю фигуры, ограничивающего поля.</span><span class="sxs-lookup"><span data-stu-id="c6cb0-104">Returns the coordinate of the specified edge of the shape's bounding box.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="c6cb0-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="c6cb0-105">Version Information</span></span>

<span data-ttu-id="c6cb0-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="c6cb0-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c6cb0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6cb0-107">Syntax</span></span>

<span data-ttu-id="c6cb0-108">BOUNDINGBOXRECT (** *индекса* **)</span><span class="sxs-lookup"><span data-stu-id="c6cb0-108">BOUNDINGBOXRECT(** *Index* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c6cb0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6cb0-109">Parameters</span></span>

|<span data-ttu-id="c6cb0-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="c6cb0-110">**Name**</span></span>|<span data-ttu-id="c6cb0-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="c6cb0-111">**Required/Optional**</span></span>|<span data-ttu-id="c6cb0-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="c6cb0-112">**Data Type**</span></span>|<span data-ttu-id="c6cb0-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c6cb0-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c6cb0-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="c6cb0-114">_Index_</span></span> <br/> |<span data-ttu-id="c6cb0-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c6cb0-115">Required</span></span>  <br/> |<span data-ttu-id="c6cb0-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="c6cb0-116">**Integer**</span></span> <br/> |<span data-ttu-id="c6cb0-117">Край фигуры прямоугольника для которого необходимо получить координаты.</span><span class="sxs-lookup"><span data-stu-id="c6cb0-117">The edge of the shape's bounding box for which to get the coordinate.</span></span> <span data-ttu-id="c6cb0-118">Возможные значения см.</span><span class="sxs-lookup"><span data-stu-id="c6cb0-118">See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c6cb0-119">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="c6cb0-119">Return value</span></span>

 <span data-ttu-id="c6cb0-120">**Число**</span><span class="sxs-lookup"><span data-stu-id="c6cb0-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c6cb0-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="c6cb0-121">Remarks</span></span>

 <span data-ttu-id="c6cb0-122">*Индекс* может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c6cb0-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="c6cb0-123">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c6cb0-123">**Item**</span></span>|<span data-ttu-id="c6cb0-124">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c6cb0-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c6cb0-125">Левые края</span><span class="sxs-lookup"><span data-stu-id="c6cb0-125">Left edge</span></span>  <br/> |<span data-ttu-id="c6cb0-126">0</span><span class="sxs-lookup"><span data-stu-id="c6cb0-126">0</span></span>  <br/> |
|<span data-ttu-id="c6cb0-127">Правые края</span><span class="sxs-lookup"><span data-stu-id="c6cb0-127">Right edge</span></span>  <br/> |<span data-ttu-id="c6cb0-128">1</span><span class="sxs-lookup"><span data-stu-id="c6cb0-128">1</span></span>  <br/> |
|<span data-ttu-id="c6cb0-129">Верхняя граница</span><span class="sxs-lookup"><span data-stu-id="c6cb0-129">Top edge</span></span>  <br/> |<span data-ttu-id="c6cb0-130">2</span><span class="sxs-lookup"><span data-stu-id="c6cb0-130">2</span></span>  <br/> |
|<span data-ttu-id="c6cb0-131">Нижний край</span><span class="sxs-lookup"><span data-stu-id="c6cb0-131">Bottom edge</span></span>  <br/> |<span data-ttu-id="c6cb0-132">3</span><span class="sxs-lookup"><span data-stu-id="c6cb0-132">3</span></span>  <br/> |
   
<span data-ttu-id="c6cb0-133">Если фигура имеет родительский объект, возвращается в системе координат родительской.</span><span class="sxs-lookup"><span data-stu-id="c6cb0-133">If the shape has a parent, the return value is in the coordinate system of that parent.</span></span>
  

