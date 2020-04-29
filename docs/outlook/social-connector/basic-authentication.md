---
title: Обычная проверка подлинности
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89349d1e-365a-442e-9ba3-2df601d9323c
description: 'Outlook Social Connector (OSC) вызывает метод ИсоЦиалпровидер:: capabilities, который определяет возможности поставщика OSC для социальной сети.'
ms.openlocfilehash: 7f716df3ef2e82712374ce3d775cdf66eb07e8b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439928"
---
# <a name="basic-authentication"></a><span data-ttu-id="99b61-103">Обычная проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="99b61-103">Basic authentication</span></span>

<span data-ttu-id="99b61-104">Outlook Social Connector (OSC) вызывает метод [исоЦиалпровидер:: Capabilities](isocialprovider-getcapabilities.md) , который определяет возможности поставщика OSC для социальной сети.</span><span class="sxs-lookup"><span data-stu-id="99b61-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="99b61-105">Для определения способа поддержки пользователя Office, который выполняет вход в эту социальную сеть, OSC использует возвращенные возможности.</span><span class="sxs-lookup"><span data-stu-id="99b61-105">The OSC uses the returned capabilities to determine how to support an Office user who is logging on to this social network.</span></span> <span data-ttu-id="99b61-106">Если элемент **уселогонвебаус** в возвращенном XML-файле **возможностей** указывает, что поставщик OSC поддерживает обычную проверку подлинности, OSC может выполнить следующую последовательность вызовов, чтобы разрешить пользователю входить в эту социальную сеть:</span><span class="sxs-lookup"><span data-stu-id="99b61-106">If the **useLogonWebAuth** element in the returned **capabilities** XML indicates that the OSC provider supports basic authentication, the OSC can make the following calling sequence to allow a user to log on to that social network:</span></span> 
  
1. <span data-ttu-id="99b61-107">[ИсоЦиалпровидер:: Load](isocialprovider-load.md) — элемент OSC загружает поставщик.</span><span class="sxs-lookup"><span data-stu-id="99b61-107">[ISocialProvider::Load](isocialprovider-load.md) —The OSC loads the provider.</span></span> 
    
2. <span data-ttu-id="99b61-108">[ИсоЦиалпровидер:: Version](isocialprovider-version.md) — объект OSC получает строку, представляющую номер версии поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="99b61-108">[ISocialProvider::Version](isocialprovider-version.md) —The OSC gets a string that represents the version number of the OSC provider.</span></span> 
    
3. <span data-ttu-id="99b61-109">[ИсоЦиалпровидер:: соЦиалнетворкнаме](isocialprovider-socialnetworkname.md) — объект OSC получает строку, представляющую имя социальной сети.</span><span class="sxs-lookup"><span data-stu-id="99b61-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) —The OSC gets a string that represents the social network name.</span></span> 
    
4. <span data-ttu-id="99b61-110">[ИсоЦиалпровидер:: соЦиалнетворкгуид](isocialprovider-socialnetworkguid.md) — объект OSC получает неизменяемый идентификатор GUID, представляющий социальную сеть.</span><span class="sxs-lookup"><span data-stu-id="99b61-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) —The OSC gets an immutable GUID that represents the social network.</span></span> 
    
5. <span data-ttu-id="99b61-111">[ИсоЦиалпровидер::-Capabilities](isocialprovider-getcapabilities.md) — получает строку, представляющую возможности поставщика, и соответствующие определению схемы для элемента **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="99b61-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) —The OSC gets a string that represents the provider's capabilities and that complies with the schema definition for the **capabilities** element.</span></span> 
    
6. <span data-ttu-id="99b61-112">[ИсоЦиалпровидер:: соЦиалнетворкикон](isocialprovider-socialnetworkicon.md) — объект OSC получает массив байтов, представляющий значок для сайта социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="99b61-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) —The OSC gets a byte array that represents the icon for the social network site.</span></span> 
    
7. <span data-ttu-id="99b61-113">[ИсоЦиалпровидер::-Session](isocialprovider-getsession.md) — OSC получает интерфейс [настроенный ISocialSession](isocialsessioniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="99b61-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) —The OSC gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
    
8. <span data-ttu-id="99b61-114">[Настроенный ISocialSession:: вход](isocialsession-logon.md) — OSC выполняет вход пользователя на сайт социальных сетей с использованием указанных имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="99b61-114">[ISocialSession::Logon](isocialsession-logon.md) —The OSC logs the user on to the social network site by using the specified user name and password.</span></span> 
    
9. <span data-ttu-id="99b61-115">[Настроенный ISocialSession:: жетлогжедонусер](isocialsession-getloggedonuser.md) — объект OSC получает интерфейс [исоЦиалпрофиле](isocialprovideriunknown.md) , представляющий пользователя, выполнившего вход в систему.</span><span class="sxs-lookup"><span data-stu-id="99b61-115">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) —The OSC gets an [ISocialProfile](isocialprovideriunknown.md) interface that represents the logged-on user.</span></span> 
    
10. <span data-ttu-id="99b61-116">[Настроенный ISocialSession:: жетнетворкидентифиер](isocialsession-getnetworkidentifier.md) — объект OSC получает строку, представляющую уникальный идентификатор для сайта социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="99b61-116">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) —The OSC gets a string that represents a unique identifier for a social network site.</span></span> <span data-ttu-id="99b61-117">Сетевой идентификатор может быть эквивалентен имени сети.</span><span class="sxs-lookup"><span data-stu-id="99b61-117">The network identifier can be equivalent to the network name.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="99b61-118">См. также</span><span class="sxs-lookup"><span data-stu-id="99b61-118">See also</span></span>

- [<span data-ttu-id="99b61-119">XML для возможностей</span><span class="sxs-lookup"><span data-stu-id="99b61-119">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="99b61-120">Переosc типичные последовательности вызовов</span><span class="sxs-lookup"><span data-stu-id="99b61-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

