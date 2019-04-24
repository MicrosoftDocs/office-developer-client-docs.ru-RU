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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341526"
---
# <a name="asin-function"></a><span data-ttu-id="ce0a9-103">Функция ASIN</span><span class="sxs-lookup"><span data-stu-id="ce0a9-103">ASIN Function</span></span>

<span data-ttu-id="ce0a9-104">Возвращает арксинус числа, например угол, синус которого равен *числу* .</span><span class="sxs-lookup"><span data-stu-id="ce0a9-104">Returns the arcsine of a number, for example, the angle whose sine is  *number*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ce0a9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce0a9-105">Syntax</span></span>

<span data-ttu-id="ce0a9-106">ASIN (\* \* *число* \* \*)</span><span class="sxs-lookup"><span data-stu-id="ce0a9-106">ASIN(\*\* *number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ce0a9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce0a9-107">Parameters</span></span>

|<span data-ttu-id="ce0a9-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="ce0a9-108">**Name**</span></span>|<span data-ttu-id="ce0a9-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="ce0a9-109">**Required/Optional**</span></span>|<span data-ttu-id="ce0a9-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="ce0a9-110">**Data Type**</span></span>|<span data-ttu-id="ce0a9-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ce0a9-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ce0a9-112">_число_</span><span class="sxs-lookup"><span data-stu-id="ce0a9-112">_number_</span></span> <br/> |<span data-ttu-id="ce0a9-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ce0a9-113">Required</span></span>  <br/> |<span data-ttu-id="ce0a9-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="ce0a9-114">**Numeric**</span></span> <br/> |<span data-ttu-id="ce0a9-115">Синус угла.</span><span class="sxs-lookup"><span data-stu-id="ce0a9-115">The sine of the angle.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce0a9-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ce0a9-116">Remarks</span></span>

<span data-ttu-id="ce0a9-117">Входное значение должно быть в диапазоне от 1 _Лт_ = *число* _лт_ = 1 или #NUM!</span><span class="sxs-lookup"><span data-stu-id="ce0a9-117">The input value must be in the range -1 <=  *number*  <= 1, or a #NUM!</span></span> <span data-ttu-id="ce0a9-118">возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="ce0a9-118">error is returned.</span></span> <span data-ttu-id="ce0a9-119">Полученный угол находится в диапазоне-Пи/2 _Лт_ = *Angle* _ЛТ_ = PI/2 радиан (-90 _лт_ = *угол* _лт_ = 90 градусов).</span><span class="sxs-lookup"><span data-stu-id="ce0a9-119">The resulting angle is in the range -PI/2 <=  *angle*  <= PI/2 radians (-90 <=  *angle*  <= 90 degrees).</span></span> 
  
## <a name="example"></a><span data-ttu-id="ce0a9-120">Пример</span><span class="sxs-lookup"><span data-stu-id="ce0a9-120">Example</span></span>

<span data-ttu-id="ce0a9-121">ASIN (1)</span><span class="sxs-lookup"><span data-stu-id="ce0a9-121">ASIN(1)</span></span>
  
<span data-ttu-id="ce0a9-122">Возвращает 90 град</span><span class="sxs-lookup"><span data-stu-id="ce0a9-122">Returns 90 deg</span></span>
  

