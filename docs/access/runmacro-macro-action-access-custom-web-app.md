---
title: Макрокоманда ЗапускМакроса (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 59ba365d-cff5-4126-bc22-4d5a37578aab
description: Макрокоманду ЗапускМакроса можно использовать для запуска макроса пользовательского интерфейса.
ms.openlocfilehash: 98e3b17a6c64fa12ac37e4551d45714c873f5ccb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307968"
---
# <a name="runmacro-macro-action-access-custom-web-app"></a><span data-ttu-id="0cd97-103">Макрокоманда ЗапускМакроса (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="0cd97-103">RunMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="0cd97-104">Макрокоманду **ЗапускМакроса** можно использовать для запуска макроса пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0cd97-104">You can use the **RunMacro** action to run a user interface (UI) macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="0cd97-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="0cd97-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="0cd97-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="0cd97-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="0cd97-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="0cd97-107">Setting</span></span>

<span data-ttu-id="0cd97-108">Макрокоманда **ЗапускМакроса** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="0cd97-108">The **RunMacro** action has the following arguments.</span></span> 
  
|<span data-ttu-id="0cd97-109">**Аргумент макрокоманды**</span><span class="sxs-lookup"><span data-stu-id="0cd97-109">**Action argument**</span></span>|<span data-ttu-id="0cd97-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0cd97-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0cd97-111">**Имя макроса**</span><span class="sxs-lookup"><span data-stu-id="0cd97-111">**Macro Name**</span></span> <br/> |<span data-ttu-id="0cd97-112">Имя макроса ПОЛЬЗОВАТЕЛЬСКОГО интерфейса, который необходимо запустить.</span><span class="sxs-lookup"><span data-stu-id="0cd97-112">The name of the UI macro to run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0cd97-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="0cd97-113">Remarks</span></span>

<span data-ttu-id="0cd97-114">При запуске макроса ПОЛЬЗОВАТЕЛЬСКОГО интерфейса, содержащего макрокоманду **ЗапускМакроса** , и достижении макрокоманды **ЗапускМакроса** вызывается макрос пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0cd97-114">When you run a UI macro containing the **RunMacro** action, and it reaches the **RunMacro** action, Access runs the called UI macro.</span></span> <span data-ttu-id="0cd97-115">После завершения вызванного макроса ПОЛЬЗОВАТЕЛЬСКОГО интерфейса Access возвращается к исходному макросу ПОЛЬЗОВАТЕЛЬСКОГО интерфейса и выполняет следующее действие.</span><span class="sxs-lookup"><span data-stu-id="0cd97-115">When the called UI macro has finished, Access returns to the original UI macro and runs the next action.</span></span> 
  

