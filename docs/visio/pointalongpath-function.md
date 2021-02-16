---
title: Функция POINTALONGPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f91e5d9-89b8-5a0d-e01f-aa81fbd5e1fd
description: Возвращает координаты точки пути или смещения от нее.
ms.openlocfilehash: ce8b54bbd821cbfa6eb1f2789193ff8d7dda42d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430485"
---
# <a name="pointalongpath-function"></a><span data-ttu-id="c141b-103">Функция POINTALONGPATH</span><span class="sxs-lookup"><span data-stu-id="c141b-103">POINTALONGPATH Function</span></span>

<span data-ttu-id="c141b-104">Возвращает координаты точки пути или смещения от нее.</span><span class="sxs-lookup"><span data-stu-id="c141b-104">Returns the coordinates of a point on, or offset from, the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="c141b-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="c141b-105">Version Information</span></span>

<span data-ttu-id="c141b-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="c141b-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c141b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c141b-107">Syntax</span></span>

<span data-ttu-id="c141b-108">POINTALONGPATH(\*\* *section* \**, \*\* *travel* \*\* *[,offset]* \*\* \*\*\* [,segment]* \*\* )</span><span class="sxs-lookup"><span data-stu-id="c141b-108">POINTALONGPATH(\*\* *section* \*\*, \*\* *travel* \*\* \*\* *[,offset]* \*\* \*\* *[,segment]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c141b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c141b-109">Parameters</span></span>

|<span data-ttu-id="c141b-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="c141b-110">**Name**</span></span>|<span data-ttu-id="c141b-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="c141b-111">**Required/Optional**</span></span>|<span data-ttu-id="c141b-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="c141b-112">**Data Type**</span></span>|<span data-ttu-id="c141b-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c141b-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c141b-114">_section_</span><span class="sxs-lookup"><span data-stu-id="c141b-114">_section_</span></span> <br/> |<span data-ttu-id="c141b-115">Обязательно</span><span class="sxs-lookup"><span data-stu-id="c141b-115">Required</span></span>  <br/> |<span data-ttu-id="c141b-116">**Строка**</span><span class="sxs-lookup"><span data-stu-id="c141b-116">**String**</span></span> <br/> |<span data-ttu-id="c141b-117">Раздел "Геометрия", который представляет путь, заданный ссылкой на его ячейку Path (например, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="c141b-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="c141b-118">_travel_</span><span class="sxs-lookup"><span data-stu-id="c141b-118">_travel_</span></span> <br/> |<span data-ttu-id="c141b-119">Обязательна</span><span class="sxs-lookup"><span data-stu-id="c141b-119">Required</span></span>  <br/> |<span data-ttu-id="c141b-120">64-разрядное число с плавающей запятой двойной точности.</span><span class="sxs-lookup"><span data-stu-id="c141b-120">**Double**</span></span> <br/> |<span data-ttu-id="c141b-121">Процент прохода пути от точки начала до конечной точки, определяемой точкой.</span><span class="sxs-lookup"><span data-stu-id="c141b-121">The percentage of the path traversed, from the begin point to the end point that identifies the point.</span></span> <span data-ttu-id="c141b-122">Должно быть от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="c141b-122">Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="c141b-123">_offset_</span><span class="sxs-lookup"><span data-stu-id="c141b-123">_offset_</span></span> <br/> |<span data-ttu-id="c141b-124">Необязательна</span><span class="sxs-lookup"><span data-stu-id="c141b-124">Optional</span></span>  <br/> |<span data-ttu-id="c141b-125">64-разрядное число с плавающей запятой двойной точности.</span><span class="sxs-lookup"><span data-stu-id="c141b-125">**Double**</span></span> <br/> |<span data-ttu-id="c141b-126">Расстояние, на которое точка смещена от пути.</span><span class="sxs-lookup"><span data-stu-id="c141b-126">The distance that the point is offset from the path.</span></span> <span data-ttu-id="c141b-127">Дополнительные сведения см. в примечаиях.</span><span class="sxs-lookup"><span data-stu-id="c141b-127">See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="c141b-128">_segment_</span><span class="sxs-lookup"><span data-stu-id="c141b-128">_segment_</span></span> <br/> |<span data-ttu-id="c141b-129">Необязательна</span><span class="sxs-lookup"><span data-stu-id="c141b-129">Optional</span></span>  <br/> |<span data-ttu-id="c141b-130">64-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="c141b-130">**Integer**</span></span> <br/> |<span data-ttu-id="c141b-131">Сегмент пути на основе 1, в котором вычисляются координаты.</span><span class="sxs-lookup"><span data-stu-id="c141b-131">The 1-based segment of the path in which to calculate the coordinates.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c141b-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c141b-132">Return value</span></span>

 <span data-ttu-id="c141b-133">**Point**</span><span class="sxs-lookup"><span data-stu-id="c141b-133">**Point**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c141b-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="c141b-134">Remarks</span></span>

<span data-ttu-id="c141b-135">Если  _раздел_ или  _сегмент_ не существует, Microsoft Visio возвращает #REF!.</span><span class="sxs-lookup"><span data-stu-id="c141b-135">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="c141b-136">Положительные  *значения*  смещения указывают точки слева от направления перемещения.</span><span class="sxs-lookup"><span data-stu-id="c141b-136">Positive  *offset*  values specify points to the left of the direction of travel.</span></span> 
  
<span data-ttu-id="c141b-137">*Отрицательные* значения смещения указывают справа от направления перемещения.</span><span class="sxs-lookup"><span data-stu-id="c141b-137">Negative  *offset*  values specify points to the right of the direction of travel.</span></span> 
  
<span data-ttu-id="c141b-138">Точка **представляет** упорядоченную пару геометрических координат *(x,y)* в виде одного значения.</span><span class="sxs-lookup"><span data-stu-id="c141b-138">A **Point** represents an ordered pair of geometric coordinates (*x,y*) as a single value.</span></span> 
  

