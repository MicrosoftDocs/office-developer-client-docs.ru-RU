---
title: Функция ANGLEALONGPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Возвращает угол касающегося на путь в данной точке.
ms.openlocfilehash: a15e45ff6135972cd1cd78382147a493f8fc8d69
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160295"
---
# <a name="anglealongpath-function"></a><span data-ttu-id="b69b0-103">Функция ANGLEALONGPATH</span><span class="sxs-lookup"><span data-stu-id="b69b0-103">ANGLEALONGPATH Function</span></span>

<span data-ttu-id="b69b0-104">Возвращает угол касающегося на путь в данной точке.</span><span class="sxs-lookup"><span data-stu-id="b69b0-104">Returns the angle of the tangent to the path at a given point.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="b69b0-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="b69b0-105">Version Information</span></span>

<span data-ttu-id="b69b0-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="b69b0-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b69b0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b69b0-107">Syntax</span></span>

<span data-ttu-id="b69b0-108">ANGLEALONGPATH ***(раздел***, ***путешествия*** ***[,сегмент]*** )</span><span class="sxs-lookup"><span data-stu-id="b69b0-108">ANGLEALONGPATH(***section***, ***travel*** ***[,segment]*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b69b0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b69b0-109">Parameters</span></span>

|<span data-ttu-id="b69b0-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="b69b0-110">**Name**</span></span>|<span data-ttu-id="b69b0-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="b69b0-111">**Required/Optional**</span></span>|<span data-ttu-id="b69b0-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="b69b0-112">**Data Type**</span></span>|<span data-ttu-id="b69b0-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b69b0-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b69b0-114">_section_</span><span class="sxs-lookup"><span data-stu-id="b69b0-114">_section_</span></span> <br/> |<span data-ttu-id="b69b0-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b69b0-115">Required</span></span>  <br/> |<span data-ttu-id="b69b0-116">**String**</span><span class="sxs-lookup"><span data-stu-id="b69b0-116">**String**</span></span> <br/> |<span data-ttu-id="b69b0-117">Раздел Геометрия, который представляет путь, заданный ссылкой на его ячейку Path (например, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="b69b0-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="b69b0-118">_путешествия_</span><span class="sxs-lookup"><span data-stu-id="b69b0-118">_travel_</span></span> <br/> |<span data-ttu-id="b69b0-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b69b0-119">Required</span></span>  <br/> |<span data-ttu-id="b69b0-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="b69b0-120">**Double**</span></span> <br/> |<span data-ttu-id="b69b0-121">Процент по пути от точки начала до конца.</span><span class="sxs-lookup"><span data-stu-id="b69b0-121">The percentage along the path from begin point to end point.</span></span> <span data-ttu-id="b69b0-122">Должно быть от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="b69b0-122">Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="b69b0-123">_segment_</span><span class="sxs-lookup"><span data-stu-id="b69b0-123">_segment_</span></span> <br/> |<span data-ttu-id="b69b0-124">Необязательный</span><span class="sxs-lookup"><span data-stu-id="b69b0-124">Optional</span></span>  <br/> |<span data-ttu-id="b69b0-125">**Integer**</span><span class="sxs-lookup"><span data-stu-id="b69b0-125">**Integer**</span></span> <br/> |<span data-ttu-id="b69b0-126">1-й сегмент пути для вычисления касающегося угла.</span><span class="sxs-lookup"><span data-stu-id="b69b0-126">The 1-based segment of the path at which to calculate the tangent angle.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b69b0-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b69b0-127">Return value</span></span>

 <span data-ttu-id="b69b0-128">**Double**</span><span class="sxs-lookup"><span data-stu-id="b69b0-128">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b69b0-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="b69b0-129">Remarks</span></span>

<span data-ttu-id="b69b0-130">Если вы включаете  _значение сегмента,_ ANGLEALONGPATH возвращает значение только для этого сегмента.</span><span class="sxs-lookup"><span data-stu-id="b69b0-130">If you include a  _segment_ value, ANGLEALONGPATH returns the value for that segment only.</span></span> 
  
<span data-ttu-id="b69b0-131">Если вы включаете значение _сегмента,_ ANGLEALONGPATH определяет точку касательной с помощью перемещения для вычисления перцертажа вдоль _сегмента_. </span><span class="sxs-lookup"><span data-stu-id="b69b0-131">If you include a  _segment_ value, ANGLEALONGPATH determines the point of the tangent by using  _travel_ to calculate the percertage along  _segment_.</span></span>
  
<span data-ttu-id="b69b0-132">Если раздел _или_ _сегмент_ не существует, корпорация Майкрософт Visio возвращает #REF!.</span><span class="sxs-lookup"><span data-stu-id="b69b0-132">If either  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

