---
title: Ипстксемулатеспулер
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315094"
---
# <a name="ipstxemulatespooler"></a><span data-ttu-id="2bb94-103">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="2bb94-103">IPSTX::EmulateSpooler</span></span>

  
  
<span data-ttu-id="2bb94-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2bb94-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2bb94-105">Задает локальное хранилище для эмуляции диспетчера протокола Outlook для постановки в очередь исходящих сообщений на сервер.</span><span class="sxs-lookup"><span data-stu-id="2bb94-105">Sets a local store to emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span>
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 <span data-ttu-id="2bb94-106">_Фемулате_</span><span class="sxs-lookup"><span data-stu-id="2bb94-106">_fEmulate_</span></span>
  
>  <span data-ttu-id="2bb94-107">возврата Установите для этого параметра значение true, если локальное хранилище должно эмулировать Диспетчер очереди печати; Если нет, задайте для него значение false.</span><span class="sxs-lookup"><span data-stu-id="2bb94-107">[in] Set this parameter to True if the local store should emulate the spooler; set it to False if not.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2bb94-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="2bb94-108">Remarks</span></span>

<span data-ttu-id="2bb94-109">Локальное хранилище вызывает **ипсткс:: емулатеспулер** для работы в качестве диспетчера протокола Outlook, отправки сообщений из очереди исходящих сообщений на внутренний сервер (например, MSN Server или AOL Server) для обработки.</span><span class="sxs-lookup"><span data-stu-id="2bb94-109">A local store calls **IPSTX::EmulateSpooler** to act as an Outlook Protocol Manager, spooling messages in the outgoing queue to the back-end server (for example, MSN server or AOL server) for processing.</span></span> <span data-ttu-id="2bb94-110">При эмуляции диспетчера очереди во время синхронизации хранилище вызывает следующие два метода:</span><span class="sxs-lookup"><span data-stu-id="2bb94-110">Emulating a spooler during synchronization, the store then calls these two methods:</span></span> 
  
1. <span data-ttu-id="2bb94-111">**[IMsgStore:: жетаутгоингкуеуе](imsgstore-getoutgoingqueue.md)** для получения очереди исходящих сообщений в хранилище.</span><span class="sxs-lookup"><span data-stu-id="2bb94-111">**[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** to get the outgoing queue of messages in the store.</span></span> <span data-ttu-id="2bb94-112">Этот метод выполняется только в том случае, если хранилище эмулирует Диспетчер протоколов Outlook.</span><span class="sxs-lookup"><span data-stu-id="2bb94-112">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> 
    
2. <span data-ttu-id="2bb94-113">**[IMsgStore:: сетлоккстате](imsgstore-setlockstate.md)** для безопасного доступа к сообщению в исходящей очереди непосредственно перед его отправкой на сервер.</span><span class="sxs-lookup"><span data-stu-id="2bb94-113">**[IMsgStore::SetLockState](imsgstore-setlockstate.md)** to secure sole access to a message in the outgoing queue just before sending it to the server.</span></span> <span data-ttu-id="2bb94-114">Этот метод выполняется только в том случае, если хранилище эмулирует Диспетчер протоколов Outlook.</span><span class="sxs-lookup"><span data-stu-id="2bb94-114">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> <span data-ttu-id="2bb94-115">После отправки сообщения хранилище повторно вызывает этот метод, чтобы освободить единственный доступ к нему.</span><span class="sxs-lookup"><span data-stu-id="2bb94-115">After sending the message, the store calls this method again to release sole access to it.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="2bb94-116">С момента поЯвления Outlook 2002 Диспетчер протоколов Outlook заменил буфер обмена MAPI и стал ответственным за постановку в очередь исходящих сообщений на внутренние серверы.</span><span class="sxs-lookup"><span data-stu-id="2bb94-116">Since Outlook 2002, the Outlook Protocol Manager replaced the MAPI spooler and became responsible for spooling outgoing messages to back-end servers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2bb94-117">См. также</span><span class="sxs-lookup"><span data-stu-id="2bb94-117">See also</span></span>



[<span data-ttu-id="2bb94-118">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="2bb94-118">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)
  
[<span data-ttu-id="2bb94-119">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="2bb94-119">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

