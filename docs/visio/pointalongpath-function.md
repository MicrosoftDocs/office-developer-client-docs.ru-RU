---
title: Функция POINTALONGPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f91e5d9-89b8-5a0d-e01f-aa81fbd5e1fd
description: Возвращает координаты точки на или смещение из пути.
ms.openlocfilehash: 9ce6f8c171515b46aaff0ce07cbe7da4f1e958d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814398"
---
# <a name="pointalongpath-function"></a><span data-ttu-id="d1df2-103">Функция POINTALONGPATH</span><span class="sxs-lookup"><span data-stu-id="d1df2-103">POINTALONGPATH Function</span></span>

<span data-ttu-id="d1df2-104">Возвращает координаты точки на или смещение из пути.</span><span class="sxs-lookup"><span data-stu-id="d1df2-104">Returns the coordinates of a point on, or offset from, the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="d1df2-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="d1df2-105">Version Information</span></span>

<span data-ttu-id="d1df2-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="d1df2-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d1df2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1df2-107">Syntax</span></span>

<span data-ttu-id="d1df2-108">POINTALONGPATH (** *раздел* **, ** *путешествий* ** ** *[, смещение]* ** ** *[, сегмент]* **)</span><span class="sxs-lookup"><span data-stu-id="d1df2-108">POINTALONGPATH(** *section* **, ** *travel* ** ** *[,offset]* ** ** *[,segment]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d1df2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d1df2-109">Parameters</span></span>

|<span data-ttu-id="d1df2-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="d1df2-110">**Name**</span></span>|<span data-ttu-id="d1df2-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="d1df2-111">**Required/Optional**</span></span>|<span data-ttu-id="d1df2-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="d1df2-112">**Data Type**</span></span>|<span data-ttu-id="d1df2-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d1df2-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d1df2-114">_section_</span><span class="sxs-lookup"><span data-stu-id="d1df2-114">_section_</span></span> <br/> |<span data-ttu-id="d1df2-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d1df2-115">Required</span></span>  <br/> |<span data-ttu-id="d1df2-116">**Строка**</span><span class="sxs-lookup"><span data-stu-id="d1df2-116">**String**</span></span> <br/> |<span data-ttu-id="d1df2-117">Раздел геометрии, представляющий путь, указанный с помощью ссылки на его ячейку Path (например, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="d1df2-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="d1df2-118">_поездки_</span><span class="sxs-lookup"><span data-stu-id="d1df2-118">_travel_</span></span> <br/> |<span data-ttu-id="d1df2-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d1df2-119">Required</span></span>  <br/> |<span data-ttu-id="d1df2-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="d1df2-120">**Double**</span></span> <br/> |<span data-ttu-id="d1df2-121">Процент путь, начиная с начальной точки в конечную точку, которая определяет точку.</span><span class="sxs-lookup"><span data-stu-id="d1df2-121">The percentage of the path traversed, from the begin point to the end point that identifies the point.</span></span> <span data-ttu-id="d1df2-122">Должен быть в диапазоне от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="d1df2-122">Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="d1df2-123">_Смещение_</span><span class="sxs-lookup"><span data-stu-id="d1df2-123">_offset_</span></span> <br/> |<span data-ttu-id="d1df2-124">Optional</span><span class="sxs-lookup"><span data-stu-id="d1df2-124">Optional</span></span>  <br/> |<span data-ttu-id="d1df2-125">**Double**</span><span class="sxs-lookup"><span data-stu-id="d1df2-125">**Double**</span></span> <br/> |<span data-ttu-id="d1df2-126">Расстояние смещения, что точка из пути.</span><span class="sxs-lookup"><span data-stu-id="d1df2-126">The distance that the point is offset from the path.</span></span> <span data-ttu-id="d1df2-127">Для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="d1df2-127">See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="d1df2-128">_сегмента_</span><span class="sxs-lookup"><span data-stu-id="d1df2-128">_segment_</span></span> <br/> |<span data-ttu-id="d1df2-129">Optional</span><span class="sxs-lookup"><span data-stu-id="d1df2-129">Optional</span></span>  <br/> |<span data-ttu-id="d1df2-130">**Integer**</span><span class="sxs-lookup"><span data-stu-id="d1df2-130">**Integer**</span></span> <br/> |<span data-ttu-id="d1df2-131">Сегмент путь для вычисления координат, основанный на 1.</span><span class="sxs-lookup"><span data-stu-id="d1df2-131">The 1-based segment of the path in which to calculate the coordinates.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d1df2-132">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="d1df2-132">Return value</span></span>

 <span data-ttu-id="d1df2-133">**Точка**</span><span class="sxs-lookup"><span data-stu-id="d1df2-133">**Point**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d1df2-134">Замечания</span><span class="sxs-lookup"><span data-stu-id="d1df2-134">Remarks</span></span>

<span data-ttu-id="d1df2-135">Если _раздел_ или _Сегмент_ не существует, Microsoft Visio возвращает #REF!.</span><span class="sxs-lookup"><span data-stu-id="d1df2-135">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="d1df2-136">Положительное *смещение* определяют точки слева от направление командировок.</span><span class="sxs-lookup"><span data-stu-id="d1df2-136">Positive  *offset*  values specify points to the left of the direction of travel.</span></span> 
  
<span data-ttu-id="d1df2-137">Отрицательное *смещение* определяют точек справа от направление командировок.</span><span class="sxs-lookup"><span data-stu-id="d1df2-137">Negative  *offset*  values specify points to the right of the direction of travel.</span></span> 
  
<span data-ttu-id="d1df2-138">**Точка** представляет упорядоченную пару геометрические координат (*x, y*) как одно значение.</span><span class="sxs-lookup"><span data-stu-id="d1df2-138">A **Point** represents an ordered pair of geometric coordinates (*x,y*) as a single value.</span></span> 
  

