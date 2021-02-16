---
title: IMAPITableAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Advise
api_type:
- COM
ms.assetid: e8b5d21e-dc14-4b61-96b3-a51bcfa0d232
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c9401c163c74ab303ec39c147e0432d1979426b8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418815"
---
# <a name="imapitableadvise"></a><span data-ttu-id="ea952-103">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="ea952-103">IMAPITable::Advise</span></span>

  
  
<span data-ttu-id="ea952-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea952-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea952-105">Регистрирует объект приемника рекомендации для получения уведомлений об указанных событиях, влияющих на таблицу.</span><span class="sxs-lookup"><span data-stu-id="ea952-105">Registers an advise sink object to receive notification of specified events affecting the table.</span></span>
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="ea952-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea952-106">Parameters</span></span>

 <span data-ttu-id="ea952-107">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="ea952-107">_ulEventMask_</span></span>
  
> <span data-ttu-id="ea952-108">[in] Значение, указывающее тип события, которое будет создавать уведомление.</span><span class="sxs-lookup"><span data-stu-id="ea952-108">[in] Value indicating the type of event that will generate the notification.</span></span> <span data-ttu-id="ea952-109">Допустимо только следующее значение:</span><span class="sxs-lookup"><span data-stu-id="ea952-109">Only the following value is valid:</span></span>
    
 `fnevTableModified`
  
 <span data-ttu-id="ea952-110">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="ea952-110">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="ea952-111">[in] Указатель на объект приемника рекомендации для получения последующих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ea952-111">[in] Pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="ea952-112">Этот рекомендуемый объект-тоник должен быть уже выделен.</span><span class="sxs-lookup"><span data-stu-id="ea952-112">This advise sink object must have been already allocated.</span></span>
    
 <span data-ttu-id="ea952-113">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="ea952-113">_lpulConnection_</span></span>
  
> <span data-ttu-id="ea952-114">[out] Указатель на неживое значение, которое представляет успешную регистрацию уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ea952-114">[out] Pointer to a nonzero value that represents the successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ea952-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ea952-115">Return value</span></span>

<span data-ttu-id="ea952-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="ea952-116">S_OK</span></span> 
  
> <span data-ttu-id="ea952-117">Регистрация уведомлений успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="ea952-117">The notification registration successfully completed.</span></span>
    
<span data-ttu-id="ea952-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="ea952-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="ea952-119">Реализация таблицы либо не поддерживает изменения строк и столбцов, либо не поддерживает уведомления.</span><span class="sxs-lookup"><span data-stu-id="ea952-119">The table implementation either does not support changes to its rows and columns or does not support notification.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ea952-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="ea952-120">Remarks</span></span>

<span data-ttu-id="ea952-121">Используйте метод **IMAPITable::Advise,** чтобы зарегистрировать объект таблицы, реализованный в поставщике, для получения вызовов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ea952-121">Use the **IMAPITable::Advise** method to register a table object implemented in the provider for notification callbacks.</span></span> <span data-ttu-id="ea952-122">При изменении объекта таблицы поставщик проверяет, какой бит маски события был задан в параметре  _ulEventMask,_ и, таким образом, тип изменения.</span><span class="sxs-lookup"><span data-stu-id="ea952-122">Whenever a change occurs to the table object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and thus what type of change occurred.</span></span> <span data-ttu-id="ea952-123">Если бит задан, поставщик вызывает метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) для объекта приемника рекомендации, заданного параметром  _lpAdviseSink,_ чтобы сообщить о событии.</span><span class="sxs-lookup"><span data-stu-id="ea952-123">If a bit is set, then the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="ea952-124">Данные, переданные в структуре уведомлений процедуре **OnNotify,** описывают событие.</span><span class="sxs-lookup"><span data-stu-id="ea952-124">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="ea952-125">Вызов **OnNotify может** произойти во время вызова, который изменяет объект, или в любое следующее время.</span><span class="sxs-lookup"><span data-stu-id="ea952-125">The call to **OnNotify** can occur during the call that changes the object, or at any following time.</span></span> <span data-ttu-id="ea952-126">В системах, поддерживаюх несколько потоков выполнения, вызов **OnNotify** может происходить в любом потоке.</span><span class="sxs-lookup"><span data-stu-id="ea952-126">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="ea952-127">Чтобы сделать вызов **OnNotify,** который может произойти во время неоппортуны, более безопасным для обработки, поставщик должен использовать функцию [HrThisThreadAdviseSink.](hrthisthreadadvisesink.md)</span><span class="sxs-lookup"><span data-stu-id="ea952-127">For a way to turn a call to **OnNotify** that might happen at an inopportune time into one that is safer to handle, a provider should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="ea952-128">Для предоставления уведомлений поставщик, реализующий advise, должен сохранить копию указателя на _объект-сигнал lpAdviseSink;_  для этого он вызывает метод **IUnknown::AddRef** для приемника рекомендации, чтобы поддерживать указатель на объект, пока регистрация уведомлений не будет отменена вызовом метода [IMAPITable::Unadvise.](imapitable-unadvise.md)</span><span class="sxs-lookup"><span data-stu-id="ea952-128">To provide notifications, the provider implementing **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, it calls the **IUnknown::AddRef** method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMAPITable::Unadvise](imapitable-unadvise.md) method.</span></span> <span data-ttu-id="ea952-129">Реализация **advise** должна назначить номер подключения регистрации уведомлений и вызвать **AddRef** на этом номере подключения, прежде чем возвращать его в _параметре lpulConnection._</span><span class="sxs-lookup"><span data-stu-id="ea952-129">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="ea952-130">Поставщики услуг могут освободить объект-сигнальный сигнал до отмены регистрации, но не должны освободить номер подключения, пока не будет вызвана служба \*\* Unadvise \*\*.</span><span class="sxs-lookup"><span data-stu-id="ea952-130">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until \*\* Unadvise \*\* has been called.</span></span> 
  
<span data-ttu-id="ea952-131">After a call to **Advise** has succeeded and before \*\* Unadvise \*\* has been called, clients must be prepared for the advise sink object to be released.</span><span class="sxs-lookup"><span data-stu-id="ea952-131">After a call to **Advise** has succeeded and before \*\* Unadvise \*\* has been called, clients must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="ea952-132">Таким образом, клиент должен освободить  свой объект-тоник консультации после того, как advise возвращается, если он не имеет определенного долгосрочного использования для него.</span><span class="sxs-lookup"><span data-stu-id="ea952-132">A client should therefore release its advise sink object after **Advise** returns unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="ea952-133">Из-за асинхронного поведения уведомлений реализации, меняя параметры столбцов таблицы, могут получать уведомления с информацией, упорядоченной в предыдущем порядке столбца.</span><span class="sxs-lookup"><span data-stu-id="ea952-133">Because of the asynchronous behavior of notification, implementations that change table column settings can receive notifications with information organized in a previous column order.</span></span> <span data-ttu-id="ea952-134">Например, строка таблицы может быть возвращена для сообщения, которое только что было удалено из контейнера.</span><span class="sxs-lookup"><span data-stu-id="ea952-134">For instance, a table row might be returned for a message that has just been deleted from the container.</span></span> <span data-ttu-id="ea952-135">Такое уведомление отправляется, когда было внося изменение параметра столбца и отправлены сведения о нем, но представление таблицы уведомлений еще не было обновлено с этой информацией.</span><span class="sxs-lookup"><span data-stu-id="ea952-135">Such a notification is sent when the column setting change has been made and information about it sent but the notification table view has not been updated with that information yet.</span></span>
  
<span data-ttu-id="ea952-136">Дополнительные сведения о процессе уведомления см. в [уведомлении о событии в MAPI.](event-notification-in-mapi.md)</span><span class="sxs-lookup"><span data-stu-id="ea952-136">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="ea952-137">Конкретные сведения об уведомлении таблицы [см. в таблице уведомлений.](about-table-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="ea952-137">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="ea952-138">Сведения об использовании методов **IMAPISupport** для поддержки уведомлений см. в подразделе ["Поддержка уведомления о событии".](supporting-event-notification.md)</span><span class="sxs-lookup"><span data-stu-id="ea952-138">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ea952-139">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ea952-139">MFCMAPI reference</span></span>

<span data-ttu-id="ea952-140">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="ea952-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ea952-141">**Файл**</span><span class="sxs-lookup"><span data-stu-id="ea952-141">**File**</span></span>|<span data-ttu-id="ea952-142">**Функция**</span><span class="sxs-lookup"><span data-stu-id="ea952-142">**Function**</span></span>|<span data-ttu-id="ea952-143">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="ea952-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ea952-144">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="ea952-144">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="ea952-145">CContestTableListCtrl::NotificationOn</span><span class="sxs-lookup"><span data-stu-id="ea952-145">CContestTableListCtrl::NotificationOn</span></span>  <br/> |<span data-ttu-id="ea952-146">MFCMAPI использует метод **IMAPITable::Advise** для регистрации уведомлений, чтобы представление таблицы оставалась актуальным.</span><span class="sxs-lookup"><span data-stu-id="ea952-146">MFCMAPI uses the **IMAPITable::Advise** method to register for notifications to allow the table view to stay current.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ea952-147">См. также</span><span class="sxs-lookup"><span data-stu-id="ea952-147">See also</span></span>



[<span data-ttu-id="ea952-148">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="ea952-148">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="ea952-149">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="ea952-149">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="ea952-150">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="ea952-150">IMAPITable::Unadvise</span></span>](imapitable-unadvise.md)
  
[<span data-ttu-id="ea952-151">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="ea952-151">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="ea952-152">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ea952-152">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="ea952-153">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="ea952-153">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

