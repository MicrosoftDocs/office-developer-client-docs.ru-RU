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
ms.openlocfilehash: b77a58b04e5cdeee7a9e84051a6ed287c1a20115
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578313"
---
# <a name="imapisupportstorelogofftransports"></a><span data-ttu-id="f223f-103">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="f223f-103">IMAPISupport::StoreLogoffTransports</span></span>

  
  
<span data-ttu-id="f223f-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f223f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f223f-105">Запрашивает надлежащей выпуске хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="f223f-105">Requests the orderly release of a message store.</span></span>
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f223f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f223f-106">Parameters</span></span>

 <span data-ttu-id="f223f-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="f223f-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="f223f-108">[in, out] Битовая маска флаги, определяющее, как выполняется выход из системы хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="f223f-108">[in, out] A bitmask of flags that controls how message store logoff occurs.</span></span> <span data-ttu-id="f223f-109">На входе все флаги для этого параметра являются взаимоисключающими; только один из следующих флагов можно установить на вызов.</span><span class="sxs-lookup"><span data-stu-id="f223f-109">On input, all flags for this parameter are mutually exclusive; only one of the following flags can be set per call:</span></span>
    
<span data-ttu-id="f223f-110">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="f223f-110">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="f223f-111">Какие-либо действия поставщика транспорта для этого хранилища должна быть прекращена до выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="f223f-111">Any transport provider activity for this store should be stopped before logoff.</span></span> <span data-ttu-id="f223f-112">Управление возвращается клиенту после остановки операции и диспетчер очереди MAPI вышел хранилище.</span><span class="sxs-lookup"><span data-stu-id="f223f-112">Control is returned to the client after the activity is stopped and the MAPI spooler has logged off the store.</span></span> <span data-ttu-id="f223f-113">Если какие-либо действия транспорта с удалением, выход из системы не происходит и не изменяется поведение поставщика транспорта или диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="f223f-113">If any transport activity is taking place, the logoff does not occur and no change in the MAPI spooler or transport provider behavior occurs.</span></span> <span data-ttu-id="f223f-114">Если в данный момент не выполняет никаких действий, диспетчер очереди MAPI освобождает хранилище.</span><span class="sxs-lookup"><span data-stu-id="f223f-114">If there is currently no activity, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="f223f-115">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="f223f-115">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="f223f-116">Диспетчер очереди MAPI следует освобождение хранилище и возврата в клиенте сразу отправляется в конце концов исходящей почты, Готово к отправке.</span><span class="sxs-lookup"><span data-stu-id="f223f-116">The MAPI spooler should release the store and return control to the client immediately after all outbound mail that is ready to be sent is sent.</span></span> <span data-ttu-id="f223f-117">Если хранилище сообщений по умолчанию папки "Входящие", полученного сообщения в процесс и затем отключена дальнейший приема.</span><span class="sxs-lookup"><span data-stu-id="f223f-117">If the message store has the default Inbox, any in-process message is received, and then further reception is disabled.</span></span> 
    
<span data-ttu-id="f223f-118">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="f223f-118">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="f223f-119">Диспетчер очереди MAPI должен освобождать хранилище и возврата в клиент сразу же после все ожидающие сообщения будут завершены обработки.</span><span class="sxs-lookup"><span data-stu-id="f223f-119">The MAPI spooler should release the store and return control to the client immediately after any pending messages are finished processing.</span></span> <span data-ttu-id="f223f-120">Новые сообщения будут обрабатываться.</span><span class="sxs-lookup"><span data-stu-id="f223f-120">No new messages should be processed.</span></span> 
    
<span data-ttu-id="f223f-121">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="f223f-121">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="f223f-122">Работает так же, как флаг LOGOFF_NO_WAIT.</span><span class="sxs-lookup"><span data-stu-id="f223f-122">Works the same as the LOGOFF_NO_WAIT flag.</span></span> <span data-ttu-id="f223f-123">После завершения флаг LOGOFF_PURGE возвращает управление вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="f223f-123">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="f223f-124">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="f223f-124">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="f223f-125">Выход из системы появляется, если какие-либо действия поставщика транспорта, предпринимаются.</span><span class="sxs-lookup"><span data-stu-id="f223f-125">The logoff should not occur if any transport provider activity is taking place.</span></span> <span data-ttu-id="f223f-126">Тип действия с удалением возвращается как флаг на выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f223f-126">The type of activity taking place is returned as a flag on output.</span></span>
    
    On output, MAPI spooler can return one or more of the following flags:
    
<span data-ttu-id="f223f-127">LOGOFF_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="f223f-127">LOGOFF_COMPLETE</span></span> 
  
> <span data-ttu-id="f223f-128">Выход из системы можно выполнить.</span><span class="sxs-lookup"><span data-stu-id="f223f-128">The logoff can complete.</span></span> <span data-ttu-id="f223f-129">Все ресурсы, связанные с хранилищем выпущенные и объект является недействительным.</span><span class="sxs-lookup"><span data-stu-id="f223f-129">All resources associated with the store have been released, and the object has been invalidated.</span></span> <span data-ttu-id="f223f-130">Диспетчер очереди MAPI выполнил или будет выполнять все запросы.</span><span class="sxs-lookup"><span data-stu-id="f223f-130">The MAPI spooler has performed or will perform all requests.</span></span> <span data-ttu-id="f223f-131">На этом этапе следует вызывать только метод **функции IUnknown::Release** хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="f223f-131">Only the message store's **IUnknown::Release** method should be called at this point.</span></span> 
    
<span data-ttu-id="f223f-132">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="f223f-132">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="f223f-133">Сообщение в настоящее время поступают в хранилище данных из одного или нескольких поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="f223f-133">A message is currently coming into the store from one or more transport providers.</span></span> 
    
<span data-ttu-id="f223f-134">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="f223f-134">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="f223f-135">В настоящее время отправляется из хранилища с одним или несколькими поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="f223f-135">A message is currently being sent from the store by one or more transport providers.</span></span> 
    
<span data-ttu-id="f223f-136">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="f223f-136">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="f223f-137">В настоящий момент в очереди исходящих сообщений для хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="f223f-137">There are currently messages in the outbound queue for the store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f223f-138">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="f223f-138">Return value</span></span>

<span data-ttu-id="f223f-139">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="f223f-139">S_OK</span></span> 
  
> <span data-ttu-id="f223f-140">Процедура logoff прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="f223f-140">The logoff procedure was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f223f-141">Замечания</span><span class="sxs-lookup"><span data-stu-id="f223f-141">Remarks</span></span>

<span data-ttu-id="f223f-142">Метод **IMAPISupport::StoreLogoffTransports** реализуется для объектов поддержки поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="f223f-142">The **IMAPISupport::StoreLogoffTransports** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="f223f-143">Поставщики хранилища сообщений вызов **StoreLogoffTransports** для предоставления клиентским приложениям управлять тем, как закрытие действие поставщика маркеров транспорта MAPI в качестве хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="f223f-143">Message store providers call **StoreLogoffTransports** to give client applications some control over how MAPI handles transport provider activity as a message store is closing.</span></span> 
  
<span data-ttu-id="f223f-144">Если другим процессом хранилища выходите открыть для одного профиля, MAPI игнорирует вызов **StoreLogoffTransports** и возвращает флаг LOGOFF_COMPLETE с помощью параметра _lpulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="f223f-144">If another process has the store to be logged off open for the same profile, MAPI ignores a call to **StoreLogoffTransports** and returns the flag LOGOFF_COMPLETE in the  _lpulFlags_ parameter.</span></span> 
  
<span data-ttu-id="f223f-145">Поведение поставщика хранилища после возврата из **StoreLogoffTransports** должен быть основан на значение _lpulFlags_, который указывает на состояние системы и передает клиента инструкции по поведение выход из системы.</span><span class="sxs-lookup"><span data-stu-id="f223f-145">The behavior of the store provider following the return from **StoreLogoffTransports** should be based on the value of  _lpulFlags_, which indicates system status and conveys client instructions for logoff behavior.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f223f-146">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="f223f-146">Notes to callers</span></span>

 <span data-ttu-id="f223f-147">**StoreLogoffTransports** обычно вызван метод [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) поставщика хранилища.</span><span class="sxs-lookup"><span data-stu-id="f223f-147">**StoreLogoffTransports** is typically called from a store provider's [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) method.</span></span> <span data-ttu-id="f223f-148">Тем не менее он может вызываться также из метода **функции IUnknown::Release** хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="f223f-148">However, it can also be called from the **IUnknown::Release** method of the message store.</span></span> <span data-ttu-id="f223f-149">Реализуйте метод **Release** для хранения сообщений, вы можете проверить ли вызов **StoreLogoffTransports** , выполненных.</span><span class="sxs-lookup"><span data-stu-id="f223f-149">Implement the **Release** method of your message store so you can check whether or not a call to **StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="f223f-150">Если звонок не произошло, вызовите **StoreLogoffTransports** с установленным флагом LOGOFF_ABORT.</span><span class="sxs-lookup"><span data-stu-id="f223f-150">If a call has not occurred, call **StoreLogoffTransports** with the LOGOFF_ABORT flag set.</span></span> 
  
<span data-ttu-id="f223f-151">Параметр _lpulFlags_ имеет значение флаг, указывающий, как клиент требует хранилище сообщений, чтобы завершить работу.</span><span class="sxs-lookup"><span data-stu-id="f223f-151">The  _lpulFlags_ parameter is set to a flag that indicates how the client requires the message store to be shut down.</span></span> <span data-ttu-id="f223f-152">Определение подходящей настройки для _ulFlags_ на основе параметра соответствующий параметр в вызове **StoreLogoff**.</span><span class="sxs-lookup"><span data-stu-id="f223f-152">Determine the appropriate setting for  _ulFlags_ based on the setting of the corresponding parameter in the call to **StoreLogoff**.</span></span> <span data-ttu-id="f223f-153">То есть клиент вызванный метод **StoreLogoff** с _ulFlags_ , задайте значение LOGOFF_ORDERLY, необходимо вызвать **StoreLogoffTransports** с _ulFlags_ , задайте значение LOGOFF_ORDERLY.</span><span class="sxs-lookup"><span data-stu-id="f223f-153">That is, if a client called your **StoreLogoff** method with  _ulFlags_ set to LOGOFF_ORDERLY, you should call **StoreLogoffTransports** with  _ulFlags_ set to LOGOFF_ORDERLY.</span></span> 
  
<span data-ttu-id="f223f-154">Дополнительные сведения о процессе выхода из системы хранения сообщений можно [Завершает работу сообщение поставщика хранилища](shutting-down-a-message-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f223f-154">For more information about the message store logoff process, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f223f-155">См. также</span><span class="sxs-lookup"><span data-stu-id="f223f-155">See also</span></span>



[<span data-ttu-id="f223f-156">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="f223f-156">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="f223f-157">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="f223f-157">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="f223f-158">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f223f-158">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

