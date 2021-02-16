---
title: Получение действий
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cb8f916-f061-4c4c-ad1b-40d44af3345a
description: OsC вызывает метод ISocialProvider::GetCapabilities, чтобы определить возможности поставщика OSC для социальной сети.
ms.openlocfilehash: 9d504fb64368a6910feaa38f0ef19ed631b4d4e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420579"
---
# <a name="getting-activities"></a>Получение действий

OsC вызывает метод [ISocialProvider::GetCapabilities,](isocialprovider-getcapabilities.md) чтобы определить возможности поставщика OSC для социальной сети. Если элементы **getActivities** и **dynamicActivitiesLookupEx** в **XML** возвращаемой возможности указывают, что поставщик OSC поддерживает получение действий по запросу и хранение действий в памяти, OSC может сделать следующую последовательность вызовов. OsC также отмечает функцию hash, указанную в **элементе hashFunction** в XML **возможностей.** OSC вызывает методы в следующей последовательности для получения действий и сведений (поддерживаемых интерфейсом [ISocialPerson)](isocialpersoniunknown.md) для друзей и других пользователей в социальной сети: 
  
1. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) — по окончании процесса проверки подлинности OSC вызывает **GetLoggedOnUser** для получения [интерфейса ISocialProfile](isocialprofileisocialperson.md) для пользователя, который проходит проверку подлинности. Дополнительные сведения о проверке подлинности см. в основных документах проверки [подлинности](basic-authentication.md) и проверке подлинности на основе [форм.](forms-based-authentication.md)
    
2. [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) — для пользователей, отображаемого в области людей Outlook, OSC получает и хеширует их SMTP-адреса, вызывает **ISocialSession2::GetActivitiesEx** и сохраняет (в памяти) данные о действиях, возвращенные для этих пользователей. OsC получает выходной параметр  _activities_, который является строкой, которая содержит коллекцию действий для друзей во время входа пользователя. Эта строка соответствует определению схемы для **элемента activityFeed.** 
    
3. [ISocialSession::GetPerson](isocialsession-getperson.md) — для каждого элемента **activityDetails** в XML **activityFeed,** возвращаемого **GetActivitiesEx,** существует элемент **ownerID,** который указывает человека, которому принадлежит это действие. OsC использует это **значение ownerID** для вызова **GetPerson,** чтобы получить **интерфейс ISocialPerson** для этого пользователя. 
    
4. [ISocialPerson::GetDetails](isocialperson-getdetails.md) — на основе объекта **ISocialPerson,** полученного на шаге 3, OSC вызывает **GetDetails,** чтобы получить сведения для этого человека, например имя и фамилию. OsC может сделать то же самое для каждого действия, указанного в элементе **activityDetails** в XML **activityFeed,** возвращаемом **GetActivitiesEx на** шаге 2. 
    
> [!NOTE]
> OsC обновляет кэш действий с интервалом по умолчанию. Дополнительные сведения об обновлениях кэша действий см. в этой [теме.](synchronizing-friends-and-activities.md) 
  
## <a name="see-also"></a>См. также

- [XML для возможностей](xml-for-capabilities.md)
- [Типичные последовательности вызовов OSC](osc-typical-calling-sequences.md)

