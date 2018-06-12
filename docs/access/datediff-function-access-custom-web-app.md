---
title: Функция DateDiff (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1c58ee87-0f57-4643-be4d-62da815df705
description: Возвращает количество границ часть определенной даты, пересекающихся указанную начальную и конечную даты.
ms.openlocfilehash: fe898ec5eb59cb341250cb0c0e2e35bc55d37eb3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806969"
---
# <a name="datediff-function-access-custom-web-app"></a><span data-ttu-id="85984-103">Функция DateDiff (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="85984-103">DateDiff function (Access custom web app)</span></span>

<span data-ttu-id="85984-104">Возвращает количество границ часть определенной даты, пересекающихся указанную начальную и конечную даты.</span><span class="sxs-lookup"><span data-stu-id="85984-104">Returns the count of the specified date part boundaries crossed between the specified start date and end date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="85984-105">Компонент хранилища облаке, описанных в этой статье в Office 2013 и Office 2016 больше не поддерживается и может привести следующее сообщение об ошибке: > *к сожалению, мы возникают проблемы с сервера, поэтому мы не удается добавить \<службы\> на данный момент. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="85984-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="85984-106">> Для облачного хранилища для Microsoft Office Online, Office для операций ввода-вывода и Office для Android можно найти в нашем [Партнерской программы Office облачных хранилища](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="85984-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="85984-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85984-107">Syntax</span></span>

<span data-ttu-id="85984-108">**Функция DateDiff** (*DatePart*, *Дата начала*, *Дата окончания*)</span><span class="sxs-lookup"><span data-stu-id="85984-108">**DateDiff** (*DatePart*, *StartDate*, *EndDate*)</span></span> 
  
<span data-ttu-id="85984-109">Функция **DateDiff** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="85984-109">The **DateDiff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="85984-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="85984-110">**Argument name**</span></span>|<span data-ttu-id="85984-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="85984-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="85984-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="85984-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="85984-113">Является частью *StartDate* и *EndDate* , которое указывает тип границы пересечение.</span><span class="sxs-lookup"><span data-stu-id="85984-113">Is the part of  *StartDate*  and  *EndDate*  that specifies the type of boundary crossed.</span></span> <span data-ttu-id="85984-114">Обратитесь к "Примечания" для списка допустимых значений.</span><span class="sxs-lookup"><span data-stu-id="85984-114">Refer to the Remarks section for the list of valid settings.</span></span>  <br/> |
| <span data-ttu-id="85984-115">*Дата начала*</span><span class="sxs-lookup"><span data-stu-id="85984-115">*StartDate*</span></span>  <br/> |<span data-ttu-id="85984-116">Выражение, которое разрешается в значение даты и времени.</span><span class="sxs-lookup"><span data-stu-id="85984-116">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="85984-117">Аргумент выражение *даты* , выражение столбца, переменной, определенной пользователем или строковый литерал.</span><span class="sxs-lookup"><span data-stu-id="85984-117">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
| <span data-ttu-id="85984-118">*Дата окончания*</span><span class="sxs-lookup"><span data-stu-id="85984-118">*EndDate*</span></span>  <br/> |<span data-ttu-id="85984-119">Выражение, которое разрешается в значение даты и времени.</span><span class="sxs-lookup"><span data-stu-id="85984-119">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="85984-120">Аргумент выражение *даты* , выражение столбца, переменной, определенной пользователем или строковый литерал.</span><span class="sxs-lookup"><span data-stu-id="85984-120">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85984-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="85984-121">Remarks</span></span>

<span data-ttu-id="85984-122">В следующей таблице перечислены все допустимые аргументы *DatePart* .</span><span class="sxs-lookup"><span data-stu-id="85984-122">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="85984-123">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="85984-123">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="85984-124">**year**</span><span class="sxs-lookup"><span data-stu-id="85984-124">**year**</span></span> <br/> |
|<span data-ttu-id="85984-125">**квартал**</span><span class="sxs-lookup"><span data-stu-id="85984-125">**quarter**</span></span> <br/> |
|<span data-ttu-id="85984-126">**month**</span><span class="sxs-lookup"><span data-stu-id="85984-126">**month**</span></span> <br/> |
|<span data-ttu-id="85984-127">**DayOfYear**</span><span class="sxs-lookup"><span data-stu-id="85984-127">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="85984-128">**день**</span><span class="sxs-lookup"><span data-stu-id="85984-128">**day**</span></span> <br/> |
|<span data-ttu-id="85984-129">**недели**</span><span class="sxs-lookup"><span data-stu-id="85984-129">**week**</span></span> <br/> |
|<span data-ttu-id="85984-130">**час**</span><span class="sxs-lookup"><span data-stu-id="85984-130">**hour**</span></span> <br/> |
|<span data-ttu-id="85984-131">**минуты**</span><span class="sxs-lookup"><span data-stu-id="85984-131">**minute**</span></span> <br/> |
|<span data-ttu-id="85984-132">**секунды**</span><span class="sxs-lookup"><span data-stu-id="85984-132">**second**</span></span> <br/> |
|<span data-ttu-id="85984-133">**мс**</span><span class="sxs-lookup"><span data-stu-id="85984-133">**millisecond**</span></span> <br/> |
   

