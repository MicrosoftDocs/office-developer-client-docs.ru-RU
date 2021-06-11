---
title: IMAPISessionAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Advise
api_type:
- COM
ms.assetid: a6a6b6b1-31e2-4899-a5fe-74d5d1c2ccfc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d5d87d7be9cb3524445107e975a298d4afd5bf98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419837"
---
# <a name="imapisessionadvise"></a><span data-ttu-id="67f3e-103">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="67f3e-103">IMAPISession::Advise</span></span>

  
  
<span data-ttu-id="67f3e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67f3e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67f3e-105">Регистрируется для получения уведомления о указанных событиях, влияющих на сеанс.</span><span class="sxs-lookup"><span data-stu-id="67f3e-105">Registers to receive notification of specified events that affect the session.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="67f3e-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="67f3e-106">Parameters</span></span>

 <span data-ttu-id="67f3e-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="67f3e-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="67f3e-108">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="67f3e-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="67f3e-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="67f3e-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="67f3e-110">[in] Указатель на идентификатор записи объекта адресной книги или магазина сообщений о том, какие уведомления должны быть созданы, или NULL, который указывает, что клиент регистрируется для получения уведомлений о событиях, затрагивающих только сеанс.</span><span class="sxs-lookup"><span data-stu-id="67f3e-110">[in] A pointer to the entry identifier of the address book or message store object about which notifications should be generated, or NULL, which indicates that the client is registering to receive notifications about events that affect only the session.</span></span> 
    
 <span data-ttu-id="67f3e-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="67f3e-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="67f3e-112">[in] Маска значений, которые указывают типы событий уведомлений, которые интересуют клиента и должны быть включены в регистрацию.</span><span class="sxs-lookup"><span data-stu-id="67f3e-112">[in] A mask of values that indicate the types of notification events that the client is interested in and should be included in the registration.</span></span> <span data-ttu-id="67f3e-113">Если  _lpEntryID_ является NULL, MAPI автоматически регистрирует клиента для событий критической ошибки, которые влияют только на сеанс.</span><span class="sxs-lookup"><span data-stu-id="67f3e-113">If  _lpEntryID_ is NULL, MAPI automatically registers the client for critical error events that affect only the session.</span></span> <span data-ttu-id="67f3e-114">Если  _lpEntryID_ указывает на идентификатор записи, для  _параметра ulEventMask_ допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="67f3e-114">When  _lpEntryID_ points to an entry identifier, the following values are valid for the  _ulEventMask_ parameter:</span></span> 
    
<span data-ttu-id="67f3e-115">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="67f3e-115">fnevCriticalError</span></span> 
  
> <span data-ttu-id="67f3e-116">Регистрирует уведомления о серьезных ошибках, например о недостаточной памяти.</span><span class="sxs-lookup"><span data-stu-id="67f3e-116">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
<span data-ttu-id="67f3e-117">fnevExtended</span><span class="sxs-lookup"><span data-stu-id="67f3e-117">fnevExtended</span></span> 
  
> <span data-ttu-id="67f3e-118">Регистрирует уведомления о событиях, определенных конкретному поставщику адресной книги или магазина сообщений, а также о закрытии сеанса.</span><span class="sxs-lookup"><span data-stu-id="67f3e-118">Registers for notifications about events specific to a particular address book or message store provider and about session shut down.</span></span>
    
<span data-ttu-id="67f3e-119">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="67f3e-119">fnevNewMail</span></span> 
  
> <span data-ttu-id="67f3e-120">Регистрация уведомлений о прибытии новых сообщений.</span><span class="sxs-lookup"><span data-stu-id="67f3e-120">Registers for notifications about the arrival of new messages.</span></span> 
    
<span data-ttu-id="67f3e-121">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="67f3e-121">fnevObjectCreated</span></span> 
  
> <span data-ttu-id="67f3e-122">Регистрирует уведомления о создании нового объекта.</span><span class="sxs-lookup"><span data-stu-id="67f3e-122">Registers for notifications about the creation of a new object.</span></span>
    
<span data-ttu-id="67f3e-123">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="67f3e-123">fnevObjectCopied</span></span>
  
> <span data-ttu-id="67f3e-124">Регистрация уведомлений о копировании объекта.</span><span class="sxs-lookup"><span data-stu-id="67f3e-124">Registers for notifications about an object being copied.</span></span>
    
<span data-ttu-id="67f3e-125">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="67f3e-125">fnevObjectDeleted</span></span>
  
> <span data-ttu-id="67f3e-126">Регистрация уведомлений об удалении объекта.</span><span class="sxs-lookup"><span data-stu-id="67f3e-126">Registers for notifications about an object being deleted.</span></span>
    
<span data-ttu-id="67f3e-127">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="67f3e-127">fnevObjectModified</span></span>
  
> <span data-ttu-id="67f3e-128">Регистры уведомлений о модифицированном объекте.</span><span class="sxs-lookup"><span data-stu-id="67f3e-128">Registers for notifications about an object being modified.</span></span>
    
<span data-ttu-id="67f3e-129">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="67f3e-129">fnevObjectMoved</span></span>
  
> <span data-ttu-id="67f3e-130">Регистрация уведомлений о перемещении объекта.</span><span class="sxs-lookup"><span data-stu-id="67f3e-130">Registers for notifications about an object being moved.</span></span>
    
<span data-ttu-id="67f3e-131">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="67f3e-131">fnevSearchComplete</span></span>
  
> <span data-ttu-id="67f3e-132">Регистрация уведомлений о завершении операции поиска.</span><span class="sxs-lookup"><span data-stu-id="67f3e-132">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="67f3e-133">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="67f3e-133">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="67f3e-134">[in] Указатель на объект раковины для получения последующих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="67f3e-134">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="67f3e-135">Этот объект по рекомендации должен быть уже выделен.</span><span class="sxs-lookup"><span data-stu-id="67f3e-135">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="67f3e-136">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="67f3e-136">_lpulConnection_</span></span>
  
> <span data-ttu-id="67f3e-137">[вышел] Указатель на номер nonzero, представляющий связь между объектом раковины рекомендации вызываемого звонищего и сеансом.</span><span class="sxs-lookup"><span data-stu-id="67f3e-137">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="67f3e-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="67f3e-138">Return value</span></span>

<span data-ttu-id="67f3e-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="67f3e-139">S_OK</span></span> 
  
> <span data-ttu-id="67f3e-140">Регистрация прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="67f3e-140">The registration was successful.</span></span>
    
<span data-ttu-id="67f3e-141">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="67f3e-141">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="67f3e-142">Идентификатор записи, на который указывает  _lpEntryID,_ не представляет допустимый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="67f3e-142">The entry identifier pointed to by  _lpEntryID_ does not represent a valid entry identifier.</span></span> 
    
<span data-ttu-id="67f3e-143">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="67f3e-143">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="67f3e-144">Поставщик услуг, отвечающий за идентификатор входа, на который указывает  _lpEntryID,_ либо не поддерживает тип событий, указанных в параметре  _ulEventMask,_ либо не поддерживает уведомление.</span><span class="sxs-lookup"><span data-stu-id="67f3e-144">The service provider responsible for the entry identifier pointed to by  _lpEntryID_ either does not support the type of events specified in the  _ulEventMask_ parameter or does not support notification.</span></span> 
    
<span data-ttu-id="67f3e-145">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="67f3e-145">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="67f3e-146">Идентификатор записи, на который указывает  _lpEntryID,_ не может обрабатываться любым из поставщиков услуг в профиле.</span><span class="sxs-lookup"><span data-stu-id="67f3e-146">The entry identifier pointed to by  _lpEntryID_ cannot be handled by any of the service providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="67f3e-147">Примечания</span><span class="sxs-lookup"><span data-stu-id="67f3e-147">Remarks</span></span>

<span data-ttu-id="67f3e-148">Метод **IMAPISession::Advise** устанавливает связь между объектом раковины рекомендации вызываемого, сеансом и, необязательно, поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="67f3e-148">The **IMAPISession::Advise** method establishes a connection between the caller's advise sink object, the session and, optionally, a service provider.</span></span> <span data-ttu-id="67f3e-149">Это подключение используется для отправки уведомлений в раковину рекомендации, когда одно или несколько событий, указанных в параметре _ulEventMask,_ происходят с объектом, на который указывает _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="67f3e-149">This connection is used to send notifications to the advise sink when one or more events specified in the  _ulEventMask_ parameter occur to the object pointed to by  _lpEntryID_.</span></span> <span data-ttu-id="67f3e-150">Если  _lpEntryID_ является NULL, целевым объектом является сеанс, и уведомления отправляются только для критических ошибок и расширенных событий.</span><span class="sxs-lookup"><span data-stu-id="67f3e-150">When  _lpEntryID_ is NULL, the target object is the session and notifications are sent only for critical errors and extended events.</span></span> 
  
<span data-ttu-id="67f3e-151">Когда _lpEntryID_ указывает на допустимый идентификатор  входа, MAPI вызывает метод Advise объекта logon, который принадлежит ответственному поставщику услуг.</span><span class="sxs-lookup"><span data-stu-id="67f3e-151">When  _lpEntryID_ points to a valid entry identifier, MAPI calls the **Advise** method of the logon object that belongs to the responsible service provider.</span></span> <span data-ttu-id="67f3e-152">Например, если  _lpEntryID_ указывает на идентификатор записи списка рассылки, MAPI вызывает метод [IABLogon::Advise](iablogon-advise.md) соответствующего поставщика адресной книги.</span><span class="sxs-lookup"><span data-stu-id="67f3e-152">For example, if  _lpEntryID_ points to the entry identifier of a distribution list, MAPI calls the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="67f3e-153">Чтобы отправить уведомление, поставщик услуг или MAPI вызывает зарегистрированный метод [IMAPIAdviseSink::OnNotify.](imapiadvisesink-onnotify.md)</span><span class="sxs-lookup"><span data-stu-id="67f3e-153">To send a notification, either the service provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="67f3e-154">Один из параметров **OnNotify**, структуры уведомлений, содержит сведения, описывая конкретное событие.</span><span class="sxs-lookup"><span data-stu-id="67f3e-154">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="67f3e-155">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="67f3e-155">Notes to callers</span></span>

<span data-ttu-id="67f3e-156">В системах, поддерживаюх несколько потоков выполнения, вызов **OnNotify** также может происходить в любом потоке в любое время.</span><span class="sxs-lookup"><span data-stu-id="67f3e-156">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="67f3e-157">Если вам нужна уверенность в том, что уведомления будут возникать только в определенное время в определенном потоке, позвоните в функцию [HrThisThreadAdviseSink,](hrthisthreadadvisesink.md) чтобы создать объект-раковину, который вы передаете методу **Advise.**</span><span class="sxs-lookup"><span data-stu-id="67f3e-157">If you need assurance that notifications will occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to the **Advise** method.</span></span> 
  
<span data-ttu-id="67f3e-158">Чтобы определить, когда клиент отключается, зарегистрируйтесь для  уведомлений в поставщике услуг, позвонив в службу Консультирование с набором _lpEntryID_ в NULL и _cbEntryID,_ заданным до 0.</span><span class="sxs-lookup"><span data-stu-id="67f3e-158">To determine when a client has logged off, register for notifications in your service provider by calling **Advise** with  _lpEntryID_ set to NULL and  _cbEntryID_ set to 0.</span></span> <span data-ttu-id="67f3e-159">Когда происходит вход, вы получите уведомление fnevExtended.</span><span class="sxs-lookup"><span data-stu-id="67f3e-159">When the logoff occurs, you will receive an fnevExtended notification.</span></span> 
  
<span data-ttu-id="67f3e-160">После успешного  звонка в совет и до вызова [IMAPISession::Unadvise](imapisession-unadvise.md) для отмены регистрации отпустите объект раковины рекомендации, если для этого не будет определенного долгосрочного использования.</span><span class="sxs-lookup"><span data-stu-id="67f3e-160">After a call to **Advise** has succeeded and before [IMAPISession::Unadvise](imapisession-unadvise.md) has been called to cancel the registration, release your advise sink object unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="67f3e-161">Обзор процесса уведомлений см. в [примере Event Notification in MAPI.](event-notification-in-mapi.md)</span><span class="sxs-lookup"><span data-stu-id="67f3e-161">For an overview of the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="67f3e-162">Дополнительные сведения об обработке уведомлений см. в [сообщении Handling Notifications.](handling-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="67f3e-162">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="67f3e-163">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="67f3e-163">MFCMAPI reference</span></span>

<span data-ttu-id="67f3e-164">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="67f3e-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="67f3e-165">**Файл**</span><span class="sxs-lookup"><span data-stu-id="67f3e-165">**File**</span></span>|<span data-ttu-id="67f3e-166">**Функция**</span><span class="sxs-lookup"><span data-stu-id="67f3e-166">**Function**</span></span>|<span data-ttu-id="67f3e-167">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="67f3e-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="67f3e-168">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="67f3e-168">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="67f3e-169">CBaseDialog::OnNotificationsOn</span><span class="sxs-lookup"><span data-stu-id="67f3e-169">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="67f3e-170">MFCMAPI использует **метод IMAPISession::Advise** для регистрации уведомлений о сеансе.</span><span class="sxs-lookup"><span data-stu-id="67f3e-170">MFCMAPI uses the **IMAPISession::Advise** method to register for notifications against the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="67f3e-171">См. также</span><span class="sxs-lookup"><span data-stu-id="67f3e-171">See also</span></span>



[<span data-ttu-id="67f3e-172">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="67f3e-172">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="67f3e-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="67f3e-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="67f3e-174">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="67f3e-174">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="67f3e-175">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="67f3e-175">IMAPISession::Unadvise</span></span>](imapisession-unadvise.md)
  
[<span data-ttu-id="67f3e-176">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="67f3e-176">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="67f3e-177">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="67f3e-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="67f3e-178">Уведомление о событиях в MAPI</span><span class="sxs-lookup"><span data-stu-id="67f3e-178">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)

