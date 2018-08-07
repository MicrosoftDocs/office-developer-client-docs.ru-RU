---
title: Больше или равно (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cceb8dcb-5ce1-4c32-b057-6201b62a646f
description: Сравнение двух выражений для больше или равно.
ms.openlocfilehash: 425745d8634f92e3bcce3cbfcd7d11a890e3be4b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806948"
---
# <a name="greater-than-or-equal-to-access-custom-web-app"></a><span data-ttu-id="88773-103">Больше или равно (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="88773-103">Greater Than or Equal To (Access custom web app)</span></span>

<span data-ttu-id="88773-104">Сравнение двух выражений для больше или равно.</span><span class="sxs-lookup"><span data-stu-id="88773-104">Compares two expressions for greater than or equal.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="88773-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="88773-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="88773-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="88773-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="88773-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88773-107">Syntax</span></span>

`>= (Greater Than or Equal To)`

<span data-ttu-id="88773-108">*выражение*  \>=  *выражение*</span><span class="sxs-lookup"><span data-stu-id="88773-108">*expression*  \>=  *expression*</span></span> 
  
<span data-ttu-id="88773-109">*выражение*  — Это любое допустимое выражение.</span><span class="sxs-lookup"><span data-stu-id="88773-109">*expression*  Is any valid expression.</span></span> <span data-ttu-id="88773-110">Оба выражения должны иметь данные неявно преобразуемых типов.</span><span class="sxs-lookup"><span data-stu-id="88773-110">Both expressions must have implicitly convertible data types.</span></span> <span data-ttu-id="88773-111">Преобразование зависит от правил очередности типов данных.</span><span class="sxs-lookup"><span data-stu-id="88773-111">The conversion depends on the rules of data type precedence.</span></span> 
  
## <a name="return-type"></a><span data-ttu-id="88773-112">Возвращаемый тип</span><span class="sxs-lookup"><span data-stu-id="88773-112">Return Type</span></span>

<span data-ttu-id="88773-113">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="88773-113">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="88773-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="88773-114">Remarks</span></span>

<span data-ttu-id="88773-115">При сравнении выражений, не являющееся null, результатом является значение TRUE, если левого операнда большее или равное значению правого операнда; в противном случае результатом является значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="88773-115">When you compare non-null expressions, the result is TRUE if the left operand has a greater or equal value than the right operand; otherwise, the result is FALSE.</span></span>
  

