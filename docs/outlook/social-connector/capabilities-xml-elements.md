---
title: Элементы XML возможностей
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1951643d-e3ca-4d04-bc0c-10d9d0b35dad
description: В таблицах этого раздела описываются элементы XML возможностей, которые сгруппировали по областям, которые они поддерживают.
ms.openlocfilehash: 6816bbdcd24eceffc47d6b9d0835a90c7089c039
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281197"
---
# <a name="capabilities-xml-elements"></a>Элементы XML возможностей

В таблицах этого раздела описываются элементы **XML** возможностей, которые сгруппировали по областям, которые они поддерживают. Значение по умолчанию для **каждого элемента возможностей** — **false.** Если элемент не указан в  XML-XML возможностей, возвращаемом методом [ISocialProvider::GetCapabilities,](isocialprovider-getcapabilities.md) значение элемента равно **false**.
  
Обзорное описание **возможностей** XML см. в [описании XML-разных возможностей.](xml-for-capabilities.md) Пример возможностей XML **см. в** [XML-примере](capabilities-xml-example.md)возможностей. Полное определение XML-схемы поставщика Microsoft Outlook Social Connector (OSC), включая элементы, которые являются обязательными или необязательными, см. в XML-схеме поставщика [Outlook Social Connector.](outlook-social-connector-provider-xml-schema.md)
  
## <a name="capabilities-for-supporting-friends"></a>Возможности для поддержки друзей

В следующей таблице показаны элементы, которые применяются к любой форме синхронизации друзей или других друзей.
  
|**Элемент**|**Описание**|
|:-----|:-----|
|**doNotFollowPerson** <br/> |Указывает, поддерживает ли поставщик вызов метода [ISocialSession::UnFollowPerson.](isocialsession-unfollowperson.md)  <br/> **followPerson** и **doNotFollowPerson — это** независимые функции поставщика OSC. Поставщик OSC может указать возможность добавления человека в качестве друга (при установке для **параметра followPerson** **true)** или удаления пользователя в качестве друга в учетной записи социальной сети (при установке для **doNotFollowPerson** этого параметра задайте для этого параметра **true).** Как правило, возможность следовать этим данным не означает возможность перестать следовать. **followPerson** — это возможность, которая не должна быть неправильно интерпретирована как действие, чтобы следовать за определенным человеком или каждым человеком в учетной записи социальной сети. **если для followPerson** **задайте true,** **это не означает, что doNotFollowPerson —** **false.**  <br/> |
|**followPerson** <br/> |Указывает, поддерживает ли поставщик вызов метода [ISocialSession::FollowPerson.](isocialsession-followperson.md) OsC проверяет **followPerson,** если **cacheFriends** имеет true (кэширование синхронизации друзей), **dynamicContactsLookup** **имеет** true (синхронизация по требованию друзей и других), или и **cacheFriends,** и **dynamicContactsLookup** являются истинными (гибридная синхронизация друзей и других).  Если поставщик задает **followPerson** как **true,** OSC отображает сетевой индикатор событий в области людей, которых отслеживает пользователь, и включает команду **on \< NetworkName \>** в меню "Добавить" **(+)** в области "Люди". Если поставщик задает **followPerson как** **false,** сетевой индикатор событий не отображается, а команда **On \< NetworkName \>** скрыта.  <br/> |
|**getFriends** <br/> |Указывает, поддерживает ли поставщик вызов метода [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) или [ISocialSession2::GetPeopleDetails.](isocialsession2-getpeopledetails.md) Если поставщик задает **для getFriends** значение **true,** OSC использует значение **cacheFriends** или **dynamicContactsLookup,** чтобы определить, разрешает ли социальная сеть хранить друзей в качестве контактных элементов Outlook или в памяти. Если поставщик задает **для getFriends** значение **false,** социальная сеть не поддерживает друзей и методы **ISocialPerson::GetFriendsAndColleagues** и **ISocialSession2::GetPeopleDetails,** а OSC игнорирует значения **cacheFriends** и **dynamicContactsLookup.**  <br/> |
   
Следующие элементы применяются только к кэшизированной синхронизации друзей или гибридной синхронизации друзей и других. Дополнительные сведения о синхронизации друзей см. в этой [теме.](synchronizing-friends-and-activities.md)
  
|**Элемент**|**Описание**|
|:-----|:-----|
|**cacheFriends** <br/> |Указывает, разрешает ли поставщик OSC хранить друзей в качестве контактных элементов Outlook. OSC проверяет **cacheFriends,** только **если getFriends** имеет **true.** Если поставщик задает **для cacheFriends** значение **true,** OSC синхронизирует друзей, кэширует их и создает папку контактов для определенных сетей в хранилище по умолчанию пользователя для других контактов. Имя папки контактов для сети является значением свойства [ISocialProvider::SocialNetworkName.](isocialprovider-socialnetworkname.md) Если поставщик задает **для cacheFriends** **false,** OSC не создает сетевую папку контактов для хранения друзей.  <br/> |
|**contactSyncRestartInterval** <br/> |Определяет интервал между попытками синхронизации сведений друзей из социальной сети (в минутах), если возникает ошибка синхронизации. OsC использует этот элемент, только если поставщик OSC поддерживает кэширование синхронизации или гибридную синхронизацию друзей с папкой контактов в социальной сети **(cacheFriends** **имеет** true).  <br/> Интервал повторной попытку по умолчанию составляет 30 минут, если только значение по умолчанию не переопределено ключом  `ContactSyncRestartInterval` под  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` . Если поставщик задает **contactSyncRestartInterval,** значение поставщика переопределит интервал повторной попытку по умолчанию, равный 30 минутам, или значение ключа реестра.  <br/> Дополнительные сведения о синхронизации сведений о друзьях и других по запросу см. в этой [теме.](synchronizing-friends-and-activities.md)  <br/> |
   
Следующие элементы применяются только к синхронизации по требованию или гибридной синхронизации друзей и других друзей.
  
|**Элемент**|**Описание**|
|:-----|:-----|
|**dynamicContactsLookup** <br/> |Указывает, поддерживает ли поставщик OSC вызов [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) для синхронизации друзей и других друзей по требованию.  <br/> OSC проверяет **dynamicContactsLookup,** только если **getFriends** имеет **true.** Значение по умолчанию для **dynamicContactsLookup** — **false.**  <br/> Если поставщик OSC указывает **dynamicContactsLookup** как **true** и **getFriends** как **true,** OSC вызывает **ISocialSession2::GetPeopleDetails при** каждом обновлении области людей. The People Pane is refreshed when the user selects another user in the People Pane or another item in the Outlook explorer window, or opens an Outlook inspector window. Динамический просмотр контактов гарантирует, что пользователь всегда видит последние изображения и данные профиля пользователя в области "Люди", но увеличивает число звонков от поставщика в социальные сети.  <br/> Если поставщик задает **dynamicContactsLookup** как **false,** OSC не будет вызывать **ISocialSession2::GetPeopleDetails** для обновления области "Люди".  <br/> |
|**showOnDemandContactsWhenMinimized** <br/> |Указывает, должна ли OSC выполнять синхронизацию по требованию для друзей и других, когда в области "Люди" свернута.  <br/> |
   
## <a name="capabilities-for-supporting-activities"></a>Возможности для поддержки действий

Следующий элемент применяется к любой форме синхронизации действий, поддерживаемых поставщиком OSC.
  
|**Элемент**|**Описание**|
|:-----|:-----|
|**getActivities** <br/> |Указывает, поддерживает ли поставщик вызовы метода [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) или [ISocialPerson::GetActivities.](isocialperson-getactivities.md) Если поставщик задает **значение getActivities** как **true,** OSC использует значение **cacheActivities** или **dynamicActivitiesLookupEx,** чтобы определить, разрешает ли сайт социальной сети хранить действия как элементы RSS Outlook или действия в памяти. Если поставщик задает **значение getActivities** как **false,** социальная сеть не поддерживает действия и методы **ISocialSession2::GetActivitiesEx** и **ISocialPerson::GetActivities,** а OSC игнорирует значения **cacheActivities** и **dynamicActivitiesLookupEx.**  <br/> |
   
Следующий элемент относится только к кэшизированной синхронизации или гибридной синхронизации действий.
  
|**Элемент**|**Описание**|
|:-----|:-----|
|**cacheActivities** <br/> |Начиная с Outlook Social Connector 2013, OSC игнорирует этот элемент, так как поставщики больше не могут синхронизировать действия, кэшировать их в скрытой папке в хранилище пользователя.  <br/> Если поставщик поддерживает действия, он должен поддерживать синхронизацию действий по запросу. Поставщик задает **для cacheActivities false** и для **dynamicActivitesLookupEx** — **true.**  OsC синхронизирует действия по запросу и кэширует действия в памяти. Кэш памяти действий обновляется с 30-минутным интервалом.  <br/> |
   
Следующие элементы применяются только к синхронизации действий по требованию или гибридной синхронизации действий.
  
|**Элемент**|**Описание**|
|:-----|:-----|
|**dynamicActivitiesLookup** <br/> |Неподготовлен в OSC 1.1.  <br/> Начиная с OSC 1.1, OSC больше не вызывает [ISocialSession::GetActivities](isocialsession-getactivities.md) и игнорирует значение **dynamicActivitiesLookup.** Чтобы поддерживать подыскание действий по требованию, установите для **cacheActivities** как **false** и **getActivities** **и dynamicActivitiesLookupEx** как **true,** и OSC будет вызывать **ISocialSession2::GetActivitiesEx**.  <br/> |
|**dynamicActivitiesLookupEx** <br/> |Указывает, поддерживает ли поставщик OSC вызов **ISocialSession2::GetActivitiesEx** для синхронизации действий по требованию.  <br/> Если поставщик OSC поддерживает синхронизацию действий по требованию, он устанавливает для **getActivities** и **dynamicActivitiesLookupEx** **true,** а **для cacheActivities** — **false.** OsC вызывает **ISocialSession2::GetActivitiesEx при** каждом обновлении области "Люди". The People Pane is refreshed when the user changes the selected item in the Outlook explorer window or opens an Outlook inspector window. Подыском динамических действий гарантирует, что пользователь всегда будет видеть последние действия в области "Люди", но увеличит число звонков от поставщика в социальные сети.  <br/> Если поставщик задает **dynamicActivitiesLookupEx** как **false,** OSC не будет вызывать **ISocialSession2::GetActivitiesEx** для людей, отображаемого в области людей.  <br/> |
|**showOnDemandActivitiesWhenMinimized** <br/> |Указывает, следует ли операционной системы выполнять синхронизацию по требованию для действий, когда в области людей свернута.  <br/> |
   
## <a name="common-capabilities-for-supporting-on-demand-or-hybrid-synchronization-of-friends-non-friends-and-activities"></a>Общие возможности для поддержки синхронизации друзей, не друзей и действий по требованию или гибридной синхронизации

|**Элемент**|**Описание**|
|:-----|:-----|
|**hashFunction** <br/> | Указывает функцию hash, поддерживаемую поставщиком OSC. Для защиты личных сведений пользователей, не включаемых в социальные сети или бизнес-приложения поставщика, OSC передает адреса электронной почты **iSocialSession2::GetPeopleDetails** и **ISocialSession2::GetActivitiesEx.**  <br/>  Если **для dynamicContactsLookup** задано значение **true** или **для dynamicActivitiesLookupEx** задано значение **true,** поставщик должен установить **для hashFunction** одно из разрешенных значений: **SHA1,** **MD5** или **CRC32MD5**. Если **hashFunction** отсутствует или указывает неверное значение, OSC возвращает ошибку.  <br/> **SHA1** — это алгоритм безопасного hash-алгоритма 1 (IETF), который [определяется [RFC3174]](https://www.rfc-editor.org/rfc/rfc3174.txt). Например, значение **sha1** для адресов электронной почты, melissa@contoso.com является  `bb81577b567262a21a4df5f6e335c1250acd7b50` .  <br/> **MD5** is Internet Engineering Task Force (IETF) MD5 Message-Digest Algorithm defined by [[RFC1321]](https://www.rfc-editor.org/rfc/rfc1321.txt). Например, значение **MD5** для адресов электронной почты, melissa@contoso.com является  `c8c39e61ca1662477b39b83d7b0a0615` .  <br/> **CRC32MD5** — это сочетание **CRC32** и **MD5,** определенных следующим образом:  <br/>  Нормализуем адрес электронной почты, удаляя в конце и в конце доску и преобразовыв все символы в нижний регистр.  <br/>  Вычисление значения **CRC32** для нормализованного адреса электронной почты и использование десятичных значений для этого значения. Если реализация возвращает подписанные integers, необходимо преобразовать подписанное в неподписаное.  <br/>  Вычислить значение **MD5** для нормализованного адреса электронной почты и использовать его в hex-представлении (с использованием нижнего регистра для A–F).  <br/>  Объединяйте эти два значения с подчеркиваемой.  <br/>  Например, значение **CRC32MD5** для адресов электронной почты melissa@contoso.com  `2149665315_c8c39e61ca1662477b39b83d7b0a0615` .  <br/> |
   
## <a name="capabilities-for-supporting-authentication-and-account-configuration"></a>Возможности для поддержки проверки подлинности и настройки учетной записи

|**Элемент**|**Описание**|
|:-----|:-----|
|**allowChangesToAutoConfigure** <br/> |Указывает, разрешает ли пользователь изменять параметры автоматической настройки, например указывать другой URL-адрес для входа.  <br/> |
|**createAccountUrl** <br/> |Если поставщик задает для **hideHyperlinks** значение **false,** при нажатии  кнопки "Щелкните здесь", чтобы создать учетную запись в диалоговом окне настройки учетной записи, URL-адрес, указанный **в createAccountUrl,** откроется в браузере по умолчанию.   <br/> |
|**displayUrl** <br/> |Указывает, должен ли OSC отображать текстовое поле **URL-адреса** для социальной сети в диалоговом окне настройки учетной записи.  <br/> |
|**forgotPasswordUrl** <br/> |Если поставщик задает **для hideHyperlinks** значение **false,** когда пользователь  нажимает кнопку "Забыли **пароль"?** В диалоговом окне настройки учетной записи в браузере по умолчанию откроется URL-адрес, указанный **по адресу forgotPasswordUrl.**  <br/> |
|**hideHyperlinks** <br/> |Указывает, должен ли OSC скрывать ссылку **"Щелкните здесь",** чтобы создать учетную запись и забыли **пароль?** Гиперссылки в диалоговом окне настройки учетной записи.  <br/> OSC 1.0 игнорирует этот параметр, и гиперссылки всегда скрыты. OSC 1.1 соблюдает значение этого параметра.  <br/> |
|**hideRememberMyPassword** <br/> |Указывает, должен ли OSC  скрывать в диалоговом окне конфигурации учетной записи поле "Запомнить мой пароль".  <br/> Если поставщик устанавливает **для hideRememberMyPassword** **true,** OSC  будет действовать так, как если бы поле "Запомнить мой пароль" не было сброшалось и пароль не сохраняется.  <br/> Если поставщик задает **для hideRememberMyPassword** задайте  **false,** OSC отобразит в диалоговом окне настройки учетной записи поле "Запомнить мой пароль".  <br/> |
|**supportsAutoConfigure** <br/> |Указывает, должен ли OSC вызывать функцию **GetAutoConfiguredSession** в интерфейсе **ISocialProvider** для автоматической настройки и входа в социальные сети для пользователя.  <br/> |
|**useLogonCached** <br/> |Указывает, поддерживает ли поставщик OSC вызов [ISocialSession2::LogonCached](isocialsession2-logoncached.md) для входа в систему с кэшными учетными данными.  <br/> Если поставщик задает **параметр useLogonCached** как **true,** OSC игнорирует параметр **useLogonWebAuth,** а OSC вызывает **ISocialSession2::LogonCached** для проверки подлинности.  <br/> Если поставщик задает **dynamicActivitiesLookupEx** как **false,** OSC не будет вызывать **ISocialSession2::LogonCached** для проверки подлинности.  <br/> |
|**useLogonWebAuth** <br/> |Указывает, должен ли OSC использовать проверку подлинности на основе форм и метод [ISocialSession::LogonWeb.](isocialsession-logonweb.md) Если поставщик задает **для useLogonWebAuth** **false,** OSC использует базовую проверку подлинности и вызывает метод [ISocialSession::Logon.](isocialsession-logon.md) Если поставщик задает **для useLogonWebAuth** **true,** OSC использует проверку подлинности на основе форм и вызывает **ISocialSession::LogonWeb.**  <br/> |
   
В зависимости от **возможностей** XML, возвращаемого поставщиком в методе **ISocialProvider::GetCapabilities,** диалоговое окно настройки учетной записи изменяется. Например, на рисунке 1 показано диалоговое окно конфигурации учетной записи для примера TestProvider. 
  
**Рисунок 1. Пример TestProvider в диалоговом окне конфигурации учетной записи**

![Информация о конфигурации примера TestProvider](media/odc_ol14_ta_OSCFigure4.jpg)
  
## <a name="see-also"></a>См. также

- [XML для возможностей](xml-for-capabilities.md)

