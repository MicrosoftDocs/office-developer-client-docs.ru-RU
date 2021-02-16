---
title: IMsgStoreAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.Advise
api_type:
- COM
ms.assetid: 8c57e743-a798-4e39-a61a-46dff8b1ac7c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3b4abef731541e308b2c2ebc6f4aaddf4458e257
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317327"
---
# <a name="imsgstoreadvise"></a><span data-ttu-id="5169f-103">IMsgStore::Advise</span><span class="sxs-lookup"><span data-stu-id="5169f-103">IMsgStore::Advise</span></span>

  
  
<span data-ttu-id="5169f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5169f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5169f-105">Регистрируется для получения уведомлений об указанных событиях, влияющих на хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="5169f-105">Registers to receive notification of specified events that affect the message store.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="5169f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5169f-106">Parameters</span></span>

 <span data-ttu-id="5169f-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="5169f-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="5169f-108">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="5169f-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="5169f-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="5169f-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="5169f-110">[in] Указатель на идентификатор записи папки или сообщения о том, какие уведомления должны быть созданы, или **null.**</span><span class="sxs-lookup"><span data-stu-id="5169f-110">[in] A pointer to the entry identifier of the folder or message about which notifications should be generated, or **null**.</span></span> <span data-ttu-id="5169f-111">Если _для lpEntryID_ задано NULL,  советуем регистрировать уведомления во всем хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="5169f-111">If  _lpEntryID_ is set to NULL, **Advise** registers for notifications on the entire message store.</span></span> 
    
 <span data-ttu-id="5169f-112">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="5169f-112">_ulEventMask_</span></span>
  
> <span data-ttu-id="5169f-113">[in] Маска значений, которые указывают типы событий уведомлений, которые интересуют вызываемого и должны быть включены в регистрацию.</span><span class="sxs-lookup"><span data-stu-id="5169f-113">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="5169f-114">Существует соответствующая структура [УВЕДОМЛЕНий,](notification.md) связанная с каждым типом события, который содержит сведения о событии.</span><span class="sxs-lookup"><span data-stu-id="5169f-114">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="5169f-115">Допустимые значения параметра _ulEventMask:_</span><span class="sxs-lookup"><span data-stu-id="5169f-115">The following are valid values for the  _ulEventMask_ parameter:</span></span> 
    
 <span data-ttu-id="5169f-116">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="5169f-116">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="5169f-117">Регистрирует уведомления о серьезных ошибках, например нехватке памяти.</span><span class="sxs-lookup"><span data-stu-id="5169f-117">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="5169f-118">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="5169f-118">_fnevExtended_</span></span>
  
> <span data-ttu-id="5169f-119">Регистрируется для уведомлений о событиях, характерных для конкретного поставщика store сообщений.</span><span class="sxs-lookup"><span data-stu-id="5169f-119">Registers for notifications about events specific to the particular message store provider.</span></span>
    
 <span data-ttu-id="5169f-120">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="5169f-120">_fnevNewMail_</span></span>
  
> <span data-ttu-id="5169f-121">Регистрируется для уведомлений о поступлении новых сообщений.</span><span class="sxs-lookup"><span data-stu-id="5169f-121">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="5169f-122">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="5169f-122">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="5169f-123">Регистрируется для уведомлений о создании новой папки или сообщения.</span><span class="sxs-lookup"><span data-stu-id="5169f-123">Registers for notifications about the creation of a new folder or message.</span></span>
    
 <span data-ttu-id="5169f-124">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="5169f-124">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="5169f-125">Регистрируется для уведомлений о папке или скопировании сообщения.</span><span class="sxs-lookup"><span data-stu-id="5169f-125">Registers for notifications about a folder or message being copied.</span></span>
    
 <span data-ttu-id="5169f-126">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="5169f-126">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="5169f-127">Регистрируется для уведомлений об удаляемой папке или сообщении.</span><span class="sxs-lookup"><span data-stu-id="5169f-127">Registers for notifications about a folder or message being deleted.</span></span>
    
 <span data-ttu-id="5169f-128">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="5169f-128">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="5169f-129">Регистрирует уведомления о папке или изменяемом сообщении.</span><span class="sxs-lookup"><span data-stu-id="5169f-129">Registers for notifications about a folder or message being modified.</span></span>
    
 <span data-ttu-id="5169f-130">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="5169f-130">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="5169f-131">Регистрирует уведомления о перемещаемой папке или сообщении.</span><span class="sxs-lookup"><span data-stu-id="5169f-131">Registers for notifications about a folder or message being moved.</span></span>
    
 <span data-ttu-id="5169f-132">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="5169f-132">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="5169f-133">Регистрируется для уведомлений о завершении операции поиска.</span><span class="sxs-lookup"><span data-stu-id="5169f-133">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="5169f-134">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="5169f-134">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="5169f-135">[in] Указатель на объект приемника рекомендации для получения последующих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="5169f-135">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="5169f-136">Этот рекомендуемый объект-тоник должен быть уже выделен.</span><span class="sxs-lookup"><span data-stu-id="5169f-136">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="5169f-137">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="5169f-137">_lpulConnection_</span></span>
  
> <span data-ttu-id="5169f-138">[out] Указатель на ненумерный номер, представляющий соединение между объектом-томером консультации вызываемого вызываемого объекта и сеансом.</span><span class="sxs-lookup"><span data-stu-id="5169f-138">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span> 
    
 <span data-ttu-id="5169f-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="5169f-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="5169f-140">[in] Указатель на объект приемника рекомендации для получения последующих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="5169f-140">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="5169f-141">Этот рекомендуемый объект-тоник должен быть уже выделен.</span><span class="sxs-lookup"><span data-stu-id="5169f-141">This advise sink object must have already been allocated.</span></span> 
    
 <span data-ttu-id="5169f-142">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="5169f-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="5169f-143">[out] Указатель на ненумеровый номер подключения, представляющий соединение между объектом-сигнальным сигналом вызываемого вызываемого объекта и хранилищем сообщений.</span><span class="sxs-lookup"><span data-stu-id="5169f-143">[out] A pointer to a nonzero connection number that represents the connection between the caller's advise sink object and the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5169f-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5169f-144">Return value</span></span>

<span data-ttu-id="5169f-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="5169f-145">S_OK</span></span> 
  
> <span data-ttu-id="5169f-146">Регистрация прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="5169f-146">The registration was successful.</span></span>
    
<span data-ttu-id="5169f-147">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="5169f-147">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="5169f-148">Поставщик store сообщений не поддерживает регистрацию уведомлений через хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="5169f-148">The message store provider does not support registration for notification through the message store.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5169f-149">Примечания</span><span class="sxs-lookup"><span data-stu-id="5169f-149">Remarks</span></span>

<span data-ttu-id="5169f-150">Метод **IMsgStore::Advise** устанавливает связь между объектом приемника консультации вызываемого объекта и хранилищем сообщений или объектом в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="5169f-150">The **IMsgStore::Advise** method establishes a connection between the caller's advise sink object and either the message store or an object in the message store.</span></span> <span data-ttu-id="5169f-151">Это подключение используется для отправки уведомлений в оконсультантный точек, когда одно или несколько событий, как указано в параметре  _ulEventMask,_ происходят с объектом источника консультации.</span><span class="sxs-lookup"><span data-stu-id="5169f-151">This connection is used to send notifications to the advise sink when one or more events, as specified in the  _ulEventMask_ parameter, occur to the advise source object.</span></span> <span data-ttu-id="5169f-152">Если параметр  _lpEntryID_ указывает на допустимый идентификатор записи, источником рекомендации является объект, определяемой этим идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="5169f-152">When the  _lpEntryID_ parameter points to a valid entry identifier, the advise source is the object identified by this entry identifier.</span></span> <span data-ttu-id="5169f-153">Если  _lpEntryID_ имеет NULL, источником рекомендации является хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="5169f-153">When  _lpEntryID_ is NULL, the advise source is the message store.</span></span> 
  
<span data-ttu-id="5169f-154">Чтобы отправить уведомление, поставщик store сообщений или MAPI вызывает метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) зарегистрированного приемника уведомлений.</span><span class="sxs-lookup"><span data-stu-id="5169f-154">To send a notification, either the message store provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="5169f-155">Один из параметров **OnNotify**, структура уведомлений, содержит сведения, описывая конкретное событие.</span><span class="sxs-lookup"><span data-stu-id="5169f-155">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5169f-156">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="5169f-156">Notes to implementers</span></span>

<span data-ttu-id="5169f-157">Вы можете поддерживать уведомления с помощью MAPI или без нее.</span><span class="sxs-lookup"><span data-stu-id="5169f-157">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="5169f-158">MAPI имеет три метода объекта поддержки для помощи поставщикам услуг в реализации уведомлений: [IMAPISupport::Subscribe,](imapisupport-subscribe.md) [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)и [IMAPISupport::Notify](imapisupport-notify.md).</span><span class="sxs-lookup"><span data-stu-id="5169f-158">MAPI has three support object methods for helping service providers implement notification: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md), and [IMAPISupport::Notify](imapisupport-notify.md).</span></span> <span data-ttu-id="5169f-159">Если вы выбрали использование методов поддержки  MAPI, вызовите subscribe при вызове метода **Advise** и отпустите указатель _lpAdviseSink._</span><span class="sxs-lookup"><span data-stu-id="5169f-159">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="5169f-160">Если вы самостоятельно выбрали поддержку уведомления, вызовите метод [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) приемника консультации, представленного параметром  _lpAdviseSink,_ чтобы сохранить копию этого указателя.</span><span class="sxs-lookup"><span data-stu-id="5169f-160">If you elect to support notification yourself, call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="5169f-161">Сохраните эту копию, пока не будет вызван метод [IMsgStore::Unadvise](imsgstore-unadvise.md) для отмены регистрации.</span><span class="sxs-lookup"><span data-stu-id="5169f-161">Maintain this copy until your [IMsgStore::Unadvise](imsgstore-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="5169f-162">Независимо от того, как вы поддерживаете уведомление, назначьте ненулевой номер подключения регистрации уведомлений и _вернетесь в параметре lpulConnection._</span><span class="sxs-lookup"><span data-stu-id="5169f-162">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="5169f-163">Не отпустите этот номер подключения, пока не будет вызвана и завершена **unadvise.**</span><span class="sxs-lookup"><span data-stu-id="5169f-163">Do not release this connection number until **Unadvise** has been called and has completed.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5169f-164">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="5169f-164">Notes to callers</span></span>

<span data-ttu-id="5169f-165">В системах, поддерживаюх несколько потоков выполнения, вызов **OnNotify** также может происходить в любом потоке в любое время.</span><span class="sxs-lookup"><span data-stu-id="5169f-165">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="5169f-166">Если вы должны быть уверены в том, что уведомления появляются только в определенное время в определенном потоке, вызовите функцию [HrThisThreadAdviseSink,](hrthisthreadadvisesink.md) чтобы создать объект-замещение, передав его в "Совет".</span><span class="sxs-lookup"><span data-stu-id="5169f-166">If you must be assured that notifications occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to **Advise**.</span></span> 
  
<span data-ttu-id="5169f-167">После успешного  вызова "Консультация" и перед вызовом **Unadvise** для отмены регистрации подготовьсь к тому, что объект-токонвейдер консультации будет отпущен.</span><span class="sxs-lookup"><span data-stu-id="5169f-167">After a call to **Advise** has succeeded and before **Unadvise** has been called to cancel the registration, be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="5169f-168">После возврата "Advise"  (Сообщить) вам следует освободить объект-конвессник, если для него не используется определенная долгосрочная версия.</span><span class="sxs-lookup"><span data-stu-id="5169f-168">You should release your advise sink object after **Advise** returns unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="5169f-169">Дополнительные сведения о процессе уведомления см. в [уведомлении о событии в MAPI.](event-notification-in-mapi.md)</span><span class="sxs-lookup"><span data-stu-id="5169f-169">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="5169f-170">Дополнительные сведения об обработке уведомлений см. в [этой теме.](handling-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="5169f-170">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5169f-171">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5169f-171">MFCMAPI reference</span></span>

<span data-ttu-id="5169f-172">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="5169f-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5169f-173">**Файл**</span><span class="sxs-lookup"><span data-stu-id="5169f-173">**File**</span></span>|<span data-ttu-id="5169f-174">**Функция**</span><span class="sxs-lookup"><span data-stu-id="5169f-174">**Function**</span></span>|<span data-ttu-id="5169f-175">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="5169f-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5169f-176">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="5169f-176">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="5169f-177">CBaseDialog::OnNotificationsOn</span><span class="sxs-lookup"><span data-stu-id="5169f-177">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="5169f-178">MFCMAPI использует метод **IMsgStore::Advise** для регистрации уведомлений во всем хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="5169f-178">MFCMAPI uses the **IMsgStore::Advise** method to register for notifications on the entire message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5169f-179">См. также</span><span class="sxs-lookup"><span data-stu-id="5169f-179">See also</span></span>



[<span data-ttu-id="5169f-180">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="5169f-180">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="5169f-181">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="5169f-181">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="5169f-182">IMsgStore::Unadvise</span><span class="sxs-lookup"><span data-stu-id="5169f-182">IMsgStore::Unadvise</span></span>](imsgstore-unadvise.md)
  
[<span data-ttu-id="5169f-183">�����������</span><span class="sxs-lookup"><span data-stu-id="5169f-183">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="5169f-184">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5169f-184">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="5169f-185">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="5169f-185">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

