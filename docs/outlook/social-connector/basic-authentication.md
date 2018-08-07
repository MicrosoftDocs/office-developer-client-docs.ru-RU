---
title: Обычная проверка подлинности
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89349d1e-365a-442e-9ba3-2df601d9323c
description: Outlook Social Connector (OSC) вызывает метод ISocialProvider::GetCapabilities, чтобы определить возможности поставщика OSC для социальных сетей.
ms.openlocfilehash: 8287133445a4e8fa928f6b7724ab41ca9b58baf9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812732"
---
# <a name="basic-authentication"></a><span data-ttu-id="427e8-103">Обычная проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="427e8-103">Basic authentication</span></span>

<span data-ttu-id="427e8-104">Outlook Social Connector (OSC) вызывает метод [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) , чтобы определить возможности поставщика OSC для социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="427e8-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="427e8-105">OSC используется возвращенные возможностей, чтобы определить, как обеспечить поддержку для Office пользователя, вошедшего в этом социальной сети.</span><span class="sxs-lookup"><span data-stu-id="427e8-105">The OSC uses the returned capabilities to determine how to support an Office user who is logging on to this social network.</span></span> <span data-ttu-id="427e8-106">Если элемент **useLogonWebAuth** в возвращенные **возможности** XML указывает, что поставщика OSC поддерживает обычную проверку подлинности, OSC можно внести следующие последовательность вызова разрешать пользователям войти в этой социальной сети:</span><span class="sxs-lookup"><span data-stu-id="427e8-106">If the **useLogonWebAuth** element in the returned **capabilities** XML indicates that the OSC provider supports basic authentication, the OSC can make the following calling sequence to allow a user to log on to that social network:</span></span> 
  
1. <span data-ttu-id="427e8-107">[ISocialProvider::Load](isocialprovider-load.md) — OSC загружает поставщика.</span><span class="sxs-lookup"><span data-stu-id="427e8-107">[ISocialProvider::Load](isocialprovider-load.md) —The OSC loads the provider.</span></span> 
    
2. <span data-ttu-id="427e8-108">[ISocialProvider::Version](isocialprovider-version.md) — OSC возвращает строку, представляющую номер версии поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="427e8-108">[ISocialProvider::Version](isocialprovider-version.md) —The OSC gets a string that represents the version number of the OSC provider.</span></span> 
    
3. <span data-ttu-id="427e8-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) — OSC возвращает строку, представляющую имя социальной сети.</span><span class="sxs-lookup"><span data-stu-id="427e8-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) —The OSC gets a string that represents the social network name.</span></span> 
    
4. <span data-ttu-id="427e8-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) — OSC получает постоянные GUID, который представляет социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="427e8-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) —The OSC gets an immutable GUID that represents the social network.</span></span> 
    
5. <span data-ttu-id="427e8-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) — OSC возвращает строку, которая представляет возможности поставщика, который соответствует определение схемы для элемента **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="427e8-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) —The OSC gets a string that represents the provider's capabilities and that complies with the schema definition for the **capabilities** element.</span></span> 
    
6. <span data-ttu-id="427e8-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) — OSC возвращает массив байтов, который представляет значок для узла социальной сети.</span><span class="sxs-lookup"><span data-stu-id="427e8-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) —The OSC gets a byte array that represents the icon for the social network site.</span></span> 
    
7. <span data-ttu-id="427e8-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) — OSC получает интерфейс [ISocialSession](isocialsessioniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="427e8-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) —The OSC gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
    
8. <span data-ttu-id="427e8-114">[ISocialSession::Logon](isocialsession-logon.md) — OSC входа пользователя на узел социальной сети с помощью указанного имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="427e8-114">[ISocialSession::Logon](isocialsession-logon.md) —The OSC logs the user on to the social network site by using the specified user name and password.</span></span> 
    
9. <span data-ttu-id="427e8-115">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) — OSC получает [ISocialProfile](isocialprovideriunknown.md) интерфейс, который представляет текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="427e8-115">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) —The OSC gets an [ISocialProfile](isocialprovideriunknown.md) interface that represents the logged-on user.</span></span> 
    
10. <span data-ttu-id="427e8-116">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) — OSC возвращает строку, представляющую уникальный идентификатор для сайтов социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="427e8-116">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) —The OSC gets a string that represents a unique identifier for a social network site.</span></span> <span data-ttu-id="427e8-117">Идентификатор сети могут быть эквивалентно сетевое имя.</span><span class="sxs-lookup"><span data-stu-id="427e8-117">The network identifier can be equivalent to the network name.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="427e8-118">См. также</span><span class="sxs-lookup"><span data-stu-id="427e8-118">See also</span></span>

- [<span data-ttu-id="427e8-119">XML-код для возможности</span><span class="sxs-lookup"><span data-stu-id="427e8-119">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="427e8-120">Типичные последовательности вызовов OSC</span><span class="sxs-lookup"><span data-stu-id="427e8-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

