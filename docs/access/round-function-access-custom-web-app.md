---
title: Функция Round (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4af7fbe2-ee34-4a52-b55e-ce3983313b5e
description: Возвращает числовое значение, округленное или сокращается до указанной длины или точности.
ms.openlocfilehash: 5a3df4a4ddd7aace5edf886db5988704e5dd6af3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807112"
---
# <a name="round-function-access-custom-web-app"></a><span data-ttu-id="2605f-103">Функция Round (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="2605f-103">Round Function (Access custom web app)</span></span>

<span data-ttu-id="2605f-104">Возвращает числовое значение, округленное или сокращается до указанной длины или точности.</span><span class="sxs-lookup"><span data-stu-id="2605f-104">Returns a numeric value, either rounded or truncated, to the specified length or precision.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="2605f-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="2605f-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="2605f-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="2605f-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2605f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2605f-107">Syntax</span></span>

 <span data-ttu-id="2605f-108">**Round** (*Номер*, *точности* [ *TruncateInsteadOfRound* ])</span><span class="sxs-lookup"><span data-stu-id="2605f-108">**Round** (*Number*, *Precision*  , [  *TruncateInsteadOfRound*  ])</span></span> 
  
<span data-ttu-id="2605f-109">Функция **Round** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="2605f-109">The **Round** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="2605f-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="2605f-110">**Argument name**</span></span>|<span data-ttu-id="2605f-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2605f-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2605f-112">*Число*</span><span class="sxs-lookup"><span data-stu-id="2605f-112">*Number*</span></span>  <br/> |<span data-ttu-id="2605f-113">Числовое выражение.</span><span class="sxs-lookup"><span data-stu-id="2605f-113">A numeric expression.</span></span>  <br/> |
| <span data-ttu-id="2605f-114">*Точность*</span><span class="sxs-lookup"><span data-stu-id="2605f-114">*Precision*</span></span>  <br/> |<span data-ttu-id="2605f-115">Точность, к которым будет округлено *номер* .</span><span class="sxs-lookup"><span data-stu-id="2605f-115">The precision to which  *Number*  is to be rounded.</span></span>  <span data-ttu-id="2605f-116">*Точность* должна быть числовое выражение.</span><span class="sxs-lookup"><span data-stu-id="2605f-116">*Precision*  must be a numeric expression.</span></span> <span data-ttu-id="2605f-117">Когда *точности* — это положительное число, *число* округляется до число десятичных знаков заданной длины.</span><span class="sxs-lookup"><span data-stu-id="2605f-117">When  *Precision*  is a positive number,  *Number*  is rounded to the number of decimal positions specified by length.</span></span> <span data-ttu-id="2605f-118">*Когда *точности* отрицательное значение, оно округляется слева от десятичной запятой, как указано в длину.*</span><span class="sxs-lookup"><span data-stu-id="2605f-118">When  *Precision*  is a negative number,  *Number*  is rounded on the left side of the decimal point, as specified by length.</span></span>  <br/> |
| <span data-ttu-id="2605f-119">*TruncateInsteadOfRound*</span><span class="sxs-lookup"><span data-stu-id="2605f-119">*TruncateInsteadOfRound*</span></span>  <br/> |<span data-ttu-id="2605f-120">Тип операции для выполнения.</span><span class="sxs-lookup"><span data-stu-id="2605f-120">The type of operation to perform.</span></span> <span data-ttu-id="2605f-121">Когда опускается, или значение 0, *число* округляется.</span><span class="sxs-lookup"><span data-stu-id="2605f-121">When omitted or set to 0,  *Number*  is rounded.</span></span> <span data-ttu-id="2605f-122">*Если указано значение, отличное от 0, оно округляется.*</span><span class="sxs-lookup"><span data-stu-id="2605f-122">When a value other than 0 is specified,  *Number*  is truncated.</span></span> <span data-ttu-id="2605f-123">Значение по умолчанию равно 0.</span><span class="sxs-lookup"><span data-stu-id="2605f-123">The default value is 0.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2605f-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="2605f-124">Remarks</span></span>

 <span data-ttu-id="2605f-125">**Round** всегда возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2605f-125">**Round** always returns a value.</span></span> <span data-ttu-id="2605f-126">Если длина отрицательные и больше, чем количество цифр перед десятичной запятой, **Round** возвращает 0.</span><span class="sxs-lookup"><span data-stu-id="2605f-126">If length is negative and larger than the number of digits before the decimal point, **Round** returns 0.</span></span> 
  

