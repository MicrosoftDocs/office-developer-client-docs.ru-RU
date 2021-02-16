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
# <a name="imapisupportspoolernotify"></a><span data-ttu-id="e52da-103">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="e52da-103">IMAPISupport::SpoolerNotify</span></span>

  
  
<span data-ttu-id="e52da-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e52da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e52da-105">Сообщает пулу MAPI об изменении состояния или запросе на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="e52da-105">Notifies the MAPI spooler of a change in status or a request for service.</span></span> 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a><span data-ttu-id="e52da-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e52da-106">Parameters</span></span>

 <span data-ttu-id="e52da-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e52da-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e52da-108">[in] Битоваяmas флагов, которая указывает тип уведомления.</span><span class="sxs-lookup"><span data-stu-id="e52da-108">[in] A bitmask of flags that indicates the type of notification.</span></span> <span data-ttu-id="e52da-109">Поставщики транспорта могут устанавливать все флаги, кроме NOTIFY_NEWMAIL_RECEIVED; только NOTIFY_NEWMAIL_RECEIVED и NOTIFY_READTOSEND допустимы для поставщиков store сообщений.</span><span class="sxs-lookup"><span data-stu-id="e52da-109">Transport providers can set all of the flags except for NOTIFY_NEWMAIL_RECEIVED; only NOTIFY_NEWMAIL_RECEIVED and NOTIFY_READTOSEND are valid for message store providers.</span></span> <span data-ttu-id="e52da-110">Для параметра  _ulFlags_ допустимы следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="e52da-110">The following flags are valid for the  _ulFlags_ parameter:</span></span> 
    
<span data-ttu-id="e52da-111">NOTIFY_CONFIG_CHANGE</span><span class="sxs-lookup"><span data-stu-id="e52da-111">NOTIFY_CONFIG_CHANGE</span></span> 
  
> <span data-ttu-id="e52da-112">Регистрирует запрос на изменение конфигурации поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="e52da-112">Registers a request to change the transport provider's configuration.</span></span> 
    
<span data-ttu-id="e52da-113">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="e52da-113">NOTIFY_CRITICAL_ERROR</span></span> 
  
> <span data-ttu-id="e52da-114">Произошла неу обнаруженная ошибка для поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="e52da-114">An unrecoverable error has occurred to the transport provider.</span></span> <span data-ttu-id="e52da-115">Так как NOTIFY_SENTDEFERRED и NOTIFY_CRITICAL_ERROR использовать параметр  _lpvData_ для вызовов поставщика транспорта, эти флаги являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="e52da-115">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter for transport provider calls, these flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="e52da-116">NOTIFY_CRITSEC</span><span class="sxs-lookup"><span data-stu-id="e52da-116">NOTIFY_CRITSEC</span></span> 
  
> <span data-ttu-id="e52da-117">Запрашивает критический раздел для поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="e52da-117">Requests a critical section for the transport provider.</span></span> <span data-ttu-id="e52da-118">Параметр  _lpvData_ не задан и должен иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="e52da-118">The  _lpvData_ parameter is undefined and should be NULL.</span></span> 
    
<span data-ttu-id="e52da-119">NOTIFY_NEWMAIL</span><span class="sxs-lookup"><span data-stu-id="e52da-119">NOTIFY_NEWMAIL</span></span> 
  
> <span data-ttu-id="e52da-120">The MAPI spooler should download any newly received messages at the next available time.</span><span class="sxs-lookup"><span data-stu-id="e52da-120">The MAPI spooler should download any newly received messages at the next available time.</span></span> <span data-ttu-id="e52da-121">Параметр  _lpvData_ не задан и должен иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="e52da-121">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="e52da-122">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="e52da-122">NOTIFY_NEWMAIL_RECEIVED</span></span> 
  
> <span data-ttu-id="e52da-123">В хранилище сообщений получено новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="e52da-123">A new message has been received in the message store.</span></span> <span data-ttu-id="e52da-124">Параметр  _lpvData указывает_ на [NEWMAIL_NOTIFICATION,](newmail_notification.md) которая описывает сообщение.</span><span class="sxs-lookup"><span data-stu-id="e52da-124">The  _lpvData_ parameter points to a [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that describes the message.</span></span> <span data-ttu-id="e52da-125">Этот флаг используется для поставщиков хранения сообщений, которые тесно совмещение с поставщиками транспорта, и игнорируется, если поставщик магазина вошел в систему с установленным MAPI_NO_MAIL флагом.</span><span class="sxs-lookup"><span data-stu-id="e52da-125">This flag is used for message store providers that are tightly coupled with transport providers and is ignored if the store provider is logged on with the MAPI_NO_MAIL flag set.</span></span> 
    
<span data-ttu-id="e52da-126">NOTIFY_NONCRIT</span><span class="sxs-lookup"><span data-stu-id="e52da-126">NOTIFY_NONCRIT</span></span> 
  
> <span data-ttu-id="e52da-127">Освобождает критический раздел, полученный при предыдущем вызове **SpoolerNotify,** для  _ulFlags_ установлено значение NOTIFY_CRITSEC.</span><span class="sxs-lookup"><span data-stu-id="e52da-127">Releases a critical section that was obtained with a previous call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="e52da-128">Параметр  _lpvData_ не задан и должен иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="e52da-128">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="e52da-129">NOTIFY_READYTOSEND</span><span class="sxs-lookup"><span data-stu-id="e52da-129">NOTIFY_READYTOSEND</span></span> 
  
> <span data-ttu-id="e52da-130">Поставщик транспорта или хранения сообщений готов к отправке сообщений.</span><span class="sxs-lookup"><span data-stu-id="e52da-130">The transport or message store provider is ready to send messages.</span></span> <span data-ttu-id="e52da-131">Параметр  _lpvData_ не задан и должен иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="e52da-131">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="e52da-132">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="e52da-132">NOTIFY_SENTDEFERRED</span></span> 
  
> <span data-ttu-id="e52da-133">Теперь необходимо отправить ранее отложенное сообщение, и поставщик транспорта должен быть уведомлен о готовности сообщения к доставке с помощью вызова метода [IXPLogon::SubmitMessage.](ixplogon-submitmessage.md)</span><span class="sxs-lookup"><span data-stu-id="e52da-133">A previously deferred message should now be sent, and the transport provider should be notified when the message is ready to be delivered by using a call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> <span data-ttu-id="e52da-134">Идентификатор записи отложенного сообщения содержится в структуре [SBinary,](sbinary.md) на который указывает _lpvData._</span><span class="sxs-lookup"><span data-stu-id="e52da-134">The entry identifier of the deferred message is contained in an [SBinary](sbinary.md) structure pointed to by  _lpvData_.</span></span> <span data-ttu-id="e52da-135">Так как NOTIFY_SENTDEFERRED и NOTIFY_CRITICAL_ERROR использовать параметр  _lpvData,_ эти флаги являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="e52da-135">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter, these flags are mutually exclusive.</span></span> 
    
 <span data-ttu-id="e52da-136">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="e52da-136">_lpvData_</span></span>
  
> <span data-ttu-id="e52da-137">[in] Указатель на связанные данные, применимые к уведомлению.</span><span class="sxs-lookup"><span data-stu-id="e52da-137">[in] A pointer to associated data applicable to a notification.</span></span> <span data-ttu-id="e52da-138">Параметр  _lpvData_ указывает на допустимые данные, только если заданы следующие флаги (_lpvData_ имеет NULL, если  _для ulFlags_ заданы другие типы уведомлений):</span><span class="sxs-lookup"><span data-stu-id="e52da-138">The  _lpvData_ parameter points to valid data only when the following flags are set (_lpvData_ is NULL when  _ulFlags_ is set to the other notification types):</span></span> 
    
|<span data-ttu-id="e52da-139">**_Параметр ulFlags_**</span><span class="sxs-lookup"><span data-stu-id="e52da-139">**_ulFlags_ setting**</span></span>|<span data-ttu-id="e52da-140">**_Значение lpvData_**</span><span class="sxs-lookup"><span data-stu-id="e52da-140">**_lpvData_ value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e52da-141">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="e52da-141">NOTIFY_CRITICAL_ERROR</span></span>  <br/> |<span data-ttu-id="e52da-142">Сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="e52da-142">Information about the error.</span></span>  <br/> |
|<span data-ttu-id="e52da-143">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="e52da-143">NOTIFY_NEWMAIL_RECEIVED</span></span>  <br/> |<span data-ttu-id="e52da-144">Структура **NEWMAIL_NOTIFICATION,** которая содержит сведения о только что доставленном сообщении.</span><span class="sxs-lookup"><span data-stu-id="e52da-144">A **NEWMAIL_NOTIFICATION** structure that contains information about the newly delivered message.</span></span>  <br/> |
|<span data-ttu-id="e52da-145">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="e52da-145">NOTIFY_SENTDEFERRED</span></span>  <br/> |<span data-ttu-id="e52da-146">Структура **SBinary,** которая содержит идентификатор записи отложенного сообщения.</span><span class="sxs-lookup"><span data-stu-id="e52da-146">An **SBinary** structure that contains the entry identifier of deferred message.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="e52da-147">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e52da-147">Return value</span></span>

<span data-ttu-id="e52da-148">S_OK</span><span class="sxs-lookup"><span data-stu-id="e52da-148">S_OK</span></span> 
  
> <span data-ttu-id="e52da-149">Уведомление успешно.</span><span class="sxs-lookup"><span data-stu-id="e52da-149">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e52da-150">Примечания</span><span class="sxs-lookup"><span data-stu-id="e52da-150">Remarks</span></span>

<span data-ttu-id="e52da-151">Метод **IMAPISupport::SpoolerNotify реализован** для объектов поддержки службы хранения сообщений и поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="e52da-151">The **IMAPISupport::SpoolerNotify** method is implemented for message store and transport provider support objects.</span></span> <span data-ttu-id="e52da-152">Эти поставщики **вызывали SpoolerNotify,** чтобы уведомить пультер MAPI об изменении состояния или запросе на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="e52da-152">These providers call **SpoolerNotify** to notify the MAPI spooler of a change in status or a request for service.</span></span> <span data-ttu-id="e52da-153">**SpoolerNotify** в основном вызван поставщиками транспорта и может быть вызван в любое время во время сеанса.</span><span class="sxs-lookup"><span data-stu-id="e52da-153">**SpoolerNotify** is called primarily by transport providers and may be called at any time during the session.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="e52da-154">Примечания для поставщиков транспорта</span><span class="sxs-lookup"><span data-stu-id="e52da-154">Notes to Transport Providers</span></span>

<span data-ttu-id="e52da-155">Если вы изменили конфигурацию поставщика транспорта, вызовите **SpoolerNotify** и установите  _для ulFlags_ NOTIFY_CONFIG_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="e52da-155">If you have changed your transport provider configuration, call **SpoolerNotify** and set  _ulFlags_ to NOTIFY_CONFIG_CHANGED.</span></span> <span data-ttu-id="e52da-156">**В ответ SpoolerNotify** вызывает метод [IXPLogon::AddressTypes](ixplogon-addresstypes.md) для запроса на изменение поддерживаемых типов адресов.</span><span class="sxs-lookup"><span data-stu-id="e52da-156">**SpoolerNotify** responds by calling the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to query for a change in supported address types.</span></span> 
  
<span data-ttu-id="e52da-157">Если требуется критический раздел для непрерывной обработки, вызовите **SpoolerNotify** с  _ulFlags,_ установленным NOTIFY_CRITSEC.</span><span class="sxs-lookup"><span data-stu-id="e52da-157">If you need a critical section to ensure uninterrupted processing, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="e52da-158">Установка этого флага сообщает пулу MAPI о том, что он не должен вызывать методы [IXPLogon::Idle](ixplogon-idle.md) и [IXPLogon::P oll.](ixplogon-poll.md)</span><span class="sxs-lookup"><span data-stu-id="e52da-158">Setting this flag informs the MAPI spooler that it should not call the [IXPLogon::Idle](ixplogon-idle.md) and [IXPLogon::Poll](ixplogon-poll.md) methods.</span></span> <span data-ttu-id="e52da-159">При открытом критическом разделе MAPI_E_BUSY каждый раз, когда будет вызван метод [IMAPIStatus::ValidateState.](imapistatus-validatestate.md)</span><span class="sxs-lookup"><span data-stu-id="e52da-159">While you have a critical section open, return MAPI_E_BUSY whenever the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is called.</span></span> <span data-ttu-id="e52da-160">Завершив критический раздел, еще раз вызовите **SpoolerNotify,** где для  _ulFlags_ установлено значение NOTIFY_NONCRIT.</span><span class="sxs-lookup"><span data-stu-id="e52da-160">When you are finished with the critical section, make another call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NONCRIT.</span></span> 
  
<span data-ttu-id="e52da-161">Например, если ваш удаленный поставщик транспорта загружает сообщения, может потребоваться разрешить пользователю вводить телефонный номер, чтобы установить удаленное подключение.</span><span class="sxs-lookup"><span data-stu-id="e52da-161">For example, if your remote transport provider is in the process of uploading messages, you might need to allow a user to enter a telephone number to establish the remote connection.</span></span> <span data-ttu-id="e52da-162">Перед циклом процедуры в диалоговом окне объявите критический раздел.</span><span class="sxs-lookup"><span data-stu-id="e52da-162">Before you loop through the dialog box procedure, you should declare a critical section.</span></span> <span data-ttu-id="e52da-163">Когда пользователь закрывает диалоговое окно, завершая процедуру диалоговых окна, необходимо освободить критический раздел.</span><span class="sxs-lookup"><span data-stu-id="e52da-163">When the user closes the dialog box, terminating the dialog box procedure, you should release the critical section.</span></span>
  
<span data-ttu-id="e52da-164">Если вы установите  _для ulFlags_ NOTIFY_CRITICAL_ERROR, пулер MAPI не будет больше звонить поставщику, кроме как освободить его.</span><span class="sxs-lookup"><span data-stu-id="e52da-164">When you set  _ulFlags_ to NOTIFY_CRITICAL_ERROR, the MAPI spooler makes no further calls to the provider except to release it.</span></span> <span data-ttu-id="e52da-165">If you call **SpoolerNotify** with NOTIFY_CRITICAL_ERROR set from the [IXPLogon::StartMessage](ixplogon-startmessage.md) or [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) methods, return with an appropriate error value from the **StartMessage** or \*\* SubmitMessage \*\* call immediately after the **SpoolerNotify** call.</span><span class="sxs-lookup"><span data-stu-id="e52da-165">If you call **SpoolerNotify** with NOTIFY_CRITICAL_ERROR set from the [IXPLogon::StartMessage](ixplogon-startmessage.md) or [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) methods, return with an appropriate error value from the **StartMessage** or \*\* SubmitMessage \*\* call immediately after the **SpoolerNotify** call.</span></span> 
  
<span data-ttu-id="e52da-166">Если ваш поставщик транспорта восстановился после условия, которое ранее вызывло сбой, вызовите **SpoolerNotify,** для  _ulFlags_ установлено NOTIFY_READYTOSEND.</span><span class="sxs-lookup"><span data-stu-id="e52da-166">If your transport provider recovered from a condition that previously caused it to fail, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_READYTOSEND.</span></span> <span data-ttu-id="e52da-167">Этот флаг указывает, что поставщик снова готов к обработке сообщений.</span><span class="sxs-lookup"><span data-stu-id="e52da-167">This flag indicates that the provider is again ready to handle messages.</span></span> 
  
## <a name="notes-to-message-store-providers"></a><span data-ttu-id="e52da-168">Примечания для поставщиков store сообщений</span><span class="sxs-lookup"><span data-stu-id="e52da-168">Notes to Message Store Providers</span></span>

<span data-ttu-id="e52da-169">Вызовите **SpoolerNotify,** передав флаг NOTIFY_READYTOSEND в _ulFlags_ перед первым вызовом [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md) в **IMessage::SubmitMessage.**</span><span class="sxs-lookup"><span data-stu-id="e52da-169">Call **SpoolerNotify**, passing the NOTIFY_READYTOSEND flag in  _ulFlags_, before you make your first call to [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) in **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="e52da-170">Этот вызов **SpoolerNotify** должен быть выполнен только один раз для каждого сеанса.</span><span class="sxs-lookup"><span data-stu-id="e52da-170">This call to **SpoolerNotify** needs to be made only once per session.</span></span> 
  
<span data-ttu-id="e52da-171">Если поставщик службы хранения сообщений тесно совмещение с поставщиком транспорта и вызовите **SpoolerNotify** с  _ulFlags,_ задав для него NOTIFY_NEWMAIL_RECEIVED, пулер MAPI откроет новое сообщение и начнет обработку новой функции обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="e52da-171">If your message store provider is tightly coupled with a transport provider and you call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NEWMAIL_RECEIVED, the MAPI spooler opens the new message and begins processing the new message hook function.</span></span> <span data-ttu-id="e52da-172">После завершения обработки пулер MAPI вызывает метод [IMsgStore::NotifyNewMail,](imsgstore-notifynewmail.md) чтобы сообщить вам о новом сообщении.</span><span class="sxs-lookup"><span data-stu-id="e52da-172">When processing is complete, the MAPI spooler calls the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method to inform you of your own new message.</span></span> 
  
<span data-ttu-id="e52da-173">Дополнительные сведения о вызове **SpoolerNotify** см. в следующих темах:</span><span class="sxs-lookup"><span data-stu-id="e52da-173">For more information about calling **SpoolerNotify**, see any of the following topics:</span></span>
  
- [<span data-ttu-id="e52da-174">Реализация метода FlushQueues</span><span class="sxs-lookup"><span data-stu-id="e52da-174">Implementing the FlushQueues Method</span></span>](implementing-the-flushqueues-method.md)
    
- [<span data-ttu-id="e52da-175">Взаимодействие с пулером MAPI</span><span class="sxs-lookup"><span data-stu-id="e52da-175">Interacting with the MAPI Spooler</span></span>](interacting-with-the-mapi-spooler.md)
    
- [<span data-ttu-id="e52da-176">Модель приема сообщений</span><span class="sxs-lookup"><span data-stu-id="e52da-176">Message Reception Model</span></span>](message-reception-model.md)
    
## <a name="see-also"></a><span data-ttu-id="e52da-177">См. также</span><span class="sxs-lookup"><span data-stu-id="e52da-177">See also</span></span>



[<span data-ttu-id="e52da-178">IMsgStore::NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="e52da-178">IMsgStore::NotifyNewMail</span></span>](imsgstore-notifynewmail.md)
  
[<span data-ttu-id="e52da-179">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="e52da-179">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="e52da-180">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="e52da-180">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="e52da-181">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e52da-181">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

