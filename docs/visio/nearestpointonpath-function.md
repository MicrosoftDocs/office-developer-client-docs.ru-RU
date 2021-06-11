---
title: Функция NEARESTPOINTONPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 539bf79a-df09-2048-2aba-8c863dd26fc2
description: Возвращает процент расстояния по пути точки, ближайшей к указанным координатам, в качестве значения от 0 до 1.
ms.openlocfilehash: ced20cdf1f3531eafaa03c2666b09334029fd3da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407335"
---
# <a name="nearestpointonpath-function"></a><span data-ttu-id="6d303-103">Функция NEARESTPOINTONPATH</span><span class="sxs-lookup"><span data-stu-id="6d303-103">NEARESTPOINTONPATH Function</span></span>

<span data-ttu-id="6d303-104">Возвращает процент расстояния по пути точки, ближайшей к указанным координатам, в качестве значения от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="6d303-104">Returns the percentage of the distance along the path of the point that is nearest to the specified coordinates, as a value between 0 and 1.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="6d303-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="6d303-105">Version Information</span></span>

<span data-ttu-id="6d303-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="6d303-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6d303-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d303-107">Syntax</span></span>

<span data-ttu-id="6d303-108">NEARESTPOINTONPATH(\*\* *раздел* \*\*, \*\* *x* \*\*, \*\* *y* \*\* )</span><span class="sxs-lookup"><span data-stu-id="6d303-108">NEARESTPOINTONPATH(\*\* *section* \*\*, \*\* *x* \*\*, \*\* *y* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6d303-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d303-109">Parameters</span></span>

|<span data-ttu-id="6d303-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="6d303-110">**Name**</span></span>|<span data-ttu-id="6d303-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="6d303-111">**Required/Optional**</span></span>|<span data-ttu-id="6d303-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="6d303-112">**Data Type**</span></span>|<span data-ttu-id="6d303-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6d303-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6d303-114">_section_</span><span class="sxs-lookup"><span data-stu-id="6d303-114">_section_</span></span> <br/> |<span data-ttu-id="6d303-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6d303-115">Required</span></span>  <br/> |<span data-ttu-id="6d303-116">**String**</span><span class="sxs-lookup"><span data-stu-id="6d303-116">**String**</span></span> <br/> |<span data-ttu-id="6d303-117">Раздел Геометрия, который представляет путь, заданный ссылкой на его ячейку Path (например, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="6d303-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="6d303-118">_x_</span><span class="sxs-lookup"><span data-stu-id="6d303-118">_x_</span></span> <br/> |<span data-ttu-id="6d303-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6d303-119">Required</span></span>  <br/> |<span data-ttu-id="6d303-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="6d303-120">**Double**</span></span> <br/> |<span data-ttu-id="6d303-121">X-координата указанной точки. </span><span class="sxs-lookup"><span data-stu-id="6d303-121">The  _x_-coordinate of the specified point.</span></span>  <br/> |
| <span data-ttu-id="6d303-122">_y_</span><span class="sxs-lookup"><span data-stu-id="6d303-122">_y_</span></span> <br/> |<span data-ttu-id="6d303-123">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6d303-123">Required</span></span>  <br/> |<span data-ttu-id="6d303-124">**Double**</span><span class="sxs-lookup"><span data-stu-id="6d303-124">**Double**</span></span> <br/> |<span data-ttu-id="6d303-125">Y-координата указанной точки. </span><span class="sxs-lookup"><span data-stu-id="6d303-125">The  _y_-coordinate of the specified point.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="6d303-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d303-126">Return value</span></span>

 <span data-ttu-id="6d303-127">**Double**</span><span class="sxs-lookup"><span data-stu-id="6d303-127">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6d303-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="6d303-128">Remarks</span></span>

<span data-ttu-id="6d303-129">Если _раздел_ не существует, корпорация Майкрософт Visio возвращает #REF!.</span><span class="sxs-lookup"><span data-stu-id="6d303-129">If  _section_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

