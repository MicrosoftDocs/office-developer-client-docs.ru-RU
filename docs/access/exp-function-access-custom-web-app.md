---
title: Функция Exp (Пользовательский доступ к веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09385b75-ec0e-4dde-b9c3-9ade4a7a2b74
description: Возвращает экспоненциальное значение указанного выражения.
ms.openlocfilehash: 30777c41005dfcf1caad896e9e60f0bcfd9d4361
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436414"
---
# <a name="exp-function-access-custom-web-app"></a><span data-ttu-id="7e072-103">Функция Exp (Пользовательский доступ к веб-приложению)</span><span class="sxs-lookup"><span data-stu-id="7e072-103">Exp Function (Access custom web app)</span></span>

<span data-ttu-id="7e072-104">Возвращает экспоненциальное значение указанного выражения.</span><span class="sxs-lookup"><span data-stu-id="7e072-104">Returns the exponential value of the specified expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="7e072-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="7e072-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="7e072-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="7e072-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7e072-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e072-107">Syntax</span></span>

 <span data-ttu-id="7e072-108">**Exp** *(NumericExpression)*</span><span class="sxs-lookup"><span data-stu-id="7e072-108">**Exp** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="7e072-109">Функция **Exp** содержит следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="7e072-109">The **Exp** function contains the following argument.</span></span> 
  
|<span data-ttu-id="7e072-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="7e072-110">**Argument name**</span></span>|<span data-ttu-id="7e072-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7e072-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="7e072-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="7e072-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="7e072-113">Выражение типа Double или типа, который можно неявно преобразовать в Double.</span><span class="sxs-lookup"><span data-stu-id="7e072-113">An expression of type Double or of a type that can be implicitly converted to Double.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e072-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="7e072-114">Remarks</span></span>

<span data-ttu-id="7e072-115">Постоянная **e** (2.718281...), является основой естественных логарифмов.</span><span class="sxs-lookup"><span data-stu-id="7e072-115">The constant **e** (2.718281…), is the base of natural logarithms.</span></span> 
  
<span data-ttu-id="7e072-116">Экспонент номера — это постоянная **электронная** почта, поднимаемая до мощности номера.</span><span class="sxs-lookup"><span data-stu-id="7e072-116">The exponent of a number is the constant **e** raised to the power of the number.</span></span> <span data-ttu-id="7e072-117">Например **Exp** (1.0) = e^1.0 = 2.71828182845905 и **Exp** (10) = e^10 = 22026.4657948067.</span><span class="sxs-lookup"><span data-stu-id="7e072-117">For example **Exp** (1.0) = e^1.0 = 2.71828182845905 and **Exp** (10) = e^10 = 22026.4657948067.</span></span> 
  
<span data-ttu-id="7e072-118">Экспоненциальный показатель естественного логарифма номера — это сам номер: **Exp (log** (n)) = n.</span><span class="sxs-lookup"><span data-stu-id="7e072-118">The exponential of the natural logarithm of a number is the number itself: **Exp** (LOG (n)) = n.</span></span> <span data-ttu-id="7e072-119">И естественным логарифмом экспоненциального числа является сам номер: LOG **(Exp** (n)) = n.</span><span class="sxs-lookup"><span data-stu-id="7e072-119">And the natural logarithm of the exponential of a number is the number itself: LOG (**Exp** (n)) = n.</span></span> 
  

