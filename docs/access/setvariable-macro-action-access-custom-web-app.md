---
title: Макрокоманда Сетвариабле (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: a4ffbd02-eed7-43ed-9da2-f0d1ff5d8014
description: Вы можете использовать действие Сетвариабле, чтобы создать временную переменную и присвоить ей определенное значение. Переменную можно использовать в качестве условия или аргумента в последующих действиях, или можно использовать переменную в другом макросе пользовательского интерфейса.
ms.openlocfilehash: 54c23868a5bfb66a2fb08465361583c6e9b5ed49
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307932"
---
# <a name="setvariable-macro-action-access-custom-web-app"></a><span data-ttu-id="73c5d-104">Макрокоманда Сетвариабле (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="73c5d-104">SetVariable Macro Action (Access custom web app)</span></span>

<span data-ttu-id="73c5d-105">Вы можете использовать действие **сетвариабле** , чтобы создать временную переменную и присвоить ей определенное значение.</span><span class="sxs-lookup"><span data-stu-id="73c5d-105">You can use the **SetVariable** action to create a temporary variable and set it to a specific value.</span></span> <span data-ttu-id="73c5d-106">Переменную можно использовать в качестве условия или аргумента в последующих действиях, или можно использовать переменную в другом макросе пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="73c5d-106">The variable can then be used as a condition or argument in subsequent actions, or you can use the variable in another user interface (UI) macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="73c5d-107">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="73c5d-107">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="73c5d-108">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="73c5d-108">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="73c5d-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="73c5d-109">Setting</span></span>

<span data-ttu-id="73c5d-110">Макрокоманда **сетвариабле** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="73c5d-110">The **SetVariable** action has the following arguments.</span></span> 
  
|<span data-ttu-id="73c5d-111">**Аргумент макрокоманды**</span><span class="sxs-lookup"><span data-stu-id="73c5d-111">**Action argument**</span></span>|<span data-ttu-id="73c5d-112">**Описание**</span><span class="sxs-lookup"><span data-stu-id="73c5d-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="73c5d-113">**Переменная**</span><span class="sxs-lookup"><span data-stu-id="73c5d-113">**Variable**</span></span> <br/> |<span data-ttu-id="73c5d-114">Введите имя временной переменной.</span><span class="sxs-lookup"><span data-stu-id="73c5d-114">Enter the name of the temporary variable.</span></span>  <br/> |
|<span data-ttu-id="73c5d-115">**Значение =**</span><span class="sxs-lookup"><span data-stu-id="73c5d-115">**Value =**</span></span> <br/> |<span data-ttu-id="73c5d-116">Введите выражение, которое будет использоваться для задания значения для этой временной переменной.</span><span class="sxs-lookup"><span data-stu-id="73c5d-116">Enter an expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="73c5d-117">Не ставьте перед выражением знак равенства (**=** ).</span><span class="sxs-lookup"><span data-stu-id="73c5d-117">Do not precede the expression with the equal (**=** ) sign.</span></span> <span data-ttu-id="73c5d-118">Чтобы использовать поСтроитель выражений для ![]задания этого аргумента, можно нажать(media/buildbut_ZA06047218.gif "формулу") с формулой для кнопки **построить** .</span><span class="sxs-lookup"><span data-stu-id="73c5d-118">You can click the **Build** button ![Formula](media/buildbut_ZA06047218.gif "Formula") to use the Expression Builder to set this argument.</span></span>  <br/> |
   

