---
title: Функция Day (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0a77e4-0653-4a85-b507-13440aef195b
description: Возвращает целое число, представляющее день (день месяца) указанной даты григорианского календаря.
ms.openlocfilehash: 720adaffbd97a735f6b1395e64965f972c6099cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280693"
---
# <a name="day-function-access-custom-web-app"></a><span data-ttu-id="c95cd-103">Функция Day (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="c95cd-103">Day function (Access custom web app)</span></span>

<span data-ttu-id="c95cd-104">Возвращает целое число, представляющее день (день месяца) указанной даты григорианского календаря.</span><span class="sxs-lookup"><span data-stu-id="c95cd-104">Returns an integer representing the day (day of the month) of the specified date in the Gregorian calendar.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c95cd-105">Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="c95cd-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="c95cd-106">Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="c95cd-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c95cd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c95cd-107">Syntax</span></span>

<span data-ttu-id="c95cd-108">**Day (день** ) (*Date*)</span><span class="sxs-lookup"><span data-stu-id="c95cd-108">**Day** (*Date*)</span></span> 
  
<span data-ttu-id="c95cd-109">Функция **Day** содержит следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="c95cd-109">The **Day** function contains the following argument.</span></span> 
  
|<span data-ttu-id="c95cd-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="c95cd-110">**Argument name**</span></span>|<span data-ttu-id="c95cd-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c95cd-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c95cd-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="c95cd-112">*Date*</span></span>  <br/> |<span data-ttu-id="c95cd-113">Выражение, которое может быть разрешено в значение даты и времени.</span><span class="sxs-lookup"><span data-stu-id="c95cd-113">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="c95cd-114">Выражение аргумента *Date* , выражение столбца, определяемая пользователем переменная или строковый литерал.</span><span class="sxs-lookup"><span data-stu-id="c95cd-114">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c95cd-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="c95cd-115">Remarks</span></span>

<span data-ttu-id="c95cd-116">**Day** возвращает то же значение, что и **DatePart** (Day, Date).</span><span class="sxs-lookup"><span data-stu-id="c95cd-116">**Day** returns the same value as **Datepart** (day, date).</span></span> 
  

