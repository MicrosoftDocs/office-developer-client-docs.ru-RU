---
title: Функция Now (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8842a555-d4c8-4528-b5f9-0ddf5691273d
description: Возвращает текущее значение даты и времени в часовом поясе, определенном приложением.
ms.openlocfilehash: 74b0a124e5715036146fedc9a6079d84a39ce84a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425717"
---
# <a name="now-function-access-custom-web-app"></a><span data-ttu-id="6f1d8-103">Функция Now (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="6f1d8-103">Now Function (Access custom web app)</span></span>

<span data-ttu-id="6f1d8-104">Возвращает текущее значение даты и времени в часовом поясе, определенном приложением.</span><span class="sxs-lookup"><span data-stu-id="6f1d8-104">Returns the current date and time value in the time zone defined by the application.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6f1d8-105">Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="6f1d8-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="6f1d8-106">Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="6f1d8-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6f1d8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f1d8-107">Syntax</span></span>

 <span data-ttu-id="6f1d8-108">**Now** ()</span><span class="sxs-lookup"><span data-stu-id="6f1d8-108">**Now** ()</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6f1d8-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="6f1d8-109">Remarks</span></span>

<span data-ttu-id="6f1d8-110">Результат выполнения функции **Now** изменяется только при обновлении столбца, содержащего формулу.</span><span class="sxs-lookup"><span data-stu-id="6f1d8-110">The result of the **Now** function changes only when the column that contains the formula is refreshed.</span></span> <span data-ttu-id="6f1d8-111">Он не обновляется непрерывно.</span><span class="sxs-lookup"><span data-stu-id="6f1d8-111">It is not updated continuously.</span></span> 
  
<span data-ttu-id="6f1d8-112">Функция **Today** возвращает ту же самую дату, но не является точной относительно времени; возвращаемое время всегда равно 12:00:00 AM и обновляется только дата.</span><span class="sxs-lookup"><span data-stu-id="6f1d8-112">The **Today** function returns the same date but is not precise with regard to time; the time returned is always 12:00:00 AM and only the date is updated.</span></span> 
  

