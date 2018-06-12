---
title: Функция Month (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5df43594-a434-4fb7-8109-e5cf0401ae09
description: Возвращает целое число, представляющее месяц указанной даты.
ms.openlocfilehash: 5e4a583a5a299456e57b90d7cef41a32b0a6ffba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807090"
---
# <a name="month-function-access-custom-web-app"></a><span data-ttu-id="f6c22-103">Функция Month (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="f6c22-103">Month Function (Access custom web app)</span></span>

<span data-ttu-id="f6c22-104">Возвращает целое число, представляющее месяц указанной даты.</span><span class="sxs-lookup"><span data-stu-id="f6c22-104">Returns an integer that represents the month of the specified date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f6c22-105">Компонент хранилища облаке, описанных в этой статье в Office 2013 и Office 2016 больше не поддерживается и может привести следующее сообщение об ошибке: > *к сожалению, мы возникают проблемы с сервера, поэтому мы не удается добавить \<службы\> на данный момент. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="f6c22-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="f6c22-106">> Для облачного хранилища для Microsoft Office Online, Office для операций ввода-вывода и Office для Android можно найти в нашем [Партнерской программы Office облачных хранилища](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="f6c22-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f6c22-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6c22-107">Syntax</span></span>

 <span data-ttu-id="f6c22-108">**Месяц** (*Дата*)</span><span class="sxs-lookup"><span data-stu-id="f6c22-108">**Month** (*Date*)</span></span> 
  
<span data-ttu-id="f6c22-109">Функция **Month** содержит следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="f6c22-109">The **Month** function contains the following argument.</span></span> 
  
|<span data-ttu-id="f6c22-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="f6c22-110">**Argument name**</span></span>|<span data-ttu-id="f6c22-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f6c22-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f6c22-112">*Дата*</span><span class="sxs-lookup"><span data-stu-id="f6c22-112">*Date*</span></span>  <br/> |<span data-ttu-id="f6c22-113">Выражение, которое разрешается в значение даты и времени.</span><span class="sxs-lookup"><span data-stu-id="f6c22-113">An expression that can be resolved to a Date/Time value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6c22-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="f6c22-114">Remarks</span></span>

 <span data-ttu-id="f6c22-115">**Месяц** возвращает совпадает со значением **DatePart** (месяц, дата).</span><span class="sxs-lookup"><span data-stu-id="f6c22-115">**Month** returns the same value as **DatePart** (month, date).</span></span> 
  
<span data-ttu-id="f6c22-116">Если *Дата* содержит только часть времени, возвращаемое значение равно 1, базовый месяца.</span><span class="sxs-lookup"><span data-stu-id="f6c22-116">If  *Date*  contains only a time part, the return value is 1, the base month.</span></span> 
  

