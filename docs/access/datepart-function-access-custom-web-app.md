---
title: Функция DatePart (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8936f0b6-f9b2-44ef-bf90-e482b64611cd
description: Возвращает числовое значение, которое представляет собой часть указанной даты указанной даты.
ms.openlocfilehash: 81aa1880e5b38c33f75018418a44ed82e5e7e8c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806927"
---
# <a name="datepart-function-access-custom-web-app"></a><span data-ttu-id="fb0b6-103">Функция DatePart (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="fb0b6-103">DatePart function (Access custom web app)</span></span>

<span data-ttu-id="fb0b6-104">Возвращает числовое значение, которое представляет собой часть указанной даты указанной даты.</span><span class="sxs-lookup"><span data-stu-id="fb0b6-104">Returns a numeric value that represents the specified date part of the specified date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fb0b6-105">Компонент хранилища облаке, описанных в этой статье в Office 2013 и Office 2016 больше не поддерживается и может привести следующее сообщение об ошибке: > *к сожалению, мы возникают проблемы с сервера, поэтому мы не удается добавить \<службы\> на данный момент. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="fb0b6-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="fb0b6-106">> Для облачного хранилища для Microsoft Office Online, Office для операций ввода-вывода и Office для Android можно найти в нашем [Партнерской программы Office облачных хранилища](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="fb0b6-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fb0b6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb0b6-107">Syntax</span></span>

<span data-ttu-id="fb0b6-108">**DatePart** (*DatePart*, *Дата*)</span><span class="sxs-lookup"><span data-stu-id="fb0b6-108">**DatePart** (*DatePart*, *Date*)</span></span> 
  
<span data-ttu-id="fb0b6-109">Функция **DatePart** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="fb0b6-109">The **DatePart** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="fb0b6-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="fb0b6-110">**Argument name**</span></span>|<span data-ttu-id="fb0b6-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fb0b6-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="fb0b6-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="fb0b6-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="fb0b6-113">Часть *даты* (значение даты или времени) для которого будет возвращено целое число.</span><span class="sxs-lookup"><span data-stu-id="fb0b6-113">The part of  *Date*  (a date or time value) for which an integer will be returned.</span></span> <span data-ttu-id="fb0b6-114">Обратитесь к "Примечания" для списка допустимые значения.</span><span class="sxs-lookup"><span data-stu-id="fb0b6-114">Refer to the Remarks section for the list of valid abbreviations.</span></span>  <br/> |
| <span data-ttu-id="fb0b6-115">*Дата*</span><span class="sxs-lookup"><span data-stu-id="fb0b6-115">*Date*</span></span>  <br/> |<span data-ttu-id="fb0b6-116">Выражение, которое разрешается в значение даты и времени.</span><span class="sxs-lookup"><span data-stu-id="fb0b6-116">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="fb0b6-117">Аргумент выражение *даты* , выражение столбца, переменной, определенной пользователем или строковый литерал.</span><span class="sxs-lookup"><span data-stu-id="fb0b6-117">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fb0b6-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="fb0b6-118">Remarks</span></span>

<span data-ttu-id="fb0b6-119">В следующей таблице перечислены все допустимые аргументы *DatePart* .</span><span class="sxs-lookup"><span data-stu-id="fb0b6-119">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="fb0b6-120">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="fb0b6-120">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="fb0b6-121">**year**</span><span class="sxs-lookup"><span data-stu-id="fb0b6-121">**year**</span></span> <br/> |
|<span data-ttu-id="fb0b6-122">**квартал**</span><span class="sxs-lookup"><span data-stu-id="fb0b6-122">**quarter**</span></span> <br/> |
|<span data-ttu-id="fb0b6-123">**month**</span><span class="sxs-lookup"><span data-stu-id="fb0b6-123">**month**</span></span> <br/> |
|<span data-ttu-id="fb0b6-124">**DayOfYear**</span><span class="sxs-lookup"><span data-stu-id="fb0b6-124">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="fb0b6-125">**день**</span><span class="sxs-lookup"><span data-stu-id="fb0b6-125">**day**</span></span> <br/> |
|<span data-ttu-id="fb0b6-126">**недели**</span><span class="sxs-lookup"><span data-stu-id="fb0b6-126">**week**</span></span> <br/> |
|<span data-ttu-id="fb0b6-127">**день недели**</span><span class="sxs-lookup"><span data-stu-id="fb0b6-127">**weekday**</span></span> <br/> |
|<span data-ttu-id="fb0b6-128">**час**</span><span class="sxs-lookup"><span data-stu-id="fb0b6-128">**hour**</span></span> <br/> |
|<span data-ttu-id="fb0b6-129">**минуты**</span><span class="sxs-lookup"><span data-stu-id="fb0b6-129">**minute**</span></span> <br/> |
|<span data-ttu-id="fb0b6-130">**секунды**</span><span class="sxs-lookup"><span data-stu-id="fb0b6-130">**second**</span></span> <br/> |
|<span data-ttu-id="fb0b6-131">**мс**</span><span class="sxs-lookup"><span data-stu-id="fb0b6-131">**millisecond**</span></span> <br/> |
   

