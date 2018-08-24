---
title: IPSTXEmulateSpooler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.EmulateSpooler
api_type:
- COM
ms.assetid: aec72e51-1f75-b2c5-76ca-626cd21fbc7d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 079b54757cfcd5c9b38365abc5a6d901e2b06724
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580721"
---
# <a name="ipstxemulatespooler"></a><span data-ttu-id="7ed74-103">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="7ed74-103">IPSTX::EmulateSpooler</span></span>

  
  
<span data-ttu-id="7ed74-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ed74-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ed74-105">Задает локальное хранилище для эмуляции диспетчера протокола Outlook очереди исходящих сообщений на сервере.</span><span class="sxs-lookup"><span data-stu-id="7ed74-105">Sets a local store to emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span>
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 <span data-ttu-id="7ed74-106">_fEmulate_</span><span class="sxs-lookup"><span data-stu-id="7ed74-106">_fEmulate_</span></span>
  
>  <span data-ttu-id="7ed74-107">[in] Присвойте этому параметру значение True, если локального хранилища эмуляции очереди; Задайте его значение False, если это не так.</span><span class="sxs-lookup"><span data-stu-id="7ed74-107">[in] Set this parameter to True if the local store should emulate the spooler; set it to False if not.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7ed74-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="7ed74-108">Remarks</span></span>

<span data-ttu-id="7ed74-109">Локальное хранилище вызывает **IPSTX::EmulateSpooler** , чтобы выступать в роли Outlook протокола диспетчера, очередь сообщений в очереди исходящих сообщений для внутреннего сервера (например, MSN сервера или сервера AOL) для обработки.</span><span class="sxs-lookup"><span data-stu-id="7ed74-109">A local store calls **IPSTX::EmulateSpooler** to act as an Outlook Protocol Manager, spooling messages in the outgoing queue to the back-end server (for example, MSN server or AOL server) for processing.</span></span> <span data-ttu-id="7ed74-110">Моделирование диспетчер очереди во время синхронизации, хранилище вызывает эти два метода:</span><span class="sxs-lookup"><span data-stu-id="7ed74-110">Emulating a spooler during synchronization, the store then calls these two methods:</span></span> 
  
1. <span data-ttu-id="7ed74-111">**[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** для получения очереди исходящих сообщений в хранилище.</span><span class="sxs-lookup"><span data-stu-id="7ed74-111">**[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** to get the outgoing queue of messages in the store.</span></span> <span data-ttu-id="7ed74-112">Этот метод выполнен успешно только в том случае, если хранилище является эмуляции диспетчера протокола Outlook.</span><span class="sxs-lookup"><span data-stu-id="7ed74-112">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> 
    
2. <span data-ttu-id="7ed74-113">**[IMsgStore::SetLockState](imsgstore-setlockstate.md)** для обеспечения безопасности единственного доступа к сообщению в очереди исходящих перед отправкой на сервер.</span><span class="sxs-lookup"><span data-stu-id="7ed74-113">**[IMsgStore::SetLockState](imsgstore-setlockstate.md)** to secure sole access to a message in the outgoing queue just before sending it to the server.</span></span> <span data-ttu-id="7ed74-114">Этот метод выполнен успешно только в том случае, если хранилище является эмуляции диспетчера протокола Outlook.</span><span class="sxs-lookup"><span data-stu-id="7ed74-114">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> <span data-ttu-id="7ed74-115">После отправки сообщения, хранилище вызывает этот метод еще раз, чтобы освободить единственного доступа к нему.</span><span class="sxs-lookup"><span data-stu-id="7ed74-115">After sending the message, the store calls this method again to release sole access to it.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="7ed74-116">Начиная с Outlook 2002 диспетчера протокола Outlook заменены диспетчер очереди MAPI и стала ответственность за исходящих сообщений буферизация фоновых серверов.</span><span class="sxs-lookup"><span data-stu-id="7ed74-116">Since Outlook 2002, the Outlook Protocol Manager replaced the MAPI spooler and became responsible for spooling outgoing messages to back-end servers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7ed74-117">См. также</span><span class="sxs-lookup"><span data-stu-id="7ed74-117">See also</span></span>



[<span data-ttu-id="7ed74-118">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="7ed74-118">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)
  
[<span data-ttu-id="7ed74-119">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="7ed74-119">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

