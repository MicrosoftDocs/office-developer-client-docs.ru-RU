---
title: Рекомендации по правильному отображению действий
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 55268188-8432-4145-9527-f5888949fc24
description: Outlook Поставщики социальных соединителов (OSC) могут установить элементы getActivities и dynamicActivitiesLookupEx для хранения элементов активности OSC в памяти.
ms.openlocfilehash: b2fcaa125ac8bf7924726f4f09ff507769c3a3f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422917"
---
# <a name="guidelines-for-properly-displaying-activities"></a>Рекомендации по правильному отображению действий

Outlook Поставщики социальных соединителов (OSC) могут установить элементы **getActivities** и **dynamicActivitiesLookupEx** для хранения элементов активности OSC в памяти. В этом разделе описывается API-API-службы поставщика extensibility OSC, которые osC вызывает для получения или обновления сведений владельца действий и действий, если поставщик OSC поддерживает синхронизацию каналов активности из социальной сети. В этой теме также перечислены несколько детских элементов элемента **activityFeed,** который поставщик OSC должен установить для OSC для правильного отображения действий в Office контактной карточке или Outlook области людей. 
  
- OsC вызывает [метод ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) для получения и хранения действий в папке Ленты новостей для зарегистрированного пользователя. Поставщик OSC должен реализовать **GetActivitiesEx,** чтобы вернуть строку _XML_ действий, которая соответствует определению схемы XML-схемы поставщика OSC элемента **activityFeed.** 
    
- Поставщик OSC должен установить **элемент ownerID,** который является детским элементом **элемента activityDetails.** **ownerID** — непрозраченная строка, определяемая владельцем действия в социальной сети. 
    
- Поставщик OSC должен установить элементы **nameHint** и **emailAddress** в **узле publisherVariable** элемента **templateVariables.** 
    
   Обратите внимание, что в схеме XML поставщика OSC элемент **nameHint** является необязательным элементом. OsC использует его, чтобы соответствовать отображаемой фамилии пользователя, выбранного в карточке контакта или области людей. Аналогичным образом элемент **emailAddress** является необязательным элементом схемы XML. OsC использует его для совпадения SMTP-адреса пользователя, выбранного в карточке контакта или в области людей. 
    
   Если указан только элемент **ownerID,** но одно или оба **имениHint** и **emailAddress** не указаны, OSC вызывает [метод ISocialSession2::GetPeopleDetails,](isocialsession2-getpeopledetails.md) а затем метод [ISocialPerson::GetDetails,](isocialperson-getdetails.md) чтобы получить дополнительные сведения о человеке, идентифицированного **ownerID**. Когда OSC вызывает **ISocialPerson::GetDetails,** поставщик должен вернуть человеку **XML,** который указывает элементы **fullName** и **emailAddress.** 
    
## <a name="see-also"></a>См. также

- [XML для действий](xml-for-activities.md)  
- [XML для друзей](xml-for-friends.md)  
- [XML для возможностей](xml-for-capabilities.md)

