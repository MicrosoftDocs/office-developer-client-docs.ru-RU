---
title: IMsgStoreStoreLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.StoreLogoff
api_type:
- COM
ms.assetid: 3773c98e-531e-4bdc-a39a-2c3bb7378cd3
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: be11c536804682d1baec8188b6d7487c71d411e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424338"
---
# <a name="imsgstorestorelogoff"></a><span data-ttu-id="6d94e-103">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="6d94e-103">IMsgStore::StoreLogoff</span></span>

  
  
<span data-ttu-id="6d94e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d94e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d94e-105">Включает упорядоченный вход в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="6d94e-105">Enables the orderly logoff of the message store.</span></span>
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="6d94e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d94e-106">Parameters</span></span>

 <span data-ttu-id="6d94e-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="6d94e-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="6d94e-108">[in, out] Битовая битовая почта флагов, которая управляет выйдите из магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="6d94e-108">[in, out] A bitmask of flags that controls logoff from the message store.</span></span> <span data-ttu-id="6d94e-109">При вводе все флаги, установленные для этого параметра, являются взаимоисключающими; Вызываемая должна указывать только один флаг для каждого вызова.</span><span class="sxs-lookup"><span data-stu-id="6d94e-109">On input, all flags set for this parameter are mutually exclusive; a caller must specify only one flag per call.</span></span> <span data-ttu-id="6d94e-110">При вводе допустимы следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="6d94e-110">The following flags are valid on input:</span></span>
    
<span data-ttu-id="6d94e-111">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="6d94e-111">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="6d94e-112">Все действия поставщика транспорта для этого хранения сообщений следует остановить перед тем, как выйти из системы.</span><span class="sxs-lookup"><span data-stu-id="6d94e-112">Any transport provider activity for this message store should be stopped before logoff.</span></span> <span data-ttu-id="6d94e-113">Управление возвращается вызываемой после того, как действие остановлено.</span><span class="sxs-lookup"><span data-stu-id="6d94e-113">Control is returned to the caller after activity is stopped.</span></span> <span data-ttu-id="6d94e-114">Если какие-либо действия поставщика транспорта происходят, то выйдите из системы и не будет никаких изменений в поведении пула MAPI или поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="6d94e-114">If any transport provider activity is taking place, the logoff does not occur and no change in the behavior of the MAPI spooler or transport providers occurs.</span></span> <span data-ttu-id="6d94e-115">Если действие поставщика транспорта не работает, то пулер MAPI освобождает хранилище.</span><span class="sxs-lookup"><span data-stu-id="6d94e-115">If transport provider activity is idle, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="6d94e-116">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="6d94e-116">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="6d94e-117">Хранилище сообщений не должно ждать сообщений от поставщиков транспорта перед закрытием.</span><span class="sxs-lookup"><span data-stu-id="6d94e-117">The message store should not wait for messages from transport providers before closing.</span></span> <span data-ttu-id="6d94e-118">Отправляются исходящие сообщения, которые готовы к отправлению.</span><span class="sxs-lookup"><span data-stu-id="6d94e-118">Outbound messages that are ready to be sent are sent.</span></span> <span data-ttu-id="6d94e-119">Если в этом хранилище есть почта по умолчанию, все сообщения, которые находятся в процессе, будут получены, а дальнейший прием будет отключен.</span><span class="sxs-lookup"><span data-stu-id="6d94e-119">If this store contains the default Inbox, any in-process messages are received, and then further reception is disabled.</span></span> <span data-ttu-id="6d94e-120">После завершения всех действий диспетчер MAPI освобождает хранилище, а управление немедленно возвращается вызываемой.</span><span class="sxs-lookup"><span data-stu-id="6d94e-120">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the caller.</span></span> 
    
<span data-ttu-id="6d94e-121">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="6d94e-121">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="6d94e-122">Хранилище сообщений не должно ждать сведений от поставщиков транспорта перед закрытием.</span><span class="sxs-lookup"><span data-stu-id="6d94e-122">The message store should not wait for information from transport providers before closing.</span></span> <span data-ttu-id="6d94e-123">Обрабатываемая в настоящее время почта завершена, но новые сообщения не обрабатываются.</span><span class="sxs-lookup"><span data-stu-id="6d94e-123">Messages that are currently being processed are completed, but no new messages are processed.</span></span> <span data-ttu-id="6d94e-124">После завершения всех действий пулер MAPI освобождает хранилище, а управление немедленно возвращается поставщику магазина.</span><span class="sxs-lookup"><span data-stu-id="6d94e-124">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the store provider.</span></span> 
    
<span data-ttu-id="6d94e-125">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="6d94e-125">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="6d94e-126">Выйдите из системы так же, как если бы установлен флаг LOGOFF_NO_WAIT, но для соответствующих поставщиков транспорта следует использовать метод [IXPLogon::FlushQueues](ixplogon-flushqueues.md) или [IMAPIStatus::FlushQueues.](imapistatus-flushqueues.md)</span><span class="sxs-lookup"><span data-stu-id="6d94e-126">The logoff should work the same as if the LOGOFF_NO_WAIT flag is set, but either the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) or [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method for the appropriate transport providers should be called.</span></span> <span data-ttu-id="6d94e-127">Флаг LOGOFF_PURGE возвращает управление вызываемой по завершении.</span><span class="sxs-lookup"><span data-stu-id="6d94e-127">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="6d94e-128">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="6d94e-128">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="6d94e-129">Если происходит какой-либо из действий поставщика транспорта, не следует делать это.</span><span class="sxs-lookup"><span data-stu-id="6d94e-129">If any transport provider activity is taking place, the logoff should not occur.</span></span>
    
    The following flags are valid on output:
    
<span data-ttu-id="6d94e-130">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="6d94e-130">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="6d94e-131">В настоящее время входящие сообщения поступать.</span><span class="sxs-lookup"><span data-stu-id="6d94e-131">Inbound messages are currently arriving.</span></span>
    
<span data-ttu-id="6d94e-132">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="6d94e-132">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="6d94e-133">Исходящие сообщения находятся в процессе их обработки.</span><span class="sxs-lookup"><span data-stu-id="6d94e-133">Outbound messages are in the process of being sent.</span></span>
    
<span data-ttu-id="6d94e-134">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="6d94e-134">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="6d94e-135">Исходящие сообщения находятся в состоянии ожидания (то есть находятся в почтовом ящике).</span><span class="sxs-lookup"><span data-stu-id="6d94e-135">Outbound messages are pending (that is, they are in the Outbox).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6d94e-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d94e-136">Return value</span></span>

<span data-ttu-id="6d94e-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="6d94e-137">S_OK</span></span> 
  
> <span data-ttu-id="6d94e-138">Вход выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="6d94e-138">The logoff completed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6d94e-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="6d94e-139">Remarks</span></span>

<span data-ttu-id="6d94e-140">Метод **IMsgStore::StoreLogoff** управляет взаимодействием хранилищ сообщений и поставщиков транспорта во время процесса выйдите из системы.</span><span class="sxs-lookup"><span data-stu-id="6d94e-140">The **IMsgStore::StoreLogoff** method exerts control over the interaction of the message store and transport providers during the logoff process.</span></span> <span data-ttu-id="6d94e-141">Вызов **StoreLogoff** действителен только для хранилищ сообщений, которые используются только вызываемой.</span><span class="sxs-lookup"><span data-stu-id="6d94e-141">Calling **StoreLogoff** is valid only for message stores that are being used only by the caller.</span></span> <span data-ttu-id="6d94e-142">Например, если два клиента используют одно хранилище сообщений и один из них вызывает **StoreLogoff,** хранилище сообщений немедленно отпущено и управление возвращается вызываемому клиенту.</span><span class="sxs-lookup"><span data-stu-id="6d94e-142">For example, when two clients are using the same message store and one of them calls **StoreLogoff**, the message store is immediately released and control is returned to the calling client.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6d94e-143">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="6d94e-143">Notes to implementers</span></span>

<span data-ttu-id="6d94e-144">Сохраните флаги, которые передаются в **StoreLogoff,** и передайте их при вызове метода [IMAPISupport::StoreLogoffTransports.](imapisupport-storelogofftransports.md)</span><span class="sxs-lookup"><span data-stu-id="6d94e-144">Save the flags that are passed to **StoreLogoff** and pass them when you call the [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) method.</span></span> <span data-ttu-id="6d94e-145">Не **вызывайте StoreLogoffTransports,** пока количество ссылок в хранилище сообщений не опускается до нуля.</span><span class="sxs-lookup"><span data-stu-id="6d94e-145">Do not call **StoreLogoffTransports** until the message store's reference count drops to zero.</span></span> <span data-ttu-id="6d94e-146">Несколько вызовов **StoreLogoffTransports** просто переописают сохраненные флаги.</span><span class="sxs-lookup"><span data-stu-id="6d94e-146">Multiple calls to **StoreLogoffTransports** simply overwrite the saved flags.</span></span> 
  
<span data-ttu-id="6d94e-147">Если в **StoreLogoff** не было выполнено ни один вызов, прежде чем количество ссылок в хранилище сообщений достигнет нуля, установите флаг LOGOFF_ABORT в _параметре ulFlags,_ передаваемом в **StoreLogoffTransports.**</span><span class="sxs-lookup"><span data-stu-id="6d94e-147">If no call has been made to **StoreLogoff** before the message store's reference count reaches zero, set the LOGOFF_ABORT flag in the  _ulFlags_ parameter that you pass to **StoreLogoffTransports**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6d94e-148">См. также</span><span class="sxs-lookup"><span data-stu-id="6d94e-148">See also</span></span>



[<span data-ttu-id="6d94e-149">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="6d94e-149">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="6d94e-150">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="6d94e-150">IMAPISupport::StoreLogoffTransports</span></span>](imapisupport-storelogofftransports.md)
  
[<span data-ttu-id="6d94e-151">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="6d94e-151">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="6d94e-152">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6d94e-152">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

