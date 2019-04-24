---
title: Пример XML друзей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83afbdef-4f12-4673-a0c1-bbf86274558f
description: 'Пример XML в этом разделе — это дружественная XML-строка, возвращаемая Outlook Social Connector (OSC) после вызова метода ИсоЦиалперсон:: Жетфриендсандколлеагуес. В примере показывается XML-файл друзей для двух друзей, каждый из которых ограничен элементом Person. Каждый друг указывает уникальное значение для элемента userID в социальной сети.'
ms.openlocfilehash: 5dbda1e4439f807ccc6e7abddd0ef654ae801fe0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280961"
---
# <a name="friends-xml-example"></a>Пример XML друзей

Пример XML в этом разделе — это дружественная XML-строка, возвращаемая Outlook Social Connector (OSC) после вызова метода [исоЦиалперсон:: жетфриендсандколлеагуес](isocialperson-getfriendsandcolleagues.md) . В примере показывается XML-файл **друзей** для двух друзей, каждый из которых ограничен элементом **Person** . Каждый друг указывает уникальное значение для элемента **UserID** в социальной сети. 
  
Остальные элементы XML-файла **друзья** имеют понятные имена. Подробное описание этих элементов приведено в статье [XML for друзья](xml-for-friends.md). 
  
## <a name="xml-example"></a>Пример XML

В следующем примере показаны XML-файлы **друзей** для двух пользователей в социальной сети. 
  
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

- [Примеры XML-кода поставщика OSC](osc-provider-xml-examples.md)  
- [Пример XML-кода возможностей](capabilities-xml-example.md) 
- [Пример XML-канала активности](activity-feed-xml-example.md) 
- [Схема XML поставщика социальных соединителей Outlook](outlook-social-connector-provider-xml-schema.md)

