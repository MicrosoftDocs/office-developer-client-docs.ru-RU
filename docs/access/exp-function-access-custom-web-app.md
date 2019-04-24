---
title: Функция EXP (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09385b75-ec0e-4dde-b9c3-9ade4a7a2b74
description: Возвращает экспоненциальное значение указанного выражения.
ms.openlocfilehash: 30777c41005dfcf1caad896e9e60f0bcfd9d4361
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308199"
---
# <a name="exp-function-access-custom-web-app"></a><span data-ttu-id="10c8c-103">Функция EXP (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="10c8c-103">Exp Function (Access custom web app)</span></span>

<span data-ttu-id="10c8c-104">Возвращает экспоненциальное значение указанного выражения.</span><span class="sxs-lookup"><span data-stu-id="10c8c-104">Returns the exponential value of the specified expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="10c8c-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="10c8c-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="10c8c-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="10c8c-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="10c8c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10c8c-107">Syntax</span></span>

 <span data-ttu-id="10c8c-108">**Exp** (*Нумерицекспрессион*)</span><span class="sxs-lookup"><span data-stu-id="10c8c-108">**Exp** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="10c8c-109">Функция **exp** содержит следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="10c8c-109">The **Exp** function contains the following argument.</span></span> 
  
|<span data-ttu-id="10c8c-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="10c8c-110">**Argument name**</span></span>|<span data-ttu-id="10c8c-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="10c8c-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="10c8c-112">*Нумерицекспрессион*</span><span class="sxs-lookup"><span data-stu-id="10c8c-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="10c8c-113">Выражение типа Double или типа, который может быть неявно преобразован в Double.</span><span class="sxs-lookup"><span data-stu-id="10c8c-113">An expression of type Double or of a type that can be implicitly converted to Double.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10c8c-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="10c8c-114">Remarks</span></span>

<span data-ttu-id="10c8c-115">Константа **e** (2,718281...) — это основание натуральных логарифмов.</span><span class="sxs-lookup"><span data-stu-id="10c8c-115">The constant **e** (2.718281…), is the base of natural logarithms.</span></span> 
  
<span data-ttu-id="10c8c-116">Экспонента числа — это константа **e** , возведенная в степень числа.</span><span class="sxs-lookup"><span data-stu-id="10c8c-116">The exponent of a number is the constant **e** raised to the power of the number.</span></span> <span data-ttu-id="10c8c-117">Например, **exp** (1,0) = e ^ 1.0 = 2.71828182845905 и **exp** (10) = e ^ 10 = 22026.4657948067.</span><span class="sxs-lookup"><span data-stu-id="10c8c-117">For example **Exp** (1.0) = e^1.0 = 2.71828182845905 and **Exp** (10) = e^10 = 22026.4657948067.</span></span> 
  
<span data-ttu-id="10c8c-118">Экспонента натурального логарифма числа — это само число: **exp** (log (n)) = n.</span><span class="sxs-lookup"><span data-stu-id="10c8c-118">The exponential of the natural logarithm of a number is the number itself: **Exp** (LOG (n)) = n.</span></span> <span data-ttu-id="10c8c-119">Натуральный логарифм экспоненты числа — это само число: LOG (**exp** (n)) = n.</span><span class="sxs-lookup"><span data-stu-id="10c8c-119">And the natural logarithm of the exponential of a number is the number itself: LOG (**Exp** (n)) = n.</span></span> 
  

