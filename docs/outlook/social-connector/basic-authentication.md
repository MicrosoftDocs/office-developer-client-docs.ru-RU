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
# <a name="basic-authentication"></a>Обычная проверка подлинности

Outlook Social Connector (OSC) вызывает метод [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) , чтобы определить возможности поставщика OSC для социальных сетей. OSC используется возвращенные возможностей, чтобы определить, как обеспечить поддержку для Office пользователя, вошедшего в этом социальной сети. Если элемент **useLogonWebAuth** в возвращенные **возможности** XML указывает, что поставщика OSC поддерживает обычную проверку подлинности, OSC можно внести следующие последовательность вызова разрешать пользователям войти в этой социальной сети: 
  
1. [ISocialProvider::Load](isocialprovider-load.md) — OSC загружает поставщика. 
    
2. [ISocialProvider::Version](isocialprovider-version.md) — OSC возвращает строку, представляющую номер версии поставщика OSC. 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) — OSC возвращает строку, представляющую имя социальной сети. 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) — OSC получает постоянные GUID, который представляет социальных сетей. 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) — OSC возвращает строку, которая представляет возможности поставщика, который соответствует определение схемы для элемента **capabilities** . 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) — OSC возвращает массив байтов, который представляет значок для узла социальной сети. 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md) — OSC получает интерфейс [ISocialSession](isocialsessioniunknown.md) . 
    
8. [ISocialSession::Logon](isocialsession-logon.md) — OSC входа пользователя на узел социальной сети с помощью указанного имени пользователя и пароля. 
    
9. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) — OSC получает [ISocialProfile](isocialprovideriunknown.md) интерфейс, который представляет текущего пользователя. 
    
10. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) — OSC возвращает строку, представляющую уникальный идентификатор для сайтов социальных сетей. Идентификатор сети могут быть эквивалентно сетевое имя. 
    
## <a name="see-also"></a>См. также

- [XML-код для возможности](xml-for-capabilities.md)
- [Типичные последовательности вызовов OSC](osc-typical-calling-sequences.md)

