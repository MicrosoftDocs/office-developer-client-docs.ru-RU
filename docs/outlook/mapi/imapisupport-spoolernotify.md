---
title: имаписуппортспулернотифи
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
# <a name="imapisupportspoolernotify"></a><span data-ttu-id="a0ec0-103">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="a0ec0-103">IMAPISupport::SpoolerNotify</span></span>

  
  
<span data-ttu-id="a0ec0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0ec0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0ec0-105">Уведомляет диспетчер очереди MAPI об изменении состояния или запросе службы.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-105">Notifies the MAPI spooler of a change in status or a request for service.</span></span> 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a><span data-ttu-id="a0ec0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0ec0-106">Parameters</span></span>

 <span data-ttu-id="a0ec0-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a0ec0-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a0ec0-108">возврата Битовая маска флагов, указывающая тип уведомления.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-108">[in] A bitmask of flags that indicates the type of notification.</span></span> <span data-ttu-id="a0ec0-109">Поставщики транспорта могут устанавливать все флаги, кроме NOTIFY_NEWMAIL_RECEIVED; для поставщиков хранилища сообщений допустимы только NOTIFY_NEWMAIL_RECEIVED и NOTIFY_READTOSEND.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-109">Transport providers can set all of the flags except for NOTIFY_NEWMAIL_RECEIVED; only NOTIFY_NEWMAIL_RECEIVED and NOTIFY_READTOSEND are valid for message store providers.</span></span> <span data-ttu-id="a0ec0-110">Для параметра _ulFlags_ допустимы следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="a0ec0-110">The following flags are valid for the  _ulFlags_ parameter:</span></span> 
    
<span data-ttu-id="a0ec0-111">NOTIFY_CONFIG_CHANGE</span><span class="sxs-lookup"><span data-stu-id="a0ec0-111">NOTIFY_CONFIG_CHANGE</span></span> 
  
> <span data-ttu-id="a0ec0-112">Регистрирует запрос на изменение конфигурации поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-112">Registers a request to change the transport provider's configuration.</span></span> 
    
<span data-ttu-id="a0ec0-113">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="a0ec0-113">NOTIFY_CRITICAL_ERROR</span></span> 
  
> <span data-ttu-id="a0ec0-114">В поставщике транспорта произошла неустранимая ошибка.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-114">An unrecoverable error has occurred to the transport provider.</span></span> <span data-ttu-id="a0ec0-115">Так как как NOTIFY_SENTDEFERRED, так и NOTIFY_CRITICAL_ERROR использовать параметр _лпвдата_ для вызовов поставщика транспорта, эти флаги являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-115">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter for transport provider calls, these flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="a0ec0-116">NOTIFY_CRITSEC</span><span class="sxs-lookup"><span data-stu-id="a0ec0-116">NOTIFY_CRITSEC</span></span> 
  
> <span data-ttu-id="a0ec0-117">Запрашивает критический раздел для поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-117">Requests a critical section for the transport provider.</span></span> <span data-ttu-id="a0ec0-118">Параметр _лпвдата_ не определен и должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-118">The  _lpvData_ parameter is undefined and should be NULL.</span></span> 
    
<span data-ttu-id="a0ec0-119">NOTIFY_NEWMAIL</span><span class="sxs-lookup"><span data-stu-id="a0ec0-119">NOTIFY_NEWMAIL</span></span> 
  
> <span data-ttu-id="a0ec0-120">Диспетчер очереди MAPI должен скачать все недавно полученные сообщения в течение следующего доступного времени.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-120">The MAPI spooler should download any newly received messages at the next available time.</span></span> <span data-ttu-id="a0ec0-121">Параметр _лпвдата_ не определен и должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-121">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="a0ec0-122">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="a0ec0-122">NOTIFY_NEWMAIL_RECEIVED</span></span> 
  
> <span data-ttu-id="a0ec0-123">В хранилище сообщений получено новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-123">A new message has been received in the message store.</span></span> <span data-ttu-id="a0ec0-124">Параметр _лпвдата_ указывает на структуру [NEWMAIL_NOTIFICATION](newmail_notification.md) , описывающую сообщение.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-124">The  _lpvData_ parameter points to a [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that describes the message.</span></span> <span data-ttu-id="a0ec0-125">Этот флаг используется для поставщиков хранилища сообщений, тесно связанных с поставщиками транспорта, и игнорируется, если поставщик услуг хранения вошел в систему с установленным флагом MAPI_NO_MAIL.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-125">This flag is used for message store providers that are tightly coupled with transport providers and is ignored if the store provider is logged on with the MAPI_NO_MAIL flag set.</span></span> 
    
<span data-ttu-id="a0ec0-126">NOTIFY_NONCRIT</span><span class="sxs-lookup"><span data-stu-id="a0ec0-126">NOTIFY_NONCRIT</span></span> 
  
> <span data-ttu-id="a0ec0-127">Освобождает критический раздел, полученный при предыдущем вызове метода **спулернотифи** с _ulFlags_ , установленным на NOTIFY_CRITSEC.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-127">Releases a critical section that was obtained with a previous call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="a0ec0-128">Параметр _лпвдата_ не определен и должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-128">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="a0ec0-129">NOTIFY_READYTOSEND</span><span class="sxs-lookup"><span data-stu-id="a0ec0-129">NOTIFY_READYTOSEND</span></span> 
  
> <span data-ttu-id="a0ec0-130">Поставщик транспорта или хранилища сообщений готов к отправке сообщений.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-130">The transport or message store provider is ready to send messages.</span></span> <span data-ttu-id="a0ec0-131">Параметр _лпвдата_ не определен и должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-131">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="a0ec0-132">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="a0ec0-132">NOTIFY_SENTDEFERRED</span></span> 
  
> <span data-ttu-id="a0ec0-133">Ранее отложенное сообщение должно быть отправлено, а поставщик транспорта должен получать уведомления о том, что сообщение готово к доставке, с помощью вызова метода [иксплогон:: субмитмессаже](ixplogon-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="a0ec0-133">A previously deferred message should now be sent, and the transport provider should be notified when the message is ready to be delivered by using a call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> <span data-ttu-id="a0ec0-134">Идентификатор записи для отложенного сообщения хранится в структуре [сбинари](sbinary.md) , на которую указывает _лпвдата_.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-134">The entry identifier of the deferred message is contained in an [SBinary](sbinary.md) structure pointed to by  _lpvData_.</span></span> <span data-ttu-id="a0ec0-135">Так как как NOTIFY_SENTDEFERRED, так и NOTIFY_CRITICAL_ERROR используют параметр _лпвдата_ , эти флаги являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-135">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter, these flags are mutually exclusive.</span></span> 
    
 <span data-ttu-id="a0ec0-136">_лпвдата_</span><span class="sxs-lookup"><span data-stu-id="a0ec0-136">_lpvData_</span></span>
  
> <span data-ttu-id="a0ec0-137">возврата Указатель на связанные данные, которые относятся к уведомлению.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-137">[in] A pointer to associated data applicable to a notification.</span></span> <span data-ttu-id="a0ec0-138">Параметр _лпвдата_ указывает на действительные данные только в том случае, если установлены следующие флаги (_лпвдата_ имеет значение null, если _ulFlags_ задано для других типов уведомлений):</span><span class="sxs-lookup"><span data-stu-id="a0ec0-138">The  _lpvData_ parameter points to valid data only when the following flags are set (_lpvData_ is NULL when  _ulFlags_ is set to the other notification types):</span></span> 
    
|<span data-ttu-id="a0ec0-139">**параметр _ulFlags_**</span><span class="sxs-lookup"><span data-stu-id="a0ec0-139">**_ulFlags_ setting**</span></span>|<span data-ttu-id="a0ec0-140">**значение _лпвдата_**</span><span class="sxs-lookup"><span data-stu-id="a0ec0-140">**_lpvData_ value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a0ec0-141">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="a0ec0-141">NOTIFY_CRITICAL_ERROR</span></span>  <br/> |<span data-ttu-id="a0ec0-142">Сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-142">Information about the error.</span></span>  <br/> |
|<span data-ttu-id="a0ec0-143">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="a0ec0-143">NOTIFY_NEWMAIL_RECEIVED</span></span>  <br/> |<span data-ttu-id="a0ec0-144">Структура **NEWMAIL_NOTIFICATION** , содержащая сведения о новом доставленном сообщении.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-144">A **NEWMAIL_NOTIFICATION** structure that contains information about the newly delivered message.</span></span>  <br/> |
|<span data-ttu-id="a0ec0-145">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="a0ec0-145">NOTIFY_SENTDEFERRED</span></span>  <br/> |<span data-ttu-id="a0ec0-146">Структура **сбинари** , содержащая идентификатор отложенного сообщения.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-146">An **SBinary** structure that contains the entry identifier of deferred message.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="a0ec0-147">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0ec0-147">Return value</span></span>

<span data-ttu-id="a0ec0-148">S_OK</span><span class="sxs-lookup"><span data-stu-id="a0ec0-148">S_OK</span></span> 
  
> <span data-ttu-id="a0ec0-149">Уведомление успешно установлено.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-149">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a0ec0-150">Примечания</span><span class="sxs-lookup"><span data-stu-id="a0ec0-150">Remarks</span></span>

<span data-ttu-id="a0ec0-151">Метод **имаписуппорт:: спулернотифи** реализован для объектов, поддерживающих хранилище сообщений и поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-151">The **IMAPISupport::SpoolerNotify** method is implemented for message store and transport provider support objects.</span></span> <span data-ttu-id="a0ec0-152">Эти поставщики вызывают **спулернотифи** , чтобы уведомить Диспетчер очереди MAPI об изменении состояния или запросе службы.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-152">These providers call **SpoolerNotify** to notify the MAPI spooler of a change in status or a request for service.</span></span> <span data-ttu-id="a0ec0-153">**Спулернотифи** вызывается преимущественно поставщиками транспорта и может вызываться в любой момент в сеансе.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-153">**SpoolerNotify** is called primarily by transport providers and may be called at any time during the session.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="a0ec0-154">Примечания для поставщиков транспорта</span><span class="sxs-lookup"><span data-stu-id="a0ec0-154">Notes to Transport Providers</span></span>

<span data-ttu-id="a0ec0-155">Если вы изменили конфигурацию поставщика транспорта, вызовите **спулернотифи** и присвойте _ulFlags_ значение NOTIFY_CONFIG_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-155">If you have changed your transport provider configuration, call **SpoolerNotify** and set  _ulFlags_ to NOTIFY_CONFIG_CHANGED.</span></span> <span data-ttu-id="a0ec0-156">**Спулернотифи** отвечает, вызывая метод [Иксплогон:: аддресстипес](ixplogon-addresstypes.md) для запроса изменений в поддерживаемых типах адресов.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-156">**SpoolerNotify** responds by calling the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to query for a change in supported address types.</span></span> 
  
<span data-ttu-id="a0ec0-157">Если требуется важный раздел для обеспечения непрерывной обработки, вызовите **спулернотифи** с _ulFlags_ , установленным на NOTIFY_CRITSEC.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-157">If you need a critical section to ensure uninterrupted processing, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="a0ec0-158">Установка этого флага информирует диспетчер очереди MAPI о том, что он не должен вызывать метод [иксплогон:: Idle](ixplogon-idle.md) и [иксплогон::P олл](ixplogon-poll.md) .</span><span class="sxs-lookup"><span data-stu-id="a0ec0-158">Setting this flag informs the MAPI spooler that it should not call the [IXPLogon::Idle](ixplogon-idle.md) and [IXPLogon::Poll](ixplogon-poll.md) methods.</span></span> <span data-ttu-id="a0ec0-159">При открытом критическом разделе возвращается MAPI_E_BUSY всякий раз, когда вызывается метод [имапистатус:: валидатестате](imapistatus-validatestate.md) .</span><span class="sxs-lookup"><span data-stu-id="a0ec0-159">While you have a critical section open, return MAPI_E_BUSY whenever the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is called.</span></span> <span data-ttu-id="a0ec0-160">Завершив работу с критическим разделом, сделайте еще один вызов **спулернотифи** с _ulFlags_ , установленным на NOTIFY_NONCRIT.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-160">When you are finished with the critical section, make another call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NONCRIT.</span></span> 
  
<span data-ttu-id="a0ec0-161">Например, если удаленный поставщик транспорта находится в процессе отправки сообщений, может потребоваться разрешить пользователю ввести номер телефона для установки удаленного подключения.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-161">For example, if your remote transport provider is in the process of uploading messages, you might need to allow a user to enter a telephone number to establish the remote connection.</span></span> <span data-ttu-id="a0ec0-162">Перед выполнением цикла обработки диалогового окна необходимо объявить критический раздел.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-162">Before you loop through the dialog box procedure, you should declare a critical section.</span></span> <span data-ttu-id="a0ec0-163">Когда пользователь закрывает диалоговое окно, а затем завершает процедуру диалогового окна, необходимо освободить критический раздел.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-163">When the user closes the dialog box, terminating the dialog box procedure, you should release the critical section.</span></span>
  
<span data-ttu-id="a0ec0-164">Если для _ulFlags_ задано значение NOTIFY_CRITICAL_ERROR, диспетчер очереди MAPI не выполняет дальнейших вызовов поставщика, кроме его освобождения.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-164">When you set  _ulFlags_ to NOTIFY_CRITICAL_ERROR, the MAPI spooler makes no further calls to the provider except to release it.</span></span> <span data-ttu-id="a0ec0-165">При вызове **спулернотифи** с набором NOTIFY_CRITICAL_ERROR из [Иксплогон:: стартмессаже](ixplogon-startmessage.md) или [иксплогон:: субмитмессаже](ixplogon-submitmessage.md) методы возвращаются с соответствующим значением ошибки из **стартмессаже** или \* \* субмитмессаже \* \* вызовов сразу после вызова **SpoolerNotify** .</span><span class="sxs-lookup"><span data-stu-id="a0ec0-165">If you call **SpoolerNotify** with NOTIFY_CRITICAL_ERROR set from the [IXPLogon::StartMessage](ixplogon-startmessage.md) or [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) methods, return with an appropriate error value from the **StartMessage** or \*\* SubmitMessage \*\* call immediately after the **SpoolerNotify** call.</span></span> 
  
<span data-ttu-id="a0ec0-166">Если поставщик транспорта был восстановлен из условия, которое ранее приводило к сбою, вызовите **спулернотифи** с параметром _ulFlags_ , для которого задано значение NOTIFY_READYTOSEND.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-166">If your transport provider recovered from a condition that previously caused it to fail, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_READYTOSEND.</span></span> <span data-ttu-id="a0ec0-167">Этот флаг указывает, что поставщик еще раз готов обрабатывать сообщения.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-167">This flag indicates that the provider is again ready to handle messages.</span></span> 
  
## <a name="notes-to-message-store-providers"></a><span data-ttu-id="a0ec0-168">Примечания к поставщикам хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="a0ec0-168">Notes to Message Store Providers</span></span>

<span data-ttu-id="a0ec0-169">Вызовите **спулернотифи**, передав флаг NOTIFY_READYTOSEND в _ulFlags_, прежде чем выполнять первый вызов [Имаписуппорт::P Репаресубмит](imapisupport-preparesubmit.md) в **iMessage:: субмитмессаже**.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-169">Call **SpoolerNotify**, passing the NOTIFY_READYTOSEND flag in  _ulFlags_, before you make your first call to [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) in **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="a0ec0-170">Этот вызов **спулернотифи** должен выполняться только один раз для каждого сеанса.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-170">This call to **SpoolerNotify** needs to be made only once per session.</span></span> 
  
<span data-ttu-id="a0ec0-171">Если поставщик хранилища сообщений тесно связан с поставщиком транспорта и вы вызываете **спулернотифи** с _ulFlags_ , установленным на NOTIFY_NEWMAIL_RECEIVED, то диспетчер очереди MAPI открывает новое сообщение и начинает обработку новой функции-ловушки сообщения.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-171">If your message store provider is tightly coupled with a transport provider and you call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NEWMAIL_RECEIVED, the MAPI spooler opens the new message and begins processing the new message hook function.</span></span> <span data-ttu-id="a0ec0-172">После завершения обработки Диспетчер очереди MAPI вызывает метод [IMsgStore:: нотифиневмаил](imsgstore-notifynewmail.md) для уведомления о новом сообщении.</span><span class="sxs-lookup"><span data-stu-id="a0ec0-172">When processing is complete, the MAPI spooler calls the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method to inform you of your own new message.</span></span> 
  
<span data-ttu-id="a0ec0-173">Дополнительные сведения о вызове **спулернотифи**можно найти в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="a0ec0-173">For more information about calling **SpoolerNotify**, see any of the following topics:</span></span>
  
- [<span data-ttu-id="a0ec0-174">Реализация метода FlushQueues</span><span class="sxs-lookup"><span data-stu-id="a0ec0-174">Implementing the FlushQueues Method</span></span>](implementing-the-flushqueues-method.md)
    
- [<span data-ttu-id="a0ec0-175">Взаимодействие с диспетчером очереди MAPI</span><span class="sxs-lookup"><span data-stu-id="a0ec0-175">Interacting with the MAPI Spooler</span></span>](interacting-with-the-mapi-spooler.md)
    
- [<span data-ttu-id="a0ec0-176">Модель приема сообщений</span><span class="sxs-lookup"><span data-stu-id="a0ec0-176">Message Reception Model</span></span>](message-reception-model.md)
    
## <a name="see-also"></a><span data-ttu-id="a0ec0-177">См. также</span><span class="sxs-lookup"><span data-stu-id="a0ec0-177">See also</span></span>



[<span data-ttu-id="a0ec0-178">IMsgStore::NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="a0ec0-178">IMsgStore::NotifyNewMail</span></span>](imsgstore-notifynewmail.md)
  
[<span data-ttu-id="a0ec0-179">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="a0ec0-179">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="a0ec0-180">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="a0ec0-180">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="a0ec0-181">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a0ec0-181">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

