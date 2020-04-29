---
title: иаддрбукадвисе
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
# <a name="iaddrbookadvise"></a><span data-ttu-id="12aa9-103">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="12aa9-103">IAddrBook::Advise</span></span>

  
  
<span data-ttu-id="12aa9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12aa9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12aa9-105">Регистрирует клиента или поставщика услуг для получения уведомлений об изменениях в одной или нескольких записях в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="12aa9-105">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="12aa9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="12aa9-106">Parameters</span></span>

 <span data-ttu-id="12aa9-107">_кбентрид_</span><span class="sxs-lookup"><span data-stu-id="12aa9-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="12aa9-108">возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="12aa9-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="12aa9-109">_лпентрид_</span><span class="sxs-lookup"><span data-stu-id="12aa9-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="12aa9-110">возврата Указатель на идентификатор записи контейнера адресной книги, пользователя обмена сообщениями или списка рассылки, который будет создавать уведомление при изменении типа или типов, описанных в параметре _улевентмаск_ .</span><span class="sxs-lookup"><span data-stu-id="12aa9-110">[in] A pointer to the entry identifier of the address book container, messaging user, or distribution list that will generate a notification when a change occurs of the type or types described in the  _ulEventMask_ parameter.</span></span> 
    
 <span data-ttu-id="12aa9-111">_улевентмаск_</span><span class="sxs-lookup"><span data-stu-id="12aa9-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="12aa9-112">возврата Одно или несколько событий уведомления, регистрируемых абонентом для получения.</span><span class="sxs-lookup"><span data-stu-id="12aa9-112">[in] One or more notification events that the caller is registering to receive.</span></span> <span data-ttu-id="12aa9-113">Каждое событие связано с определенной структурой уведомлений, которая содержит сведения о произошедших изменениях.</span><span class="sxs-lookup"><span data-stu-id="12aa9-113">Each event is associated with a particular notification structure that contains information about the change that occurred.</span></span> <span data-ttu-id="12aa9-114">В следующей таблице приведены допустимые значения для _улевентмаск_ и соответствующие им структуры.</span><span class="sxs-lookup"><span data-stu-id="12aa9-114">The following table lists the valid values for  _ulEventMask_ and their corresponding structures.</span></span> 
    
|<span data-ttu-id="12aa9-115">**Событие уведомления**</span><span class="sxs-lookup"><span data-stu-id="12aa9-115">**Notification event**</span></span>|<span data-ttu-id="12aa9-116">**Соответствующая структура**</span><span class="sxs-lookup"><span data-stu-id="12aa9-116">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="12aa9-117">**фневкритикалеррор**</span><span class="sxs-lookup"><span data-stu-id="12aa9-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="12aa9-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="12aa9-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="12aa9-119">**фневобжекткреатед**</span><span class="sxs-lookup"><span data-stu-id="12aa9-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="12aa9-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="12aa9-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="12aa9-121">**фневобжектделетед**</span><span class="sxs-lookup"><span data-stu-id="12aa9-121">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="12aa9-122">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="12aa9-122">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="12aa9-123">**фневобжектмодифиед**</span><span class="sxs-lookup"><span data-stu-id="12aa9-123">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="12aa9-124">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="12aa9-124">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="12aa9-125">**фневобжекткопиед**</span><span class="sxs-lookup"><span data-stu-id="12aa9-125">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="12aa9-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="12aa9-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="12aa9-127">**фневобжектмовед**</span><span class="sxs-lookup"><span data-stu-id="12aa9-127">**fnevObjectMoved**</span></span> <br/> |[<span data-ttu-id="12aa9-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="12aa9-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="12aa9-129">**фневтаблемодифиед**</span><span class="sxs-lookup"><span data-stu-id="12aa9-129">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="12aa9-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="12aa9-130">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
   
 <span data-ttu-id="12aa9-131">_лпадвисесинк_</span><span class="sxs-lookup"><span data-stu-id="12aa9-131">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="12aa9-132">возврата Указатель на объект приемника уведомлений, вызываемый при возникновении события, для которого было запрошено уведомление.</span><span class="sxs-lookup"><span data-stu-id="12aa9-132">[in] A pointer to the advise sink object to be called when the event for which notification has been requested occurs.</span></span>
    
 <span data-ttu-id="12aa9-133">_лпулконнектион_</span><span class="sxs-lookup"><span data-stu-id="12aa9-133">_lpulConnection_</span></span>
  
> <span data-ttu-id="12aa9-134">вышли Указатель на ненулевый номер подключения, представляющий регистрацию уведомления.</span><span class="sxs-lookup"><span data-stu-id="12aa9-134">[out] A pointer to a nonzero connection number that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="12aa9-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="12aa9-135">Return value</span></span>

<span data-ttu-id="12aa9-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="12aa9-136">S_OK</span></span> 
  
> <span data-ttu-id="12aa9-137">Успешная регистрация уведомления.</span><span class="sxs-lookup"><span data-stu-id="12aa9-137">The notification registration was successful.</span></span>
    
<span data-ttu-id="12aa9-138">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="12aa9-138">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="12aa9-139">Поставщик адресной книги, отвечающий за идентификатор записи, переданный в _лпентрид_ , не смог зарегистрировать уведомление для соответствующей записи.</span><span class="sxs-lookup"><span data-stu-id="12aa9-139">The address book provider responsible for the entry identifier passed in  _lpEntryID_ could not register a notification for the corresponding entry.</span></span> 
    
<span data-ttu-id="12aa9-140">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="12aa9-140">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="12aa9-141">Уведомление не поддерживается поставщиком адресных книг, который отвечает за объект, указанный с помощью идентификатора записи, переданного в параметре _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="12aa9-141">Notification is not supported by the address book provider responsible for the object identified by the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="12aa9-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="12aa9-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="12aa9-143">Идентификатор записи, переданный в _лпентрид_ , не может быть обработан ни одним из поставщиков адресных книг в профиле.</span><span class="sxs-lookup"><span data-stu-id="12aa9-143">The entry identifier passed in  _lpEntryID_ cannot be handled by any of the address book providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="12aa9-144">Примечания</span><span class="sxs-lookup"><span data-stu-id="12aa9-144">Remarks</span></span>

<span data-ttu-id="12aa9-145">Клиенты и поставщики услуг вызывают метод **advise** для регистрации определенного типа или типов уведомлений в записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="12aa9-145">Clients and service providers call the **Advise** method to register for a particular type or types of notification on an address book entry.</span></span> <span data-ttu-id="12aa9-146">Типы уведомлений обозначаются маской события, переданной с помощью параметра _улевентмаск_ .</span><span class="sxs-lookup"><span data-stu-id="12aa9-146">The types of notification are indicated by the event mask passed in with the  _ulEventMask_ parameter.</span></span> 
  
<span data-ttu-id="12aa9-147">MAPI пересылает этот **рекомендуемый** вызов поставщику адресной книги, который отвечает за запись, как указано в параметре _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="12aa9-147">MAPI forwards this **Advise** call to the address book provider that is responsible for the entry as indicated by the entry identifier in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="12aa9-148">Поставщик адресных книг либо обрабатывает регистрацию, либо вызывает метод поддержки, [имаписуппорт:: Subscribe](imapisupport-subscribe.md), чтобы запросить MAPI для регистрации абонента.</span><span class="sxs-lookup"><span data-stu-id="12aa9-148">The address book provider either handles the registration itself or calls the support method, [IMAPISupport::Subscribe](imapisupport-subscribe.md), to prompt MAPI to register the caller.</span></span> <span data-ttu-id="12aa9-149">Для представления успешной регистрации возвращается ненулевой номер подключения.</span><span class="sxs-lookup"><span data-stu-id="12aa9-149">A nonzero connection number is returned to represent the successful registration.</span></span>
  
<span data-ttu-id="12aa9-150">При каждом изменении записи типа, указанного с помощью регистрации уведомлений, поставщик адресной книги вызывает метод [имапиадвисесинк:: OnNotify](imapiadvisesink-onnotify.md) для объекта приемника уведомлений, указанного в параметре _лпадвисесинк_ .</span><span class="sxs-lookup"><span data-stu-id="12aa9-150">Whenever a change occurs to the entry of the type indicated by the notification registration, the address book provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object specified in the  _lpAdviseSink_ parameter.</span></span> <span data-ttu-id="12aa9-151">Метод **OnNotify** включает структуру [уведомлений](notification.md) в качестве входного параметра, который содержит данные для описания события.</span><span class="sxs-lookup"><span data-stu-id="12aa9-151">The **OnNotify** method includes a [NOTIFICATION](notification.md) structure as an input parameter that contains data to describe the event.</span></span> 
  
<span data-ttu-id="12aa9-152">В зависимости от поставщика адресных книг вызов **OnNotify** может выполняться сразу после изменения зарегистрированного объекта или позже.</span><span class="sxs-lookup"><span data-stu-id="12aa9-152">Depending on the address book provider, the call to **OnNotify** can occur immediately following the change to the registered object or at a later time.</span></span> <span data-ttu-id="12aa9-153">В системах, поддерживающих несколько потоков выполнения, вызов **OnNotify** может выполняться в любом потоке.</span><span class="sxs-lookup"><span data-stu-id="12aa9-153">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="12aa9-154">Клиенты могут запрашивать, что эти уведомления происходят в определенном потоке, вызывая функцию [хрсиссреададвисесинк](hrthisthreadadvisesink.md) для создания объекта приемника уведомлений, который передается в предложение **advise**.</span><span class="sxs-lookup"><span data-stu-id="12aa9-154">Clients can request that these notifications occur on a particular thread by calling the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to create the advise sink object that is passed to **Advise**.</span></span> 
  
<span data-ttu-id="12aa9-155">Так как поставщик адресных книг может освободить объект приемника уведомлений, переданный клиентами, в любой момент после успешного завершения вызова **advise** и до вызова [IAddrBook:: unadvise](iaddrbook-unadvise.md) для отмены уведомления, клиенты должны освободить объекты приемника **уведомлений при** возврате.</span><span class="sxs-lookup"><span data-stu-id="12aa9-155">Because an address book provider can release the advise sink object passed in by clients at any time after the successful completion of the **Advise** call and before an [IAddrBook::Unadvise](iaddrbook-unadvise.md) call to cancel the notification, clients should release their advise sink objects when **Advise** returns.</span></span> 
  
<span data-ttu-id="12aa9-156">Дополнительные сведения о процессе уведомления можно найти в статье [уведомление о событии в MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="12aa9-156">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="12aa9-157">См. также</span><span class="sxs-lookup"><span data-stu-id="12aa9-157">See also</span></span>



[<span data-ttu-id="12aa9-158">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="12aa9-158">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="12aa9-159">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="12aa9-159">IAddrBook::Unadvise</span></span>](iaddrbook-unadvise.md)
  
[<span data-ttu-id="12aa9-160">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="12aa9-160">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="12aa9-161">�����������</span><span class="sxs-lookup"><span data-stu-id="12aa9-161">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="12aa9-162">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="12aa9-162">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

