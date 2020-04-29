---
title: Функция DateAdd (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7174c585-86e1-42a3-bb7f-d6641001b0f2
description: Возвращает указанную дату с указанным интервалом (положительное или отрицательное целое число), добавленной к указанной части даты.
ms.openlocfilehash: 7cfd68c4983eee22a5e542facd72ea083deb3184
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423204"
---
# <a name="dateadd-function-access-custom-web-app"></a><span data-ttu-id="27854-103">Функция DateAdd (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="27854-103">DateAdd function (Access custom web app)</span></span>

<span data-ttu-id="27854-104">Возвращает указанную дату с указанным интервалом (положительное или отрицательное целое число), добавленной к указанной части даты.</span><span class="sxs-lookup"><span data-stu-id="27854-104">Returns a specified date with the specified number interval (positive or negative integer) added to a specified date part of that date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="27854-105">Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="27854-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="27854-106">Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="27854-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="27854-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27854-107">Syntax</span></span>

<span data-ttu-id="27854-108">**DateAdd** (*DatePart*, *Number*, *Date*)</span><span class="sxs-lookup"><span data-stu-id="27854-108">**DateAdd** (*DatePart*, *Number*, *Date*)</span></span> 
  
<span data-ttu-id="27854-109">Функция **DateAdd** содержит следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="27854-109">The **DateAdd** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="27854-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="27854-110">**Argument name**</span></span>|<span data-ttu-id="27854-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="27854-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="27854-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="27854-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="27854-113">Часть *даты* , в которую добавляется целое число.</span><span class="sxs-lookup"><span data-stu-id="27854-113">The part of  *Date*  to which an integer number is added.</span></span> <span data-ttu-id="27854-114">Список допустимых параметров можно найти в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="27854-114">Refer to the Remarks section for the list of valid settings.</span></span>  <br/> |
| <span data-ttu-id="27854-115">*Number*</span><span class="sxs-lookup"><span data-stu-id="27854-115">*Number*</span></span>  <br/> |<span data-ttu-id="27854-116">— Это выражение, которое можно сопоставить с *целым числом* , добавляемым к части *даты* .</span><span class="sxs-lookup"><span data-stu-id="27854-116">Is an expression that can be resolved to an integer that is added to a  *DatePart*  of  *Date*  .</span></span> <span data-ttu-id="27854-117">Если указать значение с десятичной дробью, дробная часть усекается.</span><span class="sxs-lookup"><span data-stu-id="27854-117">If you specify a value with a decimal fraction, the fraction is truncated.</span></span>  <br/> |
| <span data-ttu-id="27854-118">*Date*</span><span class="sxs-lookup"><span data-stu-id="27854-118">*Date*</span></span>  <br/> |<span data-ttu-id="27854-119">Выражение, которое может быть разрешено в значение даты и времени.</span><span class="sxs-lookup"><span data-stu-id="27854-119">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="27854-120">Выражение аргумента *Date* , выражение столбца, определяемая пользователем переменная или строковый литерал.</span><span class="sxs-lookup"><span data-stu-id="27854-120">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27854-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="27854-121">Remarks</span></span>

<span data-ttu-id="27854-122">В следующей таблице перечислены все допустимые аргументы *DatePart* .</span><span class="sxs-lookup"><span data-stu-id="27854-122">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="27854-123">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="27854-123">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="27854-124">**year**</span><span class="sxs-lookup"><span data-stu-id="27854-124">**year**</span></span> <br/> |
|<span data-ttu-id="27854-125">**квартале**</span><span class="sxs-lookup"><span data-stu-id="27854-125">**quarter**</span></span> <br/> |
|<span data-ttu-id="27854-126">**month**</span><span class="sxs-lookup"><span data-stu-id="27854-126">**month**</span></span> <br/> |
|<span data-ttu-id="27854-127">**DayOfYear**</span><span class="sxs-lookup"><span data-stu-id="27854-127">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="27854-128">**открыт**</span><span class="sxs-lookup"><span data-stu-id="27854-128">**day**</span></span> <br/> |
|<span data-ttu-id="27854-129">**я**</span><span class="sxs-lookup"><span data-stu-id="27854-129">**week**</span></span> <br/> |
|<span data-ttu-id="27854-130">**час**</span><span class="sxs-lookup"><span data-stu-id="27854-130">**hour**</span></span> <br/> |
|<span data-ttu-id="27854-131">**за**</span><span class="sxs-lookup"><span data-stu-id="27854-131">**minute**</span></span> <br/> |
|<span data-ttu-id="27854-132">**Втор**</span><span class="sxs-lookup"><span data-stu-id="27854-132">**second**</span></span> <br/> |
|<span data-ttu-id="27854-133">**до**</span><span class="sxs-lookup"><span data-stu-id="27854-133">**millisecond**</span></span> <br/> |
   
## <a name="example"></a><span data-ttu-id="27854-134">Пример</span><span class="sxs-lookup"><span data-stu-id="27854-134">Example</span></span>

<span data-ttu-id="27854-135">Следующее выражение вычисляет последний день текущего месяца.</span><span class="sxs-lookup"><span data-stu-id="27854-135">The following expression calculates the last day of the current month.</span></span>
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today())+1,0))`

<span data-ttu-id="27854-136">Следующее выражение вычисляет последний день предыдущего месяца.</span><span class="sxs-lookup"><span data-stu-id="27854-136">The following expression calculates the last day of the previous month.</span></span>
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today()),0))`


