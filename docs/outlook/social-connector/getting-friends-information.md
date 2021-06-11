---
title: Получение сведений о друзьях
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8a56746-4de4-4f24-af32-e85079c060b8
description: Метод Outlook social Connector (OSC) вызывает метод ISocialProvider::GetCapabilities, чтобы определить возможности поставщика OSC для социальной сети.
ms.openlocfilehash: 697902631b010afab015e9cfb73fac81ac427d6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428797"
---
# <a name="getting-friends-information"></a>Получение сведений о друзьях

Метод Outlook Social Connector (OSC) вызывает [метод ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) для определения возможностей поставщика OSC для социальной сети. Если элементы **getFriends** и **cacheFriends** в  возвращенных XML-возможностях указывают на то, что поставщик OSC поддерживает получение друзей и кэшировать друзей в качестве контактных элементов Outlook в соответствующей папке контактов, osC может сделать следующую последовательность вызовов. OsC вызывает методы в этой последовательности для получения сведений и изображений (поддерживаемых интерфейсом [ISocialPerson)](isocialpersoniunknown.md) для друзей в социальной сети. 
  
> [!NOTE]
> OsC обновляет кэш с интервалом по умолчанию. Если ошибка возникает во время обновления кэша, OSC повторно проводит повторное истечение заданного интервала, который также можно  контролировать, указав элемент **contactSyncRestartInterval** в возможностях XML. Дополнительные сведения о том, как освежить кэш контактов, см. в [руб. Синхронизация друзей и действий.](synchronizing-friends-and-activities.md) 
  
1. [ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) — OSC получает пользовательский ID пользователя Office, который вошел в социальную сеть. 
    
2. [ISocialSession::GetPerson](isocialsession-getperson.md) — используя пользовательский ID пользователя Office, OSC получает объект **ISocialPerson** для этого пользователя. 
    
3. [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) — OSC получает список друзей пользователя в социальной сети. 
    
4. [ISocialSession::GetPerson](isocialsession-getperson.md) — для каждого пользователя XML, возвращенного **GetFriendsAndColleagues,** OSC получает интерфейс **ISocialPerson.** 
    
5. [ISocialPerson::GetPicture](isocialperson-getpicture.md) — для каждого человека в XML, возвращенного **GetFriendsAndColleagues,** OSC получает ресурс изображения.
    
## <a name="see-also"></a>См. также

- [XML для возможностей](xml-for-capabilities.md)
- [Типичные последовательности вызовов OSC](osc-typical-calling-sequences.md)

