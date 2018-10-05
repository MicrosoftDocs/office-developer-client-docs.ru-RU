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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388248"
---
# <a name="imsgstoreadvise"></a><span data-ttu-id="311c3-103">IMsgStore::Advise</span><span class="sxs-lookup"><span data-stu-id="311c3-103">IMsgStore::Advise</span></span>

  
  
<span data-ttu-id="311c3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="311c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="311c3-105">Регистрация для получения уведомлений о указанного события, которые влияют на хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="311c3-105">Registers to receive notification of specified events that affect the message store.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="311c3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="311c3-106">Parameters</span></span>

 <span data-ttu-id="311c3-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="311c3-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="311c3-108">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="311c3-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="311c3-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="311c3-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="311c3-110">[in] Указатель на идентификатор записи папки или сообщения о уведомления, которое будет создан, или **значение null**.</span><span class="sxs-lookup"><span data-stu-id="311c3-110">[in] A pointer to the entry identifier of the folder or message about which notifications should be generated, or **null**.</span></span> <span data-ttu-id="311c3-111">Если _lpEntryID_ имеет значение NULL, **уведомлений** регистрирует уведомлений на хранилище всего сообщения.</span><span class="sxs-lookup"><span data-stu-id="311c3-111">If  _lpEntryID_ is set to NULL, **Advise** registers for notifications on the entire message store.</span></span> 
    
 <span data-ttu-id="311c3-112">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="311c3-112">_ulEventMask_</span></span>
  
> <span data-ttu-id="311c3-113">[in] Маска значения, которые указывают на тип события уведомлений, вызывающего заинтересована в и должно быть включено в регистрации.</span><span class="sxs-lookup"><span data-stu-id="311c3-113">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="311c3-114">Нет соответствующих структура [уведомления](notification.md) , связанные с каждым типом событий, в котором содержатся сведения о событии.</span><span class="sxs-lookup"><span data-stu-id="311c3-114">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="311c3-115">Ниже приведены допустимые значения для параметра _ulEventMask_ :</span><span class="sxs-lookup"><span data-stu-id="311c3-115">The following are valid values for the  _ulEventMask_ parameter:</span></span> 
    
 <span data-ttu-id="311c3-116">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="311c3-116">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="311c3-117">Регистрирует уведомлений о серьезной ошибки, например недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="311c3-117">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="311c3-118">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="311c3-118">_fnevExtended_</span></span>
  
> <span data-ttu-id="311c3-119">Поставщик хранилища регистрирует для уведомлений о событиях, характерные для определенного сообщения.</span><span class="sxs-lookup"><span data-stu-id="311c3-119">Registers for notifications about events specific to the particular message store provider.</span></span>
    
 <span data-ttu-id="311c3-120">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="311c3-120">_fnevNewMail_</span></span>
  
> <span data-ttu-id="311c3-121">Регистрирует уведомлений о появлении нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="311c3-121">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="311c3-122">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="311c3-122">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="311c3-123">Регистрирует уведомлений о создания новой папки или сообщения.</span><span class="sxs-lookup"><span data-stu-id="311c3-123">Registers for notifications about the creation of a new folder or message.</span></span>
    
 <span data-ttu-id="311c3-124">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="311c3-124">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="311c3-125">Регистрирует уведомлений о папке или сообщения от копирования.</span><span class="sxs-lookup"><span data-stu-id="311c3-125">Registers for notifications about a folder or message being copied.</span></span>
    
 <span data-ttu-id="311c3-126">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="311c3-126">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="311c3-127">Регистрирует уведомлений о папке или удаления сообщений.</span><span class="sxs-lookup"><span data-stu-id="311c3-127">Registers for notifications about a folder or message being deleted.</span></span>
    
 <span data-ttu-id="311c3-128">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="311c3-128">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="311c3-129">Регистрирует уведомлений о папке или изменяемого сообщения.</span><span class="sxs-lookup"><span data-stu-id="311c3-129">Registers for notifications about a folder or message being modified.</span></span>
    
 <span data-ttu-id="311c3-130">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="311c3-130">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="311c3-131">Регистрирует уведомлений о папке или перемещения сообщений.</span><span class="sxs-lookup"><span data-stu-id="311c3-131">Registers for notifications about a folder or message being moved.</span></span>
    
 <span data-ttu-id="311c3-132">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="311c3-132">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="311c3-133">Регистрирует для уведомлений о завершении операции поиска.</span><span class="sxs-lookup"><span data-stu-id="311c3-133">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="311c3-134">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="311c3-134">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="311c3-135">[in] Указатель на объект приемника уведомлений для последующих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="311c3-135">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="311c3-136">Этот объект приемника уведомлений должно уже была распределена.</span><span class="sxs-lookup"><span data-stu-id="311c3-136">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="311c3-137">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="311c3-137">_lpulConnection_</span></span>
  
> <span data-ttu-id="311c3-138">[out] Указатель на ненулевое число, представляющее соединение между вызывающего абонента уведомить объект приемника и сеанса.</span><span class="sxs-lookup"><span data-stu-id="311c3-138">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span> 
    
 <span data-ttu-id="311c3-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="311c3-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="311c3-140">[in] Указатель на объект приемника уведомлений для последующих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="311c3-140">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="311c3-141">Этот объект приемника уведомлений должно уже была распределена.</span><span class="sxs-lookup"><span data-stu-id="311c3-141">This advise sink object must have already been allocated.</span></span> 
    
 <span data-ttu-id="311c3-142">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="311c3-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="311c3-143">[out] Указатель на подключение ненулевое число, представляющее соединение между вызывающего абонента уведомить объект приемника и хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="311c3-143">[out] A pointer to a nonzero connection number that represents the connection between the caller's advise sink object and the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="311c3-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="311c3-144">Return value</span></span>

<span data-ttu-id="311c3-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="311c3-145">S_OK</span></span> 
  
> <span data-ttu-id="311c3-146">Регистрация прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="311c3-146">The registration was successful.</span></span>
    
<span data-ttu-id="311c3-147">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="311c3-147">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="311c3-148">Поставщик хранения сообщения не поддерживает регистрации для уведомлений через хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="311c3-148">The message store provider does not support registration for notification through the message store.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="311c3-149">Замечания</span><span class="sxs-lookup"><span data-stu-id="311c3-149">Remarks</span></span>

<span data-ttu-id="311c3-150">Метод **IMsgStore::Advise** устанавливает соединение между вызывающего абонента уведомить объектом приемника и хранилище сообщений или объекта в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="311c3-150">The **IMsgStore::Advise** method establishes a connection between the caller's advise sink object and either the message store or an object in the message store.</span></span> <span data-ttu-id="311c3-151">Это подключение используется для отправки уведомлений на приемник уведомлений, когда один или несколько событий, как указано в параметре _ulEventMask_ , возникающих в объект источника уведомлений.</span><span class="sxs-lookup"><span data-stu-id="311c3-151">This connection is used to send notifications to the advise sink when one or more events, as specified in the  _ulEventMask_ parameter, occur to the advise source object.</span></span> <span data-ttu-id="311c3-152">При параметр _lpEntryID_ указывает идентификатор записей, источник уведомлений — это объект идентификатором этой записи.</span><span class="sxs-lookup"><span data-stu-id="311c3-152">When the  _lpEntryID_ parameter points to a valid entry identifier, the advise source is the object identified by this entry identifier.</span></span> <span data-ttu-id="311c3-153">Когда _lpEntryID_ имеет значение NULL, источник уведомлений — это хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="311c3-153">When  _lpEntryID_ is NULL, the advise source is the message store.</span></span> 
  
<span data-ttu-id="311c3-154">Чтобы отправить уведомление, MAPI или поставщика хранилища сообщений вызывает метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) приемник зарегистрированных уведомлений.</span><span class="sxs-lookup"><span data-stu-id="311c3-154">To send a notification, either the message store provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="311c3-155">Один из параметров в **OnNotify**, уведомления о структуре, содержит сведения, описывающие определенных событий.</span><span class="sxs-lookup"><span data-stu-id="311c3-155">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="311c3-156">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="311c3-156">Notes to implementers</span></span>

<span data-ttu-id="311c3-157">Может поддерживать уведомлений с помощью или без помощи MAPI.</span><span class="sxs-lookup"><span data-stu-id="311c3-157">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="311c3-158">MAPI имеет три метода объекта поддержки за помощь реализации уведомлений поставщиков услуг: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)и [IMAPISupport::Notify](imapisupport-notify.md).</span><span class="sxs-lookup"><span data-stu-id="311c3-158">MAPI has three support object methods for helping service providers implement notification: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md), and [IMAPISupport::Notify](imapisupport-notify.md).</span></span> <span data-ttu-id="311c3-159">Если вы решите использовать методы поддержки MAPI, вызовите **подписки на** при вызове метода **уведомлений** и освобождать указатель _lpAdviseSink_ .</span><span class="sxs-lookup"><span data-stu-id="311c3-159">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="311c3-160">Если для поддержки уведомлений самостоятельно, вызовите метод [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) приемник уведомлений, представленное параметром _lpAdviseSink_ сохранить копию этого указателя.</span><span class="sxs-lookup"><span data-stu-id="311c3-160">If you elect to support notification yourself, call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="311c3-161">Ведение эту копию, пока не будет вызван метод [IMsgStore::Unadvise](imsgstore-unadvise.md) для отмены регистрации.</span><span class="sxs-lookup"><span data-stu-id="311c3-161">Maintain this copy until your [IMsgStore::Unadvise](imsgstore-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="311c3-162">Независимо от того, как вы поддерживаете уведомлений нумерации ненулевое подключения для регистрации уведомлений и вернуть его в параметре _lpulConnection_ .</span><span class="sxs-lookup"><span data-stu-id="311c3-162">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="311c3-163">Не release этот номер подключения, пока **Unadvise** вызван и завершения.</span><span class="sxs-lookup"><span data-stu-id="311c3-163">Do not release this connection number until **Unadvise** has been called and has completed.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="311c3-164">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="311c3-164">Notes to callers</span></span>

<span data-ttu-id="311c3-165">На компьютерах, поддерживающих многопоточной среде вызов **OnNotify** могут также создаваться в любом потоке в любое время.</span><span class="sxs-lookup"><span data-stu-id="311c3-165">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="311c3-166">Если вы должны быть уверенным, уведомления о возникновении только в конкретный момент времени в определенном потоке, вызовите функцию [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) для создания объекта приемник уведомлений, передаваемых в **уведомлений**.</span><span class="sxs-lookup"><span data-stu-id="311c3-166">If you must be assured that notifications occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to **Advise**.</span></span> 
  
<span data-ttu-id="311c3-167">После вызова метода **уведомлений** завершено успешно и прежде **Unadvise** вызван для отмены регистрации, подготовить для объекта приемник уведомлений нужно освободить.</span><span class="sxs-lookup"><span data-stu-id="311c3-167">After a call to **Advise** has succeeded and before **Unadvise** has been called to cancel the registration, be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="311c3-168">Объект приемника уведомлений освобождать после **уведомлений** возвращает при отсутствии определенных длительного использования для него.</span><span class="sxs-lookup"><span data-stu-id="311c3-168">You should release your advise sink object after **Advise** returns unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="311c3-169">Дополнительные сведения о процессе уведомления содержатся в разделе [Уведомление о событии в MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="311c3-169">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="311c3-170">Дополнительные сведения об обработке уведомлений можно [Обработки уведомлений](handling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="311c3-170">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="311c3-171">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="311c3-171">MFCMAPI reference</span></span>

<span data-ttu-id="311c3-172">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="311c3-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="311c3-173">**Файл**</span><span class="sxs-lookup"><span data-stu-id="311c3-173">**File**</span></span>|<span data-ttu-id="311c3-174">**Функция**</span><span class="sxs-lookup"><span data-stu-id="311c3-174">**Function**</span></span>|<span data-ttu-id="311c3-175">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="311c3-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="311c3-176">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="311c3-176">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="311c3-177">CBaseDialog::OnNotificationsOn</span><span class="sxs-lookup"><span data-stu-id="311c3-177">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="311c3-178">Mfcmapi (en) использует метод **IMsgStore::Advise** для регистрации уведомлений на хранилище всего сообщения.</span><span class="sxs-lookup"><span data-stu-id="311c3-178">MFCMAPI uses the **IMsgStore::Advise** method to register for notifications on the entire message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="311c3-179">См. также</span><span class="sxs-lookup"><span data-stu-id="311c3-179">See also</span></span>



[<span data-ttu-id="311c3-180">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="311c3-180">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="311c3-181">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="311c3-181">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="311c3-182">IMsgStore::Unadvise</span><span class="sxs-lookup"><span data-stu-id="311c3-182">IMsgStore::Unadvise</span></span>](imsgstore-unadvise.md)
  
[<span data-ttu-id="311c3-183">�����������</span><span class="sxs-lookup"><span data-stu-id="311c3-183">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="311c3-184">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="311c3-184">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="311c3-185">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="311c3-185">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

