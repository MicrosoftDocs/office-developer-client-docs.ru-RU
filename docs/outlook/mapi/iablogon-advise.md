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
ms.openlocfilehash: ea72a6fd2a22fe87ad63bb9c8fa6c1416d876b66
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564250"
---
# <a name="iablogonadvise"></a><span data-ttu-id="1cb37-103">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="1cb37-103">IABLogon::Advise</span></span>

  
  
<span data-ttu-id="1cb37-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1cb37-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1cb37-105">Регистрирует вызывающего абонента для получения уведомлений о указанного события, которые влияют на container, системы обмена сообщениями пользователя или список рассылки.</span><span class="sxs-lookup"><span data-stu-id="1cb37-105">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="1cb37-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1cb37-106">Parameters</span></span>

 <span data-ttu-id="1cb37-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="1cb37-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="1cb37-108">[in] Число байт в идентификаторе запись указывает параметр _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="1cb37-108">[in] The count of bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="1cb37-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="1cb37-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="1cb37-110">[in] Указатель на идентификатор записи о том, какие следует создавать уведомления объекта.</span><span class="sxs-lookup"><span data-stu-id="1cb37-110">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span>
    
 <span data-ttu-id="1cb37-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="1cb37-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="1cb37-112">[in] Битовая маска значений, которые указывают на тип события уведомлений, вызывающего заинтересована в и должно быть включено в регистрации.</span><span class="sxs-lookup"><span data-stu-id="1cb37-112">[in] A bitmask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="1cb37-113">Нет соответствующих структура [уведомления](notification.md) , связанные с каждым типом событий, в котором содержатся сведения о событии.</span><span class="sxs-lookup"><span data-stu-id="1cb37-113">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="1cb37-114">В следующей таблице приведены допустимые значения для параметра _ulEventMask_ и структуры, связанных с каждой значение.</span><span class="sxs-lookup"><span data-stu-id="1cb37-114">The following table lists the valid values for the  _ulEventMask_ parameter and the structures associated with each value.</span></span> 
    
|<span data-ttu-id="1cb37-115">**Тип события уведомления**</span><span class="sxs-lookup"><span data-stu-id="1cb37-115">**Notification event type**</span></span>|<span data-ttu-id="1cb37-116">\*\*Структура соответствующего \*\*уведомления\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="1cb37-116">**Corresponding **NOTIFICATION** structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1cb37-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="1cb37-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="1cb37-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1cb37-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="1cb37-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="1cb37-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="1cb37-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1cb37-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="1cb37-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="1cb37-121">**fnevObjectDeleted**</span></span> <br/> |<span data-ttu-id="1cb37-122">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="1cb37-122">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="1cb37-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="1cb37-123">**fnevObjectModified**</span></span> <br/> |<span data-ttu-id="1cb37-124">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="1cb37-124">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="1cb37-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="1cb37-125">**fnevObjectCopied**</span></span> <br/> |<span data-ttu-id="1cb37-126">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="1cb37-126">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="1cb37-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="1cb37-127">**fnevObjectMoved**</span></span> <br/> |<span data-ttu-id="1cb37-128">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="1cb37-128">**OBJECT_NOTIFICATION**</span></span> <br/> |
   
 <span data-ttu-id="1cb37-129">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="1cb37-129">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="1cb37-130">[in] Указатель на объект приемника уведомлений для последующих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="1cb37-130">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span>
    
 <span data-ttu-id="1cb37-131">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="1cb37-131">_lpulConnection_</span></span>
  
> <span data-ttu-id="1cb37-132">[out] Указатель на ненулевое значение, представляющее регистрации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="1cb37-132">[out] A pointer to a nonzero value that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1cb37-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1cb37-133">Return value</span></span>

<span data-ttu-id="1cb37-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="1cb37-134">S_OK</span></span> 
  
> <span data-ttu-id="1cb37-135">Уведомление о регистрации прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="1cb37-135">The notification registration was successful.</span></span>
    
<span data-ttu-id="1cb37-136">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1cb37-136">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="1cb37-137">Идентификатор записи, переданной в параметре _lpEntryID_ не находится в соответствующем формате.</span><span class="sxs-lookup"><span data-stu-id="1cb37-137">The entry identifier passed in the  _lpEntryID_ parameter is not in the appropriate format.</span></span> 
    
<span data-ttu-id="1cb37-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="1cb37-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="1cb37-139">Поставщик адресной книги не поддерживает уведомления, возможно, поскольку не позволяет вносить изменения в объекты.</span><span class="sxs-lookup"><span data-stu-id="1cb37-139">The address book provider does not support notification, possibly because it does not allow changes to be made to its objects.</span></span>
    
<span data-ttu-id="1cb37-140">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1cb37-140">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="1cb37-141">Поставщик адресной книги не может обработать идентификатор записи, переданные в _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="1cb37-141">The address book provider cannot handle the entry identifier passed in  _lpEntryID_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1cb37-142">Примечания</span><span class="sxs-lookup"><span data-stu-id="1cb37-142">Remarks</span></span>

<span data-ttu-id="1cb37-143">Метод **IABLogon::Advise** для регистрации звонящего на получение уведомлений при изменении объект в одну из своих контейнеров, реализуемые поставщиками адресных книг.</span><span class="sxs-lookup"><span data-stu-id="1cb37-143">Address book providers implement the **IABLogon::Advise** method to register the caller to be notified when a change occurs to an object in one of their containers.</span></span> <span data-ttu-id="1cb37-144">Вызывающие объекты можно регистрировать для уведомлений о обмена мгновенными сообщениями пользователи, списков рассылки или всей контейнеров.</span><span class="sxs-lookup"><span data-stu-id="1cb37-144">Callers can register for notifications regarding messaging users, distribution lists, or entire containers.</span></span> 
  
<span data-ttu-id="1cb37-145">Клиенты обычно вызов метода [IAddrBook::Advise](iaddrbook-advise.md) для регистрации уведомлений адресной книги.</span><span class="sxs-lookup"><span data-stu-id="1cb37-145">Clients typically call the [IAddrBook::Advise](iaddrbook-advise.md) method to register for address book notifications.</span></span> <span data-ttu-id="1cb37-146">MAPI вызывает метод **уведомлений** поставщик адресной книги, который несет ответственность за объекта, представленного идентификатор записи в _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="1cb37-146">MAPI then calls the **Advise** method of the address book provider that is responsible for the object represented by the entry identifier in  _lpEntryID_.</span></span>
  
<span data-ttu-id="1cb37-147">При изменении на указанный объект типа, представленного в _ulEventMask_, выполняется вызов метода **OnNotify** приемник уведомлений, на который указывает _lpAdviseSink_.</span><span class="sxs-lookup"><span data-stu-id="1cb37-147">When a change occurs to the indicated object of the type represented in  _ulEventMask_, a call is made to the **OnNotify** method of the advise sink pointed to by  _lpAdviseSink_.</span></span> <span data-ttu-id="1cb37-148">Данные, передаваемые в структуре **УВЕДОМЛЕНИЙ** в подпрограмму **OnNotify** описание события.</span><span class="sxs-lookup"><span data-stu-id="1cb37-148">Data passed in the **NOTIFICATION** structure to the **OnNotify** routine describes the event.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1cb37-149">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="1cb37-149">Notes to implementers</span></span>

<span data-ttu-id="1cb37-150">Может поддерживать уведомлений с помощью или без помощи MAPI.</span><span class="sxs-lookup"><span data-stu-id="1cb37-150">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="1cb37-151">MAPI имеет поддержки объект методы, позволяющие реализовать уведомление поставщиков услуг:</span><span class="sxs-lookup"><span data-stu-id="1cb37-151">MAPI has three support object methods to help service providers implement notification:</span></span>
  
- [<span data-ttu-id="1cb37-152">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="1cb37-152">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
    
- [<span data-ttu-id="1cb37-153">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="1cb37-153">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)
    
- [<span data-ttu-id="1cb37-154">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="1cb37-154">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
    
<span data-ttu-id="1cb37-155">Если вы решите использовать методы поддержки MAPI, вызовите **подписки на** при вызове метода **уведомлений** и освобождать указатель _lpAdviseSink_ .</span><span class="sxs-lookup"><span data-stu-id="1cb37-155">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="1cb37-156">Если для поддержки уведомлений самостоятельно, вызовите метод **AddRef** приемник уведомлений, представленное параметром _lpAdviseSink_ сохранить копию этого указателя.</span><span class="sxs-lookup"><span data-stu-id="1cb37-156">If you elect to support notification yourself, call the **AddRef** method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="1cb37-157">Ведение эту копию, пока не будет вызван метод [IABLogon::Unadvise](iablogon-unadvise.md) для отмены регистрации.</span><span class="sxs-lookup"><span data-stu-id="1cb37-157">Maintain this copy until your [IABLogon::Unadvise](iablogon-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="1cb37-158">Независимо от того, как вы поддерживаете уведомлений нумерации ненулевое подключения для регистрации уведомлений и вернуть его в параметре _lpulConnection_ .</span><span class="sxs-lookup"><span data-stu-id="1cb37-158">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="1cb37-159">Не release этот номер подключения до вызова метода **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="1cb37-159">Do not release this connection number until the **Unadvise** method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1cb37-160">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="1cb37-160">Notes to callers</span></span>

<span data-ttu-id="1cb37-161">Объект, которые были созданы или создания MAPI через функцию [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) можно сопоставить указателя приемника уведомлений, передаваемый в параметре _lpAdviseSink_ **уведомлений** .</span><span class="sxs-lookup"><span data-stu-id="1cb37-161">The advise sink pointer that you pass in the  _lpAdviseSink_ parameter to **Advise** can point to an object that you have created or that MAPI has created through the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> <span data-ttu-id="1cb37-162">Можно использовать **HrThisThreadAdviseSink** , если поддержка нескольких потоков выполнения и хотите убедитесь, что последующие вызовы метода **OnNotify** возникают в соответствующее время на соответствующий поток.</span><span class="sxs-lookup"><span data-stu-id="1cb37-162">You might want to use **HrThisThreadAdviseSink** if you support multiple threads of execution and want to be sure that that subsequent calls to your **OnNotify** method occur at an appropriate time on an appropriate thread.</span></span> 
  
<span data-ttu-id="1cb37-163">Подготовить для объекта приемник уведомлений нужно освободить любое время после вызова для **уведомлений** и до обращения к **Unadvise**.</span><span class="sxs-lookup"><span data-stu-id="1cb37-163">Be prepared for your advise sink object to be released any time after your call to **Advise** and before your call to **Unadvise**.</span></span> <span data-ttu-id="1cb37-164">Таким образом необходимо разблокировать объект приемника уведомлений после возвращает **уведомлений** при отсутствии определенных длительного использования для него.</span><span class="sxs-lookup"><span data-stu-id="1cb37-164">Therefore, you should release your advise sink object after **Advise** returns, unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="1cb37-165">Дополнительные сведения о процессе уведомления содержатся в разделе [Уведомление о событии в MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="1cb37-165">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="1cb37-166">Сведения о том, как использовать методы **IMAPISupport** для поддержки уведомлений [Поддержка уведомлений о событиях](supporting-event-notification.md)см.</span><span class="sxs-lookup"><span data-stu-id="1cb37-166">For information about how to use the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span> <span data-ttu-id="1cb37-167">Дополнительные сведения о многопоточность и MAPI, видеть [Threading в MAPI](threading-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="1cb37-167">For more information about multithreading and MAPI, see [Threading in MAPI](threading-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1cb37-168">См. также</span><span class="sxs-lookup"><span data-stu-id="1cb37-168">See also</span></span>



[<span data-ttu-id="1cb37-169">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="1cb37-169">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="1cb37-170">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="1cb37-170">IABLogon::Unadvise</span></span>](iablogon-unadvise.md)
  
[<span data-ttu-id="1cb37-171">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="1cb37-171">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="1cb37-172">�����������</span><span class="sxs-lookup"><span data-stu-id="1cb37-172">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="1cb37-173">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1cb37-173">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

