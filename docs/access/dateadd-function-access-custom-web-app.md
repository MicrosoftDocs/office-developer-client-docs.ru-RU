---
title: Функция DateAdd (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7174c585-86e1-42a3-bb7f-d6641001b0f2
description: Возвращает указанной даты с заданным интервалом номеров (целое положительное или отрицательное) добавлена части этой даты с указанной даты.
ms.openlocfilehash: a2baa58a2ccab7d030750d03d4fddb84e8eb8ff7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806971"
---
# <a name="dateadd-function-access-custom-web-app"></a><span data-ttu-id="c6542-103">Функция DateAdd (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="c6542-103">DateAdd function (Access custom web app)</span></span>

<span data-ttu-id="c6542-104">Возвращает указанной даты с заданным интервалом номеров (целое положительное или отрицательное) добавлена части этой даты с указанной даты.</span><span class="sxs-lookup"><span data-stu-id="c6542-104">Returns a specified date with the specified number interval (positive or negative integer) added to a specified date part of that date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c6542-105">Компонент хранилища облаке, описанных в этой статье в Office 2013 и Office 2016 больше не поддерживается и может привести следующее сообщение об ошибке: > *к сожалению, мы возникают проблемы с сервера, поэтому мы не удается добавить \<службы\> на данный момент. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="c6542-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="c6542-106">> Для облачного хранилища для Microsoft Office Online, Office для операций ввода-вывода и Office для Android можно найти в нашем [Партнерской программы Office облачных хранилища](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="c6542-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c6542-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6542-107">Syntax</span></span>

<span data-ttu-id="c6542-108">**Функция DateAdd** (*DatePart*, *номер*, *Дата*)</span><span class="sxs-lookup"><span data-stu-id="c6542-108">**DateAdd** (*DatePart*, *Number*, *Date*)</span></span> 
  
<span data-ttu-id="c6542-109">Функция **DateAdd** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="c6542-109">The **DateAdd** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="c6542-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="c6542-110">**Argument name**</span></span>|<span data-ttu-id="c6542-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c6542-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c6542-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="c6542-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="c6542-113">Часть *даты* , к которому добавляется целое число.</span><span class="sxs-lookup"><span data-stu-id="c6542-113">The part of  *Date*  to which an integer number is added.</span></span> <span data-ttu-id="c6542-114">Обратитесь к "Примечания" для списка допустимых значений.</span><span class="sxs-lookup"><span data-stu-id="c6542-114">Refer to the Remarks section for the list of valid settings.</span></span>  <br/> |
| <span data-ttu-id="c6542-115">*Число*</span><span class="sxs-lookup"><span data-stu-id="c6542-115">*Number*</span></span>  <br/> |<span data-ttu-id="c6542-116">— Это выражение, которое можно разрешить в целое число, добавляется в *указанной* *даты* .</span><span class="sxs-lookup"><span data-stu-id="c6542-116">Is an expression that can be resolved to an integer that is added to a  *DatePart*  of  *Date*  .</span></span> <span data-ttu-id="c6542-117">Если значение задано с помощью дробной, усекается дроби.</span><span class="sxs-lookup"><span data-stu-id="c6542-117">If you specify a value with a decimal fraction, the fraction is truncated.</span></span>  <br/> |
| <span data-ttu-id="c6542-118">*Дата*</span><span class="sxs-lookup"><span data-stu-id="c6542-118">*Date*</span></span>  <br/> |<span data-ttu-id="c6542-119">Выражение, которое разрешается в значение даты и времени.</span><span class="sxs-lookup"><span data-stu-id="c6542-119">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="c6542-120">Аргумент выражение *даты* , выражение столбца, переменной, определенной пользователем или строковый литерал.</span><span class="sxs-lookup"><span data-stu-id="c6542-120">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6542-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="c6542-121">Remarks</span></span>

<span data-ttu-id="c6542-122">В следующей таблице перечислены все допустимые аргументы *DatePart* .</span><span class="sxs-lookup"><span data-stu-id="c6542-122">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="c6542-123">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="c6542-123">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="c6542-124">**year**</span><span class="sxs-lookup"><span data-stu-id="c6542-124">**year**</span></span> <br/> |
|<span data-ttu-id="c6542-125">**квартал**</span><span class="sxs-lookup"><span data-stu-id="c6542-125">**quarter**</span></span> <br/> |
|<span data-ttu-id="c6542-126">**month**</span><span class="sxs-lookup"><span data-stu-id="c6542-126">**month**</span></span> <br/> |
|<span data-ttu-id="c6542-127">**DayOfYear**</span><span class="sxs-lookup"><span data-stu-id="c6542-127">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="c6542-128">**день**</span><span class="sxs-lookup"><span data-stu-id="c6542-128">**day**</span></span> <br/> |
|<span data-ttu-id="c6542-129">**недели**</span><span class="sxs-lookup"><span data-stu-id="c6542-129">**week**</span></span> <br/> |
|<span data-ttu-id="c6542-130">**час**</span><span class="sxs-lookup"><span data-stu-id="c6542-130">**hour**</span></span> <br/> |
|<span data-ttu-id="c6542-131">**минуты**</span><span class="sxs-lookup"><span data-stu-id="c6542-131">**minute**</span></span> <br/> |
|<span data-ttu-id="c6542-132">**секунды**</span><span class="sxs-lookup"><span data-stu-id="c6542-132">**second**</span></span> <br/> |
|<span data-ttu-id="c6542-133">**мс**</span><span class="sxs-lookup"><span data-stu-id="c6542-133">**millisecond**</span></span> <br/> |
   
## <a name="example"></a><span data-ttu-id="c6542-134">Пример</span><span class="sxs-lookup"><span data-stu-id="c6542-134">Example</span></span>

<span data-ttu-id="c6542-135">Следующее выражение вычисляет последний день текущего месяца.</span><span class="sxs-lookup"><span data-stu-id="c6542-135">The following expression calculates the last day of the current month.</span></span>
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today())+1,0))`

<span data-ttu-id="c6542-136">Следующее выражение вычисляет последний день предыдущего месяца.</span><span class="sxs-lookup"><span data-stu-id="c6542-136">The following expression calculates the last day of the previous month.</span></span>
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today()),0))`


