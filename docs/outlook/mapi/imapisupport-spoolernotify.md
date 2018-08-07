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
ms.openlocfilehash: 21ea5faaccb81e763d6d062b6ff567db509d9d35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809172"
---
# <a name="imapisupportspoolernotify"></a><span data-ttu-id="ee821-103">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="ee821-103">IMAPISupport::SpoolerNotify</span></span>

  
  
<span data-ttu-id="ee821-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ee821-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ee821-105">Уведомление об изменении состояния или запрос на обслуживание диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="ee821-105">Notifies the MAPI spooler of a change in status or a request for service.</span></span> 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a><span data-ttu-id="ee821-106">���������</span><span class="sxs-lookup"><span data-stu-id="ee821-106">Parameters</span></span>

 <span data-ttu-id="ee821-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ee821-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ee821-108">[in] Битовая маска флаги, которое указывает тип уведомления.</span><span class="sxs-lookup"><span data-stu-id="ee821-108">[in] A bitmask of flags that indicates the type of notification.</span></span> <span data-ttu-id="ee821-109">Поставщики транспорта можно задать все флажки кроме NOTIFY_NEWMAIL_RECEIVED; только NOTIFY_NEWMAIL_RECEIVED и NOTIFY_READTOSEND являются допустимыми для поставщиков хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="ee821-109">Transport providers can set all of the flags except for NOTIFY_NEWMAIL_RECEIVED; only NOTIFY_NEWMAIL_RECEIVED and NOTIFY_READTOSEND are valid for message store providers.</span></span> <span data-ttu-id="ee821-110">Для параметра _ulFlags_ допустимы следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="ee821-110">The following flags are valid for the  _ulFlags_ parameter:</span></span> 
    
<span data-ttu-id="ee821-111">NOTIFY_CONFIG_CHANGE</span><span class="sxs-lookup"><span data-stu-id="ee821-111">NOTIFY_CONFIG_CHANGE</span></span> 
  
> <span data-ttu-id="ee821-112">Регистрация запроса для изменения конфигурации поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="ee821-112">Registers a request to change the transport provider's configuration.</span></span> 
    
<span data-ttu-id="ee821-113">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="ee821-113">NOTIFY_CRITICAL_ERROR</span></span> 
  
> <span data-ttu-id="ee821-114">Неустранимая ошибка поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="ee821-114">An unrecoverable error has occurred to the transport provider.</span></span> <span data-ttu-id="ee821-115">Так как NOTIFY_SENTDEFERRED и NOTIFY_CRITICAL_ERROR параметр _lpvData_ используется для вызовов, поставщика транспорта, эти флаги являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="ee821-115">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter for transport provider calls, these flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="ee821-116">NOTIFY_CRITSEC</span><span class="sxs-lookup"><span data-stu-id="ee821-116">NOTIFY_CRITSEC</span></span> 
  
> <span data-ttu-id="ee821-117">Запрашивает критический раздел для поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="ee821-117">Requests a critical section for the transport provider.</span></span> <span data-ttu-id="ee821-118">Параметр _lpvData_ не определен и должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="ee821-118">The  _lpvData_ parameter is undefined and should be NULL.</span></span> 
    
<span data-ttu-id="ee821-119">NOTIFY_NEWMAIL</span><span class="sxs-lookup"><span data-stu-id="ee821-119">NOTIFY_NEWMAIL</span></span> 
  
> <span data-ttu-id="ee821-120">Диспетчер очереди MAPI следует загрузить любые полученные новые сообщения на следующего доступного времени.</span><span class="sxs-lookup"><span data-stu-id="ee821-120">The MAPI spooler should download any newly received messages at the next available time.</span></span> <span data-ttu-id="ee821-121">Параметр _lpvData_ не определен и необходимо указать значение NULL.</span><span class="sxs-lookup"><span data-stu-id="ee821-121">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="ee821-122">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="ee821-122">NOTIFY_NEWMAIL_RECEIVED</span></span> 
  
> <span data-ttu-id="ee821-123">Новое сообщение было получено, в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="ee821-123">A new message has been received in the message store.</span></span> <span data-ttu-id="ee821-124">Параметр _lpvData_ указывает на структуру [NEWMAIL_NOTIFICATION](newmail_notification.md) , описывающую сообщения.</span><span class="sxs-lookup"><span data-stu-id="ee821-124">The  _lpvData_ parameter points to a [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that describes the message.</span></span> <span data-ttu-id="ee821-125">Этот флаг используется для поставщиков хранилища сообщений, которые тесно связаны с поставщиками транспорта и игнорируется, если поставщик хранения вошел в систему с установленным флагом MAPI_NO_MAIL.</span><span class="sxs-lookup"><span data-stu-id="ee821-125">This flag is used for message store providers that are tightly coupled with transport providers and is ignored if the store provider is logged on with the MAPI_NO_MAIL flag set.</span></span> 
    
<span data-ttu-id="ee821-126">NOTIFY_NONCRIT</span><span class="sxs-lookup"><span data-stu-id="ee821-126">NOTIFY_NONCRIT</span></span> 
  
> <span data-ttu-id="ee821-127">Освобождает критический раздел, полученное с предыдущего вызова **SpoolerNotify** с _ulFlags_ , задайте значение NOTIFY_CRITSEC.</span><span class="sxs-lookup"><span data-stu-id="ee821-127">Releases a critical section that was obtained with a previous call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="ee821-128">Параметр _lpvData_ не определен и необходимо указать значение NULL.</span><span class="sxs-lookup"><span data-stu-id="ee821-128">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="ee821-129">NOTIFY_READYTOSEND</span><span class="sxs-lookup"><span data-stu-id="ee821-129">NOTIFY_READYTOSEND</span></span> 
  
> <span data-ttu-id="ee821-130">Хранилище поставщика транспорта или сообщения готова для отправки сообщений.</span><span class="sxs-lookup"><span data-stu-id="ee821-130">The transport or message store provider is ready to send messages.</span></span> <span data-ttu-id="ee821-131">Параметр _lpvData_ не определен и необходимо указать значение NULL.</span><span class="sxs-lookup"><span data-stu-id="ee821-131">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="ee821-132">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="ee821-132">NOTIFY_SENTDEFERRED</span></span> 
  
> <span data-ttu-id="ee821-133">Теперь будет отправлено сообщение ранее отложенные и поставщика транспорта уведомляться, когда сообщение будет готов для доставки с помощью вызова метода [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="ee821-133">A previously deferred message should now be sent, and the transport provider should be notified when the message is ready to be delivered by using a call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> <span data-ttu-id="ee821-134">Идентификатор записи отложенные сообщения содержится в структуру [SBinary](sbinary.md) , на который указывает _lpvData_.</span><span class="sxs-lookup"><span data-stu-id="ee821-134">The entry identifier of the deferred message is contained in an [SBinary](sbinary.md) structure pointed to by  _lpvData_.</span></span> <span data-ttu-id="ee821-135">Так как NOTIFY_SENTDEFERRED и NOTIFY_CRITICAL_ERROR использовать параметр _lpvData_ , эти флаги являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="ee821-135">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter, these flags are mutually exclusive.</span></span> 
    
 <span data-ttu-id="ee821-136">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="ee821-136">_lpvData_</span></span>
  
> <span data-ttu-id="ee821-137">[in] Указатель на связанных данных, которые применяются к уведомление.</span><span class="sxs-lookup"><span data-stu-id="ee821-137">[in] A pointer to associated data applicable to a notification.</span></span> <span data-ttu-id="ee821-138">Параметр _lpvData_ указывает на допустимый данные только в том случае, если заданы следующие флаги (_lpvData_ имеет значение NULL при _ulFlags_ задано значение других типов уведомлений):</span><span class="sxs-lookup"><span data-stu-id="ee821-138">The  _lpvData_ parameter points to valid data only when the following flags are set (_lpvData_ is NULL when  _ulFlags_ is set to the other notification types):</span></span> 
    
|<span data-ttu-id="ee821-139">**параметр _ulFlags_**</span><span class="sxs-lookup"><span data-stu-id="ee821-139">**_ulFlags_ setting**</span></span>|<span data-ttu-id="ee821-140">**значение _lpvData_**</span><span class="sxs-lookup"><span data-stu-id="ee821-140">**_lpvData_ value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ee821-141">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="ee821-141">NOTIFY_CRITICAL_ERROR</span></span>  <br/> |<span data-ttu-id="ee821-142">Сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="ee821-142">Information about the error.</span></span>  <br/> |
|<span data-ttu-id="ee821-143">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="ee821-143">NOTIFY_NEWMAIL_RECEIVED</span></span>  <br/> |<span data-ttu-id="ee821-144">Структура **NEWMAIL_NOTIFICATION** , содержащая сведения о вновь доставлено сообщение.</span><span class="sxs-lookup"><span data-stu-id="ee821-144">A **NEWMAIL_NOTIFICATION** structure that contains information about the newly delivered message.</span></span>  <br/> |
|<span data-ttu-id="ee821-145">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="ee821-145">NOTIFY_SENTDEFERRED</span></span>  <br/> |<span data-ttu-id="ee821-146">Структура **SBinary** , содержащая идентификатор записи отложенные сообщения.</span><span class="sxs-lookup"><span data-stu-id="ee821-146">An **SBinary** structure that contains the entry identifier of deferred message.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="ee821-147">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7">Return value</span></span>

<span data-ttu-id="ee821-148">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="ee821-148">S_OK</span></span> 
  
> <span data-ttu-id="ee821-149">Уведомление успешно.</span><span class="sxs-lookup"><span data-stu-id="ee821-149">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ee821-150">Замечания</span><span class="sxs-lookup"><span data-stu-id="ee821-150">Remarks</span></span>

<span data-ttu-id="ee821-151">Метод **IMAPISupport::SpoolerNotify** применяется для сообщения хранения и передачи объекты поддержки поставщика.</span><span class="sxs-lookup"><span data-stu-id="ee821-151">The **IMAPISupport::SpoolerNotify** method is implemented for message store and transport provider support objects.</span></span> <span data-ttu-id="ee821-152">Эти поставщики вызов **SpoolerNotify** для уведомления об изменении состояния или запрос на обслуживание диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="ee821-152">These providers call **SpoolerNotify** to notify the MAPI spooler of a change in status or a request for service.</span></span> <span data-ttu-id="ee821-153">**SpoolerNotify** называется главным образом поставщиками транспорта и может быть вызван в любое время во время сеанса.</span><span class="sxs-lookup"><span data-stu-id="ee821-153">**SpoolerNotify** is called primarily by transport providers and may be called at any time during the session.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="ee821-154">Примечания для поставщиками транспорта</span><span class="sxs-lookup"><span data-stu-id="ee821-154">Notes to Transport Providers</span></span>

<span data-ttu-id="ee821-155">При изменении конфигурации поставщика транспорта вызова **SpoolerNotify** и установите _ulFlags_ NOTIFY_CONFIG_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="ee821-155">If you have changed your transport provider configuration, call **SpoolerNotify** and set  _ulFlags_ to NOTIFY_CONFIG_CHANGED.</span></span> <span data-ttu-id="ee821-156">**SpoolerNotify** отвечает путем вызова метода [IXPLogon::AddressTypes](ixplogon-addresstypes.md) для запроса внести изменения в типы поддерживаемых адресов.</span><span class="sxs-lookup"><span data-stu-id="ee821-156">**SpoolerNotify** responds by calling the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to query for a change in supported address types.</span></span> 
  
<span data-ttu-id="ee821-157">При необходимости критического раздела для обеспечения бесперебойный обработки звонков **SpoolerNotify** с _ulFlags_ , задайте значение NOTIFY_CRITSEC.</span><span class="sxs-lookup"><span data-stu-id="ee821-157">If you need a critical section to ensure uninterrupted processing, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="ee821-158">Этот флаг установлен информирует диспетчер очереди MAPI, что она не вызывайте методы [IXPLogon::Idle](ixplogon-idle.md) и [IXPLogon::Poll](ixplogon-poll.md) .</span><span class="sxs-lookup"><span data-stu-id="ee821-158">Setting this flag informs the MAPI spooler that it should not call the [IXPLogon::Idle](ixplogon-idle.md) and [IXPLogon::Poll](ixplogon-poll.md) methods.</span></span> <span data-ttu-id="ee821-159">При наличии критического раздела откройте возврата MAPI_E_BUSY при вызове метода [IMAPIStatus::ValidateState](imapistatus-validatestate.md) .</span><span class="sxs-lookup"><span data-stu-id="ee821-159">While you have a critical section open, return MAPI_E_BUSY whenever the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is called.</span></span> <span data-ttu-id="ee821-160">По окончании критический раздел, сделайте другой вызов **SpoolerNotify** с _ulFlags_ , задайте значение NOTIFY_NONCRIT.</span><span class="sxs-lookup"><span data-stu-id="ee821-160">When you are finished with the critical section, make another call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NONCRIT.</span></span> 
  
<span data-ttu-id="ee821-161">К примеру Если ваш поставщик удаленного транспорта в процессе отправку сообщения, может потребоваться разрешает пользователю указать номер телефона для установления подключения к удаленному.</span><span class="sxs-lookup"><span data-stu-id="ee821-161">For example, if your remote transport provider is in the process of uploading messages, you might need to allow a user to enter a telephone number to establish the remote connection.</span></span> <span data-ttu-id="ee821-162">Прежде чем цикле процедуру диалогового окна следует объявить критический раздел.</span><span class="sxs-lookup"><span data-stu-id="ee821-162">Before you loop through the dialog box procedure, you should declare a critical section.</span></span> <span data-ttu-id="ee821-163">Когда пользователь закрывает диалоговое окно, завершение процедуру диалогового окна, необходимо разблокировать критический раздел.</span><span class="sxs-lookup"><span data-stu-id="ee821-163">When the user closes the dialog box, terminating the dialog box procedure, you should release the critical section.</span></span>
  
<span data-ttu-id="ee821-164">Если _ulFlags_ NOTIFY_CRITICAL_ERROR, диспетчер очереди MAPI не производит дальнейшие вызовы поставщика за исключением до выпуска.</span><span class="sxs-lookup"><span data-stu-id="ee821-164">When you set  _ulFlags_ to NOTIFY_CRITICAL_ERROR, the MAPI spooler makes no further calls to the provider except to release it.</span></span> <span data-ttu-id="ee821-165">При вызове **SpoolerNotify** с NOTIFY_CRITICAL_ERROR задать с помощью методов [IXPLogon::StartMessage](ixplogon-startmessage.md) или [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) возврата со значением соответствующие ошибки из **StartMessage** или ** SubmitMessage ** звонков сразу же после вызова **SpoolerNotify** .</span><span class="sxs-lookup"><span data-stu-id="ee821-165">If you call **SpoolerNotify** with NOTIFY_CRITICAL_ERROR set from the [IXPLogon::StartMessage](ixplogon-startmessage.md) or [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) methods, return with an appropriate error value from the **StartMessage** or ** SubmitMessage ** call immediately after the **SpoolerNotify** call.</span></span> 
  
<span data-ttu-id="ee821-166">Если ваш поставщик транспорта восстановлен из условие, ранее привел к сбою, вызовите **SpoolerNotify** с _ulFlags_ , задайте значение NOTIFY_READYTOSEND.</span><span class="sxs-lookup"><span data-stu-id="ee821-166">If your transport provider recovered from a condition that previously caused it to fail, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_READYTOSEND.</span></span> <span data-ttu-id="ee821-167">Этот флаг указывает, что поставщик снова готовы обрабатывать сообщения.</span><span class="sxs-lookup"><span data-stu-id="ee821-167">This flag indicates that the provider is again ready to handle messages.</span></span> 
  
## <a name="notes-to-message-store-providers"></a><span data-ttu-id="ee821-168">Примечания для поставщиков хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="ee821-168">Notes to Message Store Providers</span></span>

<span data-ttu-id="ee821-169">Вызовите **SpoolerNotify**, передав флаг NOTIFY_READYTOSEND _ulFlags_, прежде чем принять первый звонок на [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) в **IMessage::SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="ee821-169">Call **SpoolerNotify**, passing the NOTIFY_READYTOSEND flag in  _ulFlags_, before you make your first call to [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) in **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="ee821-170">Этот вызов **SpoolerNotify** должно выполняться только один раз за сеанс.</span><span class="sxs-lookup"><span data-stu-id="ee821-170">This call to **SpoolerNotify** needs to be made only once per session.</span></span> 
  
<span data-ttu-id="ee821-171">Если поставщик хранилища сообщений тесно связаны с транспорта поставщика и Вы вызовите **SpoolerNotify** _ulFlags_ имеет значение NOTIFY_NEWMAIL_RECEIVED, диспетчер очереди MAPI откроется новое сообщение и начинает обработку новой функции обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="ee821-171">If your message store provider is tightly coupled with a transport provider and you call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NEWMAIL_RECEIVED, the MAPI spooler opens the new message and begins processing the new message hook function.</span></span> <span data-ttu-id="ee821-172">После завершения обработки очереди MAPI вызывает метод [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) , чтобы сообщить о новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="ee821-172">When processing is complete, the MAPI spooler calls the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method to inform you of your own new message.</span></span> 
  
<span data-ttu-id="ee821-173">Дополнительные сведения о вызове **SpoolerNotify**видеть какие-либо из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="ee821-173">For more information about calling **SpoolerNotify**, see any of the following topics:</span></span>
  
- [<span data-ttu-id="ee821-174">Реализация метода FlushQueues</span><span class="sxs-lookup"><span data-stu-id="ee821-174">Implementing the FlushQueues Method</span></span>](implementing-the-flushqueues-method.md)
    
- [<span data-ttu-id="ee821-175">Взаимодействие с системой буферизации MAPI</span><span class="sxs-lookup"><span data-stu-id="ee821-175">Interacting with the MAPI Spooler</span></span>](interacting-with-the-mapi-spooler.md)
    
- [<span data-ttu-id="ee821-176">Модель приема сообщений</span><span class="sxs-lookup"><span data-stu-id="ee821-176">Message Reception Model</span></span>](message-reception-model.md)
    
## <a name="see-also"></a><span data-ttu-id="ee821-177">См. также</span><span class="sxs-lookup"><span data-stu-id="ee821-177">See also</span></span>



[<span data-ttu-id="ee821-178">IMsgStore::NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="ee821-178">IMsgStore::NotifyNewMail</span></span>](imsgstore-notifynewmail.md)
  
[<span data-ttu-id="ee821-179">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="ee821-179">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="ee821-180">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="ee821-180">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="ee821-181">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ee821-181">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

