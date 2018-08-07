---
title: IAddrBookAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Advise
api_type:
- COM
ms.assetid: 2def89ed-e4ce-446a-8b80-132d11ae8f8b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8214390af883432d72f608452b8b944417884fd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808751"
---
# <a name="iaddrbookadvise"></a><span data-ttu-id="f9544-103">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="f9544-103">IAddrBook::Advise</span></span>

  
  
<span data-ttu-id="f9544-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f9544-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f9544-105">Регистрация клиента или поставщика для получения уведомлений об изменениях в одну или несколько записей в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="f9544-105">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="f9544-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f9544-106">Parameters</span></span>

 <span data-ttu-id="f9544-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f9544-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="f9544-108">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="f9544-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f9544-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="f9544-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="f9544-110">[in] Указатель на идентификатор записи контейнер адресной книги, системы обмена сообщениями пользователя или список рассылки, который будет создаваться уведомление, когда происходит изменение типа или типов, описанных в параметре _ulEventMask_ .</span><span class="sxs-lookup"><span data-stu-id="f9544-110">[in] A pointer to the entry identifier of the address book container, messaging user, or distribution list that will generate a notification when a change occurs of the type or types described in the  _ulEventMask_ parameter.</span></span> 
    
 <span data-ttu-id="f9544-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="f9544-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="f9544-112">[in] Одно или несколько событий уведомлений, которые регистрации вызывающего абонента для получения.</span><span class="sxs-lookup"><span data-stu-id="f9544-112">[in] One or more notification events that the caller is registering to receive.</span></span> <span data-ttu-id="f9544-113">Каждое событие связан со структурой уведомление, который содержит сведения об изменениях, которые произошли.</span><span class="sxs-lookup"><span data-stu-id="f9544-113">Each event is associated with a particular notification structure that contains information about the change that occurred.</span></span> <span data-ttu-id="f9544-114">В следующей таблице перечислены допустимые значения для _ulEventMask_ и их соответствующие структуры.</span><span class="sxs-lookup"><span data-stu-id="f9544-114">The following table lists the valid values for  _ulEventMask_ and their corresponding structures.</span></span> 
    
|<span data-ttu-id="f9544-115">**Уведомление о событии**</span><span class="sxs-lookup"><span data-stu-id="f9544-115">**Notification event**</span></span>|<span data-ttu-id="f9544-116">**Соответствующий структуры**</span><span class="sxs-lookup"><span data-stu-id="f9544-116">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f9544-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="f9544-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="f9544-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f9544-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="f9544-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="f9544-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="f9544-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f9544-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="f9544-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="f9544-121">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="f9544-122">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f9544-122">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="f9544-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="f9544-123">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="f9544-124">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f9544-124">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="f9544-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="f9544-125">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="f9544-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f9544-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="f9544-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="f9544-127">**fnevObjectMoved**</span></span> <br/> |[<span data-ttu-id="f9544-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f9544-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="f9544-129">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="f9544-129">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="f9544-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f9544-130">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
   
 <span data-ttu-id="f9544-131">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="f9544-131">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="f9544-132">[in] Указатель на элемент уведомлений приемник, который будет вызываться, когда происходит событие, для которого был запрошен уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f9544-132">[in] A pointer to the advise sink object to be called when the event for which notification has been requested occurs.</span></span>
    
 <span data-ttu-id="f9544-133">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="f9544-133">_lpulConnection_</span></span>
  
> <span data-ttu-id="f9544-134">[out] Указатель на подключение ненулевое число, представляющее регистрации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f9544-134">[out] A pointer to a nonzero connection number that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f9544-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5">Return value</span></span>

<span data-ttu-id="f9544-136">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="f9544-136">S_OK</span></span> 
  
> <span data-ttu-id="f9544-137">Уведомление о регистрации прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="f9544-137">The notification registration was successful.</span></span>
    
<span data-ttu-id="f9544-138">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f9544-138">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="f9544-139">Поставщик адресной книги, ответственный за запись идентификатора, переданного в _lpEntryID_ не удалось зарегистрировать уведомления для соответствующей операции.</span><span class="sxs-lookup"><span data-stu-id="f9544-139">The address book provider responsible for the entry identifier passed in  _lpEntryID_ could not register a notification for the corresponding entry.</span></span> 
    
<span data-ttu-id="f9544-140">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="f9544-140">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="f9544-141">Уведомление не поддерживается поставщик адресной книги, ответственный за запись идентификатором, переданной в параметре _lpEntryID_ объекта.</span><span class="sxs-lookup"><span data-stu-id="f9544-141">Notification is not supported by the address book provider responsible for the object identified by the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="f9544-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f9544-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="f9544-143">Идентификатор записи, переданные в _lpEntryID_ не может справиться с любой из поставщиками адресной книги в профиле.</span><span class="sxs-lookup"><span data-stu-id="f9544-143">The entry identifier passed in  _lpEntryID_ cannot be handled by any of the address book providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f9544-144">Замечания</span><span class="sxs-lookup"><span data-stu-id="f9544-144">Remarks</span></span>

<span data-ttu-id="f9544-145">Клиенты и поставщики услуг вызовите метод **уведомлений** для регистрации для определенного типа или типов уведомлений на запись адресной книги.</span><span class="sxs-lookup"><span data-stu-id="f9544-145">Clients and service providers call the **Advise** method to register for a particular type or types of notification on an address book entry.</span></span> <span data-ttu-id="f9544-146">Типы уведомлений обозначены маска событие, переданное с помощью параметра _ulEventMask_ .</span><span class="sxs-lookup"><span data-stu-id="f9544-146">The types of notification are indicated by the event mask passed in with the  _ulEventMask_ parameter.</span></span> 
  
<span data-ttu-id="f9544-147">MAPI переадресует этот вызов **уведомлений** для доступа к адресной книге, который несет ответственность за запись, что указывает идентификатор записи в параметре _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="f9544-147">MAPI forwards this **Advise** call to the address book provider that is responsible for the entry as indicated by the entry identifier in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="f9544-148">Поставщик адресной книги обрабатывает регистрации самого или вызывает метод поддержки [IMAPISupport::Subscribe](imapisupport-subscribe.md), чтобы запрашивать MAPI для регистрации вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="f9544-148">The address book provider either handles the registration itself or calls the support method, [IMAPISupport::Subscribe](imapisupport-subscribe.md), to prompt MAPI to register the caller.</span></span> <span data-ttu-id="f9544-149">Для представления успешной регистрации возвращается число ненулевое подключения.</span><span class="sxs-lookup"><span data-stu-id="f9544-149">A nonzero connection number is returned to represent the successful registration.</span></span>
  
<span data-ttu-id="f9544-150">При каждом изменении записи тип, указанный в параметре регистрации уведомлений, поставщик адресной книги вызывает метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) для объекта приемник уведомлений, указанный в параметре _lpAdviseSink_ .</span><span class="sxs-lookup"><span data-stu-id="f9544-150">Whenever a change occurs to the entry of the type indicated by the notification registration, the address book provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object specified in the  _lpAdviseSink_ parameter.</span></span> <span data-ttu-id="f9544-151">Метод **OnNotify** содержит структуру [УВЕДОМЛЕНИЙ](notification.md) в качестве входного параметра, который содержит данные для описания события.</span><span class="sxs-lookup"><span data-stu-id="f9544-151">The **OnNotify** method includes a [NOTIFICATION](notification.md) structure as an input parameter that contains data to describe the event.</span></span> 
  
<span data-ttu-id="f9544-152">В зависимости от доступа к адресной книге вызов **OnNotify** может произойти сразу после изменения зарегистрированных объект или позже.</span><span class="sxs-lookup"><span data-stu-id="f9544-152">Depending on the address book provider, the call to **OnNotify** can occur immediately following the change to the registered object or at a later time.</span></span> <span data-ttu-id="f9544-153">На компьютерах, поддерживающих многопоточной среде вызов **OnNotify** может выполняться на любой поток.</span><span class="sxs-lookup"><span data-stu-id="f9544-153">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="f9544-154">Клиенты могут запрашивать только такие уведомления на определенного потока с помощью вызова функции [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) для создания объекта приемник уведомлений, который передается в **уведомлений**.</span><span class="sxs-lookup"><span data-stu-id="f9544-154">Clients can request that these notifications occur on a particular thread by calling the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to create the advise sink object that is passed to **Advise**.</span></span> 
  
<span data-ttu-id="f9544-155">Так как поставщика адресных книг можно освободить объект приемника уведомлений, переданного с клиентами в любое время после успешного завершения **уведомлений** звонков и перед [IAddrBook::Unadvise](iaddrbook-unadvise.md) звонок, чтобы отменить уведомление, освобождать клиентов их уведомлений приемника объектов при возврате **уведомлений** .</span><span class="sxs-lookup"><span data-stu-id="f9544-155">Because an address book provider can release the advise sink object passed in by clients at any time after the successful completion of the **Advise** call and before an [IAddrBook::Unadvise](iaddrbook-unadvise.md) call to cancel the notification, clients should release their advise sink objects when **Advise** returns.</span></span> 
  
<span data-ttu-id="f9544-156">Дополнительные сведения о процессе уведомления содержатся в разделе [Уведомление о событии в MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="f9544-156">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f9544-157">См. также</span><span class="sxs-lookup"><span data-stu-id="f9544-157">See also</span></span>



[<span data-ttu-id="f9544-158">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="f9544-158">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="f9544-159">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="f9544-159">IAddrBook::Unadvise</span></span>](iaddrbook-unadvise.md)
  
[<span data-ttu-id="f9544-160">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="f9544-160">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="f9544-161">�����������</span><span class="sxs-lookup"><span data-stu-id="f9544-161">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="f9544-162">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f9544-162">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

