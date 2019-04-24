---
title: Проверка подлинности на основе форм
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 282b2377-45ba-4f0c-a7d9-830fa3505c93
description: 'Outlook Social Connector (OSC) вызывает метод ИсоЦиалпровидер:: capabilities, который определяет возможности поставщика OSC для социальной сети.'
ms.openlocfilehash: 420f19a8d7632f2ab9b093eb929ffe879f8a2fc2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280992"
---
# <a name="forms-based-authentication"></a><span data-ttu-id="204c4-103">Проверка подлинности на основе форм</span><span class="sxs-lookup"><span data-stu-id="204c4-103">Forms-based authentication</span></span>

<span data-ttu-id="204c4-104">Outlook Social Connector (OSC) вызывает метод [исоЦиалпровидер:: Capabilities](isocialprovider-getcapabilities.md) , который определяет возможности поставщика OSC для социальной сети.</span><span class="sxs-lookup"><span data-stu-id="204c4-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="204c4-105">Для определения способа поддержки пользователя Office, который выполняет вход в эту социальную сеть, OSC использует возвращенные возможности.</span><span class="sxs-lookup"><span data-stu-id="204c4-105">The OSC uses the returned capabilities to determine how to support an Office user who is logging on to this social network.</span></span> 

<span data-ttu-id="204c4-106">Если элемент **уселогонвебаус** в возвращенном XML-файле **возможностей** указывает на то, что поставщик OSC поддерживает проверку подлинности на основе форм, OSC может выполнить следующую последовательность вызовов, чтобы разрешить пользователю входить в эту социальную сеть:</span><span class="sxs-lookup"><span data-stu-id="204c4-106">If the **useLogonWebAuth** element in the returned **capabilities** XML indicates that the OSC provider supports forms-based authentication, the OSC can make the following calling sequence to allow a user to log on to that social network:</span></span> 
  
1. <span data-ttu-id="204c4-107">[ИсоЦиалпровидер:: Load](isocialprovider-load.md) &ndash; OSC загружает поставщика.</span><span class="sxs-lookup"><span data-stu-id="204c4-107">[ISocialProvider::Load](isocialprovider-load.md) &ndash; The OSC loads the provider.</span></span> 
    
2. <span data-ttu-id="204c4-108">[ИсоЦиалпровидер:: версия](isocialprovider-version.md) &ndash; OSC возвращает строку, представляющую номер версии поставщика для этой социальной сети.</span><span class="sxs-lookup"><span data-stu-id="204c4-108">[ISocialProvider::Version](isocialprovider-version.md) &ndash; The OSC gets a string that represents the version number of the provider for this social network.</span></span> 
    
3. <span data-ttu-id="204c4-109">[ИсоЦиалпровидер:: соЦиалнетворкнаме](isocialprovider-socialnetworkname.md) &ndash; OSC возвращает строку, представляющую имя социальной сети.</span><span class="sxs-lookup"><span data-stu-id="204c4-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; The OSC gets a string that represents the social network name.</span></span> 
    
4. <span data-ttu-id="204c4-110">[ИсоЦиалпровидер:: соЦиалнетворкгуид](isocialprovider-socialnetworkguid.md) &ndash; OSC получает неИЗМЕНЯЕМЫЙ идентификатор GUID, представляющий социальную сеть.</span><span class="sxs-lookup"><span data-stu-id="204c4-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; The OSC gets an immutable GUID that represents the social network.</span></span> 
    
5. <span data-ttu-id="204c4-111">[ИсоЦиалпровидер:: Capabilities](isocialprovider-getcapabilities.md) &ndash; OSC возвращает строку, представляющую возможности поставщика и которая соответствует определению схемы для элемента **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="204c4-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; The OSC gets a string that represents the provider's capabilities and that complies with the schema definition for the **capabilities** element.</span></span> 
    
6. <span data-ttu-id="204c4-112">[ИсоЦиалпровидер:: соЦиалнетворкикон](isocialprovider-socialnetworkicon.md) &ndash; OSC возвращает массив байтов, представляющий значок для сайта социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="204c4-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; The OSC gets a byte array that represents the icon for the social network site.</span></span> 
    
7. <span data-ttu-id="204c4-113">[ИсоЦиалпровидер:: @ Session](isocialprovider-getsession.md) &ndash; OSC получает интерфейс [настроенный ISocialSession](isocialsessioniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="204c4-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; The OSC gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
    
8. <span data-ttu-id="204c4-114">[Настроенный ISocialSession:: логонвеб](isocialsession-logonweb.md) &ndash; OSC инициализирует вход на сайт социальных сетей с помощью проверки подлинности на основе форм.</span><span class="sxs-lookup"><span data-stu-id="204c4-114">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; The OSC initializes logging on to the social network site by forms-based authentication.</span></span> <span data-ttu-id="204c4-115">Для этого первого входного вызова OSC передает **значение NULL** для параметра _Connect_ .</span><span class="sxs-lookup"><span data-stu-id="204c4-115">For this initial logon call, the OSC passes **null** for the  _connectIn_ parameter.</span></span> 
    
9. <span data-ttu-id="204c4-116">[Настроенный ISocialSession:: жетлогонурл](isocialsession-getlogonurl.md) &ndash; OSC получает URL-адрес, который отображает форму на основе браузера для пользователя во время веб-проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="204c4-116">[ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; The OSC gets the URL to display a browser-based form to the user during web authentication.</span></span> 
    
10. <span data-ttu-id="204c4-117">[Настроенный ISocialSession:: логонвеб](isocialsession-logonweb.md) &ndash; OSC выполняет вход на сайт социальных сетей с помощью проверки подлинности на основе форм.</span><span class="sxs-lookup"><span data-stu-id="204c4-117">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; The OSC completes the logon to the social network site by using forms-based authentication.</span></span> <span data-ttu-id="204c4-118">OSC вызывает этот метод во второй раз, передавая URL-адрес формы входа поставщику в параметре _Connect_ .</span><span class="sxs-lookup"><span data-stu-id="204c4-118">The OSC calls this method a second time, passing the URL of the logon form to the provider in the  _connectIn_ parameter.</span></span> 
    
11. <span data-ttu-id="204c4-119">[Настроенный ISocialSession:: жетлогжедонусер](isocialsession-getloggedonuser.md) &ndash; OSC получает интерфейс [исоЦиалпрофиле](isocialprovideriunknown.md) , представляющий пользователя, выполнившего вход в систему.</span><span class="sxs-lookup"><span data-stu-id="204c4-119">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; The OSC gets an [ISocialProfile](isocialprovideriunknown.md) interface that represents the logged-on user.</span></span> 
    
12. <span data-ttu-id="204c4-120">[Настроенный ISocialSession:: жетнетворкидентифиер](isocialsession-getnetworkidentifier.md) &ndash; OSC возвращает строку, представляющую уникальный идентификатор для сайта социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="204c4-120">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; The OSC gets a string that represents a unique identifier for a social network site.</span></span> <span data-ttu-id="204c4-121">Сетевой идентификатор может быть эквивалентен имени сети.</span><span class="sxs-lookup"><span data-stu-id="204c4-121">The network identifier can be equivalent to the network name.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="204c4-122">См. также</span><span class="sxs-lookup"><span data-stu-id="204c4-122">See also</span></span>

- [<span data-ttu-id="204c4-123">XML для возможностей</span><span class="sxs-lookup"><span data-stu-id="204c4-123">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="204c4-124">ПереOSC типичные последовательности вызовов</span><span class="sxs-lookup"><span data-stu-id="204c4-124">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

