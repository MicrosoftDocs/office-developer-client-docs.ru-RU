---
title: Открытие сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 142c4975-08df-4501-9996-557aa44eafb3
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: bf633a971f7e3077ce2f418021ef183a36db8cc8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411094"
---
# <a name="opening-a-message"></a>Открытие сообщения
 
**Область применения**: Outlook 2013 | Outlook 2016 
  
### <a name="to-open-a-message"></a>Открытие сообщения
  
1. Извлечение идентификатора записи сообщения из одного из следующих источников:
    
   - Строка, которая представляет сообщение в таблице контента родительской папки. Дополнительные сведения о работе со содержимым папки см. в таблице [Contents Tables.](contents-tables.md)
    
   - Участник **lpEntryID** структуры [NEWMAIL_NOTIFICATION,](newmail_notification.md) которая отправляется с новым уведомлением по почте. Дополнительные сведения о получении и обработке уведомлений см. в сообщении [Handling Notifications.](handling-notifications.md)
    
   - Вызов для метода [IMAPIProp::GetProps](imapiprop-getprops.md) сообщения с запросом **свойства** PR_ENTRYID [(PidTagEntryId).](pidtagentryid-canonical-property.md) 
    
2. Вызов одного из следующих методов **OpenEntry,** чтобы открыть сообщение, задав идентификатор записи сообщения _lpEntryID:_ 
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
  Самый быстрый метод используется только для входящих сообщений и включает вызов метода **IMAPIFolder::OpenEntry.** Следующий самый быстрый метод, вызываемый **методом IMsgStore::OpenEntry** в магазине сообщений, может быть уместен для всех сообщений, так как это самый медленный метод, вызываемый **методом IMAPISession::OpenEntry**.
    
> [!NOTE]
> Папки и их таблицы содержимого могут быть закрыты в любое время, не затрагивая любые сообщения, открытые из них. 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a>Открытие сообщения, сохраненного на диске
  
1. Позвоните **в StgOpenStorage,** чтобы получить указатель интерфейса **IStorage,** передав имя файла сообщений для параметра _pwcsName._ 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. Вызов **OpenIMsgOnIStg** для получения **указателя интерфейса IMessage** для доступа к сообщению. 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


