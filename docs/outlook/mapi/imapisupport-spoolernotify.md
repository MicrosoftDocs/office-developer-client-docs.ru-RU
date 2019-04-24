---
title: Имаписуппортспулернотифи
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326287"
---
# <a name="imapisupportspoolernotify"></a><span data-ttu-id="4341b-103">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="4341b-103">IMAPISupport::SpoolerNotify</span></span>

  
  
<span data-ttu-id="4341b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4341b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4341b-105">Уведомляет диспетчер очереди MAPI об изменении состояния или запросе службы.</span><span class="sxs-lookup"><span data-stu-id="4341b-105">Notifies the MAPI spooler of a change in status or a request for service.</span></span> 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a><span data-ttu-id="4341b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4341b-106">Parameters</span></span>

 <span data-ttu-id="4341b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4341b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4341b-108">возврата Битовая маска флагов, указывающая тип уведомления.</span><span class="sxs-lookup"><span data-stu-id="4341b-108">[in] A bitmask of flags that indicates the type of notification.</span></span> <span data-ttu-id="4341b-109">Поставщики транспорта могут устанавливать все флаги, кроме НОТИФИ_НЕВМАИЛ_РЕЦЕИВЕД; для поставщиков хранилища сообщений допустимы только НОТИФИ_НЕВМАИЛ_РЕЦЕИВЕД и НОТИФИ_РЕАДТОСЕНД.</span><span class="sxs-lookup"><span data-stu-id="4341b-109">Transport providers can set all of the flags except for NOTIFY_NEWMAIL_RECEIVED; only NOTIFY_NEWMAIL_RECEIVED and NOTIFY_READTOSEND are valid for message store providers.</span></span> <span data-ttu-id="4341b-110">Для параметра _ulFlags_ допустимы следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="4341b-110">The following flags are valid for the  _ulFlags_ parameter:</span></span> 
    
<span data-ttu-id="4341b-111">НОТИФИ_КОНФИГ_ЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="4341b-111">NOTIFY_CONFIG_CHANGE</span></span> 
  
> <span data-ttu-id="4341b-112">Регистрирует запрос на изменение конфигурации поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="4341b-112">Registers a request to change the transport provider's configuration.</span></span> 
    
<span data-ttu-id="4341b-113">НОТИФИ_КРИТИКАЛ_ЕРРОР</span><span class="sxs-lookup"><span data-stu-id="4341b-113">NOTIFY_CRITICAL_ERROR</span></span> 
  
> <span data-ttu-id="4341b-114">В поставщике транспорта произошла неустранимая ошибка.</span><span class="sxs-lookup"><span data-stu-id="4341b-114">An unrecoverable error has occurred to the transport provider.</span></span> <span data-ttu-id="4341b-115">Так как оба НОТИФИ_СЕНТДЕФЕРРЕД и НОТИФИ_КРИТИКАЛ_ЕРРОР используют параметр _лпвдата_ для вызовов поставщика транспорта, эти флаги являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="4341b-115">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter for transport provider calls, these flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="4341b-116">НОТИФИ_КРИТСЕК</span><span class="sxs-lookup"><span data-stu-id="4341b-116">NOTIFY_CRITSEC</span></span> 
  
> <span data-ttu-id="4341b-117">ЗаПрашивает критический раздел для поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="4341b-117">Requests a critical section for the transport provider.</span></span> <span data-ttu-id="4341b-118">Параметр _лпвдата_ не определен и должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="4341b-118">The  _lpvData_ parameter is undefined and should be NULL.</span></span> 
    
<span data-ttu-id="4341b-119">НОТИФИ_НЕВМАИЛ</span><span class="sxs-lookup"><span data-stu-id="4341b-119">NOTIFY_NEWMAIL</span></span> 
  
> <span data-ttu-id="4341b-120">Диспетчер очереди MAPI должен скачать все недавно полученные сообщения в течение следующего доступного времени.</span><span class="sxs-lookup"><span data-stu-id="4341b-120">The MAPI spooler should download any newly received messages at the next available time.</span></span> <span data-ttu-id="4341b-121">Параметр _лпвдата_ не определен и должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="4341b-121">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="4341b-122">НОТИФИ_НЕВМАИЛ_РЕЦЕИВЕД</span><span class="sxs-lookup"><span data-stu-id="4341b-122">NOTIFY_NEWMAIL_RECEIVED</span></span> 
  
> <span data-ttu-id="4341b-123">В хранилище сообщений получено новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="4341b-123">A new message has been received in the message store.</span></span> <span data-ttu-id="4341b-124">Параметр _лпвдата_ указывает на структуру [невмаил_нотификатион](newmail_notification.md) , описывающую сообщение.</span><span class="sxs-lookup"><span data-stu-id="4341b-124">The  _lpvData_ parameter points to a [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that describes the message.</span></span> <span data-ttu-id="4341b-125">Этот флаг используется для поставщиков хранилища сообщений, тесно связанных с поставщиками транспорта, и игнорируется, если поставщик хранилища вошел в систему с установленным флагом МАПИ_НО_МАИЛ.</span><span class="sxs-lookup"><span data-stu-id="4341b-125">This flag is used for message store providers that are tightly coupled with transport providers and is ignored if the store provider is logged on with the MAPI_NO_MAIL flag set.</span></span> 
    
<span data-ttu-id="4341b-126">НОТИФИ_НОНКРИТ</span><span class="sxs-lookup"><span data-stu-id="4341b-126">NOTIFY_NONCRIT</span></span> 
  
> <span data-ttu-id="4341b-127">Освобождает критический раздел, полученный при предыдущем вызове метода **спулернотифи** с _ulFlags_ , установленным в нотифи_критсек.</span><span class="sxs-lookup"><span data-stu-id="4341b-127">Releases a critical section that was obtained with a previous call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="4341b-128">Параметр _лпвдата_ не определен и должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="4341b-128">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="4341b-129">НОТИФИ_РЕАДИТОСЕНД</span><span class="sxs-lookup"><span data-stu-id="4341b-129">NOTIFY_READYTOSEND</span></span> 
  
> <span data-ttu-id="4341b-130">Поставщик транспорта или хранилища сообщений готов к отправке сообщений.</span><span class="sxs-lookup"><span data-stu-id="4341b-130">The transport or message store provider is ready to send messages.</span></span> <span data-ttu-id="4341b-131">Параметр _лпвдата_ не определен и должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="4341b-131">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="4341b-132">НОТИФИ_СЕНТДЕФЕРРЕД</span><span class="sxs-lookup"><span data-stu-id="4341b-132">NOTIFY_SENTDEFERRED</span></span> 
  
> <span data-ttu-id="4341b-133">Ранее отложенное сообщение должно быть отправлено, а поставщик транспорта должен получать уведомления о том, что сообщение готово к доставке, с помощью вызова метода [иксплогон:: субмитмессаже](ixplogon-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="4341b-133">A previously deferred message should now be sent, and the transport provider should be notified when the message is ready to be delivered by using a call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> <span data-ttu-id="4341b-134">Идентификатор записи для отложенного сообщения хранится в структуре [сбинари](sbinary.md) , на которую указывает _лпвдата_.</span><span class="sxs-lookup"><span data-stu-id="4341b-134">The entry identifier of the deferred message is contained in an [SBinary](sbinary.md) structure pointed to by  _lpvData_.</span></span> <span data-ttu-id="4341b-135">Так как оба НОТИФИ_СЕНТДЕФЕРРЕД и НОТИФИ_КРИТИКАЛ_ЕРРОР используют параметр _лпвдата_ , эти флаги являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="4341b-135">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter, these flags are mutually exclusive.</span></span> 
    
 <span data-ttu-id="4341b-136">_Лпвдата_</span><span class="sxs-lookup"><span data-stu-id="4341b-136">_lpvData_</span></span>
  
> <span data-ttu-id="4341b-137">возврата Указатель на связанные данные, которые относятся к уведомлению.</span><span class="sxs-lookup"><span data-stu-id="4341b-137">[in] A pointer to associated data applicable to a notification.</span></span> <span data-ttu-id="4341b-138">Параметр _лпвдата_ указывает на действительные данные только в том случае, если установлены следующие флаги (_ЛПВДАТА_ имеет значение null, если _ulFlags_ задано для других типов уведомлений):</span><span class="sxs-lookup"><span data-stu-id="4341b-138">The  _lpvData_ parameter points to valid data only when the following flags are set (_lpvData_ is NULL when  _ulFlags_ is set to the other notification types):</span></span> 
    
|<span data-ttu-id="4341b-139">**параметр _ulFlags_**</span><span class="sxs-lookup"><span data-stu-id="4341b-139">**_ulFlags_ setting**</span></span>|<span data-ttu-id="4341b-140">**значение _лпвдата_**</span><span class="sxs-lookup"><span data-stu-id="4341b-140">**_lpvData_ value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4341b-141">НОТИФИ_КРИТИКАЛ_ЕРРОР</span><span class="sxs-lookup"><span data-stu-id="4341b-141">NOTIFY_CRITICAL_ERROR</span></span>  <br/> |<span data-ttu-id="4341b-142">Сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="4341b-142">Information about the error.</span></span>  <br/> |
|<span data-ttu-id="4341b-143">НОТИФИ_НЕВМАИЛ_РЕЦЕИВЕД</span><span class="sxs-lookup"><span data-stu-id="4341b-143">NOTIFY_NEWMAIL_RECEIVED</span></span>  <br/> |<span data-ttu-id="4341b-144">Структура **невмаил_нотификатион** , содержащая сведения о новом доставленном сообщении.</span><span class="sxs-lookup"><span data-stu-id="4341b-144">A **NEWMAIL_NOTIFICATION** structure that contains information about the newly delivered message.</span></span>  <br/> |
|<span data-ttu-id="4341b-145">НОТИФИ_СЕНТДЕФЕРРЕД</span><span class="sxs-lookup"><span data-stu-id="4341b-145">NOTIFY_SENTDEFERRED</span></span>  <br/> |<span data-ttu-id="4341b-146">Структура **сбинари** , содержащая идентификатор отложенного сообщения.</span><span class="sxs-lookup"><span data-stu-id="4341b-146">An **SBinary** structure that contains the entry identifier of deferred message.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="4341b-147">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4341b-147">Return value</span></span>

<span data-ttu-id="4341b-148">S_OK</span><span class="sxs-lookup"><span data-stu-id="4341b-148">S_OK</span></span> 
  
> <span data-ttu-id="4341b-149">Уведомление успешно установлено.</span><span class="sxs-lookup"><span data-stu-id="4341b-149">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4341b-150">Замечания</span><span class="sxs-lookup"><span data-stu-id="4341b-150">Remarks</span></span>

<span data-ttu-id="4341b-151">Метод **имаписуппорт:: спулернотифи** реализован для объектов, поддерживающих хранилище сообщений и поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="4341b-151">The **IMAPISupport::SpoolerNotify** method is implemented for message store and transport provider support objects.</span></span> <span data-ttu-id="4341b-152">Эти поставщики вызывают **спулернотифи** , чтобы уведомить Диспетчер очереди MAPI об изменении состояния или запросе службы.</span><span class="sxs-lookup"><span data-stu-id="4341b-152">These providers call **SpoolerNotify** to notify the MAPI spooler of a change in status or a request for service.</span></span> <span data-ttu-id="4341b-153">**Спулернотифи** вызывается преимущественно поставщиками транспорта и может вызываться в любой момент в сеансе.</span><span class="sxs-lookup"><span data-stu-id="4341b-153">**SpoolerNotify** is called primarily by transport providers and may be called at any time during the session.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="4341b-154">Примечания для поставщиков транспорта</span><span class="sxs-lookup"><span data-stu-id="4341b-154">Notes to Transport Providers</span></span>

<span data-ttu-id="4341b-155">Если вы изменили конфигурацию поставщика транспорта, вызовите **спулернотифи** и задайте _ulFlags_ в нотифи_конфиг_чанжед.</span><span class="sxs-lookup"><span data-stu-id="4341b-155">If you have changed your transport provider configuration, call **SpoolerNotify** and set  _ulFlags_ to NOTIFY_CONFIG_CHANGED.</span></span> <span data-ttu-id="4341b-156">**Спулернотифи** отвечает, вызывая метод [Иксплогон:: аддресстипес](ixplogon-addresstypes.md) для запроса изменений в поддерживаемых типах адресов.</span><span class="sxs-lookup"><span data-stu-id="4341b-156">**SpoolerNotify** responds by calling the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to query for a change in supported address types.</span></span> 
  
<span data-ttu-id="4341b-157">Если требуется важный раздел для обеспечения непрерывной обработки, вызовите **спулернотифи** с _ulFlags_ , установленным в нотифи_критсек.</span><span class="sxs-lookup"><span data-stu-id="4341b-157">If you need a critical section to ensure uninterrupted processing, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="4341b-158">Установка этого флага информирует диспетчер очереди MAPI о том, что он не должен вызывать метод [иксплогон:: Idle](ixplogon-idle.md) и [иксплогон::P олл](ixplogon-poll.md) .</span><span class="sxs-lookup"><span data-stu-id="4341b-158">Setting this flag informs the MAPI spooler that it should not call the [IXPLogon::Idle](ixplogon-idle.md) and [IXPLogon::Poll](ixplogon-poll.md) methods.</span></span> <span data-ttu-id="4341b-159">При открытом критическом разделе возвращается МАПИ_Е_БУСИ, когда вызывается метод [имапистатус:: валидатестате](imapistatus-validatestate.md) .</span><span class="sxs-lookup"><span data-stu-id="4341b-159">While you have a critical section open, return MAPI_E_BUSY whenever the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is called.</span></span> <span data-ttu-id="4341b-160">Завершив работу с критическим разделом, выполните еще один вызов **спулернотифи** с _ulFlags_ , установленным в нотифи_нонкрит.</span><span class="sxs-lookup"><span data-stu-id="4341b-160">When you are finished with the critical section, make another call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NONCRIT.</span></span> 
  
<span data-ttu-id="4341b-161">Например, если удаленный поставщик транспорта находится в процессе отправки сообщений, может потребоваться разрешить пользователю ввести номер телефона для установки удаленного подключения.</span><span class="sxs-lookup"><span data-stu-id="4341b-161">For example, if your remote transport provider is in the process of uploading messages, you might need to allow a user to enter a telephone number to establish the remote connection.</span></span> <span data-ttu-id="4341b-162">Перед выполнением цикла обработки диалогового окна необходимо объявить критический раздел.</span><span class="sxs-lookup"><span data-stu-id="4341b-162">Before you loop through the dialog box procedure, you should declare a critical section.</span></span> <span data-ttu-id="4341b-163">Когда пользователь закрывает диалоговое окно, а затем завершает процедуру диалогового окна, необходимо освободить критический раздел.</span><span class="sxs-lookup"><span data-stu-id="4341b-163">When the user closes the dialog box, terminating the dialog box procedure, you should release the critical section.</span></span>
  
<span data-ttu-id="4341b-164">При установке _ulFlags_ в нотифи_критикал_еррор Диспетчер очереди MAPI не выполняет дальнейших вызовов поставщика, кроме его освобождения.</span><span class="sxs-lookup"><span data-stu-id="4341b-164">When you set  _ulFlags_ to NOTIFY_CRITICAL_ERROR, the MAPI spooler makes no further calls to the provider except to release it.</span></span> <span data-ttu-id="4341b-165">При вызове **спулернотифи** с нотифи_критикал_еррор SET из методов [Иксплогон:: стартмессаже](ixplogon-startmessage.md) или [иксплогон:: субмитмессаже](ixplogon-submitmessage.md) возвращается соответствующее значение ошибки из вызова **StartMessage** или \* \* SubmitMessage \* \*. сразу после вызова **спулернотифи** .</span><span class="sxs-lookup"><span data-stu-id="4341b-165">If you call **SpoolerNotify** with NOTIFY_CRITICAL_ERROR set from the [IXPLogon::StartMessage](ixplogon-startmessage.md) or [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) methods, return with an appropriate error value from the **StartMessage** or \*\* SubmitMessage \*\* call immediately after the **SpoolerNotify** call.</span></span> 
  
<span data-ttu-id="4341b-166">Если поставщик транспорта был восстановлен из условия, которое ранее приводило к сбою, вызовите **спулернотифи** с _ulFlags_ , установленным в нотифи_реадитосенд.</span><span class="sxs-lookup"><span data-stu-id="4341b-166">If your transport provider recovered from a condition that previously caused it to fail, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_READYTOSEND.</span></span> <span data-ttu-id="4341b-167">Этот флаг указывает, что поставщик еще раз готов обрабатывать сообщения.</span><span class="sxs-lookup"><span data-stu-id="4341b-167">This flag indicates that the provider is again ready to handle messages.</span></span> 
  
## <a name="notes-to-message-store-providers"></a><span data-ttu-id="4341b-168">Примечания к поставщикам хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="4341b-168">Notes to Message Store Providers</span></span>

<span data-ttu-id="4341b-169">ВыЗовите **спулернотифи**, ПЕРЕДАВ флаг Нотифи_реадитосенд в _ulFlags_, прежде чем выполнять первый вызов [Имаписуппорт::P Репаресубмит](imapisupport-preparesubmit.md) в **iMessage:: субмитмессаже**.</span><span class="sxs-lookup"><span data-stu-id="4341b-169">Call **SpoolerNotify**, passing the NOTIFY_READYTOSEND flag in  _ulFlags_, before you make your first call to [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) in **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="4341b-170">Этот вызов **спулернотифи** должен выполняться только один раз для каждого сеанса.</span><span class="sxs-lookup"><span data-stu-id="4341b-170">This call to **SpoolerNotify** needs to be made only once per session.</span></span> 
  
<span data-ttu-id="4341b-171">Если поставщик хранилища сообщений тесно связан с поставщиком транспорта и вы вызываете **спулернотифи** с параметром _ulFlags_ в нотифи_невмаил_рецеивед, то диспетчер очереди MAPI открывает новое сообщение и начинает обработку новой функции-ловушки сообщения.</span><span class="sxs-lookup"><span data-stu-id="4341b-171">If your message store provider is tightly coupled with a transport provider and you call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NEWMAIL_RECEIVED, the MAPI spooler opens the new message and begins processing the new message hook function.</span></span> <span data-ttu-id="4341b-172">После завершения обработки Диспетчер очереди MAPI вызывает метод [IMsgStore:: нотифиневмаил](imsgstore-notifynewmail.md) для уведомления о новом сообщении.</span><span class="sxs-lookup"><span data-stu-id="4341b-172">When processing is complete, the MAPI spooler calls the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method to inform you of your own new message.</span></span> 
  
<span data-ttu-id="4341b-173">Дополнительные сведения о вызове **спулернотифи**можно найти в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="4341b-173">For more information about calling **SpoolerNotify**, see any of the following topics:</span></span>
  
- [<span data-ttu-id="4341b-174">Реализация метода FlushQueues</span><span class="sxs-lookup"><span data-stu-id="4341b-174">Implementing the FlushQueues Method</span></span>](implementing-the-flushqueues-method.md)
    
- [<span data-ttu-id="4341b-175">Взаимодействие с диспетчером очереди MAPI</span><span class="sxs-lookup"><span data-stu-id="4341b-175">Interacting with the MAPI Spooler</span></span>](interacting-with-the-mapi-spooler.md)
    
- [<span data-ttu-id="4341b-176">Модель приема сообщений</span><span class="sxs-lookup"><span data-stu-id="4341b-176">Message Reception Model</span></span>](message-reception-model.md)
    
## <a name="see-also"></a><span data-ttu-id="4341b-177">См. также</span><span class="sxs-lookup"><span data-stu-id="4341b-177">See also</span></span>



[<span data-ttu-id="4341b-178">IMsgStore::NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="4341b-178">IMsgStore::NotifyNewMail</span></span>](imsgstore-notifynewmail.md)
  
[<span data-ttu-id="4341b-179">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="4341b-179">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="4341b-180">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="4341b-180">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="4341b-181">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4341b-181">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

