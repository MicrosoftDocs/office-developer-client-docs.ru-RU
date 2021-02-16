---
title: Функция DateWithTimeFromParts (пользовательское веб-приложение Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: Возвращает дату и время на основе указанного года, месяца, дня и времени.
ms.openlocfilehash: ee995d346ca27e683f342cf3f611c1147997d24e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422091"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a><span data-ttu-id="8e46f-103">Функция DateWithTimeFromParts (пользовательское веб-приложение Access)</span><span class="sxs-lookup"><span data-stu-id="8e46f-103">DateWithTimeFromParts function (Access custom web app)</span></span>

<span data-ttu-id="8e46f-104">Возвращает дату и время на основе указанного года, месяца, дня и времени.</span><span class="sxs-lookup"><span data-stu-id="8e46f-104">Returns a Date and Time based on a specified year, month, day, and time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8e46f-105">Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="8e46f-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="8e46f-106">Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="8e46f-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8e46f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e46f-107">Syntax</span></span>

<span data-ttu-id="8e46f-108">**DateWithTimeFromParts** (*Year,* *Month,* *Day*, *Hour*, *Minute*, *Second*)</span><span class="sxs-lookup"><span data-stu-id="8e46f-108">**DateWithTimeFromParts** (*Year*, *Month*, *Day*, *Hour*, *Minute*, *Second*)</span></span> 
  
<span data-ttu-id="8e46f-109">Функция **DateWithTimeFromParts** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="8e46f-109">The **DateWithTimeFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="8e46f-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="8e46f-110">**Argument name**</span></span>|<span data-ttu-id="8e46f-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8e46f-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="8e46f-112">*Год*</span><span class="sxs-lookup"><span data-stu-id="8e46f-112">*Year*</span></span>  <br/> |<span data-ttu-id="8e46f-113">Integer expression specifying a year.</span><span class="sxs-lookup"><span data-stu-id="8e46f-113">Integer expression specifying a year.</span></span>  <br/> |
| <span data-ttu-id="8e46f-114">*Month*</span><span class="sxs-lookup"><span data-stu-id="8e46f-114">*Month*</span></span>  <br/> |<span data-ttu-id="8e46f-115">Integer expression specifying a month.</span><span class="sxs-lookup"><span data-stu-id="8e46f-115">Integer expression specifying a month.</span></span>  <br/> |
| <span data-ttu-id="8e46f-116">*Day*</span><span class="sxs-lookup"><span data-stu-id="8e46f-116">*Day*</span></span>  <br/> |<span data-ttu-id="8e46f-117">Integer expression specifying a day.</span><span class="sxs-lookup"><span data-stu-id="8e46f-117">Integer expression specifying a day.</span></span>  <br/> |
| <span data-ttu-id="8e46f-118">*Hour*</span><span class="sxs-lookup"><span data-stu-id="8e46f-118">*Hour*</span></span>  <br/> |<span data-ttu-id="8e46f-119">Integer expression specifying hours.</span><span class="sxs-lookup"><span data-stu-id="8e46f-119">Integer expression specifying hours.</span></span>  <br/> |
| <span data-ttu-id="8e46f-120">*Minute*</span><span class="sxs-lookup"><span data-stu-id="8e46f-120">*Minute*</span></span>  <br/> |<span data-ttu-id="8e46f-121">Integer expression specifying minutes.</span><span class="sxs-lookup"><span data-stu-id="8e46f-121">Integer expression specifying minutes.</span></span>  <br/> |
| <span data-ttu-id="8e46f-122">*Second*</span><span class="sxs-lookup"><span data-stu-id="8e46f-122">*Second*</span></span>  <br/> |<span data-ttu-id="8e46f-123">Integer expression specifying seconds.</span><span class="sxs-lookup"><span data-stu-id="8e46f-123">Integer expression specifying seconds.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e46f-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="8e46f-124">Remarks</span></span>

<span data-ttu-id="8e46f-125">**DateWithTimeFromParts** возвращает полностью инициализированное значение даты и времени.</span><span class="sxs-lookup"><span data-stu-id="8e46f-125">**DateWithTimeFromParts** returns a fully initialized Date/Time value.</span></span> <span data-ttu-id="8e46f-126">Если аргументы не являются допустимами, вызывается ошибка.</span><span class="sxs-lookup"><span data-stu-id="8e46f-126">If the arguments are not valid, an error is raised.</span></span> <span data-ttu-id="8e46f-127">Если необходимые аргументы — NULL, возвращается Null.</span><span class="sxs-lookup"><span data-stu-id="8e46f-127">If required arguments are Null, then Null is returned.</span></span> 
  

