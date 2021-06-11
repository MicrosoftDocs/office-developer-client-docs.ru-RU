---
title: Сведения об API хранилищ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: fb9b0a4c8ac1a2f41a0fddcd746dba5fc4bae1a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405557"
---
# <a name="about-the-store-api"></a>Сведения об API хранилищ

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
API Магазина предоставляет поставщикам хранения различные функции магазина. Он предоставляет следующие defintions, типы данных, свойства и интерфейсы.
  
Определения
  
- [Константы для API магазина](mapi-constants.md)
    
Типы данных:
  
- **[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**
    
- **[MSCAP_SELECTOR](mscap_selector.md)**
    
Свойства с именем:
  
- **[ArchiveSourceSupportMask](archivesourcesupportmask.md)**
    
- **[CrawlSourceSupportMask](crawlsourcesupportmask.md)**
    
- **[Размер папки display Server](display-server-folder-sizes-property.md)**
    
- **[Скрыть параметр обновления собрания](hide-meeting-update-option-property.md)**
    
- **[Make Store Type Private](make-store-type-private-property.md)**
    
- **[NoFolderScan](nofolderscan.md)**
    
> [!NOTE]
> Поставщики магазинов, которые не требуют каких-либо функций, предлагаемых этими названными свойствами, могут просто игнорировать их и не реализовывать поддержку в **интерфейсе IMAPIProp.** Поскольку эти свойства предоставляются начиная с Microsoft Outlook 2003 Пакет обновления 1, добавление их в магазин в более ранней версии Microsoft Outlook не влияет. Они игнорируются, если они не существуют или если их значение является **ложным**. 
  
Свойства:
  
- **[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**
    
- **[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**
    
- **[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**
    
- **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**
    
Интерфейсы:
  
- **[IFolderSupport](ifoldersupportiunknown.md)**
    
- **[IMSCapabilities](imscapabilitiesiunknown.md)**
    
- **[IProxyStoreObject](iproxystoreobject.md)**
    
## <a name="registering-stores-for-indexing"></a>Регистрация магазинов для индексации

Обработник протокола MAPI проверяет реестр Windows для магазинов, который он должен индексировать для целей поиска. Поставщики магазинов, которые хотят индексироваться, должны быть зарегистрированы в Windows реестре. Дополнительные сведения о регистрации поставщиков магазинов для индексации в Outlook 2013 или Outlook 2010 г. см. в этой рубке О регистрации магазинов для [индексации.](about-registering-stores-for-indexing.md)
  
## <a name="indexing-stores"></a>Магазины индексации

Поставщики магазинов MAPI могут разрешить обработщику протоколов MAPI обход и индексировать сообщения в магазине или отправлять уведомления в индексер только при индексации сообщений. Дополнительные сведения об индексации на основе уведомлений см. в Notification-Based [Store Indexing.](about-notification-based-store-indexing.md)
  

