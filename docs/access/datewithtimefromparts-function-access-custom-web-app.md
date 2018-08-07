---
title: Функция DateWithTimeFromParts (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: Возвращает дату и время в зависимости от указанного год, месяц, день и время.
ms.openlocfilehash: 8cc1fbe700d18c04d944793bcea889424b0cff3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806915"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a><span data-ttu-id="e8881-103">Функция DateWithTimeFromParts (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="e8881-103">DateWithTimeFromParts function (Access custom web app)</span></span>

<span data-ttu-id="e8881-104">Возвращает дату и время в зависимости от указанного год, месяц, день и время.</span><span class="sxs-lookup"><span data-stu-id="e8881-104">Returns a Date and Time based on a specified year, month, day, and time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e8881-105">Компонент хранилища облаке, описанных в этой статье в Office 2013 и Office 2016 больше не поддерживается и может привести следующее сообщение об ошибке: > *к сожалению, мы возникают проблемы с сервера, поэтому мы не удается добавить \<службы\> на данный момент. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="e8881-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="e8881-106">> Для облачного хранилища для Microsoft Office Online, Office для операций ввода-вывода и Office для Android можно найти в нашем [Партнерской программы Office облачных хранилища](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="e8881-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e8881-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8881-107">Syntax</span></span>

<span data-ttu-id="e8881-108">**DateWithTimeFromParts** (*Год*, *месяц*, *день*, *час*, *минута*, *второй*)</span><span class="sxs-lookup"><span data-stu-id="e8881-108">**DateWithTimeFromParts** (*Year*, *Month*, *Day*, *Hour*, *Minute*, *Second*)</span></span> 
  
<span data-ttu-id="e8881-109">Функция **DateWithTimeFromParts** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="e8881-109">The **DateWithTimeFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="e8881-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="e8881-110">**Argument name**</span></span>|<span data-ttu-id="e8881-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e8881-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e8881-112">*Year*</span><span class="sxs-lookup"><span data-stu-id="e8881-112">*Year*</span></span>  <br/> |<span data-ttu-id="e8881-113">Выражение целое число, указывающее года.</span><span class="sxs-lookup"><span data-stu-id="e8881-113">Integer expression specifying a year.</span></span>  <br/> |
| <span data-ttu-id="e8881-114">*Month*</span><span class="sxs-lookup"><span data-stu-id="e8881-114">*Month*</span></span>  <br/> |<span data-ttu-id="e8881-115">Выражение целое число, указывающее месяц.</span><span class="sxs-lookup"><span data-stu-id="e8881-115">Integer expression specifying a month.</span></span>  <br/> |
| <span data-ttu-id="e8881-116">*Day*</span><span class="sxs-lookup"><span data-stu-id="e8881-116">*Day*</span></span>  <br/> |<span data-ttu-id="e8881-117">Выражение целое число, указывающее день.</span><span class="sxs-lookup"><span data-stu-id="e8881-117">Integer expression specifying a day.</span></span>  <br/> |
| <span data-ttu-id="e8881-118">*Час*</span><span class="sxs-lookup"><span data-stu-id="e8881-118">*Hour*</span></span>  <br/> |<span data-ttu-id="e8881-119">Выражение целое число, указывающее часов.</span><span class="sxs-lookup"><span data-stu-id="e8881-119">Integer expression specifying hours.</span></span>  <br/> |
| <span data-ttu-id="e8881-120">*Минуты*</span><span class="sxs-lookup"><span data-stu-id="e8881-120">*Minute*</span></span>  <br/> |<span data-ttu-id="e8881-121">Выражение целое число, указывающее минут.</span><span class="sxs-lookup"><span data-stu-id="e8881-121">Integer expression specifying minutes.</span></span>  <br/> |
| <span data-ttu-id="e8881-122">*Секунды*</span><span class="sxs-lookup"><span data-stu-id="e8881-122">*Second*</span></span>  <br/> |<span data-ttu-id="e8881-123">Выражение целое число, указывающее секунд.</span><span class="sxs-lookup"><span data-stu-id="e8881-123">Integer expression specifying seconds.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8881-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="e8881-124">Remarks</span></span>

<span data-ttu-id="e8881-125">**DateWithTimeFromParts** возвращает полностью инициализации значение даты и времени.</span><span class="sxs-lookup"><span data-stu-id="e8881-125">**DateWithTimeFromParts** returns a fully initialized Date/Time value.</span></span> <span data-ttu-id="e8881-126">Если аргументы не допускаются, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="e8881-126">If the arguments are not valid, an error is raised.</span></span> <span data-ttu-id="e8881-127">При необходимости, что аргументы имеют значение Null, возвращается значение Null.</span><span class="sxs-lookup"><span data-stu-id="e8881-127">If required arguments are Null, then Null is returned.</span></span> 
  

