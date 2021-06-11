---
title: Функция DISTTOPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ba7d372-0c2a-9fa7-0af6-97da0aafdb12
description: Возвращает самое короткое расстояние от точки, представленной указанными координатами, в точку на пути.
ms.openlocfilehash: 5727b24739705d3e562150c48fe77f7ad6eedb57
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427019"
---
# <a name="disttopath-function"></a><span data-ttu-id="4a94b-103">Функция DISTTOPATH</span><span class="sxs-lookup"><span data-stu-id="4a94b-103">DISTTOPATH Function</span></span>

<span data-ttu-id="4a94b-104">Возвращает самое короткое расстояние от точки, представленной указанными координатами, в точку на пути.</span><span class="sxs-lookup"><span data-stu-id="4a94b-104">Returns the shortest distance from the point represented by the specified coordinates to a point on the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="4a94b-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="4a94b-105">Version Information</span></span>

<span data-ttu-id="4a94b-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="4a94b-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4a94b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a94b-107">Syntax</span></span>

<span data-ttu-id="4a94b-108">DISTTOPATH(\*\* *раздел* \*\*, \*\* *x* \*\*, \*\* *y* \*\* )</span><span class="sxs-lookup"><span data-stu-id="4a94b-108">DISTTOPATH(\*\* *section* \*\*, \*\* *x* \*\*, \*\* *y* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4a94b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a94b-109">Parameters</span></span>

|<span data-ttu-id="4a94b-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="4a94b-110">**Name**</span></span>|<span data-ttu-id="4a94b-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="4a94b-111">**Required/Optional**</span></span>|<span data-ttu-id="4a94b-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="4a94b-112">**Data Type**</span></span>|<span data-ttu-id="4a94b-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4a94b-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4a94b-114">_section_</span><span class="sxs-lookup"><span data-stu-id="4a94b-114">_section_</span></span> <br/> |<span data-ttu-id="4a94b-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4a94b-115">Required</span></span>  <br/> |<span data-ttu-id="4a94b-116">**String**</span><span class="sxs-lookup"><span data-stu-id="4a94b-116">**String**</span></span> <br/> |<span data-ttu-id="4a94b-117">Раздел Геометрия, который представляет путь, заданный ссылкой на его ячейку Path (например, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="4a94b-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="4a94b-118">_x_</span><span class="sxs-lookup"><span data-stu-id="4a94b-118">_x_</span></span> <br/> |<span data-ttu-id="4a94b-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4a94b-119">Required</span></span>  <br/> |<span data-ttu-id="4a94b-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="4a94b-120">**Double**</span></span> <br/> |<span data-ttu-id="4a94b-121">X-координата точки. </span><span class="sxs-lookup"><span data-stu-id="4a94b-121">The  _x_-coordinate of the point.</span></span>  <br/> |
| <span data-ttu-id="4a94b-122">_y_</span><span class="sxs-lookup"><span data-stu-id="4a94b-122">_y_</span></span> <br/> |<span data-ttu-id="4a94b-123">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4a94b-123">Required</span></span>  <br/> |<span data-ttu-id="4a94b-124">**Double**</span><span class="sxs-lookup"><span data-stu-id="4a94b-124">**Double**</span></span> <br/> |<span data-ttu-id="4a94b-125">_Y-координата_ точки.</span><span class="sxs-lookup"><span data-stu-id="4a94b-125">The  _y_-coordinate of the point.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="4a94b-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4a94b-126">Return value</span></span>

 <span data-ttu-id="4a94b-127">**Double**</span><span class="sxs-lookup"><span data-stu-id="4a94b-127">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4a94b-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="4a94b-128">Remarks</span></span>

<span data-ttu-id="4a94b-129">Microsoft Visio возвращает #REF!</span><span class="sxs-lookup"><span data-stu-id="4a94b-129">Microsoft Visio returns #REF!</span></span> <span data-ttu-id="4a94b-130">если  _раздел_ не существует.</span><span class="sxs-lookup"><span data-stu-id="4a94b-130">if  _section_ does not exist.</span></span> 
  
<span data-ttu-id="4a94b-131">Возвращаемая величина является положительной, если точка находится слева от направления перемещения; это отрицательно, если точка находится справа от направления перемещения.</span><span class="sxs-lookup"><span data-stu-id="4a94b-131">The returned value is positive if the point is to the left of the direction of travel; it is negative if the point is to the right of the direction of travel.</span></span>
  

