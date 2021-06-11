---
title: Пример XML возможностей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ae1abafe-160c-47c0-b4d5-4a689c8c4cb1
description: Пример XML в этом разделе — строка XML, возвращаемая в Outlook Social Connector (OSC) после вызова метода ISocialProvider::GetCapabilities для социальной сети. XML показывает, как поставщик OSC указывает свои возможности и требования для OSC.
ms.openlocfilehash: 3340f5b1e0718edd1a062ab817c6621c338bee42
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542263"
---
# <a name="capabilities-xml-example"></a>Пример XML возможностей

Пример XML в этом разделе — строка XML, возвращаемая в Outlook Social Connector (OSC) после вызова метода [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) для социальной сети. XML показывает, как поставщик OSC указывает свои возможности и требования для OSC. 
  
## <a name="capabilities-for-friends"></a>Возможности для друзей

В этом примере поставщик OSC указывает следующие элементы, чтобы показать свои возможности в поддержке функции друзей:
  
- **getFriends,** как верно, указывает, что поставщик OSC поддерживает метод [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) для программного получения информации друзей.  
    
- **cacheFriends как** **верный** для поддержки кэшировать сведения друзей в папке Outlook контактов. 
    
- **contactSyncRestartInterval** как 60, чтобы указать, что при ошибке OSC должен повторно освежать кэш каждые 60 минут. 
    
- **followPerson,** **как верно,** чтобы указать возможность добавления друзей в социальной сети. 
    
- **doNotFollowPerson**  как ложное, чтобы указать, что поставщик OSC не поддерживает удаление человека в качестве друга в социальной сети. 
    
- **dynamicContactsLookup**  как ложный, чтобы указать, что OSC не должен хранить сведения друзей в памяти. 
    
## <a name="capabilities-for-activities"></a>Возможности для действий

Поставщик OSC указывает следующие элементы, чтобы показать свои возможности для поддержки действий:
  
- **getActivities**  также верно, чтобы указать, что поставщик OSC поддерживает [метод ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) для программного получения действий друзей. 
    
- **cacheActivities** как **false** для поддержки кэшировать действия друзей в скрытой папке Outlook ленты новостей. 
    
- **dynamicActivitiesLookupEx** как **верно,** чтобы указать, что OSC должен хранить в памяти действия друзей. 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a>Возможности проверки подлинности и конфигурации учетной записи

Поставщик OSC указывает следующие элементы, чтобы показать свою поддержку проверки подлинности и конфигурации учетной записи:
  
- **используйтеLogonWebAuth** как **ложное,** чтобы указать, что поставщик OSC поддерживает базовую проверку подлинности. 
    
- **поддерживаетAutoConfigure** как  ложное, чтобы указать, что OSC не должна пытаться автоматически настраивать и входить в социальную сеть для пользователя. 
    
- **используйтеLogonCached** и **hideRememberMyPassword** как ложное, чтобы указать, что OSC должен каждый раз подсказывал пароль и не должен использовать кэшные учетные данные для входа в систему.  
    
- **displayUrl** как **ложное,** чтобы указать, что OSC не должен отображать URL-адрес социальной сети в диалоговом окне конфигурации учетной записи. 
    
- **hideHyperlinks**  как ложные, чтобы указать, что поставщик OSC поддерживает только существующие учетные записи с известными паролями, и OSC не должен отображать нажмите здесь, чтобы создать учетную запись и забыли **пароль?** гиперссылки в диалоговом окне конфигурации учетной записи.  
    
## <a name="xml-example"></a>Пример XML

В следующем примере показаны **возможности** XML поставщика OSC. 
  
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

- [Примеры XML поставщика OSC](osc-provider-xml-examples.md)  
- [XML для возможностей](xml-for-capabilities.md)  
- [Пример XML Friends](friends-xml-example.md)  
- [Пример ленты действий XML](activity-feed-xml-example.md)  
- [Outlook Схема поставщика социальных соединителем XML](outlook-social-connector-provider-xml-schema.md)

