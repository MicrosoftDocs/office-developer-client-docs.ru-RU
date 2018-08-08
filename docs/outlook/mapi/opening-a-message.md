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
ms.openlocfilehash: 4ea75f723a2fcb242d8b9a516498855aa20cfdd4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810057"
---
# <a name="opening-a-message"></a>Открытие сообщения
 
**Относится к**: Outlook 
  
### <a name="to-open-a-message"></a>Чтобы открыть сообщение
  
1. Получить идентификатор записи сообщения от одного из следующих источников:
    
   - Строка, которая представляет сообщение в таблице содержимое из родительской папки. Дополнительные сведения о работе с таблицей содержимое папки просмотрите [Содержимое таблиц](contents-tables.md).
    
   - Член **lpEntryID** структуры [NEWMAIL_NOTIFICATION](newmail_notification.md) , отправляемые с уведомление о получении почты. Дополнительные сведения о получение и обработку уведомлений можно [Обработки уведомлений](handling-notifications.md).
    
   - Вызов метода [IMAPIProp::GetProps](imapiprop-getprops.md) сообщения, запрашивающего свойство **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). 
    
2. Вызовите один из следующих методов **OpenEntry** , чтобы открыть сообщение, параметр _lpEntryID_ для записи идентификатор сообщения: 
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
  Быстрый метод можно использовать только для входящих сообщений и включает в себя вызов метода **IMAPIFolder::OpenEntry** папку получения. Далее быстрый метод вызова метода **IMsgStore::OpenEntry** хранилища сообщений, можно использовать для всех сообщений, как способ является медленным, вызов **IMAPISession::OpenEntry**.
    
> [!NOTE]
> Папки и их содержимое таблицы можно закрыть в любое время без негативного воздействия на любые сообщения, которые были открыты из внутри них. 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a>Чтобы открыть сообщение, в котором был сохранен на диск
  
1. Вызов **StgOpenStorage** для получения указателя интерфейса **IStorage** , передав имя файла сообщения для параметра _pwcsName_ . 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. Вызовите **OpenIMsgOnIStg** , чтобы получить доступ к сообщению указателя интерфейса **IMessage** . 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


