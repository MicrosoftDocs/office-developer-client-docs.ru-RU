---
title: Функция Датевистимефромпартс (пользовательское веб-приложение для Access)
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
# <a name="datewithtimefromparts-function-access-custom-web-app"></a><span data-ttu-id="8d1b1-103">Функция Датевистимефромпартс (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="8d1b1-103">DateWithTimeFromParts function (Access custom web app)</span></span>

<span data-ttu-id="8d1b1-104">Возвращает дату и время на основе указанного года, месяца, дня и времени.</span><span class="sxs-lookup"><span data-stu-id="8d1b1-104">Returns a Date and Time based on a specified year, month, day, and time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8d1b1-105">Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="8d1b1-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="8d1b1-106">Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="8d1b1-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8d1b1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d1b1-107">Syntax</span></span>

<span data-ttu-id="8d1b1-108">**Датевистимефромпартс** (*Год*, *месяц*, *день*, *час*, *минута*, *секунда*)</span><span class="sxs-lookup"><span data-stu-id="8d1b1-108">**DateWithTimeFromParts** (*Year*, *Month*, *Day*, *Hour*, *Minute*, *Second*)</span></span> 
  
<span data-ttu-id="8d1b1-109">Функция **датевистимефромпартс** содержит указанные ниже аргументы.</span><span class="sxs-lookup"><span data-stu-id="8d1b1-109">The **DateWithTimeFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="8d1b1-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="8d1b1-110">**Argument name**</span></span>|<span data-ttu-id="8d1b1-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8d1b1-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="8d1b1-112">*Year*</span><span class="sxs-lookup"><span data-stu-id="8d1b1-112">*Year*</span></span>  <br/> |<span data-ttu-id="8d1b1-113">Целочисленное выражение, задающее год.</span><span class="sxs-lookup"><span data-stu-id="8d1b1-113">Integer expression specifying a year.</span></span>  <br/> |
| <span data-ttu-id="8d1b1-114">*Month*</span><span class="sxs-lookup"><span data-stu-id="8d1b1-114">*Month*</span></span>  <br/> |<span data-ttu-id="8d1b1-115">Целочисленное выражение, задающее месяц.</span><span class="sxs-lookup"><span data-stu-id="8d1b1-115">Integer expression specifying a month.</span></span>  <br/> |
| <span data-ttu-id="8d1b1-116">*Day*</span><span class="sxs-lookup"><span data-stu-id="8d1b1-116">*Day*</span></span>  <br/> |<span data-ttu-id="8d1b1-117">Целочисленное выражение, задающее день.</span><span class="sxs-lookup"><span data-stu-id="8d1b1-117">Integer expression specifying a day.</span></span>  <br/> |
| <span data-ttu-id="8d1b1-118">*Hour*</span><span class="sxs-lookup"><span data-stu-id="8d1b1-118">*Hour*</span></span>  <br/> |<span data-ttu-id="8d1b1-119">Целочисленное выражение, задающее часы.</span><span class="sxs-lookup"><span data-stu-id="8d1b1-119">Integer expression specifying hours.</span></span>  <br/> |
| <span data-ttu-id="8d1b1-120">*Minute*</span><span class="sxs-lookup"><span data-stu-id="8d1b1-120">*Minute*</span></span>  <br/> |<span data-ttu-id="8d1b1-121">Целочисленное выражение, задающее минуты.</span><span class="sxs-lookup"><span data-stu-id="8d1b1-121">Integer expression specifying minutes.</span></span>  <br/> |
| <span data-ttu-id="8d1b1-122">*Second*</span><span class="sxs-lookup"><span data-stu-id="8d1b1-122">*Second*</span></span>  <br/> |<span data-ttu-id="8d1b1-123">Целочисленное выражение, задающее секунды.</span><span class="sxs-lookup"><span data-stu-id="8d1b1-123">Integer expression specifying seconds.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d1b1-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="8d1b1-124">Remarks</span></span>

<span data-ttu-id="8d1b1-125">**Датевистимефромпартс** Возвращает полностью инициализированное значение даты и времени.</span><span class="sxs-lookup"><span data-stu-id="8d1b1-125">**DateWithTimeFromParts** returns a fully initialized Date/Time value.</span></span> <span data-ttu-id="8d1b1-126">Если аргументы являются недопустимыми, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="8d1b1-126">If the arguments are not valid, an error is raised.</span></span> <span data-ttu-id="8d1b1-127">Если обязательные аргументы имеют значение null, возвращается значение null.</span><span class="sxs-lookup"><span data-stu-id="8d1b1-127">If required arguments are Null, then Null is returned.</span></span> 
  

