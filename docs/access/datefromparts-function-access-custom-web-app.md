---
title: Функция DateFromParts (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: Возвращает значение типа date для указанного года, месяца и дня.
ms.openlocfilehash: 5a2ff76d99076cf9f53b0dce8c5019f38d910f58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806917"
---
# <a name="datefromparts-function-access-custom-web-app"></a><span data-ttu-id="101a2-103">Функция DateFromParts (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="101a2-103">DateFromParts function (Access custom web app)</span></span>

<span data-ttu-id="101a2-104">Возвращает значение типа date для указанного года, месяца и дня.</span><span class="sxs-lookup"><span data-stu-id="101a2-104">Returns a date value for the specified year, month, and day.</span></span>
  
> [!NOTE]
> <span data-ttu-id="101a2-105">Компонент хранилища облаке, описанных в этой статье в Office 2013 и Office 2016 больше не поддерживается и может привести следующее сообщение об ошибке: > *к сожалению, мы возникают проблемы с сервера, поэтому мы не удается добавить \<службы\> на данный момент. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="101a2-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="101a2-106">> Для облачного хранилища для Microsoft Office Online, Office для операций ввода-вывода и Office для Android можно найти в нашем [Партнерской программы Office облачных хранилища](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="101a2-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="101a2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="101a2-107">Syntax</span></span>

<span data-ttu-id="101a2-108">**DateFromParts** (*Год*, *месяц*, *день*)</span><span class="sxs-lookup"><span data-stu-id="101a2-108">**DateFromParts** (*Year*, *Month*, *Day*)</span></span> 
  
<span data-ttu-id="101a2-109">Функция **DateFromParts** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="101a2-109">The **DateFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="101a2-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="101a2-110">**Argument name**</span></span>|<span data-ttu-id="101a2-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="101a2-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="101a2-112">*Год*</span><span class="sxs-lookup"><span data-stu-id="101a2-112">*Year*</span></span>  <br/> |<span data-ttu-id="101a2-113">Выражение целое число, указывающее года.</span><span class="sxs-lookup"><span data-stu-id="101a2-113">Integer expression specifying a year.</span></span>  <br/> |
| <span data-ttu-id="101a2-114">*Месяц*</span><span class="sxs-lookup"><span data-stu-id="101a2-114">*Month*</span></span>  <br/> |<span data-ttu-id="101a2-115">Выражение целое число, указывающее месяц, от 1 до 12.</span><span class="sxs-lookup"><span data-stu-id="101a2-115">Integer expression specifying a month, from 1 to 12.</span></span>  <br/> |
| <span data-ttu-id="101a2-116">*День*</span><span class="sxs-lookup"><span data-stu-id="101a2-116">*Day*</span></span>  <br/> |<span data-ttu-id="101a2-117">Выражение целое число, указывающее день.</span><span class="sxs-lookup"><span data-stu-id="101a2-117">Integer expression specifying a day.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="101a2-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="101a2-118">Remarks</span></span>

<span data-ttu-id="101a2-119">**DateFromParts** возвращает значение типа date с области даты, задайте для указанного года, месяца и дня и области времени, значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="101a2-119">**DateFromParts** returns a date value with the date portion set to the specified year, month and day, and the time portion set to the default.</span></span> <span data-ttu-id="101a2-120">Если аргументы не допускаются, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="101a2-120">If the arguments are not valid, then an error is raised.</span></span> <span data-ttu-id="101a2-121">При необходимости, что аргументы имеют значение null, возвращается значение NULL.</span><span class="sxs-lookup"><span data-stu-id="101a2-121">If required arguments are null, then NULL is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="101a2-122">Пример</span><span class="sxs-lookup"><span data-stu-id="101a2-122">Example</span></span>

<span data-ttu-id="101a2-123">Следующее выражение использует функцию **DateFromParts** для вычисления с первого дня текущего месяца.</span><span class="sxs-lookup"><span data-stu-id="101a2-123">The following expression uses the **DateFromParts** function to calculate the first day of the current month.</span></span> 
  
`DateFromParts(Year(Today()),Month(Today()),1)`



