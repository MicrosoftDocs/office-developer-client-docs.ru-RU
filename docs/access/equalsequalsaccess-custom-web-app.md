---
title: Равно (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70bc707a-3a61-4d75-816d-0defd0806319
description: Проверяет равенство двух выражений.
ms.openlocfilehash: efdd06a1735190d63c13c4df8230e1d29d71c1dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806970"
---
# <a name="equals-access-custom-web-app"></a><span data-ttu-id="e1ebe-103">Равно (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="e1ebe-103">Equals (Access custom web app)</span></span>

<span data-ttu-id="e1ebe-104">Проверяет равенство двух выражений.</span><span class="sxs-lookup"><span data-stu-id="e1ebe-104">Compares the equality of two expressions.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="e1ebe-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="e1ebe-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="e1ebe-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="e1ebe-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e1ebe-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1ebe-107">Syntax</span></span>

`= (Equals)`

<span data-ttu-id="e1ebe-108">*выражение*  =  *выражение*</span><span class="sxs-lookup"><span data-stu-id="e1ebe-108">*expression*  =  *expression*</span></span> 
  
<span data-ttu-id="e1ebe-109">*выражение*  — Это любое допустимое выражение.</span><span class="sxs-lookup"><span data-stu-id="e1ebe-109">*expression*  Is any valid expression.</span></span> <span data-ttu-id="e1ebe-110">Если выражения не представляют тот же тип данных, тип данных для одного выражения должен неявно преобразовываться в тип данных другого.</span><span class="sxs-lookup"><span data-stu-id="e1ebe-110">If the expressions are not of the same data type, the data type for one expression must be implicitly convertible to the data type of the other.</span></span> <span data-ttu-id="e1ebe-111">Преобразование зависит от правил очередности типов данных.</span><span class="sxs-lookup"><span data-stu-id="e1ebe-111">The conversion depends on the rules of data type precedence.</span></span> 
  
## <a name="return-type"></a><span data-ttu-id="e1ebe-112">Возвращаемый тип</span><span class="sxs-lookup"><span data-stu-id="e1ebe-112">Return Type</span></span>

<span data-ttu-id="e1ebe-113">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e1ebe-113">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e1ebe-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="e1ebe-114">Remarks</span></span>

<span data-ttu-id="e1ebe-115">При сравнении двух выражений значение NULL, результатом является значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="e1ebe-115">When you compare two NULL expressions, the result is TRUE.</span></span>
  
<span data-ttu-id="e1ebe-116">Сравнение NULL НЕНУЛЕВОЕ значение всегда дает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="e1ebe-116">Comparing NULL to a non-NULL value always results in FALSE.</span></span>
  

