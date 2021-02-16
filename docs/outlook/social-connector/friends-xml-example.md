---
title: Пример XML друзей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83afbdef-4f12-4673-a0c1-bbf86274558f
description: В этом разделе используется XML-строка friend, которая возвращается в Outlook Social Connector (OSC) после вызова метода ISocialPerson::GetFriendsAndColleagues. В примере показан XML-раздружения друзей для двух друзей, каждый из которых был размещен элементом person. Каждый друг указывает уникальное значение для элемента userID в социальной сети.
ms.openlocfilehash: 593019ec4dcd1b9b578bfe275fb8e6664bbd11a9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542228"
---
# <a name="friends-xml-example"></a>Пример XML друзей

В этом разделе используется XML-строка friend, которая возвращается в Outlook Social Connector (OSC) после вызова метода [ISocialPerson::GetFriendsAndColleagues.](isocialperson-getfriendsandcolleagues.md) В примере **показан** XML-раздружения друзей для двух друзей, каждый из которых был размещен **элементом person.** Каждый друг указывает уникальное значение для **элемента userID** в социальной сети. 
  
Остальные элементы XML  друзей имеют понятные имена. Подробное описание этих элементов см. в [XML для друзей.](xml-for-friends.md) 
  
## <a name="xml-example"></a>Пример XML

В следующем примере **показан** XML-xML друзей для двух пользователей в социальной сети. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<friends xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
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

- [XML-примеры поставщика OSC](osc-provider-xml-examples.md)  
- [XML-пример возможностей](capabilities-xml-example.md) 
- [Пример XML-канала активности](activity-feed-xml-example.md) 
- [XML-схема поставщика Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)

