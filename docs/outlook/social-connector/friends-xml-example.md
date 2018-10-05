---
title: Пример XML друзей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83afbdef-4f12-4673-a0c1-bbf86274558f
description: Пример XML в этом разделе — это строка friend XML, возвращенных в Outlook Social Connector (OSC) после его вызывает метод ISocialPerson::GetFriendsAndColleagues. В примере друзья XML для двух друзья каждый аргумент отделяется элемент человека. Каждый friend указывает уникальное значение для элемента идентификатор пользователя в социальных сетях.
ms.openlocfilehash: 5dbda1e4439f807ccc6e7abddd0ef654ae801fe0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395212"
---
# <a name="friends-xml-example"></a>Пример XML друзей

Пример XML в этом разделе — это строка friend XML, возвращенных в Outlook Social Connector (OSC) после его вызывает метод [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) . В примере **друзья** XML для двух друзья каждый аргумент отделяется элемент **человека** . Каждый friend указывает уникальное значение для элемента **идентификатор пользователя** в социальных сетях. 
  
Оставшиеся элементы **друзья** XML имеют назначении имен. Подробное описание этих элементов [XML для друзей](xml-for-friends.md)см. 
  
## <a name="xml-example"></a>Пример XML-файла

В следующем примере показано **друзья** XML для двух пользователей в социальных сетях. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<friends xmlns="https://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
  <person>
    <userID>4667647</userID>
    <firstName>Melissa</firstName>
    <lastName>MacBeth</lastName>
    <nickname></nickname>
    <fileAs>MacBeth, Melissa (Contoso Ltd.)</fileAs>
    <company>Contoso Ltd.</company>
    <title>Product Manager</title>
    <anniversary>2005-05-17</anniversary>
    <birthday>1979-08-09</birthday>
    <emailAddress>melissa@contoso.com</emailAddress>
    <emailAddress2>melissa@fabrikam.com</emailAddress2>
    <emailAddress3>melissa@adventureworks.com</emailAddress3>
    <webProfilePage>https://contoso.com/melissa</webProfilePage>
    <phone>800-555-1212</phone>
    <cell>888-555-1212</cell>
    <workPhone>425-555-1212</workPhone>
    <creationTime>2010-01-08T08:30:20-08:00</creationTime>
    <lastModificationTime>2010-01-08T11:40:14-08:00</lastModificationTime>
    <expirationTime>2010-01-09T11:40:14-08:00</expirationTime>
    <gender>female</gender>
    <index>0</index>
  </person>
  <person>
    <userID>5015012</userID>
    <firstName>Michael</firstName>
    <lastName>Affronti</lastName>
    <nickname>Mr. Social</nickname>
    <fileAs>Affronti, Michael (Contoso Ltd.)</fileAs>
    <company>Contoso Ltd.</company>
    <title>Sales Director</title>
    <anniversary>2009-06-21</anniversary>
    <birthday>1980-09-10</birthday>
    <emailAddress>michael@contoso.com</emailAddress>
    <emailAddress2>michael@fabrikam.com</emailAddress2>
    <emailAddress3>michael@adventureworks.com</emailAddress3>
    <webProfilePage>https://contoso.com/michael</webProfilePage>
    <phone>800-555-1212</phone>
    <cell>888-555-1212</cell>
    <workPhone>425-555-1212</workPhone>
    <creationTime>2010-01-08T08:30:20-08:00</creationTime>
    <lastModificationTime>2010-01-08T11:40:14-08:00</lastModificationTime>
    <expirationTime>2010-01-09T11:40:14-08:00</expirationTime>
    <gender>male</gender>
    <index>1</index>
  </person>
</friends>

```

## <a name="see-also"></a>См. также

- [Примеры XML поставщика OSC](osc-provider-xml-examples.md)  
- [Пример возможности XML](capabilities-xml-example.md) 
- [Пример XML веб-канала активности](activity-feed-xml-example.md) 
- [Схема XML поставщика Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)

