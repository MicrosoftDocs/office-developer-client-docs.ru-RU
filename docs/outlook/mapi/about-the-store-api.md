---
title: Сведения об API хранилищ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: 'Дата последнего изменения: 25 июня 2012 года'
ms.openlocfilehash: d72df30eab5fde4288b5feba1d7045da05117bde
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579377"
---
# <a name="about-the-store-api"></a>Сведения об API хранилищ

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
API-Интерфейс хранения предоставляет функциональные возможности прочие хранилища для хранения поставщиков. Она предоставляет файлов определения, типы данных, свойств и интерфейсы.
  
Определения:
  
- [Константы для магазина API](mapi-constants.md)
    
Типы данных:
  
- **[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**
    
- **[MSCAP_SELECTOR](mscap_selector.md)**
    
Именованные свойства:
  
- **[ArchiveSourceSupportMask](archivesourcesupportmask.md)**
    
- **[CrawlSourceSupportMask](crawlsourcesupportmask.md)**
    
- **[Вывести размер папки сервера](display-server-folder-sizes-property.md)**
    
- **[Скрытие параметра обновления собрания](hide-meeting-update-option-property.md)**
    
- **[Создание хранилища типа Private](make-store-type-private-property.md)**
    
- **[NoFolderScan](nofolderscan.md)**
    
> [!NOTE]
> Поставщики хранилища, не требуются функциональные возможности, предоставляемые эти именованные свойства можно игнорировать их и не реализации поддержки в интерфейсе **IMAPIProp** . Так как эти свойства предоставляются начиная с Microsoft Outlook 2003 с пакетом обновления 1, добавляя их в хранилище в более ранней версии Microsoft Outlook не оказывает влияния. Они игнорируются, если они не существуют или если их значение равно **false**. 
  
Свойства:
  
- **[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**
    
- **[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**
    
- **[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**
    
- **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**
    
Интерфейсы:
  
- **[IFolderSupport](ifoldersupportiunknown.md)**
    
- **[IMSCapabilities](imscapabilitiesiunknown.md)**
    
- **[IProxyStoreObject](iproxystoreobject.md)**
    
## <a name="registering-stores-for-indexing"></a>Регистрация хранилища для индексации

Обработчик протокола MAPI проверяет реестра Windows для хранилищ, которые следует индексации для поиска. Поставщики хранилища, чтобы быть индексированы должна быть зарегистрирована в реестре Windows. Дополнительные сведения о регистрации поставщиков хранилища для индексации в Outlook 2010 или Outlook 2013 можно [О регистрации хранилища для индексирования](about-registering-stores-for-indexing.md).
  
## <a name="indexing-stores"></a>Индексация хранилища

Поставщики MAPI хранилища можно разрешить обработчик протокола MAPI для обхода и индексирования сообщения в хранилище или отправлять уведомления на индексатор только в том случае, если сообщений для индексирования. Дополнительные сведения о на основе уведомлений индексирования видеть [About Notification-Based хранилища индексирования](about-notification-based-store-indexing.md).
  

