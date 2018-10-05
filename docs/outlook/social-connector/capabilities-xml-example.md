---
title: Пример XML возможностей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ae1abafe-160c-47c0-b4d5-4a689c8c4cb1
description: В примере XML в этом разделе — XML-строка возвращается в Outlook Social Connector (OSC) после его вызывает метод ISocialProvider::GetCapabilities для социальных сетей. XML-кода показано, как поставщика OSC определяет его возможности и требования для OSC.
ms.openlocfilehash: 53bd250432e7b27d984a846d206adc812c47898f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389549"
---
# <a name="capabilities-xml-example"></a>Пример XML возможностей

В примере XML в этом разделе — XML-строка возвращается в Outlook Social Connector (OSC) после его вызывает метод [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) для социальных сетей. XML-кода показано, как поставщика OSC определяет его возможности и требования для OSC. 
  
## <a name="capabilities-for-friends"></a>Возможности для друзей

В этом примере поставщика OSC определяет следующие элементы для отображения в поддержке компонентов друзьям свои возможности:
  
- **getFriends** как **значение true,** чтобы указать поставщика OSC поддерживает метод [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) для получения сведений о друзьях программными средствами. 
    
- **cacheFriends** как **true** для поддержки сведений о друзьях кэширования в папке контактов Outlook. 
    
- **contactSyncRestartInterval** как 60, чтобы указать на ошибки, OSC следует повторить, обновление кэша каждые 60 минут. 
    
- **followPerson** как **true** указывает возможность добавлять друзей в социальных сетях. 
    
- **doNotFollowPerson** как **значение false,** чтобы указать поставщика OSC не поддерживает удаление пользователя как friend в социальных сетях. 
    
- **dynamicContactsLookup** как **значение false,** чтобы указать, что OSC не следует хранить сведения друзей в памяти. 
    
## <a name="capabilities-for-activities"></a>Возможности для мероприятий

Поставщика OSC определяет следующие элементы для отображения возможности для поддержки действий:
  
- **getActivities** как **значение true,** чтобы указать, что поставщика OSC поддерживает метод [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) для получения друзей действия программными средствами. 
    
- **cacheActivities** как **значение false** для поддержки кэширования действия друзей в скрытую папку веб-канал новостей Outlook. 
    
- **dynamicActivitiesLookupEx** как **значение true,** чтобы указать, что OSC следует хранить друзей действий в памяти. 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a>Возможности настройки проверки подлинности и учетная запись

Поставщика OSC определяет следующие элементы для отображения поддержки проверки подлинности и настройка учетных записей:
  
- **useLogonWebAuth** как **значение false,** чтобы указать, что поставщика OSC поддерживает обычную проверку подлинности. 
    
- **supportsAutoConfigure** как **значение false,** чтобы указать, что OSC не следует пытаться автоматически настроить и войдите в систему в социальной сети для пользователя. 
    
- **useLogonCached** и **hideRememberMyPassword** как **значение false** для указания, что OSC следует запрашивать пароль каждый раз, а не следует использовать кэшированные учетные данные для входа для входа. 
    
- **displayUrl** как **значение false,** чтобы указать, OSC не должны отображать URL-адрес для социальных сетей в диалоговом окне настройки учетной записи. 
    
- **hideHyperlinks** как **значение false,** чтобы указать, что OSC поставщик поддерживает только существующие учетные записи с паролями, известные и OSC не должны отображаться, **щелкните здесь, чтобы создать учетную запись** и **Забыли пароль?** гиперссылки в диалоговое окно настройки учетной записи. 
    
## <a name="xml-example"></a>Пример XML-файла

В следующем примере показано **возможности** XML поставщика OSC. 
  
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

- [Примеры XML поставщика OSC](osc-provider-xml-examples.md)  
- [XML-код для возможности](xml-for-capabilities.md)  
- [Пример XML друзей](friends-xml-example.md)  
- [Пример XML веб-канала активности](activity-feed-xml-example.md)  
- [Схема XML поставщика Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)

