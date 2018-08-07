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
ms.openlocfilehash: a4e924489f2ec656f473f28407d528e9c2ddda5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809382"
---
# <a name="imsgstoresetlockstate"></a><span data-ttu-id="3d331-103">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="3d331-103">IMsgStore::SetLockState</span></span>

  
  
<span data-ttu-id="3d331-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3d331-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3d331-105">Блокирует или разблокирует сообщение.</span><span class="sxs-lookup"><span data-stu-id="3d331-105">Locks or unlocks a message.</span></span> <span data-ttu-id="3d331-106">���� ����� ���������� ������ ����������� ������� MAPI.</span><span class="sxs-lookup"><span data-stu-id="3d331-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT SetLockState(
  LPMESSAGE lpMessage,
  ULONG ulLockState  
);
```

## <a name="parameters"></a><span data-ttu-id="3d331-107">���������</span><span class="sxs-lookup"><span data-stu-id="3d331-107">Parameters</span></span>

 <span data-ttu-id="3d331-108">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="3d331-108">_lpMessage_</span></span>
  
> <span data-ttu-id="3d331-109">[in] Указатель на сообщение необходимо заблокировать или разблокировать.</span><span class="sxs-lookup"><span data-stu-id="3d331-109">[in] A pointer to the message to lock or unlock.</span></span>
    
 <span data-ttu-id="3d331-110">_ulLockState_</span><span class="sxs-lookup"><span data-stu-id="3d331-110">_ulLockState_</span></span>
  
> <span data-ttu-id="3d331-111">[in] Значение, указывающее, заблокирован или блокируется сообщения.</span><span class="sxs-lookup"><span data-stu-id="3d331-111">[in] A value that indicates whether the message should be locked or unlocked.</span></span> <span data-ttu-id="3d331-112">Допустим один из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="3d331-112">One of the following values is valid:</span></span>
    
<span data-ttu-id="3d331-113">MSG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="3d331-113">MSG_LOCKED</span></span> 
  
> <span data-ttu-id="3d331-114">Следует заблокировать сообщения.</span><span class="sxs-lookup"><span data-stu-id="3d331-114">The message should be locked.</span></span> 
    
<span data-ttu-id="3d331-115">MSG_UNLOCKED</span><span class="sxs-lookup"><span data-stu-id="3d331-115">MSG_UNLOCKED</span></span> 
  
> <span data-ttu-id="3d331-116">Сообщение необходимо разблокировать.</span><span class="sxs-lookup"><span data-stu-id="3d331-116">The message should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3d331-117">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="3d331-117">Return value</span></span>

<span data-ttu-id="3d331-118">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="3d331-118">S_OK</span></span> 
  
> <span data-ttu-id="3d331-119">Состояние блокировки сообщение успешно установлены.</span><span class="sxs-lookup"><span data-stu-id="3d331-119">The lock state of the message was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3d331-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="3d331-120">Remarks</span></span>

<span data-ttu-id="3d331-121">Метод **IMsgStore::SetLockState** блокирует или разблокирует сообщение.</span><span class="sxs-lookup"><span data-stu-id="3d331-121">The **IMsgStore::SetLockState** method locks or unlocks a message.</span></span> <span data-ttu-id="3d331-122">**SetLockState** может быть вызван только диспетчер очереди MAPI во время отправляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="3d331-122">**SetLockState** can be called only by the MAPI spooler while it is sending the message.</span></span> 
  
<span data-ttu-id="3d331-123">Как правило, когда диспетчер очереди MAPI вызывает **SetLockState** заблокировать сообщения, блокирует только наиболее старых сообщений (то есть, следующее сообщение в очереди для очереди MAPI для отправки).</span><span class="sxs-lookup"><span data-stu-id="3d331-123">Usually, when the MAPI spooler calls **SetLockState** to lock a message, it locks only the oldest message (that is, the next message queued for the MAPI spooler to send).</span></span> <span data-ttu-id="3d331-124">Если наиболее старых сообщений в очередь ожидает поставщика транспорта временно недоступен и следующее сообщение в очереди используется другой поставщик, диспетчер очереди MAPI могут начать обработку сообщений более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="3d331-124">If the oldest message in the queue is waiting for a temporarily unavailable transport provider, and the next message in the queue uses a different transport provider, the MAPI spooler can begin processing the later message.</span></span> <span data-ttu-id="3d331-125">Обработка начинается с блокировкой этого сообщения с помощью **SetLockState**.</span><span class="sxs-lookup"><span data-stu-id="3d331-125">It begins processing by locking that message by using **SetLockState**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3d331-126">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="3d331-126">Notes to implementers</span></span>

<span data-ttu-id="3d331-127">После диспетчер очереди MAPI вызова с параметром _ulLockState_ , задайте значение MSG_LOCKED **SetLockState** должен выполнить аварийное переключение вызовы метода [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) Отмена передачи сообщений.</span><span class="sxs-lookup"><span data-stu-id="3d331-127">After the MAPI spooler has called **SetLockState** with the  _ulLockState_ parameter set to MSG_LOCKED, calls to the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method to cancel the message's transmission must fail.</span></span> 
  
<span data-ttu-id="3d331-128">Вызов метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) сообщения в реализации **SetLockState** , чтобы сохранить все изменения, внесенные в сообщение перед **SetLockState** звонок был получен.</span><span class="sxs-lookup"><span data-stu-id="3d331-128">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method in your **SetLockState** implementation so that any changes that were made to the message before the **SetLockState** call was received are saved.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3d331-129">См. также</span><span class="sxs-lookup"><span data-stu-id="3d331-129">See also</span></span>



[<span data-ttu-id="3d331-130">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="3d331-130">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="3d331-131">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="3d331-131">IMsgStore::FinishedMsg</span></span>](imsgstore-finishedmsg.md)
  
[<span data-ttu-id="3d331-132">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3d331-132">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

