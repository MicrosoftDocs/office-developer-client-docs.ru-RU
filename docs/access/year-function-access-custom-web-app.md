---
title: Функция год (Доступ к настраиваемой веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a70751eb-bfde-4f7d-ad90-a1e4cca25dbc
description: Возвращает числовую величину, которая представляет год указанной даты в григорианском календаре.
ms.openlocfilehash: 1400c352bcc070035d15b46f8e547e4637364299
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433124"
---
# <a name="year-function-access-custom-web-app"></a><span data-ttu-id="2111e-103">Функция год (Доступ к настраиваемой веб-приложению)</span><span class="sxs-lookup"><span data-stu-id="2111e-103">Year Function (Access custom web app)</span></span>

<span data-ttu-id="2111e-104">Возвращает числовую величину, которая представляет год указанной даты в григорианском календаре.</span><span class="sxs-lookup"><span data-stu-id="2111e-104">Returns a numeric value that represents the year of the specified date in the Gregorian calendar.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2111e-105">Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="2111e-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="2111e-106">Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="2111e-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2111e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2111e-107">Syntax</span></span>

 <span data-ttu-id="2111e-108">**Год** *(Дата)*</span><span class="sxs-lookup"><span data-stu-id="2111e-108">**Year** (*Date*)</span></span> 
  
<span data-ttu-id="2111e-109">Функция **Год** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="2111e-109">The **Year** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="2111e-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="2111e-110">**Argument name**</span></span>|<span data-ttu-id="2111e-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2111e-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2111e-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="2111e-112">*Date*</span></span>  <br/> |<span data-ttu-id="2111e-113">Выражение, которое может быть разрешено к значению Date/Time.</span><span class="sxs-lookup"><span data-stu-id="2111e-113">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="2111e-114">Выражение  *аргумента Date,*  выражение столбца, переменная, определяемая пользователем, или строковая буквальная.</span><span class="sxs-lookup"><span data-stu-id="2111e-114">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2111e-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="2111e-115">Remarks</span></span>

<span data-ttu-id="2111e-116">Значения, возвращаемые функциями  **Год,** Месяц и День, будут григорианские значения независимо от формата отображения для предоставленного значения даты.</span><span class="sxs-lookup"><span data-stu-id="2111e-116">Values returned by the **Year**, **Month**, and **Day** functions will be Gregorian values regardless of the display format for the supplied date value.</span></span> <span data-ttu-id="2111e-117">Например, если в формате отображения предоставленной даты используется календарь хиджри, возвращенные значения для функций **Год,** Месяц и День будут значениями, связанными с эквивалентной григорианской датой.  </span><span class="sxs-lookup"><span data-stu-id="2111e-117">For example, if the display format of the supplied date uses the Hijri calendar, the returned values for the **Year**, **Month**, and **Day** functions will be values associated with the equivalent Gregorian date.</span></span> 
  

