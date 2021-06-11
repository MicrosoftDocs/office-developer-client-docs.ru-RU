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
ms.openlocfilehash: ae124cb94cff5be0a655386d31f1bf2c82f66a85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423323"
---
# <a name="ixplogonsubmitmessage"></a><span data-ttu-id="60e61-103">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="60e61-103">IXPLogon::SubmitMessage</span></span>

  
  
<span data-ttu-id="60e61-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60e61-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60e61-105">Указывает, что у пулера MAPI есть сообщение для поставщика транспорта для доставки.</span><span class="sxs-lookup"><span data-stu-id="60e61-105">Indicates that the MAPI spooler has a message for the transport provider to deliver.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef,
  ULONG FAR * lpulReturnParm
);
```

## <a name="parameters"></a><span data-ttu-id="60e61-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="60e61-106">Parameters</span></span>

 <span data-ttu-id="60e61-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="60e61-107">_ulFlags_</span></span>
  
> <span data-ttu-id="60e61-108">[in] Битмашка флагов, которые контролируют отправку сообщения.</span><span class="sxs-lookup"><span data-stu-id="60e61-108">[in] A bitmask of flags that controls how the message is submitted.</span></span> <span data-ttu-id="60e61-109">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="60e61-109">The following flag can be set:</span></span>
    
<span data-ttu-id="60e61-110">BEGIN_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="60e61-110">BEGIN_DEFERRED</span></span> 
  
> <span data-ttu-id="60e61-111">Spooler MAPI вызывает поставщика транспорта с ранее отложенным сообщением.</span><span class="sxs-lookup"><span data-stu-id="60e61-111">The MAPI spooler is calling a transport provider with a message that was previously deferred.</span></span> <span data-ttu-id="60e61-112">Идентификатор записи сообщения такой же, как и при отложении.</span><span class="sxs-lookup"><span data-stu-id="60e61-112">The entry identifier of the message is the same as when it was deferred.</span></span> <span data-ttu-id="60e61-113">Сообщение было отложено, передав идентификатор записи обратно в шпалер MAPI с помощью метода [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) с флагом NOTIFY_SENTDEFERRED.</span><span class="sxs-lookup"><span data-stu-id="60e61-113">The message was deferred by passing its entry identifier back to the MAPI spooler by using the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_SENTDEFERRED flag.</span></span> 
    
 <span data-ttu-id="60e61-114">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="60e61-114">_lpMessage_</span></span>
  
> <span data-ttu-id="60e61-115">[in] Указатель на объект сообщения (представляющий сообщение для доставки), который имеет разрешение на чтение и записи, которое поставщик транспорта использует для доступа к этому сообщению и управления им.</span><span class="sxs-lookup"><span data-stu-id="60e61-115">[in] A pointer to a message object (representing the message to deliver) that has read/write permission, which the transport provider uses to access and manipulate that message.</span></span> <span data-ttu-id="60e61-116">Этот объект остается действительным до тех пор, пока поставщик транспорта не вернется после последующего вызова к [методу IXPLogon::EndMessage.](ixplogon-endmessage.md)</span><span class="sxs-lookup"><span data-stu-id="60e61-116">This object remains valid until after the transport provider returns from a subsequent call to the [IXPLogon::EndMessage](ixplogon-endmessage.md) method.</span></span> 
    
 <span data-ttu-id="60e61-117">_lpulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="60e61-117">_lpulMsgRef_</span></span>
  
> <span data-ttu-id="60e61-118">[вышел] Указатель на переменную, в которой поставщик транспорта возвращает назначенное этому сообщению значение.</span><span class="sxs-lookup"><span data-stu-id="60e61-118">[out] A pointer to a variable in which the transport provider returns the reference value it assigned to this message.</span></span> <span data-ttu-id="60e61-119">Шпалер MAPI передает это эталонное значение в последующих вызовах для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="60e61-119">The MAPI spooler passes this reference value in subsequent calls for this message.</span></span> <span data-ttu-id="60e61-120">Spooler MAPI инициализирует значение до 0, прежде чем возвращать его поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="60e61-120">The MAPI spooler initializes the value to 0 before returning it to the transport provider.</span></span>
    
 <span data-ttu-id="60e61-121">_lpulReturnParm_</span><span class="sxs-lookup"><span data-stu-id="60e61-121">_lpulReturnParm_</span></span>
  
> <span data-ttu-id="60e61-122">[вышел] Указатель на переменную, соответствующую значению MAPI_E_WAIT или MAPI_E_NETWORK_ERROR, возвращаемой **SubmitMessage.**</span><span class="sxs-lookup"><span data-stu-id="60e61-122">[out] A pointer to a variable that corresponds to the MAPI_E_WAIT or MAPI_E_NETWORK_ERROR error value returned by **SubmitMessage**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="60e61-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60e61-123">Return value</span></span>

<span data-ttu-id="60e61-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="60e61-124">S_OK</span></span> 
  
> <span data-ttu-id="60e61-125">Вызов удался и возвращает ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="60e61-125">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="60e61-126">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="60e61-126">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="60e61-127">Поставщик транспорта не может обрабатывать сообщение, так как выполняет другую операцию.</span><span class="sxs-lookup"><span data-stu-id="60e61-127">The transport provider cannot handle the message, because it is performing another operation.</span></span> <span data-ttu-id="60e61-128">Поставщик должен использовать это возвращаемая величина, чтобы указать, что обработка не была совершена и что пульпер MAPI не должен вызывать **EndMessage.**</span><span class="sxs-lookup"><span data-stu-id="60e61-128">A provider should use this return value to indicate that no processing occurred and that the MAPI spooler should not call **EndMessage**.</span></span> <span data-ttu-id="60e61-129">Spooler MAPI снова попробует **вызов SubmitMessage** позже.</span><span class="sxs-lookup"><span data-stu-id="60e61-129">The MAPI spooler will try the **SubmitMessage** call again later.</span></span> 
    
<span data-ttu-id="60e61-130">MAPI_E_CANCEL</span><span class="sxs-lookup"><span data-stu-id="60e61-130">MAPI_E_CANCEL</span></span> 
  
> <span data-ttu-id="60e61-131">Несмотря на то, что поставщик транспорта запросил повторное повторное сообщение от пулера MAPI на предыдущем вызове **SpoolerNotify,** условия с тех пор изменились, и сообщение не должно быть обижным.</span><span class="sxs-lookup"><span data-stu-id="60e61-131">Although the transport provider requested that the MAPI spooler resubmit the message on a previous **SpoolerNotify** call, conditions have since changed, and the message should not be resent.</span></span> <span data-ttu-id="60e61-132">Шпалер MAPI будет обрабатывать что-то другое.</span><span class="sxs-lookup"><span data-stu-id="60e61-132">The MAPI spooler will go on to handle something else.</span></span> 
    
<span data-ttu-id="60e61-133">MAPI_E_NETWORK_ERROR</span><span class="sxs-lookup"><span data-stu-id="60e61-133">MAPI_E_NETWORK_ERROR</span></span> 
  
> <span data-ttu-id="60e61-134">Ошибка сети помешала успешному завершению операции.</span><span class="sxs-lookup"><span data-stu-id="60e61-134">A network error prevented successful completion of the operation.</span></span> <span data-ttu-id="60e61-135">Параметр  _lpulReturnParm_ должен быть задан в количестве секунд, которое пройдет до повторного повторного сообщения spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="60e61-135">The  _lpulReturnParm_ parameter should be set to the number of seconds that will elapse before the MAPI spooler resubmits the message.</span></span> 
    
<span data-ttu-id="60e61-136">MAPI_E_NOT_ME</span><span class="sxs-lookup"><span data-stu-id="60e61-136">MAPI_E_NOT_ME</span></span> 
  
> <span data-ttu-id="60e61-137">Поставщик транспорта не может обрабатывать это сообщение.</span><span class="sxs-lookup"><span data-stu-id="60e61-137">The transport provider cannot handle this message.</span></span> <span data-ttu-id="60e61-138">Spooler MAPI должен попытаться найти другого поставщика транспорта для него.</span><span class="sxs-lookup"><span data-stu-id="60e61-138">The MAPI spooler should try to find another transport provider for it.</span></span> <span data-ttu-id="60e61-139">Поставщик должен использовать это возвращаемая величина, чтобы указать, что обработка не была совершена и что пульпер MAPI не должен вызывать **EndMessage.**</span><span class="sxs-lookup"><span data-stu-id="60e61-139">A provider should use this return value to indicate that no processing occurred and that the MAPI spooler should not call **EndMessage**.</span></span>
    
<span data-ttu-id="60e61-140">MAPI_E_WAIT</span><span class="sxs-lookup"><span data-stu-id="60e61-140">MAPI_E_WAIT</span></span> 
  
> <span data-ttu-id="60e61-141">Временная проблема не позволяет поставщику транспорта обрабатывать сообщение.</span><span class="sxs-lookup"><span data-stu-id="60e61-141">A temporary problem prevents the transport provider from handling the message.</span></span> <span data-ttu-id="60e61-142">Параметр  _lpulReturnParm_ должен быть задан в количестве секунд, которое пройдет до повторного повторного сообщения spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="60e61-142">The  _lpulReturnParm_ parameter should be set to the number of seconds that will elapse before the MAPI spooler resubmits the message.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="60e61-143">Примечания</span><span class="sxs-lookup"><span data-stu-id="60e61-143">Remarks</span></span>

<span data-ttu-id="60e61-144">Spooler MAPI вызывает **метод IXPLogon::SubmitMessage,** когда у него есть сообщение для поставщика транспорта для доставки.</span><span class="sxs-lookup"><span data-stu-id="60e61-144">The MAPI spooler calls the **IXPLogon::SubmitMessage** method when it has a message for the transport provider to deliver.</span></span> <span data-ttu-id="60e61-145">Сообщение передается поставщику транспорта с помощью _параметра lpMessage._</span><span class="sxs-lookup"><span data-stu-id="60e61-145">The message is passed to the transport provider by using the  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="60e61-146">Если поставщик готов принять сообщение, он должен вернуть эталонное значение с помощью параметра  _lpulMsgRef,_ обработать переданный объект и вернуть соответствующее значение (как правило, S_OK).</span><span class="sxs-lookup"><span data-stu-id="60e61-146">If the provider is ready to accept the message, it should return a reference value by using the  _lpulMsgRef_ parameter, process the passed object, and return the appropriate value (usually S_OK).</span></span> <span data-ttu-id="60e61-147">Если поставщик не готов обрабатывать передачу, он должен вернуть значение ошибки и, необязательно, другое значение возврата MAPI в  _lpulReturnParm,_ чтобы указать, как долго spooler MAPI должен ждать перед повторной передачей сообщения.</span><span class="sxs-lookup"><span data-stu-id="60e61-147">If the provider is not prepared to handle the transfer, it should return an error value and, optionally, another MAPI return value in  _lpulReturnParm_ to indicate how long the MAPI spooler should wait before resubmitting the message.</span></span> 
  
<span data-ttu-id="60e61-148">Реализация этого метода поставщиком транспорта может сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="60e61-148">A transport provider's implementation of this method can do the following:</span></span>
  
- <span data-ttu-id="60e61-149">Поместите сообщение во внутреннюю очередь, чтобы дождаться передачи, возможно, скопируйте сообщение в локальное хранилище и вернись.</span><span class="sxs-lookup"><span data-stu-id="60e61-149">Put the message into an internal queue to wait for transmission, possibly copying the message to local storage, and return.</span></span>
    
- <span data-ttu-id="60e61-150">Попытка выполнить фактическую передачу и вернуться после успешного или неудачного завершения передачи.</span><span class="sxs-lookup"><span data-stu-id="60e61-150">Attempt to perform the actual transmission and return when the transmission completes, either successfully or unsuccessfully.</span></span>
    
- <span data-ttu-id="60e61-151">Определите, отправлять ли сообщение после проверки задействованного ресурса.</span><span class="sxs-lookup"><span data-stu-id="60e61-151">Determine whether to send the message after checking the resource involved.</span></span> <span data-ttu-id="60e61-152">В этом случае, если ресурс бесплатный, поставщик может заблокировать ресурс, подготовить сообщение и отправить его.</span><span class="sxs-lookup"><span data-stu-id="60e61-152">In this case, if the resource is free, the provider can lock the resource, prepare the message, and submit it.</span></span> <span data-ttu-id="60e61-153">Если ресурс занят, поставщик может подготовить сообщение и отложить отправку на более позднее время.</span><span class="sxs-lookup"><span data-stu-id="60e61-153">If the resource is busy, the provider can prepare the message and defer sending to a later time.</span></span>
    
<span data-ttu-id="60e61-154">Предпочтительный метод передачи сообщений зависит от поставщика транспорта и ожидаемого количества процессов, конкурирующих за системные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="60e61-154">The preferred technique for message transmission depends on the transport provider and the expected number of processes competing for system resources.</span></span> 
  
<span data-ttu-id="60e61-155">Во время **вызова SubmitMessage** поставщик транспорта контролирует передачу данных сообщений из объекта сообщения.</span><span class="sxs-lookup"><span data-stu-id="60e61-155">During a **SubmitMessage** call, the transport provider controls the transfer of message data from the message object.</span></span> <span data-ttu-id="60e61-156">Однако перед передачей данных поставщик транспорта должен назначить ссылку на сообщение, которому возвращает указатель _в lpulMsgRef._</span><span class="sxs-lookup"><span data-stu-id="60e61-156">However, the transport provider should assign a reference value to the message, to which it returns a pointer in  _lpulMsgRef_, before transferring data.</span></span> <span data-ttu-id="60e61-157">Это делается потому, что в любой момент во время процесса шпалер MAPI может вызвать метод [IXPLogon::TransportNotify](ixplogon-transportnotify.md) с набором флага NOTIFY_CANCEL_MESSAGE, чтобы сигнализировать поставщику о том, что он должен освободить все открытые объекты и остановить передачу сообщений.</span><span class="sxs-lookup"><span data-stu-id="60e61-157">It does so because at any point during the process, the MAPI spooler can call the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method with the NOTIFY_CANCEL_MESSAGE flag set to signal the provider that it should release any open objects and stop message transfer.</span></span> 
  
<span data-ttu-id="60e61-158">Поставщик транспорта не должен отправлять любые неограничимые свойства сообщения.</span><span class="sxs-lookup"><span data-stu-id="60e61-158">The transport provider should not send any nontransmittable properties of the message.</span></span> <span data-ttu-id="60e61-159">Когда оно находит такое свойство, оно должно перейти к обработке следующего свойства.</span><span class="sxs-lookup"><span data-stu-id="60e61-159">When it finds such a property, it should go on to process the next property.</span></span> <span data-ttu-id="60e61-160">Поставщик должен приложить все усилия, чтобы не отображать MAPI_P1 получателей в составе передаваемых сообщений; поставщик должен использовать эти сведения получателя только для решения задач.</span><span class="sxs-lookup"><span data-stu-id="60e61-160">The provider should make every effort not to display MAPI_P1 recipient information as part of the transmitted message content; the provider should use this recipient information only for addressing purposes.</span></span> <span data-ttu-id="60e61-161">MAPI_P1 получатели — это внутренне созданные получатели, которые используются для повторного использования сообщений; они не должны передаваться.</span><span class="sxs-lookup"><span data-stu-id="60e61-161">MAPI_P1 recipients are internally generated recipients that are used for resending messages; they should not be transmitted.</span></span> <span data-ttu-id="60e61-162">Вместо этого используйте другие получатели для передачи сведений о получателях.</span><span class="sxs-lookup"><span data-stu-id="60e61-162">Instead, use the other recipients for transmitting recipient information.</span></span> <span data-ttu-id="60e61-163">Цель этого соглашения состоит в том, чтобы разрешить получателям повторной выдачи видеть ту же таблицу получателей, что и исходные получатели.</span><span class="sxs-lookup"><span data-stu-id="60e61-163">The purpose of this arrangement is to permit resend recipients to see the exact same recipient table as the original recipients.</span></span>
  
<span data-ttu-id="60e61-164">Во время **вызова SubmitMessage** пулер MAPI обрабатывает методы для объектов, которые открываются во время передачи сообщения, и обрабатывает любые вложения.</span><span class="sxs-lookup"><span data-stu-id="60e61-164">During a **SubmitMessage** call, the MAPI spooler processes methods for objects that are opened during the transfer of the message, and it processes any attachments.</span></span> <span data-ttu-id="60e61-165">Эта обработка может занять много времени.</span><span class="sxs-lookup"><span data-stu-id="60e61-165">This processing can take a long time.</span></span> <span data-ttu-id="60e61-166">Поставщики транспорта могут часто вызывать [метод IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) для шпалеров MAPI во время этой обработки, чтобы освободить время ЦП для других системных задач.</span><span class="sxs-lookup"><span data-stu-id="60e61-166">Transport providers can call the [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) method for the MAPI spooler frequently during this processing to release CPU time for other system tasks.</span></span> 
  
<span data-ttu-id="60e61-167">Все получатели сообщений видны в таблице получателей сообщения, которое изначально было передано спулером MAPI.</span><span class="sxs-lookup"><span data-stu-id="60e61-167">All message recipients are visible in the recipient table of the message that the MAPI spooler originally passed.</span></span> <span data-ttu-id="60e61-168">Поставщик транспорта должен обрабатывать только те получатели, с которые он может обращаться , основываясь на идентификаторе записи, типе адреса или обоих, и у них уже нет свойств **PR_RESPONSIBILITY** [(PidTagResponsibility),](pidtagresponsibility-canonical-property.md)задаваемого true.</span><span class="sxs-lookup"><span data-stu-id="60e61-168">The transport provider should process only those recipients that it can handle — based on entry identifier, address type, or both — and that do not already have their **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property set to TRUE.</span></span> <span data-ttu-id="60e61-169">Если **PR_RESPONSIBILITY** уже установлено true, другой поставщик транспорта обсправил этого получателя.</span><span class="sxs-lookup"><span data-stu-id="60e61-169">If **PR_RESPONSIBILITY** is already set to TRUE, another transport provider has handled that recipient.</span></span> <span data-ttu-id="60e61-170">Когда поставщик завершает достаточную обработку получателя, чтобы определить, может ли он обрабатывать сообщения  для этого получателя, он должен задать свойство PR_RESPONSIBILITY получателя true в переданных сообщениях.</span><span class="sxs-lookup"><span data-stu-id="60e61-170">When the provider completes sufficient processing of a recipient to determine whether it can handle messages for that recipient, it should set that recipient's **PR_RESPONSIBILITY** property to TRUE in the passed message.</span></span> <span data-ttu-id="60e61-171">Обычно поставщик принимает это решение после завершения доставки сообщения.</span><span class="sxs-lookup"><span data-stu-id="60e61-171">Usually, the provider makes this determination after message delivery is complete.</span></span> 
  
<span data-ttu-id="60e61-172">Обычно поставщик транспорта не возвращается с вызова **SubmitMessage** до завершения передачи данных сообщений.</span><span class="sxs-lookup"><span data-stu-id="60e61-172">Typically, the transport provider does not return from a **SubmitMessage** call until it completes the transfer of message data.</span></span> <span data-ttu-id="60e61-173">Если ошибка не возвращается, следующим вызовом от пулера MAPI к поставщику является вызов метода [IXPLogon::EndMessage.](ixplogon-endmessage.md)</span><span class="sxs-lookup"><span data-stu-id="60e61-173">If no error is returned, the next call from the MAPI spooler to the provider is a call to the [IXPLogon::EndMessage](ixplogon-endmessage.md) method.</span></span> 
  
<span data-ttu-id="60e61-174">Если **SubmitMessage** возвращает ошибку, шпалер MAPI освобождает сообщение в процессе без сохранения изменений.</span><span class="sxs-lookup"><span data-stu-id="60e61-174">If **SubmitMessage** returns an error, the MAPI spooler releases the message in process without saving changes.</span></span> <span data-ttu-id="60e61-175">Если поставщику транспорта требуется сохранить изменения сообщений, перед возвращением необходимо вызвать метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) в сообщении.</span><span class="sxs-lookup"><span data-stu-id="60e61-175">If the transport provider requires message changes to be saved, it must call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the message before returning.</span></span> 
  
<span data-ttu-id="60e61-176">В случае ошибок, которые возникают из-за транспортных проблем, шпалер MAPI сохраняет сообщение, но задерживает повторное сообщение поставщику транспорта на основе значения, возвращенного в  _lpulReturnParm_.</span><span class="sxs-lookup"><span data-stu-id="60e61-176">In case of errors that occur because of transport problems, the MAPI spooler retains the message, but it delays resubmitting the message to the transport provider based on the value returned in  _lpulReturnParm_.</span></span> <span data-ttu-id="60e61-177">Поставщик транспорта должен заполнить это значение, если его возвращаемая стоимость **из SubmitMessage** MAPI_E_WAIT или MAPI_E_NETWORK_ERROR.</span><span class="sxs-lookup"><span data-stu-id="60e61-177">The transport provider must fill in that value if its return value from **SubmitMessage** is MAPI_E_WAIT or MAPI_E_NETWORK_ERROR.</span></span> <span data-ttu-id="60e61-178">Если возникает серьезное состояние ошибки, поставщик транспорта должен вызвать [метод IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) с NOTIFY_CRITICAL_ERROR флагом.</span><span class="sxs-lookup"><span data-stu-id="60e61-178">If a severe error condition occurs, the transport provider must call the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_CRITICAL_ERROR flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="60e61-179">См. также</span><span class="sxs-lookup"><span data-stu-id="60e61-179">See also</span></span>



[<span data-ttu-id="60e61-180">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="60e61-180">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="60e61-181">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="60e61-181">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="60e61-182">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="60e61-182">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="60e61-183">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="60e61-183">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md)
  
[<span data-ttu-id="60e61-184">IXPLogon::TransportNotify</span><span class="sxs-lookup"><span data-stu-id="60e61-184">IXPLogon::TransportNotify</span></span>](ixplogon-transportnotify.md)
  
[<span data-ttu-id="60e61-185">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="60e61-185">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

