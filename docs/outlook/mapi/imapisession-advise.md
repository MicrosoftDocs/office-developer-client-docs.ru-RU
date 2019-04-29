---
title: Имаписессионадвисе
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
# <a name="imapisessionadvise"></a><span data-ttu-id="b357c-103">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="b357c-103">IMAPISession::Advise</span></span>

  
  
<span data-ttu-id="b357c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b357c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b357c-105">Регистрируется для получения уведомлений об указанных событиях, влияющих на сеанс.</span><span class="sxs-lookup"><span data-stu-id="b357c-105">Registers to receive notification of specified events that affect the session.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="b357c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b357c-106">Parameters</span></span>

 <span data-ttu-id="b357c-107">_Кбентрид_</span><span class="sxs-lookup"><span data-stu-id="b357c-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="b357c-108">возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="b357c-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b357c-109">_Лпентрид_</span><span class="sxs-lookup"><span data-stu-id="b357c-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="b357c-110">возврата Указатель на идентификатор записи адресной книги или объекта хранилища сообщений о том, какие уведомления должны быть созданы, или значение NULL, которое указывает на то, что клиент регистрируется для получения уведомлений о событиях, которые влияют только на сеанс.</span><span class="sxs-lookup"><span data-stu-id="b357c-110">[in] A pointer to the entry identifier of the address book or message store object about which notifications should be generated, or NULL, which indicates that the client is registering to receive notifications about events that affect only the session.</span></span> 
    
 <span data-ttu-id="b357c-111">_Улевентмаск_</span><span class="sxs-lookup"><span data-stu-id="b357c-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="b357c-112">возврата Маска значений, указывающая типы событий уведомления, которые интересуются клиентом и должны быть включены в регистрацию.</span><span class="sxs-lookup"><span data-stu-id="b357c-112">[in] A mask of values that indicate the types of notification events that the client is interested in and should be included in the registration.</span></span> <span data-ttu-id="b357c-113">Если _лпентрид_ имеет значение null, MAPI автоматически регистрирует клиент для событий с критическими ошибками, которые влияют только на сеанс.</span><span class="sxs-lookup"><span data-stu-id="b357c-113">If  _lpEntryID_ is NULL, MAPI automatically registers the client for critical error events that affect only the session.</span></span> <span data-ttu-id="b357c-114">Когда _лпентрид_ указывает на идентификатор записи, для параметра _улевентмаск_ допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b357c-114">When  _lpEntryID_ points to an entry identifier, the following values are valid for the  _ulEventMask_ parameter:</span></span> 
    
<span data-ttu-id="b357c-115">Фневкритикалеррор</span><span class="sxs-lookup"><span data-stu-id="b357c-115">fnevCriticalError</span></span> 
  
> <span data-ttu-id="b357c-116">Регистрирует уведомления о серьезных ошибках, таких как недостаток памяти.</span><span class="sxs-lookup"><span data-stu-id="b357c-116">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
<span data-ttu-id="b357c-117">Фневекстендед</span><span class="sxs-lookup"><span data-stu-id="b357c-117">fnevExtended</span></span> 
  
> <span data-ttu-id="b357c-118">Регистрирует уведомления о событиях, относящихся к определенной адресной книге или поставщику хранилища сообщений, а также о завершении сеанса.</span><span class="sxs-lookup"><span data-stu-id="b357c-118">Registers for notifications about events specific to a particular address book or message store provider and about session shut down.</span></span>
    
<span data-ttu-id="b357c-119">Фневневмаил</span><span class="sxs-lookup"><span data-stu-id="b357c-119">fnevNewMail</span></span> 
  
> <span data-ttu-id="b357c-120">Регистрирует уведомления о поступлении новых сообщений.</span><span class="sxs-lookup"><span data-stu-id="b357c-120">Registers for notifications about the arrival of new messages.</span></span> 
    
<span data-ttu-id="b357c-121">Фневобжекткреатед</span><span class="sxs-lookup"><span data-stu-id="b357c-121">fnevObjectCreated</span></span> 
  
> <span data-ttu-id="b357c-122">Регистрирует уведомления о создании нового объекта.</span><span class="sxs-lookup"><span data-stu-id="b357c-122">Registers for notifications about the creation of a new object.</span></span>
    
<span data-ttu-id="b357c-123">Фневобжекткопиед</span><span class="sxs-lookup"><span data-stu-id="b357c-123">fnevObjectCopied</span></span>
  
> <span data-ttu-id="b357c-124">Регистрирует уведомления о копируемом объекте.</span><span class="sxs-lookup"><span data-stu-id="b357c-124">Registers for notifications about an object being copied.</span></span>
    
<span data-ttu-id="b357c-125">Фневобжектделетед</span><span class="sxs-lookup"><span data-stu-id="b357c-125">fnevObjectDeleted</span></span>
  
> <span data-ttu-id="b357c-126">Регистрирует уведомления об удалении объекта.</span><span class="sxs-lookup"><span data-stu-id="b357c-126">Registers for notifications about an object being deleted.</span></span>
    
<span data-ttu-id="b357c-127">Фневобжектмодифиед</span><span class="sxs-lookup"><span data-stu-id="b357c-127">fnevObjectModified</span></span>
  
> <span data-ttu-id="b357c-128">Регистрирует уведомления об изменяемом объекте.</span><span class="sxs-lookup"><span data-stu-id="b357c-128">Registers for notifications about an object being modified.</span></span>
    
<span data-ttu-id="b357c-129">Фневобжектмовед</span><span class="sxs-lookup"><span data-stu-id="b357c-129">fnevObjectMoved</span></span>
  
> <span data-ttu-id="b357c-130">Регистрирует уведомления об перемещении объекта.</span><span class="sxs-lookup"><span data-stu-id="b357c-130">Registers for notifications about an object being moved.</span></span>
    
<span data-ttu-id="b357c-131">Фневсеарчкомплете</span><span class="sxs-lookup"><span data-stu-id="b357c-131">fnevSearchComplete</span></span>
  
> <span data-ttu-id="b357c-132">Регистрирует уведомления о завершении операции поиска.</span><span class="sxs-lookup"><span data-stu-id="b357c-132">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="b357c-133">_Лпадвисесинк_</span><span class="sxs-lookup"><span data-stu-id="b357c-133">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="b357c-134">возврата Указатель на объект приемника уведомлений для получения последующих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="b357c-134">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="b357c-135">Этот объект приемника уведомлений должен быть уже выделен.</span><span class="sxs-lookup"><span data-stu-id="b357c-135">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="b357c-136">_Лпулконнектион_</span><span class="sxs-lookup"><span data-stu-id="b357c-136">_lpulConnection_</span></span>
  
> <span data-ttu-id="b357c-137">вышли Указатель на ненулевое число, которое представляет соединение между объектом приемника уведомлений вызывающего абонента и сеансом.</span><span class="sxs-lookup"><span data-stu-id="b357c-137">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b357c-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b357c-138">Return value</span></span>

<span data-ttu-id="b357c-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="b357c-139">S_OK</span></span> 
  
> <span data-ttu-id="b357c-140">Регистрация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b357c-140">The registration was successful.</span></span>
    
<span data-ttu-id="b357c-141">МАПИ_Е_ИНВАЛИД_ЕНТРИД</span><span class="sxs-lookup"><span data-stu-id="b357c-141">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="b357c-142">Идентификатор записи, на который указывает _лпентрид_ , не представляет допустимый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="b357c-142">The entry identifier pointed to by  _lpEntryID_ does not represent a valid entry identifier.</span></span> 
    
<span data-ttu-id="b357c-143">МАПИ_Е_НО_СУППОРТ</span><span class="sxs-lookup"><span data-stu-id="b357c-143">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="b357c-144">Поставщик услуг, ответственный за идентификатор записи, на который указывает _лпентрид_ , либо не поддерживает тип событий, указанных в параметре _улевентмаск_ , либо не поддерживает уведомление.</span><span class="sxs-lookup"><span data-stu-id="b357c-144">The service provider responsible for the entry identifier pointed to by  _lpEntryID_ either does not support the type of events specified in the  _ulEventMask_ parameter or does not support notification.</span></span> 
    
<span data-ttu-id="b357c-145">МАПИ_Е_УНКНОВН_ЕНТРИД</span><span class="sxs-lookup"><span data-stu-id="b357c-145">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="b357c-146">Идентификатор записи, на который указывает _лпентрид_ , не может быть обработан ни одним из поставщиков услуг в профиле.</span><span class="sxs-lookup"><span data-stu-id="b357c-146">The entry identifier pointed to by  _lpEntryID_ cannot be handled by any of the service providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b357c-147">Примечания</span><span class="sxs-lookup"><span data-stu-id="b357c-147">Remarks</span></span>

<span data-ttu-id="b357c-148">Метод **IMAPISession:: Advise** устанавливает соединение между объектом приемника уведомлений вызывающего абонента, сеансом и, при необходимости, поставщиком службы.</span><span class="sxs-lookup"><span data-stu-id="b357c-148">The **IMAPISession::Advise** method establishes a connection between the caller's advise sink object, the session and, optionally, a service provider.</span></span> <span data-ttu-id="b357c-149">Это подключение используется для отправки уведомлений в приемник уведомлений, когда одно или несколько событий, указанных в параметре _улевентмаск_ , происходят в объекте, на который указывает _лпентрид_.</span><span class="sxs-lookup"><span data-stu-id="b357c-149">This connection is used to send notifications to the advise sink when one or more events specified in the  _ulEventMask_ parameter occur to the object pointed to by  _lpEntryID_.</span></span> <span data-ttu-id="b357c-150">Если _лпентрид_ имеет значение null, то целевой объект является сеансом, а уведомления отправляются только для критических ошибок и расширенных событий.</span><span class="sxs-lookup"><span data-stu-id="b357c-150">When  _lpEntryID_ is NULL, the target object is the session and notifications are sent only for critical errors and extended events.</span></span> 
  
<span data-ttu-id="b357c-151">Когда _лпентрид_ указывает на допустимый идентификатор записи, MAPI вызывает метод **advise** объекта logon, принадлежащего поставщику услуг.</span><span class="sxs-lookup"><span data-stu-id="b357c-151">When  _lpEntryID_ points to a valid entry identifier, MAPI calls the **Advise** method of the logon object that belongs to the responsible service provider.</span></span> <span data-ttu-id="b357c-152">Например, если _лпентрид_ указывает на идентификатор элемента списка рассылки, MAPI вызывает соответствующий метод поставщика адресных книг [Иаблогон:: Advise](iablogon-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="b357c-152">For example, if  _lpEntryID_ points to the entry identifier of a distribution list, MAPI calls the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="b357c-153">Чтобы отправить уведомление, поставщик услуг или MAPI вызывает зарегистрированный метод [имапиадвисесинк:: OnNotify](imapiadvisesink-onnotify.md) приемника уведомлений.</span><span class="sxs-lookup"><span data-stu-id="b357c-153">To send a notification, either the service provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="b357c-154">Один из параметров для параметра **OnNotify**, структура уведомления содержит сведения, описывающие конкретное событие.</span><span class="sxs-lookup"><span data-stu-id="b357c-154">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="b357c-155">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="b357c-155">Notes to callers</span></span>

<span data-ttu-id="b357c-156">В системах, поддерживающих несколько потоков выполнения, вызов onNotify \*\*\*\* также может выполняться в любом потоке в любое время.</span><span class="sxs-lookup"><span data-stu-id="b357c-156">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="b357c-157">Если требуется гарантировать, что уведомления будут выполняться только в определенный момент в определенном потоке, вызовите функцию [хрсиссреададвисесинк](hrthisthreadadvisesink.md) , чтобы создать объект приемника уведомлений, передаваемый в метод **advise** .</span><span class="sxs-lookup"><span data-stu-id="b357c-157">If you need assurance that notifications will occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to the **Advise** method.</span></span> 
  
<span data-ttu-id="b357c-158">Чтобы определить, когда клиент вышел из системы, зарегистрируйте уведомления у поставщика услуг, вызвав предложение **advise** с _ЛПЕНТРИД_ , указав значение null, а для параметра _кбентрид_ значение 0.</span><span class="sxs-lookup"><span data-stu-id="b357c-158">To determine when a client has logged off, register for notifications in your service provider by calling **Advise** with  _lpEntryID_ set to NULL and  _cbEntryID_ set to 0.</span></span> <span data-ttu-id="b357c-159">При выходе из системы вы получите уведомление Фневекстендед.</span><span class="sxs-lookup"><span data-stu-id="b357c-159">When the logoff occurs, you will receive an fnevExtended notification.</span></span> 
  
<span data-ttu-id="b357c-160">После успешного выполнения вызова **advise** и до [IMAPISession:: unadvise](imapisession-unadvise.md) вызывается для отмены регистрации, освобождения объекта приемника уведомлений, если для него не задано конкретное долгосрочное использование.</span><span class="sxs-lookup"><span data-stu-id="b357c-160">After a call to **Advise** has succeeded and before [IMAPISession::Unadvise](imapisession-unadvise.md) has been called to cancel the registration, release your advise sink object unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="b357c-161">Обзор процесса уведомления представлен [в статье уведомление о событии в MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="b357c-161">For an overview of the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="b357c-162">Более подробную информацию об обработке уведомлений можно узнать в статье [обработка уведомлений](handling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="b357c-162">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b357c-163">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b357c-163">MFCMAPI reference</span></span>

<span data-ttu-id="b357c-164">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="b357c-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b357c-165">**Файл**</span><span class="sxs-lookup"><span data-stu-id="b357c-165">**File**</span></span>|<span data-ttu-id="b357c-166">**Функция**</span><span class="sxs-lookup"><span data-stu-id="b357c-166">**Function**</span></span>|<span data-ttu-id="b357c-167">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="b357c-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b357c-168">Баседиалог. cpp</span><span class="sxs-lookup"><span data-stu-id="b357c-168">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="b357c-169">Кбаседиалог:: Оннотификатионсон</span><span class="sxs-lookup"><span data-stu-id="b357c-169">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="b357c-170">MFCMAPI использует метод **IMAPISession:: Advise** для регистрации уведомлений в сеансе.</span><span class="sxs-lookup"><span data-stu-id="b357c-170">MFCMAPI uses the **IMAPISession::Advise** method to register for notifications against the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b357c-171">См. также</span><span class="sxs-lookup"><span data-stu-id="b357c-171">See also</span></span>



[<span data-ttu-id="b357c-172">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="b357c-172">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="b357c-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="b357c-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="b357c-174">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="b357c-174">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="b357c-175">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="b357c-175">IMAPISession::Unadvise</span></span>](imapisession-unadvise.md)
  
[<span data-ttu-id="b357c-176">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b357c-176">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="b357c-177">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="b357c-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="b357c-178">Уведомление о соБытии в MAPI</span><span class="sxs-lookup"><span data-stu-id="b357c-178">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)

