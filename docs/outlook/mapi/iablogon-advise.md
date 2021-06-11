---
title: IABLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Advise
api_type:
- COM
ms.assetid: 375d65b1-607d-4e2a-8052-9bcbf08fc2ac
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4ab0e4b023e6af19f650abf421aed122dcc21879
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428230"
---
# <a name="iablogonadvise"></a><span data-ttu-id="2175f-103">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="2175f-103">IABLogon::Advise</span></span>

  
  
<span data-ttu-id="2175f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2175f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2175f-105">Регистрирует вызываемого пользователя для получения уведомления о указанных событиях, затрагивающих контейнер, пользователя обмена сообщениями или список рассылки.</span><span class="sxs-lookup"><span data-stu-id="2175f-105">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="2175f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="2175f-106">Parameters</span></span>

 <span data-ttu-id="2175f-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="2175f-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="2175f-108">[in] Количество bytes в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="2175f-108">[in] The count of bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="2175f-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="2175f-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="2175f-110">[in] Указатель на идентификатор входа объекта, о котором должны быть созданы уведомления.</span><span class="sxs-lookup"><span data-stu-id="2175f-110">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span>
    
 <span data-ttu-id="2175f-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="2175f-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="2175f-112">[in] Битмаска значений, которые указывают типы событий уведомлений, которые вызываемого заинтересована и должна быть включена в регистрацию.</span><span class="sxs-lookup"><span data-stu-id="2175f-112">[in] A bitmask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="2175f-113">Существует соответствующая структура [УВЕДОМЛЕНий,](notification.md) связанная с каждым типом события, которое содержит сведения о событии.</span><span class="sxs-lookup"><span data-stu-id="2175f-113">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="2175f-114">В следующей таблице перечислены допустимые значения для  _параметра ulEventMask_ и структуры, связанные с каждым значением.</span><span class="sxs-lookup"><span data-stu-id="2175f-114">The following table lists the valid values for the  _ulEventMask_ parameter and the structures associated with each value.</span></span> 
    
|<span data-ttu-id="2175f-115">**Тип события уведомлений**</span><span class="sxs-lookup"><span data-stu-id="2175f-115">**Notification event type**</span></span>|<span data-ttu-id="2175f-116">\*\*Соответствующая \*\*структура УВЕДОМЛЕНий\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="2175f-116">**Corresponding **NOTIFICATION** structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2175f-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="2175f-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="2175f-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="2175f-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="2175f-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="2175f-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="2175f-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="2175f-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="2175f-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="2175f-121">**fnevObjectDeleted**</span></span> <br/> |<span data-ttu-id="2175f-122">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="2175f-122">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="2175f-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="2175f-123">**fnevObjectModified**</span></span> <br/> |<span data-ttu-id="2175f-124">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="2175f-124">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="2175f-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="2175f-125">**fnevObjectCopied**</span></span> <br/> |<span data-ttu-id="2175f-126">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="2175f-126">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="2175f-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="2175f-127">**fnevObjectMoved**</span></span> <br/> |<span data-ttu-id="2175f-128">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="2175f-128">**OBJECT_NOTIFICATION**</span></span> <br/> |
   
 <span data-ttu-id="2175f-129">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="2175f-129">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="2175f-130">[in] Указатель на объект раковины для получения последующих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="2175f-130">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span>
    
 <span data-ttu-id="2175f-131">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="2175f-131">_lpulConnection_</span></span>
  
> <span data-ttu-id="2175f-132">[вышел] Указатель на значение nonzero, представляю которое представляет регистрацию уведомлений.</span><span class="sxs-lookup"><span data-stu-id="2175f-132">[out] A pointer to a nonzero value that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2175f-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2175f-133">Return value</span></span>

<span data-ttu-id="2175f-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="2175f-134">S_OK</span></span> 
  
> <span data-ttu-id="2175f-135">Регистрация уведомлений прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="2175f-135">The notification registration was successful.</span></span>
    
<span data-ttu-id="2175f-136">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2175f-136">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="2175f-137">Идентификатор записи, переданный в  _параметре lpEntryID,_ не находится в соответствующем формате.</span><span class="sxs-lookup"><span data-stu-id="2175f-137">The entry identifier passed in the  _lpEntryID_ parameter is not in the appropriate format.</span></span> 
    
<span data-ttu-id="2175f-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="2175f-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="2175f-139">Поставщик адресной книги не поддерживает уведомление, возможно, потому, что оно не позволяет вносить изменения в свои объекты.</span><span class="sxs-lookup"><span data-stu-id="2175f-139">The address book provider does not support notification, possibly because it does not allow changes to be made to its objects.</span></span>
    
<span data-ttu-id="2175f-140">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2175f-140">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="2175f-141">Поставщик адресной книги не может обрабатывать идентификатор записи, переданный _в lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="2175f-141">The address book provider cannot handle the entry identifier passed in  _lpEntryID_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2175f-142">Примечания</span><span class="sxs-lookup"><span data-stu-id="2175f-142">Remarks</span></span>

<span data-ttu-id="2175f-143">Поставщики адресных книг реализуют метод **IABLogon::Advise,** чтобы зарегистрировать вызываемого для уведомления при изменении объекта в одном из контейнеров.</span><span class="sxs-lookup"><span data-stu-id="2175f-143">Address book providers implement the **IABLogon::Advise** method to register the caller to be notified when a change occurs to an object in one of their containers.</span></span> <span data-ttu-id="2175f-144">Звонители могут регистрироваться для уведомлений о пользователях обмена сообщениями, списках рассылки или целых контейнерах.</span><span class="sxs-lookup"><span data-stu-id="2175f-144">Callers can register for notifications regarding messaging users, distribution lists, or entire containers.</span></span> 
  
<span data-ttu-id="2175f-145">Клиенты обычно звонят по [методу IAddrBook::Advise](iaddrbook-advise.md) для регистрации уведомлений адресной книги.</span><span class="sxs-lookup"><span data-stu-id="2175f-145">Clients typically call the [IAddrBook::Advise](iaddrbook-advise.md) method to register for address book notifications.</span></span> <span data-ttu-id="2175f-146">ЗАТЕМ MAPI вызывает метод **Advise** поставщика адресной книги, который отвечает за объект, представленный идентификатором записи _в lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="2175f-146">MAPI then calls the **Advise** method of the address book provider that is responsible for the object represented by the entry identifier in  _lpEntryID_.</span></span>
  
<span data-ttu-id="2175f-147">При изменении указанного объекта типа, представленного в  _ulEventMask,_ в метод **OnNotify** в раковине рекомендации  _указывается lpAdviseSink_.</span><span class="sxs-lookup"><span data-stu-id="2175f-147">When a change occurs to the indicated object of the type represented in  _ulEventMask_, a call is made to the **OnNotify** method of the advise sink pointed to by  _lpAdviseSink_.</span></span> <span data-ttu-id="2175f-148">Данные, переданные в **структуре УВЕДОМЛЕНий** в **рутину OnNotify,** описывают событие.</span><span class="sxs-lookup"><span data-stu-id="2175f-148">Data passed in the **NOTIFICATION** structure to the **OnNotify** routine describes the event.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2175f-149">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="2175f-149">Notes to implementers</span></span>

<span data-ttu-id="2175f-150">Вы можете поддерживать уведомление с помощью MAPI или без нее.</span><span class="sxs-lookup"><span data-stu-id="2175f-150">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="2175f-151">MAPI имеет три метода объектов поддержки, которые помогают поставщикам услуг реализовать уведомление:</span><span class="sxs-lookup"><span data-stu-id="2175f-151">MAPI has three support object methods to help service providers implement notification:</span></span>
  
- [<span data-ttu-id="2175f-152">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="2175f-152">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
    
- [<span data-ttu-id="2175f-153">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="2175f-153">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)
    
- [<span data-ttu-id="2175f-154">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="2175f-154">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
    
<span data-ttu-id="2175f-155">Если вы хотите использовать методы поддержки  MAPI,  позвоните подписаться при вызове метода Advise и отпустите указатель _lpAdviseSink._</span><span class="sxs-lookup"><span data-stu-id="2175f-155">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="2175f-156">Если вы сами хотите поддержать уведомление, позвоните **методу AddRef** раковины рекомендации, представленной параметром  _lpAdviseSink,_ чтобы сохранить копию этого указателя.</span><span class="sxs-lookup"><span data-stu-id="2175f-156">If you elect to support notification yourself, call the **AddRef** method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="2175f-157">Сохраните эту копию, пока не будет вызван метод [IABLogon::Unadvise](iablogon-unadvise.md) для отмены регистрации.</span><span class="sxs-lookup"><span data-stu-id="2175f-157">Maintain this copy until your [IABLogon::Unadvise](iablogon-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="2175f-158">Независимо от того, как вы поддерживаете уведомление, назначьте номер подключения, неподключаемого к уведомлению, и верни его в _параметре lpulConnection._</span><span class="sxs-lookup"><span data-stu-id="2175f-158">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="2175f-159">Не отпустите этот номер подключения до тех пор, пока не будет вызван метод **Unadvise.**</span><span class="sxs-lookup"><span data-stu-id="2175f-159">Do not release this connection number until the **Unadvise** method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2175f-160">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="2175f-160">Notes to callers</span></span>

<span data-ttu-id="2175f-161">Указатель на раковину, который вы передаете в _параметре lpAdviseSink,_ может указать на объект, созданный вами или созданный MAPI с помощью функции [HrThisThreadAdviseSink.](hrthisthreadadvisesink.md) </span><span class="sxs-lookup"><span data-stu-id="2175f-161">The advise sink pointer that you pass in the  _lpAdviseSink_ parameter to **Advise** can point to an object that you have created or that MAPI has created through the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> <span data-ttu-id="2175f-162">Возможно, вы захотите использовать **HrThisThreadAdviseSink,** если поддерживаете несколько потоков выполнения и хотите убедиться, что последующие вызовы в метод **OnNotify** происходят в соответствующее время в соответствующем потоке.</span><span class="sxs-lookup"><span data-stu-id="2175f-162">You might want to use **HrThisThreadAdviseSink** if you support multiple threads of execution and want to be sure that that subsequent calls to your **OnNotify** method occur at an appropriate time on an appropriate thread.</span></span> 
  
<span data-ttu-id="2175f-163">Будьте готовы к тому, что объект раковины  рекомендации будет выпущен в любое время после звонка в Совет и перед вызовом **в Unadvise.**</span><span class="sxs-lookup"><span data-stu-id="2175f-163">Be prepared for your advise sink object to be released any time after your call to **Advise** and before your call to **Unadvise**.</span></span> <span data-ttu-id="2175f-164">Поэтому после возврата рекомендации следует освободить  объект погрузки, если для этого не будет определенного долгосрочного использования.</span><span class="sxs-lookup"><span data-stu-id="2175f-164">Therefore, you should release your advise sink object after **Advise** returns, unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="2175f-165">Дополнительные сведения о процессе уведомления см. в сообщении [события в MAPI.](event-notification-in-mapi.md)</span><span class="sxs-lookup"><span data-stu-id="2175f-165">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="2175f-166">Сведения о том, как использовать методы **IMAPISupport** для поддержки уведомления, см. в сообщении [о поддержке событий.](supporting-event-notification.md)</span><span class="sxs-lookup"><span data-stu-id="2175f-166">For information about how to use the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span> <span data-ttu-id="2175f-167">Дополнительные сведения о многопотоковом и MAPI см. в [ведомости в MAPI.](threading-in-mapi.md)</span><span class="sxs-lookup"><span data-stu-id="2175f-167">For more information about multithreading and MAPI, see [Threading in MAPI](threading-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2175f-168">См. также</span><span class="sxs-lookup"><span data-stu-id="2175f-168">See also</span></span>



[<span data-ttu-id="2175f-169">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="2175f-169">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="2175f-170">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="2175f-170">IABLogon::Unadvise</span></span>](iablogon-unadvise.md)
  
[<span data-ttu-id="2175f-171">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="2175f-171">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="2175f-172">�����������</span><span class="sxs-lookup"><span data-stu-id="2175f-172">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="2175f-173">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2175f-173">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

