---
title: Иаблогонадвисе
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
ms.openlocfilehash: 4ab0e4b023e6af19f650abf421aed122dcc21879
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338579"
---
# <a name="iablogonadvise"></a><span data-ttu-id="c9ffc-103">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="c9ffc-103">IABLogon::Advise</span></span>

  
  
<span data-ttu-id="c9ffc-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9ffc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9ffc-105">Регистрирует вызывающий абонент для получения уведомления об указанных событиях, влияющих на контейнер, пользователя обмена сообщениями или список рассылки.</span><span class="sxs-lookup"><span data-stu-id="c9ffc-105">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="c9ffc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9ffc-106">Parameters</span></span>

 <span data-ttu-id="c9ffc-107">_Кбентрид_</span><span class="sxs-lookup"><span data-stu-id="c9ffc-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="c9ffc-108">возврата Количество байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="c9ffc-108">[in] The count of bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="c9ffc-109">_Лпентрид_</span><span class="sxs-lookup"><span data-stu-id="c9ffc-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="c9ffc-110">возврата Указатель на идентификатор записи объекта, для которого необходимо создать уведомления.</span><span class="sxs-lookup"><span data-stu-id="c9ffc-110">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span>
    
 <span data-ttu-id="c9ffc-111">_Улевентмаск_</span><span class="sxs-lookup"><span data-stu-id="c9ffc-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="c9ffc-112">возврата Битовая маска значений, указывающая типы событий уведомлений, в которых заинтересован вызывающий абонент, которые необходимо включить в регистрацию.</span><span class="sxs-lookup"><span data-stu-id="c9ffc-112">[in] A bitmask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="c9ffc-113">Существует соответствующая структура [уведомлений](notification.md) , связанная с каждым типом события, в котором хранятся сведения о событии.</span><span class="sxs-lookup"><span data-stu-id="c9ffc-113">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="c9ffc-114">В следующей таблице приведены допустимые значения параметра _улевентмаск_ и структуры, связанные с каждым значением.</span><span class="sxs-lookup"><span data-stu-id="c9ffc-114">The following table lists the valid values for the  _ulEventMask_ parameter and the structures associated with each value.</span></span> 
    
|<span data-ttu-id="c9ffc-115">**Тип события уведомления**</span><span class="sxs-lookup"><span data-stu-id="c9ffc-115">**Notification event type**</span></span>|<span data-ttu-id="c9ffc-116">\*\*Соответствующая структура \*\*уведомлений\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c9ffc-116">**Corresponding **NOTIFICATION** structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c9ffc-117">**Фневкритикалеррор**</span><span class="sxs-lookup"><span data-stu-id="c9ffc-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="c9ffc-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c9ffc-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="c9ffc-119">**Фневобжекткреатед**</span><span class="sxs-lookup"><span data-stu-id="c9ffc-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="c9ffc-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c9ffc-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="c9ffc-121">**Фневобжектделетед**</span><span class="sxs-lookup"><span data-stu-id="c9ffc-121">**fnevObjectDeleted**</span></span> <br/> |<span data-ttu-id="c9ffc-122">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="c9ffc-122">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="c9ffc-123">**Фневобжектмодифиед**</span><span class="sxs-lookup"><span data-stu-id="c9ffc-123">**fnevObjectModified**</span></span> <br/> |<span data-ttu-id="c9ffc-124">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="c9ffc-124">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="c9ffc-125">**Фневобжекткопиед**</span><span class="sxs-lookup"><span data-stu-id="c9ffc-125">**fnevObjectCopied**</span></span> <br/> |<span data-ttu-id="c9ffc-126">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="c9ffc-126">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="c9ffc-127">**Фневобжектмовед**</span><span class="sxs-lookup"><span data-stu-id="c9ffc-127">**fnevObjectMoved**</span></span> <br/> |<span data-ttu-id="c9ffc-128">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="c9ffc-128">**OBJECT_NOTIFICATION**</span></span> <br/> |
   
 <span data-ttu-id="c9ffc-129">_Лпадвисесинк_</span><span class="sxs-lookup"><span data-stu-id="c9ffc-129">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="c9ffc-130">возврата Указатель на объект приемника уведомлений для получения последующих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c9ffc-130">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span>
    
 <span data-ttu-id="c9ffc-131">_Лпулконнектион_</span><span class="sxs-lookup"><span data-stu-id="c9ffc-131">_lpulConnection_</span></span>
  
> <span data-ttu-id="c9ffc-132">вышли Указатель на ненулевое значение, представляющее регистрацию уведомления.</span><span class="sxs-lookup"><span data-stu-id="c9ffc-132">[out] A pointer to a nonzero value that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c9ffc-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9ffc-133">Return value</span></span>

<span data-ttu-id="c9ffc-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="c9ffc-134">S_OK</span></span> 
  
> <span data-ttu-id="c9ffc-135">Успешная регистрация уведомления.</span><span class="sxs-lookup"><span data-stu-id="c9ffc-135">The notification registration was successful.</span></span>
    
<span data-ttu-id="c9ffc-136">МАПИ_Е_ИНВАЛИД_ЕНТРИД</span><span class="sxs-lookup"><span data-stu-id="c9ffc-136">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="c9ffc-137">Значение идентификатора записи, переданного в параметре _лпентрид_ , не соответствует формату.</span><span class="sxs-lookup"><span data-stu-id="c9ffc-137">The entry identifier passed in the  _lpEntryID_ parameter is not in the appropriate format.</span></span> 
    
<span data-ttu-id="c9ffc-138">МАПИ_Е_НО_СУППОРТ</span><span class="sxs-lookup"><span data-stu-id="c9ffc-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="c9ffc-139">Поставщик адресных книг не поддерживает уведомление, возможно потому, что он не позволяет вносить изменения в объекты.</span><span class="sxs-lookup"><span data-stu-id="c9ffc-139">The address book provider does not support notification, possibly because it does not allow changes to be made to its objects.</span></span>
    
<span data-ttu-id="c9ffc-140">МАПИ_Е_УНКНОВН_ЕНТРИД</span><span class="sxs-lookup"><span data-stu-id="c9ffc-140">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="c9ffc-141">Поставщик адресных книг не может обработать идентификатор записи, переданный в _лпентрид_.</span><span class="sxs-lookup"><span data-stu-id="c9ffc-141">The address book provider cannot handle the entry identifier passed in  _lpEntryID_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c9ffc-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c9ffc-142">Remarks</span></span>

<span data-ttu-id="c9ffc-143">Поставщики адресных книг реализуют метод **иаблогон:: Advise** для регистрации вызывающего абонента, чтобы получать уведомления об изменении объекта в одном из контейнеров.</span><span class="sxs-lookup"><span data-stu-id="c9ffc-143">Address book providers implement the **IABLogon::Advise** method to register the caller to be notified when a change occurs to an object in one of their containers.</span></span> <span data-ttu-id="c9ffc-144">Абоненты могут зарегистрироваться для получения уведомлений о пользователях системы обмена сообщениями, списках рассылки или всех контейнерах.</span><span class="sxs-lookup"><span data-stu-id="c9ffc-144">Callers can register for notifications regarding messaging users, distribution lists, or entire containers.</span></span> 
  
<span data-ttu-id="c9ffc-145">Клиенты обычно вызывают метод [IAddrBook:: Advise](iaddrbook-advise.md) для регистрации уведомлений в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="c9ffc-145">Clients typically call the [IAddrBook::Advise](iaddrbook-advise.md) method to register for address book notifications.</span></span> <span data-ttu-id="c9ffc-146">Затем MAPI вызывает метод **advise** поставщика адресных книг, который отвечает за объект, представленный идентификатором записи в _лпентрид_.</span><span class="sxs-lookup"><span data-stu-id="c9ffc-146">MAPI then calls the **Advise** method of the address book provider that is responsible for the object represented by the entry identifier in  _lpEntryID_.</span></span>
  
<span data-ttu-id="c9ffc-147">Когда происходит изменение указанного объекта типа, представленного в _улевентмаск_, выполняется вызов метода OnNotify приемника уведомлений, \*\*\*\* на который указывает _лпадвисесинк_.</span><span class="sxs-lookup"><span data-stu-id="c9ffc-147">When a change occurs to the indicated object of the type represented in  _ulEventMask_, a call is made to the **OnNotify** method of the advise sink pointed to by  _lpAdviseSink_.</span></span> <span data-ttu-id="c9ffc-148">Данные, переданные в структуру **уведомлений** в подпрограмму OnNotify, описывают событие. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c9ffc-148">Data passed in the **NOTIFICATION** structure to the **OnNotify** routine describes the event.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c9ffc-149">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="c9ffc-149">Notes to implementers</span></span>

<span data-ttu-id="c9ffc-150">Вы можете поддерживать уведомления с помощью интерфейса MAPI или без него.</span><span class="sxs-lookup"><span data-stu-id="c9ffc-150">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="c9ffc-151">В MAPI есть три метода поддержки объектов, которые помогают поставщикам услуг реализовать уведомления:</span><span class="sxs-lookup"><span data-stu-id="c9ffc-151">MAPI has three support object methods to help service providers implement notification:</span></span>
  
- [<span data-ttu-id="c9ffc-152">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="c9ffc-152">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
    
- [<span data-ttu-id="c9ffc-153">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="c9ffc-153">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)
    
- [<span data-ttu-id="c9ffc-154">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="c9ffc-154">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
    
<span data-ttu-id="c9ffc-155">Если вы намерены использовать методы поддержки MAPI, вызовите **подписку** при вызове метода **advise** и освободите указатель _лпадвисесинк_ .</span><span class="sxs-lookup"><span data-stu-id="c9ffc-155">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="c9ffc-156">Если вы хотите самостоятельно поддерживать уведомления, вызовите метод **AddRef** приемника уведомлений, представленный параметром _лпадвисесинк_ , чтобы сохранить копию этого указателя.</span><span class="sxs-lookup"><span data-stu-id="c9ffc-156">If you elect to support notification yourself, call the **AddRef** method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="c9ffc-157">Сохраняйте эту копию до тех пор, пока не будет вызван метод [иаблогон:: unadvise](iablogon-unadvise.md) для отмены регистрации.</span><span class="sxs-lookup"><span data-stu-id="c9ffc-157">Maintain this copy until your [IABLogon::Unadvise](iablogon-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="c9ffc-158">Независимо от того, как вы можете поддерживать уведомления, назначьте ненулевой номер подключения для регистрации уведомлений и верните его в параметр _лпулконнектион_ .</span><span class="sxs-lookup"><span data-stu-id="c9ffc-158">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="c9ffc-159">Не освобождайте этот номер подключения, пока не будет вызван метод **unadvise** .</span><span class="sxs-lookup"><span data-stu-id="c9ffc-159">Do not release this connection number until the **Unadvise** method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c9ffc-160">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="c9ffc-160">Notes to callers</span></span>

<span data-ttu-id="c9ffc-161">Указатель приемника уведомлений, который передается с помощью параметра \*\*\*\* _лпадвисесинк_ , можно указать на созданный объект или с помощью MAPI, созданного с помощью функции [хрсиссреададвисесинк](hrthisthreadadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="c9ffc-161">The advise sink pointer that you pass in the  _lpAdviseSink_ parameter to **Advise** can point to an object that you have created or that MAPI has created through the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> <span data-ttu-id="c9ffc-162">Вы можете использовать **хрсиссреададвисесинк** , если вы поддерживаете несколько потоков выполнения и хотите убедиться в том, что последующие вызовы метода OnNotify \*\*\*\* выполняются в соответствующее время в соответствующем потоке.</span><span class="sxs-lookup"><span data-stu-id="c9ffc-162">You might want to use **HrThisThreadAdviseSink** if you support multiple threads of execution and want to be sure that that subsequent calls to your **OnNotify** method occur at an appropriate time on an appropriate thread.</span></span> 
  
<span data-ttu-id="c9ffc-163">Будьте готовы к выпуску вашего объекта приемника уведомлений в любое время после вызова **advise** и перед вызовом метода \*\*\*\* unadvise.</span><span class="sxs-lookup"><span data-stu-id="c9ffc-163">Be prepared for your advise sink object to be released any time after your call to **Advise** and before your call to **Unadvise**.</span></span> <span data-ttu-id="c9ffc-164">Поэтому следует освободить объект приемника уведомлений после возврата по \*\*\*\* нажатию, если для него не задано конкретное долгосрочное использование.</span><span class="sxs-lookup"><span data-stu-id="c9ffc-164">Therefore, you should release your advise sink object after **Advise** returns, unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="c9ffc-165">Дополнительные сведения о процессе уведомления можно найти в статье [уведомление о событии в MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="c9ffc-165">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="c9ffc-166">Сведения о том, как использовать методы **имаписуппорт** для поддержки уведомлений, можно узнать в разделе [Поддержка уведомлений о событиях](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="c9ffc-166">For information about how to use the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span> <span data-ttu-id="c9ffc-167">Для получения дополнительных сведений о многопоточности и MAPI см. [](threading-in-mapi.md)</span><span class="sxs-lookup"><span data-stu-id="c9ffc-167">For more information about multithreading and MAPI, see [Threading in MAPI](threading-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c9ffc-168">См. также</span><span class="sxs-lookup"><span data-stu-id="c9ffc-168">See also</span></span>



[<span data-ttu-id="c9ffc-169">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="c9ffc-169">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="c9ffc-170">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="c9ffc-170">IABLogon::Unadvise</span></span>](iablogon-unadvise.md)
  
[<span data-ttu-id="c9ffc-171">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="c9ffc-171">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="c9ffc-172">�����������</span><span class="sxs-lookup"><span data-stu-id="c9ffc-172">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="c9ffc-173">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c9ffc-173">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

