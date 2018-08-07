---
title: Функция DISTTOPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ba7d372-0c2a-9fa7-0af6-97da0aafdb12
description: Возвращает короткий расстояние от точки, представленной по указанным координатам точку на пути.
ms.openlocfilehash: 227fe860de2e3683b5d7d3e5f9313d1e2e31b2d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813632"
---
# <a name="disttopath-function"></a><span data-ttu-id="51152-103">Функция DISTTOPATH</span><span class="sxs-lookup"><span data-stu-id="51152-103">DISTTOPATH Function</span></span>

<span data-ttu-id="51152-104">Возвращает короткий расстояние от точки, представленной по указанным координатам точку на пути.</span><span class="sxs-lookup"><span data-stu-id="51152-104">Returns the shortest distance from the point represented by the specified coordinates to a point on the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="51152-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="51152-105">Version Information</span></span>

<span data-ttu-id="51152-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="51152-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="51152-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51152-107">Syntax</span></span>

<span data-ttu-id="51152-108">DISTTOPATH (** *раздел* **, ** *x* **, ** *y* **)</span><span class="sxs-lookup"><span data-stu-id="51152-108">DISTTOPATH(** *section* **, ** *x* **, ** *y* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="51152-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="51152-109">Parameters</span></span>

|<span data-ttu-id="51152-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="51152-110">**Name**</span></span>|<span data-ttu-id="51152-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="51152-111">**Required/Optional**</span></span>|<span data-ttu-id="51152-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="51152-112">**Data Type**</span></span>|<span data-ttu-id="51152-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="51152-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="51152-114">_section_</span><span class="sxs-lookup"><span data-stu-id="51152-114">_section_</span></span> <br/> |<span data-ttu-id="51152-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="51152-115">Required</span></span>  <br/> |<span data-ttu-id="51152-116">**Строка**</span><span class="sxs-lookup"><span data-stu-id="51152-116">**String**</span></span> <br/> |<span data-ttu-id="51152-117">Раздел геометрии, представляющий путь, указанный с помощью ссылки на его ячейку Path (например, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="51152-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="51152-118">_x_</span><span class="sxs-lookup"><span data-stu-id="51152-118">_x_</span></span> <br/> |<span data-ttu-id="51152-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="51152-119">Required</span></span>  <br/> |<span data-ttu-id="51152-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="51152-120">**Double**</span></span> <br/> |<span data-ttu-id="51152-121">_X_-координаты точки.</span><span class="sxs-lookup"><span data-stu-id="51152-121">The  _x_-coordinate of the point.</span></span>  <br/> |
| <span data-ttu-id="51152-122">_y_</span><span class="sxs-lookup"><span data-stu-id="51152-122">_y_</span></span> <br/> |<span data-ttu-id="51152-123">Обязательный</span><span class="sxs-lookup"><span data-stu-id="51152-123">Required</span></span>  <br/> |<span data-ttu-id="51152-124">**Double**</span><span class="sxs-lookup"><span data-stu-id="51152-124">**Double**</span></span> <br/> |<span data-ttu-id="51152-125">_Y_-координаты точки.</span><span class="sxs-lookup"><span data-stu-id="51152-125">The  _y_-coordinate of the point.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="51152-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6">Return value</span></span>

 <span data-ttu-id="51152-127">**Double**</span><span class="sxs-lookup"><span data-stu-id="51152-127">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="51152-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="51152-128">Remarks</span></span>

<span data-ttu-id="51152-129">Microsoft Visio возвращает #REF!</span><span class="sxs-lookup"><span data-stu-id="51152-129">Microsoft Visio returns #REF!</span></span> <span data-ttu-id="51152-130">Если _раздел_ не существует.</span><span class="sxs-lookup"><span data-stu-id="51152-130">if  _section_ does not exist.</span></span> 
  
<span data-ttu-id="51152-131">Возвращаемое значение является положительным, если точка находится слева от направления командировки; является отрицательным точка находится справа от направления командировок.</span><span class="sxs-lookup"><span data-stu-id="51152-131">The returned value is positive if the point is to the left of the direction of travel; it is negative if the point is to the right of the direction of travel.</span></span>
  

