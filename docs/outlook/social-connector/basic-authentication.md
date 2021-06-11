---
title: Обычная проверка подлинности
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89349d1e-365a-442e-9ba3-2df601d9323c
description: Метод Outlook social Connector (OSC) вызывает метод ISocialProvider::GetCapabilities, чтобы определить возможности поставщика OSC для социальной сети.
ms.openlocfilehash: 7f716df3ef2e82712374ce3d775cdf66eb07e8b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439928"
---
# <a name="basic-authentication"></a><span data-ttu-id="76eff-103">Обычная проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="76eff-103">Basic authentication</span></span>

<span data-ttu-id="76eff-104">Метод Outlook Social Connector (OSC) вызывает [метод ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) для определения возможностей поставщика OSC для социальной сети.</span><span class="sxs-lookup"><span data-stu-id="76eff-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="76eff-105">OsC использует возвращенные возможности, чтобы определить, как поддерживать Office пользователя, входившего в эту социальную сеть.</span><span class="sxs-lookup"><span data-stu-id="76eff-105">The OSC uses the returned capabilities to determine how to support an Office user who is logging on to this social network.</span></span> <span data-ttu-id="76eff-106">Если элемент **useLogonWebAuth** в возвращенных возможностях **XML** указывает, что поставщик OSC поддерживает базовую проверку подлинности, OSC может сделать следующую последовательность вызовов, чтобы позволить пользователю войти в эту социальную сеть:</span><span class="sxs-lookup"><span data-stu-id="76eff-106">If the **useLogonWebAuth** element in the returned **capabilities** XML indicates that the OSC provider supports basic authentication, the OSC can make the following calling sequence to allow a user to log on to that social network:</span></span> 
  
1. <span data-ttu-id="76eff-107">[ISocialProvider::Load](isocialprovider-load.md) — OSC загружает поставщика.</span><span class="sxs-lookup"><span data-stu-id="76eff-107">[ISocialProvider::Load](isocialprovider-load.md) —The OSC loads the provider.</span></span> 
    
2. <span data-ttu-id="76eff-108">[ISocialProvider::Version](isocialprovider-version.md) — OSC получает строку, представляюную номер версии поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="76eff-108">[ISocialProvider::Version](isocialprovider-version.md) —The OSC gets a string that represents the version number of the OSC provider.</span></span> 
    
3. <span data-ttu-id="76eff-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) — OSC получает строку, представляюную имя социальной сети.</span><span class="sxs-lookup"><span data-stu-id="76eff-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) —The OSC gets a string that represents the social network name.</span></span> 
    
4. <span data-ttu-id="76eff-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) — OSC получает неизменяемый GUID, который представляет социальную сеть.</span><span class="sxs-lookup"><span data-stu-id="76eff-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) —The OSC gets an immutable GUID that represents the social network.</span></span> 
    
5. <span data-ttu-id="76eff-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) — OSC получает строку, которая представляет возможности поставщика и соответствует определению схемы элемента **возможностей.**</span><span class="sxs-lookup"><span data-stu-id="76eff-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) —The OSC gets a string that represents the provider's capabilities and that complies with the schema definition for the **capabilities** element.</span></span> 
    
6. <span data-ttu-id="76eff-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) — OSC получает массив byte, представляючий значок для сайта социальной сети.</span><span class="sxs-lookup"><span data-stu-id="76eff-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) —The OSC gets a byte array that represents the icon for the social network site.</span></span> 
    
7. <span data-ttu-id="76eff-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) — OSC получает [интерфейс ISocialSession.](isocialsessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="76eff-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) —The OSC gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
    
8. <span data-ttu-id="76eff-114">[ISocialSession::Logon](isocialsession-logon.md) — OSC регистрирует пользователя на сайте социальной сети с помощью указанного имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="76eff-114">[ISocialSession::Logon](isocialsession-logon.md) —The OSC logs the user on to the social network site by using the specified user name and password.</span></span> 
    
9. <span data-ttu-id="76eff-115">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) — OSC получает [интерфейс ISocialProfile,](isocialprovideriunknown.md) который представляет зарегистрированного пользователя.</span><span class="sxs-lookup"><span data-stu-id="76eff-115">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) —The OSC gets an [ISocialProfile](isocialprovideriunknown.md) interface that represents the logged-on user.</span></span> 
    
10. <span data-ttu-id="76eff-116">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) — OSC получает строку, представляюную уникальный идентификатор для сайта социальной сети.</span><span class="sxs-lookup"><span data-stu-id="76eff-116">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) —The OSC gets a string that represents a unique identifier for a social network site.</span></span> <span data-ttu-id="76eff-117">Идентификатор сети может быть эквивалентен имени сети.</span><span class="sxs-lookup"><span data-stu-id="76eff-117">The network identifier can be equivalent to the network name.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="76eff-118">См. также</span><span class="sxs-lookup"><span data-stu-id="76eff-118">See also</span></span>

- [<span data-ttu-id="76eff-119">XML для возможностей</span><span class="sxs-lookup"><span data-stu-id="76eff-119">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="76eff-120">Типичные последовательности вызовов OSC</span><span class="sxs-lookup"><span data-stu-id="76eff-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

