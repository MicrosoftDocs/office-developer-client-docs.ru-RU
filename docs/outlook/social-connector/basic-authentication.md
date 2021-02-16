---
title: Обычная проверка подлинности
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89349d1e-365a-442e-9ba3-2df601d9323c
description: Outlook Social Connector (OSC) вызывает метод ISocialProvider::GetCapabilities, чтобы определить возможности поставщика OSC для социальной сети.
ms.openlocfilehash: 7f716df3ef2e82712374ce3d775cdf66eb07e8b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439928"
---
# <a name="basic-authentication"></a>Обычная проверка подлинности

Outlook Social Connector (OSC) вызывает метод [ISocialProvider::GetCapabilities,](isocialprovider-getcapabilities.md) чтобы определить возможности поставщика OSC для социальной сети. OsC использует возвращенные возможности, чтобы определить, как поддерживать пользователя Office, который вошел в эту социальную сеть. Если элемент **useLogonWebAuth** в **XML** возвращаемой возможности указывает, что поставщик OSC поддерживает базовую проверку подлинности, osC может сделать следующую последовательность вызовов, чтобы позволить пользователю войти в эту сетею: 
  
1. [ISocialProvider::Load](isocialprovider-load.md) — OSC загружает поставщика. 
    
2. [ISocialProvider::Version](isocialprovider-version.md) — OSC получает строку, представляюную номер версии поставщика OSC. 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) — OSC получает строку, представляюную имя социальной сети. 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) — OSC получает неизменяемый GUID, который представляет социальные сети. 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) — OSC получает строку, которая представляет возможности поставщика и соответствует определению схемы для элемента **возможностей.** 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) — OSC получает массив byte, который представляет значок для сайта социальной сети. 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md) — OSC получает [интерфейс ISocialSession.](isocialsessioniunknown.md) 
    
8. [ISocialSession::Logon](isocialsession-logon.md) — OSC регистрирует пользователя на сайте социальной сети, используя указанное имя пользователя и пароль. 
    
9. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) — OSC получает [интерфейс ISocialProfile,](isocialprovideriunknown.md) который представляет во входе пользователя. 
    
10. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) — OSC получает строку, представляюную уникальный идентификатор для сайта социальной сети. Сетевой идентификатор может быть эквивалентен сетевому имени. 
    
## <a name="see-also"></a>См. также

- [XML для возможностей](xml-for-capabilities.md)
- [Типичные последовательности вызовов OSC](osc-typical-calling-sequences.md)

