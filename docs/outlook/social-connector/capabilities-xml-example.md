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
# <a name="capabilities-xml-example"></a><span data-ttu-id="77342-104">Пример XML возможностей</span><span class="sxs-lookup"><span data-stu-id="77342-104">Capabilities XML example</span></span>

<span data-ttu-id="77342-105">В примере XML в этом разделе — XML-строка возвращается в Outlook Social Connector (OSC) после его вызывает метод [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) для социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="77342-105">The XML example in this topic is an XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method for a social network.</span></span> <span data-ttu-id="77342-106">XML-кода показано, как поставщика OSC определяет его возможности и требования для OSC.</span><span class="sxs-lookup"><span data-stu-id="77342-106">The XML shows how an OSC provider specifies its capabilities and requirements for the OSC.</span></span> 
  
## <a name="capabilities-for-friends"></a><span data-ttu-id="77342-107">Возможности для друзей</span><span class="sxs-lookup"><span data-stu-id="77342-107">Capabilities for friends</span></span>

<span data-ttu-id="77342-108">В этом примере поставщика OSC определяет следующие элементы для отображения в поддержке компонентов друзьям свои возможности:</span><span class="sxs-lookup"><span data-stu-id="77342-108">In this example, the OSC provider specifies the following elements to show its capabilities in supporting the friends feature:</span></span>
  
- <span data-ttu-id="77342-109">**getFriends** как **значение true,** чтобы указать поставщика OSC поддерживает метод [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) для получения сведений о друзьях программными средствами.</span><span class="sxs-lookup"><span data-stu-id="77342-109">**getFriends** as **true** to indicate the OSC provider supports the [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) method to get friends' information programmatically.</span></span> 
    
- <span data-ttu-id="77342-110">**cacheFriends** как **true** для поддержки сведений о друзьях кэширования в папке контактов Outlook.</span><span class="sxs-lookup"><span data-stu-id="77342-110">**cacheFriends** as **true** to support caching friends' information in an Outlook contacts folder.</span></span> 
    
- <span data-ttu-id="77342-111">**contactSyncRestartInterval** как 60, чтобы указать на ошибки, OSC следует повторить, обновление кэша каждые 60 минут.</span><span class="sxs-lookup"><span data-stu-id="77342-111">**contactSyncRestartInterval** as 60 to indicate that on error, the OSC should retry refreshing the cache every 60 minutes.</span></span> 
    
- <span data-ttu-id="77342-112">**followPerson** как **true** указывает возможность добавлять друзей в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="77342-112">**followPerson** as **true** to indicate the ability to add friends on the social network.</span></span> 
    
- <span data-ttu-id="77342-113">**doNotFollowPerson** как **значение false,** чтобы указать поставщика OSC не поддерживает удаление пользователя как friend в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="77342-113">**doNotFollowPerson** as **false** to indicate the OSC provider does not support removing a person as a friend on the social network.</span></span> 
    
- <span data-ttu-id="77342-114">**dynamicContactsLookup** как **значение false,** чтобы указать, что OSC не следует хранить сведения друзей в памяти.</span><span class="sxs-lookup"><span data-stu-id="77342-114">**dynamicContactsLookup** as **false** to indicate that the OSC should not store friends' information in memory.</span></span> 
    
## <a name="capabilities-for-activities"></a><span data-ttu-id="77342-115">Возможности для мероприятий</span><span class="sxs-lookup"><span data-stu-id="77342-115">Capabilities for activities</span></span>

<span data-ttu-id="77342-116">Поставщика OSC определяет следующие элементы для отображения возможности для поддержки действий:</span><span class="sxs-lookup"><span data-stu-id="77342-116">The OSC provider specifies the following elements to show its capability to support activities:</span></span>
  
- <span data-ttu-id="77342-117">**getActivities** как **значение true,** чтобы указать, что поставщика OSC поддерживает метод [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) для получения друзей действия программными средствами.</span><span class="sxs-lookup"><span data-stu-id="77342-117">**getActivities** as **true** to indicate that the OSC provider supports the [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) method to get friends' activities programmatically.</span></span> 
    
- <span data-ttu-id="77342-118">**cacheActivities** как **значение false** для поддержки кэширования действия друзей в скрытую папку веб-канал новостей Outlook.</span><span class="sxs-lookup"><span data-stu-id="77342-118">**cacheActivities** as **false** to support caching activities of friends in the hidden Outlook News Feed folder.</span></span> 
    
- <span data-ttu-id="77342-119">**dynamicActivitiesLookupEx** как **значение true,** чтобы указать, что OSC следует хранить друзей действий в памяти.</span><span class="sxs-lookup"><span data-stu-id="77342-119">**dynamicActivitiesLookupEx** as **true** to indicate that the OSC should store friends' activities in memory.</span></span> 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a><span data-ttu-id="77342-120">Возможности настройки проверки подлинности и учетная запись</span><span class="sxs-lookup"><span data-stu-id="77342-120">Capabilities for authentication and account configuration</span></span>

<span data-ttu-id="77342-121">Поставщика OSC определяет следующие элементы для отображения поддержки проверки подлинности и настройка учетных записей:</span><span class="sxs-lookup"><span data-stu-id="77342-121">The OSC provider specifies the following elements to show its support for authentication and account configuration:</span></span>
  
- <span data-ttu-id="77342-122">**useLogonWebAuth** как **значение false,** чтобы указать, что поставщика OSC поддерживает обычную проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="77342-122">**useLogonWebAuth** as **false** to indicate that the OSC provider supports basic authentication.</span></span> 
    
- <span data-ttu-id="77342-123">**supportsAutoConfigure** как **значение false,** чтобы указать, что OSC не следует пытаться автоматически настроить и войдите в систему в социальной сети для пользователя.</span><span class="sxs-lookup"><span data-stu-id="77342-123">**supportsAutoConfigure** as **false** to indicate that the OSC should not attempt to automatically configure and log on to the social network for the user.</span></span> 
    
- <span data-ttu-id="77342-124">**useLogonCached** и **hideRememberMyPassword** как **значение false** для указания, что OSC следует запрашивать пароль каждый раз, а не следует использовать кэшированные учетные данные для входа для входа.</span><span class="sxs-lookup"><span data-stu-id="77342-124">**useLogonCached** and **hideRememberMyPassword** as **false** to indicate that the OSC should prompt for password every time and should not use cached logon credentials to log on.</span></span> 
    
- <span data-ttu-id="77342-125">**displayUrl** как **значение false,** чтобы указать, OSC не должны отображать URL-адрес для социальных сетей в диалоговом окне настройки учетной записи.</span><span class="sxs-lookup"><span data-stu-id="77342-125">**displayUrl** as **false** to indicate that the OSC should not display the URL for the social network in the account configuration dialog box.</span></span> 
    
- <span data-ttu-id="77342-126">**hideHyperlinks** как **значение false,** чтобы указать, что OSC поставщик поддерживает только существующие учетные записи с паролями, известные и OSC не должны отображаться, **щелкните здесь, чтобы создать учетную запись** и **Забыли пароль?** гиперссылки в диалоговое окно настройки учетной записи.</span><span class="sxs-lookup"><span data-stu-id="77342-126">**hideHyperlinks** as **false** to indicate that the OSC provider supports only existing accounts with known passwords, and the OSC should not display the **Click here to create an account** and **Forgot your password?** hyperlinks in the account configuration dialog box.</span></span> 
    
## <a name="xml-example"></a><span data-ttu-id="77342-127">Пример XML-файла</span><span class="sxs-lookup"><span data-stu-id="77342-127">XML example</span></span>

<span data-ttu-id="77342-128">В следующем примере показано **возможности** XML поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="77342-128">The following example shows the **capabilities** XML of an OSC provider.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="77342-129">См. также</span><span class="sxs-lookup"><span data-stu-id="77342-129">See also</span></span>

- [<span data-ttu-id="77342-130">Примеры XML поставщика OSC</span><span class="sxs-lookup"><span data-stu-id="77342-130">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="77342-131">XML-код для возможности</span><span class="sxs-lookup"><span data-stu-id="77342-131">XML for Capabilities</span></span>](xml-for-capabilities.md)  
- [<span data-ttu-id="77342-132">Пример XML друзей</span><span class="sxs-lookup"><span data-stu-id="77342-132">Friends XML Example</span></span>](friends-xml-example.md)  
- [<span data-ttu-id="77342-133">Пример XML веб-канала активности</span><span class="sxs-lookup"><span data-stu-id="77342-133">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)  
- [<span data-ttu-id="77342-134">Схема XML поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="77342-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

