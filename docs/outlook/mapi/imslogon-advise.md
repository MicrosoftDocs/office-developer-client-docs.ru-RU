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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317313"
---
# <a name="imslogonadvise"></a><span data-ttu-id="1216f-103">IMSLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="1216f-103">IMSLogon::Advise</span></span>

  
  
<span data-ttu-id="1216f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1216f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1216f-105">Регистрирует объект у поставщика store сообщений для уведомлений об изменениях в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="1216f-105">Registers an object with a message store provider for notifications about changes in the message store.</span></span> <span data-ttu-id="1216f-106">Затем хранилище сообщений будет отправлять уведомления об изменениях зарегистрированного объекта.</span><span class="sxs-lookup"><span data-stu-id="1216f-106">The message store will then send notifications about changes to the registered object.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="1216f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1216f-107">Parameters</span></span>

 <span data-ttu-id="1216f-108">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="1216f-108">_cbEntryID_</span></span>
  
> <span data-ttu-id="1216f-109">[in] Размер идентификатора записи в вайтах, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="1216f-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="1216f-110">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="1216f-110">_lpEntryID_</span></span>
  
> <span data-ttu-id="1216f-111">[in] Указатель на идентификатор записи объекта, о котором должны быть созданы уведомления.</span><span class="sxs-lookup"><span data-stu-id="1216f-111">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span> <span data-ttu-id="1216f-112">Этот объект может быть папкой, сообщением или любым другим объектом в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="1216f-112">This object can be a folder, a message, or any other object in the message store.</span></span> <span data-ttu-id="1216f-113">Кроме того, если MAPI задает для параметра  _cbEntryID_ 0 и передает **null** для  _lpEntryID,_ то в окну рекомендации будут отправляться уведомления об изменениях во всем хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="1216f-113">Alternatively, if MAPI sets the  _cbEntryID_ parameter to 0 and passes **null** for  _lpEntryID_, the advise sink provides notifications about changes to the entire message store.</span></span>
    
 <span data-ttu-id="1216f-114">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="1216f-114">_ulEventMask_</span></span>
  
> <span data-ttu-id="1216f-115">[in] Маска событий типов событий уведомлений, происходящих для объекта, для которого MAPI будет создавать уведомления.</span><span class="sxs-lookup"><span data-stu-id="1216f-115">[in] An event mask of the types of notification events occurring for the object about which MAPI will generate notifications.</span></span> <span data-ttu-id="1216f-116">Маска фильтрует определенные случаи.</span><span class="sxs-lookup"><span data-stu-id="1216f-116">The mask filters specific cases.</span></span> <span data-ttu-id="1216f-117">Каждый тип события имеет связанную с ним структуру, которая содержит дополнительные сведения о событии.</span><span class="sxs-lookup"><span data-stu-id="1216f-117">Each event type has a structure associated with it that contains additional information about the event.</span></span> <span data-ttu-id="1216f-118">В следующей таблице перечислены возможные типы событий, а также соответствующие структуры.</span><span class="sxs-lookup"><span data-stu-id="1216f-118">The following table lists the possible event types along with their corresponding structures.</span></span>
    
|<span data-ttu-id="1216f-119">**Тип события notification**</span><span class="sxs-lookup"><span data-stu-id="1216f-119">**Notification event type**</span></span>|<span data-ttu-id="1216f-120">**Соответствующая структура**</span><span class="sxs-lookup"><span data-stu-id="1216f-120">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1216f-121">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="1216f-121">fnevCriticalError</span></span>  <br/> |[<span data-ttu-id="1216f-122">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1216f-122">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="1216f-123">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="1216f-123">fnevNewMail</span></span>  <br/> |[<span data-ttu-id="1216f-124">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1216f-124">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="1216f-125">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="1216f-125">fnevObjectCreated</span></span>  <br/> |[<span data-ttu-id="1216f-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1216f-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="1216f-127">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="1216f-127">fnevObjectDeleted</span></span>  <br/> |[<span data-ttu-id="1216f-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1216f-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="1216f-129">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="1216f-129">fnevObjectModified</span></span>  <br/> |[<span data-ttu-id="1216f-130">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1216f-130">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="1216f-131">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="1216f-131">fnevObjectCopied</span></span>  <br/> |[<span data-ttu-id="1216f-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1216f-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="1216f-133">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="1216f-133">fnevObjectMoved</span></span>  <br/> |[<span data-ttu-id="1216f-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1216f-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="1216f-135">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="1216f-135">fnevSearchComplete</span></span>  <br/> |[<span data-ttu-id="1216f-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1216f-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="1216f-137">fnevStatusObjectModified</span><span class="sxs-lookup"><span data-stu-id="1216f-137">fnevStatusObjectModified</span></span>  <br/> |[<span data-ttu-id="1216f-138">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1216f-138">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
   
 <span data-ttu-id="1216f-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="1216f-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="1216f-140">[in] Указатель на объект-консультант, который будет вызван при событии объекта сеанса, о том, какое уведомление запрашивается.</span><span class="sxs-lookup"><span data-stu-id="1216f-140">[in] A pointer to an advise sink object to be called when an event occurs for the session object about which notification has been requested.</span></span> <span data-ttu-id="1216f-141">Этот рекомендуемый объект-тоник уже должен существовать.</span><span class="sxs-lookup"><span data-stu-id="1216f-141">This advise sink object must already exist.</span></span>
    
 <span data-ttu-id="1216f-142">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="1216f-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="1216f-143">[out] Указатель на переменную, которая после успешного возврата содержит номер подключения для регистрации уведомления.</span><span class="sxs-lookup"><span data-stu-id="1216f-143">[out] A pointer to a variable that upon a successful return holds the connection number for the notification registration.</span></span> <span data-ttu-id="1216f-144">Номер подключения должен быть неzero.</span><span class="sxs-lookup"><span data-stu-id="1216f-144">The connection number must be nonzero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1216f-145">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1216f-145">Return value</span></span>

<span data-ttu-id="1216f-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="1216f-146">S_OK</span></span> 
  
> <span data-ttu-id="1216f-147">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="1216f-147">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="1216f-148">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="1216f-148">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="1216f-149">Операция не поддерживается MAPI или одним или более поставщиками услуг.</span><span class="sxs-lookup"><span data-stu-id="1216f-149">The operation is not supported by MAPI or by one or more service providers.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1216f-150">Примечания</span><span class="sxs-lookup"><span data-stu-id="1216f-150">Remarks</span></span>

<span data-ttu-id="1216f-151">Поставщики store сообщений реализуют метод **IMSLogon::Advise** для регистрации объекта для методов вызова уведомлений.</span><span class="sxs-lookup"><span data-stu-id="1216f-151">Message store providers implement the **IMSLogon::Advise** method to register an object for notification callbacks.</span></span> <span data-ttu-id="1216f-152">При изменении заданного объекта поставщик проверяет, какой бит маски события был задан в параметре  _ulEventMask,_ и, следовательно, тип изменения.</span><span class="sxs-lookup"><span data-stu-id="1216f-152">Whenever a change occurs to the indicated object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and, therefore, what type of change occurred.</span></span> <span data-ttu-id="1216f-153">Если бит задан, поставщик вызывает метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) для объекта приемника рекомендации, заданного параметром  _lpAdviseSink,_ чтобы сообщить о событии.</span><span class="sxs-lookup"><span data-stu-id="1216f-153">If a bit is set, the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="1216f-154">Данные, переданные в структуре уведомлений процедуре **OnNotify,** описывают событие.</span><span class="sxs-lookup"><span data-stu-id="1216f-154">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="1216f-155">Вызов **OnNotify может** произойти во время вызова, который изменяет объект, или в любое время.</span><span class="sxs-lookup"><span data-stu-id="1216f-155">The call to **OnNotify** can occur during the call that changes the object, or at any later time.</span></span> <span data-ttu-id="1216f-156">В системах, поддерживаюх несколько потоков выполнения, вызов **OnNotify** может происходить в любом потоке.</span><span class="sxs-lookup"><span data-stu-id="1216f-156">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="1216f-157">Для безопасной обработки вызова **OnNotify,** который может произойти во время неоппортуна, клиентские приложения должны использовать функцию [HrThisThreadAdviseSink.](hrthisthreadadvisesink.md)</span><span class="sxs-lookup"><span data-stu-id="1216f-157">To safely handle a call to **OnNotify** that might happen at an inopportune time, a client application should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="1216f-158">Для предоставления уведомлений поставщику  store сообщений, который реализует advise, необходимо сохранить копию указателя на объект-замещение _lpAdviseSink;_ Для этого поставщик вызывает метод [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) для приемника консультаций, чтобы сохранить указатель на объект, пока регистрация уведомления не будет отменена с помощью вызова метода [IMSLogon::Unadvise.](imslogon-unadvise.md)</span><span class="sxs-lookup"><span data-stu-id="1216f-158">To provide notifications, the message store provider that implements **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, the provider calls the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMSLogon::Unadvise](imslogon-unadvise.md) method.</span></span> <span data-ttu-id="1216f-159">Реализация **advise** должна назначить номер подключения регистрации уведомлений и вызвать **AddRef** по этому номеру подключения, прежде чем возвращать его в _параметре lpulConnection._</span><span class="sxs-lookup"><span data-stu-id="1216f-159">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="1216f-160">Перед отменой регистрации поставщики услуг могут освободить объект-тонконсультант, но не должны отпускать номер подключения, пока не будет вызвана служба **Unadvise.**</span><span class="sxs-lookup"><span data-stu-id="1216f-160">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until **Unadvise** has been called.</span></span> 
  
<span data-ttu-id="1216f-161">После успешного  вызова "Консультация" и перед вызовом **Unadvise** поставщики должны быть готовы к тому, чтобы объект-сигнальный сигнал был отпущен.</span><span class="sxs-lookup"><span data-stu-id="1216f-161">After a call to **Advise** has succeeded and before **Unadvise** has been called, providers must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="1216f-162">Таким образом, поставщик должен освободить объект-сигнальный сигнал после возврата advise, если он не имеет определенного долгосрочного использования для него. </span><span class="sxs-lookup"><span data-stu-id="1216f-162">Therefore, a provider should release its advise sink object after **Advise** returns, unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="1216f-163">Дополнительные сведения о процессе уведомления см. в [уведомлении о событии в MAPI.](event-notification-in-mapi.md)</span><span class="sxs-lookup"><span data-stu-id="1216f-163">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1216f-164">См. также</span><span class="sxs-lookup"><span data-stu-id="1216f-164">See also</span></span>



[<span data-ttu-id="1216f-165">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="1216f-165">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="1216f-166">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="1216f-166">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="1216f-167">IMSLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="1216f-167">IMSLogon::Unadvise</span></span>](imslogon-unadvise.md)
  
[<span data-ttu-id="1216f-168">�����������</span><span class="sxs-lookup"><span data-stu-id="1216f-168">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="1216f-169">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1216f-169">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

