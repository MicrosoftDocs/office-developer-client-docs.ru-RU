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
 
**Относится к**: Outlook 2013 | Outlook 2016 
  
### <a name="to-open-a-message"></a>Открытие сообщения
  
1. Получение идентификатора записи сообщения из одного из следующих источников:
    
   - Строка, представляющая сообщение в таблице содержимого родительской папки. Для получения дополнительных сведений о работе с таблицей содержимого папок, ознакомьтесь с [таблицами оглавления](contents-tables.md).
    
   - Элемент **лпентрид** структуры [NEWMAIL_NOTIFICATION](newmail_notification.md) , который отправляется с новым почтовым уведомлением. Более подробную информацию о получении и обработке уведомлений можно узнать в статье [обработка уведомлений](handling-notifications.md).
    
   - Вызов метода [IMAPIProp::-PROPS](imapiprop-getprops.md) сообщения, запрашивающего свойство **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). 
    
2. Вызовите один из следующих методов **OpenEntry** , чтобы открыть сообщение, задав _лпентрид_ в качестве идентификатора записи сообщения: 
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
  Самый быстрый метод можно использовать только для входящих сообщений и включает вызов метода **IMAPIFolder:: OpenEntry** для папки получения. Следующий самый быстрый метод **: метод IMsgStore:: OpenEntry** в хранилище сообщений можно использовать для всех сообщений, как это самый медленный метод, вызывающий **IMAPISession:: OpenEntry**.
    
> [!NOTE]
> Папки и их таблицы содержимого можно закрыть в любое время без отрицательного влияния на сообщения, которые открывались в них. 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a>Открытие сообщения, сохраненного на диске
  
1. Вызовите **стгопенстораже** , чтобы получить указатель интерфейса **IStorage** , передав имя файла сообщения для параметра _пвкснаме_ . 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. Вызовите **опенимсгонистг** , чтобы получить указатель интерфейса **iMessage** для доступа к сообщению. 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


