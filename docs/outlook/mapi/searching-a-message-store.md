---
title: Поиск в хранилище сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9e8d4639-7507-4d98-b56f-a65be369dc40
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7240f49a15fdaea4d1f30dae578d25c3f2c1c0f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426039"
---
# <a name="searching-a-message-store"></a>Поиск в хранилище сообщений

**Область применения**: Outlook 2013 | Outlook 2016 
  
Клиентские приложения могут искать сообщения в одной или несколько папок, которые соответствуют критериям поиска. Самый простой метод поиска предполагает применение ограничения для определения критериев и размещение результатов в папку результатов поиска, созданную явно для этого поиска или для предварительного поиска. Не все хранилища сообщений поддерживают этот метод. 

Чтобы определить, используется ли хранилище сообщений с помощью папок результатов поиска, позвоните по методу [IMAPIProp::GetProps](imapiprop-getprops.md) для получения свойства PR **\_ STORE_SUPPORT_MASK** [(PidTagStoreSupportMask).](pidtagstoresupportmask-canonical-property.md) Если установлен STORE_SEARCH_OK флаг, поиск поддерживается. Если она не установлена, вам потребуется альтернативный подход, например ручная проверка целевых папок.
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a>Поиск одной или более папок в хранилище сообщений
  
1. Если у вас есть папка результатов поиска из предыдущего поиска, пропустите шаг 2. В противном случае для создания папки результатов поиска:
    
    1. Извлечение идентификатора записи для корневой папки результатов поиска путем вызова метода [IMAPIProp::GetProps](imapiprop-getprops.md) магазина сообщений и запроса PR_FINDER_ENTRYID[(PidTagFinderEntryId).](pidtagfinderentryid-canonical-property.md) 
        
    2. Позвоните [в IMsgStore::OpenEntry,](imsgstore-openentry.md) чтобы открыть папку, представленную PR_FINDER_ENTRYID. 
        
    3. Вызов метода [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) для создания папки результатов поиска с FOLDER_SEARCH флагом. 
    
2. Создайте ограничение для удержания критериев поиска. 
    
3. Создайте массив идентификаторов записей, которые представляют папки для поиска. Этот шаг не является необходимым, если папка результатов поиска была использована ранее, и вы хотите искать те же папки.
    
4. Вызовите метод [IMAPIContainer::SetSearchCriteria,](imapicontainer-setsearchcriteria.md) указав  _lpContainerList_ на массив идентификатора входа и  _lpRestriction_ к ограничению. 
    
5. Если вы зарегистрировались для поиска полных уведомлений в хранилище сообщений, дождись прибытия уведомления.
    
6. Просмотр результатов поиска с помощью метода [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) для доступа к его таблице содержимого. 
    
7. Для получения сообщений, удовлетворяющих критериям поиска, вызовите метод [IMAPITable::QueryRows](imapitable-queryrows.md) таблицы содержимого. 
    

