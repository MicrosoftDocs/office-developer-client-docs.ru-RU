---
title: IMsgStoreLogoff
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
# <a name="imsgstorestorelogoff"></a><span data-ttu-id="f2b65-103">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="f2b65-103">IMsgStore::StoreLogoff</span></span>

  
  
<span data-ttu-id="f2b65-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2b65-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2b65-105">Включает упорядоченный журнал магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="f2b65-105">Enables the orderly logoff of the message store.</span></span>
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f2b65-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="f2b65-106">Parameters</span></span>

 <span data-ttu-id="f2b65-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="f2b65-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="f2b65-108">[in, out] Битмашка флагов, которые контролируют журнал из магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="f2b65-108">[in, out] A bitmask of flags that controls logoff from the message store.</span></span> <span data-ttu-id="f2b65-109">На входе все флаги, заданные для этого параметра, являются взаимоисключающими; вызываемая должна указывать только один флаг на один вызов.</span><span class="sxs-lookup"><span data-stu-id="f2b65-109">On input, all flags set for this parameter are mutually exclusive; a caller must specify only one flag per call.</span></span> <span data-ttu-id="f2b65-110">При входе допустимы следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="f2b65-110">The following flags are valid on input:</span></span>
    
<span data-ttu-id="f2b65-111">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="f2b65-111">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="f2b65-112">Все действия поставщика транспорта для этого магазина сообщений должны быть остановлены перед входом в систему.</span><span class="sxs-lookup"><span data-stu-id="f2b65-112">Any transport provider activity for this message store should be stopped before logoff.</span></span> <span data-ttu-id="f2b65-113">Управление возвращается вызываемой после того, как действие остановлено.</span><span class="sxs-lookup"><span data-stu-id="f2b65-113">Control is returned to the caller after activity is stopped.</span></span> <span data-ttu-id="f2b65-114">Если какие-либо действия поставщика транспорта происходят, журнал не происходит, и не происходит никаких изменений в поведении пулера MAPI или поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="f2b65-114">If any transport provider activity is taking place, the logoff does not occur and no change in the behavior of the MAPI spooler or transport providers occurs.</span></span> <span data-ttu-id="f2b65-115">Если деятельность поставщика транспорта простаивает, пульпер MAPI освобождает магазин.</span><span class="sxs-lookup"><span data-stu-id="f2b65-115">If transport provider activity is idle, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="f2b65-116">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="f2b65-116">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="f2b65-117">Хранилище сообщений не должно ждать сообщений от поставщиков транспорта перед закрытием.</span><span class="sxs-lookup"><span data-stu-id="f2b65-117">The message store should not wait for messages from transport providers before closing.</span></span> <span data-ttu-id="f2b65-118">Исходящие сообщения, готовые к отправлению, отправляются.</span><span class="sxs-lookup"><span data-stu-id="f2b65-118">Outbound messages that are ready to be sent are sent.</span></span> <span data-ttu-id="f2b65-119">Если этот магазин содержит почтовый ящик по умолчанию, все в процессе сообщения будут получены, а затем дополнительный прием отключен.</span><span class="sxs-lookup"><span data-stu-id="f2b65-119">If this store contains the default Inbox, any in-process messages are received, and then further reception is disabled.</span></span> <span data-ttu-id="f2b65-120">Когда все действия завершены, пульпер MAPI освобождает магазин, и управление немедленно возвращается вызываемой.</span><span class="sxs-lookup"><span data-stu-id="f2b65-120">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the caller.</span></span> 
    
<span data-ttu-id="f2b65-121">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="f2b65-121">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="f2b65-122">Хранилище сообщений не должно ждать информации от поставщиков транспорта перед закрытием.</span><span class="sxs-lookup"><span data-stu-id="f2b65-122">The message store should not wait for information from transport providers before closing.</span></span> <span data-ttu-id="f2b65-123">Сообщения, которые в настоящее время обрабатываются, завершались, но новые сообщения не обрабатываются.</span><span class="sxs-lookup"><span data-stu-id="f2b65-123">Messages that are currently being processed are completed, but no new messages are processed.</span></span> <span data-ttu-id="f2b65-124">Когда все действия завершены, пульпер MAPI освобождает магазин, и управление немедленно возвращается поставщику магазина.</span><span class="sxs-lookup"><span data-stu-id="f2b65-124">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the store provider.</span></span> 
    
<span data-ttu-id="f2b65-125">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="f2b65-125">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="f2b65-126">Вход должен работать так же, как если бы флаг LOGOFF_NO_WAIT установлен, но для соответствующих поставщиков транспорта должен быть вызван метод [IXPLogon::FlushQueues](ixplogon-flushqueues.md) или [IMAPIStatus::FlushQueues.](imapistatus-flushqueues.md)</span><span class="sxs-lookup"><span data-stu-id="f2b65-126">The logoff should work the same as if the LOGOFF_NO_WAIT flag is set, but either the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) or [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method for the appropriate transport providers should be called.</span></span> <span data-ttu-id="f2b65-127">Флаг LOGOFF_PURGE возвращает управление вызываемой после завершения.</span><span class="sxs-lookup"><span data-stu-id="f2b65-127">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="f2b65-128">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="f2b65-128">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="f2b65-129">Если какие-либо действия поставщика транспорта происходят, журнал не должен происходить.</span><span class="sxs-lookup"><span data-stu-id="f2b65-129">If any transport provider activity is taking place, the logoff should not occur.</span></span>
    
    The following flags are valid on output:
    
<span data-ttu-id="f2b65-130">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="f2b65-130">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="f2b65-131">В настоящее время прибывают входящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="f2b65-131">Inbound messages are currently arriving.</span></span>
    
<span data-ttu-id="f2b65-132">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="f2b65-132">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="f2b65-133">Исходящие сообщения находятся в процессе отосла.</span><span class="sxs-lookup"><span data-stu-id="f2b65-133">Outbound messages are in the process of being sent.</span></span>
    
<span data-ttu-id="f2b65-134">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="f2b65-134">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="f2b65-135">Исходящие сообщения находятся в ожидании (то есть они находятся в исходящие сообщения).</span><span class="sxs-lookup"><span data-stu-id="f2b65-135">Outbound messages are pending (that is, they are in the Outbox).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f2b65-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2b65-136">Return value</span></span>

<span data-ttu-id="f2b65-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="f2b65-137">S_OK</span></span> 
  
> <span data-ttu-id="f2b65-138">Журнал успешно завершен.</span><span class="sxs-lookup"><span data-stu-id="f2b65-138">The logoff completed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f2b65-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="f2b65-139">Remarks</span></span>

<span data-ttu-id="f2b65-140">Метод **IMsgStore::StoreLogoff** контролирует взаимодействие магазина сообщений и поставщиков транспорта во время процесса входа.</span><span class="sxs-lookup"><span data-stu-id="f2b65-140">The **IMsgStore::StoreLogoff** method exerts control over the interaction of the message store and transport providers during the logoff process.</span></span> <span data-ttu-id="f2b65-141">Вызов **StoreLogoff** действителен только для магазинов сообщений, которые используются только вызываемой.</span><span class="sxs-lookup"><span data-stu-id="f2b65-141">Calling **StoreLogoff** is valid only for message stores that are being used only by the caller.</span></span> <span data-ttu-id="f2b65-142">Например, когда два клиента используют один и тот же хранилище сообщений и один из них вызывает **StoreLogoff,** магазин сообщений немедленно освобожден и управление возвращается вызываемому клиенту.</span><span class="sxs-lookup"><span data-stu-id="f2b65-142">For example, when two clients are using the same message store and one of them calls **StoreLogoff**, the message store is immediately released and control is returned to the calling client.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f2b65-143">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="f2b65-143">Notes to implementers</span></span>

<span data-ttu-id="f2b65-144">Сохраните флаги, которые передаются **в StoreLogoff,** и передайте их при вызове метода [IMAPISupport::StoreLogoffTransports.](imapisupport-storelogofftransports.md)</span><span class="sxs-lookup"><span data-stu-id="f2b65-144">Save the flags that are passed to **StoreLogoff** and pass them when you call the [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) method.</span></span> <span data-ttu-id="f2b65-145">Не **вызывайте StoreLogoffTransports** до тех пор, пока количество ссылок магазина сообщений не опустится до нуля.</span><span class="sxs-lookup"><span data-stu-id="f2b65-145">Do not call **StoreLogoffTransports** until the message store's reference count drops to zero.</span></span> <span data-ttu-id="f2b65-146">Несколько вызовов **в StoreLogoffTransports просто** переопишут сохраненные флаги.</span><span class="sxs-lookup"><span data-stu-id="f2b65-146">Multiple calls to **StoreLogoffTransports** simply overwrite the saved flags.</span></span> 
  
<span data-ttu-id="f2b65-147">Если вызов в **StoreLogoff** не был выполнен до достижения нулевого отсчета в хранилище сообщений, установите флаг LOGOFF_ABORT в параметре _ulFlags,_ который передается в **StoreLogoffTransports.**</span><span class="sxs-lookup"><span data-stu-id="f2b65-147">If no call has been made to **StoreLogoff** before the message store's reference count reaches zero, set the LOGOFF_ABORT flag in the  _ulFlags_ parameter that you pass to **StoreLogoffTransports**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f2b65-148">См. также</span><span class="sxs-lookup"><span data-stu-id="f2b65-148">See also</span></span>



[<span data-ttu-id="f2b65-149">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="f2b65-149">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="f2b65-150">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="f2b65-150">IMAPISupport::StoreLogoffTransports</span></span>](imapisupport-storelogofftransports.md)
  
[<span data-ttu-id="f2b65-151">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="f2b65-151">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="f2b65-152">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f2b65-152">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

