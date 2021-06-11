---
title: / (Разделяй) (Доступ к настраиваемой веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3d296730-197b-44db-853b-881597dd9b48
description: Делит один номер на другой.
ms.openlocfilehash: 48d43b224743949f86c5d206d9919a9e2d6fbcae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435189"
---
# <a name="-divide-access-custom-web-app"></a><span data-ttu-id="cef40-103">/ (Разделяй) (Доступ к настраиваемой веб-приложению)</span><span class="sxs-lookup"><span data-stu-id="cef40-103">/ (Divide) (Access custom web app)</span></span>

<span data-ttu-id="cef40-104">Делит один номер на другой.</span><span class="sxs-lookup"><span data-stu-id="cef40-104">Divides one number by another.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="cef40-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="cef40-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="cef40-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="cef40-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="cef40-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cef40-107">Syntax</span></span>

 <span data-ttu-id="cef40-108">*дивиденды*   /   *divisor*</span><span class="sxs-lookup"><span data-stu-id="cef40-108">*dividend*  /  *divisor*</span></span> 
  
 <span data-ttu-id="cef40-109">*дивиденды*  Является ли числовая выражение разделяемой.</span><span class="sxs-lookup"><span data-stu-id="cef40-109">*dividend*  Is the numeric expression to divide.</span></span> <span data-ttu-id="cef40-110">Может быть любым допустимым выражением любого из типов данных категории числовых типов данных, за исключением типа данных даты.</span><span class="sxs-lookup"><span data-stu-id="cef40-110">Can be any valid expression of any one of the data types of the numeric data type category, except the datetime data type.</span></span> 
  
 <span data-ttu-id="cef40-111">*Divisor*  Это числовая выражение, с помощью которого можно разделить дивиденды.</span><span class="sxs-lookup"><span data-stu-id="cef40-111">*Divisor*  Is the numeric expression by which to divide the dividend.</span></span> <span data-ttu-id="cef40-112">Может быть любым допустимым выражением любого из типов данных категории числовых типов данных, за исключением типа данных даты.</span><span class="sxs-lookup"><span data-stu-id="cef40-112">Can be any valid expression of any one of the data types of the numeric data type category, except the datetime data type.</span></span> 
  
## <a name="return-type"></a><span data-ttu-id="cef40-113">Возвращаемый тип</span><span class="sxs-lookup"><span data-stu-id="cef40-113">Return Type</span></span>

<span data-ttu-id="cef40-114">Возвращает тип данных аргумента с более высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="cef40-114">Returns the data type of the argument with the higher precedence.</span></span> 
  
<span data-ttu-id="cef40-115">Если дивиденды  на несколько этапов делятся  на разделителем, то в результате будет отсечена часть результата.</span><span class="sxs-lookup"><span data-stu-id="cef40-115">If an integer  *dividend*  is divided by an integer  *divisor*  , the result is an integer that has any fractional part of the result truncated.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cef40-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="cef40-116">Remarks</span></span>

<span data-ttu-id="cef40-117">Фактическое значение, возвращаемое оператором, — это коэффициент первого выражения, разделенного вторым выражением.</span><span class="sxs-lookup"><span data-stu-id="cef40-117">The actual value returned by the / operator is the quotient of the first expression divided by the second expression.</span></span>
  

