---
title: / (Разделить) (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3d296730-197b-44db-853b-881597dd9b48
description: Делит одно число на другое.
ms.openlocfilehash: fd5ce0f26d6ea03f14103cd76779a95ca8a34b1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806973"
---
# <a name="-divide-access-custom-web-app"></a><span data-ttu-id="c6790-103">/ (Разделить) (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="c6790-103">/ (Divide) (Access custom web app)</span></span>

<span data-ttu-id="c6790-104">Делит одно число на другое.</span><span class="sxs-lookup"><span data-stu-id="c6790-104">Divides one number by another.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="c6790-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="c6790-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="c6790-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="c6790-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c6790-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6790-107">Syntax</span></span>

 <span data-ttu-id="c6790-108">*дивидендов*  /  *делителя*</span><span class="sxs-lookup"><span data-stu-id="c6790-108">*dividend*  /  *divisor*</span></span> 
  
 <span data-ttu-id="c6790-109">*дивидендов*  — Числовое выражение для деления.</span><span class="sxs-lookup"><span data-stu-id="c6790-109">*dividend*  Is the numeric expression to divide.</span></span> <span data-ttu-id="c6790-110">Может быть любым допустимым выражением одного типа данных из категории числовых типов данных, за исключением тип данных даты и времени.</span><span class="sxs-lookup"><span data-stu-id="c6790-110">Can be any valid expression of any one of the data types of the numeric data type category, except the datetime data type.</span></span> 
  
 <span data-ttu-id="c6790-111">*Делителя*  — Числовое выражение для деления дивидендов.</span><span class="sxs-lookup"><span data-stu-id="c6790-111">*Divisor*  Is the numeric expression by which to divide the dividend.</span></span> <span data-ttu-id="c6790-112">Может быть любым допустимым выражением одного типа данных из категории числовых типов данных, за исключением тип данных даты и времени.</span><span class="sxs-lookup"><span data-stu-id="c6790-112">Can be any valid expression of any one of the data types of the numeric data type category, except the datetime data type.</span></span> 
  
## <a name="return-type"></a><span data-ttu-id="c6790-113">Возвращаемый тип</span><span class="sxs-lookup"><span data-stu-id="c6790-113">Return Type</span></span>

<span data-ttu-id="c6790-114">Возвращает тип данных аргумента с более высокий приоритет.</span><span class="sxs-lookup"><span data-stu-id="c6790-114">Returns the data type of the argument with the higher precedence.</span></span> 
  
<span data-ttu-id="c6790-115">Если целое число *дивидендов* на целый *делителя* , результатом является целое число, имеет дробная часть результат усечено.</span><span class="sxs-lookup"><span data-stu-id="c6790-115">If an integer  *dividend*  is divided by an integer  *divisor*  , the result is an integer that has any fractional part of the result truncated.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c6790-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="c6790-116">Remarks</span></span>

<span data-ttu-id="c6790-117">Фактическое значение, возвращаемое аудио- и оператор — частное от деления первого выражения на второе выражение.</span><span class="sxs-lookup"><span data-stu-id="c6790-117">The actual value returned by the / operator is the quotient of the first expression divided by the second expression.</span></span>
  

