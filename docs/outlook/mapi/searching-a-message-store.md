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

**Относится к**: Outlook 2013 | Outlook 2016 
  
Клиентские приложения могут искать сообщения, которые соответствуют условиям поиска, в одной или более папках. Самый простой способ поиска включает применение ограничения для определения критериев и помещение результатов в папку результатов поиска, созданную явно для этого поиска или для предыдущего поиска. Не все хранилища сообщений поддерживают этот метод. 

Чтобы определить, поддерживает ли используемное хранилище сообщений использование папок результатов поиска, вызовите его метод [IMAPIProp::GetProps,](imapiprop-getprops.md) чтобы получить **свойство PR \_ STORE_SUPPORT_MASK** ([PidTagStoreSupportMask).](pidtagstoresupportmask-canonical-property.md) Если установлен STORE_SEARCH_OK флага, поиск поддерживается. Если он не установлен, вам потребуется альтернативный подход, например проверка целевых папок вручную.
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a>Поиск в одной или более папках в хранилище сообщений
  
1. Если у вас есть папка результатов поиска из предыдущего поиска, переперейти к шагу 2. В противном случае создайте папку результатов поиска:
    
    1. Получите идентификатор записи для корневой папки результатов поиска, вызывая метод [IMAPIProp::GetProps](imapiprop-getprops.md) в хранилище сообщений и запрашивая **PR_FINDER_ENTRYID** ([PidTagFinderEntryId).](pidtagfinderentryid-canonical-property.md)
        
    2. Вызовите [IMsgStore::OpenEntry,](imsgstore-openentry.md) чтобы открыть папку, представленную PR_FINDER_ENTRYID. 
        
    3. Вызовите метод [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) папки результатов поиска с установленным FOLDER_SEARCH флагом. 
    
2. Создайте ограничение для удержания критериев поиска. 
    
3. Создайте массив идентификаторов записей, которые представляют папки для поиска. Этот шаг не является необходимым, если папка результатов поиска использовалась ранее и вы хотите искать в этих же папках.
    
4. Вызовите метод [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) папки результатов поиска, указав  _lpContainerList_ на массив идентификаторов записей, а  _lpRestriction_ — на ограничение. 
    
5. Если вы зарегистрировали полные уведомления о поиске в хранилище сообщений, дождись их поступления.
    
6. Чтобы просмотреть результаты поиска, вы можете вызывать метод [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) папки результатов поиска для доступа к таблице содержимого. 
    
7. Вызовите метод [IMAPITable::QueryRows](imapitable-queryrows.md) таблицы содержимого, чтобы получить сообщения, удовлетворяющие условиям поиска. 
    

