---
title: IMAPISupportSpoolerNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SpoolerNotify
api_type:
- COM
ms.assetid: d4f153b2-939f-4153-85fb-dc510193848c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 99377d63b4b5cf8731809446b70770f0c24231ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423771"
---
# <a name="imapisupportspoolernotify"></a><span data-ttu-id="5a546-103">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="5a546-103">IMAPISupport::SpoolerNotify</span></span>

  
  
<span data-ttu-id="5a546-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a546-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a546-105">Сообщает шпалеру MAPI об изменении состояния или запросе на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="5a546-105">Notifies the MAPI spooler of a change in status or a request for service.</span></span> 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a><span data-ttu-id="5a546-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="5a546-106">Parameters</span></span>

 <span data-ttu-id="5a546-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5a546-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5a546-108">[in] Битмашка флагов, которая указывает тип уведомления.</span><span class="sxs-lookup"><span data-stu-id="5a546-108">[in] A bitmask of flags that indicates the type of notification.</span></span> <span data-ttu-id="5a546-109">Поставщики транспорта могут устанавливать все флаги, за исключением NOTIFY_NEWMAIL_RECEIVED; только NOTIFY_NEWMAIL_RECEIVED и NOTIFY_READTOSEND допустимы для поставщиков хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="5a546-109">Transport providers can set all of the flags except for NOTIFY_NEWMAIL_RECEIVED; only NOTIFY_NEWMAIL_RECEIVED and NOTIFY_READTOSEND are valid for message store providers.</span></span> <span data-ttu-id="5a546-110">Для параметра  _ulFlags_ допустимы следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="5a546-110">The following flags are valid for the  _ulFlags_ parameter:</span></span> 
    
<span data-ttu-id="5a546-111">NOTIFY_CONFIG_CHANGE</span><span class="sxs-lookup"><span data-stu-id="5a546-111">NOTIFY_CONFIG_CHANGE</span></span> 
  
> <span data-ttu-id="5a546-112">Регистрирует запрос на изменение конфигурации поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="5a546-112">Registers a request to change the transport provider's configuration.</span></span> 
    
<span data-ttu-id="5a546-113">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="5a546-113">NOTIFY_CRITICAL_ERROR</span></span> 
  
> <span data-ttu-id="5a546-114">В поставщике транспорта произошла невозвратная ошибка.</span><span class="sxs-lookup"><span data-stu-id="5a546-114">An unrecoverable error has occurred to the transport provider.</span></span> <span data-ttu-id="5a546-115">Так как NOTIFY_SENTDEFERRED и NOTIFY_CRITICAL_ERROR для вызовов поставщика транспорта используется параметр  _lpvData,_ эти флаги являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="5a546-115">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter for transport provider calls, these flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="5a546-116">NOTIFY_CRITSEC</span><span class="sxs-lookup"><span data-stu-id="5a546-116">NOTIFY_CRITSEC</span></span> 
  
> <span data-ttu-id="5a546-117">Запрашивает критически важный раздел для поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="5a546-117">Requests a critical section for the transport provider.</span></span> <span data-ttu-id="5a546-118">Параметр  _lpvData_ неопределяем и должен быть NULL.</span><span class="sxs-lookup"><span data-stu-id="5a546-118">The  _lpvData_ parameter is undefined and should be NULL.</span></span> 
    
<span data-ttu-id="5a546-119">NOTIFY_NEWMAIL</span><span class="sxs-lookup"><span data-stu-id="5a546-119">NOTIFY_NEWMAIL</span></span> 
  
> <span data-ttu-id="5a546-120">Шпалер MAPI должен скачать все вновь полученные сообщения в следующее доступное время.</span><span class="sxs-lookup"><span data-stu-id="5a546-120">The MAPI spooler should download any newly received messages at the next available time.</span></span> <span data-ttu-id="5a546-121">Параметр  _lpvData_ не установлен и должен быть задан в NULL.</span><span class="sxs-lookup"><span data-stu-id="5a546-121">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="5a546-122">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="5a546-122">NOTIFY_NEWMAIL_RECEIVED</span></span> 
  
> <span data-ttu-id="5a546-123">В хранилище сообщений получено новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="5a546-123">A new message has been received in the message store.</span></span> <span data-ttu-id="5a546-124">Параметр  _lpvData_ указывает на структуру [NEWMAIL_NOTIFICATION,](newmail_notification.md) описываемую сообщение.</span><span class="sxs-lookup"><span data-stu-id="5a546-124">The  _lpvData_ parameter points to a [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that describes the message.</span></span> <span data-ttu-id="5a546-125">Этот флаг используется для поставщиков магазинов сообщений, тесно соединых с поставщиками транспорта, и игнорируется, если поставщик магазина вошел в систему с MAPI_NO_MAIL флагом.</span><span class="sxs-lookup"><span data-stu-id="5a546-125">This flag is used for message store providers that are tightly coupled with transport providers and is ignored if the store provider is logged on with the MAPI_NO_MAIL flag set.</span></span> 
    
<span data-ttu-id="5a546-126">NOTIFY_NONCRIT</span><span class="sxs-lookup"><span data-stu-id="5a546-126">NOTIFY_NONCRIT</span></span> 
  
> <span data-ttu-id="5a546-127">Выпускает критический раздел, полученный при предыдущем вызове **в SpoolerNotify** с  _набором ulFlags_ для NOTIFY_CRITSEC.</span><span class="sxs-lookup"><span data-stu-id="5a546-127">Releases a critical section that was obtained with a previous call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="5a546-128">Параметр  _lpvData_ не установлен и должен быть задан в NULL.</span><span class="sxs-lookup"><span data-stu-id="5a546-128">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="5a546-129">NOTIFY_READYTOSEND</span><span class="sxs-lookup"><span data-stu-id="5a546-129">NOTIFY_READYTOSEND</span></span> 
  
> <span data-ttu-id="5a546-130">Поставщик транспорта или магазина сообщений готов отправлять сообщения.</span><span class="sxs-lookup"><span data-stu-id="5a546-130">The transport or message store provider is ready to send messages.</span></span> <span data-ttu-id="5a546-131">Параметр  _lpvData_ не установлен и должен быть задан в NULL.</span><span class="sxs-lookup"><span data-stu-id="5a546-131">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="5a546-132">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="5a546-132">NOTIFY_SENTDEFERRED</span></span> 
  
> <span data-ttu-id="5a546-133">Ранее отложенное сообщение должно быть отправлено, и поставщик транспорта должен быть уведомлен, когда сообщение будет готово к отправке с помощью вызова метода [IXPLogon::SubmitMessage.](ixplogon-submitmessage.md)</span><span class="sxs-lookup"><span data-stu-id="5a546-133">A previously deferred message should now be sent, and the transport provider should be notified when the message is ready to be delivered by using a call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> <span data-ttu-id="5a546-134">Идентификатор входа отложенного сообщения содержится в [структуре SBinary,](sbinary.md) на которые указывает _lpvData._</span><span class="sxs-lookup"><span data-stu-id="5a546-134">The entry identifier of the deferred message is contained in an [SBinary](sbinary.md) structure pointed to by  _lpvData_.</span></span> <span data-ttu-id="5a546-135">Так как NOTIFY_SENTDEFERRED и NOTIFY_CRITICAL_ERROR используют параметр  _lpvData,_ эти флаги являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="5a546-135">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter, these flags are mutually exclusive.</span></span> 
    
 <span data-ttu-id="5a546-136">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="5a546-136">_lpvData_</span></span>
  
> <span data-ttu-id="5a546-137">[in] Указатель на связанные данные, применимые к уведомлению.</span><span class="sxs-lookup"><span data-stu-id="5a546-137">[in] A pointer to associated data applicable to a notification.</span></span> <span data-ttu-id="5a546-138">Параметр  _lpvData_ указывает на допустимые данные только при задании следующих флагов _(lpvData_ является NULL, когда  _ulFlags_ задан для других типов уведомлений):</span><span class="sxs-lookup"><span data-stu-id="5a546-138">The  _lpvData_ parameter points to valid data only when the following flags are set (_lpvData_ is NULL when  _ulFlags_ is set to the other notification types):</span></span> 
    
|<span data-ttu-id="5a546-139">**_Параметр ulFlags_**</span><span class="sxs-lookup"><span data-stu-id="5a546-139">**_ulFlags_ setting**</span></span>|<span data-ttu-id="5a546-140">**_значение lpvData_**</span><span class="sxs-lookup"><span data-stu-id="5a546-140">**_lpvData_ value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5a546-141">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="5a546-141">NOTIFY_CRITICAL_ERROR</span></span>  <br/> |<span data-ttu-id="5a546-142">Сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="5a546-142">Information about the error.</span></span>  <br/> |
|<span data-ttu-id="5a546-143">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="5a546-143">NOTIFY_NEWMAIL_RECEIVED</span></span>  <br/> |<span data-ttu-id="5a546-144">Структура **NEWMAIL_NOTIFICATION,** которая содержит сведения о вновь доставленном сообщении.</span><span class="sxs-lookup"><span data-stu-id="5a546-144">A **NEWMAIL_NOTIFICATION** structure that contains information about the newly delivered message.</span></span>  <br/> |
|<span data-ttu-id="5a546-145">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="5a546-145">NOTIFY_SENTDEFERRED</span></span>  <br/> |<span data-ttu-id="5a546-146">Структура **SBinary,** которая содержит идентификатор входа отложенного сообщения.</span><span class="sxs-lookup"><span data-stu-id="5a546-146">An **SBinary** structure that contains the entry identifier of deferred message.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="5a546-147">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5a546-147">Return value</span></span>

<span data-ttu-id="5a546-148">S_OK</span><span class="sxs-lookup"><span data-stu-id="5a546-148">S_OK</span></span> 
  
> <span data-ttu-id="5a546-149">Уведомление было успешным.</span><span class="sxs-lookup"><span data-stu-id="5a546-149">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5a546-150">Примечания</span><span class="sxs-lookup"><span data-stu-id="5a546-150">Remarks</span></span>

<span data-ttu-id="5a546-151">Метод **IMAPISupport::SpoolerNotify** реализован для объектов хранения сообщений и поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="5a546-151">The **IMAPISupport::SpoolerNotify** method is implemented for message store and transport provider support objects.</span></span> <span data-ttu-id="5a546-152">Эти поставщики **звонят в SpoolerNotify,** чтобы уведомить шпалер MAPI об изменении состояния или запросе на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="5a546-152">These providers call **SpoolerNotify** to notify the MAPI spooler of a change in status or a request for service.</span></span> <span data-ttu-id="5a546-153">**SpoolerNotify** называется главным образом поставщиками транспорта и может быть вызвана в любое время во время сеанса.</span><span class="sxs-lookup"><span data-stu-id="5a546-153">**SpoolerNotify** is called primarily by transport providers and may be called at any time during the session.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="5a546-154">Заметки поставщикам транспорта</span><span class="sxs-lookup"><span data-stu-id="5a546-154">Notes to Transport Providers</span></span>

<span data-ttu-id="5a546-155">Если вы изменили конфигурацию поставщика транспорта, позвоните **в SpoolerNotify** и установите  _ulFlags_ для NOTIFY_CONFIG_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="5a546-155">If you have changed your transport provider configuration, call **SpoolerNotify** and set  _ulFlags_ to NOTIFY_CONFIG_CHANGED.</span></span> <span data-ttu-id="5a546-156">**SpoolerNotify** отвечает, вызывая [метод IXPLogon::AddressTypes](ixplogon-addresstypes.md) для запроса на изменение поддерживаемых типов адресов.</span><span class="sxs-lookup"><span data-stu-id="5a546-156">**SpoolerNotify** responds by calling the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to query for a change in supported address types.</span></span> 
  
<span data-ttu-id="5a546-157">Если вам нужен критический раздел для обеспечения непрерывной обработки, позвоните **в SpoolerNotify** с  _набором ulFlags_ для NOTIFY_CRITSEC.</span><span class="sxs-lookup"><span data-stu-id="5a546-157">If you need a critical section to ensure uninterrupted processing, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="5a546-158">Настройка этого флага информирует шпалер MAPI о том, что он не должен вызывать методы [IXPLogon::Idle](ixplogon-idle.md) и [IXPLogon::P oll.](ixplogon-poll.md)</span><span class="sxs-lookup"><span data-stu-id="5a546-158">Setting this flag informs the MAPI spooler that it should not call the [IXPLogon::Idle](ixplogon-idle.md) and [IXPLogon::Poll](ixplogon-poll.md) methods.</span></span> <span data-ttu-id="5a546-159">Хотя у вас открыт критический раздел, MAPI_E_BUSY, когда называется метод [IMAPIStatus::ValidateState.](imapistatus-validatestate.md)</span><span class="sxs-lookup"><span data-stu-id="5a546-159">While you have a critical section open, return MAPI_E_BUSY whenever the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is called.</span></span> <span data-ttu-id="5a546-160">После завершения критического раздела сделайте еще один вызов **в SpoolerNotify** с  _набором ulFlags_ для NOTIFY_NONCRIT.</span><span class="sxs-lookup"><span data-stu-id="5a546-160">When you are finished with the critical section, make another call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NONCRIT.</span></span> 
  
<span data-ttu-id="5a546-161">Например, если поставщик удаленного транспорта находится в процессе отправки сообщений, может потребоваться разрешить пользователю ввести номер телефона для установления удаленного подключения.</span><span class="sxs-lookup"><span data-stu-id="5a546-161">For example, if your remote transport provider is in the process of uploading messages, you might need to allow a user to enter a telephone number to establish the remote connection.</span></span> <span data-ttu-id="5a546-162">Перед циклом в диалоговом окне необходимо объявить критический раздел.</span><span class="sxs-lookup"><span data-stu-id="5a546-162">Before you loop through the dialog box procedure, you should declare a critical section.</span></span> <span data-ttu-id="5a546-163">Когда пользователь закрывает диалоговое окно, завершая процедуру диалогового окна, необходимо освободить критический раздел.</span><span class="sxs-lookup"><span data-stu-id="5a546-163">When the user closes the dialog box, terminating the dialog box procedure, you should release the critical section.</span></span>
  
<span data-ttu-id="5a546-164">При задаче  _ulFlags_ NOTIFY_CRITICAL_ERROR, пуллер MAPI не вызывает поставщика, кроме как освободить его.</span><span class="sxs-lookup"><span data-stu-id="5a546-164">When you set  _ulFlags_ to NOTIFY_CRITICAL_ERROR, the MAPI spooler makes no further calls to the provider except to release it.</span></span> <span data-ttu-id="5a546-165">Если вы вызываете **SpoolerNotify** с набором NOTIFY_CRITICAL_ERROR из [IXPLogon::StartMessage](ixplogon-startmessage.md) или [IXPLogon::SubmitMessage,](ixplogon-submitmessage.md) вернись с соответствующим значением ошибки из **startMessage** или \*\* SubmitMessage \*\* call immediately after the **SpoolerNotify** call.</span><span class="sxs-lookup"><span data-stu-id="5a546-165">If you call **SpoolerNotify** with NOTIFY_CRITICAL_ERROR set from the [IXPLogon::StartMessage](ixplogon-startmessage.md) or [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) methods, return with an appropriate error value from the **StartMessage** or \*\* SubmitMessage \*\* call immediately after the **SpoolerNotify** call.</span></span> 
  
<span data-ttu-id="5a546-166">Если поставщик транспорта оправился от условия, которое ранее привело к сбойу, позвоните **в SpoolerNotify** с  _набором ulFlags_ для NOTIFY_READYTOSEND.</span><span class="sxs-lookup"><span data-stu-id="5a546-166">If your transport provider recovered from a condition that previously caused it to fail, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_READYTOSEND.</span></span> <span data-ttu-id="5a546-167">Этот флаг указывает, что поставщик снова готов обрабатывать сообщения.</span><span class="sxs-lookup"><span data-stu-id="5a546-167">This flag indicates that the provider is again ready to handle messages.</span></span> 
  
## <a name="notes-to-message-store-providers"></a><span data-ttu-id="5a546-168">Заметки поставщикам магазина сообщений</span><span class="sxs-lookup"><span data-stu-id="5a546-168">Notes to Message Store Providers</span></span>

<span data-ttu-id="5a546-169">Вызывай **SpoolerNotify** NOTIFY_READYTOSEND, перед тем как сделать первый звонок в [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md) в **IMessage::SubmitMessage.**</span><span class="sxs-lookup"><span data-stu-id="5a546-169">Call **SpoolerNotify**, passing the NOTIFY_READYTOSEND flag in  _ulFlags_, before you make your first call to [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) in **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="5a546-170">Этот вызов **в SpoolerNotify** должен быть выполнен только один раз за сеанс.</span><span class="sxs-lookup"><span data-stu-id="5a546-170">This call to **SpoolerNotify** needs to be made only once per session.</span></span> 
  
<span data-ttu-id="5a546-171">Если поставщик магазина сообщений тесно соединимся с поставщиком транспорта, и вы звоните **в SpoolerNotify** с набором  _ulFlags_ NOTIFY_NEWMAIL_RECEIVED, пульпер MAPI открывает новое сообщение и начинает обработку новой функции крюка сообщения.</span><span class="sxs-lookup"><span data-stu-id="5a546-171">If your message store provider is tightly coupled with a transport provider and you call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NEWMAIL_RECEIVED, the MAPI spooler opens the new message and begins processing the new message hook function.</span></span> <span data-ttu-id="5a546-172">После завершения обработки шпалер MAPI вызывает [метод IMsgStore::NotifyNewMail,](imsgstore-notifynewmail.md) чтобы сообщить вам о новом сообщении.</span><span class="sxs-lookup"><span data-stu-id="5a546-172">When processing is complete, the MAPI spooler calls the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method to inform you of your own new message.</span></span> 
  
<span data-ttu-id="5a546-173">Дополнительные сведения о вызове **SpoolerNotify** см. в следующих темах:</span><span class="sxs-lookup"><span data-stu-id="5a546-173">For more information about calling **SpoolerNotify**, see any of the following topics:</span></span>
  
- [<span data-ttu-id="5a546-174">Реализация метода FlushQueues</span><span class="sxs-lookup"><span data-stu-id="5a546-174">Implementing the FlushQueues Method</span></span>](implementing-the-flushqueues-method.md)
    
- [<span data-ttu-id="5a546-175">Взаимодействие со Spooler MAPI</span><span class="sxs-lookup"><span data-stu-id="5a546-175">Interacting with the MAPI Spooler</span></span>](interacting-with-the-mapi-spooler.md)
    
- [<span data-ttu-id="5a546-176">Модель приема сообщений</span><span class="sxs-lookup"><span data-stu-id="5a546-176">Message Reception Model</span></span>](message-reception-model.md)
    
## <a name="see-also"></a><span data-ttu-id="5a546-177">См. также</span><span class="sxs-lookup"><span data-stu-id="5a546-177">See also</span></span>



[<span data-ttu-id="5a546-178">IMsgStore::NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="5a546-178">IMsgStore::NotifyNewMail</span></span>](imsgstore-notifynewmail.md)
  
[<span data-ttu-id="5a546-179">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="5a546-179">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="5a546-180">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="5a546-180">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="5a546-181">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5a546-181">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

