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
description: Возвращает дату, представленную в формате года, месяца и дня в соответствии с кратким стилем даты в региональных параметрах системы. Значения года, месяца и дня отражают григорианский календарь.
ms.openlocfilehash: 0175c1f06ec3dbdf89774759546c65994d38105e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360335"
---
# <a name="date-function-visioshapesheet"></a><span data-ttu-id="08d85-104">DATE Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="08d85-104">DATE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="08d85-105">Возвращает дату, представленную в формате  *года,* месяца и дня в соответствии с кратким стилем даты в региональных параметрах системы.</span><span class="sxs-lookup"><span data-stu-id="08d85-105">Returns the date represented by  *year, month,*  and  *day*  formatted according to the short date style in the system's Regional Settings.</span></span> <span data-ttu-id="08d85-106">Значения  *года,* *месяца и*  дня  *отражают*  григорианский календарь.</span><span class="sxs-lookup"><span data-stu-id="08d85-106">The values for  *year*, *month*  , and  *day*  reflect the Gregorian calendar.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="08d85-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08d85-107">Syntax</span></span>

<span data-ttu-id="08d85-108">DATE(\*\* *year* \*\*, \*\* *month* \*\*, \*\* *day* \*\* )</span><span class="sxs-lookup"><span data-stu-id="08d85-108">DATE(\*\* *year* \*\*, \*\* *month* \*\*, \*\* *day* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="08d85-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="08d85-109">Parameters</span></span>

|<span data-ttu-id="08d85-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="08d85-110">**Name**</span></span>|<span data-ttu-id="08d85-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="08d85-111">**Required/Optional**</span></span>|<span data-ttu-id="08d85-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="08d85-112">**Data Type**</span></span>|<span data-ttu-id="08d85-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="08d85-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="08d85-114">_year_</span><span class="sxs-lookup"><span data-stu-id="08d85-114">_year_</span></span> <br/> |<span data-ttu-id="08d85-115">Обязательна</span><span class="sxs-lookup"><span data-stu-id="08d85-115">Required</span></span>  <br/> |<span data-ttu-id="08d85-116">64-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="08d85-116">**Integer**</span></span> <br/> |<span data-ttu-id="08d85-117">Год.</span><span class="sxs-lookup"><span data-stu-id="08d85-117">The year.</span></span>  <br/> |
| <span data-ttu-id="08d85-118">_month_</span><span class="sxs-lookup"><span data-stu-id="08d85-118">_month_</span></span> <br/> |<span data-ttu-id="08d85-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="08d85-119">Required</span></span>  <br/> |<span data-ttu-id="08d85-120">64-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="08d85-120">**Integer**</span></span> <br/> |<span data-ttu-id="08d85-121">Месяц.</span><span class="sxs-lookup"><span data-stu-id="08d85-121">The month.</span></span>  <br/> |
| <span data-ttu-id="08d85-122">_day_</span><span class="sxs-lookup"><span data-stu-id="08d85-122">_day_</span></span> <br/> |<span data-ttu-id="08d85-123">Обязательна</span><span class="sxs-lookup"><span data-stu-id="08d85-123">Required</span></span>  <br/> |<span data-ttu-id="08d85-124">64-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="08d85-124">**Integer**</span></span> <br/> |<span data-ttu-id="08d85-125">День.</span><span class="sxs-lookup"><span data-stu-id="08d85-125">The day.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="08d85-126">Пример 1</span><span class="sxs-lookup"><span data-stu-id="08d85-126">Example 1</span></span>

<span data-ttu-id="08d85-127">DATE(1999,6,7)</span><span class="sxs-lookup"><span data-stu-id="08d85-127">DATE(1999,6,7)</span></span>
  
<span data-ttu-id="08d85-128">Возвращает значение, представляющее 07.06.1999.</span><span class="sxs-lookup"><span data-stu-id="08d85-128">Returns the value representing 6/7/1999.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="08d85-129">Пример 2</span><span class="sxs-lookup"><span data-stu-id="08d85-129">Example 2</span></span>

<span data-ttu-id="08d85-130">DATE(1999,6,7) + 4 ed.</span><span class="sxs-lookup"><span data-stu-id="08d85-130">DATE(1999,6,7) + 4 ed.</span></span>
  
<span data-ttu-id="08d85-131">Возвращает значение, представляющее 11.06.1999.</span><span class="sxs-lookup"><span data-stu-id="08d85-131">Returns the value representing 6/11/1999.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="08d85-132">Пример 3</span><span class="sxs-lookup"><span data-stu-id="08d85-132">Example 3</span></span>

<span data-ttu-id="08d85-133">FORMAT(DATE(1999,10,14),"C")</span><span class="sxs-lookup"><span data-stu-id="08d85-133">FORMAT(DATE(1999,10,14),"C")</span></span>
  
<span data-ttu-id="08d85-134">Возвращает значение, представляющее вторник, 14 октября 1999 г.</span><span class="sxs-lookup"><span data-stu-id="08d85-134">Returns the value representing Tuesday, October 14, 1999.</span></span>
  

