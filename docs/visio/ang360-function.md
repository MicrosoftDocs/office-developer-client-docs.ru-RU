---
title: Функция ANG360
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251392
localization_priority: Normal
ms.assetid: 23e6899d-0a94-a7d8-8de2-091e0531f163
description: Нормализует диапазон угла.
ms.openlocfilehash: 01092e06b55c73953417fe7d0fa1c9f74d668922
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813144"
---
# <a name="ang360-function"></a><span data-ttu-id="3d156-103">Функция ANG360</span><span class="sxs-lookup"><span data-stu-id="3d156-103">ANG360 Function</span></span>

<span data-ttu-id="3d156-104">Нормализует диапазон угла до 0 \<= результатов \< 2PI радианах (0 \<= результатов \< 360 градусов).</span><span class="sxs-lookup"><span data-stu-id="3d156-104">Normalizes an angle's range to be 0 \<= result \< 2PI radians (0 \<= result \< 360 degrees).</span></span>
  
## <a name="syntax"></a><span data-ttu-id="3d156-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d156-105">Syntax</span></span>

<span data-ttu-id="3d156-106">ANG360 (** *угол* **)</span><span class="sxs-lookup"><span data-stu-id="3d156-106">ANG360(** *angle* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3d156-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d156-107">Parameters</span></span>

|<span data-ttu-id="3d156-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="3d156-108">**Name**</span></span>|<span data-ttu-id="3d156-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="3d156-109">**Required/Optional**</span></span>|<span data-ttu-id="3d156-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="3d156-110">**Data Type**</span></span>|<span data-ttu-id="3d156-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3d156-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3d156-112">_угол_</span><span class="sxs-lookup"><span data-stu-id="3d156-112">_angle_</span></span> <br/> |<span data-ttu-id="3d156-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3d156-113">Required</span></span>  <br/> |<span data-ttu-id="3d156-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="3d156-114">**Numeric**</span></span> <br/> |<span data-ttu-id="3d156-115">Угол, чтобы он был нормализован.</span><span class="sxs-lookup"><span data-stu-id="3d156-115">The angle to be normalized.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d156-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="3d156-116">Remarks</span></span>

<span data-ttu-id="3d156-117">Если *угол* не указан с помощью угловые единиц измерения, он интерпретируется в радианах.</span><span class="sxs-lookup"><span data-stu-id="3d156-117">If  *angle*  is not specified by using angular units, it is interpreted as radians.</span></span> <span data-ttu-id="3d156-118">Если значение #VALUE не может быть преобразована *угол* !</span><span class="sxs-lookup"><span data-stu-id="3d156-118">If  *angle*  cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="3d156-119">возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="3d156-119">error is returned.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="3d156-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3d156-120">Example 1</span></span>

<span data-ttu-id="3d156-121">ANG360(395 deg)</span><span class="sxs-lookup"><span data-stu-id="3d156-121">ANG360(395 deg)</span></span>
  
<span data-ttu-id="3d156-122">Возвращает 35 градусов</span><span class="sxs-lookup"><span data-stu-id="3d156-122">Returns 35 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="3d156-123">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3d156-123">Example 2</span></span>

<span data-ttu-id="3d156-124">ANG360(-9.8 RAD)</span><span class="sxs-lookup"><span data-stu-id="3d156-124">ANG360(-9.8 rad)</span></span>
  
<span data-ttu-id="3d156-125">Возвращает 2.7664 rad</span><span class="sxs-lookup"><span data-stu-id="3d156-125">Returns 2.7664 rad</span></span>
  
## <a name="example-3"></a><span data-ttu-id="3d156-126">Пример 3</span><span class="sxs-lookup"><span data-stu-id="3d156-126">Example 3</span></span>

<span data-ttu-id="3d156-127">ANG360(45)</span><span class="sxs-lookup"><span data-stu-id="3d156-127">ANG360(45)</span></span>
  
<span data-ttu-id="3d156-128">Возвращает 58.31 градусов (1.0177 rad)</span><span class="sxs-lookup"><span data-stu-id="3d156-128">Returns 58.31 deg (1.0177 rad)</span></span>
  

