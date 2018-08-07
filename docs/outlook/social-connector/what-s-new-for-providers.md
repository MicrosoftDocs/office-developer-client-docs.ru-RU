---
title: Новые возможности для поставщиков
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92f59a0d-3834-424d-ad81-167fdeba9bd0
description: В этом разделе перечислены основные изменения в Outlook Social Connector 2013 (OSC). Представляет сравнение возможностей, доступных в Outlook Social Connector 2013 и Outlook Social Connector 1.1.
ms.openlocfilehash: bdd7f7998f34a0ad096964050543f3f687bd0841
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812855"
---
# <a name="whats-new-for-providers"></a>Новые возможности для поставщиков

В этом разделе перечислены основные изменения в Outlook Social Connector 2013 (OSC). Представляет сравнение возможностей, доступных в Outlook Social Connector 2013 и Outlook Social Connector 1.1. Этот параметр также описывает члены интерфейса и XML-элементы, которые были добавлены, измененные или устаревшие. 
  
В Office 2013 OSC для работы с не только Outlook, но также SharePoint Server, SharePoint Workspace, клиент Lync и всех других приложений Office клиентских приложений, которые поддерживают сведения о присутствии и карточки контакта. Поставщика OSC можно контактной информации социальных обновлений на вкладке **новые возможности** в области пользователей Outlook, а также в карточке контакта. 
  
Ниже перечислены некоторые значительные изменения в Outlook Social Connector 2013. 
  
- Если поставщик поддерживает отображение действий, поставщик всегда синхронизирует мероприятий по запросу и больше не зависит от ранее записанных действий. Это означает, что поставщик сохраняет друзей и действия не друзей в памяти для отображения более текущей деятельности.
    
- По соображениям безопасности поставщиков, которые взаимодействуют с серверами через Интернет следует использовать протокол HTTPS (протокол HTTP (Hypertext Transfer) с помощью Secure сокетов протокол SSL). В противном случае является риском, адреса электронной почты, действия социальной сети и других пользователей перехвата и представленных в процессе передачи данных.
    
- Если у вас есть поставщики, которые работают с более ранней версии Outlook, для поддержки Office 2013, следует обновить пакет установки. [Для получения дополнительных сведений см.](installation-checklist.md) 
    
В следующей таблице показаны доступности различных функций в Outlook Social Connector 2013 по сравнению со Outlook Social Connector 1.1.
  
|**Функция**|**Outlook Social Connector 2013**|**Outlook Social Connector версии 1.1**|
|:-----|:-----|:-----|
|Интерфейс конечного пользователя  <br/> |SharePoint Server, SharePoint Workspace клиента Lync, карточки контакта в все клиентские приложения Office и области пользователей в Outlook  <br/> |Область людей в Outlook  <br/> |
|Обычная проверка подлинности  <br/> |Да  <br/> |Да  <br/> |
|Проверка подлинности на основе форм  <br/> |Да  <br/> |Да  <br/> |
|Кэшированные проверки подлинности  <br/> |Да  <br/> |Да  <br/> |
|Хранения кэшированной синхронизация для друзей для папки «Контакты» по умолчанию  <br/> |Да  <br/> |Да  <br/> |
|Синхронизация кэшированные действий для друзей скрытую папку **канала новостей**  <br/> |Нет  <br/> |Да  <br/> |
|Синхронизация по запросу (рисунок, имя, заголовок) для друзья и не-сети  <br/> |Да  <br/> |Да  <br/> |
|Синхронизация мероприятий по запросу для друзья и не-сети  <br/> |Да  <br/> |Да  <br/> |
|Выполните в сети  <br/> |Да  <br/> |Да  <br/> |
|Не выполняйте в сети  <br/> |Да  <br/> |Да  <br/> |
|Посетите страницу профиля пользователя  <br/> |С помощью ссылки  <br/> |С помощью значка сети  <br/> |
|Наблюдение за параметрами конфиденциальности в социальных сетях (например, отображение профилей и действия не друзья, разрешить просмотр такие)  <br/> |Да  <br/> |Да  <br/> |
|Адреса электронной почты хэш передан поставщика  <br/> |Да  <br/> |Да  <br/> |

<a name="OlSocialConnector_Changes"> </a>

## <a name="changes-from-the-previous-version-of-osc-provider-extensibility"></a>Изменения из предыдущей версии возможности расширения поставщика OSC

Ниже приведены члены, которые были добавлены или, удаленные из соответствующих интерфейса.
  
|**Интерфейс и члена**|**�����������**|
|:-----|:-----|
|**ISocialProfile::GetActivitiesOfFriendsAndColleagues** <br/> |Не поддерживаются в Outlook Social Connector 2013. Обратите внимание на то, что **ISocialSession::GetActivities** также устарел и начиная с Outlook Social Connector 1.1.  <br/> Чтобы синхронизировать веб-каналов активности, следует применить метод [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) . Задайте **значение true**, которое выводит запрос, OSC вместо этого вызов **ISocialSession2::GetActivitiesEx** **dynamicActivitiesLookupEx** .  <br/> |
   
В следующей таблице показаны элементы схемы, которые были изменены.
  
|**Элемент схемы**|**�����������**|
|:-----|:-----|
|**capabilities** <br/> |Добавлена в Outlook Social Connector 2013: **allowChangesToAutoConfigure** элемент.  <br/> Не поддерживаются в Outlook Social Connector 2013: **cacheActivities** элемент.  <br/> |
|**person** <br/> |Добавлена в Outlook Social Connector 2013: **askmeabout**, **businessAddress**, **businessCity**, **businessCountryOrRegion**, **businessState**, **businessZip**, **отраслях**, **интересами**, ** расположение**, элементы **otherAddress**, **otherCity**, **otherCountryOrRegion**, **otherState**, **otherZip**, **навыки**, **школ**и **веб-сайта** .  <br/> |
   
## <a name="see-also"></a>См. также

- [XML-код для возможности](xml-for-capabilities.md)
- [XML-код для друзей](xml-for-friends.md)
- [Начало разработки поставщика Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

