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
description: Возвращает арксинус числа, например угол, синус которого равен числу.
ms.openlocfilehash: a7585dc07053466203f11cc04ce249ceb62fbda0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432823"
---
# <a name="asin-function"></a><span data-ttu-id="cb803-103">Функция ASIN</span><span class="sxs-lookup"><span data-stu-id="cb803-103">ASIN Function</span></span>

<span data-ttu-id="cb803-104">Возвращает арксинус числа, например угол, синус которого равен *числу* .</span><span class="sxs-lookup"><span data-stu-id="cb803-104">Returns the arcsine of a number, for example, the angle whose sine is  *number*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="cb803-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb803-105">Syntax</span></span>

<span data-ttu-id="cb803-106">ASIN (\* \* *число* \* \*)</span><span class="sxs-lookup"><span data-stu-id="cb803-106">ASIN(\*\* *number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="cb803-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb803-107">Parameters</span></span>

|<span data-ttu-id="cb803-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="cb803-108">**Name**</span></span>|<span data-ttu-id="cb803-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="cb803-109">**Required/Optional**</span></span>|<span data-ttu-id="cb803-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="cb803-110">**Data Type**</span></span>|<span data-ttu-id="cb803-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cb803-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="cb803-112">_число_</span><span class="sxs-lookup"><span data-stu-id="cb803-112">_number_</span></span> <br/> |<span data-ttu-id="cb803-113">Обязательна</span><span class="sxs-lookup"><span data-stu-id="cb803-113">Required</span></span>  <br/> |<span data-ttu-id="cb803-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="cb803-114">**Numeric**</span></span> <br/> |<span data-ttu-id="cb803-115">Синус угла.</span><span class="sxs-lookup"><span data-stu-id="cb803-115">The sine of the angle.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb803-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="cb803-116">Remarks</span></span>

<span data-ttu-id="cb803-117">Входное значение должно быть в диапазоне от 1 <= *число* <= 1 или #NUM!</span><span class="sxs-lookup"><span data-stu-id="cb803-117">The input value must be in the range -1 <=  *number*  <= 1, or a #NUM!</span></span> <span data-ttu-id="cb803-118">возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="cb803-118">error is returned.</span></span> <span data-ttu-id="cb803-119">Полученный угол находится в диапазоне-Пи/2 <= *angle* <= Пи/2 радианы (-90 <= *угол* <= 90 градусов).</span><span class="sxs-lookup"><span data-stu-id="cb803-119">The resulting angle is in the range -PI/2 <=  *angle*  <= PI/2 radians (-90 <=  *angle*  <= 90 degrees).</span></span> 
  
## <a name="example"></a><span data-ttu-id="cb803-120">Пример</span><span class="sxs-lookup"><span data-stu-id="cb803-120">Example</span></span>

<span data-ttu-id="cb803-121">ASIN (1)</span><span class="sxs-lookup"><span data-stu-id="cb803-121">ASIN(1)</span></span>
  
<span data-ttu-id="cb803-122">Возвращает 90 град</span><span class="sxs-lookup"><span data-stu-id="cb803-122">Returns 90 deg</span></span>
  

