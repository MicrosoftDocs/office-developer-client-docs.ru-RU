---
title: Пример XML возможностей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ae1abafe-160c-47c0-b4d5-4a689c8c4cb1
description: Пример XML в этом разделе — это XML-строка, возвращаемая Outlook Social Connector (OSC) после вызова метода ИсоЦиалпровидер::-Capabilities для социальной сети. В XML-коде показано, как поставщик OSC указывает свои возможности и требования для OSC.
ms.openlocfilehash: 53bd250432e7b27d984a846d206adc812c47898f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281232"
---
# <a name="capabilities-xml-example"></a>Пример XML возможностей

Пример XML в этом разделе — это XML-строка, возвращаемая Outlook Social Connector (OSC) после вызова метода [исоЦиалпровидер::-Capabilities](isocialprovider-getcapabilities.md) для социальной сети. В XML-коде показано, как поставщик OSC указывает свои возможности и требования для OSC. 
  
## <a name="capabilities-for-friends"></a>Возможности для друзей

В этом примере поставщик OSC задает следующие элементы для отображения его возможностей в поддержке функции друзей:
  
- **друзья** как **true** , чтобы указать, что поставщик OSC поддерживает программный метод [исоЦиалперсон:: жетфриендсандколлеагуес](isocialperson-getfriendsandcolleagues.md) для программного получения сведений о друзьях. 
    
- **качефриендс** как **true** для поддержки кэширования сведений о друзьях в папке "Контакты" Outlook. 
    
- **контактсинкрестартинтервал** как 60 указывает, что при возникновении ошибки OSC должен повторить обновление кэша каждые 60 минут. 
    
- **фолловперсон** как **true** , чтобы указать возможность добавлять друзей в социальную сеть. 
    
- **донотфолловперсон** как **false** , чтобы указать, что поставщик OSC не поддерживает удаление пользователя в качестве друга в социальной сети. 
    
- **динамикконтактслукуп** как **false** , чтобы показать, что OSC не должен хранить информацию о друзьях в памяти. 
    
## <a name="capabilities-for-activities"></a>Возможности для действий

Поставщик OSC указывает следующие элементы, чтобы показать его возможности для поддержки действий:
  
- методические **действия** имеют **значение true** , чтобы указать, что поставщик OSC поддерживает метод [исоЦиалпрофиле:: жетактивитиесоффриендсандколлеагуес](isocialprofile-getactivitiesoffriendsandcolleagues.md) для программного получения действий друзей. 
    
- **качеактивитиес** в качестве значения **false** для поддержки действий по кэшированию друзей в скрытОй папке веб-канала новостей Outlook. 
    
- **динамикактивитиеслукупекс** как **true** , чтобы указать, что OSC должен хранить действия друзей в памяти. 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a>Возможности проверки подлинности и конфигурации учетной записи

Поставщик OSC указывает следующие элементы, чтобы показать его поддержку для проверки подлинности и конфигурации учетной записи:
  
- **уселогонвебаус** как **false** , чтобы указать, что поставщик OSC поддерживает обычную проверку подлинности. 
    
- **суппортсаутоконфигуре** как **false** , чтобы показать, что OSC не должен выполнять автоматическую настройку и вход в социальную сеть для пользователя. 
    
- **уселогонкачед** и **хидеремембермипассворд** как **false** , чтобы указать, что OSC должен запрашивать пароль каждый раз и не использовать кэшированные учетные данные для входа в систему. 
    
- **дисплайурл** как **false** , чтобы показать, что OSC не должен отображать URL-адрес социальной сети в диалоговом окне Настройка учетной записи. 
    
- **хидехиперлинкс** как **false** , чтобы указать, что поставщик OSC поддерживает только существующие учетные записи с известными паролями, а OSC не должен отображать этот **элемент, чтобы создать учетную запись** и **забыли пароль?** гиперссылки в разделе диалоговое окно "Настройка учетной записи". 
    
## <a name="xml-example"></a>Пример XML

В следующем примере показан XML-код **возможностей** поставщика OSC. 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<capabilities xmlns="https://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
  <getFriends>true</getFriends>
  <cacheFriends>true</cacheFriends>
  <followPerson>true</followPerson>
  <doNotFollowPerson>false</doNotFollowPerson>
  <getActivities>true</getActivities>
  <cacheActivities>false</cacheActivities>
  <displayUrl>false</displayUrl>
  <useLogonWebAuth>false</useLogonWebAuth>
  <hideHyperlinks>false</hideHyperlinks>
  <supportsAutoConfigure>false</supportsAutoConfigure>
  <contactSyncRestartInterval>60</contactSyncRestartInterval>
  <dynamicActivitiesLookupEx>true</dynamicActivitiesLookupEx>
  <dynamicContactsLookup>false</dynamicContactsLookup>
  <useLogonCached>false</useLogonCached>
  <hideRememberMyPassword>false</hideRememberMyPassword>
  <createAccountUrl>https://contoso.com/createAccount</createAccountUrl>
  <forgotPasswordUrl>https://contoso.com/forgotPassword</forgotPasswordUrl>
</capabilities>

```

## <a name="see-also"></a>См. также

- [Примеры XML-кода поставщика OSC](osc-provider-xml-examples.md)  
- [XML для возможностей](xml-for-capabilities.md)  
- [Пример XML-кода друзей](friends-xml-example.md)  
- [Пример XML-канала активности](activity-feed-xml-example.md)  
- [Схема XML поставщика социальных соединителей Outlook](outlook-social-connector-provider-xml-schema.md)

