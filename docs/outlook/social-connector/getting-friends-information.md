---
title: Получение сведений о друзьях
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8a56746-4de4-4f24-af32-e85079c060b8
description: Outlook Social Connector (OSC) вызывает метод ISocialProvider::GetCapabilities, чтобы определить возможности поставщика OSC для социальных сетей.
ms.openlocfilehash: 68443992351f4c83e8e560a753941e97bf91de67
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812706"
---
# <a name="getting-friends-information"></a>Получение сведений о друзьях

Outlook Social Connector (OSC) вызывает метод [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) , чтобы определить возможности поставщика OSC для социальных сетей. Если элементы **getFriends** и **cacheFriends** в возвращенные **возможности** XML показывают, что поставщика OSC поддерживает получение друзей и элементы в соответствующей папке контактов контактов кэширования друзья как Outlook, можно сделать OSC следующую последовательность вызова. OSC вызывает методы в следующем порядке, чтобы получить сведения и рисунки (как поддерживаемый интерфейс [ISocialPerson](isocialpersoniunknown.md) ) для друзей в социальных сетях. 
  
> [!NOTE]
> OSC обновляет кэш с интервалом по умолчанию. При возникновении ошибки во время кэша обновите, повторных попыток OSC в другой предварительно интервала, что также можно управлять путем указания элемент **contactSyncRestartInterval** в **возможности** XML. Дополнительные сведения об обновлении кэша контакты можно [Синхронизация друзей и действия](synchronizing-friends-and-activities.md). 
  
1. [ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) — OSC Получает идентификатор пользователя Office, который вошел в систему социальных сетей. 
    
2. [ISocialSession::GetPerson](isocialsession-getperson.md) , используя идентификатор пользователя Microsoft Office, OSC возвращает объект **ISocialPerson** для этого пользователя. 
    
3. [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) — OSC Получает список friend пользователя в социальных сетях. 
    
4. [ISocialSession::GetPerson](isocialsession-getperson.md) — для каждого пользователя в XML-код возвращает **GetFriendsAndColleagues**, OSC получает интерфейс **ISocialPerson** . 
    
5. [ISocialPerson::GetPicture](isocialperson-getpicture.md) — для каждого пользователя в XML-код возвращает **GetFriendsAndColleagues**, OSC получает ресурсов изображений.
    
## <a name="see-also"></a>См. также

- [XML-код для возможности](xml-for-capabilities.md)
- [Типичные последовательности вызовов OSC](osc-typical-calling-sequences.md)

