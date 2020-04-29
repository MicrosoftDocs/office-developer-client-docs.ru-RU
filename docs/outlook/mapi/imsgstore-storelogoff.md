---
title: имсгсторесторелогофф
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
# <a name="imsgstorestorelogoff"></a><span data-ttu-id="1733a-103">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="1733a-103">IMsgStore::StoreLogoff</span></span>

  
  
<span data-ttu-id="1733a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1733a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1733a-105">Позволяет выполнять упорядоченный выход из хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="1733a-105">Enables the orderly logoff of the message store.</span></span>
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1733a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1733a-106">Parameters</span></span>

 <span data-ttu-id="1733a-107">_лпулфлагс_</span><span class="sxs-lookup"><span data-stu-id="1733a-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="1733a-108">[вход, выход] Битовая маска флагов, которые управляют выходом из хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="1733a-108">[in, out] A bitmask of flags that controls logoff from the message store.</span></span> <span data-ttu-id="1733a-109">Во входных данных все флаги, установленные для этого параметра, являются взаимоисключающими; вызывающий абонент должен указать только один флаг для каждого вызова.</span><span class="sxs-lookup"><span data-stu-id="1733a-109">On input, all flags set for this parameter are mutually exclusive; a caller must specify only one flag per call.</span></span> <span data-ttu-id="1733a-110">Следующие флаги допустимы для входных данных:</span><span class="sxs-lookup"><span data-stu-id="1733a-110">The following flags are valid on input:</span></span>
    
<span data-ttu-id="1733a-111">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="1733a-111">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="1733a-112">Перед выходом из системы необходимо остановить все действия поставщика транспорта для этого хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="1733a-112">Any transport provider activity for this message store should be stopped before logoff.</span></span> <span data-ttu-id="1733a-113">Управление возвращается вызывающему абоненту после остановки действия.</span><span class="sxs-lookup"><span data-stu-id="1733a-113">Control is returned to the caller after activity is stopped.</span></span> <span data-ttu-id="1733a-114">Если выполняется какое-либо действие поставщика транспорта, выход не выполняется и не происходит никаких изменений в работе диспетчера очереди MAPI или поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="1733a-114">If any transport provider activity is taking place, the logoff does not occur and no change in the behavior of the MAPI spooler or transport providers occurs.</span></span> <span data-ttu-id="1733a-115">Если активность поставщика транспорта неактивна, то диспетчер очереди MAPI освобождает хранилище.</span><span class="sxs-lookup"><span data-stu-id="1733a-115">If transport provider activity is idle, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="1733a-116">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="1733a-116">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="1733a-117">Перед закрытием хранилище сообщений не должно ждать сообщений от поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="1733a-117">The message store should not wait for messages from transport providers before closing.</span></span> <span data-ttu-id="1733a-118">Отправляются исходящие сообщения, готовые к отправке.</span><span class="sxs-lookup"><span data-stu-id="1733a-118">Outbound messages that are ready to be sent are sent.</span></span> <span data-ttu-id="1733a-119">Если это хранилище содержит папку "Входящие" по умолчанию, все сообщения в процессе принимаются, а затем дальнейший прием отключен.</span><span class="sxs-lookup"><span data-stu-id="1733a-119">If this store contains the default Inbox, any in-process messages are received, and then further reception is disabled.</span></span> <span data-ttu-id="1733a-120">После завершения всех действий Диспетчер очереди MAPI освобождает хранилище, а управление немедленно возвращается вызывающему абоненту.</span><span class="sxs-lookup"><span data-stu-id="1733a-120">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the caller.</span></span> 
    
<span data-ttu-id="1733a-121">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="1733a-121">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="1733a-122">Хранилище сообщений не должно ждать получения информации от поставщиков транспорта перед закрытием.</span><span class="sxs-lookup"><span data-stu-id="1733a-122">The message store should not wait for information from transport providers before closing.</span></span> <span data-ttu-id="1733a-123">Сообщения, которые обрабатываются в данный момент, заполняются, но новые сообщения не обрабатываются.</span><span class="sxs-lookup"><span data-stu-id="1733a-123">Messages that are currently being processed are completed, but no new messages are processed.</span></span> <span data-ttu-id="1733a-124">После завершения всех действий Диспетчер очереди MAPI освобождает хранилище, а управление немедленно возвращается поставщику хранилища.</span><span class="sxs-lookup"><span data-stu-id="1733a-124">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the store provider.</span></span> 
    
<span data-ttu-id="1733a-125">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="1733a-125">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="1733a-126">Выход должен работать так же, как при установке флага LOGOFF_NO_WAIT, но метод [иксплогон:: FlushQueues](ixplogon-flushqueues.md) или [Имапистатус:: FlushQueues](imapistatus-flushqueues.md) должен вызываться для соответствующих поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="1733a-126">The logoff should work the same as if the LOGOFF_NO_WAIT flag is set, but either the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) or [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method for the appropriate transport providers should be called.</span></span> <span data-ttu-id="1733a-127">Флаг LOGOFF_PURGE возвращает управление вызывающей стороне после завершения.</span><span class="sxs-lookup"><span data-stu-id="1733a-127">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="1733a-128">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="1733a-128">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="1733a-129">Если выполняется какое-либо действие поставщика транспорта, выход из системы не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1733a-129">If any transport provider activity is taking place, the logoff should not occur.</span></span>
    
    The following flags are valid on output:
    
<span data-ttu-id="1733a-130">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="1733a-130">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="1733a-131">Входящие сообщения в настоящее время поступают.</span><span class="sxs-lookup"><span data-stu-id="1733a-131">Inbound messages are currently arriving.</span></span>
    
<span data-ttu-id="1733a-132">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="1733a-132">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="1733a-133">Исходящие сообщения находятся в процессе отправки.</span><span class="sxs-lookup"><span data-stu-id="1733a-133">Outbound messages are in the process of being sent.</span></span>
    
<span data-ttu-id="1733a-134">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="1733a-134">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="1733a-135">Исходящие сообщения находятся в папке "Исходящие" (то есть в папке "Исходящие").</span><span class="sxs-lookup"><span data-stu-id="1733a-135">Outbound messages are pending (that is, they are in the Outbox).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1733a-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1733a-136">Return value</span></span>

<span data-ttu-id="1733a-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="1733a-137">S_OK</span></span> 
  
> <span data-ttu-id="1733a-138">Выход из системы успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="1733a-138">The logoff completed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1733a-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="1733a-139">Remarks</span></span>

<span data-ttu-id="1733a-140">Метод **IMsgStore:: сторелогофф** оказывает Управление взаимодействием между хранилищем сообщений и поставщиками транспорта в процессе выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="1733a-140">The **IMsgStore::StoreLogoff** method exerts control over the interaction of the message store and transport providers during the logoff process.</span></span> <span data-ttu-id="1733a-141">Вызов **сторелогофф** является допустимым только для хранилищ сообщений, используемых вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="1733a-141">Calling **StoreLogoff** is valid only for message stores that are being used only by the caller.</span></span> <span data-ttu-id="1733a-142">Например, если два клиента используют одно и то же хранилище сообщений и один из них вызывает **сторелогофф**, то хранилище сообщений немедленно освободится и управление возвращается вызывающему клиенту.</span><span class="sxs-lookup"><span data-stu-id="1733a-142">For example, when two clients are using the same message store and one of them calls **StoreLogoff**, the message store is immediately released and control is returned to the calling client.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1733a-143">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="1733a-143">Notes to implementers</span></span>

<span data-ttu-id="1733a-144">Сохраните флаги, которые передаются в **сторелогофф** , и передайте их при вызове метода [Имаписуппорт:: сторелогоффтранспортс](imapisupport-storelogofftransports.md) .</span><span class="sxs-lookup"><span data-stu-id="1733a-144">Save the flags that are passed to **StoreLogoff** and pass them when you call the [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) method.</span></span> <span data-ttu-id="1733a-145">Не вызывайте **сторелогоффтранспортс** , пока счетчик ссылок хранилища сообщений не сбрасывается в ноль.</span><span class="sxs-lookup"><span data-stu-id="1733a-145">Do not call **StoreLogoffTransports** until the message store's reference count drops to zero.</span></span> <span data-ttu-id="1733a-146">Несколько вызовов **сторелогоффтранспортс** просто перезаписывают сохраненные флаги.</span><span class="sxs-lookup"><span data-stu-id="1733a-146">Multiple calls to **StoreLogoffTransports** simply overwrite the saved flags.</span></span> 
  
<span data-ttu-id="1733a-147">Если в **сторелогофф** не был выполнен вызов до тех пор, пока значение счетчика ссылок банка сообщений достигнет нуля, установите флаг LOGOFF_ABORT в параметре _ulFlags_ , передаваемый в **сторелогоффтранспортс**.</span><span class="sxs-lookup"><span data-stu-id="1733a-147">If no call has been made to **StoreLogoff** before the message store's reference count reaches zero, set the LOGOFF_ABORT flag in the  _ulFlags_ parameter that you pass to **StoreLogoffTransports**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1733a-148">См. также</span><span class="sxs-lookup"><span data-stu-id="1733a-148">See also</span></span>



[<span data-ttu-id="1733a-149">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="1733a-149">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="1733a-150">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="1733a-150">IMAPISupport::StoreLogoffTransports</span></span>](imapisupport-storelogofftransports.md)
  
[<span data-ttu-id="1733a-151">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="1733a-151">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="1733a-152">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1733a-152">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

