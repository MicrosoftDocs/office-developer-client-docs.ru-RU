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
# <a name="ipstxemulatespooler"></a><span data-ttu-id="f8b47-103">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="f8b47-103">IPSTX::EmulateSpooler</span></span>

  
  
<span data-ttu-id="f8b47-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8b47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8b47-105">Задает локальный магазин, чтобы подражать диспетчеру Outlook протоколов, чтобы перенаправление исходяющих сообщений на сервер.</span><span class="sxs-lookup"><span data-stu-id="f8b47-105">Sets a local store to emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span>
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 <span data-ttu-id="f8b47-106">_fEmulate_</span><span class="sxs-lookup"><span data-stu-id="f8b47-106">_fEmulate_</span></span>
  
>  <span data-ttu-id="f8b47-107">[in] Установите этот параметр true, если локальный магазин должен подражать шпалеру; установите его false, если нет.</span><span class="sxs-lookup"><span data-stu-id="f8b47-107">[in] Set this parameter to True if the local store should emulate the spooler; set it to False if not.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f8b47-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="f8b47-108">Remarks</span></span>

<span data-ttu-id="f8b47-109">Локальный магазин вызывает **IPSTX::EmulateSpooler,** чтобы выступать в качестве диспетчера протоколов Outlook, выполнив перенаправление сообщений в исходяющей очереди на сервер заднего сервера (например, msN server или AOL server) для обработки.</span><span class="sxs-lookup"><span data-stu-id="f8b47-109">A local store calls **IPSTX::EmulateSpooler** to act as an Outlook Protocol Manager, spooling messages in the outgoing queue to the back-end server (for example, MSN server or AOL server) for processing.</span></span> <span data-ttu-id="f8b47-110">Эмулируя шпалер во время синхронизации, магазин вызывает эти два метода:</span><span class="sxs-lookup"><span data-stu-id="f8b47-110">Emulating a spooler during synchronization, the store then calls these two methods:</span></span> 
  
1. <span data-ttu-id="f8b47-111">**[IMsgStore::GetOutgoingQueue,](imsgstore-getoutgoingqueue.md)** чтобы получить исходятую очередь сообщений в магазине.</span><span class="sxs-lookup"><span data-stu-id="f8b47-111">**[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** to get the outgoing queue of messages in the store.</span></span> <span data-ttu-id="f8b47-112">Этот метод успешно используется только в том случае, если магазин эмулирует Outlook Диспетчер протокола.</span><span class="sxs-lookup"><span data-stu-id="f8b47-112">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> 
    
2. <span data-ttu-id="f8b47-113">**[IMsgStore::SetLockState](imsgstore-setlockstate.md)** для обеспечения единого доступа к сообщению в исходя из очереди перед отправкой на сервер.</span><span class="sxs-lookup"><span data-stu-id="f8b47-113">**[IMsgStore::SetLockState](imsgstore-setlockstate.md)** to secure sole access to a message in the outgoing queue just before sending it to the server.</span></span> <span data-ttu-id="f8b47-114">Этот метод успешно используется только в том случае, если магазин эмулирует Outlook Диспетчер протокола.</span><span class="sxs-lookup"><span data-stu-id="f8b47-114">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> <span data-ttu-id="f8b47-115">После отправки сообщения магазин снова вызывает этот метод, чтобы освободить единственный доступ к нему.</span><span class="sxs-lookup"><span data-stu-id="f8b47-115">After sending the message, the store calls this method again to release sole access to it.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="f8b47-116">С Outlook 2002 года диспетчер протокола Outlook spooler MAPI и стал отвечать за перенаправление исходяющих сообщений на серверы заднего конца.</span><span class="sxs-lookup"><span data-stu-id="f8b47-116">Since Outlook 2002, the Outlook Protocol Manager replaced the MAPI spooler and became responsible for spooling outgoing messages to back-end servers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f8b47-117">См. также</span><span class="sxs-lookup"><span data-stu-id="f8b47-117">See also</span></span>



[<span data-ttu-id="f8b47-118">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="f8b47-118">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)
  
[<span data-ttu-id="f8b47-119">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="f8b47-119">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

