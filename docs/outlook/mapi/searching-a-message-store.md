---
title: Поиск хранилища сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9e8d4639-7507-4d98-b56f-a65be369dc40
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 74b63719f6d72e3c92cbcef6fdb26ee106d4b9aa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571838"
---
# <a name="searching-a-message-store"></a>Поиск хранилища сообщений

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Клиентские приложения могут выполнять поиск по одной или нескольких папок, поиск сообщений, которые соответствуют условиям поиска. Самый простой способ поиска включает применение ограничения для определения условий и помещает результаты в папку результатов поиска, созданные явным образом для поиска или для предыдущего поиска. Не все хранилища сообщений поддерживает этот метод. 

Для определения того, является ли хранилище сообщений используется поддерживает использование результатов поиска папок, вызвать его метод [IMAPIProp::GetProps](imapiprop-getprops.md) для получения **связей с Общественностью\_STORE_SUPPORT_MASK** свойство ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). Если установлен флаг STORE_SEARCH_OK, поддерживается поиск. Если не задано, то необходимо альтернативный подход, такие как вручную проверкой целевые папки.
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a>Для поиска одного или нескольких папок в хранилище сообщений
  
1. Если у вас есть папка результатов поиска из предыдущего поиска, перейдите к шагу 2. В противном случае — создание папки результатов поиска:
    
    1. Получите идентификатор записи на корневую папку результатов поиска путем вызова метода [IMAPIProp::GetProps](imapiprop-getprops.md) хранилища сообщений и разрешения на запрос **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).
        
    2. Вызовите [IMsgStore::OpenEntry](imsgstore-openentry.md) , чтобы открыть папку, представленного PR_FINDER_ENTRYID. 
        
    3. Вызов метода [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) папки для создания папки результатов поиска с установленным флагом FOLDER_SEARCH. 
    
2. Создание ограничения для хранения условиям поиска. 
    
3. Создайте массив идентификаторов записи, представляющие папки для поиска. Этот шаг можно пропустить, если раньше папка результатов поиска, и вы хотите найти те же папки.
    
4. Вызовите метод [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) папка результатов поиска, с указанием _lpContainerList_ запись идентификатор массива и _lpRestriction_ ограничения. 
    
5. Если вы зарегистрировали уведомлений завершения поиска с хранилища сообщений, ожидание уведомления поступления.
    
6. Просмотр результатов поиска путем вызова метода [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) папки для доступа к его содержимое в таблице результатов поиска. 
    
7. Метод содержимое таблицы [IMAPITable::QueryRows](imapitable-queryrows.md) для получения сообщений, соответствующих критериям поиска. 
    

