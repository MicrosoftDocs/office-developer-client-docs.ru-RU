---
title: IMsgStoreSetLockState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.SetLockState
api_type:
- COM
ms.assetid: 4b1176ec-4126-43f5-856d-cbab8d622825
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2efee531e277b6295b7d4bc299eefc789a805d34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571089"
---
# <a name="imsgstoresetlockstate"></a><span data-ttu-id="729ae-103">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="729ae-103">IMsgStore::SetLockState</span></span>

  
  
<span data-ttu-id="729ae-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="729ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="729ae-105">Блокирует или разблокирует сообщение.</span><span class="sxs-lookup"><span data-stu-id="729ae-105">Locks or unlocks a message.</span></span> <span data-ttu-id="729ae-106">���� ����� ���������� ������ ����������� ������� MAPI.</span><span class="sxs-lookup"><span data-stu-id="729ae-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT SetLockState(
  LPMESSAGE lpMessage,
  ULONG ulLockState  
);
```

## <a name="parameters"></a><span data-ttu-id="729ae-107">���������</span><span class="sxs-lookup"><span data-stu-id="729ae-107">Parameters</span></span>

 <span data-ttu-id="729ae-108">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="729ae-108">_lpMessage_</span></span>
  
> <span data-ttu-id="729ae-109">[in] Указатель на сообщение необходимо заблокировать или разблокировать.</span><span class="sxs-lookup"><span data-stu-id="729ae-109">[in] A pointer to the message to lock or unlock.</span></span>
    
 <span data-ttu-id="729ae-110">_ulLockState_</span><span class="sxs-lookup"><span data-stu-id="729ae-110">_ulLockState_</span></span>
  
> <span data-ttu-id="729ae-111">[in] Значение, указывающее, заблокирован или блокируется сообщения.</span><span class="sxs-lookup"><span data-stu-id="729ae-111">[in] A value that indicates whether the message should be locked or unlocked.</span></span> <span data-ttu-id="729ae-112">Допустим один из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="729ae-112">One of the following values is valid:</span></span>
    
<span data-ttu-id="729ae-113">MSG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="729ae-113">MSG_LOCKED</span></span> 
  
> <span data-ttu-id="729ae-114">Следует заблокировать сообщения.</span><span class="sxs-lookup"><span data-stu-id="729ae-114">The message should be locked.</span></span> 
    
<span data-ttu-id="729ae-115">MSG_UNLOCKED</span><span class="sxs-lookup"><span data-stu-id="729ae-115">MSG_UNLOCKED</span></span> 
  
> <span data-ttu-id="729ae-116">Сообщение необходимо разблокировать.</span><span class="sxs-lookup"><span data-stu-id="729ae-116">The message should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="729ae-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="729ae-117">Return value</span></span>

<span data-ttu-id="729ae-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="729ae-118">S_OK</span></span> 
  
> <span data-ttu-id="729ae-119">Состояние блокировки сообщение успешно установлены.</span><span class="sxs-lookup"><span data-stu-id="729ae-119">The lock state of the message was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="729ae-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="729ae-120">Remarks</span></span>

<span data-ttu-id="729ae-121">Метод **IMsgStore::SetLockState** блокирует или разблокирует сообщение.</span><span class="sxs-lookup"><span data-stu-id="729ae-121">The **IMsgStore::SetLockState** method locks or unlocks a message.</span></span> <span data-ttu-id="729ae-122">**SetLockState** может быть вызван только диспетчер очереди MAPI во время отправляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="729ae-122">**SetLockState** can be called only by the MAPI spooler while it is sending the message.</span></span> 
  
<span data-ttu-id="729ae-123">Как правило, когда диспетчер очереди MAPI вызывает **SetLockState** заблокировать сообщения, блокирует только наиболее старых сообщений (то есть, следующее сообщение в очереди для очереди MAPI для отправки).</span><span class="sxs-lookup"><span data-stu-id="729ae-123">Usually, when the MAPI spooler calls **SetLockState** to lock a message, it locks only the oldest message (that is, the next message queued for the MAPI spooler to send).</span></span> <span data-ttu-id="729ae-124">Если наиболее старых сообщений в очередь ожидает поставщика транспорта временно недоступен и следующее сообщение в очереди используется другой поставщик, диспетчер очереди MAPI могут начать обработку сообщений более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="729ae-124">If the oldest message in the queue is waiting for a temporarily unavailable transport provider, and the next message in the queue uses a different transport provider, the MAPI spooler can begin processing the later message.</span></span> <span data-ttu-id="729ae-125">Обработка начинается с блокировкой этого сообщения с помощью **SetLockState**.</span><span class="sxs-lookup"><span data-stu-id="729ae-125">It begins processing by locking that message by using **SetLockState**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="729ae-126">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="729ae-126">Notes to implementers</span></span>

<span data-ttu-id="729ae-127">После диспетчер очереди MAPI вызова с параметром _ulLockState_ , задайте значение MSG_LOCKED **SetLockState** должен выполнить аварийное переключение вызовы метода [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) Отмена передачи сообщений.</span><span class="sxs-lookup"><span data-stu-id="729ae-127">After the MAPI spooler has called **SetLockState** with the  _ulLockState_ parameter set to MSG_LOCKED, calls to the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method to cancel the message's transmission must fail.</span></span> 
  
<span data-ttu-id="729ae-128">Вызов метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) сообщения в реализации **SetLockState** , чтобы сохранить все изменения, внесенные в сообщение перед **SetLockState** звонок был получен.</span><span class="sxs-lookup"><span data-stu-id="729ae-128">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method in your **SetLockState** implementation so that any changes that were made to the message before the **SetLockState** call was received are saved.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="729ae-129">См. также</span><span class="sxs-lookup"><span data-stu-id="729ae-129">See also</span></span>



[<span data-ttu-id="729ae-130">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="729ae-130">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="729ae-131">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="729ae-131">IMsgStore::FinishedMsg</span></span>](imsgstore-finishedmsg.md)
  
[<span data-ttu-id="729ae-132">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="729ae-132">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

