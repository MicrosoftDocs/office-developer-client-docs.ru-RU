---
title: Функция EXP (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09385b75-ec0e-4dde-b9c3-9ade4a7a2b74
description: Возвращает значение экспоненты указанного выражения.
ms.openlocfilehash: 9c4929a25da6a8eec5984f9e9a1a6695a049614d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806935"
---
# <a name="exp-function-access-custom-web-app"></a><span data-ttu-id="6f51f-103">Функция EXP (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="6f51f-103">Exp Function (Access custom web app)</span></span>

<span data-ttu-id="6f51f-104">Возвращает значение экспоненты указанного выражения.</span><span class="sxs-lookup"><span data-stu-id="6f51f-104">Returns the exponential value of the specified expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="6f51f-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6f51f-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="6f51f-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="6f51f-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6f51f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f51f-107">Syntax</span></span>

 <span data-ttu-id="6f51f-108">**Exp** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="6f51f-108">**Exp** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="6f51f-109">Функция **Exp** содержит следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="6f51f-109">The **Exp** function contains the following argument.</span></span> 
  
|<span data-ttu-id="6f51f-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="6f51f-110">**Argument name**</span></span>|<span data-ttu-id="6f51f-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6f51f-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6f51f-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="6f51f-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="6f51f-113">Выражение типа Double или типа, который можно неявно преобразовать в Double.</span><span class="sxs-lookup"><span data-stu-id="6f51f-113">An expression of type Double or of a type that can be implicitly converted to Double.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f51f-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="6f51f-114">Remarks</span></span>

<span data-ttu-id="6f51f-115">Константа **e** (2,718281...), — это основание натуральных логарифмов.</span><span class="sxs-lookup"><span data-stu-id="6f51f-115">The constant **e** (2.718281…), is the base of natural logarithms.</span></span> 
  
<span data-ttu-id="6f51f-116">Экспоненты числа — константа **e** , возведенное в степень номера телефона.</span><span class="sxs-lookup"><span data-stu-id="6f51f-116">The exponent of a number is the constant **e** raised to the power of the number.</span></span> <span data-ttu-id="6f51f-117">Например **Exp** (1.0) = e ^ 1.0 = 2,71828182845905 и **Exp** (10) = e ^ 10 = 22026.4657948067.</span><span class="sxs-lookup"><span data-stu-id="6f51f-117">For example **Exp** (1.0) = e^1.0 = 2.71828182845905 and **Exp** (10) = e^10 = 22026.4657948067.</span></span> 
  
<span data-ttu-id="6f51f-118">Экспонента натурального логарифма от числа — номер самого: **Exp** (LOG (n)) = n.</span><span class="sxs-lookup"><span data-stu-id="6f51f-118">The exponential of the natural logarithm of a number is the number itself: **Exp** (LOG (n)) = n.</span></span> <span data-ttu-id="6f51f-119">И натуральный логарифм экспоненты числа — номер самого: ЖУРНАЛА (**Exp** (n)) = n.</span><span class="sxs-lookup"><span data-stu-id="6f51f-119">And the natural logarithm of the exponential of a number is the number itself: LOG (**Exp** (n)) = n.</span></span> 
  

