---
title: Функция BOUNDINGBOXRECT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: Возвращает координату указанного края ограничительной рамки фигуры.
ms.openlocfilehash: 0018118eb0991fe9dc1da0eb000566b69d8a4b4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338054"
---
# <a name="boundingboxrect-function"></a><span data-ttu-id="1ff42-103">Функция BOUNDINGBOXRECT</span><span class="sxs-lookup"><span data-stu-id="1ff42-103">BOUNDINGBOXRECT Function</span></span>

<span data-ttu-id="1ff42-104">Возвращает координату указанного края ограничительной рамки фигуры.</span><span class="sxs-lookup"><span data-stu-id="1ff42-104">Returns the coordinate of the specified edge of the shape's bounding box.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="1ff42-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="1ff42-105">Version Information</span></span>

<span data-ttu-id="1ff42-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="1ff42-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1ff42-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ff42-107">Syntax</span></span>

<span data-ttu-id="1ff42-108">BOUNDINGBOXRECT (\* \* *index* \* \*)</span><span class="sxs-lookup"><span data-stu-id="1ff42-108">BOUNDINGBOXRECT(\*\* *Index* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1ff42-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ff42-109">Parameters</span></span>

|<span data-ttu-id="1ff42-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="1ff42-110">**Name**</span></span>|<span data-ttu-id="1ff42-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="1ff42-111">**Required/Optional**</span></span>|<span data-ttu-id="1ff42-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="1ff42-112">**Data Type**</span></span>|<span data-ttu-id="1ff42-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1ff42-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1ff42-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="1ff42-114">_Index_</span></span> <br/> |<span data-ttu-id="1ff42-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="1ff42-115">Required</span></span>  <br/> |<span data-ttu-id="1ff42-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="1ff42-116">**Integer**</span></span> <br/> |<span data-ttu-id="1ff42-117">Край ограничительной рамки фигуры, для которой необходимо получить координаты.</span><span class="sxs-lookup"><span data-stu-id="1ff42-117">The edge of the shape's bounding box for which to get the coordinate.</span></span> <span data-ttu-id="1ff42-118">Возможные значения приведены в разделе reMarks.</span><span class="sxs-lookup"><span data-stu-id="1ff42-118">See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="1ff42-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ff42-119">Return value</span></span>

 <span data-ttu-id="1ff42-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="1ff42-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1ff42-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ff42-121">Remarks</span></span>

 <span data-ttu-id="1ff42-122">*Индекс* может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="1ff42-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="1ff42-123">**Item**</span><span class="sxs-lookup"><span data-stu-id="1ff42-123">**Item**</span></span>|<span data-ttu-id="1ff42-124">**Значение**</span><span class="sxs-lookup"><span data-stu-id="1ff42-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1ff42-125">Левый край</span><span class="sxs-lookup"><span data-stu-id="1ff42-125">Left edge</span></span>  <br/> |<span data-ttu-id="1ff42-126">нуль</span><span class="sxs-lookup"><span data-stu-id="1ff42-126">0</span></span>  <br/> |
|<span data-ttu-id="1ff42-127">Правый край</span><span class="sxs-lookup"><span data-stu-id="1ff42-127">Right edge</span></span>  <br/> |<span data-ttu-id="1ff42-128">1,1</span><span class="sxs-lookup"><span data-stu-id="1ff42-128">1</span></span>  <br/> |
|<span data-ttu-id="1ff42-129">Верхняя граница</span><span class="sxs-lookup"><span data-stu-id="1ff42-129">Top edge</span></span>  <br/> |<span data-ttu-id="1ff42-130">2</span><span class="sxs-lookup"><span data-stu-id="1ff42-130">2</span></span>  <br/> |
|<span data-ttu-id="1ff42-131">Нижняя граница</span><span class="sxs-lookup"><span data-stu-id="1ff42-131">Bottom edge</span></span>  <br/> |<span data-ttu-id="1ff42-132">4</span><span class="sxs-lookup"><span data-stu-id="1ff42-132">3</span></span>  <br/> |
   
<span data-ttu-id="1ff42-133">Если у фигуры есть родительский объект, возвращаемое значение находится в системе координат родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="1ff42-133">If the shape has a parent, the return value is in the coordinate system of that parent.</span></span>
  

