---
title: Имаписуппортсторелогоффтранспортс
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326497"
---
# <a name="imapisupportstorelogofftransports"></a><span data-ttu-id="8f2e6-103">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="8f2e6-103">IMAPISupport::StoreLogoffTransports</span></span>

  
  
<span data-ttu-id="8f2e6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f2e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f2e6-105">ЗаПрашивает выпуск хранилища сообщений по расрядку.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-105">Requests the orderly release of a message store.</span></span>
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8f2e6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8f2e6-106">Parameters</span></span>

 <span data-ttu-id="8f2e6-107">_Лпулфлагс_</span><span class="sxs-lookup"><span data-stu-id="8f2e6-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="8f2e6-108">[вход, выход] Битовая маска флагов, определяющих способ выхода из хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-108">[in, out] A bitmask of flags that controls how message store logoff occurs.</span></span> <span data-ttu-id="8f2e6-109">Во входных данных все флаги этого параметра являются взаимоисключающими; для каждого вызова можно задать только один из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="8f2e6-109">On input, all flags for this parameter are mutually exclusive; only one of the following flags can be set per call:</span></span>
    
<span data-ttu-id="8f2e6-110">ЛОГОФФ_АБОРТ</span><span class="sxs-lookup"><span data-stu-id="8f2e6-110">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="8f2e6-111">Перед выходом из системы необходимо остановить все действия поставщика транспорта для этого хранилища.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-111">Any transport provider activity for this store should be stopped before logoff.</span></span> <span data-ttu-id="8f2e6-112">Управление возвращается клиенту после того, как действие остановлено, а диспетчер очереди MAPI вышел из хранилища.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-112">Control is returned to the client after the activity is stopped and the MAPI spooler has logged off the store.</span></span> <span data-ttu-id="8f2e6-113">Если выполняется какое-либо действие транспорта, выход из системы не выполняется, и не происходит никаких изменений в работе диспетчера очереди MAPI или поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-113">If any transport activity is taking place, the logoff does not occur and no change in the MAPI spooler or transport provider behavior occurs.</span></span> <span data-ttu-id="8f2e6-114">Если в настоящее время нет действий, то диспетчер очереди MAPI освобождает хранилище.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-114">If there is currently no activity, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="8f2e6-115">ЛОГОФФ_НО_ВАИТ</span><span class="sxs-lookup"><span data-stu-id="8f2e6-115">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="8f2e6-116">Диспетчер очереди MAPI должен освобождать хранилище и возвращать его клиенту сразу после отправки всей исходящей почты, готовой к отправке.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-116">The MAPI spooler should release the store and return control to the client immediately after all outbound mail that is ready to be sent is sent.</span></span> <span data-ttu-id="8f2e6-117">Если в хранилище сообщений есть папка "Входящие" по умолчанию, то будет получено любое сообщение в процессе, а затем дальнейший прием отключен.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-117">If the message store has the default Inbox, any in-process message is received, and then further reception is disabled.</span></span> 
    
<span data-ttu-id="8f2e6-118">ЛОГОФФ_ОРДЕРЛИ</span><span class="sxs-lookup"><span data-stu-id="8f2e6-118">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="8f2e6-119">Диспетчер очереди MAPI должен освободить хранилище и вернуть управление клиенту сразу после обработки всех ожидающих сообщений.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-119">The MAPI spooler should release the store and return control to the client immediately after any pending messages are finished processing.</span></span> <span data-ttu-id="8f2e6-120">Новые сообщения не обрабатываются.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-120">No new messages should be processed.</span></span> 
    
<span data-ttu-id="8f2e6-121">ЛОГОФФ_ПУРЖЕ</span><span class="sxs-lookup"><span data-stu-id="8f2e6-121">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="8f2e6-122">Работает так же, как и флаг ЛОГОФФ_НО_ВАИТ.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-122">Works the same as the LOGOFF_NO_WAIT flag.</span></span> <span data-ttu-id="8f2e6-123">Флаг ЛОГОФФ_ПУРЖЕ возвращает управление вызывающей стороне после завершения.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-123">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="8f2e6-124">ЛОГОФФ_КУИЕТ</span><span class="sxs-lookup"><span data-stu-id="8f2e6-124">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="8f2e6-125">Если выполняется какое-либо действие поставщика транспорта, выход из системы не должен выполняться.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-125">The logoff should not occur if any transport provider activity is taking place.</span></span> <span data-ttu-id="8f2e6-126">Тип выполняемого действия возвращается в виде флага в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-126">The type of activity taking place is returned as a flag on output.</span></span>
    
    On output, MAPI spooler can return one or more of the following flags:
    
<span data-ttu-id="8f2e6-127">ЛОГОФФ_КОМПЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="8f2e6-127">LOGOFF_COMPLETE</span></span> 
  
> <span data-ttu-id="8f2e6-128">Может завершиться выход из системы.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-128">The logoff can complete.</span></span> <span data-ttu-id="8f2e6-129">Все ресурсы, связанные с хранилищем, были выпущены, а объект является недействительным.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-129">All resources associated with the store have been released, and the object has been invalidated.</span></span> <span data-ttu-id="8f2e6-130">Очередь MAPI выполнила или выполнит все запросы.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-130">The MAPI spooler has performed or will perform all requests.</span></span> <span data-ttu-id="8f2e6-131">В этой точке должен быть вызван только метод **IUnknown:: Release** хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-131">Only the message store's **IUnknown::Release** method should be called at this point.</span></span> 
    
<span data-ttu-id="8f2e6-132">ЛОГОФФ_ИНБАУНД</span><span class="sxs-lookup"><span data-stu-id="8f2e6-132">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="8f2e6-133">В данный момент сообщение поступает в хранилище от одного или нескольких поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-133">A message is currently coming into the store from one or more transport providers.</span></span> 
    
<span data-ttu-id="8f2e6-134">ЛОГОФФ_АУТБАУНД</span><span class="sxs-lookup"><span data-stu-id="8f2e6-134">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="8f2e6-135">В данный момент сообщение отправляется из хранилища одним или несколькими поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-135">A message is currently being sent from the store by one or more transport providers.</span></span> 
    
<span data-ttu-id="8f2e6-136">ЛОГОФФ_АУТБАУНД_КУЕУЕ</span><span class="sxs-lookup"><span data-stu-id="8f2e6-136">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="8f2e6-137">В данный момент в очереди исходящих сообщений для этого хранилища есть сообщения.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-137">There are currently messages in the outbound queue for the store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8f2e6-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8f2e6-138">Return value</span></span>

<span data-ttu-id="8f2e6-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="8f2e6-139">S_OK</span></span> 
  
> <span data-ttu-id="8f2e6-140">Процедура выхода выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-140">The logoff procedure was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8f2e6-141">Замечания</span><span class="sxs-lookup"><span data-stu-id="8f2e6-141">Remarks</span></span>

<span data-ttu-id="8f2e6-142">Метод **имаписуппорт:: сторелогоффтранспортс** реализован для объектов поддержки поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-142">The **IMAPISupport::StoreLogoffTransports** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="8f2e6-143">Поставщики хранилищ сообщений вызывают **сторелогоффтранспортс** , чтобы предоставить клиентским приложениям возможность управления процессом обработки службой MAPI действия поставщика транспорта в случае закрытия хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-143">Message store providers call **StoreLogoffTransports** to give client applications some control over how MAPI handles transport provider activity as a message store is closing.</span></span> 
  
<span data-ttu-id="8f2e6-144">Если для одного и того же профиля другой процесс отключился от магазина, MAPI игнорирует вызов **сторелогоффтранспортс** и ВОЗВРАЩАЕТ флаг логофф_комплете в параметре _лпулфлагс_ .</span><span class="sxs-lookup"><span data-stu-id="8f2e6-144">If another process has the store to be logged off open for the same profile, MAPI ignores a call to **StoreLogoffTransports** and returns the flag LOGOFF_COMPLETE in the  _lpulFlags_ parameter.</span></span> 
  
<span data-ttu-id="8f2e6-145">Поведение поставщика услуг хранения, следующего за возвратом из **сторелогоффтранспортс** , должно основываться на значении _лпулфлагс_, которое указывает состояние системы и передает клиентские инструкции для выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-145">The behavior of the store provider following the return from **StoreLogoffTransports** should be based on the value of  _lpulFlags_, which indicates system status and conveys client instructions for logoff behavior.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8f2e6-146">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="8f2e6-146">Notes to callers</span></span>

 <span data-ttu-id="8f2e6-147">**Сторелогоффтранспортс** обычно вызывается из метода [IMsgStore:: сторелогофф](imsgstore-storelogoff.md) поставщика хранилища.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-147">**StoreLogoffTransports** is typically called from a store provider's [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) method.</span></span> <span data-ttu-id="8f2e6-148">Однако он также может вызываться из метода **IUnknown:: Release** хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-148">However, it can also be called from the **IUnknown::Release** method of the message store.</span></span> <span data-ttu-id="8f2e6-149">Реализуйте метод **Release** хранилища сообщений, чтобы можно было проверить, не вызван ли вызов **сторелогоффтранспортс** .</span><span class="sxs-lookup"><span data-stu-id="8f2e6-149">Implement the **Release** method of your message store so you can check whether or not a call to **StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="8f2e6-150">Если вызов не выполнялся, вызовите **сторелогоффтранспортс** с установленным флагом логофф_аборт.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-150">If a call has not occurred, call **StoreLogoffTransports** with the LOGOFF_ABORT flag set.</span></span> 
  
<span data-ttu-id="8f2e6-151">В параметре _лпулфлагс_ задается флаг, указывающий, как клиенту требуется завершение работы хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-151">The  _lpulFlags_ parameter is set to a flag that indicates how the client requires the message store to be shut down.</span></span> <span data-ttu-id="8f2e6-152">Определите соответствующий параметр для _ulFlags_ в соответствии с параметром соответствующего параметра в вызове **сторелогофф**.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-152">Determine the appropriate setting for  _ulFlags_ based on the setting of the corresponding parameter in the call to **StoreLogoff**.</span></span> <span data-ttu-id="8f2e6-153">То есть, если клиент, вызываемый методом **сторелогофф** с _ulFlags_ , имеет значение Логофф_ордерли, необходимо вызвать **сторелогоффтранспортс** с _ulFlags_ , равным логофф_ордерли.</span><span class="sxs-lookup"><span data-stu-id="8f2e6-153">That is, if a client called your **StoreLogoff** method with  _ulFlags_ set to LOGOFF_ORDERLY, you should call **StoreLogoffTransports** with  _ulFlags_ set to LOGOFF_ORDERLY.</span></span> 
  
<span data-ttu-id="8f2e6-154">Дополнительные сведения о процессе выхода из хранилища сообщений приведены в разделе [Завершение работы поставщика хранилища сообщений](shutting-down-a-message-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8f2e6-154">For more information about the message store logoff process, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8f2e6-155">См. также</span><span class="sxs-lookup"><span data-stu-id="8f2e6-155">See also</span></span>



[<span data-ttu-id="8f2e6-156">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="8f2e6-156">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="8f2e6-157">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="8f2e6-157">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="8f2e6-158">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8f2e6-158">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

