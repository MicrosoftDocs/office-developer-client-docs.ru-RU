---
title: Функция Month (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5df43594-a434-4fb7-8109-e5cf0401ae09
description: Возвращает целое число, представляющее месяц указанной даты.
ms.openlocfilehash: 0ca7059a2fd6dad1f9790ad6f4eafe7affa014dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411493"
---
# <a name="month-function-access-custom-web-app"></a><span data-ttu-id="434f3-103">Функция Month (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="434f3-103">Month Function (Access custom web app)</span></span>

<span data-ttu-id="434f3-104">Возвращает целое число, представляющее месяц указанной даты.</span><span class="sxs-lookup"><span data-stu-id="434f3-104">Returns an integer that represents the month of the specified date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="434f3-105">Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="434f3-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="434f3-106">Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="434f3-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="434f3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="434f3-107">Syntax</span></span>

 <span data-ttu-id="434f3-108">**Month (месяц** ) (*Date*)</span><span class="sxs-lookup"><span data-stu-id="434f3-108">**Month** (*Date*)</span></span> 
  
<span data-ttu-id="434f3-109">Функция **Month** содержит следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="434f3-109">The **Month** function contains the following argument.</span></span> 
  
|<span data-ttu-id="434f3-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="434f3-110">**Argument name**</span></span>|<span data-ttu-id="434f3-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="434f3-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="434f3-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="434f3-112">*Date*</span></span>  <br/> |<span data-ttu-id="434f3-113">Выражение, которое может быть разрешено в значение даты и времени.</span><span class="sxs-lookup"><span data-stu-id="434f3-113">An expression that can be resolved to a Date/Time value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="434f3-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="434f3-114">Remarks</span></span>

 <span data-ttu-id="434f3-115">**Month** возвращает то же значение, что и **DatePart** (month, Date).</span><span class="sxs-lookup"><span data-stu-id="434f3-115">**Month** returns the same value as **DatePart** (month, date).</span></span> 
  
<span data-ttu-id="434f3-116">Если *Дата* содержит только часть времени, возвращается значение 1, базовый месяц.</span><span class="sxs-lookup"><span data-stu-id="434f3-116">If  *Date*  contains only a time part, the return value is 1, the base month.</span></span> 
  

