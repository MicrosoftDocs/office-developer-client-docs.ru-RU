---
title: Проверка подлинности на основе форм
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 282b2377-45ba-4f0c-a7d9-830fa3505c93
description: Outlook Social Connector (OSC) вызывает метод ISocialProvider::GetCapabilities, чтобы определить возможности поставщика OSC для социальной сети.
ms.openlocfilehash: 420f19a8d7632f2ab9b093eb929ffe879f8a2fc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435532"
---
# <a name="forms-based-authentication"></a>Проверка подлинности на основе форм

Outlook Social Connector (OSC) вызывает метод [ISocialProvider::GetCapabilities,](isocialprovider-getcapabilities.md) чтобы определить возможности поставщика OSC для социальной сети. OsC использует возвращенные возможности, чтобы определить, как поддерживать пользователя Office, который вошел в эту социальную сеть. 

Если элемент **useLogonWebAuth** в **XML** возвращаемой возможности указывает, что поставщик OSC поддерживает проверку подлинности на основе форм, osC может сделать следующую последовательность вызовов, чтобы позволить пользователю войти в эту сетею: 
  
1. [ISocialProvider::Load](isocialprovider-load.md) &ndash; OSC загружает поставщика. 
    
2. [ISocialProvider::Version](isocialprovider-version.md) &ndash; OsC получает строку, представляюную номер версии поставщика для этой социальной сети. 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; OsC получает строку, представляюную имя социальной сети. 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; OSC получает не изменяемый GUID, представляюща социальных сетей. 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; OSC получает строку, которая представляет возможности поставщика и соответствует определению схемы для **элемента возможностей.** 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; OsC получает массив byte, который представляет значок для сайта социальной сети. 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; OsC получает [интерфейс ISocialSession.](isocialsessioniunknown.md) 
    
8. [ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; OsC инициализирует вход на сайт социальной сети с помощью проверки подлинности на основе форм. Для этого начального вызова для логин OSC передается **null** для _параметра connectIn._ 
    
9. [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; OsC получает URL-адрес для отображения пользователю браузерной формы во время веб-проверки подлинности. 
    
10. [ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; OsC завершает учетные данных для сайта социальной сети с помощью проверки подлинности на основе форм. OSC вызывает этот метод второй раз, передавая URL-адрес формы для логотипа поставщику в _параметре connectIn._ 
    
11. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; OsC получает интерфейс [ISocialProfile,](isocialprovideriunknown.md) который представляет во входе пользователя. 
    
12. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; OSC получает строку, представляюную уникальный идентификатор для сайта социальной сети. Сетевой идентификатор может быть эквивалентен сетевому имени. 
    
## <a name="see-also"></a>См. также

- [XML для возможностей](xml-for-capabilities.md)
- [Типичные последовательности вызовов OSC](osc-typical-calling-sequences.md)

