---
title: RunDataMacro Macro Action (пользовательское веб-приложение Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f6010ac5-6c08-4c1b-a811-ff81b30ed5f0
description: С помощью действия RunDataMacro можно запустить автономный макрос данных.
ms.openlocfilehash: 68c0e5a3837039bdab1165e686adb3bdf2a5b6f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439347"
---
# <a name="rundatamacro-macro-action-access-custom-web-app"></a><span data-ttu-id="39cda-103">RunDataMacro Macro Action (пользовательское веб-приложение Access)</span><span class="sxs-lookup"><span data-stu-id="39cda-103">RunDataMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="39cda-104">Вы можете использовать действие **RunDataMacro** для запуска макроса автономных данных.</span><span class="sxs-lookup"><span data-stu-id="39cda-104">You can use the **RunDataMacro** action to run a standalone data macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="39cda-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="39cda-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="39cda-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="39cda-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="39cda-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="39cda-107">Setting</span></span>

<span data-ttu-id="39cda-108">Действие **RunDataMacro** имеет следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="39cda-108">The **RunDataMacro** action has the following argument.</span></span> 
  
|<span data-ttu-id="39cda-109">**Аргумент макрокоманды**</span><span class="sxs-lookup"><span data-stu-id="39cda-109">**Action argument**</span></span>|<span data-ttu-id="39cda-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="39cda-110">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="39cda-111">_Имя макроса_</span><span class="sxs-lookup"><span data-stu-id="39cda-111">_Macro Name_</span></span> <br/> |<span data-ttu-id="39cda-112">Имя запускаемого макроса данных.</span><span class="sxs-lookup"><span data-stu-id="39cda-112">The name of the data macro to run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39cda-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="39cda-113">Remarks</span></span>

<span data-ttu-id="39cda-114">При выборе макроса данных, который необходимо запустить в конструкторе макроса, Access определяет, требуются ли для макроса данных параметры.</span><span class="sxs-lookup"><span data-stu-id="39cda-114">When you select the data macro that you want to run in the macro designer, Access determines if the data macro requires parameters.</span></span> <span data-ttu-id="39cda-115">Если макрос данных требует параметров, отображаются текстовые поля, в которых можно ввести аргументы.</span><span class="sxs-lookup"><span data-stu-id="39cda-115">If the data macro requires parameters, text boxes appear where you can type in the arguments.</span></span>
  
<span data-ttu-id="39cda-116">При запуске макроса, который содержит действие **RunDataMacro** и достигает действия **RunDataMacro,** Access запускает называемый макрос данных.</span><span class="sxs-lookup"><span data-stu-id="39cda-116">When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro.</span></span> <span data-ttu-id="39cda-117">После завершения называемого макроса данных Access возвращается к исходному макросу и выполняет следующее действие.</span><span class="sxs-lookup"><span data-stu-id="39cda-117">When the called data macro has finished, Access returns to the original macro and runs the next action.</span></span> 
  

