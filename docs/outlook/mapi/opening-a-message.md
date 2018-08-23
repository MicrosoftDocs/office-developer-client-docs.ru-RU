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
ms.openlocfilehash: e0701e64469576a8241002a6ff11299d1c343556
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582982"
---
# <a name="opening-a-message"></a><span data-ttu-id="3238d-103">Открытие сообщения</span><span class="sxs-lookup"><span data-stu-id="3238d-103">Opening a message</span></span>
 
<span data-ttu-id="3238d-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3238d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
### <a name="to-open-a-message"></a><span data-ttu-id="3238d-105">Чтобы открыть сообщение</span><span class="sxs-lookup"><span data-stu-id="3238d-105">To open a message</span></span>
  
1. <span data-ttu-id="3238d-106">Получить идентификатор записи сообщения от одного из следующих источников:</span><span class="sxs-lookup"><span data-stu-id="3238d-106">Retrieve the message's entry identifier from one of the following sources:</span></span>
    
   - <span data-ttu-id="3238d-107">Строка, которая представляет сообщение в таблице содержимое из родительской папки.</span><span class="sxs-lookup"><span data-stu-id="3238d-107">The row that represents the message in the contents table of its parent folder.</span></span> <span data-ttu-id="3238d-108">Дополнительные сведения о работе с таблицей содержимое папки просмотрите [Содержимое таблиц](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="3238d-108">For more information about working with a folder contents table, see [Contents Tables](contents-tables.md).</span></span>
    
   - <span data-ttu-id="3238d-109">Член **lpEntryID** структуры [NEWMAIL_NOTIFICATION](newmail_notification.md) , отправляемые с уведомление о получении почты.</span><span class="sxs-lookup"><span data-stu-id="3238d-109">The **lpEntryID** member of the [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that is sent with a new mail notification.</span></span> <span data-ttu-id="3238d-110">Дополнительные сведения о получение и обработку уведомлений можно [Обработки уведомлений](handling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="3238d-110">For more information about receiving and handling notifications, see [Handling Notifications](handling-notifications.md).</span></span>
    
   - <span data-ttu-id="3238d-111">Вызов метода [IMAPIProp::GetProps](imapiprop-getprops.md) сообщения, запрашивающего свойство **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3238d-111">A call to the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="3238d-112">Вызовите один из следующих методов **OpenEntry** , чтобы открыть сообщение, параметр _lpEntryID_ для записи идентификатор сообщения:</span><span class="sxs-lookup"><span data-stu-id="3238d-112">Call one of the following **OpenEntry** methods to open the message, setting  _lpEntryID_ to the message's entry identifier:</span></span> 
    
   - [<span data-ttu-id="3238d-113">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="3238d-113">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
    
   - [<span data-ttu-id="3238d-114">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="3238d-114">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
    
   - [<span data-ttu-id="3238d-115">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="3238d-115">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
    
  <span data-ttu-id="3238d-116">Быстрый метод можно использовать только для входящих сообщений и включает в себя вызов метода **IMAPIFolder::OpenEntry** папку получения.</span><span class="sxs-lookup"><span data-stu-id="3238d-116">The fastest method is usable only for incoming messages and involves calling the receive folder's **IMAPIFolder::OpenEntry** method.</span></span> <span data-ttu-id="3238d-117">Далее быстрый метод вызова метода **IMsgStore::OpenEntry** хранилища сообщений, можно использовать для всех сообщений, как способ является медленным, вызов **IMAPISession::OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="3238d-117">The next fastest method, calling the message store's **IMsgStore::OpenEntry** method, is usable for all messages as is the slowest method, calling **IMAPISession::OpenEntry**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="3238d-118">Папки и их содержимое таблицы можно закрыть в любое время без негативного воздействия на любые сообщения, которые были открыты из внутри них.</span><span class="sxs-lookup"><span data-stu-id="3238d-118">Folders and their contents tables can be closed at any time without adversely affecting any of the messages that were opened from within them.</span></span> 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a><span data-ttu-id="3238d-119">Чтобы открыть сообщение, в котором был сохранен на диск</span><span class="sxs-lookup"><span data-stu-id="3238d-119">To open a message that has been saved on disk</span></span>
  
1. <span data-ttu-id="3238d-120">Вызов **StgOpenStorage** для получения указателя интерфейса **IStorage** , передав имя файла сообщения для параметра _pwcsName_ .</span><span class="sxs-lookup"><span data-stu-id="3238d-120">Call **StgOpenStorage** to retrieve an **IStorage** interface pointer, passing the name of the message file for the  _pwcsName_ parameter.</span></span> 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. <span data-ttu-id="3238d-121">Вызовите **OpenIMsgOnIStg** , чтобы получить доступ к сообщению указателя интерфейса **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="3238d-121">Call **OpenIMsgOnIStg** to retrieve an **IMessage** interface pointer to access the message.</span></span> 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


