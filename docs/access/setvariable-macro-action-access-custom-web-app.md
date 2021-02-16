---
title: SetVariable Macro Action (пользовательское веб-приложение Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: a4ffbd02-eed7-43ed-9da2-f0d1ff5d8014
description: С помощью действия SetVariable можно создать временную переменную и установить для нее определенное значение. Затем переменную можно использовать в качестве условия или аргумента в последующих действиях, или можно использовать переменную в другом макросе пользовательского интерфейса.
ms.openlocfilehash: 54c23868a5bfb66a2fb08465361583c6e9b5ed49
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433922"
---
# <a name="setvariable-macro-action-access-custom-web-app"></a><span data-ttu-id="5c3a4-104">SetVariable Macro Action (пользовательское веб-приложение Access)</span><span class="sxs-lookup"><span data-stu-id="5c3a4-104">SetVariable Macro Action (Access custom web app)</span></span>

<span data-ttu-id="5c3a4-105">С помощью действия **SetVariable** можно создать временную переменную и установить для нее определенное значение.</span><span class="sxs-lookup"><span data-stu-id="5c3a4-105">You can use the **SetVariable** action to create a temporary variable and set it to a specific value.</span></span> <span data-ttu-id="5c3a4-106">Затем переменную можно использовать в качестве условия или аргумента в последующих действиях, или можно использовать переменную в другом макросе пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5c3a4-106">The variable can then be used as a condition or argument in subsequent actions, or you can use the variable in another user interface (UI) macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="5c3a4-107">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5c3a4-107">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="5c3a4-108">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="5c3a4-108">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="5c3a4-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="5c3a4-109">Setting</span></span>

<span data-ttu-id="5c3a4-110">Действие **SetVariable** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="5c3a4-110">The **SetVariable** action has the following arguments.</span></span> 
  
|<span data-ttu-id="5c3a4-111">**Аргумент макрокоманды**</span><span class="sxs-lookup"><span data-stu-id="5c3a4-111">**Action argument**</span></span>|<span data-ttu-id="5c3a4-112">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5c3a4-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5c3a4-113">**Переменная**</span><span class="sxs-lookup"><span data-stu-id="5c3a4-113">**Variable**</span></span> <br/> |<span data-ttu-id="5c3a4-114">Введите имя временной переменной.</span><span class="sxs-lookup"><span data-stu-id="5c3a4-114">Enter the name of the temporary variable.</span></span>  <br/> |
|<span data-ttu-id="5c3a4-115">**Значение =**</span><span class="sxs-lookup"><span data-stu-id="5c3a4-115">**Value =**</span></span> <br/> |<span data-ttu-id="5c3a4-116">Введите выражение, которое будет использоваться для ввода значения для этой временной переменной.</span><span class="sxs-lookup"><span data-stu-id="5c3a4-116">Enter an expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="5c3a4-117">Не запишите перед выражением знак "равно" **=** ().</span><span class="sxs-lookup"><span data-stu-id="5c3a4-117">Do not precede the expression with the equal (**=** ) sign.</span></span> <span data-ttu-id="5c3a4-118">Вы можете нажать **кнопку** !["Формула](media/buildbut_ZA06047218.gif "построения\",") чтобы использовать построитель выражений для этого аргумента.</span><span class="sxs-lookup"><span data-stu-id="5c3a4-118">You can click the **Build** button ![Formula](media/buildbut_ZA06047218.gif "Formula") to use the Expression Builder to set this argument.</span></span>  <br/> |
   

