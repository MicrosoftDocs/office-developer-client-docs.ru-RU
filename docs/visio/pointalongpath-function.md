---
title: Функция POINTALONGPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f91e5d9-89b8-5a0d-e01f-aa81fbd5e1fd
description: Возвращает координаты точки, а также смещение относительно пути.
ms.openlocfilehash: ce8b54bbd821cbfa6eb1f2789193ff8d7dda42d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430485"
---
# <a name="pointalongpath-function"></a><span data-ttu-id="8d605-103">Функция POINTALONGPATH</span><span class="sxs-lookup"><span data-stu-id="8d605-103">POINTALONGPATH Function</span></span>

<span data-ttu-id="8d605-104">Возвращает координаты точки, а также смещение относительно пути.</span><span class="sxs-lookup"><span data-stu-id="8d605-104">Returns the coordinates of a point on, or offset from, the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="8d605-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="8d605-105">Version Information</span></span>

<span data-ttu-id="8d605-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="8d605-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8d605-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d605-107">Syntax</span></span>

<span data-ttu-id="8d605-108">POINTALONGPATH (\* \* *раздел* \* \*, \* \* *путешествие* \* \* \* \* *[, offset]* \* \* \* \* *[, сегмент]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="8d605-108">POINTALONGPATH(\*\* *section* \*\*, \*\* *travel* \*\* \*\* *[,offset]* \*\* \*\* *[,segment]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8d605-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d605-109">Parameters</span></span>

|<span data-ttu-id="8d605-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="8d605-110">**Name**</span></span>|<span data-ttu-id="8d605-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="8d605-111">**Required/Optional**</span></span>|<span data-ttu-id="8d605-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="8d605-112">**Data Type**</span></span>|<span data-ttu-id="8d605-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8d605-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8d605-114">_section_</span><span class="sxs-lookup"><span data-stu-id="8d605-114">_section_</span></span> <br/> |<span data-ttu-id="8d605-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8d605-115">Required</span></span>  <br/> |<span data-ttu-id="8d605-116">**String**</span><span class="sxs-lookup"><span data-stu-id="8d605-116">**String**</span></span> <br/> |<span data-ttu-id="8d605-117">Раздел геометрии, представляющий путь, заданный ссылкой на ячейку пути (например, Geometry1. Path).</span><span class="sxs-lookup"><span data-stu-id="8d605-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="8d605-118">_дающих_</span><span class="sxs-lookup"><span data-stu-id="8d605-118">_travel_</span></span> <br/> |<span data-ttu-id="8d605-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8d605-119">Required</span></span>  <br/> |<span data-ttu-id="8d605-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="8d605-120">**Double**</span></span> <br/> |<span data-ttu-id="8d605-121">Процент прохождения пути от точки Begin до конечной точки, определяющей точку.</span><span class="sxs-lookup"><span data-stu-id="8d605-121">The percentage of the path traversed, from the begin point to the end point that identifies the point.</span></span> <span data-ttu-id="8d605-122">Значение должно находиться в пределах от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="8d605-122">Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="8d605-123">_корреспондирующей_</span><span class="sxs-lookup"><span data-stu-id="8d605-123">_offset_</span></span> <br/> |<span data-ttu-id="8d605-124">Необязательный</span><span class="sxs-lookup"><span data-stu-id="8d605-124">Optional</span></span>  <br/> |<span data-ttu-id="8d605-125">**Double**</span><span class="sxs-lookup"><span data-stu-id="8d605-125">**Double**</span></span> <br/> |<span data-ttu-id="8d605-126">Расстояние, на которое точка смещается относительно пути.</span><span class="sxs-lookup"><span data-stu-id="8d605-126">The distance that the point is offset from the path.</span></span> <span data-ttu-id="8d605-127">Дополнительные сведения см.</span><span class="sxs-lookup"><span data-stu-id="8d605-127">See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="8d605-128">_сегмент_</span><span class="sxs-lookup"><span data-stu-id="8d605-128">_segment_</span></span> <br/> |<span data-ttu-id="8d605-129">Необязательный</span><span class="sxs-lookup"><span data-stu-id="8d605-129">Optional</span></span>  <br/> |<span data-ttu-id="8d605-130">**Integer**</span><span class="sxs-lookup"><span data-stu-id="8d605-130">**Integer**</span></span> <br/> |<span data-ttu-id="8d605-131">Сегмент на основе 1 пути, в котором вычисляется координат.</span><span class="sxs-lookup"><span data-stu-id="8d605-131">The 1-based segment of the path in which to calculate the coordinates.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8d605-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d605-132">Return value</span></span>

 <span data-ttu-id="8d605-133">**Point**</span><span class="sxs-lookup"><span data-stu-id="8d605-133">**Point**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8d605-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="8d605-134">Remarks</span></span>

<span data-ttu-id="8d605-135">Если _раздел_ или _сегмент_ не существует, Microsoft Visio возвращает #REF!.</span><span class="sxs-lookup"><span data-stu-id="8d605-135">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="8d605-136">Положительные значения *смещения* задают точки слева от направления поездки.</span><span class="sxs-lookup"><span data-stu-id="8d605-136">Positive  *offset*  values specify points to the left of the direction of travel.</span></span> 
  
<span data-ttu-id="8d605-137">Отрицательные значения *смещения* задают точки справа от направления поездки.</span><span class="sxs-lookup"><span data-stu-id="8d605-137">Negative  *offset*  values specify points to the right of the direction of travel.</span></span> 
  
<span data-ttu-id="8d605-138">**Точка** представляет собой упорядоченную комбинацию геометрических координат (*x, y*) в виде одного значения.</span><span class="sxs-lookup"><span data-stu-id="8d605-138">A **Point** represents an ordered pair of geometric coordinates (*x,y*) as a single value.</span></span> 
  

