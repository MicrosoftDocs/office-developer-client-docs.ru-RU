---
title: Функция Year (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a70751eb-bfde-4f7d-ad90-a1e4cca25dbc
description: Возвращает числовое значение, представляющее год указанной даты в григорианском календаре.
ms.openlocfilehash: 1400c352bcc070035d15b46f8e547e4637364299
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433124"
---
# <a name="year-function-access-custom-web-app"></a><span data-ttu-id="8f01a-103">Функция Year (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="8f01a-103">Year Function (Access custom web app)</span></span>

<span data-ttu-id="8f01a-104">Возвращает числовое значение, представляющее год указанной даты в григорианском календаре.</span><span class="sxs-lookup"><span data-stu-id="8f01a-104">Returns a numeric value that represents the year of the specified date in the Gregorian calendar.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8f01a-105">Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="8f01a-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="8f01a-106">Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="8f01a-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8f01a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f01a-107">Syntax</span></span>

 <span data-ttu-id="8f01a-108">**Year (год** ) (*Date*)</span><span class="sxs-lookup"><span data-stu-id="8f01a-108">**Year** (*Date*)</span></span> 
  
<span data-ttu-id="8f01a-109">Функция **year** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="8f01a-109">The **Year** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="8f01a-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="8f01a-110">**Argument name**</span></span>|<span data-ttu-id="8f01a-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8f01a-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="8f01a-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="8f01a-112">*Date*</span></span>  <br/> |<span data-ttu-id="8f01a-113">Выражение, которое может быть разрешено в значение даты и времени.</span><span class="sxs-lookup"><span data-stu-id="8f01a-113">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="8f01a-114">Выражение аргумента *Date* , выражение столбца, определяемая пользователем переменная или строковый литерал.</span><span class="sxs-lookup"><span data-stu-id="8f01a-114">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8f01a-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="8f01a-115">Remarks</span></span>

<span data-ttu-id="8f01a-116">Значения, возвращаемые функциями **year**, **Month**и **Day** , будут иметь значения григорианского, независимо от формата отображения для указанного значения даты.</span><span class="sxs-lookup"><span data-stu-id="8f01a-116">Values returned by the **Year**, **Month**, and **Day** functions will be Gregorian values regardless of the display format for the supplied date value.</span></span> <span data-ttu-id="8f01a-117">Например, если формат отображения предоставленной даты использует календарь Хиджра, возвращаемые значения для функций **год**, **месяц**и **день** будут иметь значения, связанные с эквивалентной датой григорианского календаря.</span><span class="sxs-lookup"><span data-stu-id="8f01a-117">For example, if the display format of the supplied date uses the Hijri calendar, the returned values for the **Year**, **Month**, and **Day** functions will be values associated with the equivalent Gregorian date.</span></span> 
  

