---
title: Иксплогонсубмитмессаже
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351592"
---
# <a name="ixplogonsubmitmessage"></a><span data-ttu-id="85112-103">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="85112-103">IXPLogon::SubmitMessage</span></span>

  
  
<span data-ttu-id="85112-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85112-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85112-105">Указывает на то, что диспетчер очереди MAPI имеет сообщение, которое будет доставлено поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="85112-105">Indicates that the MAPI spooler has a message for the transport provider to deliver.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef,
  ULONG FAR * lpulReturnParm
);
```

## <a name="parameters"></a><span data-ttu-id="85112-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="85112-106">Parameters</span></span>

 <span data-ttu-id="85112-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="85112-107">_ulFlags_</span></span>
  
> <span data-ttu-id="85112-108">возврата Битовая маска флагов, определяющих способ отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="85112-108">[in] A bitmask of flags that controls how the message is submitted.</span></span> <span data-ttu-id="85112-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="85112-109">The following flag can be set:</span></span>
    
<span data-ttu-id="85112-110">БЕГИН_ДЕФЕРРЕД</span><span class="sxs-lookup"><span data-stu-id="85112-110">BEGIN_DEFERRED</span></span> 
  
> <span data-ttu-id="85112-111">Диспетчер очереди MAPI вызывает поставщик транспорта с сообщением, которое ранее было отложено.</span><span class="sxs-lookup"><span data-stu-id="85112-111">The MAPI spooler is calling a transport provider with a message that was previously deferred.</span></span> <span data-ttu-id="85112-112">Идентификатор записи сообщения такой же, как и при его отложенной отправку.</span><span class="sxs-lookup"><span data-stu-id="85112-112">The entry identifier of the message is the same as when it was deferred.</span></span> <span data-ttu-id="85112-113">Сообщение было отложено путем передачи его идентификатора записи обратно в буфер обмена MAPI с помощью метода [имаписуппорт:: спулернотифи](imapisupport-spoolernotify.md) с флагом нотифи_сентдеферред.</span><span class="sxs-lookup"><span data-stu-id="85112-113">The message was deferred by passing its entry identifier back to the MAPI spooler by using the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_SENTDEFERRED flag.</span></span> 
    
 <span data-ttu-id="85112-114">_Лпмессаже_</span><span class="sxs-lookup"><span data-stu-id="85112-114">_lpMessage_</span></span>
  
> <span data-ttu-id="85112-115">возврата Указатель на объект Message (представляющий сообщение для доставки), у которого есть разрешение на чтение и запись, которое поставщик транспорта использует для доступа к этому сообщению и управления им.</span><span class="sxs-lookup"><span data-stu-id="85112-115">[in] A pointer to a message object (representing the message to deliver) that has read/write permission, which the transport provider uses to access and manipulate that message.</span></span> <span data-ttu-id="85112-116">Этот объект остается действительным до тех пор, пока поставщик транспорта не вернется из последующего вызова метода [иксплогон:: ендмессаже](ixplogon-endmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="85112-116">This object remains valid until after the transport provider returns from a subsequent call to the [IXPLogon::EndMessage](ixplogon-endmessage.md) method.</span></span> 
    
 <span data-ttu-id="85112-117">_Лпулмсгреф_</span><span class="sxs-lookup"><span data-stu-id="85112-117">_lpulMsgRef_</span></span>
  
> <span data-ttu-id="85112-118">вышли Указатель на переменную, в которой поставщик транспорта возвращает значение ссылки, назначенное этому сообщению.</span><span class="sxs-lookup"><span data-stu-id="85112-118">[out] A pointer to a variable in which the transport provider returns the reference value it assigned to this message.</span></span> <span data-ttu-id="85112-119">Диспетчер очереди MAPI передает это значение ссылки в последующих вызовах этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="85112-119">The MAPI spooler passes this reference value in subsequent calls for this message.</span></span> <span data-ttu-id="85112-120">Диспетчер очереди MAPI Инициализирует значение равным 0 перед его возвратом поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="85112-120">The MAPI spooler initializes the value to 0 before returning it to the transport provider.</span></span>
    
 <span data-ttu-id="85112-121">_Лпулретурнпарм_</span><span class="sxs-lookup"><span data-stu-id="85112-121">_lpulReturnParm_</span></span>
  
> <span data-ttu-id="85112-122">вышли Указатель на переменную, которая соответствует значению ошибки МАПИ_Е_ВАИТ или МАПИ_Е_НЕТВОРК_ЕРРОР, возвращенному **субмитмессаже**.</span><span class="sxs-lookup"><span data-stu-id="85112-122">[out] A pointer to a variable that corresponds to the MAPI_E_WAIT or MAPI_E_NETWORK_ERROR error value returned by **SubmitMessage**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="85112-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85112-123">Return value</span></span>

<span data-ttu-id="85112-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="85112-124">S_OK</span></span> 
  
> <span data-ttu-id="85112-125">Вызов выполнен успешно и вернул ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="85112-125">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="85112-126">МАПИ_Е_БУСИ</span><span class="sxs-lookup"><span data-stu-id="85112-126">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="85112-127">Поставщик транспорта не может обработать сообщение, так как он выполняет другую операцию.</span><span class="sxs-lookup"><span data-stu-id="85112-127">The transport provider cannot handle the message, because it is performing another operation.</span></span> <span data-ttu-id="85112-128">Поставщик должен использовать это возвращаемое значение, чтобы показать, что обработка не выполнялась, и что диспетчер очереди MAPI не должен вызывать **ендмессаже**.</span><span class="sxs-lookup"><span data-stu-id="85112-128">A provider should use this return value to indicate that no processing occurred and that the MAPI spooler should not call **EndMessage**.</span></span> <span data-ttu-id="85112-129">Диспетчер очереди MAPI повторит вызов **субмитмессаже** позже.</span><span class="sxs-lookup"><span data-stu-id="85112-129">The MAPI spooler will try the **SubmitMessage** call again later.</span></span> 
    
<span data-ttu-id="85112-130">МАПИ_Е_КАНЦЕЛ</span><span class="sxs-lookup"><span data-stu-id="85112-130">MAPI_E_CANCEL</span></span> 
  
> <span data-ttu-id="85112-131">Хотя поставщик транспорта запросил, чтобы диспетчер очереди MAPI повторно отправил сообщение в предыдущий вызов **спулернотифи** , условия изменились, и сообщение не должно повторно использоваться.</span><span class="sxs-lookup"><span data-stu-id="85112-131">Although the transport provider requested that the MAPI spooler resubmit the message on a previous **SpoolerNotify** call, conditions have since changed, and the message should not be resent.</span></span> <span data-ttu-id="85112-132">Диспетчер очереди MAPI перейдет на страницу, чтобы обработать что-либо еще.</span><span class="sxs-lookup"><span data-stu-id="85112-132">The MAPI spooler will go on to handle something else.</span></span> 
    
<span data-ttu-id="85112-133">МАПИ_Е_НЕТВОРК_ЕРРОР</span><span class="sxs-lookup"><span data-stu-id="85112-133">MAPI_E_NETWORK_ERROR</span></span> 
  
> <span data-ttu-id="85112-134">Не удалось успешно завершить операцию из – за сетевой ошибки.</span><span class="sxs-lookup"><span data-stu-id="85112-134">A network error prevented successful completion of the operation.</span></span> <span data-ttu-id="85112-135">Для параметра _лпулретурнпарм_ необходимо указать время в секундах, по истечении которого диспетчер очереди MAPI повторно отправит сообщение.</span><span class="sxs-lookup"><span data-stu-id="85112-135">The  _lpulReturnParm_ parameter should be set to the number of seconds that will elapse before the MAPI spooler resubmits the message.</span></span> 
    
<span data-ttu-id="85112-136">МАПИ_Е_НОТ_МЕ</span><span class="sxs-lookup"><span data-stu-id="85112-136">MAPI_E_NOT_ME</span></span> 
  
> <span data-ttu-id="85112-137">Поставщик транспорта не может обработать это сообщение.</span><span class="sxs-lookup"><span data-stu-id="85112-137">The transport provider cannot handle this message.</span></span> <span data-ttu-id="85112-138">Диспетчер очереди MAPI должен попытаться найти другого поставщика транспорта для него.</span><span class="sxs-lookup"><span data-stu-id="85112-138">The MAPI spooler should try to find another transport provider for it.</span></span> <span data-ttu-id="85112-139">Поставщик должен использовать это возвращаемое значение, чтобы показать, что обработка не выполнялась, и что диспетчер очереди MAPI не должен вызывать **ендмессаже**.</span><span class="sxs-lookup"><span data-stu-id="85112-139">A provider should use this return value to indicate that no processing occurred and that the MAPI spooler should not call **EndMessage**.</span></span>
    
<span data-ttu-id="85112-140">МАПИ_Е_ВАИТ</span><span class="sxs-lookup"><span data-stu-id="85112-140">MAPI_E_WAIT</span></span> 
  
> <span data-ttu-id="85112-141">Временная проблема не позволяет поставщику транспорта обрабатывать сообщение.</span><span class="sxs-lookup"><span data-stu-id="85112-141">A temporary problem prevents the transport provider from handling the message.</span></span> <span data-ttu-id="85112-142">Для параметра _лпулретурнпарм_ необходимо указать время в секундах, по истечении которого диспетчер очереди MAPI повторно отправит сообщение.</span><span class="sxs-lookup"><span data-stu-id="85112-142">The  _lpulReturnParm_ parameter should be set to the number of seconds that will elapse before the MAPI spooler resubmits the message.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="85112-143">Примечания</span><span class="sxs-lookup"><span data-stu-id="85112-143">Remarks</span></span>

<span data-ttu-id="85112-144">Диспетчер очереди MAPI вызывает метод **иксплогон:: субмитмессаже** , когда у него есть сообщение для доставки поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="85112-144">The MAPI spooler calls the **IXPLogon::SubmitMessage** method when it has a message for the transport provider to deliver.</span></span> <span data-ttu-id="85112-145">Сообщение передается поставщику транспорта с помощью параметра _лпмессаже_ .</span><span class="sxs-lookup"><span data-stu-id="85112-145">The message is passed to the transport provider by using the  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="85112-146">Если поставщик готов принять сообщение, он должен возвратить значение ссылки с помощью параметра _лпулмсгреф_ , обработать переданный объект и возвратить соответствующее значение (обычно S_OK).</span><span class="sxs-lookup"><span data-stu-id="85112-146">If the provider is ready to accept the message, it should return a reference value by using the  _lpulMsgRef_ parameter, process the passed object, and return the appropriate value (usually S_OK).</span></span> <span data-ttu-id="85112-147">Если поставщик не готов к передаче, он должен возвратить значение ошибки и (необязательно) другое возвращаемое значение MAPI в _лпулретурнпарм_ , чтобы указать время ожидания перед повторной отправкой сообщения диспетчером MAPI.</span><span class="sxs-lookup"><span data-stu-id="85112-147">If the provider is not prepared to handle the transfer, it should return an error value and, optionally, another MAPI return value in  _lpulReturnParm_ to indicate how long the MAPI spooler should wait before resubmitting the message.</span></span> 
  
<span data-ttu-id="85112-148">Реализация этого метода поставщиком транспорта может выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="85112-148">A transport provider's implementation of this method can do the following:</span></span>
  
- <span data-ttu-id="85112-149">Помещение сообщения во внутреннюю очередь для ожидания передачи, возможно, копирования сообщения в локальное хранилище и возврата.</span><span class="sxs-lookup"><span data-stu-id="85112-149">Put the message into an internal queue to wait for transmission, possibly copying the message to local storage, and return.</span></span>
    
- <span data-ttu-id="85112-150">Попытка выполнить фактическую передачу и возврат, когда передача завершается успешно или неудачно.</span><span class="sxs-lookup"><span data-stu-id="85112-150">Attempt to perform the actual transmission and return when the transmission completes, either successfully or unsuccessfully.</span></span>
    
- <span data-ttu-id="85112-151">Определите, следует ли отправлять сообщение после проверки задействованного ресурса.</span><span class="sxs-lookup"><span data-stu-id="85112-151">Determine whether to send the message after checking the resource involved.</span></span> <span data-ttu-id="85112-152">В этом случае, если ресурс свободен, поставщик может заблокировать ресурс, подготовить сообщение и передать его.</span><span class="sxs-lookup"><span data-stu-id="85112-152">In this case, if the resource is free, the provider can lock the resource, prepare the message, and submit it.</span></span> <span data-ttu-id="85112-153">Если ресурс занят, поставщик может подготовить сообщение и отложить отправку на более позднее время.</span><span class="sxs-lookup"><span data-stu-id="85112-153">If the resource is busy, the provider can prepare the message and defer sending to a later time.</span></span>
    
<span data-ttu-id="85112-154">Предпочтительный способ передачи сообщений зависит от поставщика транспорта и от ожидаемого количества процессов, конкурирующих за системные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="85112-154">The preferred technique for message transmission depends on the transport provider and the expected number of processes competing for system resources.</span></span> 
  
<span data-ttu-id="85112-155">При вызове **субмитмессаже** поставщик транспорта управляет передачей данных сообщения из объекта Message.</span><span class="sxs-lookup"><span data-stu-id="85112-155">During a **SubmitMessage** call, the transport provider controls the transfer of message data from the message object.</span></span> <span data-ttu-id="85112-156">Тем не менее, поставщик транспорта должен назначить значение ссылки на сообщение, чтобы оно возвращало указатель в _лпулмсгреф_, перед передачей данных.</span><span class="sxs-lookup"><span data-stu-id="85112-156">However, the transport provider should assign a reference value to the message, to which it returns a pointer in  _lpulMsgRef_, before transferring data.</span></span> <span data-ttu-id="85112-157">Это происходит потому, что в любой момент процесса диспетчер очереди MAPI может вызвать метод [иксплогон:: транспортнотифи](ixplogon-transportnotify.md) с установленным ФЛАГом нотифи_канцел_мессаже, чтобы сообщить поставщику, что он должен освободить открытые объекты и остановить передачу сообщений.</span><span class="sxs-lookup"><span data-stu-id="85112-157">It does so because at any point during the process, the MAPI spooler can call the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method with the NOTIFY_CANCEL_MESSAGE flag set to signal the provider that it should release any open objects and stop message transfer.</span></span> 
  
<span data-ttu-id="85112-158">Поставщик транспорта не должен отправлять недопустимые свойства сообщения.</span><span class="sxs-lookup"><span data-stu-id="85112-158">The transport provider should not send any nontransmittable properties of the message.</span></span> <span data-ttu-id="85112-159">При обнаружении такого свойства он должен перейти к обработке следующего свойства.</span><span class="sxs-lookup"><span data-stu-id="85112-159">When it finds such a property, it should go on to process the next property.</span></span> <span data-ttu-id="85112-160">Поставщик должен сделать все усилия, чтобы не отображали сведения о получателе MAPI_P1 в переданном содержимом сообщения; Поставщик должен использовать эти сведения о получателе только для целей адресации.</span><span class="sxs-lookup"><span data-stu-id="85112-160">The provider should make every effort not to display MAPI_P1 recipient information as part of the transmitted message content; the provider should use this recipient information only for addressing purposes.</span></span> <span data-ttu-id="85112-161">Получатели MAPI_P1 — это внутренние получатели, которые используются для повторной отправки сообщений; они не должны передаваться.</span><span class="sxs-lookup"><span data-stu-id="85112-161">MAPI_P1 recipients are internally generated recipients that are used for resending messages; they should not be transmitted.</span></span> <span data-ttu-id="85112-162">Вместо этого используйте других получателей для передачи сведений о получателях.</span><span class="sxs-lookup"><span data-stu-id="85112-162">Instead, use the other recipients for transmitting recipient information.</span></span> <span data-ttu-id="85112-163">Цель этого размещения заключается в том, чтобы разрешить получателю повторной отправки просматривать точно ту же таблицу получателей, что и исходные получатели.</span><span class="sxs-lookup"><span data-stu-id="85112-163">The purpose of this arrangement is to permit resend recipients to see the exact same recipient table as the original recipients.</span></span>
  
<span data-ttu-id="85112-164">Во время вызова **субмитмессаже** Диспетчер очереди MAPI обрабатывает методы для объектов, которые открываются во время передачи сообщения, и обрабатывает все вложения.</span><span class="sxs-lookup"><span data-stu-id="85112-164">During a **SubmitMessage** call, the MAPI spooler processes methods for objects that are opened during the transfer of the message, and it processes any attachments.</span></span> <span data-ttu-id="85112-165">Обработка может занять длительное время.</span><span class="sxs-lookup"><span data-stu-id="85112-165">This processing can take a long time.</span></span> <span data-ttu-id="85112-166">Поставщики транспорта могут часто вызывать метод [имаписуппорт:: спулериелд](imapisupport-spooleryield.md) для ДИСПЕТЧЕРА очереди MAPI во время этой обработки, чтобы освободить время ЦП для других системных задач.</span><span class="sxs-lookup"><span data-stu-id="85112-166">Transport providers can call the [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) method for the MAPI spooler frequently during this processing to release CPU time for other system tasks.</span></span> 
  
<span data-ttu-id="85112-167">Все получатели сообщения отображаются в таблице получателей сообщения о первоначальном переданном диспетчере очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="85112-167">All message recipients are visible in the recipient table of the message that the MAPI spooler originally passed.</span></span> <span data-ttu-id="85112-168">Поставщик транспорта должен обрабатывать только тех получателей, которые могут обрабатываться, на основе идентификатора записи, типа адреса или того, у которого нет свойства **пр_респонсибилити** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)), для которого не задано значение true.</span><span class="sxs-lookup"><span data-stu-id="85112-168">The transport provider should process only those recipients that it can handle — based on entry identifier, address type, or both — and that do not already have their **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property set to TRUE.</span></span> <span data-ttu-id="85112-169">Если для **пр_респонсибилити** уже ЗАДАНО значение true, этот получатель обработал другой поставщик транспорта.</span><span class="sxs-lookup"><span data-stu-id="85112-169">If **PR_RESPONSIBILITY** is already set to TRUE, another transport provider has handled that recipient.</span></span> <span data-ttu-id="85112-170">Когда поставщик выполняет достаточную обработку получателя, чтобы определить, может ли он обрабатывать сообщения для этого получателя, он должен задать для свойства **пр_респонсибилити** этого получателя значение true в переданном сообщении.</span><span class="sxs-lookup"><span data-stu-id="85112-170">When the provider completes sufficient processing of a recipient to determine whether it can handle messages for that recipient, it should set that recipient's **PR_RESPONSIBILITY** property to TRUE in the passed message.</span></span> <span data-ttu-id="85112-171">Как правило, поставщик выполняет это определение после завершения доставки сообщения.</span><span class="sxs-lookup"><span data-stu-id="85112-171">Usually, the provider makes this determination after message delivery is complete.</span></span> 
  
<span data-ttu-id="85112-172">Как правило, поставщик транспорта не возвращает вызов **субмитмессаже** до завершения передачи данных сообщения.</span><span class="sxs-lookup"><span data-stu-id="85112-172">Typically, the transport provider does not return from a **SubmitMessage** call until it completes the transfer of message data.</span></span> <span data-ttu-id="85112-173">Если сообщение об ошибке не возвращается, следующий вызов из очереди MAPI к поставщику является вызовом метода [иксплогон:: ендмессаже](ixplogon-endmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="85112-173">If no error is returned, the next call from the MAPI spooler to the provider is a call to the [IXPLogon::EndMessage](ixplogon-endmessage.md) method.</span></span> 
  
<span data-ttu-id="85112-174">Если **субмитмессаже** возвращает ошибку, диспетчер очереди MAPI освобождает сообщение в процессе без сохранения изменений.</span><span class="sxs-lookup"><span data-stu-id="85112-174">If **SubmitMessage** returns an error, the MAPI spooler releases the message in process without saving changes.</span></span> <span data-ttu-id="85112-175">Если поставщик транспорта требует сохранения изменений в сообщениях, он должен вызвать метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) для сообщения перед возвращением.</span><span class="sxs-lookup"><span data-stu-id="85112-175">If the transport provider requires message changes to be saved, it must call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the message before returning.</span></span> 
  
<span data-ttu-id="85112-176">В случае ошибок, возникающих из-за проблем транспорта, диспетчер очереди MAPI сохраняет сообщение, но откладывает повторную отправку сообщения поставщику транспорта на основании значения, возвращаемого в _лпулретурнпарм_.</span><span class="sxs-lookup"><span data-stu-id="85112-176">In case of errors that occur because of transport problems, the MAPI spooler retains the message, but it delays resubmitting the message to the transport provider based on the value returned in  _lpulReturnParm_.</span></span> <span data-ttu-id="85112-177">Поставщик транспорта должен заполнить это значение, если его возвращаемое значение из **субмитмессаже** равно МАПИ_Е_ВАИТ или мапи_е_нетворк_еррор.</span><span class="sxs-lookup"><span data-stu-id="85112-177">The transport provider must fill in that value if its return value from **SubmitMessage** is MAPI_E_WAIT or MAPI_E_NETWORK_ERROR.</span></span> <span data-ttu-id="85112-178">При возникновении критической ошибки поставщик транспорта должен вызвать метод [имаписуппорт:: спулернотифи](imapisupport-spoolernotify.md) с флагом нотифи_критикал_еррор.</span><span class="sxs-lookup"><span data-stu-id="85112-178">If a severe error condition occurs, the transport provider must call the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_CRITICAL_ERROR flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="85112-179">См. также</span><span class="sxs-lookup"><span data-stu-id="85112-179">See also</span></span>



[<span data-ttu-id="85112-180">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="85112-180">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="85112-181">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="85112-181">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="85112-182">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="85112-182">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="85112-183">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="85112-183">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md)
  
[<span data-ttu-id="85112-184">IXPLogon::TransportNotify</span><span class="sxs-lookup"><span data-stu-id="85112-184">IXPLogon::TransportNotify</span></span>](ixplogon-transportnotify.md)
  
[<span data-ttu-id="85112-185">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="85112-185">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

