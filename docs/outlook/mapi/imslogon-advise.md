---
title: имслогонадвисе
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
# <a name="imslogonadvise"></a><span data-ttu-id="c63bc-103">IMSLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="c63bc-103">IMSLogon::Advise</span></span>

  
  
<span data-ttu-id="c63bc-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c63bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c63bc-105">Регистрирует объект с поставщиком хранилища сообщений для уведомлений об изменениях в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="c63bc-105">Registers an object with a message store provider for notifications about changes in the message store.</span></span> <span data-ttu-id="c63bc-106">После этого хранилище сообщений будет отправлять уведомления об изменениях в зарегистрированном объекте.</span><span class="sxs-lookup"><span data-stu-id="c63bc-106">The message store will then send notifications about changes to the registered object.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="c63bc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c63bc-107">Parameters</span></span>

 <span data-ttu-id="c63bc-108">_кбентрид_</span><span class="sxs-lookup"><span data-stu-id="c63bc-108">_cbEntryID_</span></span>
  
> <span data-ttu-id="c63bc-109">возврата Размер (в байтах) идентификатора записи, на который указывает параметр _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="c63bc-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="c63bc-110">_лпентрид_</span><span class="sxs-lookup"><span data-stu-id="c63bc-110">_lpEntryID_</span></span>
  
> <span data-ttu-id="c63bc-111">возврата Указатель на идентификатор записи объекта, для которого необходимо создать уведомления.</span><span class="sxs-lookup"><span data-stu-id="c63bc-111">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span> <span data-ttu-id="c63bc-112">Этот объект может быть папкой, сообщением или любым другим объектом в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="c63bc-112">This object can be a folder, a message, or any other object in the message store.</span></span> <span data-ttu-id="c63bc-113">Кроме того, если MAPI задает для параметра _кбентрид_ значение 0 и передает **значение NULL** для _лпентрид_, приемник уведомлений предоставляет уведомления об изменениях во всем хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="c63bc-113">Alternatively, if MAPI sets the  _cbEntryID_ parameter to 0 and passes **null** for  _lpEntryID_, the advise sink provides notifications about changes to the entire message store.</span></span>
    
 <span data-ttu-id="c63bc-114">_улевентмаск_</span><span class="sxs-lookup"><span data-stu-id="c63bc-114">_ulEventMask_</span></span>
  
> <span data-ttu-id="c63bc-115">возврата Маска событий типов событий уведомления, происходящих для объекта, сведения о том, какие MAPI будут создавать уведомления.</span><span class="sxs-lookup"><span data-stu-id="c63bc-115">[in] An event mask of the types of notification events occurring for the object about which MAPI will generate notifications.</span></span> <span data-ttu-id="c63bc-116">Маска фильтрует конкретные варианты.</span><span class="sxs-lookup"><span data-stu-id="c63bc-116">The mask filters specific cases.</span></span> <span data-ttu-id="c63bc-117">С каждым типом события связана структура, содержащая дополнительные сведения о событии.</span><span class="sxs-lookup"><span data-stu-id="c63bc-117">Each event type has a structure associated with it that contains additional information about the event.</span></span> <span data-ttu-id="c63bc-118">В следующей таблице приведены возможные типы событий и соответствующие им структуры.</span><span class="sxs-lookup"><span data-stu-id="c63bc-118">The following table lists the possible event types along with their corresponding structures.</span></span>
    
|<span data-ttu-id="c63bc-119">**Тип события уведомления**</span><span class="sxs-lookup"><span data-stu-id="c63bc-119">**Notification event type**</span></span>|<span data-ttu-id="c63bc-120">**Соответствующая структура**</span><span class="sxs-lookup"><span data-stu-id="c63bc-120">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c63bc-121">фневкритикалеррор</span><span class="sxs-lookup"><span data-stu-id="c63bc-121">fnevCriticalError</span></span>  <br/> |[<span data-ttu-id="c63bc-122">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c63bc-122">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="c63bc-123">фневневмаил</span><span class="sxs-lookup"><span data-stu-id="c63bc-123">fnevNewMail</span></span>  <br/> |[<span data-ttu-id="c63bc-124">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c63bc-124">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="c63bc-125">фневобжекткреатед</span><span class="sxs-lookup"><span data-stu-id="c63bc-125">fnevObjectCreated</span></span>  <br/> |[<span data-ttu-id="c63bc-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c63bc-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="c63bc-127">фневобжектделетед</span><span class="sxs-lookup"><span data-stu-id="c63bc-127">fnevObjectDeleted</span></span>  <br/> |[<span data-ttu-id="c63bc-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c63bc-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="c63bc-129">фневобжектмодифиед</span><span class="sxs-lookup"><span data-stu-id="c63bc-129">fnevObjectModified</span></span>  <br/> |[<span data-ttu-id="c63bc-130">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c63bc-130">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="c63bc-131">фневобжекткопиед</span><span class="sxs-lookup"><span data-stu-id="c63bc-131">fnevObjectCopied</span></span>  <br/> |[<span data-ttu-id="c63bc-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c63bc-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="c63bc-133">фневобжектмовед</span><span class="sxs-lookup"><span data-stu-id="c63bc-133">fnevObjectMoved</span></span>  <br/> |[<span data-ttu-id="c63bc-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c63bc-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="c63bc-135">фневсеарчкомплете</span><span class="sxs-lookup"><span data-stu-id="c63bc-135">fnevSearchComplete</span></span>  <br/> |[<span data-ttu-id="c63bc-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c63bc-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="c63bc-137">фневстатусобжектмодифиед</span><span class="sxs-lookup"><span data-stu-id="c63bc-137">fnevStatusObjectModified</span></span>  <br/> |[<span data-ttu-id="c63bc-138">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c63bc-138">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
   
 <span data-ttu-id="c63bc-139">_лпадвисесинк_</span><span class="sxs-lookup"><span data-stu-id="c63bc-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="c63bc-140">возврата Указатель на объект приемника уведомлений, который вызывается при возникновении события для объекта Session, для которого было запрошено уведомление.</span><span class="sxs-lookup"><span data-stu-id="c63bc-140">[in] A pointer to an advise sink object to be called when an event occurs for the session object about which notification has been requested.</span></span> <span data-ttu-id="c63bc-141">Этот объект приемника уведомлений должен уже существовать.</span><span class="sxs-lookup"><span data-stu-id="c63bc-141">This advise sink object must already exist.</span></span>
    
 <span data-ttu-id="c63bc-142">_лпулконнектион_</span><span class="sxs-lookup"><span data-stu-id="c63bc-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="c63bc-143">вышли Указатель на переменную, которая после успешного возврата содержит номер подключения для регистрации уведомления.</span><span class="sxs-lookup"><span data-stu-id="c63bc-143">[out] A pointer to a variable that upon a successful return holds the connection number for the notification registration.</span></span> <span data-ttu-id="c63bc-144">Номер подключения должен быть ненулевым.</span><span class="sxs-lookup"><span data-stu-id="c63bc-144">The connection number must be nonzero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c63bc-145">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c63bc-145">Return value</span></span>

<span data-ttu-id="c63bc-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="c63bc-146">S_OK</span></span> 
  
> <span data-ttu-id="c63bc-147">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="c63bc-147">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="c63bc-148">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="c63bc-148">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="c63bc-149">Эта операция не поддерживается MAPI или одним или несколькими поставщиками услуг.</span><span class="sxs-lookup"><span data-stu-id="c63bc-149">The operation is not supported by MAPI or by one or more service providers.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c63bc-150">Примечания</span><span class="sxs-lookup"><span data-stu-id="c63bc-150">Remarks</span></span>

<span data-ttu-id="c63bc-151">Поставщики хранилища сообщений реализуют метод **имслогон:: Advise** для регистрации объекта для обратных вызовов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c63bc-151">Message store providers implement the **IMSLogon::Advise** method to register an object for notification callbacks.</span></span> <span data-ttu-id="c63bc-152">При каждом изменении указанного объекта поставщик проверяет, какой бит маски события был задан в параметре _улевентмаск_ , и, соответственно, какого типа произошло изменение.</span><span class="sxs-lookup"><span data-stu-id="c63bc-152">Whenever a change occurs to the indicated object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and, therefore, what type of change occurred.</span></span> <span data-ttu-id="c63bc-153">Если задан бит, поставщик вызывает метод [имапиадвисесинк:: OnNotify](imapiadvisesink-onnotify.md) для объекта приемника уведомлений, указанного параметром _лпадвисесинк_ , чтобы сообщить о событии.</span><span class="sxs-lookup"><span data-stu-id="c63bc-153">If a bit is set, the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="c63bc-154">Данные, переданные в структуру уведомлений в подпрограмму **OnNotify** , описывают событие.</span><span class="sxs-lookup"><span data-stu-id="c63bc-154">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="c63bc-155">Вызов **OnNotify** может выполняться во время вызова, который изменяет объект или в любое время позже.</span><span class="sxs-lookup"><span data-stu-id="c63bc-155">The call to **OnNotify** can occur during the call that changes the object, or at any later time.</span></span> <span data-ttu-id="c63bc-156">В системах, поддерживающих несколько потоков выполнения, вызов **OnNotify** может выполняться в любом потоке.</span><span class="sxs-lookup"><span data-stu-id="c63bc-156">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="c63bc-157">Для безопасной обработки вызовов **OnNotify** , которые могут произойти во время иноппортуне, клиентское приложение должно использовать функцию [хрсиссреададвисесинк](hrthisthreadadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="c63bc-157">To safely handle a call to **OnNotify** that might happen at an inopportune time, a client application should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="c63bc-158">Для предоставления уведомлений поставщик хранилища сообщений, который реализует **advise** , должен хранить копию указателя на объект приемника уведомлений _лпадвисесинк_ ; для этого поставщик вызывает метод [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) для приемника уведомлений, чтобы сохранить указатель на объект до тех пор, пока регистрация уведомлений не будет отменена с помощью вызова метода [имслогон:: unadvise](imslogon-unadvise.md) .</span><span class="sxs-lookup"><span data-stu-id="c63bc-158">To provide notifications, the message store provider that implements **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, the provider calls the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMSLogon::Unadvise](imslogon-unadvise.md) method.</span></span> <span data-ttu-id="c63bc-159">При реализации **рекомендаций** необходимо назначить номер подключения для регистрации уведомлений и **AddRef** вызовов для этого номера подключения, прежде чем возвратить его в параметре _лпулконнектион_ .</span><span class="sxs-lookup"><span data-stu-id="c63bc-159">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="c63bc-160">Поставщики услуг могут освободить объект приемника уведомлений, прежде чем регистрация будет отменена, но не должна освобождать номер подключения, пока не будет вызвано предложение **unadvise** .</span><span class="sxs-lookup"><span data-stu-id="c63bc-160">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until **Unadvise** has been called.</span></span> 
  
<span data-ttu-id="c63bc-161">После успешного вызова метода **advise** и вызова метода **unadvise** поставщики должны подготовиться к выпуску объекта приемника уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c63bc-161">After a call to **Advise** has succeeded and before **Unadvise** has been called, providers must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="c63bc-162">Таким образом, поставщик должен освободить объект приемника **уведомлений после возврата,** если для него не задано конкретное долговременное использование.</span><span class="sxs-lookup"><span data-stu-id="c63bc-162">Therefore, a provider should release its advise sink object after **Advise** returns, unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="c63bc-163">Дополнительные сведения о процессе уведомления можно найти в статье [уведомление о событии в MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="c63bc-163">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c63bc-164">См. также</span><span class="sxs-lookup"><span data-stu-id="c63bc-164">See also</span></span>



[<span data-ttu-id="c63bc-165">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="c63bc-165">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="c63bc-166">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="c63bc-166">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="c63bc-167">IMSLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="c63bc-167">IMSLogon::Unadvise</span></span>](imslogon-unadvise.md)
  
[<span data-ttu-id="c63bc-168">�����������</span><span class="sxs-lookup"><span data-stu-id="c63bc-168">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="c63bc-169">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c63bc-169">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

