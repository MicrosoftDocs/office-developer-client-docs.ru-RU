---
title: IMAPISupportStoreLogoffTransports
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.StoreLogoffTransports
api_type:
- COM
ms.assetid: f21fba96-c5ca-4d41-9b93-c7955ab7327f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 30c91ec7a5a28b0c270da5223a2a245fb504d8c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421384"
---
# <a name="imapisupportstorelogofftransports"></a><span data-ttu-id="1b459-103">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="1b459-103">IMAPISupport::StoreLogoffTransports</span></span>

  
  
<span data-ttu-id="1b459-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b459-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b459-105">Запрашивает упорядоченный выпуск магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="1b459-105">Requests the orderly release of a message store.</span></span>
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1b459-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="1b459-106">Parameters</span></span>

 <span data-ttu-id="1b459-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="1b459-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="1b459-108">[in, out] Битмаска флагов, которые контролируют процесс входа в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="1b459-108">[in, out] A bitmask of flags that controls how message store logoff occurs.</span></span> <span data-ttu-id="1b459-109">На входе все флаги для этого параметра являются взаимоисключающими; на один вызов можно установить только один из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="1b459-109">On input, all flags for this parameter are mutually exclusive; only one of the following flags can be set per call:</span></span>
    
<span data-ttu-id="1b459-110">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="1b459-110">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="1b459-111">Все действия поставщика транспорта для этого магазина должны быть остановлены перед входом в систему.</span><span class="sxs-lookup"><span data-stu-id="1b459-111">Any transport provider activity for this store should be stopped before logoff.</span></span> <span data-ttu-id="1b459-112">Управление возвращается клиенту после того, как действие остановлено, а пульпер MAPI выключил магазин.</span><span class="sxs-lookup"><span data-stu-id="1b459-112">Control is returned to the client after the activity is stopped and the MAPI spooler has logged off the store.</span></span> <span data-ttu-id="1b459-113">Если какие-либо транспортные действия происходят, журнал не происходит, и не происходит никаких изменений в пулере MAPI или поведении поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="1b459-113">If any transport activity is taking place, the logoff does not occur and no change in the MAPI spooler or transport provider behavior occurs.</span></span> <span data-ttu-id="1b459-114">Если в настоящее время нет действий, пульпер MAPI освобождает магазин.</span><span class="sxs-lookup"><span data-stu-id="1b459-114">If there is currently no activity, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="1b459-115">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="1b459-115">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="1b459-116">Пульпер MAPI должен освободить хранилище и вернуть управление клиенту сразу после того, как будет отправлена вся готовая к отправлению почта.</span><span class="sxs-lookup"><span data-stu-id="1b459-116">The MAPI spooler should release the store and return control to the client immediately after all outbound mail that is ready to be sent is sent.</span></span> <span data-ttu-id="1b459-117">Если в хранилище сообщений имеется почтовый ящик по умолчанию, любое в процессе сообщения получается, а затем дополнительный прием отключен.</span><span class="sxs-lookup"><span data-stu-id="1b459-117">If the message store has the default Inbox, any in-process message is received, and then further reception is disabled.</span></span> 
    
<span data-ttu-id="1b459-118">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="1b459-118">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="1b459-119">Пульпер MAPI должен освободить магазин и вернуть управление клиенту сразу после завершения обработки всех ожидающих сообщений.</span><span class="sxs-lookup"><span data-stu-id="1b459-119">The MAPI spooler should release the store and return control to the client immediately after any pending messages are finished processing.</span></span> <span data-ttu-id="1b459-120">Новые сообщения не должны обрабатываться.</span><span class="sxs-lookup"><span data-stu-id="1b459-120">No new messages should be processed.</span></span> 
    
<span data-ttu-id="1b459-121">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="1b459-121">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="1b459-122">Работает так же, как LOGOFF_NO_WAIT флаг.</span><span class="sxs-lookup"><span data-stu-id="1b459-122">Works the same as the LOGOFF_NO_WAIT flag.</span></span> <span data-ttu-id="1b459-123">Флаг LOGOFF_PURGE возвращает управление вызываемой после завершения.</span><span class="sxs-lookup"><span data-stu-id="1b459-123">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="1b459-124">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="1b459-124">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="1b459-125">Журнал не должен происходить, если какие-либо действия поставщика транспорта происходят.</span><span class="sxs-lookup"><span data-stu-id="1b459-125">The logoff should not occur if any transport provider activity is taking place.</span></span> <span data-ttu-id="1b459-126">Тип действия, который происходит, возвращается в виде флага на выходе.</span><span class="sxs-lookup"><span data-stu-id="1b459-126">The type of activity taking place is returned as a flag on output.</span></span>
    
    On output, MAPI spooler can return one or more of the following flags:
    
<span data-ttu-id="1b459-127">LOGOFF_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="1b459-127">LOGOFF_COMPLETE</span></span> 
  
> <span data-ttu-id="1b459-128">Журнал может завершиться.</span><span class="sxs-lookup"><span data-stu-id="1b459-128">The logoff can complete.</span></span> <span data-ttu-id="1b459-129">Все ресурсы, связанные с хранилищем, были освобождены, а объект признан недействительным.</span><span class="sxs-lookup"><span data-stu-id="1b459-129">All resources associated with the store have been released, and the object has been invalidated.</span></span> <span data-ttu-id="1b459-130">Шпалер MAPI выполнил или выполнит все запросы.</span><span class="sxs-lookup"><span data-stu-id="1b459-130">The MAPI spooler has performed or will perform all requests.</span></span> <span data-ttu-id="1b459-131">В этой точке должен быть вызван только метод **IUnknown::Release** магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="1b459-131">Only the message store's **IUnknown::Release** method should be called at this point.</span></span> 
    
<span data-ttu-id="1b459-132">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="1b459-132">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="1b459-133">В настоящее время сообщение приходит в магазин от одного или более поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="1b459-133">A message is currently coming into the store from one or more transport providers.</span></span> 
    
<span data-ttu-id="1b459-134">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="1b459-134">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="1b459-135">В настоящее время сообщение отправляется из магазина одним или более поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="1b459-135">A message is currently being sent from the store by one or more transport providers.</span></span> 
    
<span data-ttu-id="1b459-136">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="1b459-136">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="1b459-137">В настоящее время сообщения в исходящие очереди для магазина.</span><span class="sxs-lookup"><span data-stu-id="1b459-137">There are currently messages in the outbound queue for the store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1b459-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1b459-138">Return value</span></span>

<span data-ttu-id="1b459-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="1b459-139">S_OK</span></span> 
  
> <span data-ttu-id="1b459-140">Процедура входа прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="1b459-140">The logoff procedure was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1b459-141">Примечания</span><span class="sxs-lookup"><span data-stu-id="1b459-141">Remarks</span></span>

<span data-ttu-id="1b459-142">Метод **IMAPISupport::StoreLogoffTransports** реализован для объектов поддержки поставщиков сообщений.</span><span class="sxs-lookup"><span data-stu-id="1b459-142">The **IMAPISupport::StoreLogoffTransports** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="1b459-143">Поставщики магазинов сообщений звонят **в StoreLogoffTransports,** чтобы предоставить клиентские приложениям определенный контроль над тем, как MAPI обрабатывает деятельность поставщика транспорта по мере закрытия магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="1b459-143">Message store providers call **StoreLogoffTransports** to give client applications some control over how MAPI handles transport provider activity as a message store is closing.</span></span> 
  
<span data-ttu-id="1b459-144">Если другой процесс должен открыть магазин для того же профиля, MAPI игнорирует вызов **в StoreLogoffTransports** и возвращает флаг LOGOFF_COMPLETE в _параметре lpulFlags._</span><span class="sxs-lookup"><span data-stu-id="1b459-144">If another process has the store to be logged off open for the same profile, MAPI ignores a call to **StoreLogoffTransports** and returns the flag LOGOFF_COMPLETE in the  _lpulFlags_ parameter.</span></span> 
  
<span data-ttu-id="1b459-145">Поведение поставщика магазина после возврата из **StoreLogoffTransports** должно основываться на значении  _lpulFlags,_ которое указывает состояние системы и передает инструкции клиента по поведению журналов.</span><span class="sxs-lookup"><span data-stu-id="1b459-145">The behavior of the store provider following the return from **StoreLogoffTransports** should be based on the value of  _lpulFlags_, which indicates system status and conveys client instructions for logoff behavior.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1b459-146">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="1b459-146">Notes to callers</span></span>

 <span data-ttu-id="1b459-147">**StoreLogoffTransports** обычно называется методом [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) поставщика магазина.</span><span class="sxs-lookup"><span data-stu-id="1b459-147">**StoreLogoffTransports** is typically called from a store provider's [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) method.</span></span> <span data-ttu-id="1b459-148">Однако его можно также назвать **методом IUnknown::Release** магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="1b459-148">However, it can also be called from the **IUnknown::Release** method of the message store.</span></span> <span data-ttu-id="1b459-149">Реализуйте **метод выпуска** вашего магазина сообщений, чтобы проверить, был ли звонок в **StoreLogoffTransports.**</span><span class="sxs-lookup"><span data-stu-id="1b459-149">Implement the **Release** method of your message store so you can check whether or not a call to **StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="1b459-150">Если вызов не произошел, позвоните **в StoreLogoffTransports** с LOGOFF_ABORT флагом.</span><span class="sxs-lookup"><span data-stu-id="1b459-150">If a call has not occurred, call **StoreLogoffTransports** with the LOGOFF_ABORT flag set.</span></span> 
  
<span data-ttu-id="1b459-151">Параметр  _lpulFlags задан_ флагу, который указывает, как клиент требует закрыть хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="1b459-151">The  _lpulFlags_ parameter is set to a flag that indicates how the client requires the message store to be shut down.</span></span> <span data-ttu-id="1b459-152">Определите соответствующий параметр  _для ulFlags_ на основе параметра соответствующего параметра в вызове **в StoreLogoff**.</span><span class="sxs-lookup"><span data-stu-id="1b459-152">Determine the appropriate setting for  _ulFlags_ based on the setting of the corresponding parameter in the call to **StoreLogoff**.</span></span> <span data-ttu-id="1b459-153">То есть, если клиент вызвал метод **StoreLogoff** с набором  _ulFlags_ LOGOFF_ORDERLY, необходимо вызвать **StoreLogoffTransports** с  _набором ulFlags_ для LOGOFF_ORDERLY.</span><span class="sxs-lookup"><span data-stu-id="1b459-153">That is, if a client called your **StoreLogoff** method with  _ulFlags_ set to LOGOFF_ORDERLY, you should call **StoreLogoffTransports** with  _ulFlags_ set to LOGOFF_ORDERLY.</span></span> 
  
<span data-ttu-id="1b459-154">Дополнительные сведения о процессе входа в хранилище сообщений см. в [журнале Shutting Down a Message Store Provider.](shutting-down-a-message-store-provider.md)</span><span class="sxs-lookup"><span data-stu-id="1b459-154">For more information about the message store logoff process, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1b459-155">См. также</span><span class="sxs-lookup"><span data-stu-id="1b459-155">See also</span></span>



[<span data-ttu-id="1b459-156">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="1b459-156">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="1b459-157">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="1b459-157">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="1b459-158">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1b459-158">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

