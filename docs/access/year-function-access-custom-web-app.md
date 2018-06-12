---
title: Функция Year (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a70751eb-bfde-4f7d-ad90-a1e4cca25dbc
description: Возвращает числовое значение, представляющее год указанной даты в григорианский календарь.
ms.openlocfilehash: f9d72343637734257a2ed9589e5539b845933826
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807141"
---
# <a name="year-function-access-custom-web-app"></a><span data-ttu-id="98b2d-103">Функция Year (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="98b2d-103">Year Function (Access custom web app)</span></span>

<span data-ttu-id="98b2d-104">Возвращает числовое значение, представляющее год указанной даты в григорианский календарь.</span><span class="sxs-lookup"><span data-stu-id="98b2d-104">Returns a numeric value that represents the year of the specified date in the Gregorian calendar.</span></span>
  
> [!NOTE]
> <span data-ttu-id="98b2d-105">Компонент хранилища облаке, описанных в этой статье в Office 2013 и Office 2016 больше не поддерживается и может привести следующее сообщение об ошибке: > *к сожалению, мы возникают проблемы с сервера, поэтому мы не удается добавить \<службы\> на данный момент. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="98b2d-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="98b2d-106">> Для облачного хранилища для Microsoft Office Online, Office для операций ввода-вывода и Office для Android можно найти в нашем [Партнерской программы Office облачных хранилища](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="98b2d-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="98b2d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98b2d-107">Syntax</span></span>

 <span data-ttu-id="98b2d-108">**Год** (*Дата*)</span><span class="sxs-lookup"><span data-stu-id="98b2d-108">**Year** (*Date*)</span></span> 
  
<span data-ttu-id="98b2d-109">Функция **Year** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="98b2d-109">The **Year** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="98b2d-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="98b2d-110">**Argument name**</span></span>|<span data-ttu-id="98b2d-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="98b2d-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="98b2d-112">*Дата*</span><span class="sxs-lookup"><span data-stu-id="98b2d-112">*Date*</span></span>  <br/> |<span data-ttu-id="98b2d-113">Выражение, которое разрешается в значение даты и времени.</span><span class="sxs-lookup"><span data-stu-id="98b2d-113">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="98b2d-114">Аргумент выражение *даты* , выражение столбца, переменной, определенной пользователем или строковый литерал.</span><span class="sxs-lookup"><span data-stu-id="98b2d-114">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98b2d-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="98b2d-115">Remarks</span></span>

<span data-ttu-id="98b2d-116">Значения, возвращаемые функциями **год**, **месяц**и **день** , считаются григорианский независимо от того, формат отображения для значения даты.</span><span class="sxs-lookup"><span data-stu-id="98b2d-116">Values returned by the **Year**, **Month**, and **Day** functions will be Gregorian values regardless of the display format for the supplied date value.</span></span> <span data-ttu-id="98b2d-117">Например если формат отображения даты используется календарь хиджра, возвращаемые **год**, **месяц**и **день** функции будут быть значения, связанные с эквивалентный даты григорианский.</span><span class="sxs-lookup"><span data-stu-id="98b2d-117">For example, if the display format of the supplied date uses the Hijri calendar, the returned values for the **Year**, **Month**, and **Day** functions will be values associated with the equivalent Gregorian date.</span></span> 
  

