---
title: Действия Макрос RunMacro (Доступ к настраиваемой веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 59ba365d-cff5-4126-bc22-4d5a37578aab
description: Вы можете использовать действие RunMacro для запуска макроса пользовательского интерфейса (пользовательского интерфейса).
ms.openlocfilehash: 98e3b17a6c64fa12ac37e4551d45714c873f5ccb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438444"
---
# <a name="runmacro-macro-action-access-custom-web-app"></a><span data-ttu-id="1e5f2-103">Действия Макрос RunMacro (Доступ к настраиваемой веб-приложению)</span><span class="sxs-lookup"><span data-stu-id="1e5f2-103">RunMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="1e5f2-104">Вы можете использовать **действие RunMacro** для запуска макроса пользовательского интерфейса (пользовательского интерфейса).</span><span class="sxs-lookup"><span data-stu-id="1e5f2-104">You can use the **RunMacro** action to run a user interface (UI) macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="1e5f2-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="1e5f2-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="1e5f2-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="1e5f2-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="1e5f2-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="1e5f2-107">Setting</span></span>

<span data-ttu-id="1e5f2-108">Действие **RunMacro** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="1e5f2-108">The **RunMacro** action has the following arguments.</span></span> 
  
|<span data-ttu-id="1e5f2-109">**Аргумент макрокоманды**</span><span class="sxs-lookup"><span data-stu-id="1e5f2-109">**Action argument**</span></span>|<span data-ttu-id="1e5f2-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1e5f2-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1e5f2-111">**Имя макроса**</span><span class="sxs-lookup"><span data-stu-id="1e5f2-111">**Macro Name**</span></span> <br/> |<span data-ttu-id="1e5f2-112">Имя макроса пользовательского интерфейса для запуска.</span><span class="sxs-lookup"><span data-stu-id="1e5f2-112">The name of the UI macro to run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e5f2-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="1e5f2-113">Remarks</span></span>

<span data-ttu-id="1e5f2-114">При запуске макроса пользовательского интерфейса, содержащего действие **RunMacro** и достигаемого действия **RunMacro,** Access запускает называемый макрос пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="1e5f2-114">When you run a UI macro containing the **RunMacro** action, and it reaches the **RunMacro** action, Access runs the called UI macro.</span></span> <span data-ttu-id="1e5f2-115">После завершения так называемого макроса пользовательского интерфейса Access возвращается к исходному макросу пользовательского интерфейса и выполняет следующее действие.</span><span class="sxs-lookup"><span data-stu-id="1e5f2-115">When the called UI macro has finished, Access returns to the original UI macro and runs the next action.</span></span> 
  

