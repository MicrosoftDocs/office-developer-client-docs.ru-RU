---
title: Функция NEARESTPOINTONPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 539bf79a-df09-2048-2aba-8c863dd26fc2
description: Возвращает процент расстояния вдоль пути к точке, ближайшей к указанным координатам, в виде значения от 0 до 1.
ms.openlocfilehash: ced20cdf1f3531eafaa03c2666b09334029fd3da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407335"
---
# <a name="nearestpointonpath-function"></a><span data-ttu-id="adda4-103">Функция NEARESTPOINTONPATH</span><span class="sxs-lookup"><span data-stu-id="adda4-103">NEARESTPOINTONPATH Function</span></span>

<span data-ttu-id="adda4-104">Возвращает процент расстояния по пути к точке, ближайшей к указанным координатам, в виде значения от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="adda4-104">Returns the percentage of the distance along the path of the point that is nearest to the specified coordinates, as a value between 0 and 1.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="adda4-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="adda4-105">Version Information</span></span>

<span data-ttu-id="adda4-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="adda4-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="adda4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="adda4-107">Syntax</span></span>

<span data-ttu-id="adda4-108">NEARESTPOINTONPATH(\*\* *section* \*\*, \*\* *x* \*\*, \*\* *y* \*\* )</span><span class="sxs-lookup"><span data-stu-id="adda4-108">NEARESTPOINTONPATH(\*\* *section* \*\*, \*\* *x* \*\*, \*\* *y* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="adda4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="adda4-109">Parameters</span></span>

|<span data-ttu-id="adda4-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="adda4-110">**Name**</span></span>|<span data-ttu-id="adda4-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="adda4-111">**Required/Optional**</span></span>|<span data-ttu-id="adda4-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="adda4-112">**Data Type**</span></span>|<span data-ttu-id="adda4-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="adda4-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="adda4-114">_section_</span><span class="sxs-lookup"><span data-stu-id="adda4-114">_section_</span></span> <br/> |<span data-ttu-id="adda4-115">Обязательно</span><span class="sxs-lookup"><span data-stu-id="adda4-115">Required</span></span>  <br/> |<span data-ttu-id="adda4-116">**Строка**</span><span class="sxs-lookup"><span data-stu-id="adda4-116">**String**</span></span> <br/> |<span data-ttu-id="adda4-117">Раздел "Геометрия", который представляет путь, заданный ссылкой на его ячейку Path (например, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="adda4-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="adda4-118">_x_</span><span class="sxs-lookup"><span data-stu-id="adda4-118">_x_</span></span> <br/> |<span data-ttu-id="adda4-119">Обязательна</span><span class="sxs-lookup"><span data-stu-id="adda4-119">Required</span></span>  <br/> |<span data-ttu-id="adda4-120">64-разрядное число с плавающей запятой двойной точности.</span><span class="sxs-lookup"><span data-stu-id="adda4-120">**Double**</span></span> <br/> |<span data-ttu-id="adda4-121">X-координата указанной точки. </span><span class="sxs-lookup"><span data-stu-id="adda4-121">The  _x_-coordinate of the specified point.</span></span>  <br/> |
| <span data-ttu-id="adda4-122">_y_</span><span class="sxs-lookup"><span data-stu-id="adda4-122">_y_</span></span> <br/> |<span data-ttu-id="adda4-123">Обязательна</span><span class="sxs-lookup"><span data-stu-id="adda4-123">Required</span></span>  <br/> |<span data-ttu-id="adda4-124">64-разрядное число с плавающей запятой двойной точности.</span><span class="sxs-lookup"><span data-stu-id="adda4-124">**Double**</span></span> <br/> |<span data-ttu-id="adda4-125">Y-координата указанной точки. </span><span class="sxs-lookup"><span data-stu-id="adda4-125">The  _y_-coordinate of the specified point.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="adda4-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="adda4-126">Return value</span></span>

 <span data-ttu-id="adda4-127">64-разрядное число с плавающей запятой двойной точности.</span><span class="sxs-lookup"><span data-stu-id="adda4-127">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="adda4-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="adda4-128">Remarks</span></span>

<span data-ttu-id="adda4-129">Если  _раздел_ не существует, Microsoft Visio возвращает #REF!.</span><span class="sxs-lookup"><span data-stu-id="adda4-129">If  _section_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

