---
title: Элементы XML возможностей
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1951643d-e3ca-4d04-bc0c-10d9d0b35dad
description: В таблицах этого раздела описывается процесс дочерние элементы возможности XML и сгруппированные по области, которые они поддерживают.
ms.openlocfilehash: 53bce69bbe22f6e950302a92b0ada21ed0f5a1f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812705"
---
# <a name="capabilities-xml-elements"></a>Элементы XML возможностей

В таблицах этого раздела описывается процесс дочерние элементы **возможности** XML и сгруппированные по области, которые они поддерживают. Значение по умолчанию для каждого элемента **capabilities** присвоено **значение false**. Если элемент не указан в **возможности** XML, возвращенный методом [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) , значение элемента равно **false**.
  
Общие сведения о **возможностях** XML в разделе [XML для возможности](xml-for-capabilities.md). [Пример XML возможности](capabilities-xml-example.md) **возможности** XML, см. Полное определение схемы XML поставщика Social Connector Microsoft Outlook (OSC), включая, какие элементы являются обязательный или необязательный см в [Outlook Social Connector поставщика XML-схему](outlook-social-connector-provider-xml-schema.md).
  
## <a name="capabilities-for-supporting-friends"></a>Возможности для поддержки друзей

В следующей таблице перечислены элементы, которые применяются к любой форме синхронизации друзей или не друзей.
  
|**Элемент**|**Описание**|
|:-----|:-----|
|**doNotFollowPerson** <br/> |Указывает, поддерживает ли поставщик вызова метода [ISocialSession::UnFollowPerson](isocialsession-unfollowperson.md) .  <br/> **followPerson** и **doNotFollowPerson** являются независимые компоненты поставщика OSC. Поставщика OSC можно указать, возможность возможность добавления пользователя как friend (параметр **followPerson** значение **true**) или удалить человеком как friend (параметр **doNotFollowPerson** значение **true**) для учетной записи социальной сети будет невозможно. Как правило не сможет выполнить не означает возможность отменить подписку. **followPerson** это возможность, и его не ошибочно как действие следовать определенным человеком или каждого пользователя для учетной записи социальных сетей. **followPerson** , **значение true** означает, что **doNotFollowPerson** имеет **значение false**.  <br/> |
|**followPerson** <br/> |Указывает, поддерживает ли поставщик вызова метода [ISocialSession::FollowPerson](isocialsession-followperson.md) . OSC проверяет **followPerson** , если **cacheFriends** **значение true** (кэшированные синхронизации друзей), **dynamicContactsLookup** — **значение true** (по требованию синхронизации друзья и не), или оба cacheFriends ** **и **dynamicContactsLookup** (гибридный синхронизации друзья и не). Если поставщик устанавливает **followPerson** **значение true**, OSC отображает значка сети в области пользователей для пользователей, которым пользователь подписан и позволяет **на \<NetworkName\> ** команд в меню **Добавить (+)** в разделе пользователи Область. Если поставщик устанавливает **followPerson** **значение false**, значка сети не отображается и **на \<NetworkName\> ** команда скрыто.  <br/> |
|**getFriends** <br/> |Указывает, является ли поставщик поддерживает вызов метода [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) или [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) . Если поставщик устанавливает **getFriends** **значение true**, OSC использует значение **cacheFriends** или **dynamicContactsLookup** , чтобы определить, позволяет ли социальной сети хранения друзья как элементов контактов Outlook или в памяти. Если поставщик устанавливает **getFriends** **значение false**, социальные сети не поддерживает друзей и **ISocialPerson::GetFriendsAndColleagues** и **ISocialSession2::GetPeopleDetails** методы и OSC игнорирует значения **cacheFriends** и **dynamicContactsLookup**.  <br/> |
   
Следующие элементы применяются только к кэшированной друзей или гибридного друзей и не являющиеся друзей. Дополнительные сведения о синхронизации друзей можно [Синхронизация друзей и действия](synchronizing-friends-and-activities.md).
  
|**Элемент**|**Описание**|
|:-----|:-----|
|**cacheFriends** <br/> |Указывает, разрешено ли поставщика OSC хранение друзей в виде элементов контактов Outlook. OSC проверяет **cacheFriends** только в том случае, если **getFriends** имеет **значение true**. Если поставщик устанавливает **cacheFriends** **значение true**, OSC синхронизирует друзья путем кэширования и создает папку Контакты относящиеся к сети в хранилище пользователя по умолчанию для контактов, friend. Имя папки, относящиеся к сети контактов — это значение свойства [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) . Если поставщик устанавливает **cacheFriends** **значение false**, OSC не создает папку Контакты сетевые параметры для контактов friend для хранения друзей.  <br/> |
|**contactSyncRestartInterval** <br/> |Определяет интервал повтора в минутах между попытками для синхронизации данных друзей из социальных сетей, при возникновении ошибки синхронизации. Этот элемент OSC используется только в том случае, если поставщика OSC поддерживает кэшированные синхронизации или папка контактов синхронизации гибридного друзей на социальные сети конкретную (**cacheFriends** имеет **значение true**).  <br/> Интервал повтора по умолчанию — 30 минут, если не переопределено по умолчанию `ContactSyncRestartInterval` ключа в разделе `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`. Если поставщик устанавливает **contactSyncRestartInterval**, значение поставщика переопределяет интервал повтора по умолчанию 30 минут или значение раздела реестра.  <br/> Дополнительные сведения о синхронизации друзей и не являющиеся друзья сведения по запросу можно [Синхронизация друзей и действия](synchronizing-friends-and-activities.md).  <br/> |
   
Следующие элементы относятся к только по запросу или гибридного друзей и не являющиеся друзей.
  
|**Элемент**|**Описание**|
|:-----|:-----|
|**dynamicContactsLookup** <br/> |Указывает, поддерживает ли поставщика OSC [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) вызова по требованию синхронизации друзья и не.  <br/> OSC проверяет **dynamicContactsLookup** только в том случае, если **getFriends** имеет **значение true**. Значение по умолчанию для **dynamicContactsLookup** имеет **значение false**.  <br/> Если поставщика OSC указывает **dynamicContactsLookup** как **true** и **getFriends** **значение true**, OSC вызывает **ISocialSession2::GetPeopleDetails** в каждом обновлении области пользователей. Области пользователей обновляется, когда пользователь выбирает другой пользователь в области пользователей или другой элемент в окне проводника Outlook или открывается в окне инспектора Outlook. Подстановки динамического контакты гарантирует, что пользователь всегда видит последние фотографии пользователя и сведений о профиле в области пользователей, но увеличивает число звонков от поставщика в социальной сети.  <br/> Если поставщик устанавливает **dynamicContactsLookup** **значение false**, OSC не вызывает **ISocialSession2::GetPeopleDetails** обновление области пользователей.  <br/> |
|**showOnDemandContactsWhenMinimized** <br/> |Указывает, будет выполнена Если OSC синхронизации по запросу для друзья и не, свернутое области пользователей.  <br/> |
   
## <a name="capabilities-for-supporting-activities"></a>Возможности для поддержки действий

Следующий элемент относится к любой форме синхронизации действия, поддерживаемые поставщика OSC.
  
|**Элемент**|**Описание**|
|:-----|:-----|
|**getActivities** <br/> |Указывает, является ли поставщик поддерживает вызовы методов [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) или [ISocialPerson::GetActivities](isocialperson-getactivities.md) . Если поставщик устанавливает **getActivities** **значение true**, OSC использует значение **cacheActivities** или **dynamicActivitiesLookupEx** , чтобы определить, допускает ли сайт социальной сети хранения действий, как элементы Outlook RSS-канал или действия в памяти. Если поставщик устанавливает **getActivities** **значение false**, социальные сети не поддерживает действия и **ISocialSession2::GetActivitiesEx** и **ISocialPerson::GetActivities** методов и OSC игнорирует значения ** cacheActivities** и **dynamicActivitiesLookupEx**.  <br/> |
   
Следующий элемент применяется только кэшированные синхронизации или синхронизации гибридного действий.
  
|**Элемент**|**Описание**|
|:-----|:-----|
|**cacheActivities** <br/> |Начиная с Outlook Social Connector 2013, OSC игнорирует этот элемент, поскольку поставщики больше не можно синхронизировать действия, кэширование их в скрытой папке в хранилище пользователя.  <br/> Если поставщик поддерживает действий, поставщик должен поддерживать синхронизацию мероприятий по запросу. Поставщик показана **cacheActivities** **значение false** и **dynamicActivitesLookupEx** **значение true**. OSC синхронизирует мероприятий по запросу и кэширует действий в памяти. На 30-минутный интервал обновления кэша памяти действий.  <br/> |
   
Следующие элементы относятся к только по запросу или гибридного действий.
  
|**Элемент**|**Описание**|
|:-----|:-----|
|**dynamicActivitiesLookup** <br/> |Не поддерживаются в OSC 1.1.  <br/> Начиная с версии OSC 1.1, OSC больше не вызывает [ISocialSession::GetActivities](isocialsession-getactivities.md) и игнорирует значение **dynamicActivitiesLookup**. Для поддержки поиска действий по запросу, задайте **cacheActivities** как **значение false** и **getActivities** и **dynamicActivitiesLookupEx** **значение true**, а OSC выполняется звонок **ISocialSession2::GetActivitiesEx**.  <br/> |
|**dynamicActivitiesLookupEx** <br/> |Указывает, поддерживает ли поставщика OSC **ISocialSession2::GetActivitiesEx** вызова по требованию синхронизации действий.  <br/> Если поставщика OSC поддерживает синхронизацию мероприятий по запросу, задает **getActivities** и **dynamicActivitiesLookupEx** как **true**и **cacheActivities** **значение false**. OSC вызывает **ISocialSession2::GetActivitiesEx** в каждом обновлении области пользователей. Области пользователей обновляется, когда пользователь изменяет выбранный элемент в окне проводника Outlook или открывается в окне инспектора Outlook. Динамических операций поиска гарантирует, что пользователь всегда будет отображаться последние действия в области пользователей, но будет увеличиваться количество вызовов от поставщика социальных сетей.  <br/> Если поставщик устанавливает **dynamicActivitiesLookupEx** **значение false**, OSC не вызывает **ISocialSession2::GetActivitiesEx** для людей, отображаемые в области пользователей.  <br/> |
|**showOnDemandActivitiesWhenMinimized** <br/> |Указывает, следует ли OSC выполнить синхронизации по запросу для мероприятий, свернутое области пользователей.  <br/> |
   
## <a name="common-capabilities-for-supporting-on-demand-or-hybrid-synchronization-of-friends-non-friends-and-activities"></a>Общие возможности для поддержки синхронизации по запросу или комбинированным друзья, не являющиеся друзей и действий

|**Элемент**|**Описание**|
|:-----|:-----|
|**hashFunction** <br/> | Указывает хэш-функции, которая поддерживает поставщика OSC. Для защиты персональные сведения для пользователей, которые не представлены в социальных сетях или бизнес-приложение поставщика OSC передает адреса электронной почты хэш **ISocialSession2::GetPeopleDetails** и **ISocialSession2:: GetActivitiesEx**.  <br/>  Если **dynamicContactsLookup** имеет значение **true** или **dynamicActivitiesLookupEx** имеет значение **true**, поставщик должен значение **hashFunction** один из допустимых значений: **SHA1**, **MD5**или **CRC32MD5**. Если **hashFunction** отсутствует или указывает неверное значение, OSC возвращает ошибку.  <br/> **SHA1** будет безопасный алгоритм хэширования 1, определенные в [[RFC3174]](http://www.rfc-editor.org/rfc/rfc3174.txt)Task Force IETF (Internet Engineering) США. Например, имеет значение **SHA1** хэшируются melissa@contoso.com адрес электронной почты `bb81577b567262a21a4df5f6e335c1250acd7b50`.  <br/> **MD5** — Task Force IETF (Internet Engineering) MD5 хэш-алгоритм определяется [[RFC1321]](http://www.rfc-editor.org/rfc/rfc1321.txt). Например, имеет значение **MD5** хэшируются melissa@contoso.com адрес электронной почты `c8c39e61ca1662477b39b83d7b0a0615`.  <br/> **CRC32MD5** состоит из **CRC32** и **MD5** определены следующим образом:  <br/>  Нормализация адрес электронной почты, удалив начальные и конечные пробелы и преобразование все символы в нижнем регистре.  <br/>  Вычисление значения **CRC32** для адреса нормализованный электронной почты и использование десятичное целое число, представляющее этого значения. Если реализация возвращает целые числа со знаком, необходимо преобразовать целое число со знаком в целое число без знака.  <br/>  Вычисление значения **MD5** для адреса нормализованный электронной почты и использование шестнадцатеричный это значение (с использованием нижнего регистра для A-F).  <br/>  Эти два значения объединить с подчеркивания.  <br/>  Например, имеет значение **CRC32MD5** хэшируются melissa@contoso.com адрес электронной почты `2149665315_c8c39e61ca1662477b39b83d7b0a0615`.  <br/> |
   
## <a name="capabilities-for-supporting-authentication-and-account-configuration"></a>Возможности для поддержки проверки подлинности и настройка учетных записей

|**Элемент**|**Описание**|
|:-----|:-----|
|**allowChangesToAutoConfigure** <br/> |Указывает, разрешено ли социальной сети пользователям изменять параметры автоматической настройки, такие как предоставление другой URL-адрес для входа.  <br/> |
|**createAccountUrl** <br/> |Если поставщик устанавливает **hideHyperlinks** как **значение false**, при нажатии кнопки в диалоговом окне " **Настройка учетных записей** " **щелкните здесь, чтобы создать учетную запись** , URL-адрес, указанный с **createAccountUrl** откроется в браузере по умолчанию.  <br/> |
|**displayUrl** <br/> |Указывает, должно ли отображаться OSC текстовое поле **URL-адрес** для социальных сетей в диалоговом окне Настройка учетной записи.  <br/> |
|**forgotPasswordUrl** <br/> |Если поставщик устанавливает **hideHyperlinks** как **значение false**, при нажатии кнопки **Забыли пароль?** в диалоговом окне **Настройка учетных записей** URL-адрес, указанный с **forgotPasswordUrl** открывается в браузере по умолчанию.  <br/> |
|**hideHyperlinks** <br/> |Указывает, следует ли OSC скрыть, **щелкните здесь, чтобы создать учетную запись** и **Забыли пароль?** гиперссылки в диалоговом окне настройки учетной записи.  <br/> OSC 1.0 игнорирует этот параметр и гиперссылок всегда являются скрытыми. OSC 1.1 обнаруживает значения этого параметра.  <br/> |
|**hideRememberMyPassword** <br/> |Указывает, следует ли OSC скрыть флажок **Сохранить пароль** в диалоговом окне настройки учетной записи.  <br/> Если поставщик устанавливает **hideRememberMyPassword** **значение true**, OSC будет действовать как в том случае, если не установлен флажок **Сохранить пароль** и не будет сохранять пароль.  <br/> Если поставщик устанавливает **hideRememberMyPassword** **значение false**, OSC будет отображаться флажок **Сохранить пароль** в диалоговом окне настройки учетной записи.  <br/> |
|**supportsAutoConfigure** <br/> |Указывает, следует ли OSC вызовите функцию **GetAutoConfiguredSession** в интерфейсе **ISocialProvider** попытаться Автоматическая настройка и войдите в социальных сетях для пользователя.  <br/> |
|**useLogonCached** <br/> |Указывает, поддерживает ли поставщика OSC вызова [ISocialSession2::LogonCached](isocialsession2-logoncached.md) выполнить вход с использованием кэшированных учетных данных.  <br/> Если поставщик устанавливает **useLogonCached** **значение true**, OSC игнорирует для **useLogonWebAuth** и OSC вызывает **ISocialSession2::LogonCached** для проверки подлинности.  <br/> Если поставщик устанавливает **dynamicActivitiesLookupEx** **значение false**, OSC не вызывает **ISocialSession2::LogonCached** для проверки подлинности.  <br/> |
|**useLogonWebAuth** <br/> |Указывает, следует ли использовать OSC проверки подлинности на основе форм и метод [ISocialSession::LogonWeb](isocialsession-logonweb.md) . Если поставщик устанавливает **useLogonWebAuth** **значение false**, OSC используется обычная проверка подлинности и вызывает метод [ISocialSession::Logon](isocialsession-logon.md) . Если поставщик устанавливает **useLogonWebAuth** **значение true**, OSC проверкой подлинности на основе форм и вызывает **ISocialSession::LogonWeb**.  <br/> |
   
В зависимости от **возможностей** XML Поставщик вернул в методе **ISocialProvider::GetCapabilities** конфигурации учетной записи диалогового окна изменяется. Например на рисунке 1 показано диалоговое окно настройки учетной записи для примера TestProvider. 
  
**На рисунке 1. Пример TestProvider в диалоговом окне Настройка учетной записи**

![Информация о конфигурации примера TestProvider](media/odc_ol14_ta_OSCFigure4.jpg)
  
## <a name="see-also"></a>См. также

- [XML-код для возможности](xml-for-capabilities.md)
