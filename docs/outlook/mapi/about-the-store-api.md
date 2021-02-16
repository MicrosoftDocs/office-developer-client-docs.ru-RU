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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
API Магазина предоставляет различные функции магазина для хранения поставщиков. Он предоставляет следующие отсрочки, типы данных, свойства и интерфейсы.
  
Определения
  
- [Константы для API Магазина](mapi-constants.md)
    
Типы данных:
  
- **[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**
    
- **[MSCAP_SELECTOR](mscap_selector.md)**
    
Именуемые свойства:
  
- **[ArchiveSourceSupportMask](archivesourcesupportmask.md)**
    
- **[CrawlSourceSupportMask](crawlsourcesupportmask.md)**
    
- **[Размеры папок сервера отображения](display-server-folder-sizes-property.md)**
    
- **[Скрытие параметра обновления собрания](hide-meeting-update-option-property.md)**
    
- **[Сделайте тип магазина частным](make-store-type-private-property.md)**
    
- **[NoFolderScan](nofolderscan.md)**
    
> [!NOTE]
> Поставщики магазина, для которых не требуются функции этих именуемого свойства, могут просто игнорировать их и не реализовать поддержку в **интерфейсе IMAPIProp.** Так как эти свойства предоставляются начиная с Microsoft Outlook 2003 Пакет обновления 1, их добавление в магазин в более ранней версии Microsoft Outlook не влияет. Они игнорируются, если они не существуют или если их значение **false.** 
  
Свойства:
  
- **[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**
    
- **[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**
    
- **[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**
    
- **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**
    
Интерфейсы:
  
- **[IFolderSupport](ifoldersupportiunknown.md)**
    
- **[IMSCapabilities](imscapabilitiesiunknown.md)**
    
- **[IProxyStoreObject](iproxystoreobject.md)**
    
## <a name="registering-stores-for-indexing"></a>Регистрация хранилищ для индексации

Обработник протокола MAPI проверяет реестр Windows на наличие хранилищ, которые он должен индексировать в целях поиска. Поставщики магазина, которые хотят индексироваться, должны быть зарегистрированы в реестре Windows. Дополнительные сведения о регистрации поставщиков хранилища для индексации в Outlook 2013 или Outlook 2010 см. в сведениях о регистрации хранилищ для [индексации.](about-registering-stores-for-indexing.md)
  
## <a name="indexing-stores"></a>Хранилища индексации

Поставщики store MAPI могут разрешить обработщику протокола MAPI обходить и индексировать сообщения в хранилище или отправлять уведомления индекселю только при индексации сообщений. Дополнительные сведения об индексации на основе уведомлений см. в Notification-Based [Store.](about-notification-based-store-indexing.md)
  

