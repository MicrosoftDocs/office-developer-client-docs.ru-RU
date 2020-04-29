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
ms.openlocfilehash: 017dd89bd3b814c10422cd32eea1ee7e343eaf50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417198"
---
# <a name="ang360-function"></a><span data-ttu-id="32fcf-103">Функция ANG360</span><span class="sxs-lookup"><span data-stu-id="32fcf-103">ANG360 Function</span></span>

<span data-ttu-id="32fcf-104">Нормализует диапазон \<угла до 0 = результат \< 2pi радиан (0 \<= результат \< 360 градусов).</span><span class="sxs-lookup"><span data-stu-id="32fcf-104">Normalizes an angle's range to be 0 \<= result \< 2PI radians (0 \<= result \< 360 degrees).</span></span>
  
## <a name="syntax"></a><span data-ttu-id="32fcf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32fcf-105">Syntax</span></span>

<span data-ttu-id="32fcf-106">ANG360 (\* \* *угол* \* \*)</span><span class="sxs-lookup"><span data-stu-id="32fcf-106">ANG360(\*\* *angle* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="32fcf-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="32fcf-107">Parameters</span></span>

|<span data-ttu-id="32fcf-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="32fcf-108">**Name**</span></span>|<span data-ttu-id="32fcf-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="32fcf-109">**Required/Optional**</span></span>|<span data-ttu-id="32fcf-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="32fcf-110">**Data Type**</span></span>|<span data-ttu-id="32fcf-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="32fcf-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="32fcf-112">_градусов_</span><span class="sxs-lookup"><span data-stu-id="32fcf-112">_angle_</span></span> <br/> |<span data-ttu-id="32fcf-113">Обязательна</span><span class="sxs-lookup"><span data-stu-id="32fcf-113">Required</span></span>  <br/> |<span data-ttu-id="32fcf-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="32fcf-114">**Numeric**</span></span> <br/> |<span data-ttu-id="32fcf-115">Угол для нормализации.</span><span class="sxs-lookup"><span data-stu-id="32fcf-115">The angle to be normalized.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="32fcf-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="32fcf-116">Remarks</span></span>

<span data-ttu-id="32fcf-117">Если *угол* не указан с помощью угловых единиц, он интерпретируется как радианы.</span><span class="sxs-lookup"><span data-stu-id="32fcf-117">If  *angle*  is not specified by using angular units, it is interpreted as radians.</span></span> <span data-ttu-id="32fcf-118">Если *угол* не может быть преобразован в значение, то #VALUE!</span><span class="sxs-lookup"><span data-stu-id="32fcf-118">If  *angle*  cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="32fcf-119">возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="32fcf-119">error is returned.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="32fcf-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="32fcf-120">Example 1</span></span>

<span data-ttu-id="32fcf-121">ANG360 (395 градусов)</span><span class="sxs-lookup"><span data-stu-id="32fcf-121">ANG360(395 deg)</span></span>
  
<span data-ttu-id="32fcf-122">Возвращает 35 град</span><span class="sxs-lookup"><span data-stu-id="32fcf-122">Returns 35 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="32fcf-123">Пример 2</span><span class="sxs-lookup"><span data-stu-id="32fcf-123">Example 2</span></span>

<span data-ttu-id="32fcf-124">ANG360 (-9,8 RAD)</span><span class="sxs-lookup"><span data-stu-id="32fcf-124">ANG360(-9.8 rad)</span></span>
  
<span data-ttu-id="32fcf-125">Возвращает 2,7664 RAD</span><span class="sxs-lookup"><span data-stu-id="32fcf-125">Returns 2.7664 rad</span></span>
  
## <a name="example-3"></a><span data-ttu-id="32fcf-126">Пример 3</span><span class="sxs-lookup"><span data-stu-id="32fcf-126">Example 3</span></span>

<span data-ttu-id="32fcf-127">ANG360 (45)</span><span class="sxs-lookup"><span data-stu-id="32fcf-127">ANG360(45)</span></span>
  
<span data-ttu-id="32fcf-128">Возвращает 58,31 град (1,0177 RAD)</span><span class="sxs-lookup"><span data-stu-id="32fcf-128">Returns 58.31 deg (1.0177 rad)</span></span>
  

