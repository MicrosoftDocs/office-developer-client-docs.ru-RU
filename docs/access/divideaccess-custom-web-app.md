---
title: / (Деление) (пользовательское веб-приложение Access)
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
# <a name="-divide-access-custom-web-app"></a><span data-ttu-id="e3a7d-103">/ (Деление) (пользовательское веб-приложение Access)</span><span class="sxs-lookup"><span data-stu-id="e3a7d-103">/ (Divide) (Access custom web app)</span></span>

<span data-ttu-id="e3a7d-104">Делит одно число на другое.</span><span class="sxs-lookup"><span data-stu-id="e3a7d-104">Divides one number by another.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="e3a7d-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="e3a7d-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="e3a7d-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="e3a7d-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e3a7d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3a7d-107">Syntax</span></span>

 <span data-ttu-id="e3a7d-108">*2016*   /   *divisor*</span><span class="sxs-lookup"><span data-stu-id="e3a7d-108">*dividend*  /  *divisor*</span></span> 
  
 <span data-ttu-id="e3a7d-109">*2016*  Является ли числовое выражение для деление.</span><span class="sxs-lookup"><span data-stu-id="e3a7d-109">*dividend*  Is the numeric expression to divide.</span></span> <span data-ttu-id="e3a7d-110">Может быть любым допустимым выражением любого из типов данных категории числовых типов данных, кроме типа данных даты и времени.</span><span class="sxs-lookup"><span data-stu-id="e3a7d-110">Can be any valid expression of any one of the data types of the numeric data type category, except the datetime data type.</span></span> 
  
 <span data-ttu-id="e3a7d-111">*Дивизор*  Является числовом выражением, по которому делится расчисть.</span><span class="sxs-lookup"><span data-stu-id="e3a7d-111">*Divisor*  Is the numeric expression by which to divide the dividend.</span></span> <span data-ttu-id="e3a7d-112">Может быть любым допустимым выражением любого из типов данных категории числовых типов данных, кроме типа данных даты и времени.</span><span class="sxs-lookup"><span data-stu-id="e3a7d-112">Can be any valid expression of any one of the data types of the numeric data type category, except the datetime data type.</span></span> 
  
## <a name="return-type"></a><span data-ttu-id="e3a7d-113">Возвращаемый тип</span><span class="sxs-lookup"><span data-stu-id="e3a7d-113">Return Type</span></span>

<span data-ttu-id="e3a7d-114">Возвращает тип данных аргумента с более высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="e3a7d-114">Returns the data type of the argument with the higher precedence.</span></span> 
  
<span data-ttu-id="e3a7d-115">Если дробная  часть результата разделена на  дробную часть, то результатом будет любое дробное.</span><span class="sxs-lookup"><span data-stu-id="e3a7d-115">If an integer  *dividend*  is divided by an integer  *divisor*  , the result is an integer that has any fractional part of the result truncated.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e3a7d-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="e3a7d-116">Remarks</span></span>

<span data-ttu-id="e3a7d-117">Фактическое значение, возвращаемое оператором /, — это кворум первого выражения, разделенного на второе выражение.</span><span class="sxs-lookup"><span data-stu-id="e3a7d-117">The actual value returned by the / operator is the quotient of the first expression divided by the second expression.</span></span>
  

