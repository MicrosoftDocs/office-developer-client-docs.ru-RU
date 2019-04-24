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
# <a name="capabilities-xml-example"></a><span data-ttu-id="36c21-104">Пример XML возможностей</span><span class="sxs-lookup"><span data-stu-id="36c21-104">Capabilities XML example</span></span>

<span data-ttu-id="36c21-105">Пример XML в этом разделе — это XML-строка, возвращаемая Outlook Social Connector (OSC) после вызова метода [исоЦиалпровидер::-Capabilities](isocialprovider-getcapabilities.md) для социальной сети.</span><span class="sxs-lookup"><span data-stu-id="36c21-105">The XML example in this topic is an XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method for a social network.</span></span> <span data-ttu-id="36c21-106">В XML-коде показано, как поставщик OSC указывает свои возможности и требования для OSC.</span><span class="sxs-lookup"><span data-stu-id="36c21-106">The XML shows how an OSC provider specifies its capabilities and requirements for the OSC.</span></span> 
  
## <a name="capabilities-for-friends"></a><span data-ttu-id="36c21-107">Возможности для друзей</span><span class="sxs-lookup"><span data-stu-id="36c21-107">Capabilities for friends</span></span>

<span data-ttu-id="36c21-108">В этом примере поставщик OSC задает следующие элементы для отображения его возможностей в поддержке функции друзей:</span><span class="sxs-lookup"><span data-stu-id="36c21-108">In this example, the OSC provider specifies the following elements to show its capabilities in supporting the friends feature:</span></span>
  
- <span data-ttu-id="36c21-109">**друзья** как **true** , чтобы указать, что поставщик OSC поддерживает программный метод [исоЦиалперсон:: жетфриендсандколлеагуес](isocialperson-getfriendsandcolleagues.md) для программного получения сведений о друзьях.</span><span class="sxs-lookup"><span data-stu-id="36c21-109">**getFriends** as **true** to indicate the OSC provider supports the [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) method to get friends' information programmatically.</span></span> 
    
- <span data-ttu-id="36c21-110">**качефриендс** как **true** для поддержки кэширования сведений о друзьях в папке "Контакты" Outlook.</span><span class="sxs-lookup"><span data-stu-id="36c21-110">**cacheFriends** as **true** to support caching friends' information in an Outlook contacts folder.</span></span> 
    
- <span data-ttu-id="36c21-111">**контактсинкрестартинтервал** как 60 указывает, что при возникновении ошибки OSC должен повторить обновление кэша каждые 60 минут.</span><span class="sxs-lookup"><span data-stu-id="36c21-111">**contactSyncRestartInterval** as 60 to indicate that on error, the OSC should retry refreshing the cache every 60 minutes.</span></span> 
    
- <span data-ttu-id="36c21-112">**фолловперсон** как **true** , чтобы указать возможность добавлять друзей в социальную сеть.</span><span class="sxs-lookup"><span data-stu-id="36c21-112">**followPerson** as **true** to indicate the ability to add friends on the social network.</span></span> 
    
- <span data-ttu-id="36c21-113">**донотфолловперсон** как **false** , чтобы указать, что поставщик OSC не поддерживает удаление пользователя в качестве друга в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="36c21-113">**doNotFollowPerson** as **false** to indicate the OSC provider does not support removing a person as a friend on the social network.</span></span> 
    
- <span data-ttu-id="36c21-114">**динамикконтактслукуп** как **false** , чтобы показать, что OSC не должен хранить информацию о друзьях в памяти.</span><span class="sxs-lookup"><span data-stu-id="36c21-114">**dynamicContactsLookup** as **false** to indicate that the OSC should not store friends' information in memory.</span></span> 
    
## <a name="capabilities-for-activities"></a><span data-ttu-id="36c21-115">Возможности для действий</span><span class="sxs-lookup"><span data-stu-id="36c21-115">Capabilities for activities</span></span>

<span data-ttu-id="36c21-116">Поставщик OSC указывает следующие элементы, чтобы показать его возможности для поддержки действий:</span><span class="sxs-lookup"><span data-stu-id="36c21-116">The OSC provider specifies the following elements to show its capability to support activities:</span></span>
  
- <span data-ttu-id="36c21-117">методические **действия** имеют **значение true** , чтобы указать, что поставщик OSC поддерживает метод [исоЦиалпрофиле:: жетактивитиесоффриендсандколлеагуес](isocialprofile-getactivitiesoffriendsandcolleagues.md) для программного получения действий друзей.</span><span class="sxs-lookup"><span data-stu-id="36c21-117">**getActivities** as **true** to indicate that the OSC provider supports the [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) method to get friends' activities programmatically.</span></span> 
    
- <span data-ttu-id="36c21-118">**качеактивитиес** в качестве значения **false** для поддержки действий по кэшированию друзей в скрытОй папке веб-канала новостей Outlook.</span><span class="sxs-lookup"><span data-stu-id="36c21-118">**cacheActivities** as **false** to support caching activities of friends in the hidden Outlook News Feed folder.</span></span> 
    
- <span data-ttu-id="36c21-119">**динамикактивитиеслукупекс** как **true** , чтобы указать, что OSC должен хранить действия друзей в памяти.</span><span class="sxs-lookup"><span data-stu-id="36c21-119">**dynamicActivitiesLookupEx** as **true** to indicate that the OSC should store friends' activities in memory.</span></span> 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a><span data-ttu-id="36c21-120">Возможности проверки подлинности и конфигурации учетной записи</span><span class="sxs-lookup"><span data-stu-id="36c21-120">Capabilities for authentication and account configuration</span></span>

<span data-ttu-id="36c21-121">Поставщик OSC указывает следующие элементы, чтобы показать его поддержку для проверки подлинности и конфигурации учетной записи:</span><span class="sxs-lookup"><span data-stu-id="36c21-121">The OSC provider specifies the following elements to show its support for authentication and account configuration:</span></span>
  
- <span data-ttu-id="36c21-122">**уселогонвебаус** как **false** , чтобы указать, что поставщик OSC поддерживает обычную проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="36c21-122">**useLogonWebAuth** as **false** to indicate that the OSC provider supports basic authentication.</span></span> 
    
- <span data-ttu-id="36c21-123">**суппортсаутоконфигуре** как **false** , чтобы показать, что OSC не должен выполнять автоматическую настройку и вход в социальную сеть для пользователя.</span><span class="sxs-lookup"><span data-stu-id="36c21-123">**supportsAutoConfigure** as **false** to indicate that the OSC should not attempt to automatically configure and log on to the social network for the user.</span></span> 
    
- <span data-ttu-id="36c21-124">**уселогонкачед** и **хидеремембермипассворд** как **false** , чтобы указать, что OSC должен запрашивать пароль каждый раз и не использовать кэшированные учетные данные для входа в систему.</span><span class="sxs-lookup"><span data-stu-id="36c21-124">**useLogonCached** and **hideRememberMyPassword** as **false** to indicate that the OSC should prompt for password every time and should not use cached logon credentials to log on.</span></span> 
    
- <span data-ttu-id="36c21-125">**дисплайурл** как **false** , чтобы показать, что OSC не должен отображать URL-адрес социальной сети в диалоговом окне Настройка учетной записи.</span><span class="sxs-lookup"><span data-stu-id="36c21-125">**displayUrl** as **false** to indicate that the OSC should not display the URL for the social network in the account configuration dialog box.</span></span> 
    
- <span data-ttu-id="36c21-126">**хидехиперлинкс** как **false** , чтобы указать, что поставщик OSC поддерживает только существующие учетные записи с известными паролями, а OSC не должен отображать этот **элемент, чтобы создать учетную запись** и **забыли пароль?** гиперссылки в разделе диалоговое окно "Настройка учетной записи".</span><span class="sxs-lookup"><span data-stu-id="36c21-126">**hideHyperlinks** as **false** to indicate that the OSC provider supports only existing accounts with known passwords, and the OSC should not display the **Click here to create an account** and **Forgot your password?** hyperlinks in the account configuration dialog box.</span></span> 
    
## <a name="xml-example"></a><span data-ttu-id="36c21-127">Пример XML</span><span class="sxs-lookup"><span data-stu-id="36c21-127">XML example</span></span>

<span data-ttu-id="36c21-128">В следующем примере показан XML-код **возможностей** поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="36c21-128">The following example shows the **capabilities** XML of an OSC provider.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="36c21-129">См. также</span><span class="sxs-lookup"><span data-stu-id="36c21-129">See also</span></span>

- [<span data-ttu-id="36c21-130">Примеры XML-кода поставщика OSC</span><span class="sxs-lookup"><span data-stu-id="36c21-130">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="36c21-131">XML для возможностей</span><span class="sxs-lookup"><span data-stu-id="36c21-131">XML for Capabilities</span></span>](xml-for-capabilities.md)  
- [<span data-ttu-id="36c21-132">Пример XML-кода друзей</span><span class="sxs-lookup"><span data-stu-id="36c21-132">Friends XML Example</span></span>](friends-xml-example.md)  
- [<span data-ttu-id="36c21-133">Пример XML-канала активности</span><span class="sxs-lookup"><span data-stu-id="36c21-133">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)  
- [<span data-ttu-id="36c21-134">Схема XML поставщика социальных соединителей Outlook</span><span class="sxs-lookup"><span data-stu-id="36c21-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

