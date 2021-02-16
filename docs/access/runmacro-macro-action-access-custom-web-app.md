---
title: RunMacro Macro Action (пользовательское веб-приложение Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 59ba365d-cff5-4126-bc22-4d5a37578aab
description: Макрос пользовательского интерфейса можно использовать для запуска макроса RunMacro.
ms.openlocfilehash: 98e3b17a6c64fa12ac37e4551d45714c873f5ccb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438444"
---
# <a name="runmacro-macro-action-access-custom-web-app"></a><span data-ttu-id="8eb25-103">RunMacro Macro Action (пользовательское веб-приложение Access)</span><span class="sxs-lookup"><span data-stu-id="8eb25-103">RunMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="8eb25-104">Макрос пользовательского интерфейса можно использовать для запуска макроса **RunMacro.**</span><span class="sxs-lookup"><span data-stu-id="8eb25-104">You can use the **RunMacro** action to run a user interface (UI) macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="8eb25-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="8eb25-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="8eb25-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="8eb25-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="8eb25-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="8eb25-107">Setting</span></span>

<span data-ttu-id="8eb25-108">Действие **RunMacro** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="8eb25-108">The **RunMacro** action has the following arguments.</span></span> 
  
|<span data-ttu-id="8eb25-109">**Аргумент макрокоманды**</span><span class="sxs-lookup"><span data-stu-id="8eb25-109">**Action argument**</span></span>|<span data-ttu-id="8eb25-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8eb25-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8eb25-111">**Имя макроса**</span><span class="sxs-lookup"><span data-stu-id="8eb25-111">**Macro Name**</span></span> <br/> |<span data-ttu-id="8eb25-112">Имя запускаемого макроса пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8eb25-112">The name of the UI macro to run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8eb25-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="8eb25-113">Remarks</span></span>

<span data-ttu-id="8eb25-114">Когда вы запускаете макрос пользовательского интерфейса, содержащий действие **RunMacro,** и оно достигает действия **RunMacro,** Access запускает называемый макрос пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8eb25-114">When you run a UI macro containing the **RunMacro** action, and it reaches the **RunMacro** action, Access runs the called UI macro.</span></span> <span data-ttu-id="8eb25-115">После завершения называемого макроса пользовательского интерфейса Access возвращается к исходному макросу пользовательского интерфейса и выполняет следующее действие.</span><span class="sxs-lookup"><span data-stu-id="8eb25-115">When the called UI macro has finished, Access returns to the original UI macro and runs the next action.</span></span> 
  

