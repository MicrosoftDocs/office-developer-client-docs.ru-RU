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
  
API Store предоставляет различные функции хранения для хранения поставщиков. Он предоставляет следующие дефинтионс, типы данных, свойства и интерфейсы.
  
Определения
  
- [Константы для API Store](mapi-constants.md)
    
Типы данных:
  
- **[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**
    
- **[MSCAP_SELECTOR](mscap_selector.md)**
    
Именованные свойства:
  
- **[ArchiveSourceSupportMask](archivesourcesupportmask.md)**
    
- **[CrawlSourceSupportMask](crawlsourcesupportmask.md)**
    
- **[Отображение размеров папок сервера](display-server-folder-sizes-property.md)**
    
- **[Параметр "Скрыть обновление собрания"](hide-meeting-update-option-property.md)**
    
- **[Сделать тип хранилища частным](make-store-type-private-property.md)**
    
- **[NoFolderScan](nofolderscan.md)**
    
> [!NOTE]
> Поставщики хранилища, не требующие функциональных возможностей, предоставляемых этими именованными свойствами, могут просто игнорировать их и не реализовать поддержку в интерфейсе **IMAPIProp** . Так как эти свойства предоставляются начиная с Microsoft Outlook 2003 с пакетом обновления 1 (SP1), добавление их в хранилище в более ранней версии Microsoft Outlook не оказывает никакого действия. Они игнорируются, если они не существуют, или если их значение равно **false**. 
  
Свойства:
  
- **[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**
    
- **[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**
    
- **[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**
    
- **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**
    
Интерфейс
  
- **[IFolderSupport](ifoldersupportiunknown.md)**
    
- **[IMSCapabilities](imscapabilitiesiunknown.md)**
    
- **[IProxyStoreObject](iproxystoreobject.md)**
    
## <a name="registering-stores-for-indexing"></a>Регистрация хранилищ для индексирования

Обработчик протокола MAPI проверяет реестр Windows для хранения, который он должен индексировать для целей поиска. Поставщики хранилища, которые требуется индексировать, должны быть зарегистрированы в реестре Windows. Дополнительные сведения о регистрации поставщиков услуг хранения для индексации в Outlook 2013 или Outlook 2010 приведены в статье [Регистрация хранилищ для индексирования](about-registering-stores-for-indexing.md).
  
## <a name="indexing-stores"></a>Индексирование хранилищ

Поставщики хранилища MAPI могут разрешить обработчику протокола MAPI обходить и индексировать сообщения в хранилище, а также отправлять уведомления индексатору только при наличии сообщений для индексирования. Более подробную информацию об индексировании хранилищ на основе уведомлений можно узнать в статье [об индексировании хранилищ на основе уведомлений](about-notification-based-store-indexing.md).
  

