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
# <a name="forms-based-authentication"></a>Проверка подлинности на основе форм

Outlook Social Connector (OSC) вызывает метод [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) , чтобы определить возможности поставщика OSC для социальных сетей. OSC используется возвращенные возможностей, чтобы определить, как обеспечить поддержку для Office пользователя, вошедшего в этом социальной сети. 

Если элемент **useLogonWebAuth** в возвращенные **возможности** XML указывает, что поставщик OSC поддерживает проверку подлинности на основе форм, OSC можно внести следующие последовательность вызова разрешать пользователям войти в этой социальной сети: 
  
1. [ISocialProvider::Load](isocialprovider-load.md) &ndash; OSC загружает поставщика. 
    
2. [ISocialProvider::Version](isocialprovider-version.md) &ndash; OSC возвращает строку, представляющую номер версии поставщика для этой социальной сети. 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; OSC возвращает строку, представляющую имя социальной сети. 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; OSC получает постоянные GUID, который представляет социальных сетей. 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; OSC возвращает строку, которая представляет возможности поставщика, который соответствует определение схемы для элемента **capabilities** . 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; OSC возвращает массив байтов, который представляет значок для узла социальной сети. 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; OSC получает интерфейс [ISocialSession](isocialsessioniunknown.md) . 
    
8. [ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; OSC инициализирует выполнение входа на сайт социальных сетей, проверки подлинности на основе форм. Для этого вызова начальное входа OSC передает **значение null** для параметра _connectIn_ . 
    
9. [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; OSC получает URL-адрес для отображения формы на основе браузера для пользователя в ходе проверки подлинности web. 
    
10. [ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; OSC завершает входа на сайт социальной сети с помощью проверки подлинности на основе форм. OSC вызывает этот метод еще раз, передав URL-адрес формы входа в систему для поставщика с помощью параметра _connectIn_ . 
    
11. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; OSC получает [ISocialProfile](isocialprovideriunknown.md) интерфейс, который представляет текущего пользователя. 
    
12. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; OSC возвращает строку, представляющую уникальный идентификатор для сайтов социальных сетей. Идентификатор сети могут быть эквивалентно сетевое имя. 
    
## <a name="see-also"></a>См. также

- [XML-код для возможности](xml-for-capabilities.md)
- [Типичные последовательности вызовов OSC](osc-typical-calling-sequences.md)

