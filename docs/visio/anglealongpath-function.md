---
title: Функция ANGLEALONGPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Возвращает угол тангенса для пути в заданной точке.
ms.openlocfilehash: 0d38fc0e123a7e38b7826b55415cfc09c1789c0e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407328"
---
# <a name="anglealongpath-function"></a><span data-ttu-id="4ed8e-103">Функция ANGLEALONGPATH</span><span class="sxs-lookup"><span data-stu-id="4ed8e-103">ANGLEALONGPATH Function</span></span>

<span data-ttu-id="4ed8e-104">Возвращает угол тангенса для пути в заданной точке.</span><span class="sxs-lookup"><span data-stu-id="4ed8e-104">Returns the angle of the tangent to the path at a given point.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="4ed8e-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="4ed8e-105">Version Information</span></span>

<span data-ttu-id="4ed8e-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="4ed8e-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4ed8e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ed8e-107">Syntax</span></span>

<span data-ttu-id="4ed8e-108">ANGLEALONGPATH (\* \* *раздел* \* \*, \* \* *путешествие* \* \* \* \* *[, сегмент]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="4ed8e-108">ANGLEALONGPATH(\*\* *section* \*\*, \*\* *travel* \*\* \*\* *[,segment]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4ed8e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ed8e-109">Parameters</span></span>

|<span data-ttu-id="4ed8e-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="4ed8e-110">**Name**</span></span>|<span data-ttu-id="4ed8e-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="4ed8e-111">**Required/Optional**</span></span>|<span data-ttu-id="4ed8e-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="4ed8e-112">**Data Type**</span></span>|<span data-ttu-id="4ed8e-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4ed8e-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4ed8e-114">_section_</span><span class="sxs-lookup"><span data-stu-id="4ed8e-114">_section_</span></span> <br/> |<span data-ttu-id="4ed8e-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4ed8e-115">Required</span></span>  <br/> |<span data-ttu-id="4ed8e-116">**String**</span><span class="sxs-lookup"><span data-stu-id="4ed8e-116">**String**</span></span> <br/> |<span data-ttu-id="4ed8e-117">Раздел геометрии, представляющий путь, заданный ссылкой на ячейку пути (например, Geometry1. Path).</span><span class="sxs-lookup"><span data-stu-id="4ed8e-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="4ed8e-118">_дающих_</span><span class="sxs-lookup"><span data-stu-id="4ed8e-118">_travel_</span></span> <br/> |<span data-ttu-id="4ed8e-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4ed8e-119">Required</span></span>  <br/> |<span data-ttu-id="4ed8e-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="4ed8e-120">**Double**</span></span> <br/> |<span data-ttu-id="4ed8e-121">Процентная доля пути от начала до конечной точки.</span><span class="sxs-lookup"><span data-stu-id="4ed8e-121">The percentage along the path from begin point to end point.</span></span> <span data-ttu-id="4ed8e-122">Значение должно находиться в пределах от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="4ed8e-122">Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="4ed8e-123">_сегмент_</span><span class="sxs-lookup"><span data-stu-id="4ed8e-123">_segment_</span></span> <br/> |<span data-ttu-id="4ed8e-124">Необязательный</span><span class="sxs-lookup"><span data-stu-id="4ed8e-124">Optional</span></span>  <br/> |<span data-ttu-id="4ed8e-125">**Integer**</span><span class="sxs-lookup"><span data-stu-id="4ed8e-125">**Integer**</span></span> <br/> |<span data-ttu-id="4ed8e-126">Сегмент на основе 1 пути, по которому вычисляется угол тангенса.</span><span class="sxs-lookup"><span data-stu-id="4ed8e-126">The 1-based segment of the path at which to calculate the tangent angle.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="4ed8e-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4ed8e-127">Return value</span></span>

 <span data-ttu-id="4ed8e-128">**Double**</span><span class="sxs-lookup"><span data-stu-id="4ed8e-128">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4ed8e-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="4ed8e-129">Remarks</span></span>

<span data-ttu-id="4ed8e-130">Если вы включаете значение _сегмента_ , ANGLEALONGPATH возвращает значение только для этого сегмента.</span><span class="sxs-lookup"><span data-stu-id="4ed8e-130">If you include a  _segment_ value, ANGLEALONGPATH returns the value for that segment only.</span></span> 
  
<span data-ttu-id="4ed8e-131">Если вы включаете значение _сегмента_ , ANGLEALONGPATH определяет точку тангенса с помощью функции _командировок_ для вычисления _сегмента_перцертаже.</span><span class="sxs-lookup"><span data-stu-id="4ed8e-131">If you include a  _segment_ value, ANGLEALONGPATH determines the point of the tangent by using  _travel_ to calculate the percertage along  _segment_.</span></span>
  
<span data-ttu-id="4ed8e-132">Если один _раздел_ или _сегмент_ не существует, Microsoft Visio возвращает #REF!.</span><span class="sxs-lookup"><span data-stu-id="4ed8e-132">If either  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

