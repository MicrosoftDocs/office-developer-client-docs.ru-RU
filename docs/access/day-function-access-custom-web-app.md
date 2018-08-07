---
title: Функция Day (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0a77e4-0653-4a85-b507-13440aef195b
description: Возвращает значение типа integer, представляющее день указанной даты в календаре григорианский (день месяца).
ms.openlocfilehash: ae0e5f4671a8c0ee3dc95683240328351ea2c5d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806930"
---
# <a name="day-function-access-custom-web-app"></a><span data-ttu-id="17acc-103">Функция Day (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="17acc-103">Day function (Access custom web app)</span></span>

<span data-ttu-id="17acc-104">Возвращает значение типа integer, представляющее день указанной даты в календаре григорианский (день месяца).</span><span class="sxs-lookup"><span data-stu-id="17acc-104">Returns an integer representing the day (day of the month) of the specified date in the Gregorian calendar.</span></span>
  
> [!NOTE]
> <span data-ttu-id="17acc-105">Компонент хранилища облаке, описанных в этой статье в Office 2013 и Office 2016 больше не поддерживается и может привести следующее сообщение об ошибке: > *к сожалению, мы возникают проблемы с сервера, поэтому мы не удается добавить \<службы\> на данный момент. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="17acc-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="17acc-106">> Для облачного хранилища для Microsoft Office Online, Office для операций ввода-вывода и Office для Android можно найти в нашем [Партнерской программы Office облачных хранилища](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="17acc-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="17acc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17acc-107">Syntax</span></span>

<span data-ttu-id="17acc-108">**День** (*Дата*)</span><span class="sxs-lookup"><span data-stu-id="17acc-108">**Day** (*Date*)</span></span> 
  
<span data-ttu-id="17acc-109">Функция **Day** содержит следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="17acc-109">The **Day** function contains the following argument.</span></span> 
  
|<span data-ttu-id="17acc-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="17acc-110">**Argument name**</span></span>|<span data-ttu-id="17acc-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="17acc-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="17acc-112">*Дата*</span><span class="sxs-lookup"><span data-stu-id="17acc-112">*Date*</span></span>  <br/> |<span data-ttu-id="17acc-113">Выражение, которое разрешается в значение даты и времени.</span><span class="sxs-lookup"><span data-stu-id="17acc-113">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="17acc-114">Аргумент выражение *даты* , выражение столбца, переменной, определенной пользователем или строковый литерал.</span><span class="sxs-lookup"><span data-stu-id="17acc-114">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17acc-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="17acc-115">Remarks</span></span>

<span data-ttu-id="17acc-116">**День** возвращает совпадает со значением **Datepart** (день, дата).</span><span class="sxs-lookup"><span data-stu-id="17acc-116">**Day** returns the same value as **Datepart** (day, date).</span></span> 
  

