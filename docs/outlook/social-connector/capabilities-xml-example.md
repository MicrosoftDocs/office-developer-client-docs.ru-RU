---
title: Пример XML возможностей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ae1abafe-160c-47c0-b4d5-4a689c8c4cb1
description: XML-пример в этом разделе — это строка XML, которая возвращается в Outlook Social Connector (OSC) после вызова метода ISocialProvider::GetCapabilities для социальной сети. В XML-документе показано, как поставщик OSC определяет свои возможности и требования для OSC.
ms.openlocfilehash: 3340f5b1e0718edd1a062ab817c6621c338bee42
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542263"
---
# <a name="capabilities-xml-example"></a>Пример XML возможностей

XML-пример в этом разделе — это строка XML, которая возвращается в Outlook Social Connector (OSC) после вызова метода [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) для социальной сети. В XML-документе показано, как поставщик OSC определяет свои возможности и требования для OSC. 
  
## <a name="capabilities-for-friends"></a>Возможности для друзей

В этом примере поставщик OSC указывает следующие элементы, чтобы показать свои возможности в поддержке функции друзей:
  
- **getFriends** как **true,** чтобы указать, что поставщик OSC поддерживает метод [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) для программного получения информации друзей. 
    
- **cacheFriends** как **true для** поддержки кэшировать сведения друзей в папке контактов Outlook. 
    
- **contactSyncRestartInterval** как 60, чтобы указать, что при ошибке OSC должен повторить попытку обновления кэша каждые 60 минут. 
    
- **followPerson** как **true,** чтобы указать возможность добавления друзей в социальные сети. 
    
- **doNotFollowPerson** как **false,** чтобы указать, что поставщик OSC не поддерживает удаление человека в качестве друга в социальной сети. 
    
- **dynamicContactsLookup** как **false,** чтобы указать, что OSC не должен хранить сведения друзей в памяти. 
    
## <a name="capabilities-for-activities"></a>Возможности для действий

Поставщик OSC указывает следующие элементы для демонстрации возможности поддержки действий:
  
- **getActivities** как **true,** чтобы указать, что поставщик OSC поддерживает метод [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) для программного получения действий друзей. 
    
- **cacheActivities** as **false** to support caching activities of friends in the hidden Outlook News Feed folder. 
    
- **dynamicActivitiesLookupEx** как **true,** чтобы указать, что OSC должен хранить действия друзей в памяти. 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a>Возможности проверки подлинности и настройки учетной записи

Поставщик OSC указывает следующие элементы, чтобы показать поддержку проверки подлинности и конфигурации учетной записи:
  
- **используйтеLogonWebAuth** как **false,** чтобы указать, что поставщик OSC поддерживает базовую проверку подлинности. 
    
- **supportsAutoConfigure** как **false,** чтобы указать, что OSC не должен пытаться автоматически настроить и войти в социальные сети для пользователя. 
    
- **используйтеLogonCached и** **hideRememberMyPassword** как false, чтобы указать, что OSC должен каждый раз запросить пароль и не должен использовать кэш учетные данные для входа в систему.  
    
- **displayUrl** как **false,** чтобы указать, что OSC не должен отображать URL-адрес для социальной сети в диалоговом окне конфигурации учетной записи. 
    
- **hideHyperlinks**  как false, чтобы указать, что поставщик OSC поддерживает только существующие учетные записи с известными паролями, и OSC не должен отображать ссылку **"Щелкните здесь",** чтобы создать учетную запись и забыли **пароль?** Гиперссылки в диалоговом окне настройки учетной записи. 
    
## <a name="xml-example"></a>Пример XML

В следующем примере **показаны** XML-данные возможностей поставщика OSC. 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<capabilities xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
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

- [XML-примеры поставщика OSC](osc-provider-xml-examples.md)  
- [XML для возможностей](xml-for-capabilities.md)  
- [Пример XML-разных друзей](friends-xml-example.md)  
- [Пример XML-канала активности](activity-feed-xml-example.md)  
- [XML-схема поставщика Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)

