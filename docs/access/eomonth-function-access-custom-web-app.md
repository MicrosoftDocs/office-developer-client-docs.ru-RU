---
title: Функция КОНМЕСЯЦА (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: Возвращает последний день месяца, прежде чем или указанное число месяцев.
ms.openlocfilehash: cee42c4e5cb3a24b2e702673238ac9ee09bc7372
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806936"
---
# <a name="eomonth-function-access-custom-web-app"></a><span data-ttu-id="1c77d-103">Функция КОНМЕСЯЦА (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="1c77d-103">EOMonth Function (Access custom web app)</span></span>

<span data-ttu-id="1c77d-104">Возвращает последний день месяца, прежде чем или указанное число месяцев.</span><span class="sxs-lookup"><span data-stu-id="1c77d-104">Returns the last day of the month before or specified number of months.</span></span>
  
> [!NOTE]
> <span data-ttu-id="1c77d-105">Компонент хранилища облаке, описанных в этой статье в Office 2013 и Office 2016 больше не поддерживается и может привести следующее сообщение об ошибке: > *к сожалению, мы возникают проблемы с сервера, поэтому мы не удается добавить \<службы\> на данный момент. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="1c77d-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="1c77d-106">> Для облачного хранилища для Microsoft Office Online, Office для операций ввода-вывода и Office для Android можно найти в нашем [Партнерской программы Office облачных хранилища](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="1c77d-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1c77d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c77d-107">Syntax</span></span>

 <span data-ttu-id="1c77d-108">**КОНМЕСЯЦА** (*Дата*, *NumberOfMonth*)</span><span class="sxs-lookup"><span data-stu-id="1c77d-108">**EOMonth** (*Date*, *NumberOfMonth*)</span></span> 
  
<span data-ttu-id="1c77d-109">**КОНМЕСЯЦА** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="1c77d-109">The **EOMonth** contains the following arguments.</span></span> 
  
|<span data-ttu-id="1c77d-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="1c77d-110">**Argument name**</span></span>|<span data-ttu-id="1c77d-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1c77d-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="1c77d-112">*Дата*</span><span class="sxs-lookup"><span data-stu-id="1c77d-112">*Date*</span></span>  <br/> |<span data-ttu-id="1c77d-113">Дата начала в формат даты и времени или в обслуживаемых текстовым представлением даты.</span><span class="sxs-lookup"><span data-stu-id="1c77d-113">The start date in Date/Time format, or in an accepted text representation of a date.</span></span>  <br/> |
| <span data-ttu-id="1c77d-114">*NumberOfMonth*</span><span class="sxs-lookup"><span data-stu-id="1c77d-114">*NumberOfMonth*</span></span>  <br/> |<span data-ttu-id="1c77d-115">Число, представляющее количество месяцев до или после *даты* .</span><span class="sxs-lookup"><span data-stu-id="1c77d-115">A number representing the number of months before or after the  *Date*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c77d-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="1c77d-116">Remarks</span></span>

<span data-ttu-id="1c77d-117">Если *Дата* не является допустимой датой, **то КОНМЕСЯЦА** возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="1c77d-117">If  *Date*  is not a valid date, **EOMonth** returns an error.</span></span> 
  
<span data-ttu-id="1c77d-118">Если *Дата* , а также *NumberOfMonth* дает недопустимые даты, **то КОНМЕСЯЦА** возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="1c77d-118">If  *Date*  plus  *NumberOfMonth*  yields an invalid date, **EOMonth** returns an error.</span></span> 
  

