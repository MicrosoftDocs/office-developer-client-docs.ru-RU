---
title: Функция Датефромпартс (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: Возвращает значение даты для указанного года, месяца и дня.
ms.openlocfilehash: 7d47fe93d1990365f1db5885a3ea8fc056aabb9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423225"
---
# <a name="datefromparts-function-access-custom-web-app"></a><span data-ttu-id="fab01-103">Функция Датефромпартс (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="fab01-103">DateFromParts function (Access custom web app)</span></span>

<span data-ttu-id="fab01-104">Возвращает значение даты для указанного года, месяца и дня.</span><span class="sxs-lookup"><span data-stu-id="fab01-104">Returns a date value for the specified year, month, and day.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fab01-105">Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="fab01-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="fab01-106">Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="fab01-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fab01-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fab01-107">Syntax</span></span>

<span data-ttu-id="fab01-108">**Датефромпартс** (*Год*, *месяц*, *день*)</span><span class="sxs-lookup"><span data-stu-id="fab01-108">**DateFromParts** (*Year*, *Month*, *Day*)</span></span> 
  
<span data-ttu-id="fab01-109">Функция **датефромпартс** содержит указанные ниже аргументы.</span><span class="sxs-lookup"><span data-stu-id="fab01-109">The **DateFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="fab01-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="fab01-110">**Argument name**</span></span>|<span data-ttu-id="fab01-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fab01-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="fab01-112">*Year*</span><span class="sxs-lookup"><span data-stu-id="fab01-112">*Year*</span></span>  <br/> |<span data-ttu-id="fab01-113">Целочисленное выражение, задающее год.</span><span class="sxs-lookup"><span data-stu-id="fab01-113">Integer expression specifying a year.</span></span>  <br/> |
| <span data-ttu-id="fab01-114">*Month*</span><span class="sxs-lookup"><span data-stu-id="fab01-114">*Month*</span></span>  <br/> |<span data-ttu-id="fab01-115">Целочисленное выражение, задающее месяц, от 1 до 12.</span><span class="sxs-lookup"><span data-stu-id="fab01-115">Integer expression specifying a month, from 1 to 12.</span></span>  <br/> |
| <span data-ttu-id="fab01-116">*Day*</span><span class="sxs-lookup"><span data-stu-id="fab01-116">*Day*</span></span>  <br/> |<span data-ttu-id="fab01-117">Целочисленное выражение, задающее день.</span><span class="sxs-lookup"><span data-stu-id="fab01-117">Integer expression specifying a day.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fab01-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="fab01-118">Remarks</span></span>

<span data-ttu-id="fab01-119">**Датефромпартс** возвращает значение даты с компонентом Date, значение которого равно указанному году, месяцу и дню и временной части, установленной по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fab01-119">**DateFromParts** returns a date value with the date portion set to the specified year, month and day, and the time portion set to the default.</span></span> <span data-ttu-id="fab01-120">Если аргументы являются недопустимыми, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="fab01-120">If the arguments are not valid, then an error is raised.</span></span> <span data-ttu-id="fab01-121">Если обязательные аргументы имеют значение null, возвращается значение NULL.</span><span class="sxs-lookup"><span data-stu-id="fab01-121">If required arguments are null, then NULL is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="fab01-122">Пример</span><span class="sxs-lookup"><span data-stu-id="fab01-122">Example</span></span>

<span data-ttu-id="fab01-123">Следующее выражение использует функцию **датефромпартс** для вычисления первого дня текущего месяца.</span><span class="sxs-lookup"><span data-stu-id="fab01-123">The following expression uses the **DateFromParts** function to calculate the first day of the current month.</span></span> 
  
`DateFromParts(Year(Today()),Month(Today()),1)`



