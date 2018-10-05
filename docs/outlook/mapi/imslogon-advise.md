---
title: IMSLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Advise
api_type:
- COM
ms.assetid: a3c5d937-642b-463b-b5a0-5d099e651895
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: abe4867b965f05e781f931d2e72920474d007d78
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382759"
---
# <a name="imslogonadvise"></a><span data-ttu-id="7a0ea-103">IMSLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="7a0ea-103">IMSLogon::Advise</span></span>

  
  
<span data-ttu-id="7a0ea-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a0ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a0ea-105">Регистрирует объект поставщика хранилища сообщений для уведомлений об изменениях в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="7a0ea-105">Registers an object with a message store provider for notifications about changes in the message store.</span></span> <span data-ttu-id="7a0ea-106">Хранилище сообщений будет отправлять уведомления об изменениях зарегистрированных объект.</span><span class="sxs-lookup"><span data-stu-id="7a0ea-106">The message store will then send notifications about changes to the registered object.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="7a0ea-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a0ea-107">Parameters</span></span>

 <span data-ttu-id="7a0ea-108">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="7a0ea-108">_cbEntryID_</span></span>
  
> <span data-ttu-id="7a0ea-109">[in] Размер в байтах, идентификатор записи, на который указывает параметр _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="7a0ea-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="7a0ea-110">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="7a0ea-110">_lpEntryID_</span></span>
  
> <span data-ttu-id="7a0ea-111">[in] Указатель на идентификатор записи о том, какие следует создавать уведомления объекта.</span><span class="sxs-lookup"><span data-stu-id="7a0ea-111">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span> <span data-ttu-id="7a0ea-112">Этот объект можно папки, сообщение или любого другого объекта в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="7a0ea-112">This object can be a folder, a message, or any other object in the message store.</span></span> <span data-ttu-id="7a0ea-113">Кроме того Если MAPI задается параметр _cbEntryID_ 0 и передает **значение null** для _lpEntryID_, приемник уведомлений предоставляет уведомления об изменениях в хранилище всего сообщения.</span><span class="sxs-lookup"><span data-stu-id="7a0ea-113">Alternatively, if MAPI sets the  _cbEntryID_ parameter to 0 and passes **null** for  _lpEntryID_, the advise sink provides notifications about changes to the entire message store.</span></span>
    
 <span data-ttu-id="7a0ea-114">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="7a0ea-114">_ulEventMask_</span></span>
  
> <span data-ttu-id="7a0ea-115">[in] Маски события типов событий уведомлений для объекта, о том, какие MAPI будет создавать уведомления.</span><span class="sxs-lookup"><span data-stu-id="7a0ea-115">[in] An event mask of the types of notification events occurring for the object about which MAPI will generate notifications.</span></span> <span data-ttu-id="7a0ea-116">Маска фильтр определенных случаев.</span><span class="sxs-lookup"><span data-stu-id="7a0ea-116">The mask filters specific cases.</span></span> <span data-ttu-id="7a0ea-117">Каждый тип события имеет структуру, связанные с ним, который содержит дополнительные сведения о событии.</span><span class="sxs-lookup"><span data-stu-id="7a0ea-117">Each event type has a structure associated with it that contains additional information about the event.</span></span> <span data-ttu-id="7a0ea-118">В следующей таблице перечислены типы возможных событий вместе с их соответствующие структуры.</span><span class="sxs-lookup"><span data-stu-id="7a0ea-118">The following table lists the possible event types along with their corresponding structures.</span></span>
    
|<span data-ttu-id="7a0ea-119">**Тип события уведомления**</span><span class="sxs-lookup"><span data-stu-id="7a0ea-119">**Notification event type**</span></span>|<span data-ttu-id="7a0ea-120">**Соответствующий структуры**</span><span class="sxs-lookup"><span data-stu-id="7a0ea-120">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7a0ea-121">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="7a0ea-121">fnevCriticalError</span></span>  <br/> |[<span data-ttu-id="7a0ea-122">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7a0ea-122">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="7a0ea-123">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="7a0ea-123">fnevNewMail</span></span>  <br/> |[<span data-ttu-id="7a0ea-124">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7a0ea-124">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="7a0ea-125">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="7a0ea-125">fnevObjectCreated</span></span>  <br/> |[<span data-ttu-id="7a0ea-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7a0ea-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="7a0ea-127">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="7a0ea-127">fnevObjectDeleted</span></span>  <br/> |[<span data-ttu-id="7a0ea-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7a0ea-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="7a0ea-129">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="7a0ea-129">fnevObjectModified</span></span>  <br/> |[<span data-ttu-id="7a0ea-130">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7a0ea-130">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="7a0ea-131">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="7a0ea-131">fnevObjectCopied</span></span>  <br/> |[<span data-ttu-id="7a0ea-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7a0ea-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="7a0ea-133">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="7a0ea-133">fnevObjectMoved</span></span>  <br/> |[<span data-ttu-id="7a0ea-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7a0ea-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="7a0ea-135">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="7a0ea-135">fnevSearchComplete</span></span>  <br/> |[<span data-ttu-id="7a0ea-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7a0ea-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="7a0ea-137">fnevStatusObjectModified</span><span class="sxs-lookup"><span data-stu-id="7a0ea-137">fnevStatusObjectModified</span></span>  <br/> |[<span data-ttu-id="7a0ea-138">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7a0ea-138">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
   
 <span data-ttu-id="7a0ea-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="7a0ea-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="7a0ea-140">[in] Указатель на объект приемника уведомлений будет вызываться при возникновении события для объекта сеанса, о том, какие запросил уведомление.</span><span class="sxs-lookup"><span data-stu-id="7a0ea-140">[in] A pointer to an advise sink object to be called when an event occurs for the session object about which notification has been requested.</span></span> <span data-ttu-id="7a0ea-141">Этот объект приемника уведомлений должны уже существовать.</span><span class="sxs-lookup"><span data-stu-id="7a0ea-141">This advise sink object must already exist.</span></span>
    
 <span data-ttu-id="7a0ea-142">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="7a0ea-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="7a0ea-143">[out] Указатель на переменную, которая после успешного возврата содержит номер подключения для регистрации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="7a0ea-143">[out] A pointer to a variable that upon a successful return holds the connection number for the notification registration.</span></span> <span data-ttu-id="7a0ea-144">Номер подключения должен быть отличное от нуля.</span><span class="sxs-lookup"><span data-stu-id="7a0ea-144">The connection number must be nonzero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7a0ea-145">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7a0ea-145">Return value</span></span>

<span data-ttu-id="7a0ea-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="7a0ea-146">S_OK</span></span> 
  
> <span data-ttu-id="7a0ea-147">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="7a0ea-147">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="7a0ea-148">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="7a0ea-148">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="7a0ea-149">Операция не поддерживается с MAPI или с одного или нескольких поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="7a0ea-149">The operation is not supported by MAPI or by one or more service providers.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7a0ea-150">Замечания</span><span class="sxs-lookup"><span data-stu-id="7a0ea-150">Remarks</span></span>

<span data-ttu-id="7a0ea-151">Поставщики хранилища сообщений реализуйте метод **IMSLogon::Advise** для регистрации объекта для обратных вызовов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="7a0ea-151">Message store providers implement the **IMSLogon::Advise** method to register an object for notification callbacks.</span></span> <span data-ttu-id="7a0ea-152">При каждом изменении на указанный объект, поставщик проверяет маска какие события было задано с помощью параметра _ulEventMask_ и, следовательно, какой тип изменения произошло.</span><span class="sxs-lookup"><span data-stu-id="7a0ea-152">Whenever a change occurs to the indicated object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and, therefore, what type of change occurred.</span></span> <span data-ttu-id="7a0ea-153">Если немного, поставщик вызывает метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) для объекта приемник уведомлений, указанное с помощью параметра _lpAdviseSink_ сообщение о событии.</span><span class="sxs-lookup"><span data-stu-id="7a0ea-153">If a bit is set, the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="7a0ea-154">Данные, передаваемые в структуре уведомлений в подпрограмму **OnNotify** описание события.</span><span class="sxs-lookup"><span data-stu-id="7a0ea-154">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="7a0ea-155">Вызов **OnNotify** может возникнуть во время звонка, которое изменяет объект или в любой момент позже.</span><span class="sxs-lookup"><span data-stu-id="7a0ea-155">The call to **OnNotify** can occur during the call that changes the object, or at any later time.</span></span> <span data-ttu-id="7a0ea-156">На компьютерах, поддерживающих многопоточной среде вызов **OnNotify** может выполняться на любой поток.</span><span class="sxs-lookup"><span data-stu-id="7a0ea-156">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="7a0ea-157">Безопасно обработка вызова **OnNotify** , который может произойти в неподходящее время, клиентское приложение должно использовать функцию [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="7a0ea-157">To safely handle a call to **OnNotify** that might happen at an inopportune time, a client application should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="7a0ea-158">Для предоставления уведомлений, объект приемника; рекомендаций поставщика хранилища сообщений, который реализует **уведомлений** необходимо сохранить копию указатель _lpAdviseSink_ для этого поставщика вызывает метод [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) для приемник уведомлений на обслуживание указателя на объект до отмены регистрации уведомлений с помощью вызова метода [IMSLogon::Unadvise](imslogon-unadvise.md) .</span><span class="sxs-lookup"><span data-stu-id="7a0ea-158">To provide notifications, the message store provider that implements **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, the provider calls the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMSLogon::Unadvise](imslogon-unadvise.md) method.</span></span> <span data-ttu-id="7a0ea-159">Реализации **уведомлений** следует присвоить номер подключения для регистрации уведомлений и вызов **AddRef** на этот номер подключения до возвращения в параметре _lpulConnection_ .</span><span class="sxs-lookup"><span data-stu-id="7a0ea-159">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="7a0ea-160">Поставщиков услуг можно освободить объект приемника уведомлений перед отменяется регистрация, но они не должны освобождать номер подключения до вызова **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="7a0ea-160">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until **Unadvise** has been called.</span></span> 
  
<span data-ttu-id="7a0ea-161">После вызова **уведомлений** прошло успешно, и перед **Unadvise** вызван поставщиков должен быть подготовлен для объекта приемник уведомлений нужно освободить.</span><span class="sxs-lookup"><span data-stu-id="7a0ea-161">After a call to **Advise** has succeeded and before **Unadvise** has been called, providers must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="7a0ea-162">Таким образом поставщика освобождать возвращается объект приемника уведомлений после возвращает **уведомлений** , если оно не имеет определенного длительного использования для него.</span><span class="sxs-lookup"><span data-stu-id="7a0ea-162">Therefore, a provider should release its advise sink object after **Advise** returns, unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="7a0ea-163">Дополнительные сведения о процессе уведомления содержатся в разделе [Уведомление о событии в MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="7a0ea-163">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7a0ea-164">См. также</span><span class="sxs-lookup"><span data-stu-id="7a0ea-164">See also</span></span>



[<span data-ttu-id="7a0ea-165">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="7a0ea-165">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="7a0ea-166">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="7a0ea-166">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="7a0ea-167">IMSLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="7a0ea-167">IMSLogon::Unadvise</span></span>](imslogon-unadvise.md)
  
[<span data-ttu-id="7a0ea-168">�����������</span><span class="sxs-lookup"><span data-stu-id="7a0ea-168">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="7a0ea-169">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7a0ea-169">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

