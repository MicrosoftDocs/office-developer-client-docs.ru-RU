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
ms.openlocfilehash: 024583926b5d0be638b33b1b60c5d4c5dc74d05b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438955"
---
# <a name="ipstxemulatespooler"></a><span data-ttu-id="a64a6-103">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="a64a6-103">IPSTX::EmulateSpooler</span></span>

  
  
<span data-ttu-id="a64a6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a64a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a64a6-105">Задает локальное хранилище для эмуляции диспетчера протоколов Outlook для перенаправления исходяющих сообщений на сервер.</span><span class="sxs-lookup"><span data-stu-id="a64a6-105">Sets a local store to emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span>
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 <span data-ttu-id="a64a6-106">_fEmulate_</span><span class="sxs-lookup"><span data-stu-id="a64a6-106">_fEmulate_</span></span>
  
>  <span data-ttu-id="a64a6-107">[in] Установите для этого параметра true, если локальное хранилище должно эмулировать пул; Если нет, установите для него false.</span><span class="sxs-lookup"><span data-stu-id="a64a6-107">[in] Set this parameter to True if the local store should emulate the spooler; set it to False if not.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a64a6-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="a64a6-108">Remarks</span></span>

<span data-ttu-id="a64a6-109">Локальное хранилище вызывает **IPSTX::EmulateSpooler,** чтобы выступать в качестве диспетчера протоколов Outlook, перенаправление сообщений из исходяющей очереди на тыловой сервер (например, сервер MSN или сервер AOL) для обработки.</span><span class="sxs-lookup"><span data-stu-id="a64a6-109">A local store calls **IPSTX::EmulateSpooler** to act as an Outlook Protocol Manager, spooling messages in the outgoing queue to the back-end server (for example, MSN server or AOL server) for processing.</span></span> <span data-ttu-id="a64a6-110">После эмуляции пула во время синхронизации хранилище вызывает эти два метода:</span><span class="sxs-lookup"><span data-stu-id="a64a6-110">Emulating a spooler during synchronization, the store then calls these two methods:</span></span> 
  
1. <span data-ttu-id="a64a6-111">**[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** для получения очереди исходяющих сообщений в магазине.</span><span class="sxs-lookup"><span data-stu-id="a64a6-111">**[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** to get the outgoing queue of messages in the store.</span></span> <span data-ttu-id="a64a6-112">Этот метод успешно используется, только если хранилище эмулирует диспетчер протоколов Outlook.</span><span class="sxs-lookup"><span data-stu-id="a64a6-112">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> 
    
2. <span data-ttu-id="a64a6-113">**[IMsgStore::SetLockState](imsgstore-setlockstate.md)** для защиты единственного доступа к сообщению в исходявой очереди перед отправкой на сервер.</span><span class="sxs-lookup"><span data-stu-id="a64a6-113">**[IMsgStore::SetLockState](imsgstore-setlockstate.md)** to secure sole access to a message in the outgoing queue just before sending it to the server.</span></span> <span data-ttu-id="a64a6-114">Этот метод успешно используется, только если хранилище эмулирует диспетчер протоколов Outlook.</span><span class="sxs-lookup"><span data-stu-id="a64a6-114">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> <span data-ttu-id="a64a6-115">После отправки сообщения магазин снова вызывает этот метод, чтобы освободить к нему единственный доступ.</span><span class="sxs-lookup"><span data-stu-id="a64a6-115">After sending the message, the store calls this method again to release sole access to it.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="a64a6-116">Начиная с Outlook 2002 диспетчер протоколов Outlook заменил диспетчер протокола MAPI и стал отвечать за перенаправление исходяющих сообщений на серверы.</span><span class="sxs-lookup"><span data-stu-id="a64a6-116">Since Outlook 2002, the Outlook Protocol Manager replaced the MAPI spooler and became responsible for spooling outgoing messages to back-end servers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a64a6-117">См. также</span><span class="sxs-lookup"><span data-stu-id="a64a6-117">See also</span></span>



[<span data-ttu-id="a64a6-118">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a64a6-118">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)
  
[<span data-ttu-id="a64a6-119">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="a64a6-119">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

