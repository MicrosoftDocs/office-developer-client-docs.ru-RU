---
title: Проверка подлинности на основе форм
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 282b2377-45ba-4f0c-a7d9-830fa3505c93
description: Outlook Social Connector (OSC) вызывает метод ISocialProvider::GetCapabilities, чтобы определить возможности поставщика OSC для социальных сетей.
ms.openlocfilehash: bf6534b72af7db92e02bed74f2028a086b26cbcf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812720"
---
# <a name="forms-based-authentication"></a><span data-ttu-id="119c0-103">Проверка подлинности на основе форм</span><span class="sxs-lookup"><span data-stu-id="119c0-103">Forms-based authentication</span></span>

<span data-ttu-id="119c0-104">Outlook Social Connector (OSC) вызывает метод [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) , чтобы определить возможности поставщика OSC для социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="119c0-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="119c0-105">OSC используется возвращенные возможностей, чтобы определить, как обеспечить поддержку для Office пользователя, вошедшего в этом социальной сети.</span><span class="sxs-lookup"><span data-stu-id="119c0-105">The OSC uses the returned capabilities to determine how to support an Office user who is logging on to this social network.</span></span> 

<span data-ttu-id="119c0-106">Если элемент **useLogonWebAuth** в возвращенные **возможности** XML указывает, что поставщик OSC поддерживает проверку подлинности на основе форм, OSC можно внести следующие последовательность вызова разрешать пользователям войти в этой социальной сети:</span><span class="sxs-lookup"><span data-stu-id="119c0-106">If the **useLogonWebAuth** element in the returned **capabilities** XML indicates that the OSC provider supports forms-based authentication, the OSC can make the following calling sequence to allow a user to log on to that social network:</span></span> 
  
1. <span data-ttu-id="119c0-107">[ISocialProvider::Load](isocialprovider-load.md) &ndash; OSC загружает поставщика.</span><span class="sxs-lookup"><span data-stu-id="119c0-107">[ISocialProvider::Load](isocialprovider-load.md) &ndash; The OSC loads the provider.</span></span> 
    
2. <span data-ttu-id="119c0-108">[ISocialProvider::Version](isocialprovider-version.md) &ndash; OSC возвращает строку, представляющую номер версии поставщика для этой социальной сети.</span><span class="sxs-lookup"><span data-stu-id="119c0-108">[ISocialProvider::Version](isocialprovider-version.md) &ndash; The OSC gets a string that represents the version number of the provider for this social network.</span></span> 
    
3. <span data-ttu-id="119c0-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; OSC возвращает строку, представляющую имя социальной сети.</span><span class="sxs-lookup"><span data-stu-id="119c0-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; The OSC gets a string that represents the social network name.</span></span> 
    
4. <span data-ttu-id="119c0-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; OSC получает постоянные GUID, который представляет социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="119c0-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; The OSC gets an immutable GUID that represents the social network.</span></span> 
    
5. <span data-ttu-id="119c0-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; OSC возвращает строку, которая представляет возможности поставщика, который соответствует определение схемы для элемента **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="119c0-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; The OSC gets a string that represents the provider's capabilities and that complies with the schema definition for the **capabilities** element.</span></span> 
    
6. <span data-ttu-id="119c0-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; OSC возвращает массив байтов, который представляет значок для узла социальной сети.</span><span class="sxs-lookup"><span data-stu-id="119c0-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; The OSC gets a byte array that represents the icon for the social network site.</span></span> 
    
7. <span data-ttu-id="119c0-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; OSC получает интерфейс [ISocialSession](isocialsessioniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="119c0-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; The OSC gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
    
8. <span data-ttu-id="119c0-114">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; OSC инициализирует выполнение входа на сайт социальных сетей, проверки подлинности на основе форм.</span><span class="sxs-lookup"><span data-stu-id="119c0-114">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; The OSC initializes logging on to the social network site by forms-based authentication.</span></span> <span data-ttu-id="119c0-115">Для этого вызова начальное входа OSC передает **значение null** для параметра _connectIn_ .</span><span class="sxs-lookup"><span data-stu-id="119c0-115">For this initial logon call, the OSC passes **null** for the  _connectIn_ parameter.</span></span> 
    
9. <span data-ttu-id="119c0-116">[ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; OSC получает URL-адрес для отображения формы на основе браузера для пользователя в ходе проверки подлинности web.</span><span class="sxs-lookup"><span data-stu-id="119c0-116">[ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; The OSC gets the URL to display a browser-based form to the user during web authentication.</span></span> 
    
10. <span data-ttu-id="119c0-117">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; OSC завершает входа на сайт социальной сети с помощью проверки подлинности на основе форм.</span><span class="sxs-lookup"><span data-stu-id="119c0-117">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; The OSC completes the logon to the social network site by using forms-based authentication.</span></span> <span data-ttu-id="119c0-118">OSC вызывает этот метод еще раз, передав URL-адрес формы входа в систему для поставщика с помощью параметра _connectIn_ .</span><span class="sxs-lookup"><span data-stu-id="119c0-118">The OSC calls this method a second time, passing the URL of the logon form to the provider in the  _connectIn_ parameter.</span></span> 
    
11. <span data-ttu-id="119c0-119">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; OSC получает [ISocialProfile](isocialprovideriunknown.md) интерфейс, который представляет текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="119c0-119">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; The OSC gets an [ISocialProfile](isocialprovideriunknown.md) interface that represents the logged-on user.</span></span> 
    
12. <span data-ttu-id="119c0-120">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; OSC возвращает строку, представляющую уникальный идентификатор для сайтов социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="119c0-120">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; The OSC gets a string that represents a unique identifier for a social network site.</span></span> <span data-ttu-id="119c0-121">Идентификатор сети могут быть эквивалентно сетевое имя.</span><span class="sxs-lookup"><span data-stu-id="119c0-121">The network identifier can be equivalent to the network name.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="119c0-122">См. также</span><span class="sxs-lookup"><span data-stu-id="119c0-122">See also</span></span>

- [<span data-ttu-id="119c0-123">XML-код для возможности</span><span class="sxs-lookup"><span data-stu-id="119c0-123">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="119c0-124">Типичные последовательности вызовов OSC</span><span class="sxs-lookup"><span data-stu-id="119c0-124">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

