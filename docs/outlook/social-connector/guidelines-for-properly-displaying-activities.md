---
title: Рекомендации по правильному отображению действий
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 55268188-8432-4145-9527-f5888949fc24
description: Поставщики Outlook Social Connector (OSC) могут настроить элементы getActivities и dynamicActivitiesLookupEx для хранения элементов активности OSC в памяти.
ms.openlocfilehash: b2fcaa125ac8bf7924726f4f09ff507769c3a3f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422917"
---
# <a name="guidelines-for-properly-displaying-activities"></a>Рекомендации по правильному отображению действий

Поставщики Outlook Social Connector (OSC) могут настроить элементы **getActivities** и **dynamicActivitiesLookupEx** для хранения элементов активности OSC в памяти. В этом разделе описываются API-aPI для обеспечения возможности работы поставщика OSC, которые OSC вызывает для получения или обновления действий и сведений владельца действия, если поставщик OSC поддерживает синхронизацию веб-каналов активности из социальной сети. В этом разделе также перечислены несколько элементов элемента **activityFeed,** которые поставщик OSC должен настроить для OSC для правильного отображения действий в карточке контакта Office или в области людей Outlook. 
  
- OsC вызывает метод [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) для получения и хранения действий в папке "Канал новостей" для пользователя, выполнимого при входе в систему. Поставщик OSC должен реализовать **GetActivitiesEx,** чтобы вернуть  XML-строку действий, которая соответствует определению XML-схемы поставщика OSC элемента **activityFeed.** 
    
- Поставщик OSC должен установить элемент **ownerID,** который является ключевым элементом **элемента activityDetails.** **ownerID** — непрозраченная строка, идентифицирует владельца действия в социальной сети. 
    
- Поставщик OSC должен установить **элементы nameHint** и **emailAddress** в узле **publisherVariable** элемента **templateVariables.** 
    
   Обратите внимание, что в XML-схеме поставщика OSC элемент **nameHint** является необязательным элементом. OsC использует его для совпадения с отображаемым именем пользователя, выбранного в карточке контакта или области "Люди". Аналогичным образом элемент **emailAddress** является необязательным элементом в схеме XML. OsC использует его для связи с SMTP-адресом пользователя, выбранного в карточке контакта или области "Люди". 
    
   Если указан только элемент **ownerID,** но один или оба элемента **nameHint** и **emailAddress** не указаны, OSC вызывает метод [ISocialSession2::GetPeopleDetails,](isocialsession2-getpeopledetails.md) а затем метод [ISocialPerson::GetDetails,](isocialperson-getdetails.md) чтобы получить дополнительные сведения о человеке, определенном **по ownerID.** Когда OSC вызывает **ISocialPerson::GetDetails,** поставщик должен вернуть  XML-код пользователя, который указывает элементы **fullName** и **emailAddress.** 
    
## <a name="see-also"></a>См. также

- [XML для действий](xml-for-activities.md)  
- [XML для друзей](xml-for-friends.md)  
- [XML для возможностей](xml-for-capabilities.md)

