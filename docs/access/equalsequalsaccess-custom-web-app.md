---
title: Equals (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70bc707a-3a61-4d75-816d-0defd0806319
description: Сравнивает равенство двух выражений.
ms.openlocfilehash: 8c551e3dbc057433b49bc2558e08feba5ee3d04f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308227"
---
# <a name="equals-access-custom-web-app"></a><span data-ttu-id="bd36b-103">Equals (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="bd36b-103">Equals (Access custom web app)</span></span>

<span data-ttu-id="bd36b-104">Сравнивает равенство двух выражений.</span><span class="sxs-lookup"><span data-stu-id="bd36b-104">Compares the equality of two expressions.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="bd36b-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="bd36b-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="bd36b-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="bd36b-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="bd36b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bd36b-107">Syntax</span></span>

`= (Equals)`

<span data-ttu-id="bd36b-108">\*\*  =  *выражение* выражения</span><span class="sxs-lookup"><span data-stu-id="bd36b-108">*expression*  =  *expression*</span></span> 
  
<span data-ttu-id="bd36b-109">*expression* — любое допустимое выражение.</span><span class="sxs-lookup"><span data-stu-id="bd36b-109">*expression*  Is any valid expression.</span></span> <span data-ttu-id="bd36b-110">Если выражения относятся к одному и тому же типу данных, то тип данных для одного выражения должен быть неявно преобразуемым к типу данных другого.</span><span class="sxs-lookup"><span data-stu-id="bd36b-110">If the expressions are not of the same data type, the data type for one expression must be implicitly convertible to the data type of the other.</span></span> <span data-ttu-id="bd36b-111">Преобразование зависит от правил приоритета для типов данных.</span><span class="sxs-lookup"><span data-stu-id="bd36b-111">The conversion depends on the rules of data type precedence.</span></span> 
  
## <a name="return-type"></a><span data-ttu-id="bd36b-112">Возвращаемый тип</span><span class="sxs-lookup"><span data-stu-id="bd36b-112">Return Type</span></span>

<span data-ttu-id="bd36b-113">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="bd36b-113">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bd36b-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="bd36b-114">Remarks</span></span>

<span data-ttu-id="bd36b-115">При сравнении двух выражений NULL результат будет иметь значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="bd36b-115">When you compare two NULL expressions, the result is TRUE.</span></span>
  
<span data-ttu-id="bd36b-116">При сравнении значения NULL со значением, отличным от NULL, всегда получается значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="bd36b-116">Comparing NULL to a non-NULL value always results in FALSE.</span></span>
  

