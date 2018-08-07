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
description: Возвращает арксинус числа, например, угол, синус которого равен числу.
ms.openlocfilehash: e5ed8f9fc8c85ac4816fede03bfe6f6af5cbf5f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813185"
---
# <a name="asin-function"></a><span data-ttu-id="0d228-103">Функция ASIN</span><span class="sxs-lookup"><span data-stu-id="0d228-103">ASIN Function</span></span>

<span data-ttu-id="0d228-104">Возвращает арксинус числа, например, угол, синус которого равен *числу* .</span><span class="sxs-lookup"><span data-stu-id="0d228-104">Returns the arcsine of a number, for example, the angle whose sine is  *number*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0d228-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d228-105">Syntax</span></span>

<span data-ttu-id="0d228-106">ASIN (** *номер* **)</span><span class="sxs-lookup"><span data-stu-id="0d228-106">ASIN(** *number* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0d228-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d228-107">Parameters</span></span>

|<span data-ttu-id="0d228-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="0d228-108">**Name**</span></span>|<span data-ttu-id="0d228-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="0d228-109">**Required/Optional**</span></span>|<span data-ttu-id="0d228-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="0d228-110">**Data Type**</span></span>|<span data-ttu-id="0d228-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0d228-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0d228-112">_number_</span><span class="sxs-lookup"><span data-stu-id="0d228-112">_number_</span></span> <br/> |<span data-ttu-id="0d228-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0d228-113">Required</span></span>  <br/> |<span data-ttu-id="0d228-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="0d228-114">**Numeric**</span></span> <br/> |<span data-ttu-id="0d228-115">Синус угла.</span><span class="sxs-lookup"><span data-stu-id="0d228-115">The sine of the angle.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d228-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="0d228-116">Remarks</span></span>

<span data-ttu-id="0d228-117">Входное значение должно быть в диапазоне от -1 < = *номер* < = 1 или #NUM!</span><span class="sxs-lookup"><span data-stu-id="0d228-117">The input value must be in the range -1 <=  *number*  <= 1, or a #NUM!</span></span> <span data-ttu-id="0d228-118">возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="0d228-118">error is returned.</span></span> <span data-ttu-id="0d228-119">Полученного угла находится в диапазоне -ПИ/2 < = *угол* < = пи/2 радианов (-90 < = *угол* < = 90 градусов).</span><span class="sxs-lookup"><span data-stu-id="0d228-119">The resulting angle is in the range -PI/2 <=  *angle*  <= PI/2 radians (-90 <=  *angle*  <= 90 degrees).</span></span> 
  
## <a name="example"></a><span data-ttu-id="0d228-120">Пример</span><span class="sxs-lookup"><span data-stu-id="0d228-120">Example</span></span>

<span data-ttu-id="0d228-121">ASIN(1)</span><span class="sxs-lookup"><span data-stu-id="0d228-121">ASIN(1)</span></span>
  
<span data-ttu-id="0d228-122">Возвращает 90 градусов</span><span class="sxs-lookup"><span data-stu-id="0d228-122">Returns 90 deg</span></span>
  

