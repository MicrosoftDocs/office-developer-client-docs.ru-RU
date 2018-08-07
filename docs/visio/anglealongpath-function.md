---
title: Функция ANGLEALONGPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Возвращает тангенс угла пути в данный момент.
ms.openlocfilehash: ec5529037275fc8661972cc7403886cd33150b38
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813174"
---
# <a name="anglealongpath-function"></a><span data-ttu-id="4f97b-103">Функция ANGLEALONGPATH</span><span class="sxs-lookup"><span data-stu-id="4f97b-103">ANGLEALONGPATH Function</span></span>

<span data-ttu-id="4f97b-104">Возвращает тангенс угла пути в данный момент.</span><span class="sxs-lookup"><span data-stu-id="4f97b-104">Returns the angle of the tangent to the path at a given point.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="4f97b-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="4f97b-105">Version Information</span></span>

<span data-ttu-id="4f97b-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="4f97b-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4f97b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f97b-107">Syntax</span></span>

<span data-ttu-id="4f97b-108">ANGLEALONGPATH (** *раздел* **, ** *путешествий* ** ** *[, сегмент]* **)</span><span class="sxs-lookup"><span data-stu-id="4f97b-108">ANGLEALONGPATH(** *section* **, ** *travel* ** ** *[,segment]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4f97b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f97b-109">Parameters</span></span>

|<span data-ttu-id="4f97b-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="4f97b-110">**Name**</span></span>|<span data-ttu-id="4f97b-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="4f97b-111">**Required/Optional**</span></span>|<span data-ttu-id="4f97b-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="4f97b-112">**Data Type**</span></span>|<span data-ttu-id="4f97b-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4f97b-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4f97b-114">_section_</span><span class="sxs-lookup"><span data-stu-id="4f97b-114">_section_</span></span> <br/> |<span data-ttu-id="4f97b-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4f97b-115">Required</span></span>  <br/> |<span data-ttu-id="4f97b-116">**Строка**</span><span class="sxs-lookup"><span data-stu-id="4f97b-116">**String**</span></span> <br/> |<span data-ttu-id="4f97b-117">Раздел геометрии, представляющий путь, указанный с помощью ссылки на его ячейку Path (например, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="4f97b-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="4f97b-118">_поездки_</span><span class="sxs-lookup"><span data-stu-id="4f97b-118">_travel_</span></span> <br/> |<span data-ttu-id="4f97b-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4f97b-119">Required</span></span>  <br/> |<span data-ttu-id="4f97b-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="4f97b-120">**Double**</span></span> <br/> |<span data-ttu-id="4f97b-121">Процент по пути из начальной точки конечную точку.</span><span class="sxs-lookup"><span data-stu-id="4f97b-121">The percentage along the path from begin point to end point.</span></span> <span data-ttu-id="4f97b-122">Должен быть в диапазоне от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="4f97b-122">Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="4f97b-123">_сегмента_</span><span class="sxs-lookup"><span data-stu-id="4f97b-123">_segment_</span></span> <br/> |<span data-ttu-id="4f97b-124">Optional</span><span class="sxs-lookup"><span data-stu-id="4f97b-124">Optional</span></span>  <br/> |<span data-ttu-id="4f97b-125">**Integer**</span><span class="sxs-lookup"><span data-stu-id="4f97b-125">**Integer**</span></span> <br/> |<span data-ttu-id="4f97b-126">На основе 1 сегмент путь, на котором для вычисления тангенс угла.</span><span class="sxs-lookup"><span data-stu-id="4f97b-126">The 1-based segment of the path at which to calculate the tangent angle.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="4f97b-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7">Return value</span></span>

 <span data-ttu-id="4f97b-128">**Double**</span><span class="sxs-lookup"><span data-stu-id="4f97b-128">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4f97b-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="4f97b-129">Remarks</span></span>

<span data-ttu-id="4f97b-130">Если включить значение _сегмента_ ANGLEALONGPATH возвращает значение сегмента только.</span><span class="sxs-lookup"><span data-stu-id="4f97b-130">If you include a  _segment_ value, ANGLEALONGPATH returns the value for that segment only.</span></span> 
  
<span data-ttu-id="4f97b-131">При включении значение _сегмента_ ANGLEALONGPATH определяет точку тангенс с помощью _выезжает_ для вычисления percertage по _сегмента_.</span><span class="sxs-lookup"><span data-stu-id="4f97b-131">If you include a  _segment_ value, ANGLEALONGPATH determines the point of the tangent by using  _travel_ to calculate the percertage along  _segment_.</span></span>
  
<span data-ttu-id="4f97b-132">Если _раздел_ или _Сегмент_ не существует, Microsoft Visio возвращает #REF!.</span><span class="sxs-lookup"><span data-stu-id="4f97b-132">If either  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

