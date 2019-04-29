---
title: /(Деление) (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3d296730-197b-44db-853b-881597dd9b48
description: Делит одно число на другое.
ms.openlocfilehash: 48d43b224743949f86c5d206d9919a9e2d6fbcae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435189"
---
# <a name="-divide-access-custom-web-app"></a><span data-ttu-id="594b9-103">/(Деление) (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="594b9-103">/ (Divide) (Access custom web app)</span></span>

<span data-ttu-id="594b9-104">Делит одно число на другое.</span><span class="sxs-lookup"><span data-stu-id="594b9-104">Divides one number by another.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="594b9-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="594b9-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="594b9-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="594b9-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="594b9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="594b9-107">Syntax</span></span>

 <span data-ttu-id="594b9-108">*Делимое*  /  *делитель*</span><span class="sxs-lookup"><span data-stu-id="594b9-108">*dividend*  /  *divisor*</span></span> 
  
 <span data-ttu-id="594b9-109">*делимое* (делимое)  — Числовое выражение, которое необходимо разделить.</span><span class="sxs-lookup"><span data-stu-id="594b9-109">*dividend*  Is the numeric expression to divide.</span></span> <span data-ttu-id="594b9-110">Может быть любым допустимым выражением любого типа данных категории числового типа данных, кроме типа данных DateTime.</span><span class="sxs-lookup"><span data-stu-id="594b9-110">Can be any valid expression of any one of the data types of the numeric data type category, except the datetime data type.</span></span> 
  
 <span data-ttu-id="594b9-111">*Делитель*  Числовое выражение, используемое для деления делимого.</span><span class="sxs-lookup"><span data-stu-id="594b9-111">*Divisor*  Is the numeric expression by which to divide the dividend.</span></span> <span data-ttu-id="594b9-112">Может быть любым допустимым выражением любого типа данных категории числового типа данных, кроме типа данных DateTime.</span><span class="sxs-lookup"><span data-stu-id="594b9-112">Can be any valid expression of any one of the data types of the numeric data type category, except the datetime data type.</span></span> 
  
## <a name="return-type"></a><span data-ttu-id="594b9-113">Возвращаемый тип</span><span class="sxs-lookup"><span data-stu-id="594b9-113">Return Type</span></span>

<span data-ttu-id="594b9-114">Возвращает тип данных аргумента с более высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="594b9-114">Returns the data type of the argument with the higher precedence.</span></span> 
  
<span data-ttu-id="594b9-115">Если целочисленный *делимый* делится на целый *делитель* , результатом является целое число, которое содержит дробную часть результата.</span><span class="sxs-lookup"><span data-stu-id="594b9-115">If an integer  *dividend*  is divided by an integer  *divisor*  , the result is an integer that has any fractional part of the result truncated.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="594b9-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="594b9-116">Remarks</span></span>

<span data-ttu-id="594b9-117">Фактические значения, возвращаемые оператором/, являются частными первого выражения, разделенного вторым выражением.</span><span class="sxs-lookup"><span data-stu-id="594b9-117">The actual value returned by the / operator is the quotient of the first expression divided by the second expression.</span></span>
  

