---
title: Функция DatePart (пользовательское веб-приложение Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8936f0b6-f9b2-44ef-bf90-e482b64611cd
description: Возвращает числовом значении, которое представляет указанную часть даты указанной даты.
ms.openlocfilehash: 31ac6423614afd61ed943bb7ba375f14696df1ea
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411437"
---
# <a name="datepart-function-access-custom-web-app"></a><span data-ttu-id="96c67-103">Функция DatePart (пользовательское веб-приложение Access)</span><span class="sxs-lookup"><span data-stu-id="96c67-103">DatePart function (Access custom web app)</span></span>

<span data-ttu-id="96c67-104">Возвращает числовом значении, которое представляет указанную часть даты указанной даты.</span><span class="sxs-lookup"><span data-stu-id="96c67-104">Returns a numeric value that represents the specified date part of the specified date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="96c67-105">Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="96c67-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="96c67-106">Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="96c67-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="96c67-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96c67-107">Syntax</span></span>

<span data-ttu-id="96c67-108">**DatePart** (*DatePart*, *Date*)</span><span class="sxs-lookup"><span data-stu-id="96c67-108">**DatePart** (*DatePart*, *Date*)</span></span> 
  
<span data-ttu-id="96c67-109">Функция **DatePart** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="96c67-109">The **DatePart** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="96c67-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="96c67-110">**Argument name**</span></span>|<span data-ttu-id="96c67-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="96c67-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="96c67-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="96c67-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="96c67-113">Часть  *даты*  (значения даты или времени), для которой будет возвращено значение.</span><span class="sxs-lookup"><span data-stu-id="96c67-113">The part of  *Date*  (a date or time value) for which an integer will be returned.</span></span> <span data-ttu-id="96c67-114">Список допустимой аббревиатуры можно найти в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="96c67-114">Refer to the Remarks section for the list of valid abbreviations.</span></span>  <br/> |
| <span data-ttu-id="96c67-115">*Дата*</span><span class="sxs-lookup"><span data-stu-id="96c67-115">*Date*</span></span>  <br/> |<span data-ttu-id="96c67-116">Выражение, которое можно разрешить в значение даты и времени.</span><span class="sxs-lookup"><span data-stu-id="96c67-116">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="96c67-117">Выражение  *аргумента Date,*  выражение столбца, определяемая пользователем переменная или строковый литерал.</span><span class="sxs-lookup"><span data-stu-id="96c67-117">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96c67-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="96c67-118">Remarks</span></span>

<span data-ttu-id="96c67-119">В следующей таблице перечислены все допустимые *аргументы DatePart.*</span><span class="sxs-lookup"><span data-stu-id="96c67-119">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="96c67-120">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="96c67-120">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="96c67-121">**year**</span><span class="sxs-lookup"><span data-stu-id="96c67-121">**year**</span></span> <br/> |
|<span data-ttu-id="96c67-122">**quarter**</span><span class="sxs-lookup"><span data-stu-id="96c67-122">**quarter**</span></span> <br/> |
|<span data-ttu-id="96c67-123">**month**</span><span class="sxs-lookup"><span data-stu-id="96c67-123">**month**</span></span> <br/> |
|<span data-ttu-id="96c67-124">**dayofyear**</span><span class="sxs-lookup"><span data-stu-id="96c67-124">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="96c67-125">**day**</span><span class="sxs-lookup"><span data-stu-id="96c67-125">**day**</span></span> <br/> |
|<span data-ttu-id="96c67-126">**week**</span><span class="sxs-lookup"><span data-stu-id="96c67-126">**week**</span></span> <br/> |
|<span data-ttu-id="96c67-127">**weekday**</span><span class="sxs-lookup"><span data-stu-id="96c67-127">**weekday**</span></span> <br/> |
|<span data-ttu-id="96c67-128">**hour**</span><span class="sxs-lookup"><span data-stu-id="96c67-128">**hour**</span></span> <br/> |
|<span data-ttu-id="96c67-129">**minute**</span><span class="sxs-lookup"><span data-stu-id="96c67-129">**minute**</span></span> <br/> |
|<span data-ttu-id="96c67-130">**second**</span><span class="sxs-lookup"><span data-stu-id="96c67-130">**second**</span></span> <br/> |
|<span data-ttu-id="96c67-131">**миллисекунд**</span><span class="sxs-lookup"><span data-stu-id="96c67-131">**millisecond**</span></span> <br/> |
   

