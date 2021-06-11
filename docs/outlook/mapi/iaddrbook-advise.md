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
ms.openlocfilehash: 7abafafd3d4bd9618d85a7dac34e4556545167bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406278"
---
# <a name="iaddrbookadvise"></a><span data-ttu-id="2f244-103">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="2f244-103">IAddrBook::Advise</span></span>

  
  
<span data-ttu-id="2f244-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f244-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f244-105">Регистрирует клиента или поставщика услуг для получения уведомлений об изменениях одной или более записей в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="2f244-105">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="2f244-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="2f244-106">Parameters</span></span>

 <span data-ttu-id="2f244-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="2f244-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="2f244-108">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="2f244-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="2f244-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="2f244-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="2f244-110">[in] Указатель на идентификатор входа контейнера адресной книги, пользователя обмена сообщениями или списка рассылки, который генерирует уведомление при изменении типа или типов, описанных в параметре _ulEventMask._</span><span class="sxs-lookup"><span data-stu-id="2f244-110">[in] A pointer to the entry identifier of the address book container, messaging user, or distribution list that will generate a notification when a change occurs of the type or types described in the  _ulEventMask_ parameter.</span></span> 
    
 <span data-ttu-id="2f244-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="2f244-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="2f244-112">[in] Одно или несколько событий уведомления, которые регистрируется для получения вызываемой стороны.</span><span class="sxs-lookup"><span data-stu-id="2f244-112">[in] One or more notification events that the caller is registering to receive.</span></span> <span data-ttu-id="2f244-113">Каждое событие связано с определенной структурой уведомлений, которая содержит сведения о произошедших изменениях.</span><span class="sxs-lookup"><span data-stu-id="2f244-113">Each event is associated with a particular notification structure that contains information about the change that occurred.</span></span> <span data-ttu-id="2f244-114">В следующей таблице перечислены допустимые значения  _для ulEventMask_ и их соответствующих структур.</span><span class="sxs-lookup"><span data-stu-id="2f244-114">The following table lists the valid values for  _ulEventMask_ and their corresponding structures.</span></span> 
    
|<span data-ttu-id="2f244-115">**Событие уведомлений**</span><span class="sxs-lookup"><span data-stu-id="2f244-115">**Notification event**</span></span>|<span data-ttu-id="2f244-116">**Соответствующая структура**</span><span class="sxs-lookup"><span data-stu-id="2f244-116">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2f244-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="2f244-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="2f244-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="2f244-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="2f244-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="2f244-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="2f244-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="2f244-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="2f244-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="2f244-121">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="2f244-122">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="2f244-122">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="2f244-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="2f244-123">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="2f244-124">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="2f244-124">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="2f244-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="2f244-125">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="2f244-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="2f244-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="2f244-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="2f244-127">**fnevObjectMoved**</span></span> <br/> |[<span data-ttu-id="2f244-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="2f244-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="2f244-129">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="2f244-129">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="2f244-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="2f244-130">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
   
 <span data-ttu-id="2f244-131">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="2f244-131">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="2f244-132">[in] Указатель на объект раковины рекомендации, который будет вызван, когда происходит событие, для которого было запрощено уведомление.</span><span class="sxs-lookup"><span data-stu-id="2f244-132">[in] A pointer to the advise sink object to be called when the event for which notification has been requested occurs.</span></span>
    
 <span data-ttu-id="2f244-133">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="2f244-133">_lpulConnection_</span></span>
  
> <span data-ttu-id="2f244-134">[вышел] Указатель на номер подключения, который представляет регистрацию уведомлений.</span><span class="sxs-lookup"><span data-stu-id="2f244-134">[out] A pointer to a nonzero connection number that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2f244-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f244-135">Return value</span></span>

<span data-ttu-id="2f244-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="2f244-136">S_OK</span></span> 
  
> <span data-ttu-id="2f244-137">Регистрация уведомлений прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="2f244-137">The notification registration was successful.</span></span>
    
<span data-ttu-id="2f244-138">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2f244-138">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="2f244-139">Поставщик адресной книги, ответственный за идентификатор записи, переданный  _в lpEntryID,_ не смог зарегистрировать уведомление для соответствующей записи.</span><span class="sxs-lookup"><span data-stu-id="2f244-139">The address book provider responsible for the entry identifier passed in  _lpEntryID_ could not register a notification for the corresponding entry.</span></span> 
    
<span data-ttu-id="2f244-140">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="2f244-140">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="2f244-141">Уведомление не поддерживается поставщиком адресной книги, ответственным за объект, идентифицированный идентификатором записи, переданным в _параметре lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="2f244-141">Notification is not supported by the address book provider responsible for the object identified by the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="2f244-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2f244-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="2f244-143">Идентификатор записи, переданный  _в lpEntryID,_ не может обрабатываться любым из поставщиков адресных книг в профиле.</span><span class="sxs-lookup"><span data-stu-id="2f244-143">The entry identifier passed in  _lpEntryID_ cannot be handled by any of the address book providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2f244-144">Примечания</span><span class="sxs-lookup"><span data-stu-id="2f244-144">Remarks</span></span>

<span data-ttu-id="2f244-145">Клиенты и поставщики услуг звонят **методу Advise** для регистрации для определенного типа или типов уведомлений в записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="2f244-145">Clients and service providers call the **Advise** method to register for a particular type or types of notification on an address book entry.</span></span> <span data-ttu-id="2f244-146">Типы уведомлений указываются в маске события, переданной с _параметром ulEventMask._</span><span class="sxs-lookup"><span data-stu-id="2f244-146">The types of notification are indicated by the event mask passed in with the  _ulEventMask_ parameter.</span></span> 
  
<span data-ttu-id="2f244-147">MAPI передает этот вызов **сообщить** поставщику адресной книги, который отвечает за запись, как указано идентификатором записи в _параметре lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="2f244-147">MAPI forwards this **Advise** call to the address book provider that is responsible for the entry as indicated by the entry identifier in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="2f244-148">Поставщик адресной книги либо обрабатывает сам процесс регистрации, либо вызывает метод поддержки [IMAPISupport::Subscribe,](imapisupport-subscribe.md)чтобы побудить MAPI зарегистрировать вызываемого.</span><span class="sxs-lookup"><span data-stu-id="2f244-148">The address book provider either handles the registration itself or calls the support method, [IMAPISupport::Subscribe](imapisupport-subscribe.md), to prompt MAPI to register the caller.</span></span> <span data-ttu-id="2f244-149">Для успешной регистрации возвращается номер подключения незеро.</span><span class="sxs-lookup"><span data-stu-id="2f244-149">A nonzero connection number is returned to represent the successful registration.</span></span>
  
<span data-ttu-id="2f244-150">Всякий раз, когда происходит изменение в записи типа, указанного в регистрации уведомлений, поставщик адресной книги вызывает [метод IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) для объекта раковины рекомендации, указанного в параметре _lpAdviseSink._</span><span class="sxs-lookup"><span data-stu-id="2f244-150">Whenever a change occurs to the entry of the type indicated by the notification registration, the address book provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object specified in the  _lpAdviseSink_ parameter.</span></span> <span data-ttu-id="2f244-151">Метод **OnNotify** включает структуру [УВЕДОМЛЕНий](notification.md) в качестве параметра ввода, который содержит данные для описания события.</span><span class="sxs-lookup"><span data-stu-id="2f244-151">The **OnNotify** method includes a [NOTIFICATION](notification.md) structure as an input parameter that contains data to describe the event.</span></span> 
  
<span data-ttu-id="2f244-152">В зависимости от поставщика адресной книги вызов **OnNotify** может произойти сразу после изменения зарегистрированного объекта или позднее.</span><span class="sxs-lookup"><span data-stu-id="2f244-152">Depending on the address book provider, the call to **OnNotify** can occur immediately following the change to the registered object or at a later time.</span></span> <span data-ttu-id="2f244-153">В системах, поддерживаюх несколько потоков выполнения, вызов **OnNotify** может происходить в любом потоке.</span><span class="sxs-lookup"><span data-stu-id="2f244-153">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="2f244-154">Клиенты могут запросить, чтобы эти уведомления были в определенном потоке, позвонив в функцию [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) для создания объекта-раковины, передаваемого **совету**.</span><span class="sxs-lookup"><span data-stu-id="2f244-154">Clients can request that these notifications occur on a particular thread by calling the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to create the advise sink object that is passed to **Advise**.</span></span> 
  
<span data-ttu-id="2f244-155">Так как поставщик адресной книги может освободить объект раковины рекомендации, переданный  клиентами в любое время после успешного завершения вызова "Советы" и перед вызовом  [IAddrBook::Unadvise,](iaddrbook-unadvise.md) чтобы отменить уведомление, клиенты должны освободить свои объекты раковины рекомендации, когда сообщите возвращается.</span><span class="sxs-lookup"><span data-stu-id="2f244-155">Because an address book provider can release the advise sink object passed in by clients at any time after the successful completion of the **Advise** call and before an [IAddrBook::Unadvise](iaddrbook-unadvise.md) call to cancel the notification, clients should release their advise sink objects when **Advise** returns.</span></span> 
  
<span data-ttu-id="2f244-156">Дополнительные сведения о процессе уведомления см. в сообщении [события в MAPI.](event-notification-in-mapi.md)</span><span class="sxs-lookup"><span data-stu-id="2f244-156">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2f244-157">См. также</span><span class="sxs-lookup"><span data-stu-id="2f244-157">See also</span></span>



[<span data-ttu-id="2f244-158">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="2f244-158">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="2f244-159">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="2f244-159">IAddrBook::Unadvise</span></span>](iaddrbook-unadvise.md)
  
[<span data-ttu-id="2f244-160">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="2f244-160">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="2f244-161">�����������</span><span class="sxs-lookup"><span data-stu-id="2f244-161">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="2f244-162">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2f244-162">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

