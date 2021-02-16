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
# <a name="opening-a-message"></a><span data-ttu-id="74bbf-103">Открытие сообщения</span><span class="sxs-lookup"><span data-stu-id="74bbf-103">Opening a message</span></span>
 
<span data-ttu-id="74bbf-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74bbf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
### <a name="to-open-a-message"></a><span data-ttu-id="74bbf-105">Открытие сообщения</span><span class="sxs-lookup"><span data-stu-id="74bbf-105">To open a message</span></span>
  
1. <span data-ttu-id="74bbf-106">Извлекать идентификатор записи сообщения из одного из следующих источников:</span><span class="sxs-lookup"><span data-stu-id="74bbf-106">Retrieve the message's entry identifier from one of the following sources:</span></span>
    
   - <span data-ttu-id="74bbf-107">Строка, представляюная сообщение в таблице содержимого родительской папки.</span><span class="sxs-lookup"><span data-stu-id="74bbf-107">The row that represents the message in the contents table of its parent folder.</span></span> <span data-ttu-id="74bbf-108">Дополнительные сведения о работе с таблицей содержимого папки см. в [таблицах содержимого.](contents-tables.md)</span><span class="sxs-lookup"><span data-stu-id="74bbf-108">For more information about working with a folder contents table, see [Contents Tables](contents-tables.md).</span></span>
    
   - <span data-ttu-id="74bbf-109">Член **lpEntryID** структуры [NEWMAIL_NOTIFICATION,](newmail_notification.md) которая отправляется с новым уведомлением о почте.</span><span class="sxs-lookup"><span data-stu-id="74bbf-109">The **lpEntryID** member of the [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that is sent with a new mail notification.</span></span> <span data-ttu-id="74bbf-110">Дополнительные сведения о получении и обработке уведомлений см. в под [управлением уведомлений.](handling-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="74bbf-110">For more information about receiving and handling notifications, see [Handling Notifications](handling-notifications.md).</span></span>
    
   - <span data-ttu-id="74bbf-111">Вызов метода [IMAPIProp::GetProps](imapiprop-getprops.md) сообщения, **запрашивающий** свойство PR_ENTRYID ([PidTagEntryId).](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="74bbf-111">A call to the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="74bbf-112">Вызовите один из следующих методов **OpenEntry,** чтобы открыть сообщение, задав  _для lpEntryID_ идентификатор записи сообщения:</span><span class="sxs-lookup"><span data-stu-id="74bbf-112">Call one of the following **OpenEntry** methods to open the message, setting  _lpEntryID_ to the message's entry identifier:</span></span> 
    
   - [<span data-ttu-id="74bbf-113">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="74bbf-113">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
    
   - [<span data-ttu-id="74bbf-114">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="74bbf-114">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
    
   - [<span data-ttu-id="74bbf-115">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="74bbf-115">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
    
  <span data-ttu-id="74bbf-116">Самый быстрый способ используется только для входящих сообщений и включает вызов метода **IMAPIFolder::OpenEntry** папки получения.</span><span class="sxs-lookup"><span data-stu-id="74bbf-116">The fastest method is usable only for incoming messages and involves calling the receive folder's **IMAPIFolder::OpenEntry** method.</span></span> <span data-ttu-id="74bbf-117">Следующий самый быстрый метод, вызываемый метод **IMsgStore::OpenEntry** в хранилище сообщений, может быть уместен для всех сообщений, так как это самый медленный метод, который вызывает **IMAPISession::OpenEntry.**</span><span class="sxs-lookup"><span data-stu-id="74bbf-117">The next fastest method, calling the message store's **IMsgStore::OpenEntry** method, is usable for all messages as is the slowest method, calling **IMAPISession::OpenEntry**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="74bbf-118">Папки и их таблицы содержимого можно закрыть в любое время, не затрагивая сообщения, открытые из них.</span><span class="sxs-lookup"><span data-stu-id="74bbf-118">Folders and their contents tables can be closed at any time without adversely affecting any of the messages that were opened from within them.</span></span> 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a><span data-ttu-id="74bbf-119">Открытие сообщения, сохраненного на диске</span><span class="sxs-lookup"><span data-stu-id="74bbf-119">To open a message that has been saved on disk</span></span>
  
1. <span data-ttu-id="74bbf-120">Вызовите **StgOpenStorage,** чтобы получить указатель интерфейса **IStorage,** передав имя файла сообщения для _параметра pwcsName._</span><span class="sxs-lookup"><span data-stu-id="74bbf-120">Call **StgOpenStorage** to retrieve an **IStorage** interface pointer, passing the name of the message file for the  _pwcsName_ parameter.</span></span> 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. <span data-ttu-id="74bbf-121">Вызовите **OpenIMsgOnIStg,** чтобы получить указатель интерфейса **IMessage** для доступа к сообщению.</span><span class="sxs-lookup"><span data-stu-id="74bbf-121">Call **OpenIMsgOnIStg** to retrieve an **IMessage** interface pointer to access the message.</span></span> 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


