---
title: Макрос ЗапускМакроса (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 59ba365d-cff5-4126-bc22-4d5a37578aab
description: ЗапускМакроса можно использовать для запуска макроса пользовательского интерфейса (UI).
ms.openlocfilehash: 68a59e246c0af8385a17aedcf3da771c720f8fd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807108"
---
# <a name="runmacro-macro-action-access-custom-web-app"></a><span data-ttu-id="26d85-103">Макрос ЗапускМакроса (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="26d85-103">RunMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="26d85-104">**ЗапускМакроса** можно использовать для запуска макроса пользовательского интерфейса (UI).</span><span class="sxs-lookup"><span data-stu-id="26d85-104">You can use the **RunMacro** action to run a user interface (UI) macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="26d85-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="26d85-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="26d85-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="26d85-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="26d85-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="26d85-107">Setting</span></span>

<span data-ttu-id="26d85-108">**ЗапускМакроса** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="26d85-108">The **RunMacro** action has the following arguments.</span></span> 
  
|<span data-ttu-id="26d85-109">**Аргумент действия**</span><span class="sxs-lookup"><span data-stu-id="26d85-109">**Action argument**</span></span>|<span data-ttu-id="26d85-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="26d85-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="26d85-111">**Имя макроса**</span><span class="sxs-lookup"><span data-stu-id="26d85-111">**Macro Name**</span></span> <br/> |<span data-ttu-id="26d85-112">Имя макроса для запуска пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="26d85-112">The name of the UI macro to run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26d85-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="26d85-113">Remarks</span></span>

<span data-ttu-id="26d85-114">Если макрос пользовательского интерфейса, содержащий **ЗапускМакроса** достигает **ЗапускМакроса** , Access запускает называемое макрос пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="26d85-114">When you run a UI macro containing the **RunMacro** action, and it reaches the **RunMacro** action, Access runs the called UI macro.</span></span> <span data-ttu-id="26d85-115">По завершении называемое макрос пользовательского интерфейса Access возвращает исходное макрос пользовательского интерфейса и выполняется следующее действие.</span><span class="sxs-lookup"><span data-stu-id="26d85-115">When the called UI macro has finished, Access returns to the original UI macro and runs the next action.</span></span> 
  

