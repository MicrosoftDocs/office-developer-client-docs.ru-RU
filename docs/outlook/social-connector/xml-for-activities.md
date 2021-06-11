---
title: XML для действий
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: acc4a555-a3bf-4a79-86dc-aba6477733b8
description: В этом разделе показан пример сценария, в который Outlook API extensibility API поставщика социальных соединителов (OSC), который реализует поставщик OSC, и который osC делает для получения сведений о действиях. Сведения выражены в строках XML, которые соответствуют схеме XML поставщика OSC.
ms.openlocfilehash: a4f1c6ce1f33b59811f6a6fecb737cd1f737946b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409631"
---
# <a name="xml-for-activities"></a>XML для действий

В этом разделе показан пример сценария, в который Outlook API extensibility API поставщика социальных соединителов (OSC), который реализует поставщик OSC, и который osC делает для получения сведений о действиях. Сведения выражены в строках XML, которые соответствуют схеме XML поставщика OSC.
  
Схема XML-схемы поставщика OSC позволяет поставщику OSC определять действия. Сведения об активности могут включать социальную сеть, в которой появились элементы ленты действий, сведения о каждом элементе ленты действий (например, владельца, типа и даты публикации действия) и шаблон для отображения действия. Чтобы поддерживать отображение действий на области пользователей или контактной карте, поставщик OSC социальной сети должен реализовать и вернуть правильные действия XML. Пример XML-канала активности см. в [примере Activity Feed XML.](activity-feed-xml-example.md) Дополнительные сведения о синхронизации действий друзей см. в [интернете.](synchronizing-friends-and-activities.md) Полное определение схемы XML-схемы поставщика OSC, в том числе необходимых или необязательных элементов, см. в Outlook [social Connector Provider XML Schema.](outlook-social-connector-provider-xml-schema.md) 
  
В следующем сценарии OSC динамически синхронизирует действия для человека, выбранного в области people, и получает сведения об этом человеке:
  
1. Поставщик OSC, который поддерживает синхронизацию действий по запросу, указывает, что для OSC используется **элементы getActivities** и **dynamicActivitiesLookupEx.** Поставщик OSC также задает элемент **hashFunction.** Все три элемента — это детские **элементы возможностей.** 
    
2. Поставщик OSC реализует методы **ISocialProvider::GetCapabilities** и [ISocialSession2::GetActivitiesEx.](isocialsession2-getactivitiesex.md) 
    
3. OsC вызывает **ISocialProvider::GetCapabilities,** чтобы проверить значение **getActivities** и **dynamicActivitiesLookupEx,** чтобы убедиться, что поставщик OSC поддерживает синхронизацию действий по запросу. OsC также отмечает значение элемента **hashFunction,** поддерживаемого поставщиком OSC. 
    
4. OsC обновляет области людей или контактную карту, чтобы позволить пользователю видеть последние действия выбранного человека. OSC шифрует SMTP-адрес человека с помощью функции hashAddresses, указанной в элементе **hashFunction,** образуя строку XML, которая соответствует определению схемы XML для элемента **hashedAddresses.** 
    
5. OsC вызывает **ISocialSession2::GetActivitiesEx,** предоставляя эту строку XML-адреса в качестве параметра _hashedAddresses,_ чтобы получить текущую коллекцию действий для этого человека в параметре _действия._ _Строка_ параметра действия соответствует определению схемы XML элемента **activityFeed.** 
    
6. На основе определения схемы XML для **activityFeed** OSC  далее размыкает строку действий, чтобы узнать тип, дату публикации и другие сведения о каждом действии и о том, как отобразить действие. 
    
7. Чтобы получить сведения о выбранном человеке, OSC вызывает [ISocialSession2::GetPeopleDetails,](isocialsession2-getpeopledetails.md)предоставляя ту же строку XML-адресов, что и аргумент для _параметра personsAddresses._ Сведения о человеке возвращаются в _параметре personsCollection._ Эти сведения могут включать **firstName,** **lastName** и **emailAddress.** Параметр _personsCollection_ соответствует определению схемы XML для **элемента person.** 
    
Дополнительные сведения о указании XML для действий можно найти в следующих разделах этого раздела:
  
- [Обзор XML для элемента ленты действий](overview-of-xml-for-an-activity-feed-item.md)
    
- [элемент activityDetails](activitydetails-element.md)
    
- [элемент activityTemplateContainer](activitytemplatecontainer-element.md)
    
- [Переменные шаблона](template-variables.md)
    
- [Рекомендации для правильного отображения действий](guidelines-for-properly-displaying-activities.md)
    
## <a name="see-also"></a>См. также

- [Пример ленты действий XML](activity-feed-xml-example.md)  
- [Синхронизация друзей и действий](synchronizing-friends-and-activities.md) 
- [XML для возможностей](xml-for-capabilities.md)  
- [XML для друзей](xml-for-friends.md)
- [Разработка поставщика с помощью схемы XML OSC](developing-a-provider-with-the-osc-xml-schema.md)

