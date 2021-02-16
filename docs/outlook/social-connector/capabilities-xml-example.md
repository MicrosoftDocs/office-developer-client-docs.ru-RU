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
# <a name="capabilities-xml-example"></a><span data-ttu-id="9a21c-104">Пример XML возможностей</span><span class="sxs-lookup"><span data-stu-id="9a21c-104">Capabilities XML example</span></span>

<span data-ttu-id="9a21c-105">XML-пример в этом разделе — это строка XML, которая возвращается в Outlook Social Connector (OSC) после вызова метода [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) для социальной сети.</span><span class="sxs-lookup"><span data-stu-id="9a21c-105">The XML example in this topic is an XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method for a social network.</span></span> <span data-ttu-id="9a21c-106">В XML-документе показано, как поставщик OSC определяет свои возможности и требования для OSC.</span><span class="sxs-lookup"><span data-stu-id="9a21c-106">The XML shows how an OSC provider specifies its capabilities and requirements for the OSC.</span></span> 
  
## <a name="capabilities-for-friends"></a><span data-ttu-id="9a21c-107">Возможности для друзей</span><span class="sxs-lookup"><span data-stu-id="9a21c-107">Capabilities for friends</span></span>

<span data-ttu-id="9a21c-108">В этом примере поставщик OSC указывает следующие элементы, чтобы показать свои возможности в поддержке функции друзей:</span><span class="sxs-lookup"><span data-stu-id="9a21c-108">In this example, the OSC provider specifies the following elements to show its capabilities in supporting the friends feature:</span></span>
  
- <span data-ttu-id="9a21c-109">**getFriends** как **true,** чтобы указать, что поставщик OSC поддерживает метод [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) для программного получения информации друзей.</span><span class="sxs-lookup"><span data-stu-id="9a21c-109">**getFriends** as **true** to indicate the OSC provider supports the [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) method to get friends' information programmatically.</span></span> 
    
- <span data-ttu-id="9a21c-110">**cacheFriends** как **true для** поддержки кэшировать сведения друзей в папке контактов Outlook.</span><span class="sxs-lookup"><span data-stu-id="9a21c-110">**cacheFriends** as **true** to support caching friends' information in an Outlook contacts folder.</span></span> 
    
- <span data-ttu-id="9a21c-111">**contactSyncRestartInterval** как 60, чтобы указать, что при ошибке OSC должен повторить попытку обновления кэша каждые 60 минут.</span><span class="sxs-lookup"><span data-stu-id="9a21c-111">**contactSyncRestartInterval** as 60 to indicate that on error, the OSC should retry refreshing the cache every 60 minutes.</span></span> 
    
- <span data-ttu-id="9a21c-112">**followPerson** как **true,** чтобы указать возможность добавления друзей в социальные сети.</span><span class="sxs-lookup"><span data-stu-id="9a21c-112">**followPerson** as **true** to indicate the ability to add friends on the social network.</span></span> 
    
- <span data-ttu-id="9a21c-113">**doNotFollowPerson** как **false,** чтобы указать, что поставщик OSC не поддерживает удаление человека в качестве друга в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="9a21c-113">**doNotFollowPerson** as **false** to indicate the OSC provider does not support removing a person as a friend on the social network.</span></span> 
    
- <span data-ttu-id="9a21c-114">**dynamicContactsLookup** как **false,** чтобы указать, что OSC не должен хранить сведения друзей в памяти.</span><span class="sxs-lookup"><span data-stu-id="9a21c-114">**dynamicContactsLookup** as **false** to indicate that the OSC should not store friends' information in memory.</span></span> 
    
## <a name="capabilities-for-activities"></a><span data-ttu-id="9a21c-115">Возможности для действий</span><span class="sxs-lookup"><span data-stu-id="9a21c-115">Capabilities for activities</span></span>

<span data-ttu-id="9a21c-116">Поставщик OSC указывает следующие элементы для демонстрации возможности поддержки действий:</span><span class="sxs-lookup"><span data-stu-id="9a21c-116">The OSC provider specifies the following elements to show its capability to support activities:</span></span>
  
- <span data-ttu-id="9a21c-117">**getActivities** как **true,** чтобы указать, что поставщик OSC поддерживает метод [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) для программного получения действий друзей.</span><span class="sxs-lookup"><span data-stu-id="9a21c-117">**getActivities** as **true** to indicate that the OSC provider supports the [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) method to get friends' activities programmatically.</span></span> 
    
- <span data-ttu-id="9a21c-118">**cacheActivities** as **false** to support caching activities of friends in the hidden Outlook News Feed folder.</span><span class="sxs-lookup"><span data-stu-id="9a21c-118">**cacheActivities** as **false** to support caching activities of friends in the hidden Outlook News Feed folder.</span></span> 
    
- <span data-ttu-id="9a21c-119">**dynamicActivitiesLookupEx** как **true,** чтобы указать, что OSC должен хранить действия друзей в памяти.</span><span class="sxs-lookup"><span data-stu-id="9a21c-119">**dynamicActivitiesLookupEx** as **true** to indicate that the OSC should store friends' activities in memory.</span></span> 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a><span data-ttu-id="9a21c-120">Возможности проверки подлинности и настройки учетной записи</span><span class="sxs-lookup"><span data-stu-id="9a21c-120">Capabilities for authentication and account configuration</span></span>

<span data-ttu-id="9a21c-121">Поставщик OSC указывает следующие элементы, чтобы показать поддержку проверки подлинности и конфигурации учетной записи:</span><span class="sxs-lookup"><span data-stu-id="9a21c-121">The OSC provider specifies the following elements to show its support for authentication and account configuration:</span></span>
  
- <span data-ttu-id="9a21c-122">**используйтеLogonWebAuth** как **false,** чтобы указать, что поставщик OSC поддерживает базовую проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="9a21c-122">**useLogonWebAuth** as **false** to indicate that the OSC provider supports basic authentication.</span></span> 
    
- <span data-ttu-id="9a21c-123">**supportsAutoConfigure** как **false,** чтобы указать, что OSC не должен пытаться автоматически настроить и войти в социальные сети для пользователя.</span><span class="sxs-lookup"><span data-stu-id="9a21c-123">**supportsAutoConfigure** as **false** to indicate that the OSC should not attempt to automatically configure and log on to the social network for the user.</span></span> 
    
- <span data-ttu-id="9a21c-124">**используйтеLogonCached и** **hideRememberMyPassword** как false, чтобы указать, что OSC должен каждый раз запросить пароль и не должен использовать кэш учетные данные для входа в систему. </span><span class="sxs-lookup"><span data-stu-id="9a21c-124">**useLogonCached** and **hideRememberMyPassword** as **false** to indicate that the OSC should prompt for password every time and should not use cached logon credentials to log on.</span></span> 
    
- <span data-ttu-id="9a21c-125">**displayUrl** как **false,** чтобы указать, что OSC не должен отображать URL-адрес для социальной сети в диалоговом окне конфигурации учетной записи.</span><span class="sxs-lookup"><span data-stu-id="9a21c-125">**displayUrl** as **false** to indicate that the OSC should not display the URL for the social network in the account configuration dialog box.</span></span> 
    
- <span data-ttu-id="9a21c-126">**hideHyperlinks**  как false, чтобы указать, что поставщик OSC поддерживает только существующие учетные записи с известными паролями, и OSC не должен отображать ссылку **"Щелкните здесь",** чтобы создать учетную запись и забыли **пароль?** Гиперссылки в диалоговом окне настройки учетной записи.</span><span class="sxs-lookup"><span data-stu-id="9a21c-126">**hideHyperlinks** as **false** to indicate that the OSC provider supports only existing accounts with known passwords, and the OSC should not display the **Click here to create an account** and **Forgot your password?** hyperlinks in the account configuration dialog box.</span></span> 
    
## <a name="xml-example"></a><span data-ttu-id="9a21c-127">Пример XML</span><span class="sxs-lookup"><span data-stu-id="9a21c-127">XML example</span></span>

<span data-ttu-id="9a21c-128">В следующем примере **показаны** XML-данные возможностей поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="9a21c-128">The following example shows the **capabilities** XML of an OSC provider.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="9a21c-129">См. также</span><span class="sxs-lookup"><span data-stu-id="9a21c-129">See also</span></span>

- [<span data-ttu-id="9a21c-130">XML-примеры поставщика OSC</span><span class="sxs-lookup"><span data-stu-id="9a21c-130">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="9a21c-131">XML для возможностей</span><span class="sxs-lookup"><span data-stu-id="9a21c-131">XML for Capabilities</span></span>](xml-for-capabilities.md)  
- [<span data-ttu-id="9a21c-132">Пример XML-разных друзей</span><span class="sxs-lookup"><span data-stu-id="9a21c-132">Friends XML Example</span></span>](friends-xml-example.md)  
- [<span data-ttu-id="9a21c-133">Пример XML-канала активности</span><span class="sxs-lookup"><span data-stu-id="9a21c-133">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)  
- [<span data-ttu-id="9a21c-134">XML-схема поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="9a21c-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

