---
title: Регистрация поставщика
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: В этом разделе описываются разделах реестра Windows, которые используются при установке поставщика Outlook Social Connector (OSC).
ms.openlocfilehash: 3ec594ec94b045d2ceb583144781a5746b945b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812829"
---
# <a name="registering-a-provider"></a><span data-ttu-id="5e0be-103">Регистрация поставщика</span><span class="sxs-lookup"><span data-stu-id="5e0be-103">Registering a provider</span></span>

<span data-ttu-id="5e0be-104">В этом разделе описываются разделах реестра Windows, которые используются при установке поставщика Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="5e0be-104">This topic describes the Windows registry locations that are used when you install an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="com-registration"></a><span data-ttu-id="5e0be-105">Регистрация COM</span><span class="sxs-lookup"><span data-stu-id="5e0be-105">COM registration</span></span>

<span data-ttu-id="5e0be-106">Необходимо настроить поставщика OSC DLL-Библиотеку для регистрации с помощью COM самостоятельной регистрации или regsvr32 во время установки.</span><span class="sxs-lookup"><span data-stu-id="5e0be-106">You must configure the OSC provider DLL to register using COM self-registration or regsvr32 during installation.</span></span> <span data-ttu-id="5e0be-107">Регистрация COM DLL-Библиотеки поставщика регистрируется поставщик OSC в разделе `HKEY_CLASSES_ROOT` куст реестра.</span><span class="sxs-lookup"><span data-stu-id="5e0be-107">COM registration of the provider DLL registers the OSC provider under the `HKEY_CLASSES_ROOT` registry hive.</span></span> 
  
<span data-ttu-id="5e0be-108">Поставщика OSC, разработанных в управляемом коде имеет COM-видимым сборки поставщика.</span><span class="sxs-lookup"><span data-stu-id="5e0be-108">An OSC provider developed in managed code has a COM-visible provider assembly.</span></span> <span data-ttu-id="5e0be-109">Следует использовать отдельного домена приложений для компонента поставщика.</span><span class="sxs-lookup"><span data-stu-id="5e0be-109">You should use a separate application domain for the provider component.</span></span> <span data-ttu-id="5e0be-110">В противном случае поставщика OSC использует домен общего приложения по умолчанию, используемый с другими компонентами и поставщик может не работать нормально.</span><span class="sxs-lookup"><span data-stu-id="5e0be-110">Otherwise, the OSC provider uses the default shared application domain that is used by other components, and the provider may not operate as expected.</span></span>
  
## <a name="registering-provider-progid"></a><span data-ttu-id="5e0be-111">Регистрация поставщика ProgID</span><span class="sxs-lookup"><span data-stu-id="5e0be-111">Registering provider ProgID</span></span>

<span data-ttu-id="5e0be-112">Каждый поставщик OSC необходимо зарегистрировать программный идентификатор (`ProgID`).</span><span class="sxs-lookup"><span data-stu-id="5e0be-112">Each OSC provider must register a programmatic identifier (`ProgID`).</span></span> <span data-ttu-id="5e0be-113">Установщик поставщика можно выбрать один из следующих расположений для добавления или удаления `ProgID`:</span><span class="sxs-lookup"><span data-stu-id="5e0be-113">The provider installer can choose one of the following locations to add or remove the `ProgID`:</span></span>
  
- <span data-ttu-id="5e0be-114">`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Установщик поставщика следует использовать это расположение, если поставщик устанавливается только для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="5e0be-114">`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` &ndash; Your provider installer should use this location if the provider is installed for only the currently logged-on user.</span></span>
    
- <span data-ttu-id="5e0be-115">`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Установщик поставщика следует использовать это расположение поставщик в случае установки для всех пользователей на компьютере.</span><span class="sxs-lookup"><span data-stu-id="5e0be-115">`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` &ndash; Your provider installer should use this location if the provider is installed for all users on the computer.</span></span>
    
<span data-ttu-id="5e0be-116">Находит поставщика OSC `ProgID` в вышеуказанных местах, только при наличии 32-разрядная версия Outlook при работе на 64-разрядной операционной системы Windows на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="5e0be-116">The OSC looks for the provider  `ProgID` in the above locations, unless the client computer has 32-bit Outlook running on a 64-bit Windows operating system.</span></span> <span data-ttu-id="5e0be-117">В этом случае установщик поставщик должен выбрать один из следующих расположений в `HKEY_CURRENT_USER` или `HKEY_LOCAL_MACHINE` куст:</span><span class="sxs-lookup"><span data-stu-id="5e0be-117">In such a case, your provider installer should choose one of the following locations in the  `HKEY_CURRENT_USER` or  `HKEY_LOCAL_MACHINE` hive:</span></span> 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
<span data-ttu-id="5e0be-118">Click-to-Run версии системы Office установщик поставщик должен выбрать один из следующих расположений в кусте HKEY_CURRENT_USER или HKEY_LOCAL_MACHINE:</span><span class="sxs-lookup"><span data-stu-id="5e0be-118">For a Click-to-Run version of Office, your provider installer should choose one of the following locations in the HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE hive:</span></span>
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a><span data-ttu-id="5e0be-119">См. также</span><span class="sxs-lookup"><span data-stu-id="5e0be-119">See also</span></span>

- [<span data-ttu-id="5e0be-120">Контрольный список установки</span><span class="sxs-lookup"><span data-stu-id="5e0be-120">Installation Checklist</span></span>](installation-checklist.md)
- [<span data-ttu-id="5e0be-121">Быстрый шаги, необходимые для разработки поставщика</span><span class="sxs-lookup"><span data-stu-id="5e0be-121">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="5e0be-122">Развертывание поставщика</span><span class="sxs-lookup"><span data-stu-id="5e0be-122">Deploying a Provider</span></span>](deploying-a-provider.md)

