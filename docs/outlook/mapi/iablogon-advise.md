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
# <a name="iablogonadvise"></a><span data-ttu-id="f688d-103">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="f688d-103">IABLogon::Advise</span></span>

  
  
<span data-ttu-id="f688d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f688d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f688d-105">Регистрирует вызываемого пользователя для получения уведомлений об указанных событиях, влияющих на контейнер, пользователя обмена сообщениями или список рассылки.</span><span class="sxs-lookup"><span data-stu-id="f688d-105">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="f688d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f688d-106">Parameters</span></span>

 <span data-ttu-id="f688d-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f688d-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="f688d-108">[in] Количествобайтов в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="f688d-108">[in] The count of bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f688d-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="f688d-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="f688d-110">[in] Указатель на идентификатор записи объекта, о котором должны быть созданы уведомления.</span><span class="sxs-lookup"><span data-stu-id="f688d-110">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span>
    
 <span data-ttu-id="f688d-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="f688d-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="f688d-112">[in] Битоваяmas значений, которая указывает типы событий уведомлений, которые интересуют вызываемого и должны быть включены в регистрацию.</span><span class="sxs-lookup"><span data-stu-id="f688d-112">[in] A bitmask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="f688d-113">Существует соответствующая структура [УВЕДОМЛЕНий,](notification.md) связанная с каждым типом события, который содержит сведения о событии.</span><span class="sxs-lookup"><span data-stu-id="f688d-113">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="f688d-114">В следующей таблице перечислены допустимые значения для параметра  _ulEventMask_ и структуры, связанные с каждым значением.</span><span class="sxs-lookup"><span data-stu-id="f688d-114">The following table lists the valid values for the  _ulEventMask_ parameter and the structures associated with each value.</span></span> 
    
|<span data-ttu-id="f688d-115">**Тип события уведомления**</span><span class="sxs-lookup"><span data-stu-id="f688d-115">**Notification event type**</span></span>|<span data-ttu-id="f688d-116">\*\*Соответствующая \*\*структура УВЕДОМЛЕНий\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f688d-116">**Corresponding **NOTIFICATION** structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f688d-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="f688d-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="f688d-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f688d-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="f688d-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="f688d-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="f688d-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f688d-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="f688d-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="f688d-121">**fnevObjectDeleted**</span></span> <br/> |<span data-ttu-id="f688d-122">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="f688d-122">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="f688d-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="f688d-123">**fnevObjectModified**</span></span> <br/> |<span data-ttu-id="f688d-124">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="f688d-124">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="f688d-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="f688d-125">**fnevObjectCopied**</span></span> <br/> |<span data-ttu-id="f688d-126">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="f688d-126">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="f688d-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="f688d-127">**fnevObjectMoved**</span></span> <br/> |<span data-ttu-id="f688d-128">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="f688d-128">**OBJECT_NOTIFICATION**</span></span> <br/> |
   
 <span data-ttu-id="f688d-129">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="f688d-129">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="f688d-130">[in] Указатель на объект приемника рекомендации для получения последующих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f688d-130">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span>
    
 <span data-ttu-id="f688d-131">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="f688d-131">_lpulConnection_</span></span>
  
> <span data-ttu-id="f688d-132">[out] Указатель на неимякое значение, которое представляет регистрацию уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f688d-132">[out] A pointer to a nonzero value that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f688d-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f688d-133">Return value</span></span>

<span data-ttu-id="f688d-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="f688d-134">S_OK</span></span> 
  
> <span data-ttu-id="f688d-135">Регистрация уведомлений прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="f688d-135">The notification registration was successful.</span></span>
    
<span data-ttu-id="f688d-136">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f688d-136">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="f688d-137">Идентификатор записи, переданный в  _параметре lpEntryID,_ не имеет соответствующего формата.</span><span class="sxs-lookup"><span data-stu-id="f688d-137">The entry identifier passed in the  _lpEntryID_ parameter is not in the appropriate format.</span></span> 
    
<span data-ttu-id="f688d-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="f688d-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="f688d-139">Поставщик адресной книги не поддерживает уведомление, возможно, потому, что он не позволяет вносить изменения в свои объекты.</span><span class="sxs-lookup"><span data-stu-id="f688d-139">The address book provider does not support notification, possibly because it does not allow changes to be made to its objects.</span></span>
    
<span data-ttu-id="f688d-140">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f688d-140">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="f688d-141">Поставщик адресной книги не может обрабатывать идентификатор записи, переданный _в lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="f688d-141">The address book provider cannot handle the entry identifier passed in  _lpEntryID_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f688d-142">Примечания</span><span class="sxs-lookup"><span data-stu-id="f688d-142">Remarks</span></span>

<span data-ttu-id="f688d-143">Поставщики адресных книг реализуют метод **IABLogon::Advise** для регистрации вызываемого объекта для получения уведомлений при изменении объекта в одном из контейнеров.</span><span class="sxs-lookup"><span data-stu-id="f688d-143">Address book providers implement the **IABLogon::Advise** method to register the caller to be notified when a change occurs to an object in one of their containers.</span></span> <span data-ttu-id="f688d-144">Звоняющие могут регистрироваться для уведомлений о пользователях сообщений, списках рассылки или целых контейнерах.</span><span class="sxs-lookup"><span data-stu-id="f688d-144">Callers can register for notifications regarding messaging users, distribution lists, or entire containers.</span></span> 
  
<span data-ttu-id="f688d-145">Клиенты обычно звонят [методу IAddrBook::Advise](iaddrbook-advise.md) для регистрации уведомлений адресной книги.</span><span class="sxs-lookup"><span data-stu-id="f688d-145">Clients typically call the [IAddrBook::Advise](iaddrbook-advise.md) method to register for address book notifications.</span></span> <span data-ttu-id="f688d-146">MAPI затем вызывает метод **Advise** поставщика адресной книги, который отвечает за объект, представленный идентификатором записи  _в lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="f688d-146">MAPI then calls the **Advise** method of the address book provider that is responsible for the object represented by the entry identifier in  _lpEntryID_.</span></span>
  
<span data-ttu-id="f688d-147">При изменении объекта, представленного в _ulEventMask,_ происходит вызов метода **OnNotify** приемника консультации, на который указывает _lpAdviseSink._</span><span class="sxs-lookup"><span data-stu-id="f688d-147">When a change occurs to the indicated object of the type represented in  _ulEventMask_, a call is made to the **OnNotify** method of the advise sink pointed to by  _lpAdviseSink_.</span></span> <span data-ttu-id="f688d-148">Данные, переданные в **структуре NOTIFICATION** процедуре **OnNotify,** описывают событие.</span><span class="sxs-lookup"><span data-stu-id="f688d-148">Data passed in the **NOTIFICATION** structure to the **OnNotify** routine describes the event.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f688d-149">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="f688d-149">Notes to implementers</span></span>

<span data-ttu-id="f688d-150">Вы можете поддерживать уведомления с помощью MAPI или без нее.</span><span class="sxs-lookup"><span data-stu-id="f688d-150">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="f688d-151">MAPI имеет три метода объекта поддержки, которые помогают поставщикам услуг реализовать уведомления:</span><span class="sxs-lookup"><span data-stu-id="f688d-151">MAPI has three support object methods to help service providers implement notification:</span></span>
  
- [<span data-ttu-id="f688d-152">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="f688d-152">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
    
- [<span data-ttu-id="f688d-153">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="f688d-153">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)
    
- [<span data-ttu-id="f688d-154">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="f688d-154">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
    
<span data-ttu-id="f688d-155">Если вы выбрали использование методов поддержки MAPI, вызовите **subscribe** при вызове метода **Advise** и отпустите указатель _lpAdviseSink._</span><span class="sxs-lookup"><span data-stu-id="f688d-155">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="f688d-156">Если вы самостоятельно выбрали поддержку уведомления, вызовите метод **AddRef** приемника рекомендации, представленного параметром  _lpAdviseSink,_ чтобы сохранить копию этого указателя.</span><span class="sxs-lookup"><span data-stu-id="f688d-156">If you elect to support notification yourself, call the **AddRef** method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="f688d-157">Сохраните эту копию, пока не будет вызван метод [IABLogon::Unadvise](iablogon-unadvise.md) для отмены регистрации.</span><span class="sxs-lookup"><span data-stu-id="f688d-157">Maintain this copy until your [IABLogon::Unadvise](iablogon-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="f688d-158">Независимо от того, как вы поддерживаете уведомление, назначьте ненулевую номер подключения регистрации уведомления и вернетесь в _параметре lpulConnection._</span><span class="sxs-lookup"><span data-stu-id="f688d-158">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="f688d-159">Не отпускать этот номер подключения, пока не будет вызван метод **Unadvise.**</span><span class="sxs-lookup"><span data-stu-id="f688d-159">Do not release this connection number until the **Unadvise** method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f688d-160">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="f688d-160">Notes to callers</span></span>

<span data-ttu-id="f688d-161">Указатель lpAdviseSink, переданный в параметр  _lpAdviseSink,_ может указать на созданный объект или на созданный с помощью функции [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) mapI.</span><span class="sxs-lookup"><span data-stu-id="f688d-161">The advise sink pointer that you pass in the  _lpAdviseSink_ parameter to **Advise** can point to an object that you have created or that MAPI has created through the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> <span data-ttu-id="f688d-162">Вы можете использовать **HrThisThreadAdviseSink,** если поддерживаете несколько потоков выполнения и хотите убедиться, что последующие вызовы метода **OnNotify** происходят в соответствующее время в соответствующем потоке.</span><span class="sxs-lookup"><span data-stu-id="f688d-162">You might want to use **HrThisThreadAdviseSink** if you support multiple threads of execution and want to be sure that that subsequent calls to your **OnNotify** method occur at an appropriate time on an appropriate thread.</span></span> 
  
<span data-ttu-id="f688d-163">Будьте готовы к тому, что ваш объект-тонконвейдер будет освобожден в любое время после вызова "Сообщить" и до вызова **unadvise.** </span><span class="sxs-lookup"><span data-stu-id="f688d-163">Be prepared for your advise sink object to be released any time after your call to **Advise** and before your call to **Unadvise**.</span></span> <span data-ttu-id="f688d-164">Следовательно, после возврата "Advise"  вам следует освободить объект-тонконсульт, если вы не используете его в течение длительного времени.</span><span class="sxs-lookup"><span data-stu-id="f688d-164">Therefore, you should release your advise sink object after **Advise** returns, unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="f688d-165">Дополнительные сведения о процессе уведомления см. в [уведомлении о событии в MAPI.](event-notification-in-mapi.md)</span><span class="sxs-lookup"><span data-stu-id="f688d-165">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="f688d-166">Сведения об использовании методов **IMAPISupport** для поддержки уведомлений см. в подразделе ["Поддержка уведомлений о событиях".](supporting-event-notification.md)</span><span class="sxs-lookup"><span data-stu-id="f688d-166">For information about how to use the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span> <span data-ttu-id="f688d-167">Дополнительные сведения о многопотооке и MAPI см. в [threading in MAPI.](threading-in-mapi.md)</span><span class="sxs-lookup"><span data-stu-id="f688d-167">For more information about multithreading and MAPI, see [Threading in MAPI](threading-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f688d-168">См. также</span><span class="sxs-lookup"><span data-stu-id="f688d-168">See also</span></span>



[<span data-ttu-id="f688d-169">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="f688d-169">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="f688d-170">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="f688d-170">IABLogon::Unadvise</span></span>](iablogon-unadvise.md)
  
[<span data-ttu-id="f688d-171">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="f688d-171">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="f688d-172">�����������</span><span class="sxs-lookup"><span data-stu-id="f688d-172">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="f688d-173">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f688d-173">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

