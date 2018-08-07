---
title: Рекомендации по правильному отображению действий
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 55268188-8432-4145-9527-f5888949fc24
description: Outlook Social Connector (OSC) поставщиков можно задать элементы getActivities и dynamicActivitiesLookupEx иметь OSC хранения элементов активности в памяти.
ms.openlocfilehash: f8cb5850c8920f09f784343db18372bb75ca17a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812708"
---
# <a name="guidelines-for-properly-displaying-activities"></a>Рекомендации по правильному отображению действий

Outlook Social Connector (OSC) поставщиков можно задать **getActivities** и элементам **dynamicActivitiesLookupEx** OSC хранения элементов активности в памяти. В этом разделе описываются возможности расширения поставщика OSC, интерфейсы API, который вызывает OSC получить или обновить действия и сведения о действиях владельца, если поставщик OSC поддерживает синхронизации активности каналов из социальных сетей. Также в разделе описываются некоторые дочерние элементы элемента **activityFeed** , что поставщика OSC следует устанавливать для OSC для правильного отображения действий в карточке контакта Office или области пользователей Outlook. 
  
- OSC вызывает метод [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) для получения и хранения действий в папку веб-канал новостей для пользователя, вошедшего в систему. Поставщика OSC необходимо реализовать **GetActivitiesEx** возвращает строку XML _действия_ , соответствующего стандарту поставщика OSC определение схемы XML элемента **activityFeed** . 
    
- Поставщика OSC необходимо задать элемент **ownerID** , который является дочерним элементом элемента **activityDetails** . **ownerID** представляет собой непрозрачную строку, которая определяет владельца активности в социальных сетях. 
    
- В узел **publisherVariable** элемента **templateVariables** поставщика OSC выбрать элементы **nameHint** и **emailAddress** . 
    
   Обратите внимание, что в схеме XML поставщика OSC элемент **nameHint** дополнительный элемент. OSC использует его в соответствии с отображаемое имя пользователя, выбранного в карточке контакта или области пользователей. Аналогично элемент **emailAddress** — это дополнительный элемент в XML-схему. OSC использует его в соответствии с SMTP-адрес пользователя, выбранного в карточке контакта или области пользователей. 
    
   Если только указан элемент **ownerID** , но не указан один или оба **nameHint** и **emailAddress** , OSC вызывает метод [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) , а затем [ISocialPerson::GetDetails](isocialperson-getdetails.md) метод, чтобы получить дополнительные сведения об этом человеке, определяемую средством **ownerID**. Когда OSC вызывает **ISocialPerson::GetDetails**, поставщик должен возвращать **человека** XML, которая определяет элементы **полное имя** и **emailAddress** . 
    
## <a name="see-also"></a>См. также

- [XML-код для действия](xml-for-activities.md)  
- [XML-код для друзей](xml-for-friends.md)  
- [XML-код для возможности](xml-for-capabilities.md)

