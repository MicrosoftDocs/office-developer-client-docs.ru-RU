---
title: DATE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251412
localization_priority: Normal
ms.assetid: 2b6c5375-c543-ff2f-f20a-6d92fd65717a
description: Возврат значения даты, представленной года, месяца и дня отформатированное в соответствии с краткий формат в региональных параметрах компьютера. Значения для года, месяца и дня отражают григорианский календарь.
ms.openlocfilehash: 7a19d97f70f9314ecdbd2228078e1e18b1ac9146
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813566"
---
# <a name="date-function-visioshapesheet"></a><span data-ttu-id="be40b-104">DATE Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="be40b-104">DATE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="be40b-105">Возврат значения даты, представленной *год, месяц,* *день* и отформатированное в соответствии с краткий формат в региональных параметрах компьютера.</span><span class="sxs-lookup"><span data-stu-id="be40b-105">Returns the date represented by  *year, month,*  and  *day*  formatted according to the short date style in the system's Regional Settings.</span></span> <span data-ttu-id="be40b-106">Значения для *года*, *месяца* и *дня* отражают григорианский календарь.</span><span class="sxs-lookup"><span data-stu-id="be40b-106">The values for  *year*, *month*  , and  *day*  reflect the Gregorian calendar.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="be40b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be40b-107">Syntax</span></span>

<span data-ttu-id="be40b-108">Дата (** *год* **, ** *месяц* **, ** *день* **)</span><span class="sxs-lookup"><span data-stu-id="be40b-108">DATE(** *year* **, ** *month* **, ** *day* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="be40b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="be40b-109">Parameters</span></span>

|<span data-ttu-id="be40b-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="be40b-110">**Name**</span></span>|<span data-ttu-id="be40b-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="be40b-111">**Required/Optional**</span></span>|<span data-ttu-id="be40b-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="be40b-112">**Data Type**</span></span>|<span data-ttu-id="be40b-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="be40b-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="be40b-114">_year_</span><span class="sxs-lookup"><span data-stu-id="be40b-114">_year_</span></span> <br/> |<span data-ttu-id="be40b-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="be40b-115">Required</span></span>  <br/> |<span data-ttu-id="be40b-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="be40b-116">**Integer**</span></span> <br/> |<span data-ttu-id="be40b-117">Год.</span><span class="sxs-lookup"><span data-stu-id="be40b-117">The year.</span></span>  <br/> |
| <span data-ttu-id="be40b-118">_month_</span><span class="sxs-lookup"><span data-stu-id="be40b-118">_month_</span></span> <br/> |<span data-ttu-id="be40b-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="be40b-119">Required</span></span>  <br/> |<span data-ttu-id="be40b-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="be40b-120">**Integer**</span></span> <br/> |<span data-ttu-id="be40b-121">Месяц.</span><span class="sxs-lookup"><span data-stu-id="be40b-121">The month.</span></span>  <br/> |
| <span data-ttu-id="be40b-122">_день_</span><span class="sxs-lookup"><span data-stu-id="be40b-122">_day_</span></span> <br/> |<span data-ttu-id="be40b-123">Обязательный</span><span class="sxs-lookup"><span data-stu-id="be40b-123">Required</span></span>  <br/> |<span data-ttu-id="be40b-124">**Integer**</span><span class="sxs-lookup"><span data-stu-id="be40b-124">**Integer**</span></span> <br/> |<span data-ttu-id="be40b-125">День.</span><span class="sxs-lookup"><span data-stu-id="be40b-125">The day.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="be40b-126">Пример 1</span><span class="sxs-lookup"><span data-stu-id="be40b-126">Example 1</span></span>

<span data-ttu-id="be40b-127">DATE(1999,6,7)</span><span class="sxs-lookup"><span data-stu-id="be40b-127">DATE(1999,6,7)</span></span>
  
<span data-ttu-id="be40b-128">Возвращает значение, представляющее 6 и 7/1999 г.</span><span class="sxs-lookup"><span data-stu-id="be40b-128">Returns the value representing 6/7/1999.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="be40b-129">Пример 2</span><span class="sxs-lookup"><span data-stu-id="be40b-129">Example 2</span></span>

<span data-ttu-id="be40b-130">Date(1999,6,7) + 4 ed.</span><span class="sxs-lookup"><span data-stu-id="be40b-130">DATE(1999,6,7) + 4 ed.</span></span>
  
<span data-ttu-id="be40b-131">Возвращает значение, представляющее 6/11/1999 г.</span><span class="sxs-lookup"><span data-stu-id="be40b-131">Returns the value representing 6/11/1999.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="be40b-132">Пример 3</span><span class="sxs-lookup"><span data-stu-id="be40b-132">Example 3</span></span>

<span data-ttu-id="be40b-133">FORMAT(DATE(1999,10,14),"C")</span><span class="sxs-lookup"><span data-stu-id="be40b-133">FORMAT(DATE(1999,10,14),"C")</span></span>
  
<span data-ttu-id="be40b-134">Возвращает значение, представляющее вторник 14 октября 1999 г.</span><span class="sxs-lookup"><span data-stu-id="be40b-134">Returns the value representing Tuesday, October 14, 1999.</span></span>
  

