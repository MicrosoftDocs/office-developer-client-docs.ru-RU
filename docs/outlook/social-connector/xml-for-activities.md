---
title: XML для действий
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: acc4a555-a3bf-4a79-86dc-aba6477733b8
description: В этом разделе содержится пример сценария, в который показано, как API extensibility поставщика Outlook Social Connector (OSC) вызывает, который реализует поставщик OSC и который OSC делает для получения сведений о действиях. Информация выражается в строках XML, которые соответствуют XML-схеме поставщика OSC.
ms.openlocfilehash: a4f1c6ce1f33b59811f6a6fecb737cd1f737946b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409631"
---
# <a name="xml-for-activities"></a>XML для действий

В этом разделе содержится пример сценария, в который показано, как API extensibility поставщика Outlook Social Connector (OSC) вызывает, который реализует поставщик OSC и который OSC делает для получения сведений о действиях. Информация выражается в строках XML, которые соответствуют XML-схеме поставщика OSC.
  
XML-схема поставщика OSC позволяет поставщику OSC определять действия. Сведения об активности могут включать в себя социальные сети, в которых ились элементы веб-канала активности, сведения о каждом элементе веб-канала активности (например, владелец, тип и дата публикации действия) и шаблон для отображения действия. Чтобы поддерживать отображение действий в области пользователей или карточке контакта, поставщик OSC социальной сети должен реализовать и вернуть правильные действия XML. Пример XML-канала активности см. в [XML-примере](activity-feed-xml-example.md)веб-канала активности. Дополнительные сведения о синхронизации действий друзей см. в этой [теме.](synchronizing-friends-and-activities.md) Полное определение XML-схемы поставщика OSC, включая элементы, которые являются обязательными или необязательными, см. в XML-схеме поставщика [Outlook Social Connector.](outlook-social-connector-provider-xml-schema.md) 
  
В следующем сценарии OSC динамически синхронизирует действия для человека, выбранного в области "Люди", и получает сведения о нем:
  
1. Поставщик OSC, который поддерживает синхронизацию действий по требованию, указывает, что для OSC используется **элемент getActivities** и **dynamicActivitiesLookupEx.** Поставщик OSC также задает элемент **hashFunction.** Все три элемента являются элементами **возможностей.** 
    
2. Поставщик OSC реализует методы **ISocialProvider::GetCapabilities** и [ISocialSession2::GetActivitiesEx.](isocialsession2-getactivitiesex.md) 
    
3. OsC вызывает **ISocialProvider::GetCapabilities,** чтобы проверить значение **getActivities** и **dynamicActivitiesLookupEx,** чтобы убедиться, что поставщик OSC поддерживает синхронизацию действий по требованию. OsC также отмечает значение элемента **hashFunction,** поддерживаемого поставщиком OSC. 
    
4. OsC обновляет области пользователей или карточки контакта, чтобы пользователь видел последние действия выбранного пользователя. OSC шифрует SMTP-адрес человека с помощью функции hashFunction, указанной в элементе **hashFunction,** образуя строку XML, которая соответствует определению схемы XML для элемента **hashedAddresses.** 
    
5. OSC вызывает **ISocialSession2::GetActivitiesEx,** предоставляя эту строку XML-адреса в качестве параметра _hashedAddresses,_ чтобы получить текущую коллекцию действий для этого человека в параметре _activities._ _Строка_ параметра activities соответствует определению схемы XML элемента **activityFeed.** 
    
6. На основе определения схемы XML для **activityFeed** OSC  дополнительно синтаксирует строку действий, чтобы узнать тип, дату публикации и другие сведения о каждом действии, а также способ отображения действия. 
    
7. Чтобы получить сведения о выбранном человеке, OSC вызывает [ISocialSession2::GetPeopleDetails,](isocialsession2-getpeopledetails.md)предоставляя ту же строку XML-адресов, что и аргумент _параметра personsAddresses._ Сведения о человеке возвращаются в _параметре personsCollection._ Эти сведения могут включать **firstName,** **lastName** и **emailAddress.** Параметр _personsCollection_ соответствует определению схемы XML для элемента **person.** 
    
Дополнительные сведения об указании XML для действий можно найти в следующих разделах этого раздела:
  
- [Обзор XML для элемента веб-канала активности](overview-of-xml-for-an-activity-feed-item.md)
    
- [Элемент activityDetails](activitydetails-element.md)
    
- [Элемент activityTemplateContainer](activitytemplatecontainer-element.md)
    
- [Переменные шаблона](template-variables.md)
    
- [Руководство по правильному отобралку действий](guidelines-for-properly-displaying-activities.md)
    
## <a name="see-also"></a>См. также

- [Пример XML-канала активности](activity-feed-xml-example.md)  
- [Синхронизация друзей и действий](synchronizing-friends-and-activities.md) 
- [XML для возможностей](xml-for-capabilities.md)  
- [XML для друзей](xml-for-friends.md)
- [Разработка поставщика с помощью схемы OSC XML](developing-a-provider-with-the-osc-xml-schema.md)

