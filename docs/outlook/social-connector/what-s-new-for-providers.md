---
title: Новые возможности для поставщиков
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92f59a0d-3834-424d-ad81-167fdeba9bd0
description: В этом разделе перечислены основные изменения в Outlook Social Connector 2013 (OSC). Здесь представлено сравнение функций, доступных между Outlook Social Connector 2013 и Outlook Social Connector 1.1.
ms.openlocfilehash: 6b735555d312c149d7dc8b827990b96bfc229678
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435455"
---
# <a name="whats-new-for-providers"></a>Новые возможности для поставщиков

В этом разделе перечислены основные изменения в Outlook Social Connector 2013 (OSC). Здесь представлено сравнение функций, доступных между Outlook Social Connector 2013 и Outlook Social Connector 1.1. Здесь также описываются элементы интерфейса и элементы XML, которые были добавлены, изменены или являются неподготовленными. 
  
В Office 2013 OSC работает не только с Outlook, но и с SharePoint Server, SharePoint Workspace, клиентом Lync и всеми другими клиентские приложения Office, которые поддерживают сведения о присутствии и карточку контакта. Поставщик OSC может вывести обновления социальных данных на вкладку **"НОВЫЕ** ВОЗМОЖНОСТИ" в области пользователей Outlook, а также в карточке контакта. 
  
В Outlook Social Connector 2013 внесены следующие важные изменения: 
  
- Если поставщик поддерживает отображение действий, он всегда синхронизирует действия по запросу и больше не использует ранее кэшизированные действия. Это означает, что поставщик сохраняет действия друзей и других людей в памяти для отображения более текущих действий.
    
- Из соображений безопасности поставщики, которые взаимодействуют с серверами через Интернет, должны использовать протокол HTTPS (Hypertext Transfer Protocol (HTTP) с протоколом SSL. В противном случае существует риск перехвата или передачи адресов электронной почты, действий в социальных сетях и других пользовательских данных во время передачи.
    
- Если у вас есть поставщики, которые работают с более ранней версией Outlook, для поддержки Office 2013, необходимо обновить пакет установки. Дополнительные [сведения см. в](installation-checklist.md) контрольных списках установки. 
    
В следующей таблице показана доступность различных функций в Outlook Social Connector 2013 по сравнению с Outlook Social Connector 1.1.
  
|**Функция**|**Outlook Social Connector 2013**|**Outlook Social Connector 1.1**|
|:-----|:-----|:-----|
|Пользовательский интерфейс конечных пользователей  <br/> |SharePoint Server, SharePoint Workspace, клиент Lync, карточка контакта во всех клиентских приложениях Office и область "Люди" в Outlook  <br/> |People Pane in Outlook  <br/> |
|Обычная проверка подлинности  <br/> |Да  <br/> |Да  <br/> |
|Проверка подлинности на основе форм  <br/> |Да  <br/> |Да  <br/> |
|Кэширование проверки подлинности  <br/> |Да  <br/> |Да  <br/> |
|Кэшизированная синхронизация друзей с папкой контактов в хранилище по умолчанию  <br/> |Да  <br/> |Да  <br/> |
|Синхронизация кэшных действий для друзей со скрытой папкой **"Newsfeed"**  <br/> |Нет  <br/> |Да  <br/> |
|Синхронизация по требованию (изображение, имя, название) для друзей и других пользователей в сети  <br/> |Да  <br/> |Да  <br/> |
|Синхронизация действий по запросу для друзей и других пользователей в сети  <br/> |Да  <br/> |Да  <br/> |
|Follow on network  <br/> |Да  <br/> |Да  <br/> |
|Не следовать по сети  <br/> |Да  <br/> |Да  <br/> |
|Посетите страницу профиля пользователя  <br/> |По ссылке  <br/> |Через сетевой индикатор событий  <br/> |
|Наблюдение за настройками конфиденциальности в социальной сети (например, отображение профиля и действий пользователей, которые не являются друзьями, которые позволяют просматривать такие данные)  <br/> |Да  <br/> |Да  <br/> |
|Hashed email addresses passed to provider  <br/> |Да  <br/> |Да  <br/> |

<a name="OlSocialConnector_Changes"> </a>

## <a name="changes-from-the-previous-version-of-osc-provider-extensibility"></a>Изменения, внесенные в предыдущую версию extensibility поставщика OSC

В следующей таблице показаны члены, добавленные или неподготовленные из соответствующего интерфейса.
  
|**Интерфейс и член**|**Comment**|
|:-----|:-----|
|**ISocialProfile::GetActivitiesOfFriendsAndColleagues** <br/> |Неподготовлен в Outlook Social Connector 2013. Обратите **внимание, что ISocialSession::GetActivities** также был неподготовлен с Outlook Social Connector 1.1.  <br/> Для синхронизации веб-каналов активности необходимо реализовать метод [ISocialSession2::GetActivitiesEx.](isocialsession2-getactivitiesex.md) Установите **для dynamicActivitiesLookupEx** **true,** что позволит OSC вызвать **ISocialSession2::GetActivitiesEx.**  <br/> |
   
В следующей таблице показаны измененные элементы схемы.
  
|**Элемент Schema**|**Comment**|
|:-----|:-----|
|**capabilities** <br/> |Добавлено в Outlook Social Connector 2013: **элемент allowChangesToAutoConfigure.**  <br/> Неподготовлен в Outlook Social Connector 2013: **элемент cacheActivities.**  <br/> |
|**person** <br/> |Добавлено в Outlook Social Connector 2013: **askmeabout**, **businessAddress**, **businessCity**, **businessCountryOrRegion**, **businessState**, **businessZip**, **industries**, **interests**, **location**, **otherAddress**, **otherCity**, **otherCountryOrRegion**, **otherState**, **otherZip**, **skills**, **schools,** and **website** elements.  <br/> |
   
## <a name="see-also"></a>См. также

- [XML для возможностей](xml-for-capabilities.md)
- [XML для друзей](xml-for-friends.md)
- [Начало разработки поставщика Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

