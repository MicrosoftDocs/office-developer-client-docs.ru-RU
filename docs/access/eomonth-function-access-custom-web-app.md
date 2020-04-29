---
title: Функция КОНМЕСЯЦА (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: Возвращает последний день месяца до или указанное количество месяцев.
ms.openlocfilehash: 87a837069be223fdd2f9c809d706782e0955e2aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437457"
---
# <a name="eomonth-function-access-custom-web-app"></a><span data-ttu-id="5f555-103">Функция КОНМЕСЯЦА (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="5f555-103">EOMonth Function (Access custom web app)</span></span>

<span data-ttu-id="5f555-104">Возвращает последний день месяца до или указанное количество месяцев.</span><span class="sxs-lookup"><span data-stu-id="5f555-104">Returns the last day of the month before or specified number of months.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5f555-105">Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="5f555-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="5f555-106">Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="5f555-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5f555-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f555-107">Syntax</span></span>

 <span data-ttu-id="5f555-108">**КОНМЕСЯЦА** (*Date*, *нумберофмонс*)</span><span class="sxs-lookup"><span data-stu-id="5f555-108">**EOMonth** (*Date*, *NumberOfMonth*)</span></span> 
  
<span data-ttu-id="5f555-109">**КОНМЕСЯЦА** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="5f555-109">The **EOMonth** contains the following arguments.</span></span> 
  
|<span data-ttu-id="5f555-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="5f555-110">**Argument name**</span></span>|<span data-ttu-id="5f555-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5f555-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5f555-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="5f555-112">*Date*</span></span>  <br/> |<span data-ttu-id="5f555-113">Дата начала в формате даты/времени или в допустимом текстовом представлении даты.</span><span class="sxs-lookup"><span data-stu-id="5f555-113">The start date in Date/Time format, or in an accepted text representation of a date.</span></span>  <br/> |
| <span data-ttu-id="5f555-114">*нумберофмонс*</span><span class="sxs-lookup"><span data-stu-id="5f555-114">*NumberOfMonth*</span></span>  <br/> |<span data-ttu-id="5f555-115">Число, представляющее количество месяцев до или после *даты* .</span><span class="sxs-lookup"><span data-stu-id="5f555-115">A number representing the number of months before or after the  *Date*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f555-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="5f555-116">Remarks</span></span>

<span data-ttu-id="5f555-117">Если *Дата* не является допустимой датой, **КОНМЕСЯЦА** возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="5f555-117">If  *Date*  is not a valid date, **EOMonth** returns an error.</span></span> 
  
<span data-ttu-id="5f555-118">Если *Дата* плюс *нумберофмонс* возвращает недопустимую дату, **КОНМЕСЯЦА** возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="5f555-118">If  *Date*  plus  *NumberOfMonth*  yields an invalid date, **EOMonth** returns an error.</span></span> 
  

