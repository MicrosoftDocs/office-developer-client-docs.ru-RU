---
title: имсгстореадвисе
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.Advise
api_type:
- COM
ms.assetid: 8c57e743-a798-4e39-a61a-46dff8b1ac7c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3b4abef731541e308b2c2ebc6f4aaddf4458e257
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317327"
---
# <a name="imsgstoreadvise"></a><span data-ttu-id="ba588-103">IMsgStore::Advise</span><span class="sxs-lookup"><span data-stu-id="ba588-103">IMsgStore::Advise</span></span>

  
  
<span data-ttu-id="ba588-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba588-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba588-105">Регистрируется для получения уведомлений об указанных событиях, влияющих на хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="ba588-105">Registers to receive notification of specified events that affect the message store.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="ba588-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba588-106">Parameters</span></span>

 <span data-ttu-id="ba588-107">_кбентрид_</span><span class="sxs-lookup"><span data-stu-id="ba588-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="ba588-108">возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="ba588-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ba588-109">_лпентрид_</span><span class="sxs-lookup"><span data-stu-id="ba588-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="ba588-110">возврата Указатель на идентификатор записи папки или сообщения о том, какие уведомления должны создаваться, или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ba588-110">[in] A pointer to the entry identifier of the folder or message about which notifications should be generated, or **null**.</span></span> <span data-ttu-id="ba588-111">Если для _лпентрид_ ЗАДАНО значение null, регистры **рекомендаций** для уведомлений для всего хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="ba588-111">If  _lpEntryID_ is set to NULL, **Advise** registers for notifications on the entire message store.</span></span> 
    
 <span data-ttu-id="ba588-112">_улевентмаск_</span><span class="sxs-lookup"><span data-stu-id="ba588-112">_ulEventMask_</span></span>
  
> <span data-ttu-id="ba588-113">возврата Маска значений, указывающая типы событий уведомлений, в которых заинтересован вызывающий абонент, которые необходимо включить в регистрацию.</span><span class="sxs-lookup"><span data-stu-id="ba588-113">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="ba588-114">Существует соответствующая структура [уведомлений](notification.md) , связанная с каждым типом события, в котором хранятся сведения о событии.</span><span class="sxs-lookup"><span data-stu-id="ba588-114">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="ba588-115">Ниже приведены допустимые значения параметра _улевентмаск_ .</span><span class="sxs-lookup"><span data-stu-id="ba588-115">The following are valid values for the  _ulEventMask_ parameter:</span></span> 
    
 <span data-ttu-id="ba588-116">_фневкритикалеррор_</span><span class="sxs-lookup"><span data-stu-id="ba588-116">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="ba588-117">Регистрирует уведомления о серьезных ошибках, таких как недостаток памяти.</span><span class="sxs-lookup"><span data-stu-id="ba588-117">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="ba588-118">_фневекстендед_</span><span class="sxs-lookup"><span data-stu-id="ba588-118">_fnevExtended_</span></span>
  
> <span data-ttu-id="ba588-119">Регистрирует уведомления о событиях, относящихся к определенному поставщику хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="ba588-119">Registers for notifications about events specific to the particular message store provider.</span></span>
    
 <span data-ttu-id="ba588-120">_фневневмаил_</span><span class="sxs-lookup"><span data-stu-id="ba588-120">_fnevNewMail_</span></span>
  
> <span data-ttu-id="ba588-121">Регистрирует уведомления о поступлении новых сообщений.</span><span class="sxs-lookup"><span data-stu-id="ba588-121">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="ba588-122">_фневобжекткреатед_</span><span class="sxs-lookup"><span data-stu-id="ba588-122">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="ba588-123">Регистрирует уведомления о создании новой папки или сообщения.</span><span class="sxs-lookup"><span data-stu-id="ba588-123">Registers for notifications about the creation of a new folder or message.</span></span>
    
 <span data-ttu-id="ba588-124">_фневобжекткопиед_</span><span class="sxs-lookup"><span data-stu-id="ba588-124">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="ba588-125">Регистрирует уведомления о копируемых папках или сообщениях.</span><span class="sxs-lookup"><span data-stu-id="ba588-125">Registers for notifications about a folder or message being copied.</span></span>
    
 <span data-ttu-id="ba588-126">_фневобжектделетед_</span><span class="sxs-lookup"><span data-stu-id="ba588-126">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="ba588-127">Регистрирует уведомления об удалении папки или сообщения.</span><span class="sxs-lookup"><span data-stu-id="ba588-127">Registers for notifications about a folder or message being deleted.</span></span>
    
 <span data-ttu-id="ba588-128">_фневобжектмодифиед_</span><span class="sxs-lookup"><span data-stu-id="ba588-128">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="ba588-129">Регистрирует уведомления об изменении папки или сообщения.</span><span class="sxs-lookup"><span data-stu-id="ba588-129">Registers for notifications about a folder or message being modified.</span></span>
    
 <span data-ttu-id="ba588-130">_фневобжектмовед_</span><span class="sxs-lookup"><span data-stu-id="ba588-130">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="ba588-131">Регистрирует уведомления о перемещении папки или сообщения.</span><span class="sxs-lookup"><span data-stu-id="ba588-131">Registers for notifications about a folder or message being moved.</span></span>
    
 <span data-ttu-id="ba588-132">_фневсеарчкомплете_</span><span class="sxs-lookup"><span data-stu-id="ba588-132">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="ba588-133">Регистрирует уведомления о завершении операции поиска.</span><span class="sxs-lookup"><span data-stu-id="ba588-133">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="ba588-134">_лпадвисесинк_</span><span class="sxs-lookup"><span data-stu-id="ba588-134">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="ba588-135">возврата Указатель на объект приемника уведомлений для получения последующих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ba588-135">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="ba588-136">Этот объект приемника уведомлений должен быть уже выделен.</span><span class="sxs-lookup"><span data-stu-id="ba588-136">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="ba588-137">_лпулконнектион_</span><span class="sxs-lookup"><span data-stu-id="ba588-137">_lpulConnection_</span></span>
  
> <span data-ttu-id="ba588-138">вышли Указатель на ненулевое число, которое представляет соединение между объектом приемника уведомлений вызывающего абонента и сеансом.</span><span class="sxs-lookup"><span data-stu-id="ba588-138">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span> 
    
 <span data-ttu-id="ba588-139">_лпадвисесинк_</span><span class="sxs-lookup"><span data-stu-id="ba588-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="ba588-140">возврата Указатель на объект приемника уведомлений для получения последующих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ba588-140">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="ba588-141">Этот объект приемника уведомлений должен быть уже выделен.</span><span class="sxs-lookup"><span data-stu-id="ba588-141">This advise sink object must have already been allocated.</span></span> 
    
 <span data-ttu-id="ba588-142">_лпулконнектион_</span><span class="sxs-lookup"><span data-stu-id="ba588-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="ba588-143">вышли Указатель на ненулевый номер подключения, представляющий соединение между объектом приемника уведомлений вызывающего абонента и хранилищем сообщений.</span><span class="sxs-lookup"><span data-stu-id="ba588-143">[out] A pointer to a nonzero connection number that represents the connection between the caller's advise sink object and the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ba588-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ba588-144">Return value</span></span>

<span data-ttu-id="ba588-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="ba588-145">S_OK</span></span> 
  
> <span data-ttu-id="ba588-146">Регистрация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="ba588-146">The registration was successful.</span></span>
    
<span data-ttu-id="ba588-147">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="ba588-147">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="ba588-148">Поставщик хранилища сообщений не поддерживает регистрацию для уведомления в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="ba588-148">The message store provider does not support registration for notification through the message store.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ba588-149">Примечания</span><span class="sxs-lookup"><span data-stu-id="ba588-149">Remarks</span></span>

<span data-ttu-id="ba588-150">Метод **IMsgStore:: Advise** устанавливает соединение между объектом приемника уведомлений вызывающего абонента и либо хранилищем сообщений, либо объектом в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="ba588-150">The **IMsgStore::Advise** method establishes a connection between the caller's advise sink object and either the message store or an object in the message store.</span></span> <span data-ttu-id="ba588-151">Это подключение используется для отправки уведомлений в приемник уведомлений, когда одно или несколько событий, указанных в параметре _улевентмаск_ , происходят с исходным объектом Advise.</span><span class="sxs-lookup"><span data-stu-id="ba588-151">This connection is used to send notifications to the advise sink when one or more events, as specified in the  _ulEventMask_ parameter, occur to the advise source object.</span></span> <span data-ttu-id="ba588-152">Если параметр _лпентрид_ указывает на допустимый идентификатор записи, источником рекомендаций является объект, идентифицируемый этим идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="ba588-152">When the  _lpEntryID_ parameter points to a valid entry identifier, the advise source is the object identified by this entry identifier.</span></span> <span data-ttu-id="ba588-153">Если _лпентрид_ имеет значение null, то источником уведомления является хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="ba588-153">When  _lpEntryID_ is NULL, the advise source is the message store.</span></span> 
  
<span data-ttu-id="ba588-154">Чтобы отправить уведомление, поставщик хранилища сообщений или MAPI вызывает зарегистрированный метод [имапиадвисесинк:: OnNotify](imapiadvisesink-onnotify.md) приемника уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ba588-154">To send a notification, either the message store provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="ba588-155">Один из параметров для параметра **OnNotify**, структура уведомления содержит сведения, описывающие конкретное событие.</span><span class="sxs-lookup"><span data-stu-id="ba588-155">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ba588-156">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="ba588-156">Notes to implementers</span></span>

<span data-ttu-id="ba588-157">Вы можете поддерживать уведомления с помощью интерфейса MAPI или без него.</span><span class="sxs-lookup"><span data-stu-id="ba588-157">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="ba588-158">В MAPI есть три метода поддержки объектов для оказания помощи поставщикам услуг по внедрению уведомлений: [имаписуппорт:: Subscribe](imapisupport-subscribe.md), [имаписуппорт:: unsubscribe](imapisupport-unsubscribe.md)и [имаписуппорт:: notify](imapisupport-notify.md).</span><span class="sxs-lookup"><span data-stu-id="ba588-158">MAPI has three support object methods for helping service providers implement notification: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md), and [IMAPISupport::Notify](imapisupport-notify.md).</span></span> <span data-ttu-id="ba588-159">Если вы намерены использовать методы поддержки MAPI, вызовите **подписку** при вызове метода **advise** и освободите указатель _лпадвисесинк_ .</span><span class="sxs-lookup"><span data-stu-id="ba588-159">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="ba588-160">Если вы хотите самостоятельно поддерживать уведомления, вызовите метод [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) приемника уведомлений, представленный параметром _лпадвисесинк_ , чтобы сохранить копию этого указателя.</span><span class="sxs-lookup"><span data-stu-id="ba588-160">If you elect to support notification yourself, call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="ba588-161">Сохраняйте эту копию до тех пор, пока не будет вызван метод [IMsgStore:: unadvise](imsgstore-unadvise.md) для отмены регистрации.</span><span class="sxs-lookup"><span data-stu-id="ba588-161">Maintain this copy until your [IMsgStore::Unadvise](imsgstore-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="ba588-162">Независимо от того, как вы можете поддерживать уведомления, назначьте ненулевой номер подключения для регистрации уведомлений и верните его в параметр _лпулконнектион_ .</span><span class="sxs-lookup"><span data-stu-id="ba588-162">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="ba588-163">Не освобождайте этот номер подключения, пока не будет вызвано и завершено действие **unadvise** .</span><span class="sxs-lookup"><span data-stu-id="ba588-163">Do not release this connection number until **Unadvise** has been called and has completed.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ba588-164">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="ba588-164">Notes to callers</span></span>

<span data-ttu-id="ba588-165">В системах, поддерживающих несколько потоков выполнения, вызов **OnNotify** также может выполняться в любом потоке в любое время.</span><span class="sxs-lookup"><span data-stu-id="ba588-165">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="ba588-166">Если необходимо гарантировать, что уведомления происходят только в определенный момент в определенном потоке, вызовите функцию [хрсиссреададвисесинк](hrthisthreadadvisesink.md) , чтобы создать объект приемника уведомлений, который вы передаете в предложение **advise**.</span><span class="sxs-lookup"><span data-stu-id="ba588-166">If you must be assured that notifications occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to **Advise**.</span></span> 
  
<span data-ttu-id="ba588-167">После успешного выполнения вызова **advise** и вызова **метода Unadvise для** отмены регистрации необходимо подготовить объект приемника уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ba588-167">After a call to **Advise** has succeeded and before **Unadvise** has been called to cancel the registration, be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="ba588-168">Вы должны освободить объект приемника **уведомлений после возврата,** если для него не задано конкретное долгосрочное использование.</span><span class="sxs-lookup"><span data-stu-id="ba588-168">You should release your advise sink object after **Advise** returns unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="ba588-169">Дополнительные сведения о процессе уведомления можно найти в статье [уведомление о событии в MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="ba588-169">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="ba588-170">Более подробную информацию об обработке уведомлений можно узнать в статье [обработка уведомлений](handling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="ba588-170">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ba588-171">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ba588-171">MFCMAPI reference</span></span>

<span data-ttu-id="ba588-172">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="ba588-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ba588-173">**Файл**</span><span class="sxs-lookup"><span data-stu-id="ba588-173">**File**</span></span>|<span data-ttu-id="ba588-174">**Функция**</span><span class="sxs-lookup"><span data-stu-id="ba588-174">**Function**</span></span>|<span data-ttu-id="ba588-175">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="ba588-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ba588-176">Баседиалог. cpp</span><span class="sxs-lookup"><span data-stu-id="ba588-176">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="ba588-177">Кбаседиалог:: Оннотификатионсон</span><span class="sxs-lookup"><span data-stu-id="ba588-177">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="ba588-178">MFCMAPI использует метод **IMsgStore:: Advise** для регистрации уведомлений во всем хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="ba588-178">MFCMAPI uses the **IMsgStore::Advise** method to register for notifications on the entire message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba588-179">См. также</span><span class="sxs-lookup"><span data-stu-id="ba588-179">See also</span></span>



[<span data-ttu-id="ba588-180">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="ba588-180">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="ba588-181">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="ba588-181">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="ba588-182">IMsgStore::Unadvise</span><span class="sxs-lookup"><span data-stu-id="ba588-182">IMsgStore::Unadvise</span></span>](imsgstore-unadvise.md)
  
[<span data-ttu-id="ba588-183">�����������</span><span class="sxs-lookup"><span data-stu-id="ba588-183">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="ba588-184">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ba588-184">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="ba588-185">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="ba588-185">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

