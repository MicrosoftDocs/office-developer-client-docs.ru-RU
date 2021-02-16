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
ms.openlocfilehash: 9eeede2a430f5186daf429dd6ed59f312ae334be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423631"
---
# <a name="imsgstoresetlockstate"></a><span data-ttu-id="f1da0-103">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="f1da0-103">IMsgStore::SetLockState</span></span>

  
  
<span data-ttu-id="f1da0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1da0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1da0-105">Блокирует или разблокирует сообщение.</span><span class="sxs-lookup"><span data-stu-id="f1da0-105">Locks or unlocks a message.</span></span> <span data-ttu-id="f1da0-106">���� ����� ���������� ������ ����������� ������� MAPI.</span><span class="sxs-lookup"><span data-stu-id="f1da0-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT SetLockState(
  LPMESSAGE lpMessage,
  ULONG ulLockState  
);
```

## <a name="parameters"></a><span data-ttu-id="f1da0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1da0-107">Parameters</span></span>

 <span data-ttu-id="f1da0-108">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="f1da0-108">_lpMessage_</span></span>
  
> <span data-ttu-id="f1da0-109">[in] Указатель на сообщение для блокировки или разблокировки.</span><span class="sxs-lookup"><span data-stu-id="f1da0-109">[in] A pointer to the message to lock or unlock.</span></span>
    
 <span data-ttu-id="f1da0-110">_ulLockState_</span><span class="sxs-lookup"><span data-stu-id="f1da0-110">_ulLockState_</span></span>
  
> <span data-ttu-id="f1da0-111">[in] Значение, которое указывает, следует ли заблокировать или разблокировать сообщение.</span><span class="sxs-lookup"><span data-stu-id="f1da0-111">[in] A value that indicates whether the message should be locked or unlocked.</span></span> <span data-ttu-id="f1da0-112">Допустимо одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="f1da0-112">One of the following values is valid:</span></span>
    
<span data-ttu-id="f1da0-113">MSG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="f1da0-113">MSG_LOCKED</span></span> 
  
> <span data-ttu-id="f1da0-114">Сообщение должно быть заблокировано.</span><span class="sxs-lookup"><span data-stu-id="f1da0-114">The message should be locked.</span></span> 
    
<span data-ttu-id="f1da0-115">MSG_UNLOCKED</span><span class="sxs-lookup"><span data-stu-id="f1da0-115">MSG_UNLOCKED</span></span> 
  
> <span data-ttu-id="f1da0-116">Сообщение должно быть разблокировано.</span><span class="sxs-lookup"><span data-stu-id="f1da0-116">The message should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f1da0-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f1da0-117">Return value</span></span>

<span data-ttu-id="f1da0-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="f1da0-118">S_OK</span></span> 
  
> <span data-ttu-id="f1da0-119">Состояние блокировки сообщения успешно установлено.</span><span class="sxs-lookup"><span data-stu-id="f1da0-119">The lock state of the message was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f1da0-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="f1da0-120">Remarks</span></span>

<span data-ttu-id="f1da0-121">Метод **IMsgStore::SetLockState** блокирует или разблокирует сообщение.</span><span class="sxs-lookup"><span data-stu-id="f1da0-121">The **IMsgStore::SetLockState** method locks or unlocks a message.</span></span> <span data-ttu-id="f1da0-122">**SetLockState** может быть вызван только пулером MAPI во время отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="f1da0-122">**SetLockState** can be called only by the MAPI spooler while it is sending the message.</span></span> 
  
<span data-ttu-id="f1da0-123">Обычно, когда пулер MAPI вызывает **SetLockState** для блокировки сообщения, он блокирует только самое старое сообщение (то есть следующее сообщение, поставленное в очередь для отправки пулом MAPI).</span><span class="sxs-lookup"><span data-stu-id="f1da0-123">Usually, when the MAPI spooler calls **SetLockState** to lock a message, it locks only the oldest message (that is, the next message queued for the MAPI spooler to send).</span></span> <span data-ttu-id="f1da0-124">Если самое старое сообщение в очереди ожидает временно недоступного поставщика транспорта, а следующее сообщение в очереди использует другого поставщика транспорта, то пулер MAPI может начать обработку следующего сообщения.</span><span class="sxs-lookup"><span data-stu-id="f1da0-124">If the oldest message in the queue is waiting for a temporarily unavailable transport provider, and the next message in the queue uses a different transport provider, the MAPI spooler can begin processing the later message.</span></span> <span data-ttu-id="f1da0-125">Обработка начинается с блокировки сообщения с помощью **SetLockState.**</span><span class="sxs-lookup"><span data-stu-id="f1da0-125">It begins processing by locking that message by using **SetLockState**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f1da0-126">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="f1da0-126">Notes to implementers</span></span>

<span data-ttu-id="f1da0-127">После того как пулер MAPI вызывает **SetLockState** с параметром  _ulLockState,_ установленным в MSG_LOCKED, вызов метода [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) для отмены передачи сообщения должен быть неудачным.</span><span class="sxs-lookup"><span data-stu-id="f1da0-127">After the MAPI spooler has called **SetLockState** with the  _ulLockState_ parameter set to MSG_LOCKED, calls to the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method to cancel the message's transmission must fail.</span></span> 
  
<span data-ttu-id="f1da0-128">Вызовите метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) сообщения в реализации **SetLockState,** чтобы сохранить все изменения, внесенные в сообщение до получения вызова **SetLockState.**</span><span class="sxs-lookup"><span data-stu-id="f1da0-128">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method in your **SetLockState** implementation so that any changes that were made to the message before the **SetLockState** call was received are saved.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f1da0-129">См. также</span><span class="sxs-lookup"><span data-stu-id="f1da0-129">See also</span></span>



[<span data-ttu-id="f1da0-130">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="f1da0-130">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="f1da0-131">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="f1da0-131">IMsgStore::FinishedMsg</span></span>](imsgstore-finishedmsg.md)
  
[<span data-ttu-id="f1da0-132">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f1da0-132">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

