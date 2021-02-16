---
title: Функция DateAdd (пользовательское веб-приложение Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7174c585-86e1-42a3-bb7f-d6641001b0f2
description: Возвращает указанную дату с указанным интервалом номера (положительным или отрицательным числом), добавленным к указанной части даты.
ms.openlocfilehash: 7cfd68c4983eee22a5e542facd72ea083deb3184
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423204"
---
# <a name="dateadd-function-access-custom-web-app"></a><span data-ttu-id="603b1-103">Функция DateAdd (пользовательское веб-приложение Access)</span><span class="sxs-lookup"><span data-stu-id="603b1-103">DateAdd function (Access custom web app)</span></span>

<span data-ttu-id="603b1-104">Возвращает указанную дату с указанным интервалом номера (положительным или отрицательным числом), добавленным к указанной части даты.</span><span class="sxs-lookup"><span data-stu-id="603b1-104">Returns a specified date with the specified number interval (positive or negative integer) added to a specified date part of that date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="603b1-105">Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="603b1-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="603b1-106">Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="603b1-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="603b1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="603b1-107">Syntax</span></span>

<span data-ttu-id="603b1-108">**DateAdd** (*DatePart*, *Number*, *Date*)</span><span class="sxs-lookup"><span data-stu-id="603b1-108">**DateAdd** (*DatePart*, *Number*, *Date*)</span></span> 
  
<span data-ttu-id="603b1-109">Функция **DateAdd** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="603b1-109">The **DateAdd** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="603b1-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="603b1-110">**Argument name**</span></span>|<span data-ttu-id="603b1-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="603b1-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="603b1-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="603b1-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="603b1-113">Часть  *даты,*  к которой добавляется целый номер.</span><span class="sxs-lookup"><span data-stu-id="603b1-113">The part of  *Date*  to which an integer number is added.</span></span> <span data-ttu-id="603b1-114">Список допустимого параметра можно найти в разделе "Примечаний".</span><span class="sxs-lookup"><span data-stu-id="603b1-114">Refer to the Remarks section for the list of valid settings.</span></span>  <br/> |
| <span data-ttu-id="603b1-115">*Number*</span><span class="sxs-lookup"><span data-stu-id="603b1-115">*Number*</span></span>  <br/> |<span data-ttu-id="603b1-116">Это выражение, которое может быть разрешено в integer, которое добавляется в  *DatePart*  *даты*  .</span><span class="sxs-lookup"><span data-stu-id="603b1-116">Is an expression that can be resolved to an integer that is added to a  *DatePart*  of  *Date*  .</span></span> <span data-ttu-id="603b1-117">Если указать значение с дробной дробью, дробь усечена.</span><span class="sxs-lookup"><span data-stu-id="603b1-117">If you specify a value with a decimal fraction, the fraction is truncated.</span></span>  <br/> |
| <span data-ttu-id="603b1-118">*Дата*</span><span class="sxs-lookup"><span data-stu-id="603b1-118">*Date*</span></span>  <br/> |<span data-ttu-id="603b1-119">Выражение, которое можно разрешить в значение даты и времени.</span><span class="sxs-lookup"><span data-stu-id="603b1-119">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="603b1-120">Выражение  *аргумента Date,*  выражение столбца, определяемая пользователем переменная или строковый литерал.</span><span class="sxs-lookup"><span data-stu-id="603b1-120">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="603b1-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="603b1-121">Remarks</span></span>

<span data-ttu-id="603b1-122">В следующей таблице перечислены все допустимые *аргументы DatePart.*</span><span class="sxs-lookup"><span data-stu-id="603b1-122">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="603b1-123">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="603b1-123">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="603b1-124">**year**</span><span class="sxs-lookup"><span data-stu-id="603b1-124">**year**</span></span> <br/> |
|<span data-ttu-id="603b1-125">**quarter**</span><span class="sxs-lookup"><span data-stu-id="603b1-125">**quarter**</span></span> <br/> |
|<span data-ttu-id="603b1-126">**month**</span><span class="sxs-lookup"><span data-stu-id="603b1-126">**month**</span></span> <br/> |
|<span data-ttu-id="603b1-127">**dayofyear**</span><span class="sxs-lookup"><span data-stu-id="603b1-127">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="603b1-128">**day**</span><span class="sxs-lookup"><span data-stu-id="603b1-128">**day**</span></span> <br/> |
|<span data-ttu-id="603b1-129">**week**</span><span class="sxs-lookup"><span data-stu-id="603b1-129">**week**</span></span> <br/> |
|<span data-ttu-id="603b1-130">**hour**</span><span class="sxs-lookup"><span data-stu-id="603b1-130">**hour**</span></span> <br/> |
|<span data-ttu-id="603b1-131">**minute**</span><span class="sxs-lookup"><span data-stu-id="603b1-131">**minute**</span></span> <br/> |
|<span data-ttu-id="603b1-132">**second**</span><span class="sxs-lookup"><span data-stu-id="603b1-132">**second**</span></span> <br/> |
|<span data-ttu-id="603b1-133">**миллисекунд**</span><span class="sxs-lookup"><span data-stu-id="603b1-133">**millisecond**</span></span> <br/> |
   
## <a name="example"></a><span data-ttu-id="603b1-134">Пример</span><span class="sxs-lookup"><span data-stu-id="603b1-134">Example</span></span>

<span data-ttu-id="603b1-135">Следующее выражение вычисляет последний день текущего месяца.</span><span class="sxs-lookup"><span data-stu-id="603b1-135">The following expression calculates the last day of the current month.</span></span>
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today())+1,0))`

<span data-ttu-id="603b1-136">Следующее выражение вычисляет последний день предыдущего месяца.</span><span class="sxs-lookup"><span data-stu-id="603b1-136">The following expression calculates the last day of the previous month.</span></span>
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today()),0))`


