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
# <a name="basic-authentication"></a>Обычная проверка подлинности

Метод Outlook Social Connector (OSC) вызывает [метод ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) для определения возможностей поставщика OSC для социальной сети. OsC использует возвращенные возможности, чтобы определить, как поддерживать Office пользователя, входившего в эту социальную сеть. Если элемент **useLogonWebAuth** в возвращенных возможностях **XML** указывает, что поставщик OSC поддерживает базовую проверку подлинности, OSC может сделать следующую последовательность вызовов, чтобы позволить пользователю войти в эту социальную сеть: 
  
1. [ISocialProvider::Load](isocialprovider-load.md) — OSC загружает поставщика. 
    
2. [ISocialProvider::Version](isocialprovider-version.md) — OSC получает строку, представляюную номер версии поставщика OSC. 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) — OSC получает строку, представляюную имя социальной сети. 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) — OSC получает неизменяемый GUID, который представляет социальную сеть. 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) — OSC получает строку, которая представляет возможности поставщика и соответствует определению схемы элемента **возможностей.** 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) — OSC получает массив byte, представляючий значок для сайта социальной сети. 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md) — OSC получает [интерфейс ISocialSession.](isocialsessioniunknown.md) 
    
8. [ISocialSession::Logon](isocialsession-logon.md) — OSC регистрирует пользователя на сайте социальной сети с помощью указанного имени пользователя и пароля. 
    
9. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) — OSC получает [интерфейс ISocialProfile,](isocialprovideriunknown.md) который представляет зарегистрированного пользователя. 
    
10. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) — OSC получает строку, представляюную уникальный идентификатор для сайта социальной сети. Идентификатор сети может быть эквивалентен имени сети. 
    
## <a name="see-also"></a>См. также

- [XML для возможностей](xml-for-capabilities.md)
- [Типичные последовательности вызовов OSC](osc-typical-calling-sequences.md)

