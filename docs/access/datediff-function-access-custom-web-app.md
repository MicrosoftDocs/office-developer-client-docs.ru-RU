---
title: Функция DateDiff (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1c58ee87-0f57-4643-be4d-62da815df705
description: Возвращает количество заданных границ части даты, пересеченных с указанной датой начала и датой окончания.
ms.openlocfilehash: 1cce8a501c5a57384372e681f903baa4f4c20bef
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415616"
---
# <a name="datediff-function-access-custom-web-app"></a><span data-ttu-id="3cb5c-103">Функция DateDiff (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="3cb5c-103">DateDiff function (Access custom web app)</span></span>

<span data-ttu-id="3cb5c-104">Возвращает количество заданных границ части даты, пересеченных с указанной датой начала и датой окончания.</span><span class="sxs-lookup"><span data-stu-id="3cb5c-104">Returns the count of the specified date part boundaries crossed between the specified start date and end date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3cb5c-105">Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="3cb5c-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="3cb5c-106">Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="3cb5c-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3cb5c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3cb5c-107">Syntax</span></span>

<span data-ttu-id="3cb5c-108">**DateDiff** (*DatePart*, *StartDate*, *EndDate*)</span><span class="sxs-lookup"><span data-stu-id="3cb5c-108">**DateDiff** (*DatePart*, *StartDate*, *EndDate*)</span></span> 
  
<span data-ttu-id="3cb5c-109">Функция **DateDiff** содержит следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="3cb5c-109">The **DateDiff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="3cb5c-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="3cb5c-110">**Argument name**</span></span>|<span data-ttu-id="3cb5c-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3cb5c-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3cb5c-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="3cb5c-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="3cb5c-113">— Это часть *StartDate* и *EndDate* , указывающая тип перекрестной границы.</span><span class="sxs-lookup"><span data-stu-id="3cb5c-113">Is the part of  *StartDate*  and  *EndDate*  that specifies the type of boundary crossed.</span></span> <span data-ttu-id="3cb5c-114">Список допустимых параметров можно найти в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="3cb5c-114">Refer to the Remarks section for the list of valid settings.</span></span>  <br/> |
| <span data-ttu-id="3cb5c-115">*StartDate*</span><span class="sxs-lookup"><span data-stu-id="3cb5c-115">*StartDate*</span></span>  <br/> |<span data-ttu-id="3cb5c-116">Выражение, которое может быть разрешено в значение даты и времени.</span><span class="sxs-lookup"><span data-stu-id="3cb5c-116">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="3cb5c-117">Выражение аргумента *Date* , выражение столбца, определяемая пользователем переменная или строковый литерал.</span><span class="sxs-lookup"><span data-stu-id="3cb5c-117">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
| <span data-ttu-id="3cb5c-118">*EndDate*</span><span class="sxs-lookup"><span data-stu-id="3cb5c-118">*EndDate*</span></span>  <br/> |<span data-ttu-id="3cb5c-119">Выражение, которое может быть разрешено в значение даты и времени.</span><span class="sxs-lookup"><span data-stu-id="3cb5c-119">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="3cb5c-120">Выражение аргумента *Date* , выражение столбца, определяемая пользователем переменная или строковый литерал.</span><span class="sxs-lookup"><span data-stu-id="3cb5c-120">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3cb5c-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="3cb5c-121">Remarks</span></span>

<span data-ttu-id="3cb5c-122">В следующей таблице перечислены все допустимые аргументы *DatePart* .</span><span class="sxs-lookup"><span data-stu-id="3cb5c-122">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="3cb5c-123">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="3cb5c-123">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="3cb5c-124">**year**</span><span class="sxs-lookup"><span data-stu-id="3cb5c-124">**year**</span></span> <br/> |
|<span data-ttu-id="3cb5c-125">**квартале**</span><span class="sxs-lookup"><span data-stu-id="3cb5c-125">**quarter**</span></span> <br/> |
|<span data-ttu-id="3cb5c-126">**month**</span><span class="sxs-lookup"><span data-stu-id="3cb5c-126">**month**</span></span> <br/> |
|<span data-ttu-id="3cb5c-127">**DayOfYear**</span><span class="sxs-lookup"><span data-stu-id="3cb5c-127">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="3cb5c-128">**открыт**</span><span class="sxs-lookup"><span data-stu-id="3cb5c-128">**day**</span></span> <br/> |
|<span data-ttu-id="3cb5c-129">**я**</span><span class="sxs-lookup"><span data-stu-id="3cb5c-129">**week**</span></span> <br/> |
|<span data-ttu-id="3cb5c-130">**час**</span><span class="sxs-lookup"><span data-stu-id="3cb5c-130">**hour**</span></span> <br/> |
|<span data-ttu-id="3cb5c-131">**за**</span><span class="sxs-lookup"><span data-stu-id="3cb5c-131">**minute**</span></span> <br/> |
|<span data-ttu-id="3cb5c-132">**Втор**</span><span class="sxs-lookup"><span data-stu-id="3cb5c-132">**second**</span></span> <br/> |
|<span data-ttu-id="3cb5c-133">**до**</span><span class="sxs-lookup"><span data-stu-id="3cb5c-133">**millisecond**</span></span> <br/> |
   

