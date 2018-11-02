---
title: IXPLogonSubmitMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.SubmitMessage
api_type:
- COM
ms.assetid: a261ba0d-cb56-4935-b745-1d4bbd0b8b9d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 28e7874d1e61c0a4fe0ad702f206ca03a9a1096a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575877"
---
# <a name="ixplogonsubmitmessage"></a><span data-ttu-id="9e7e7-103">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="9e7e7-103">IXPLogon::SubmitMessage</span></span>

  
  
<span data-ttu-id="9e7e7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e7e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e7e7-105">Указывает, что диспетчер очереди MAPI для поставщика транспорта для доставки сообщения.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-105">Indicates that the MAPI spooler has a message for the transport provider to deliver.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef,
  ULONG FAR * lpulReturnParm
);
```

## <a name="parameters"></a><span data-ttu-id="9e7e7-106">���������</span><span class="sxs-lookup"><span data-stu-id="9e7e7-106">Parameters</span></span>

 <span data-ttu-id="9e7e7-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9e7e7-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9e7e7-108">[in] Битовая маска флаги, который определяет, как отправить сообщение.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-108">[in] A bitmask of flags that controls how the message is submitted.</span></span> <span data-ttu-id="9e7e7-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="9e7e7-109">The following flag can be set:</span></span>
    
<span data-ttu-id="9e7e7-110">BEGIN_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="9e7e7-110">BEGIN_DEFERRED</span></span> 
  
> <span data-ttu-id="9e7e7-111">Диспетчер очереди MAPI вызывает поставщика транспорта с сообщением, которое ранее отложено.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-111">The MAPI spooler is calling a transport provider with a message that was previously deferred.</span></span> <span data-ttu-id="9e7e7-112">Идентификатор записи сообщения совпадает с при его отложено.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-112">The entry identifier of the message is the same as when it was deferred.</span></span> <span data-ttu-id="9e7e7-113">Сообщение отложено, передав ее идентификатор записи обратно в диспетчер очереди MAPI с помощью метода [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) с флагом NOTIFY_SENTDEFERRED.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-113">The message was deferred by passing its entry identifier back to the MAPI spooler by using the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_SENTDEFERRED flag.</span></span> 
    
 <span data-ttu-id="9e7e7-114">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="9e7e7-114">_lpMessage_</span></span>
  
> <span data-ttu-id="9e7e7-115">[in] Указатель на объект message (представляющие сообщения для доставки), которая имеет разрешение на чтение/запись, поставщика транспорта, используемый для доступа и работы с этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-115">[in] A pointer to a message object (representing the message to deliver) that has read/write permission, which the transport provider uses to access and manipulate that message.</span></span> <span data-ttu-id="9e7e7-116">Этот объект действителен до того времени, после поставщика транспорта возвращает из последующих вызов метода [IXPLogon::EndMessage](ixplogon-endmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="9e7e7-116">This object remains valid until after the transport provider returns from a subsequent call to the [IXPLogon::EndMessage](ixplogon-endmessage.md) method.</span></span> 
    
 <span data-ttu-id="9e7e7-117">_lpulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="9e7e7-117">_lpulMsgRef_</span></span>
  
> <span data-ttu-id="9e7e7-118">[out] Указатель на переменную, в котором поставщика транспорта возвращает значение ссылки, назначенных для данного сообщения.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-118">[out] A pointer to a variable in which the transport provider returns the reference value it assigned to this message.</span></span> <span data-ttu-id="9e7e7-119">Диспетчер очереди MAPI передает это значение ссылку в последующих вызовов для данного сообщения.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-119">The MAPI spooler passes this reference value in subsequent calls for this message.</span></span> <span data-ttu-id="9e7e7-120">Диспетчер очереди MAPI Инициализирует значение 0 перед возвращением поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-120">The MAPI spooler initializes the value to 0 before returning it to the transport provider.</span></span>
    
 <span data-ttu-id="9e7e7-121">_lpulReturnParm_</span><span class="sxs-lookup"><span data-stu-id="9e7e7-121">_lpulReturnParm_</span></span>
  
> <span data-ttu-id="9e7e7-122">[out] Указатель на переменную, которая соответствует значению MAPI_E_WAIT или MAPI_E_NETWORK_ERROR об ошибке, возвращенное **SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-122">[out] A pointer to a variable that corresponds to the MAPI_E_WAIT or MAPI_E_NETWORK_ERROR error value returned by **SubmitMessage**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9e7e7-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e7e7-123">Return value</span></span>

<span data-ttu-id="9e7e7-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="9e7e7-124">S_OK</span></span> 
  
> <span data-ttu-id="9e7e7-125">Вызов успешно и возвращается ожидаемым значением или значения.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-125">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="9e7e7-126">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="9e7e7-126">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="9e7e7-127">Поставщика транспорта не может обрабатывать сообщения, так как он выполнение другой операции.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-127">The transport provider cannot handle the message, because it is performing another operation.</span></span> <span data-ttu-id="9e7e7-128">Для указания, что обработка не произошло и диспетчер очереди MAPI не должны вызывать **EndMessage**поставщика следует использовать это возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-128">A provider should use this return value to indicate that no processing occurred and that the MAPI spooler should not call **EndMessage**.</span></span> <span data-ttu-id="9e7e7-129">Диспетчер очереди MAPI повторите вызов **SubmitMessage** попытку позже.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-129">The MAPI spooler will try the **SubmitMessage** call again later.</span></span> 
    
<span data-ttu-id="9e7e7-130">MAPI_E_CANCEL</span><span class="sxs-lookup"><span data-stu-id="9e7e7-130">MAPI_E_CANCEL</span></span> 
  
> <span data-ttu-id="9e7e7-131">Хотя поставщика транспорта и запрашивает, что диспетчер очереди MAPI повторно отправить сообщения на предыдущей **SpoolerNotify** звонок, условия был изменен после и сообщения не должна быть повторно.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-131">Although the transport provider requested that the MAPI spooler resubmit the message on a previous **SpoolerNotify** call, conditions have since changed, and the message should not be resent.</span></span> <span data-ttu-id="9e7e7-132">Диспетчер очереди MAPI будут поступать какой-либо другой обработки.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-132">The MAPI spooler will go on to handle something else.</span></span> 
    
<span data-ttu-id="9e7e7-133">MAPI_E_NETWORK_ERROR</span><span class="sxs-lookup"><span data-stu-id="9e7e7-133">MAPI_E_NETWORK_ERROR</span></span> 
  
> <span data-ttu-id="9e7e7-134">Ошибка сети запрещено успешного завершения операции.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-134">A network error prevented successful completion of the operation.</span></span> <span data-ttu-id="9e7e7-135">Параметр _lpulReturnParm_ должен иметь значение количество секунд, по истечении которого диспетчер очереди MAPI повторно предоставляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-135">The  _lpulReturnParm_ parameter should be set to the number of seconds that will elapse before the MAPI spooler resubmits the message.</span></span> 
    
<span data-ttu-id="9e7e7-136">MAPI_E_NOT_ME</span><span class="sxs-lookup"><span data-stu-id="9e7e7-136">MAPI_E_NOT_ME</span></span> 
  
> <span data-ttu-id="9e7e7-137">Поставщика транспорта не удается обработать это сообщение.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-137">The transport provider cannot handle this message.</span></span> <span data-ttu-id="9e7e7-138">Диспетчер очереди MAPI должны пытаться поиск другого поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-138">The MAPI spooler should try to find another transport provider for it.</span></span> <span data-ttu-id="9e7e7-139">Для указания, что обработка не произошло и диспетчер очереди MAPI не должны вызывать **EndMessage**поставщика следует использовать это возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-139">A provider should use this return value to indicate that no processing occurred and that the MAPI spooler should not call **EndMessage**.</span></span>
    
<span data-ttu-id="9e7e7-140">MAPI_E_WAIT</span><span class="sxs-lookup"><span data-stu-id="9e7e7-140">MAPI_E_WAIT</span></span> 
  
> <span data-ttu-id="9e7e7-141">Временные неполадки предотвращает поставщика транспорта обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-141">A temporary problem prevents the transport provider from handling the message.</span></span> <span data-ttu-id="9e7e7-142">Параметр _lpulReturnParm_ должен иметь значение количество секунд, по истечении которого диспетчер очереди MAPI повторно предоставляет сообщение.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-142">The  _lpulReturnParm_ parameter should be set to the number of seconds that will elapse before the MAPI spooler resubmits the message.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9e7e7-143">Примечания</span><span class="sxs-lookup"><span data-stu-id="9e7e7-143">Remarks</span></span>

<span data-ttu-id="9e7e7-144">Диспетчер очереди MAPI вызывает метод **IXPLogon::SubmitMessage** при получении сообщения для поставщика транспорта для доставки.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-144">The MAPI spooler calls the **IXPLogon::SubmitMessage** method when it has a message for the transport provider to deliver.</span></span> <span data-ttu-id="9e7e7-145">Сообщение передается поставщика транспорта с помощью параметра _lpMessage_ .</span><span class="sxs-lookup"><span data-stu-id="9e7e7-145">The message is passed to the transport provider by using the  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="9e7e7-146">Если поставщик готов принять сообщение, он возвращает значение ссылки с помощью параметра _lpulMsgRef_ процесс переданный объект и вернуть соответствующее значение (обычно это значение S_OK).</span><span class="sxs-lookup"><span data-stu-id="9e7e7-146">If the provider is ready to accept the message, it should return a reference value by using the  _lpulMsgRef_ parameter, process the passed object, and return the appropriate value (usually S_OK).</span></span> <span data-ttu-id="9e7e7-147">Если поставщик не готовы обрабатывать передачу, он должен возвращать значение ошибки, и при необходимости другой MAPI возврат значения в _lpulReturnParm_ , чтобы указать время ожидания очереди MAPI перед повторной отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-147">If the provider is not prepared to handle the transfer, it should return an error value and, optionally, another MAPI return value in  _lpulReturnParm_ to indicate how long the MAPI spooler should wait before resubmitting the message.</span></span> 
  
<span data-ttu-id="9e7e7-148">Реализация поставщика транспорта этого метода можно выполнить следующие:</span><span class="sxs-lookup"><span data-stu-id="9e7e7-148">A transport provider's implementation of this method can do the following:</span></span>
  
- <span data-ttu-id="9e7e7-149">Поместить сообщение в внутреннюю очередь ожидания для передачи, возможно копирование сообщения на локальное хранилище и возврата.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-149">Put the message into an internal queue to wait for transmission, possibly copying the message to local storage, and return.</span></span>
    
- <span data-ttu-id="9e7e7-150">Попытка выполнения фактических передачи и вернуть по завершении передачи успешно или неудачно.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-150">Attempt to perform the actual transmission and return when the transmission completes, either successfully or unsuccessfully.</span></span>
    
- <span data-ttu-id="9e7e7-151">Определите необходимость отправки сообщения после проверки используемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-151">Determine whether to send the message after checking the resource involved.</span></span> <span data-ttu-id="9e7e7-152">В этом случае если ресурс свободен, поставщик может блокировки, Подготовка сообщение и отправить его.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-152">In this case, if the resource is free, the provider can lock the resource, prepare the message, and submit it.</span></span> <span data-ttu-id="9e7e7-153">Если ресурсом «занят», поставщик можно подготовить сообщения и отложить передачу позднее.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-153">If the resource is busy, the provider can prepare the message and defer sending to a later time.</span></span>
    
<span data-ttu-id="9e7e7-154">Предпочтительный способ передачи сообщений зависит от поставщика транспорта и ожидаемого числа процессов за для системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-154">The preferred technique for message transmission depends on the transport provider and the expected number of processes competing for system resources.</span></span> 
  
<span data-ttu-id="9e7e7-155">Во время звонка **SubmitMessage** поставщика транспорта управляет передачи данных сообщений из объекта сообщения.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-155">During a **SubmitMessage** call, the transport provider controls the transfer of message data from the message object.</span></span> <span data-ttu-id="9e7e7-156">Тем не менее поставщика транспорта следует назначить значение ссылки сообщения, к которой он возвращает указатель в _lpulMsgRef_перед передачей данных.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-156">However, the transport provider should assign a reference value to the message, to which it returns a pointer in  _lpulMsgRef_, before transferring data.</span></span> <span data-ttu-id="9e7e7-157">Так, так как в любой момент во время процесса диспетчер очереди MAPI можно вызвать метод [IXPLogon::TransportNotify](ixplogon-transportnotify.md) с флагом NOTIFY_CANCEL_MESSAGE выполнен сигнала поставщика, который должен освобождать все открытые объекты и остановки передачи сообщений.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-157">It does so because at any point during the process, the MAPI spooler can call the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method with the NOTIFY_CANCEL_MESSAGE flag set to signal the provider that it should release any open objects and stop message transfer.</span></span> 
  
<span data-ttu-id="9e7e7-158">Поставщика транспорта не следует отправлять все свойства nontransmittable сообщения.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-158">The transport provider should not send any nontransmittable properties of the message.</span></span> <span data-ttu-id="9e7e7-159">При обнаружении таких свойств, его следует перейти к обработки следующее свойство.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-159">When it finds such a property, it should go on to process the next property.</span></span> <span data-ttu-id="9e7e7-160">Поставщик должен постарайтесь не отображаются сведения о получателях MAPI_P1 как часть содержимого передаваемого сообщения; Поставщик следует использовать эти получателей сведения только для целей-адресов.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-160">The provider should make every effort not to display MAPI_P1 recipient information as part of the transmitted message content; the provider should use this recipient information only for addressing purposes.</span></span> <span data-ttu-id="9e7e7-161">MAPI_P1 получатели являются внутренними получателей, которые используются для повторной отправки сообщений. они должны не передаются.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-161">MAPI_P1 recipients are internally generated recipients that are used for resending messages; they should not be transmitted.</span></span> <span data-ttu-id="9e7e7-162">Используйте другие получателей для передачи сведения о получателях.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-162">Instead, use the other recipients for transmitting recipient information.</span></span> <span data-ttu-id="9e7e7-163">Упорядочение предназначен для разрешения Отправить получателей той же получателей таблицы как изначально указанным получателям.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-163">The purpose of this arrangement is to permit resend recipients to see the exact same recipient table as the original recipients.</span></span>
  
<span data-ttu-id="9e7e7-164">Во время звонка **SubmitMessage** диспетчер очереди MAPI обрабатывает методы для объектов, которые открыты во время передачи сообщения, и он обрабатывает все вложения.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-164">During a **SubmitMessage** call, the MAPI spooler processes methods for objects that are opened during the transfer of the message, and it processes any attachments.</span></span> <span data-ttu-id="9e7e7-165">В этом обработка может занять много времени.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-165">This processing can take a long time.</span></span> <span data-ttu-id="9e7e7-166">Поставщики транспорта можно вызвать метод [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) для очереди MAPI часто во время такой обработки для освобождения времени использования Процессора для других системных задач.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-166">Transport providers can call the [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) method for the MAPI spooler frequently during this processing to release CPU time for other system tasks.</span></span> 
  
<span data-ttu-id="9e7e7-167">В таблице получателей сообщения, диспетчер очереди MAPI изначально передается видны всех получателей сообщений.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-167">All message recipients are visible in the recipient table of the message that the MAPI spooler originally passed.</span></span> <span data-ttu-id="9e7e7-168">Поставщика транспорта должен обрабатывать только получателей, которые можно обрабатывать — на основании идентификатор записи и тип адреса — и, который еще не их свойство **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)), задайте значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-168">The transport provider should process only those recipients that it can handle — based on entry identifier, address type, or both — and that do not already have their **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property set to TRUE.</span></span> <span data-ttu-id="9e7e7-169">Если **PR_RESPONSIBILITY** уже имеет значение TRUE, другой поставщик транспорта обработал получателя.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-169">If **PR_RESPONSIBILITY** is already set to TRUE, another transport provider has handled that recipient.</span></span> <span data-ttu-id="9e7e7-170">По завершении обработки достаточно получателя для определения ли он может обрабатывать сообщения для этого получателя поставщика его следует задать свойство **PR_RESPONSIBILITY** этого получателя значение TRUE в переданного сообщения.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-170">When the provider completes sufficient processing of a recipient to determine whether it can handle messages for that recipient, it should set that recipient's **PR_RESPONSIBILITY** property to TRUE in the passed message.</span></span> <span data-ttu-id="9e7e7-171">Как правило поставщик Осуществляет это определение после завершения доставки сообщений.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-171">Usually, the provider makes this determination after message delivery is complete.</span></span> 
  
<span data-ttu-id="9e7e7-172">Как правило поставщика транспорта не возвращает из вызова **SubmitMessage** до завершения переноса данных сообщений.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-172">Typically, the transport provider does not return from a **SubmitMessage** call until it completes the transfer of message data.</span></span> <span data-ttu-id="9e7e7-173">Если сообщение об ошибке не возвращается, вызов метода [IXPLogon::EndMessage](ixplogon-endmessage.md) представляет собой следующий вызов из очереди MAPI, к поставщику.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-173">If no error is returned, the next call from the MAPI spooler to the provider is a call to the [IXPLogon::EndMessage](ixplogon-endmessage.md) method.</span></span> 
  
<span data-ttu-id="9e7e7-174">Если **SubmitMessage** возвращает ошибку, диспетчер очереди MAPI освобождает сообщение в процессе без сохранения изменений.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-174">If **SubmitMessage** returns an error, the MAPI spooler releases the message in process without saving changes.</span></span> <span data-ttu-id="9e7e7-175">Если поставщика транспорта требуется для сохранения изменений сообщение, необходимо вызвать метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) в окне сообщения до возвращения.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-175">If the transport provider requires message changes to be saved, it must call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the message before returning.</span></span> 
  
<span data-ttu-id="9e7e7-176">В случае ошибки, которые возникают из-за проблем с транспорта диспетчер очереди MAPI сохраняет сообщения, но задержку повторной отправки сообщений для поставщика транспорта, на основе значения, возвращаемого в _lpulReturnParm_.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-176">In case of errors that occur because of transport problems, the MAPI spooler retains the message, but it delays resubmitting the message to the transport provider based on the value returned in  _lpulReturnParm_.</span></span> <span data-ttu-id="9e7e7-177">Поставщика транспорта необходимо заполнить это значение, если ее значение, возвращаемое **SubmitMessage** MAPI_E_WAIT или MAPI_E_NETWORK_ERROR.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-177">The transport provider must fill in that value if its return value from **SubmitMessage** is MAPI_E_WAIT or MAPI_E_NETWORK_ERROR.</span></span> <span data-ttu-id="9e7e7-178">При возникновении серьезной ошибки, поставщика транспорта необходимо вызвать метод [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) с флагом NOTIFY_CRITICAL_ERROR.</span><span class="sxs-lookup"><span data-stu-id="9e7e7-178">If a severe error condition occurs, the transport provider must call the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_CRITICAL_ERROR flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9e7e7-179">См. также</span><span class="sxs-lookup"><span data-stu-id="9e7e7-179">See also</span></span>



[<span data-ttu-id="9e7e7-180">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="9e7e7-180">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="9e7e7-181">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="9e7e7-181">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="9e7e7-182">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="9e7e7-182">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="9e7e7-183">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="9e7e7-183">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md)
  
[<span data-ttu-id="9e7e7-184">IXPLogon::TransportNotify</span><span class="sxs-lookup"><span data-stu-id="9e7e7-184">IXPLogon::TransportNotify</span></span>](ixplogon-transportnotify.md)
  
[<span data-ttu-id="9e7e7-185">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9e7e7-185">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

