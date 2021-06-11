---
title: Проверка подлинности на основе форм
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 282b2377-45ba-4f0c-a7d9-830fa3505c93
description: Метод Outlook social Connector (OSC) вызывает метод ISocialProvider::GetCapabilities, чтобы определить возможности поставщика OSC для социальной сети.
ms.openlocfilehash: 420f19a8d7632f2ab9b093eb929ffe879f8a2fc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435532"
---
# <a name="forms-based-authentication"></a><span data-ttu-id="3d77f-103">Проверка подлинности на основе форм</span><span class="sxs-lookup"><span data-stu-id="3d77f-103">Forms-based authentication</span></span>

<span data-ttu-id="3d77f-104">Метод Outlook Social Connector (OSC) вызывает [метод ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) для определения возможностей поставщика OSC для социальной сети.</span><span class="sxs-lookup"><span data-stu-id="3d77f-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="3d77f-105">OsC использует возвращенные возможности, чтобы определить, как поддерживать Office пользователя, входившего в эту социальную сеть.</span><span class="sxs-lookup"><span data-stu-id="3d77f-105">The OSC uses the returned capabilities to determine how to support an Office user who is logging on to this social network.</span></span> 

<span data-ttu-id="3d77f-106">Если элемент **useLogonWebAuth** в возвращенных возможностях **XML** указывает на то, что поставщик OSC поддерживает проверку подлинности на основе форм, OSC может сделать следующую последовательность вызовов, чтобы позволить пользователю войти в эту социальную сеть:</span><span class="sxs-lookup"><span data-stu-id="3d77f-106">If the **useLogonWebAuth** element in the returned **capabilities** XML indicates that the OSC provider supports forms-based authentication, the OSC can make the following calling sequence to allow a user to log on to that social network:</span></span> 
  
1. <span data-ttu-id="3d77f-107">[ISocialProvider::Load](isocialprovider-load.md) &ndash; OsC загружает поставщика.</span><span class="sxs-lookup"><span data-stu-id="3d77f-107">[ISocialProvider::Load](isocialprovider-load.md) &ndash; The OSC loads the provider.</span></span> 
    
2. <span data-ttu-id="3d77f-108">[ISocialProvider::Version](isocialprovider-version.md) &ndash; OsC получает строку, которая представляет номер версии поставщика для этой социальной сети.</span><span class="sxs-lookup"><span data-stu-id="3d77f-108">[ISocialProvider::Version](isocialprovider-version.md) &ndash; The OSC gets a string that represents the version number of the provider for this social network.</span></span> 
    
3. <span data-ttu-id="3d77f-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; OsC получает строку, представляюную имя социальной сети.</span><span class="sxs-lookup"><span data-stu-id="3d77f-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; The OSC gets a string that represents the social network name.</span></span> 
    
4. <span data-ttu-id="3d77f-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; OsC получает неоменяемый GUID, который представляет социальную сеть.</span><span class="sxs-lookup"><span data-stu-id="3d77f-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; The OSC gets an immutable GUID that represents the social network.</span></span> 
    
5. <span data-ttu-id="3d77f-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; OsC получает строку, которая представляет возможности поставщика и соответствует определению схемы элемента **возможностей.**</span><span class="sxs-lookup"><span data-stu-id="3d77f-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; The OSC gets a string that represents the provider's capabilities and that complies with the schema definition for the **capabilities** element.</span></span> 
    
6. <span data-ttu-id="3d77f-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; OsC получает массив byte, который представляет значок для сайта социальной сети.</span><span class="sxs-lookup"><span data-stu-id="3d77f-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; The OSC gets a byte array that represents the icon for the social network site.</span></span> 
    
7. <span data-ttu-id="3d77f-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; OsC получает [интерфейс ISocialSession.](isocialsessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="3d77f-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; The OSC gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
    
8. <span data-ttu-id="3d77f-114">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; OsC инициализирует вход на сайт социальной сети путем проверки подлинности на основе форм.</span><span class="sxs-lookup"><span data-stu-id="3d77f-114">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; The OSC initializes logging on to the social network site by forms-based authentication.</span></span> <span data-ttu-id="3d77f-115">Для этого начального вызова логотипа OSC передает **null** для _параметра connectIn._</span><span class="sxs-lookup"><span data-stu-id="3d77f-115">For this initial logon call, the OSC passes **null** for the  _connectIn_ parameter.</span></span> 
    
9. <span data-ttu-id="3d77f-116">[ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; OsC получает URL-адрес для отображения формы на основе браузера для пользователя во время веб-проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="3d77f-116">[ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; The OSC gets the URL to display a browser-based form to the user during web authentication.</span></span> 
    
10. <span data-ttu-id="3d77f-117">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; OsC завершает логотип на сайте социальной сети с помощью проверки подлинности на основе форм.</span><span class="sxs-lookup"><span data-stu-id="3d77f-117">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; The OSC completes the logon to the social network site by using forms-based authentication.</span></span> <span data-ttu-id="3d77f-118">OsC вызывает этот метод во второй раз, передав URL-адрес формы logon поставщику в _параметре connectIn._</span><span class="sxs-lookup"><span data-stu-id="3d77f-118">The OSC calls this method a second time, passing the URL of the logon form to the provider in the  _connectIn_ parameter.</span></span> 
    
11. <span data-ttu-id="3d77f-119">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; OsC получает интерфейс [ISocialProfile,](isocialprovideriunknown.md) который представляет зарегистрированного пользователя.</span><span class="sxs-lookup"><span data-stu-id="3d77f-119">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; The OSC gets an [ISocialProfile](isocialprovideriunknown.md) interface that represents the logged-on user.</span></span> 
    
12. <span data-ttu-id="3d77f-120">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; OsC получает строку, представляюную уникальный идентификатор для сайта социальной сети.</span><span class="sxs-lookup"><span data-stu-id="3d77f-120">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; The OSC gets a string that represents a unique identifier for a social network site.</span></span> <span data-ttu-id="3d77f-121">Идентификатор сети может быть эквивалентен имени сети.</span><span class="sxs-lookup"><span data-stu-id="3d77f-121">The network identifier can be equivalent to the network name.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="3d77f-122">См. также</span><span class="sxs-lookup"><span data-stu-id="3d77f-122">See also</span></span>

- [<span data-ttu-id="3d77f-123">XML для возможностей</span><span class="sxs-lookup"><span data-stu-id="3d77f-123">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="3d77f-124">Типичные последовательности вызовов OSC</span><span class="sxs-lookup"><span data-stu-id="3d77f-124">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

