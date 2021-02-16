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
# <a name="imapisupportstorelogofftransports"></a><span data-ttu-id="320de-103">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="320de-103">IMAPISupport::StoreLogoffTransports</span></span>

  
  
<span data-ttu-id="320de-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="320de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="320de-105">Запрашивает упорядоченный выпуск хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="320de-105">Requests the orderly release of a message store.</span></span>
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="320de-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="320de-106">Parameters</span></span>

 <span data-ttu-id="320de-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="320de-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="320de-108">[in, out] Битоваяmas флагов, которая управляет процессом входа в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="320de-108">[in, out] A bitmask of flags that controls how message store logoff occurs.</span></span> <span data-ttu-id="320de-109">При вводе все флаги для этого параметра являются взаимоисключающими; Для каждого вызова можно установить только один из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="320de-109">On input, all flags for this parameter are mutually exclusive; only one of the following flags can be set per call:</span></span>
    
<span data-ttu-id="320de-110">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="320de-110">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="320de-111">Все действия поставщика транспорта для этого магазина должны быть остановлены перед тем, как выйти из системы.</span><span class="sxs-lookup"><span data-stu-id="320de-111">Any transport provider activity for this store should be stopped before logoff.</span></span> <span data-ttu-id="320de-112">Управление возвращается клиенту после того, как действие остановлено, и пулер MAPI выошел из магазина.</span><span class="sxs-lookup"><span data-stu-id="320de-112">Control is returned to the client after the activity is stopped and the MAPI spooler has logged off the store.</span></span> <span data-ttu-id="320de-113">Если какие-либо действия транспорта происходят, то выйдите из системы, а поведение поставщика транспорта или пула MAPI не изменится.</span><span class="sxs-lookup"><span data-stu-id="320de-113">If any transport activity is taking place, the logoff does not occur and no change in the MAPI spooler or transport provider behavior occurs.</span></span> <span data-ttu-id="320de-114">Если в настоящее время действий нет, то пульщик MAPI освобождает хранилище.</span><span class="sxs-lookup"><span data-stu-id="320de-114">If there is currently no activity, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="320de-115">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="320de-115">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="320de-116">Пулер MAPI должен освободить хранилище и вернуть управление клиенту сразу после того, как будет отправлена вся готовая к рассылке почта.</span><span class="sxs-lookup"><span data-stu-id="320de-116">The MAPI spooler should release the store and return control to the client immediately after all outbound mail that is ready to be sent is sent.</span></span> <span data-ttu-id="320de-117">Если в хранилище сообщений есть почта по умолчанию, то получается любое сообщение, которое находится в процессе, а затем дополнительная приемная будет отключена.</span><span class="sxs-lookup"><span data-stu-id="320de-117">If the message store has the default Inbox, any in-process message is received, and then further reception is disabled.</span></span> 
    
<span data-ttu-id="320de-118">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="320de-118">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="320de-119">Пулер MAPI должен освободить хранилище и вернуть управление клиенту сразу после завершения обработки ожидающих сообщений.</span><span class="sxs-lookup"><span data-stu-id="320de-119">The MAPI spooler should release the store and return control to the client immediately after any pending messages are finished processing.</span></span> <span data-ttu-id="320de-120">Новые сообщения не должны обрабатываться.</span><span class="sxs-lookup"><span data-stu-id="320de-120">No new messages should be processed.</span></span> 
    
<span data-ttu-id="320de-121">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="320de-121">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="320de-122">Работает так же, как флаг LOGOFF_NO_WAIT.</span><span class="sxs-lookup"><span data-stu-id="320de-122">Works the same as the LOGOFF_NO_WAIT flag.</span></span> <span data-ttu-id="320de-123">Флаг LOGOFF_PURGE возвращает управление вызываемой по завершении.</span><span class="sxs-lookup"><span data-stu-id="320de-123">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="320de-124">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="320de-124">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="320de-125">Вход не должен происходить, если происходит какой-либо из действий поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="320de-125">The logoff should not occur if any transport provider activity is taking place.</span></span> <span data-ttu-id="320de-126">Тип действия, которое происходит, возвращается в качестве флага при выходе.</span><span class="sxs-lookup"><span data-stu-id="320de-126">The type of activity taking place is returned as a flag on output.</span></span>
    
    On output, MAPI spooler can return one or more of the following flags:
    
<span data-ttu-id="320de-127">LOGOFF_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="320de-127">LOGOFF_COMPLETE</span></span> 
  
> <span data-ttu-id="320de-128">Выйдите из нее.</span><span class="sxs-lookup"><span data-stu-id="320de-128">The logoff can complete.</span></span> <span data-ttu-id="320de-129">Все ресурсы, связанные с хранилищем, освобождены, а объект стал недействительным.</span><span class="sxs-lookup"><span data-stu-id="320de-129">All resources associated with the store have been released, and the object has been invalidated.</span></span> <span data-ttu-id="320de-130">Пулер MAPI выполнил или выполнит все запросы.</span><span class="sxs-lookup"><span data-stu-id="320de-130">The MAPI spooler has performed or will perform all requests.</span></span> <span data-ttu-id="320de-131">На этом этапе должен быть вызван только метод **IUnknown::Release** в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="320de-131">Only the message store's **IUnknown::Release** method should be called at this point.</span></span> 
    
<span data-ttu-id="320de-132">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="320de-132">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="320de-133">В настоящее время в хранилище приходит сообщение от одного или более поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="320de-133">A message is currently coming into the store from one or more transport providers.</span></span> 
    
<span data-ttu-id="320de-134">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="320de-134">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="320de-135">В настоящее время сообщение отправляется из магазина одним или более поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="320de-135">A message is currently being sent from the store by one or more transport providers.</span></span> 
    
<span data-ttu-id="320de-136">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="320de-136">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="320de-137">В настоящее время в очереди исходящие сообщения для магазина.</span><span class="sxs-lookup"><span data-stu-id="320de-137">There are currently messages in the outbound queue for the store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="320de-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="320de-138">Return value</span></span>

<span data-ttu-id="320de-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="320de-139">S_OK</span></span> 
  
> <span data-ttu-id="320de-140">Процедура logoff прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="320de-140">The logoff procedure was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="320de-141">Примечания</span><span class="sxs-lookup"><span data-stu-id="320de-141">Remarks</span></span>

<span data-ttu-id="320de-142">Метод **IMAPISupport::StoreLogoffTransports** реализован для объектов поддержки поставщика store сообщений.</span><span class="sxs-lookup"><span data-stu-id="320de-142">The **IMAPISupport::StoreLogoffTransports** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="320de-143">Поставщики store сообщений звонят **в StoreLogoffTransports,** чтобы предоставить клиентские приложениям некоторый контроль над тем, как MAPI обрабатывает действия поставщиков транспорта, когда хранилище сообщений закрывается.</span><span class="sxs-lookup"><span data-stu-id="320de-143">Message store providers call **StoreLogoffTransports** to give client applications some control over how MAPI handles transport provider activity as a message store is closing.</span></span> 
  
<span data-ttu-id="320de-144">Если для другого процесса необходимо отключить хранилище для того же профиля, MAPI игнорирует вызов **StoreLogoffTransports** и возвращает флаг LOGOFF_COMPLETE в _параметре lpulFlags._</span><span class="sxs-lookup"><span data-stu-id="320de-144">If another process has the store to be logged off open for the same profile, MAPI ignores a call to **StoreLogoffTransports** and returns the flag LOGOFF_COMPLETE in the  _lpulFlags_ parameter.</span></span> 
  
<span data-ttu-id="320de-145">Поведение поставщика магазина после возврата **из StoreLogoffTransports** должно основываться на значении  _lpulFlags,_ которое указывает состояние системы и передает клиентские инструкции для поведения при выйдите из системы.</span><span class="sxs-lookup"><span data-stu-id="320de-145">The behavior of the store provider following the return from **StoreLogoffTransports** should be based on the value of  _lpulFlags_, which indicates system status and conveys client instructions for logoff behavior.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="320de-146">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="320de-146">Notes to callers</span></span>

 <span data-ttu-id="320de-147">**StoreLogoffTransports** обычно вызван из метода [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) поставщика магазина.</span><span class="sxs-lookup"><span data-stu-id="320de-147">**StoreLogoffTransports** is typically called from a store provider's [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) method.</span></span> <span data-ttu-id="320de-148">Однако его также можно использовать из метода **IUnknown::Release** в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="320de-148">However, it can also be called from the **IUnknown::Release** method of the message store.</span></span> <span data-ttu-id="320de-149">**Внедрите метод Release** для вашего хранения сообщений, чтобы можно было проверить, был ли выполнен вызов **StoreLogoffTransports.**</span><span class="sxs-lookup"><span data-stu-id="320de-149">Implement the **Release** method of your message store so you can check whether or not a call to **StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="320de-150">Если вызов не произошел, вызовите **StoreLogoffTransports** с установленным LOGOFF_ABORT флагом.</span><span class="sxs-lookup"><span data-stu-id="320de-150">If a call has not occurred, call **StoreLogoffTransports** with the LOGOFF_ABORT flag set.</span></span> 
  
<span data-ttu-id="320de-151">Для  _параметра lpulFlags_ установлен флаг, который указывает, как клиент требует, чтобы хранилище сообщений было закрыто.</span><span class="sxs-lookup"><span data-stu-id="320de-151">The  _lpulFlags_ parameter is set to a flag that indicates how the client requires the message store to be shut down.</span></span> <span data-ttu-id="320de-152">Определите соответствующий параметр _для ulFlags_ на основе параметра соответствующего параметра в вызове **StoreLogoff.**</span><span class="sxs-lookup"><span data-stu-id="320de-152">Determine the appropriate setting for  _ulFlags_ based on the setting of the corresponding parameter in the call to **StoreLogoff**.</span></span> <span data-ttu-id="320de-153">То есть, если клиент называется **методом StoreLogoff,** для  _ulFlags_ установлено LOGOFF_ORDERLY, следует вызвать **StoreLogoffTransports,** для  _ulFlags_ установлено LOGOFF_ORDERLY.</span><span class="sxs-lookup"><span data-stu-id="320de-153">That is, if a client called your **StoreLogoff** method with  _ulFlags_ set to LOGOFF_ORDERLY, you should call **StoreLogoffTransports** with  _ulFlags_ set to LOGOFF_ORDERLY.</span></span> 
  
<span data-ttu-id="320de-154">Дополнительные сведения о процессе выключения из магазина сообщений см. в записи ["Завершение работы поставщика store сообщений".](shutting-down-a-message-store-provider.md)</span><span class="sxs-lookup"><span data-stu-id="320de-154">For more information about the message store logoff process, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="320de-155">См. также</span><span class="sxs-lookup"><span data-stu-id="320de-155">See also</span></span>



[<span data-ttu-id="320de-156">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="320de-156">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="320de-157">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="320de-157">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="320de-158">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="320de-158">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

