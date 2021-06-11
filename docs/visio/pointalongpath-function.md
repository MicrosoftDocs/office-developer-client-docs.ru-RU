---
title: Функция POINTALONGPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f91e5d9-89b8-5a0d-e01f-aa81fbd5e1fd
description: Возвращает координаты точки на пути или смещения с нее.
ms.openlocfilehash: ce8b54bbd821cbfa6eb1f2789193ff8d7dda42d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430485"
---
# <a name="pointalongpath-function"></a><span data-ttu-id="90cbd-103">Функция POINTALONGPATH</span><span class="sxs-lookup"><span data-stu-id="90cbd-103">POINTALONGPATH Function</span></span>

<span data-ttu-id="90cbd-104">Возвращает координаты точки на пути или смещения с нее.</span><span class="sxs-lookup"><span data-stu-id="90cbd-104">Returns the coordinates of a point on, or offset from, the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="90cbd-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="90cbd-105">Version Information</span></span>

<span data-ttu-id="90cbd-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="90cbd-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="90cbd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="90cbd-107">Syntax</span></span>

<span data-ttu-id="90cbd-108">POINTALONGPATH(\*\* *раздел* \**, \*\*\*\* путешествия \*\* \*\*\* [,смещение]* \*\* *[,сегмент]* \*\* \* )</span><span class="sxs-lookup"><span data-stu-id="90cbd-108">POINTALONGPATH(\*\* *section* \*\*, \*\* *travel* \*\* \*\* *[,offset]* \*\* \*\* *[,segment]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="90cbd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="90cbd-109">Parameters</span></span>

|<span data-ttu-id="90cbd-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="90cbd-110">**Name**</span></span>|<span data-ttu-id="90cbd-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="90cbd-111">**Required/Optional**</span></span>|<span data-ttu-id="90cbd-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="90cbd-112">**Data Type**</span></span>|<span data-ttu-id="90cbd-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="90cbd-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="90cbd-114">_section_</span><span class="sxs-lookup"><span data-stu-id="90cbd-114">_section_</span></span> <br/> |<span data-ttu-id="90cbd-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="90cbd-115">Required</span></span>  <br/> |<span data-ttu-id="90cbd-116">**String**</span><span class="sxs-lookup"><span data-stu-id="90cbd-116">**String**</span></span> <br/> |<span data-ttu-id="90cbd-117">Раздел Геометрия, который представляет путь, заданный ссылкой на его ячейку Path (например, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="90cbd-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="90cbd-118">_путешествия_</span><span class="sxs-lookup"><span data-stu-id="90cbd-118">_travel_</span></span> <br/> |<span data-ttu-id="90cbd-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="90cbd-119">Required</span></span>  <br/> |<span data-ttu-id="90cbd-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="90cbd-120">**Double**</span></span> <br/> |<span data-ttu-id="90cbd-121">Процент пройденного пути от точки начала до конечной точки, определяемой точкой.</span><span class="sxs-lookup"><span data-stu-id="90cbd-121">The percentage of the path traversed, from the begin point to the end point that identifies the point.</span></span> <span data-ttu-id="90cbd-122">Должно быть от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="90cbd-122">Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="90cbd-123">_смещение_</span><span class="sxs-lookup"><span data-stu-id="90cbd-123">_offset_</span></span> <br/> |<span data-ttu-id="90cbd-124">Необязательный</span><span class="sxs-lookup"><span data-stu-id="90cbd-124">Optional</span></span>  <br/> |<span data-ttu-id="90cbd-125">**Double**</span><span class="sxs-lookup"><span data-stu-id="90cbd-125">**Double**</span></span> <br/> |<span data-ttu-id="90cbd-126">Расстояние, которое точка смещена с пути.</span><span class="sxs-lookup"><span data-stu-id="90cbd-126">The distance that the point is offset from the path.</span></span> <span data-ttu-id="90cbd-127">Дополнительные сведения см. в комментарии.</span><span class="sxs-lookup"><span data-stu-id="90cbd-127">See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="90cbd-128">_segment_</span><span class="sxs-lookup"><span data-stu-id="90cbd-128">_segment_</span></span> <br/> |<span data-ttu-id="90cbd-129">Необязательный</span><span class="sxs-lookup"><span data-stu-id="90cbd-129">Optional</span></span>  <br/> |<span data-ttu-id="90cbd-130">**Integer**</span><span class="sxs-lookup"><span data-stu-id="90cbd-130">**Integer**</span></span> <br/> |<span data-ttu-id="90cbd-131">1-ый сегмент пути, в котором вычисляются координаты.</span><span class="sxs-lookup"><span data-stu-id="90cbd-131">The 1-based segment of the path in which to calculate the coordinates.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="90cbd-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="90cbd-132">Return value</span></span>

 <span data-ttu-id="90cbd-133">**Point**</span><span class="sxs-lookup"><span data-stu-id="90cbd-133">**Point**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="90cbd-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="90cbd-134">Remarks</span></span>

<span data-ttu-id="90cbd-135">Если _раздел_ или _сегмент_ не существует, корпорация Майкрософт Visio возвращает #REF!.</span><span class="sxs-lookup"><span data-stu-id="90cbd-135">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="90cbd-136">Положительные  *значения*  смещения указывают точки слева от направления перемещения.</span><span class="sxs-lookup"><span data-stu-id="90cbd-136">Positive  *offset*  values specify points to the left of the direction of travel.</span></span> 
  
<span data-ttu-id="90cbd-137">*Отрицательные* значения смещения указывают точки справа от направления перемещения.</span><span class="sxs-lookup"><span data-stu-id="90cbd-137">Negative  *offset*  values specify points to the right of the direction of travel.</span></span> 
  
<span data-ttu-id="90cbd-138">Точка **представляет** упорядоченную пару геометрических координат *(x,y)* как единое значение.</span><span class="sxs-lookup"><span data-stu-id="90cbd-138">A **Point** represents an ordered pair of geometric coordinates (*x,y*) as a single value.</span></span> 
  

