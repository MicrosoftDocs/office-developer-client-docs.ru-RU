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
ms.openlocfilehash: a55fc361120472473bcba70152c153fb7824fb9e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566553"
---
# <a name="imsgstorestorelogoff"></a><span data-ttu-id="8a405-103">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="8a405-103">IMsgStore::StoreLogoff</span></span>

  
  
<span data-ttu-id="8a405-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a405-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a405-105">Включение упорядоченного выхода хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="8a405-105">Enables the orderly logoff of the message store.</span></span>
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8a405-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a405-106">Parameters</span></span>

 <span data-ttu-id="8a405-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="8a405-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="8a405-108">[in, out] Битовая маска флаги, который управляет выхода из хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="8a405-108">[in, out] A bitmask of flags that controls logoff from the message store.</span></span> <span data-ttu-id="8a405-109">Для ввода данных задайте для этого параметра все флаги являются взаимоисключающими; вызывающий объект необходимо указать только один флаг на вызов.</span><span class="sxs-lookup"><span data-stu-id="8a405-109">On input, all flags set for this parameter are mutually exclusive; a caller must specify only one flag per call.</span></span> <span data-ttu-id="8a405-110">Следующие флаги являются допустимыми на входные данные:</span><span class="sxs-lookup"><span data-stu-id="8a405-110">The following flags are valid on input:</span></span>
    
<span data-ttu-id="8a405-111">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="8a405-111">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="8a405-112">Какие-либо действия поставщика транспорта для хранилища должна быть прекращена до выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="8a405-112">Any transport provider activity for this message store should be stopped before logoff.</span></span> <span data-ttu-id="8a405-113">Управление возвращается вызывающему после остановки активности.</span><span class="sxs-lookup"><span data-stu-id="8a405-113">Control is returned to the caller after activity is stopped.</span></span> <span data-ttu-id="8a405-114">Если какие-либо действия поставщика транспорта с удалением, выхода из системы не происходит и не изменяется поведения очереди или транспорта поставщики MAPI.</span><span class="sxs-lookup"><span data-stu-id="8a405-114">If any transport provider activity is taking place, the logoff does not occur and no change in the behavior of the MAPI spooler or transport providers occurs.</span></span> <span data-ttu-id="8a405-115">Если действие поставщика транспорта простоя, диспетчер очереди MAPI освобождает хранилище.</span><span class="sxs-lookup"><span data-stu-id="8a405-115">If transport provider activity is idle, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="8a405-116">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="8a405-116">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="8a405-117">Хранилище сообщений не должна ожидать сообщения от поставщиками транспорта перед закрытием.</span><span class="sxs-lookup"><span data-stu-id="8a405-117">The message store should not wait for messages from transport providers before closing.</span></span> <span data-ttu-id="8a405-118">Отправки исходящих сообщений, которые являются Готово к отправке.</span><span class="sxs-lookup"><span data-stu-id="8a405-118">Outbound messages that are ready to be sent are sent.</span></span> <span data-ttu-id="8a405-119">Если это хранилище содержит папки "Входящие" по умолчанию, полученного сообщения в процесс и затем отключено дальнейший приема.</span><span class="sxs-lookup"><span data-stu-id="8a405-119">If this store contains the default Inbox, any in-process messages are received, and then further reception is disabled.</span></span> <span data-ttu-id="8a405-120">После завершения всех действий диспетчера очереди MAPI освобождает хранилище и управление немедленно возвращается вызывающему.</span><span class="sxs-lookup"><span data-stu-id="8a405-120">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the caller.</span></span> 
    
<span data-ttu-id="8a405-121">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="8a405-121">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="8a405-122">Хранилище сообщений не должна ожидать сведений из поставщиков транспорта перед закрытием.</span><span class="sxs-lookup"><span data-stu-id="8a405-122">The message store should not wait for information from transport providers before closing.</span></span> <span data-ttu-id="8a405-123">Сообщения, которые обрабатываются в настоящее время завершения, но не новые сообщения обрабатываются.</span><span class="sxs-lookup"><span data-stu-id="8a405-123">Messages that are currently being processed are completed, but no new messages are processed.</span></span> <span data-ttu-id="8a405-124">После завершения всех действий диспетчера очереди MAPI освобождает хранилище и управление немедленно возвращается поставщика хранилища.</span><span class="sxs-lookup"><span data-stu-id="8a405-124">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the store provider.</span></span> 
    
<span data-ttu-id="8a405-125">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="8a405-125">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="8a405-126">Выход из системы должны работать же, как если бы значение флага LOGOFF_NO_WAIT, но необходимо вызвать метод либо [IXPLogon::FlushQueues](ixplogon-flushqueues.md) , либо [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) для поставщиков соответствующий транспортный протокол.</span><span class="sxs-lookup"><span data-stu-id="8a405-126">The logoff should work the same as if the LOGOFF_NO_WAIT flag is set, but either the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) or [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method for the appropriate transport providers should be called.</span></span> <span data-ttu-id="8a405-127">После завершения флаг LOGOFF_PURGE возвращает управление вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="8a405-127">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="8a405-128">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="8a405-128">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="8a405-129">Если какие-либо действия поставщика транспорта с удалением, выход из системы не должно происходить.</span><span class="sxs-lookup"><span data-stu-id="8a405-129">If any transport provider activity is taking place, the logoff should not occur.</span></span>
    
    The following flags are valid on output:
    
<span data-ttu-id="8a405-130">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="8a405-130">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="8a405-131">Входящие сообщения поступают в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="8a405-131">Inbound messages are currently arriving.</span></span>
    
<span data-ttu-id="8a405-132">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="8a405-132">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="8a405-133">Исходящие сообщения, в процессе отправки.</span><span class="sxs-lookup"><span data-stu-id="8a405-133">Outbound messages are in the process of being sent.</span></span>
    
<span data-ttu-id="8a405-134">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="8a405-134">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="8a405-135">Исходящие сообщения, ожидающие (то есть, они находятся в папке Исходящие).</span><span class="sxs-lookup"><span data-stu-id="8a405-135">Outbound messages are pending (that is, they are in the Outbox).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8a405-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8a405-136">Return value</span></span>

<span data-ttu-id="8a405-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="8a405-137">S_OK</span></span> 
  
> <span data-ttu-id="8a405-138">Выход из системы, успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="8a405-138">The logoff completed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8a405-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="8a405-139">Remarks</span></span>

<span data-ttu-id="8a405-140">Метод **IMsgStore::StoreLogoff** оказывает управления через взаимодействие сообщение хранения и поставщиками транспорта во время выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="8a405-140">The **IMsgStore::StoreLogoff** method exerts control over the interaction of the message store and transport providers during the logoff process.</span></span> <span data-ttu-id="8a405-141">Вызов **StoreLogoff** допустимо только для хранилищ сообщений, которые используются только вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="8a405-141">Calling **StoreLogoff** is valid only for message stores that are being used only by the caller.</span></span> <span data-ttu-id="8a405-142">Например при два клиента с помощью одного хранилища сообщений и один из них вызывает **StoreLogoff**, сразу же выпущен хранилища сообщений и управление возвращается вызывающему клиенту.</span><span class="sxs-lookup"><span data-stu-id="8a405-142">For example, when two clients are using the same message store and one of them calls **StoreLogoff**, the message store is immediately released and control is returned to the calling client.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8a405-143">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="8a405-143">Notes to implementers</span></span>

<span data-ttu-id="8a405-144">Сохраните флаги, которые передаются в **StoreLogoff** и передавайте их при вызове метода [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) .</span><span class="sxs-lookup"><span data-stu-id="8a405-144">Save the flags that are passed to **StoreLogoff** and pass them when you call the [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) method.</span></span> <span data-ttu-id="8a405-145">Не вызывайте **StoreLogoffTransports** , пока число ссылок хранилища сообщений не станет нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="8a405-145">Do not call **StoreLogoffTransports** until the message store's reference count drops to zero.</span></span> <span data-ttu-id="8a405-146">Несколько вызовов **StoreLogoffTransports** просто перезаписать сохраненного флаги.</span><span class="sxs-lookup"><span data-stu-id="8a405-146">Multiple calls to **StoreLogoffTransports** simply overwrite the saved flags.</span></span> 
  
<span data-ttu-id="8a405-147">Если не вызов для **StoreLogoff** перед сообщением магазина число ссылок достигает нуля, задавать флаг LOGOFF_ABORT в параметре _ulFlags_ , передаваемый **StoreLogoffTransports**.</span><span class="sxs-lookup"><span data-stu-id="8a405-147">If no call has been made to **StoreLogoff** before the message store's reference count reaches zero, set the LOGOFF_ABORT flag in the  _ulFlags_ parameter that you pass to **StoreLogoffTransports**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8a405-148">См. также</span><span class="sxs-lookup"><span data-stu-id="8a405-148">See also</span></span>



[<span data-ttu-id="8a405-149">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="8a405-149">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="8a405-150">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="8a405-150">IMAPISupport::StoreLogoffTransports</span></span>](imapisupport-storelogofftransports.md)
  
[<span data-ttu-id="8a405-151">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="8a405-151">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="8a405-152">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8a405-152">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

