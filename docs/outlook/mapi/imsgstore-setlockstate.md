---
title: Имсгсторесетлоккстате
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348750"
---
# <a name="imsgstoresetlockstate"></a><span data-ttu-id="76cbc-103">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="76cbc-103">IMsgStore::SetLockState</span></span>

  
  
<span data-ttu-id="76cbc-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76cbc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76cbc-105">Блокировка или разблокировка сообщения.</span><span class="sxs-lookup"><span data-stu-id="76cbc-105">Locks or unlocks a message.</span></span> <span data-ttu-id="76cbc-106">���� ����� ���������� ������ ����������� ������� MAPI.</span><span class="sxs-lookup"><span data-stu-id="76cbc-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT SetLockState(
  LPMESSAGE lpMessage,
  ULONG ulLockState  
);
```

## <a name="parameters"></a><span data-ttu-id="76cbc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="76cbc-107">Parameters</span></span>

 <span data-ttu-id="76cbc-108">_Лпмессаже_</span><span class="sxs-lookup"><span data-stu-id="76cbc-108">_lpMessage_</span></span>
  
> <span data-ttu-id="76cbc-109">возврата Указатель на сообщение, которое необходимо заблокировать или разблокировать.</span><span class="sxs-lookup"><span data-stu-id="76cbc-109">[in] A pointer to the message to lock or unlock.</span></span>
    
 <span data-ttu-id="76cbc-110">_Уллоккстате_</span><span class="sxs-lookup"><span data-stu-id="76cbc-110">_ulLockState_</span></span>
  
> <span data-ttu-id="76cbc-111">возврата Значение, указывающее, должно ли сообщение блокироваться или разблокировано.</span><span class="sxs-lookup"><span data-stu-id="76cbc-111">[in] A value that indicates whether the message should be locked or unlocked.</span></span> <span data-ttu-id="76cbc-112">Допустимо одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="76cbc-112">One of the following values is valid:</span></span>
    
<span data-ttu-id="76cbc-113">МСГ_ЛОККЕД</span><span class="sxs-lookup"><span data-stu-id="76cbc-113">MSG_LOCKED</span></span> 
  
> <span data-ttu-id="76cbc-114">Сообщение должно быть заблокировано.</span><span class="sxs-lookup"><span data-stu-id="76cbc-114">The message should be locked.</span></span> 
    
<span data-ttu-id="76cbc-115">МСГ_УНЛОККЕД</span><span class="sxs-lookup"><span data-stu-id="76cbc-115">MSG_UNLOCKED</span></span> 
  
> <span data-ttu-id="76cbc-116">Сообщение должно быть разблокировано.</span><span class="sxs-lookup"><span data-stu-id="76cbc-116">The message should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="76cbc-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="76cbc-117">Return value</span></span>

<span data-ttu-id="76cbc-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="76cbc-118">S_OK</span></span> 
  
> <span data-ttu-id="76cbc-119">Состояние блокировки сообщения успешно задано.</span><span class="sxs-lookup"><span data-stu-id="76cbc-119">The lock state of the message was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="76cbc-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="76cbc-120">Remarks</span></span>

<span data-ttu-id="76cbc-121">Метод **IMsgStore:: сетлоккстате** блокирует или разблокирует сообщение.</span><span class="sxs-lookup"><span data-stu-id="76cbc-121">The **IMsgStore::SetLockState** method locks or unlocks a message.</span></span> <span data-ttu-id="76cbc-122">**Сетлоккстате** может вызываться только диспетчером очереди MAPI при отправке сообщения.</span><span class="sxs-lookup"><span data-stu-id="76cbc-122">**SetLockState** can be called only by the MAPI spooler while it is sending the message.</span></span> 
  
<span data-ttu-id="76cbc-123">Как правило, когда диспетчер очереди MAPI вызывает **сетлоккстате** для блокировки сообщения, он блокирует только самое старое сообщение (то есть следующее сообщение помещено в очередь на отправку буфера обмена MAPI).</span><span class="sxs-lookup"><span data-stu-id="76cbc-123">Usually, when the MAPI spooler calls **SetLockState** to lock a message, it locks only the oldest message (that is, the next message queued for the MAPI spooler to send).</span></span> <span data-ttu-id="76cbc-124">Если самое старое сообщение в очереди ожидает временно доступного поставщика транспорта, а для следующего сообщения в очереди используется другой поставщик транспорта, диспетчер очереди MAPI может начать обработку следующего сообщения.</span><span class="sxs-lookup"><span data-stu-id="76cbc-124">If the oldest message in the queue is waiting for a temporarily unavailable transport provider, and the next message in the queue uses a different transport provider, the MAPI spooler can begin processing the later message.</span></span> <span data-ttu-id="76cbc-125">Он начинает обработку, блокируя это сообщение с помощью **сетлоккстате**.</span><span class="sxs-lookup"><span data-stu-id="76cbc-125">It begins processing by locking that message by using **SetLockState**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="76cbc-126">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="76cbc-126">Notes to implementers</span></span>

<span data-ttu-id="76cbc-127">После того как диспетчер очереди MAPI вызвал **сетлоккстате** с параметром _уллоккстате_ , для которого задано значение Мсг_локкед, вызовы метода [IMsgStore:: абортсубмит](imsgstore-abortsubmit.md) для отмены передачи сообщения должны завершиться с ошибками.</span><span class="sxs-lookup"><span data-stu-id="76cbc-127">After the MAPI spooler has called **SetLockState** with the  _ulLockState_ parameter set to MSG_LOCKED, calls to the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method to cancel the message's transmission must fail.</span></span> 
  
<span data-ttu-id="76cbc-128">ВыЗовите метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) в реализации **сетлоккстате** , чтобы все изменения, внесенные в сообщение перед получением вызова **сетлоккстате** , сохранялись.</span><span class="sxs-lookup"><span data-stu-id="76cbc-128">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method in your **SetLockState** implementation so that any changes that were made to the message before the **SetLockState** call was received are saved.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="76cbc-129">См. также</span><span class="sxs-lookup"><span data-stu-id="76cbc-129">See also</span></span>



[<span data-ttu-id="76cbc-130">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="76cbc-130">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="76cbc-131">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="76cbc-131">IMsgStore::FinishedMsg</span></span>](imsgstore-finishedmsg.md)
  
[<span data-ttu-id="76cbc-132">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="76cbc-132">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

