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
# <a name="imapisessionadvise"></a><span data-ttu-id="c3092-103">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="c3092-103">IMAPISession::Advise</span></span>

  
  
<span data-ttu-id="c3092-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3092-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3092-105">Регистрируется для получения уведомлений об указанных событиях, влияющих на сеанс.</span><span class="sxs-lookup"><span data-stu-id="c3092-105">Registers to receive notification of specified events that affect the session.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="c3092-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3092-106">Parameters</span></span>

 <span data-ttu-id="c3092-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="c3092-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="c3092-108">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="c3092-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="c3092-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="c3092-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="c3092-110">[in] Указатель на идентификатор записи объекта адресной книги или хранения сообщений о том, какие уведомления должны быть созданы, или NULL, что указывает, что клиент регистрируется для получения уведомлений о событиях, влияющих только на сеанс.</span><span class="sxs-lookup"><span data-stu-id="c3092-110">[in] A pointer to the entry identifier of the address book or message store object about which notifications should be generated, or NULL, which indicates that the client is registering to receive notifications about events that affect only the session.</span></span> 
    
 <span data-ttu-id="c3092-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="c3092-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="c3092-112">[in] Маска значений, которые указывают типы событий уведомлений, которые интересуют клиента и должны быть включены в регистрацию.</span><span class="sxs-lookup"><span data-stu-id="c3092-112">[in] A mask of values that indicate the types of notification events that the client is interested in and should be included in the registration.</span></span> <span data-ttu-id="c3092-113">Если  _lpEntryID_ имеет значение NULL, MAPI автоматически регистрирует клиент для критических ошибок, влияющих только на сеанс.</span><span class="sxs-lookup"><span data-stu-id="c3092-113">If  _lpEntryID_ is NULL, MAPI automatically registers the client for critical error events that affect only the session.</span></span> <span data-ttu-id="c3092-114">Если  _lpEntryID_ указывает на идентификатор записи, для параметра  _ulEventMask_ допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c3092-114">When  _lpEntryID_ points to an entry identifier, the following values are valid for the  _ulEventMask_ parameter:</span></span> 
    
<span data-ttu-id="c3092-115">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="c3092-115">fnevCriticalError</span></span> 
  
> <span data-ttu-id="c3092-116">Регистрирует уведомления о серьезных ошибках, например нехватке памяти.</span><span class="sxs-lookup"><span data-stu-id="c3092-116">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
<span data-ttu-id="c3092-117">fnevExtended</span><span class="sxs-lookup"><span data-stu-id="c3092-117">fnevExtended</span></span> 
  
> <span data-ttu-id="c3092-118">Регистрирует уведомления о событиях, характерных для конкретной адресной книги или поставщика store сообщений, а также о закрытии сеанса.</span><span class="sxs-lookup"><span data-stu-id="c3092-118">Registers for notifications about events specific to a particular address book or message store provider and about session shut down.</span></span>
    
<span data-ttu-id="c3092-119">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="c3092-119">fnevNewMail</span></span> 
  
> <span data-ttu-id="c3092-120">Регистрируется для уведомлений о поступлении новых сообщений.</span><span class="sxs-lookup"><span data-stu-id="c3092-120">Registers for notifications about the arrival of new messages.</span></span> 
    
<span data-ttu-id="c3092-121">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="c3092-121">fnevObjectCreated</span></span> 
  
> <span data-ttu-id="c3092-122">Регистрируется для уведомлений о создании нового объекта.</span><span class="sxs-lookup"><span data-stu-id="c3092-122">Registers for notifications about the creation of a new object.</span></span>
    
<span data-ttu-id="c3092-123">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="c3092-123">fnevObjectCopied</span></span>
  
> <span data-ttu-id="c3092-124">Регистрируется для уведомлений об объекте, который копируется.</span><span class="sxs-lookup"><span data-stu-id="c3092-124">Registers for notifications about an object being copied.</span></span>
    
<span data-ttu-id="c3092-125">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="c3092-125">fnevObjectDeleted</span></span>
  
> <span data-ttu-id="c3092-126">Регистрирует уведомления об удаляемом объекте.</span><span class="sxs-lookup"><span data-stu-id="c3092-126">Registers for notifications about an object being deleted.</span></span>
    
<span data-ttu-id="c3092-127">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="c3092-127">fnevObjectModified</span></span>
  
> <span data-ttu-id="c3092-128">Регистрирует уведомления об изменяемом объекте.</span><span class="sxs-lookup"><span data-stu-id="c3092-128">Registers for notifications about an object being modified.</span></span>
    
<span data-ttu-id="c3092-129">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="c3092-129">fnevObjectMoved</span></span>
  
> <span data-ttu-id="c3092-130">Регистрирует уведомления о перемещаемом объекте.</span><span class="sxs-lookup"><span data-stu-id="c3092-130">Registers for notifications about an object being moved.</span></span>
    
<span data-ttu-id="c3092-131">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="c3092-131">fnevSearchComplete</span></span>
  
> <span data-ttu-id="c3092-132">Регистрируется для уведомлений о завершении операции поиска.</span><span class="sxs-lookup"><span data-stu-id="c3092-132">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="c3092-133">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="c3092-133">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="c3092-134">[in] Указатель на объект приемника рекомендации для получения последующих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c3092-134">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="c3092-135">Этот рекомендуемый объект-тоник должен быть уже выделен.</span><span class="sxs-lookup"><span data-stu-id="c3092-135">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="c3092-136">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="c3092-136">_lpulConnection_</span></span>
  
> <span data-ttu-id="c3092-137">[out] Указатель на ненумерный номер, представляющий соединение между объектом-томером консультации вызываемого вызываемого объекта и сеансом.</span><span class="sxs-lookup"><span data-stu-id="c3092-137">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c3092-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c3092-138">Return value</span></span>

<span data-ttu-id="c3092-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="c3092-139">S_OK</span></span> 
  
> <span data-ttu-id="c3092-140">Регистрация прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="c3092-140">The registration was successful.</span></span>
    
<span data-ttu-id="c3092-141">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c3092-141">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="c3092-142">Идентификатор записи, на который указывает  _lpEntryID,_ не представляет допустимый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="c3092-142">The entry identifier pointed to by  _lpEntryID_ does not represent a valid entry identifier.</span></span> 
    
<span data-ttu-id="c3092-143">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="c3092-143">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="c3092-144">Поставщик услуг, отвечающий за идентификатор записи, на который указывает  _lpEntryID,_ либо не поддерживает тип событий, указанный в параметре  _ulEventMask,_ либо не поддерживает уведомление.</span><span class="sxs-lookup"><span data-stu-id="c3092-144">The service provider responsible for the entry identifier pointed to by  _lpEntryID_ either does not support the type of events specified in the  _ulEventMask_ parameter or does not support notification.</span></span> 
    
<span data-ttu-id="c3092-145">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c3092-145">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="c3092-146">Идентификатор записи, на который указывает  _lpEntryID,_ не может быть обработан ни одним из поставщиков служб в профиле.</span><span class="sxs-lookup"><span data-stu-id="c3092-146">The entry identifier pointed to by  _lpEntryID_ cannot be handled by any of the service providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c3092-147">Примечания</span><span class="sxs-lookup"><span data-stu-id="c3092-147">Remarks</span></span>

<span data-ttu-id="c3092-148">Метод **IMAPISession::Advise** устанавливает связь между объектом приемника консультации вызываемого, сеансом и, при желании, поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="c3092-148">The **IMAPISession::Advise** method establishes a connection between the caller's advise sink object, the session and, optionally, a service provider.</span></span> <span data-ttu-id="c3092-149">Это подключение используется для отправки уведомлений в обемник консультации, когда одно или несколько событий, указанных в параметре _ulEventMask,_ происходят в объекте, на который указывает _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="c3092-149">This connection is used to send notifications to the advise sink when one or more events specified in the  _ulEventMask_ parameter occur to the object pointed to by  _lpEntryID_.</span></span> <span data-ttu-id="c3092-150">Если  _lpEntryID_ имеет значение NULL, целевым объектом является сеанс, а уведомления отправляются только при критических ошибках и расширенных событиях.</span><span class="sxs-lookup"><span data-stu-id="c3092-150">When  _lpEntryID_ is NULL, the target object is the session and notifications are sent only for critical errors and extended events.</span></span> 
  
<span data-ttu-id="c3092-151">Когда  _lpEntryID_ указывает на допустимый идентификатор записи, MAPI вызывает метод **Advise** объекта входа, который принадлежит ответственному поставщику услуг.</span><span class="sxs-lookup"><span data-stu-id="c3092-151">When  _lpEntryID_ points to a valid entry identifier, MAPI calls the **Advise** method of the logon object that belongs to the responsible service provider.</span></span> <span data-ttu-id="c3092-152">Например, если  _lpEntryID_ указывает на идентификатор записи списка рассылки, MAPI вызывает метод [IABLogon::Advise](iablogon-advise.md) соответствующего поставщика адресной книги.</span><span class="sxs-lookup"><span data-stu-id="c3092-152">For example, if  _lpEntryID_ points to the entry identifier of a distribution list, MAPI calls the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="c3092-153">Чтобы отправить уведомление, поставщик услуг или MAPI вызывает зарегистрированный метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) зарегистрированного приемника уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c3092-153">To send a notification, either the service provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="c3092-154">Один из параметров **OnNotify**, структура уведомлений, содержит сведения, описывая конкретное событие.</span><span class="sxs-lookup"><span data-stu-id="c3092-154">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="c3092-155">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="c3092-155">Notes to callers</span></span>

<span data-ttu-id="c3092-156">В системах, поддерживаюх несколько потоков выполнения, вызов **OnNotify** также может происходить в любом потоке в любое время.</span><span class="sxs-lookup"><span data-stu-id="c3092-156">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="c3092-157">Если вам нужна уверенность в том, что уведомления будут происходить только в определенное время в определенном потоке, вызовите функцию [HrThisThreadAdviseSink,](hrthisthreadadvisesink.md) чтобы создать объект приемника рекомендации, который вы передаете методу **Advise.**</span><span class="sxs-lookup"><span data-stu-id="c3092-157">If you need assurance that notifications will occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to the **Advise** method.</span></span> 
  
<span data-ttu-id="c3092-158">Чтобы определить, когда клиент выошел из системы, зарегистрируйтесь для уведомлений у поставщика услуг, вызывая advise с _lpEntryID,_ заданным как NULL, а _cbEntryID_ имеет 0. </span><span class="sxs-lookup"><span data-stu-id="c3092-158">To determine when a client has logged off, register for notifications in your service provider by calling **Advise** with  _lpEntryID_ set to NULL and  _cbEntryID_ set to 0.</span></span> <span data-ttu-id="c3092-159">После этого вы получите уведомление fnevExtended.</span><span class="sxs-lookup"><span data-stu-id="c3092-159">When the logoff occurs, you will receive an fnevExtended notification.</span></span> 
  
<span data-ttu-id="c3092-160">После успешного  вызова "Консультация" и до вызова [IMAPISession::Unadvise](imapisession-unadvise.md) для отмены регистрации отпустите объект-конюхн.</span><span class="sxs-lookup"><span data-stu-id="c3092-160">After a call to **Advise** has succeeded and before [IMAPISession::Unadvise](imapisession-unadvise.md) has been called to cancel the registration, release your advise sink object unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="c3092-161">Обзор процесса уведомления см. в уведомлении [о событии в MAPI.](event-notification-in-mapi.md)</span><span class="sxs-lookup"><span data-stu-id="c3092-161">For an overview of the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="c3092-162">Дополнительные сведения об обработке уведомлений см. в [этой теме.](handling-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="c3092-162">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c3092-163">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c3092-163">MFCMAPI reference</span></span>

<span data-ttu-id="c3092-164">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="c3092-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c3092-165">**Файл**</span><span class="sxs-lookup"><span data-stu-id="c3092-165">**File**</span></span>|<span data-ttu-id="c3092-166">**Функция**</span><span class="sxs-lookup"><span data-stu-id="c3092-166">**Function**</span></span>|<span data-ttu-id="c3092-167">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="c3092-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c3092-168">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="c3092-168">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="c3092-169">CBaseDialog::OnNotificationsOn</span><span class="sxs-lookup"><span data-stu-id="c3092-169">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="c3092-170">MFCMAPI использует метод **IMAPISession::Advise** для регистрации уведомлений о сеансе.</span><span class="sxs-lookup"><span data-stu-id="c3092-170">MFCMAPI uses the **IMAPISession::Advise** method to register for notifications against the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c3092-171">См. также</span><span class="sxs-lookup"><span data-stu-id="c3092-171">See also</span></span>



[<span data-ttu-id="c3092-172">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="c3092-172">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="c3092-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="c3092-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="c3092-174">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="c3092-174">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="c3092-175">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="c3092-175">IMAPISession::Unadvise</span></span>](imapisession-unadvise.md)
  
[<span data-ttu-id="c3092-176">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c3092-176">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="c3092-177">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="c3092-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="c3092-178">Уведомление о событии в MAPI</span><span class="sxs-lookup"><span data-stu-id="c3092-178">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)

