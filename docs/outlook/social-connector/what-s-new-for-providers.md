---
title: Новые возможности для поставщиков
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92f59a0d-3834-424d-ad81-167fdeba9bd0
description: В этом разделе перечислены основные изменения Outlook Social Connector 2013 (OSC). В нем представлено сравнение функций, доступных между Outlook Social Connector 2013 и Outlook Social Connector 1.1.
ms.openlocfilehash: 6b735555d312c149d7dc8b827990b96bfc229678
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435455"
---
# <a name="whats-new-for-providers"></a>Новые возможности для поставщиков

В этом разделе перечислены основные изменения Outlook Social Connector 2013 (OSC). В нем представлено сравнение функций, доступных между Outlook Social Connector 2013 и Outlook Social Connector 1.1. В нем также описываются участники интерфейса и элементы XML, которые были добавлены, изменены или обесценились. 
  
В Office 2013 г. OSC работает не только с Outlook, но и с SharePoint Server, SharePoint Workspace, клиентом Lync и всеми другими Office приложениями, которые поддерживают сведения о присутствии и карточку контактов. Поставщик OSC может всплыть обновления социальных сведений в вкладке **WHAT's NEW** в области Outlook людей, а также в карточке контактов. 
  
Несколько основных изменений в Outlook Social Connector 2013 включают следующие: 
  
- Если поставщик поддерживает отображение действий, поставщик всегда синхронизирует действия по запросу и больше не зависит от ранее кэшизированных действий. Это означает, что поставщик сохраняет в памяти действия друзей и не друзей, чтобы отображать более актуальные действия.
    
- В целях безопасности поставщикам, которые взаимодействуют с серверами через Интернет, следует использовать протокол HTTPS (Протокол передачи гипертекстов (HTTP) с протоколом Secure Socket Layer (SSL)). В противном случае существует риск перехвата или разоблачеть адреса электронной почты, действия социальных сетей и другие данные пользователей во время транзита.
    
- Если у вас есть поставщики, которые работают с более ранней версией Outlook, чтобы поддерживать Office 2013 г., необходимо обновить пакет установки. Дополнительные [сведения см. в](installation-checklist.md) списке установки. 
    
В следующей таблице показана доступность различных функций в Outlook Social Connector 2013 по сравнению с Outlook Social Connector 1.1.
  
|**Функция**|**Outlook Social Connector 2013**|**Outlook Социальный соединитатель 1.1**|
|:-----|:-----|:-----|
|Интерфейс конечных пользователей  <br/> |SharePoint Сервер, SharePoint, клиент Lync, контактная карта во Office клиентских приложениях и область Outlook  <br/> |People Pane в Outlook  <br/> |
|Обычная проверка подлинности  <br/> |Да  <br/> |Да  <br/> |
|Проверка подлинности на основе форм  <br/> |Да  <br/> |Да  <br/> |
|Кэширование подлинности  <br/> |Да  <br/> |Да  <br/> |
|Cached sync for friends to contacts folder on default store  <br/> |Да  <br/> |Да  <br/> |
|Синхронизация действий кэшируются для друзей со скрытой **папкой новостей**  <br/> |Нет  <br/> |Да  <br/> |
|Синхронизация по запросу (изображение, имя, название) для друзей и не друзей в сети  <br/> |Да  <br/> |Да  <br/> |
|Синхронизация действий по запросу для друзей и не друзей в сети  <br/> |Да  <br/> |Да  <br/> |
|Следуйте по сети  <br/> |Да  <br/> |Да  <br/> |
|Не следуйте в сети  <br/> |Да  <br/> |Да  <br/> |
|Посетите страницу профилей пользователей  <br/> |По ссылке  <br/> |С помощью сетевого значка  <br/> |
|Соблюдение параметров конфиденциальности в социальной сети (например, отображение профиля и действий не друзей, которые позволяют просматривать такие)  <br/> |Да  <br/> |Да  <br/> |
|Hashed email addresses passed to provider  <br/> |Да  <br/> |Да  <br/> |

<a name="OlSocialConnector_Changes"> </a>

## <a name="changes-from-the-previous-version-of-osc-provider-extensibility"></a>Изменения по сравнению с предыдущей версией extensibility поставщика OSC

В следующей таблице показаны участники, которые были добавлены или отсутствуют от соответствующего интерфейса.
  
|**Интерфейс и член**|**Comment**|
|:-----|:-----|
|**ISocialProfile::GetActivitiesOfFriendsAndColleagues** <br/> |Deprecated in Outlook Social Connector 2013. Обратите внимание, что **iSocialSession::GetActivities** также был обесценчен с Outlook social Connector 1.1.  <br/> Чтобы синхронизировать каналы активности, необходимо реализовать [метод ISocialSession2::GetActivitiesEx.](isocialsession2-getactivitiesex.md) Установите **dynamicActivitiesLookupEx** как **истинное,** что будет побуждать OSC вызывать **ISocialSession2::GetActivitiesEx** вместо этого.  <br/> |
   
В следующей таблице показаны измененные элементы схемы.
  
|**Элемент Схемы**|**Comment**|
|:-----|:-----|
|**capabilities** <br/> |Добавлено Outlook Social Connector 2013: **allowChangesToAutoConfigure.**  <br/> Deprecated in Outlook Social Connector 2013: **cacheActivities** element.  <br/> |
|**person** <br/> |Добавлено в Outlook Social Connector 2013: **askmeabout**, **businessAddress**, **businessCity**, **businessCountryOrRegion**, **businessState**, **businessZip**, **industries**, **interests**, **location**, **otherAddress**, **otherCity**, **otherCountryOrRegion**, **otherState**, otherZip , **skills**, **schools** and **website** elements.   <br/> |
   
## <a name="see-also"></a>См. также

- [XML для возможностей](xml-for-capabilities.md)
- [XML для друзей](xml-for-friends.md)
- [Начало работы с разработкой Outlook поставщика социальных соединители](getting-started-with-developing-an-outlook-social-connector-provider.md)

