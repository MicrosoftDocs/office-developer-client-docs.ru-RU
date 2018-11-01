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
ms.openlocfilehash: 704a556b97f5fd90989641a17afe5a11d127e51b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577172"
---
# <a name="imapisessionadvise"></a><span data-ttu-id="de1d2-103">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="de1d2-103">IMAPISession::Advise</span></span>

  
  
<span data-ttu-id="de1d2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de1d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de1d2-105">Регистрация для получения уведомлений о указанного события, которые влияют на сеанс.</span><span class="sxs-lookup"><span data-stu-id="de1d2-105">Registers to receive notification of specified events that affect the session.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="de1d2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="de1d2-106">Parameters</span></span>

 <span data-ttu-id="de1d2-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="de1d2-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="de1d2-108">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="de1d2-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="de1d2-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="de1d2-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="de1d2-110">[in] Указатель на идентификатор записи адресной книги или объекта хранилища сообщение о том, какие следует создавать уведомления или значение NULL, это означает, что клиент регистрируется для получения уведомлений о событиях, которые влияют на только на сеанс.</span><span class="sxs-lookup"><span data-stu-id="de1d2-110">[in] A pointer to the entry identifier of the address book or message store object about which notifications should be generated, or NULL, which indicates that the client is registering to receive notifications about events that affect only the session.</span></span> 
    
 <span data-ttu-id="de1d2-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="de1d2-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="de1d2-112">[in] Маска значения, которые указывают на тип события уведомлений, которые клиент заинтересована в и должно быть включено в регистрации.</span><span class="sxs-lookup"><span data-stu-id="de1d2-112">[in] A mask of values that indicate the types of notification events that the client is interested in and should be included in the registration.</span></span> <span data-ttu-id="de1d2-113">Если _lpEntryID_ имеет значение NULL, MAPI автоматически регистрирует клиента для событий критическая ошибка, влияющие на только на сеанс.</span><span class="sxs-lookup"><span data-stu-id="de1d2-113">If  _lpEntryID_ is NULL, MAPI automatically registers the client for critical error events that affect only the session.</span></span> <span data-ttu-id="de1d2-114">Если _lpEntryID_ указывает на идентификатор записи, для параметра _ulEventMask_ допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="de1d2-114">When  _lpEntryID_ points to an entry identifier, the following values are valid for the  _ulEventMask_ parameter:</span></span> 
    
<span data-ttu-id="de1d2-115">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="de1d2-115">fnevCriticalError</span></span> 
  
> <span data-ttu-id="de1d2-116">Регистрирует уведомлений о серьезной ошибки, например недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="de1d2-116">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
<span data-ttu-id="de1d2-117">fnevExtended</span><span class="sxs-lookup"><span data-stu-id="de1d2-117">fnevExtended</span></span> 
  
> <span data-ttu-id="de1d2-118">Регистрирует для уведомлений о событиях, характерные для определенного адресной книги или сообщения поставщик хранилища и о сеансе завершение работы.</span><span class="sxs-lookup"><span data-stu-id="de1d2-118">Registers for notifications about events specific to a particular address book or message store provider and about session shut down.</span></span>
    
<span data-ttu-id="de1d2-119">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="de1d2-119">fnevNewMail</span></span> 
  
> <span data-ttu-id="de1d2-120">Регистрирует уведомлений о появлении нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="de1d2-120">Registers for notifications about the arrival of new messages.</span></span> 
    
<span data-ttu-id="de1d2-121">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="de1d2-121">fnevObjectCreated</span></span> 
  
> <span data-ttu-id="de1d2-122">Регистрирует уведомлений о создании нового объекта.</span><span class="sxs-lookup"><span data-stu-id="de1d2-122">Registers for notifications about the creation of a new object.</span></span>
    
<span data-ttu-id="de1d2-123">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="de1d2-123">fnevObjectCopied</span></span>
  
> <span data-ttu-id="de1d2-124">Регистрирует для уведомлений об объекте копируются.</span><span class="sxs-lookup"><span data-stu-id="de1d2-124">Registers for notifications about an object being copied.</span></span>
    
<span data-ttu-id="de1d2-125">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="de1d2-125">fnevObjectDeleted</span></span>
  
> <span data-ttu-id="de1d2-126">Регистрирует для уведомлений об объекте удаляются.</span><span class="sxs-lookup"><span data-stu-id="de1d2-126">Registers for notifications about an object being deleted.</span></span>
    
<span data-ttu-id="de1d2-127">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="de1d2-127">fnevObjectModified</span></span>
  
> <span data-ttu-id="de1d2-128">Регистрирует для уведомлений об объекте изменяется.</span><span class="sxs-lookup"><span data-stu-id="de1d2-128">Registers for notifications about an object being modified.</span></span>
    
<span data-ttu-id="de1d2-129">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="de1d2-129">fnevObjectMoved</span></span>
  
> <span data-ttu-id="de1d2-130">Регистрирует для уведомлений об объекте происходит перемещение.</span><span class="sxs-lookup"><span data-stu-id="de1d2-130">Registers for notifications about an object being moved.</span></span>
    
<span data-ttu-id="de1d2-131">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="de1d2-131">fnevSearchComplete</span></span>
  
> <span data-ttu-id="de1d2-132">Регистрирует для уведомлений о завершении операции поиска.</span><span class="sxs-lookup"><span data-stu-id="de1d2-132">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="de1d2-133">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="de1d2-133">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="de1d2-134">[in] Указатель на объект приемника уведомлений для последующих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="de1d2-134">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="de1d2-135">Этот объект приемника уведомлений должно уже была распределена.</span><span class="sxs-lookup"><span data-stu-id="de1d2-135">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="de1d2-136">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="de1d2-136">_lpulConnection_</span></span>
  
> <span data-ttu-id="de1d2-137">[out] Указатель на ненулевое число, представляющее соединение между вызывающего абонента уведомить объект приемника и сеанса.</span><span class="sxs-lookup"><span data-stu-id="de1d2-137">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="de1d2-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de1d2-138">Return value</span></span>

<span data-ttu-id="de1d2-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="de1d2-139">S_OK</span></span> 
  
> <span data-ttu-id="de1d2-140">Регистрация прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="de1d2-140">The registration was successful.</span></span>
    
<span data-ttu-id="de1d2-141">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="de1d2-141">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="de1d2-142">Идентификатор записи, на который указывает _lpEntryID_ не представляет идентификатор допустимый записи.</span><span class="sxs-lookup"><span data-stu-id="de1d2-142">The entry identifier pointed to by  _lpEntryID_ does not represent a valid entry identifier.</span></span> 
    
<span data-ttu-id="de1d2-143">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="de1d2-143">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="de1d2-144">Поставщик услуг, ответственный за запись идентификатор, на который указывает _lpEntryID_ не поддерживает тип события, указанного в параметре _ulEventMask_ или не поддерживает уведомления.</span><span class="sxs-lookup"><span data-stu-id="de1d2-144">The service provider responsible for the entry identifier pointed to by  _lpEntryID_ either does not support the type of events specified in the  _ulEventMask_ parameter or does not support notification.</span></span> 
    
<span data-ttu-id="de1d2-145">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="de1d2-145">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="de1d2-146">Идентификатор записи, на который указывает _lpEntryID_ не может справиться с любой из поставщиков услуг в профиле.</span><span class="sxs-lookup"><span data-stu-id="de1d2-146">The entry identifier pointed to by  _lpEntryID_ cannot be handled by any of the service providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="de1d2-147">Замечания</span><span class="sxs-lookup"><span data-stu-id="de1d2-147">Remarks</span></span>

<span data-ttu-id="de1d2-148">Метод **IMAPISession::Advise** устанавливает объект приемника, сеанса и (необязательно) поставщика услуг 's рекомендаций соединение между вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="de1d2-148">The **IMAPISession::Advise** method establishes a connection between the caller's advise sink object, the session and, optionally, a service provider.</span></span> <span data-ttu-id="de1d2-149">Это подключение используется для отправки уведомлений на приемник уведомлений, когда один или несколько указанных в параметре _ulEventMask_ событиями на объект, на который указывает _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="de1d2-149">This connection is used to send notifications to the advise sink when one or more events specified in the  _ulEventMask_ parameter occur to the object pointed to by  _lpEntryID_.</span></span> <span data-ttu-id="de1d2-150">Если _lpEntryID_ имеет значение NULL, целевой объект сеанса и отправлять уведомления только для критические ошибки и расширенные события.</span><span class="sxs-lookup"><span data-stu-id="de1d2-150">When  _lpEntryID_ is NULL, the target object is the session and notifications are sent only for critical errors and extended events.</span></span> 
  
<span data-ttu-id="de1d2-151">При _lpEntryID_ указывает идентификатор записей, MAPI вызывает метод **уведомлений** объекта входа в систему, к которой относится к поставщику услуг ответственность.</span><span class="sxs-lookup"><span data-stu-id="de1d2-151">When  _lpEntryID_ points to a valid entry identifier, MAPI calls the **Advise** method of the logon object that belongs to the responsible service provider.</span></span> <span data-ttu-id="de1d2-152">Например если _lpEntryID_ указывает идентификатор записи в список рассылки, MAPI вызывает метод [IABLogon::Advise](iablogon-advise.md) поставщик соответствующие адресной книги.</span><span class="sxs-lookup"><span data-stu-id="de1d2-152">For example, if  _lpEntryID_ points to the entry identifier of a distribution list, MAPI calls the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="de1d2-153">Чтобы отправить уведомление, поставщиком услуг или MAPI вызывает метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) приемник зарегистрированных уведомлений.</span><span class="sxs-lookup"><span data-stu-id="de1d2-153">To send a notification, either the service provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="de1d2-154">Один из параметров в **OnNotify**, уведомления о структуре, содержит сведения, описывающие определенных событий.</span><span class="sxs-lookup"><span data-stu-id="de1d2-154">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="de1d2-155">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="de1d2-155">Notes to callers</span></span>

<span data-ttu-id="de1d2-156">На компьютерах, поддерживающих многопоточной среде вызов **OnNotify** могут также создаваться в любом потоке в любое время.</span><span class="sxs-lookup"><span data-stu-id="de1d2-156">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="de1d2-157">Если вам требуется Software assurance возникновения уведомления только в конкретный момент времени в определенном потоке, вызовите функцию [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) для создания объекта приемник уведомлений, передайте методу **уведомлений** .</span><span class="sxs-lookup"><span data-stu-id="de1d2-157">If you need assurance that notifications will occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to the **Advise** method.</span></span> 
  
<span data-ttu-id="de1d2-158">Чтобы определить, когда вышел клиента, зарегистрируйте уведомления в ваш поставщик услуг, вызвав **уведомлений** с _lpEntryID_ значение NULL, а _cbEntryID_ значение 0.</span><span class="sxs-lookup"><span data-stu-id="de1d2-158">To determine when a client has logged off, register for notifications in your service provider by calling **Advise** with  _lpEntryID_ set to NULL and  _cbEntryID_ set to 0.</span></span> <span data-ttu-id="de1d2-159">В случае выхода из системы, вы получите уведомление о fnevExtended.</span><span class="sxs-lookup"><span data-stu-id="de1d2-159">When the logoff occurs, you will receive an fnevExtended notification.</span></span> 
  
<span data-ttu-id="de1d2-160">После вызова **уведомлений** прошло успешно, и перед [IMAPISession::Unadvise](imapisession-unadvise.md) вызван для отмены регистрации, release объекта приемник уведомлений при отсутствии определенных длительного использования для него.</span><span class="sxs-lookup"><span data-stu-id="de1d2-160">After a call to **Advise** has succeeded and before [IMAPISession::Unadvise](imapisession-unadvise.md) has been called to cancel the registration, release your advise sink object unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="de1d2-161">Общие сведения о процессе уведомления в разделе [Уведомление о событии в MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="de1d2-161">For an overview of the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="de1d2-162">Дополнительные сведения об обработке уведомлений можно [Обработки уведомлений](handling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="de1d2-162">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="de1d2-163">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="de1d2-163">MFCMAPI reference</span></span>

<span data-ttu-id="de1d2-164">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="de1d2-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="de1d2-165">**Файл**</span><span class="sxs-lookup"><span data-stu-id="de1d2-165">**File**</span></span>|<span data-ttu-id="de1d2-166">**Функция**</span><span class="sxs-lookup"><span data-stu-id="de1d2-166">**Function**</span></span>|<span data-ttu-id="de1d2-167">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="de1d2-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="de1d2-168">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="de1d2-168">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="de1d2-169">CBaseDialog::OnNotificationsOn</span><span class="sxs-lookup"><span data-stu-id="de1d2-169">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="de1d2-170">Mfcmapi (en) использует метод **IMAPISession::Advise** для регистрации уведомлений от сеанса.</span><span class="sxs-lookup"><span data-stu-id="de1d2-170">MFCMAPI uses the **IMAPISession::Advise** method to register for notifications against the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="de1d2-171">См. также</span><span class="sxs-lookup"><span data-stu-id="de1d2-171">See also</span></span>



[<span data-ttu-id="de1d2-172">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="de1d2-172">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="de1d2-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="de1d2-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="de1d2-174">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="de1d2-174">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="de1d2-175">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="de1d2-175">IMAPISession::Unadvise</span></span>](imapisession-unadvise.md)
  
[<span data-ttu-id="de1d2-176">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="de1d2-176">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="de1d2-177">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="de1d2-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="de1d2-178">Уведомление о событии в MAPI</span><span class="sxs-lookup"><span data-stu-id="de1d2-178">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)

