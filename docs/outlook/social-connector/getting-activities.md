---
title: Получение действий
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cb8f916-f061-4c4c-ad1b-40d44af3345a
description: OSC вызывает метод ISocialProvider::GetCapabilities, чтобы определить возможности поставщика OSC для социальных сетей.
ms.openlocfilehash: 82bb5322118fa3ebd7610f56b8f34ae95b59a40f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812709"
---
# <a name="getting-activities"></a>Получение действий

OSC вызывает метод [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) , чтобы определить возможности поставщика OSC для социальных сетей. Если элементы **getActivities** и **dynamicActivitiesLookupEx** в возвращенные **возможности** XML показывают, что поставщика OSC поддерживает получение мероприятий по запросу и хранение действий в памяти, можно сделать следующие OSC последовательность вызовов. OSC также заметки о хэш-функции, заданная в элементе **hashFunction** в **возможности** XML. В следующей последовательности для получения информации и действия (как поддерживаемый интерфейс [ISocialPerson](isocialpersoniunknown.md) ) друзья и не-в социальных сетях OSC вызывает методы: 
  
1. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) — в конце процесса проверки подлинности OSC вызывает **GetLoggedOnUser** для получения интерфейса [ISocialProfile](isocialprofileisocialperson.md) для прохождения проверки подлинности пользователя. Дополнительные сведения о проверке подлинности можно [Обычная проверка подлинности](basic-authentication.md) и [проверки подлинности на основе форм](forms-based-authentication.md).
    
2. [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) — для лиц, отображаемые в области пользователей Outlook, получает OSC и хэш-значений их SMTP решает, вызывает **ISocialSession2::GetActivitiesEx**и сохраняет (в памяти) данные действия возвращаются для Эти лица. Получает OSC в выходной параметр _действий_, который является строка, содержащая набор операций для друзей пользователя, вошедшего в систему. Эта строка соответствует определение схемы для элемента **activityFeed** . 
    
3. [ISocialSession::GetPerson](isocialsession-getperson.md) — для каждого элемента **activityDetails** в **activityFeed** XML, возвращенные **GetActivitiesEx**, существует элемент в **ownerID** , указывающее пользователя, выполняющего действия. OSC использует это значение **ownerID** для вызова **GetPerson** для получения интерфейс **ISocialPerson** этого контакта. 
    
4. [ISocialPerson::GetDetails](isocialperson-getdetails.md) — на основе **ISocialPerson** объекта получить на шаге 3, OSC вызывает **GetDetails** для получения сведений об этом контакте, например, имя и Фамилия. OSC можно сделать это для каждого действия, указанная в элемент **activityDetails** в **activityFeed** XML, возвращенные **GetActivitiesEx** на шаге 2. 
    
> [!NOTE]
> OSC обновляется кэш действий с интервалом по умолчанию. Дополнительные сведения об обновлении кэша действий можно [Синхронизация друзей и действия](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>См. также

- [XML-код для возможности](xml-for-capabilities.md)
- [Типичные последовательности вызовов OSC](osc-typical-calling-sequences.md)

