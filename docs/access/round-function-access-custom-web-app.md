---
title: Функция ОКРУГЛ (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4af7fbe2-ee34-4a52-b55e-ce3983313b5e
description: Возвращает числовое значение, которое округляется или усекается до указанной длины или точности.
ms.openlocfilehash: 0afab8c3434aef58c4bb25aee22eefd95732797b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413747"
---
# <a name="round-function-access-custom-web-app"></a><span data-ttu-id="a0468-103">Функция ОКРУГЛ (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="a0468-103">Round Function (Access custom web app)</span></span>

<span data-ttu-id="a0468-104">Возвращает числовое значение, которое округляется или усекается до указанной длины или точности.</span><span class="sxs-lookup"><span data-stu-id="a0468-104">Returns a numeric value, either rounded or truncated, to the specified length or precision.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a0468-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a0468-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="a0468-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="a0468-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a0468-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0468-107">Syntax</span></span>

 <span data-ttu-id="a0468-108">**Round** (*число*, *точность* , [ *трункатеинстеадофраунд* ])</span><span class="sxs-lookup"><span data-stu-id="a0468-108">**Round** (*Number*, *Precision*  , [  *TruncateInsteadOfRound*  ])</span></span> 
  
<span data-ttu-id="a0468-109">Функция **ОКРУГЛ** содержит следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="a0468-109">The **Round** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="a0468-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="a0468-110">**Argument name**</span></span>|<span data-ttu-id="a0468-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a0468-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a0468-112">*Number*</span><span class="sxs-lookup"><span data-stu-id="a0468-112">*Number*</span></span>  <br/> |<span data-ttu-id="a0468-113">Числовое выражение.</span><span class="sxs-lookup"><span data-stu-id="a0468-113">A numeric expression.</span></span>  <br/> |
| <span data-ttu-id="a0468-114">*Точности*</span><span class="sxs-lookup"><span data-stu-id="a0468-114">*Precision*</span></span>  <br/> |<span data-ttu-id="a0468-115">Точность округления *числа* .</span><span class="sxs-lookup"><span data-stu-id="a0468-115">The precision to which  *Number*  is to be rounded.</span></span>  <span data-ttu-id="a0468-116">*Точность* должна быть числовым выражением.</span><span class="sxs-lookup"><span data-stu-id="a0468-116">*Precision*  must be a numeric expression.</span></span> <span data-ttu-id="a0468-117">Если *точность* является положительным числом, то *число* округляется до количества десятичных позиций, заданных по длине.</span><span class="sxs-lookup"><span data-stu-id="a0468-117">When  *Precision*  is a positive number,  *Number*  is rounded to the number of decimal positions specified by length.</span></span> <span data-ttu-id="a0468-118">Если *точность* является отрицательным числом, то *число* округляется в левой части десятичной точки, как указано по значению length.</span><span class="sxs-lookup"><span data-stu-id="a0468-118">When  *Precision*  is a negative number,  *Number*  is rounded on the left side of the decimal point, as specified by length.</span></span>  <br/> |
| <span data-ttu-id="a0468-119">*трункатеинстеадофраунд*</span><span class="sxs-lookup"><span data-stu-id="a0468-119">*TruncateInsteadOfRound*</span></span>  <br/> |<span data-ttu-id="a0468-120">Тип выполняемой операции.</span><span class="sxs-lookup"><span data-stu-id="a0468-120">The type of operation to perform.</span></span> <span data-ttu-id="a0468-121">Если этот параметр опущен или не задано значение 0, то *число* округляется.</span><span class="sxs-lookup"><span data-stu-id="a0468-121">When omitted or set to 0,  *Number*  is rounded.</span></span> <span data-ttu-id="a0468-122">Если указано значение, отличное от 0, *число* усекается.</span><span class="sxs-lookup"><span data-stu-id="a0468-122">When a value other than 0 is specified,  *Number*  is truncated.</span></span> <span data-ttu-id="a0468-123">Значение по умолчанию равно 0.</span><span class="sxs-lookup"><span data-stu-id="a0468-123">The default value is 0.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0468-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="a0468-124">Remarks</span></span>

 <span data-ttu-id="a0468-125">Функция **Round** всегда возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a0468-125">**Round** always returns a value.</span></span> <span data-ttu-id="a0468-126">Если длина имеет отрицательное значение, превышающее количество цифр до запятой, то функция **Round** возвращает 0.</span><span class="sxs-lookup"><span data-stu-id="a0468-126">If length is negative and larger than the number of digits before the decimal point, **Round** returns 0.</span></span> 
  

