---
title: Регистрация поставщика
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: В этом разделе описываются расположения реестра Windows, используемые при установке поставщика Outlook Social Connector (OSC).
ms.openlocfilehash: a5f76850f9bebcba3c2bff31e799a3b012d6b91a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421762"
---
# <a name="registering-a-provider"></a><span data-ttu-id="6ec3e-103">Регистрация поставщика</span><span class="sxs-lookup"><span data-stu-id="6ec3e-103">Registering a provider</span></span>

<span data-ttu-id="6ec3e-104">В этом разделе описываются расположения реестра Windows, используемые при установке поставщика Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="6ec3e-104">This topic describes the Windows registry locations that are used when you install an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="com-registration"></a><span data-ttu-id="6ec3e-105">Регистрация COM</span><span class="sxs-lookup"><span data-stu-id="6ec3e-105">COM registration</span></span>

<span data-ttu-id="6ec3e-106">Необходимо настроить БИБЛИОТЕКУ DLL поставщика OSC для регистрации с помощью функции самостоятельной регистрации COM или regsvr32 во время установки.</span><span class="sxs-lookup"><span data-stu-id="6ec3e-106">You must configure the OSC provider DLL to register using COM self-registration or regsvr32 during installation.</span></span> <span data-ttu-id="6ec3e-107">Регистрация в COM для библиотеки DLL поставщика регистрирует поставщика OSC в кусте `HKEY_CLASSES_ROOT` реестра.</span><span class="sxs-lookup"><span data-stu-id="6ec3e-107">COM registration of the provider DLL registers the OSC provider under the `HKEY_CLASSES_ROOT` registry hive.</span></span> 
  
<span data-ttu-id="6ec3e-108">Поставщик OSC, разработанный в управляемом коде, имеет сборку поставщика, видимую для COM.</span><span class="sxs-lookup"><span data-stu-id="6ec3e-108">An OSC provider developed in managed code has a COM-visible provider assembly.</span></span> <span data-ttu-id="6ec3e-109">Для компонента поставщика следует использовать отдельный домен приложения.</span><span class="sxs-lookup"><span data-stu-id="6ec3e-109">You should use a separate application domain for the provider component.</span></span> <span data-ttu-id="6ec3e-110">В противном случае поставщик OSC использует общий домен приложения по умолчанию, который используется другими компонентами, и поставщик может работать не так, как ожидалось.</span><span class="sxs-lookup"><span data-stu-id="6ec3e-110">Otherwise, the OSC provider uses the default shared application domain that is used by other components, and the provider may not operate as expected.</span></span>
  
## <a name="registering-provider-progid"></a><span data-ttu-id="6ec3e-111">Регистрация ProgID поставщика</span><span class="sxs-lookup"><span data-stu-id="6ec3e-111">Registering provider ProgID</span></span>

<span data-ttu-id="6ec3e-112">Каждый поставщик OSC должен зарегистрировать программный идентификатор (`ProgID`).</span><span class="sxs-lookup"><span data-stu-id="6ec3e-112">Each OSC provider must register a programmatic identifier (`ProgID`).</span></span> <span data-ttu-id="6ec3e-113">Установщик поставщика может выбрать одно из следующих расположений, `ProgID`чтобы добавить или удалить:</span><span class="sxs-lookup"><span data-stu-id="6ec3e-113">The provider installer can choose one of the following locations to add or remove the `ProgID`:</span></span>
  
- <span data-ttu-id="6ec3e-114">`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Установщик поставщика должен использовать это расположение, если поставщик установлен только для пользователя, выполнившего вход в систему.</span><span class="sxs-lookup"><span data-stu-id="6ec3e-114">`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` &ndash; Your provider installer should use this location if the provider is installed for only the currently logged-on user.</span></span>
    
- <span data-ttu-id="6ec3e-115">`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Установщик поставщика должен использовать это расположение, если поставщик установлен для всех пользователей компьютера.</span><span class="sxs-lookup"><span data-stu-id="6ec3e-115">`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` &ndash; Your provider installer should use this location if the provider is installed for all users on the computer.</span></span>
    
<span data-ttu-id="6ec3e-116">OSC ищет поставщика `ProgID` в указанных выше расположениях, если на клиентском компьютере не установлено приложение 32 (в том случае, если на нем работает приложение в 64 — более разрядная версия операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="6ec3e-116">The OSC looks for the provider  `ProgID` in the above locations, unless the client computer has 32-bit Outlook running on a 64-bit Windows operating system.</span></span> <span data-ttu-id="6ec3e-117">В этом случае установщик поставщика должен выбрать одно из следующих расположений в кусте `HKEY_CURRENT_USER` или `HKEY_LOCAL_MACHINE` кусте:</span><span class="sxs-lookup"><span data-stu-id="6ec3e-117">In such a case, your provider installer should choose one of the following locations in the  `HKEY_CURRENT_USER` or  `HKEY_LOCAL_MACHINE` hive:</span></span> 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
<span data-ttu-id="6ec3e-118">Для версии Office "нажми и работай" установщик поставщика должен выбрать одно из следующих расположений в кусте HKEY_CURRENT_USER или HKEY_LOCAL_MACHINE:</span><span class="sxs-lookup"><span data-stu-id="6ec3e-118">For a Click-to-Run version of Office, your provider installer should choose one of the following locations in the HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE hive:</span></span>
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a><span data-ttu-id="6ec3e-119">См. также</span><span class="sxs-lookup"><span data-stu-id="6ec3e-119">See also</span></span>

- [<span data-ttu-id="6ec3e-120">Контрольный список установки</span><span class="sxs-lookup"><span data-stu-id="6ec3e-120">Installation Checklist</span></span>](installation-checklist.md)
- [<span data-ttu-id="6ec3e-121">Быстрые действия для изучения разработки поставщика</span><span class="sxs-lookup"><span data-stu-id="6ec3e-121">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="6ec3e-122">Развертывание поставщика</span><span class="sxs-lookup"><span data-stu-id="6ec3e-122">Deploying a Provider</span></span>](deploying-a-provider.md)

