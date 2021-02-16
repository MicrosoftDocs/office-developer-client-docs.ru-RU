---
title: Функция ASIN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251395
localization_priority: Normal
ms.assetid: 7d917be4-65b1-002f-48cc-6d81916a1157
description: Возвращает арксинус числа, например угол, чей sine является числом.
ms.openlocfilehash: e66ed9ab3d01ac79bceb18f5c793afc928e5e4b4
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293508"
---
# <a name="asin-function"></a><span data-ttu-id="a98dc-103">Функция ASIN</span><span class="sxs-lookup"><span data-stu-id="a98dc-103">ASIN Function</span></span>

<span data-ttu-id="a98dc-104">Возвращает арксинус числа, например угол, чей sine — *число.*</span><span class="sxs-lookup"><span data-stu-id="a98dc-104">Returns the arcsine of a number, for example, the angle whose sine is  *number*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a98dc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a98dc-105">Syntax</span></span>

<span data-ttu-id="a98dc-106">***ASIN(number)***</span><span class="sxs-lookup"><span data-stu-id="a98dc-106">ASIN(***number*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a98dc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a98dc-107">Parameters</span></span>

|<span data-ttu-id="a98dc-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="a98dc-108">**Name**</span></span>|<span data-ttu-id="a98dc-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="a98dc-109">**Required/Optional**</span></span>|<span data-ttu-id="a98dc-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="a98dc-110">**Data Type**</span></span>|<span data-ttu-id="a98dc-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a98dc-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a98dc-112">_число_</span><span class="sxs-lookup"><span data-stu-id="a98dc-112">_number_</span></span> <br/> |<span data-ttu-id="a98dc-113">Обязательна</span><span class="sxs-lookup"><span data-stu-id="a98dc-113">Required</span></span>  <br/> |<span data-ttu-id="a98dc-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="a98dc-114">**Numeric**</span></span> <br/> |<span data-ttu-id="a98dc-115">Sine угла.</span><span class="sxs-lookup"><span data-stu-id="a98dc-115">The sine of the angle.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a98dc-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="a98dc-116">Remarks</span></span>

<span data-ttu-id="a98dc-117">Входное значение должно быть в диапазоне -1 <=  *номер*  <= 1 или #NUM!</span><span class="sxs-lookup"><span data-stu-id="a98dc-117">The input value must be in the range -1 <=  *number*  <= 1, or a #NUM!</span></span> <span data-ttu-id="a98dc-118">возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="a98dc-118">error is returned.</span></span> <span data-ttu-id="a98dc-119">В результате угол находится в диапазоне -PI/2 < *=*  угол <= PI/2 радиан (-90 <=  *угол*  <= 90 градусов).</span><span class="sxs-lookup"><span data-stu-id="a98dc-119">The resulting angle is in the range -PI/2 <=  *angle*  <= PI/2 radians (-90 <=  *angle*  <= 90 degrees).</span></span> 
  
## <a name="example"></a><span data-ttu-id="a98dc-120">Пример</span><span class="sxs-lookup"><span data-stu-id="a98dc-120">Example</span></span>

<span data-ttu-id="a98dc-121">ASIN(1)</span><span class="sxs-lookup"><span data-stu-id="a98dc-121">ASIN(1)</span></span>
  
<span data-ttu-id="a98dc-122">Возвращает 90 deg</span><span class="sxs-lookup"><span data-stu-id="a98dc-122">Returns 90 deg</span></span>
  

