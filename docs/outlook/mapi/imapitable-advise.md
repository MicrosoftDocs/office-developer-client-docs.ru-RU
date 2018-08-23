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
ms.openlocfilehash: cd6b119bd88fccf80bf2488592a24b3398e6e8af
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594245"
---
# <a name="imapitableadvise"></a><span data-ttu-id="3b9a3-103">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="3b9a3-103">IMAPITable::Advise</span></span>

  
  
<span data-ttu-id="3b9a3-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b9a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b9a3-105">Регистрирует объект приемника уведомлений для получения уведомлений о влияния на таблице указанных событий.</span><span class="sxs-lookup"><span data-stu-id="3b9a3-105">Registers an advise sink object to receive notification of specified events affecting the table.</span></span>
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="3b9a3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b9a3-106">Parameters</span></span>

 <span data-ttu-id="3b9a3-107">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="3b9a3-107">_ulEventMask_</span></span>
  
> <span data-ttu-id="3b9a3-108">[in] Значение, указывающее тип события, которое будет создавать уведомления.</span><span class="sxs-lookup"><span data-stu-id="3b9a3-108">[in] Value indicating the type of event that will generate the notification.</span></span> <span data-ttu-id="3b9a3-109">Допустим только следующее значение:</span><span class="sxs-lookup"><span data-stu-id="3b9a3-109">Only the following value is valid:</span></span>
    
 `fnevTableModified`
  
 <span data-ttu-id="3b9a3-110">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="3b9a3-110">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="3b9a3-111">[in] Указатель на объект приемника уведомлений для последующих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3b9a3-111">[in] Pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="3b9a3-112">Этот объект приемника уведомлений должны уже выделено.</span><span class="sxs-lookup"><span data-stu-id="3b9a3-112">This advise sink object must have been already allocated.</span></span>
    
 <span data-ttu-id="3b9a3-113">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="3b9a3-113">_lpulConnection_</span></span>
  
> <span data-ttu-id="3b9a3-114">[out] Указатель на ненулевое значение, представляющее регистрации успешного уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3b9a3-114">[out] Pointer to a nonzero value that represents the successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3b9a3-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="3b9a3-115">Return value</span></span>

<span data-ttu-id="3b9a3-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="3b9a3-116">S_OK</span></span> 
  
> <span data-ttu-id="3b9a3-117">Регистрация уведомлений, успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="3b9a3-117">The notification registration successfully completed.</span></span>
    
<span data-ttu-id="3b9a3-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="3b9a3-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="3b9a3-119">Реализация таблицы не поддерживает изменения в его строках и столбцах или не поддерживает уведомления.</span><span class="sxs-lookup"><span data-stu-id="3b9a3-119">The table implementation either does not support changes to its rows and columns or does not support notification.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3b9a3-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="3b9a3-120">Remarks</span></span>

<span data-ttu-id="3b9a3-121">Используйте метод **IMAPITable::Advise** для регистрации объекта таблицы, реализованный в поставщик для обратных вызовов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3b9a3-121">Use the **IMAPITable::Advise** method to register a table object implemented in the provider for notification callbacks.</span></span> <span data-ttu-id="3b9a3-122">При каждом изменении объекта таблицы Поставщик проверяет маска какие события было задано с помощью параметра _ulEventMask_ и, следовательно, какой тип изменения произошло.</span><span class="sxs-lookup"><span data-stu-id="3b9a3-122">Whenever a change occurs to the table object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and thus what type of change occurred.</span></span> <span data-ttu-id="3b9a3-123">Если немного, поставщик вызывает метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) для объекта приемник уведомлений, указанное с помощью параметра _lpAdviseSink_ сообщение о событии.</span><span class="sxs-lookup"><span data-stu-id="3b9a3-123">If a bit is set, then the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="3b9a3-124">Данные, передаваемые в структуре уведомлений в подпрограмму **OnNotify** описание события.</span><span class="sxs-lookup"><span data-stu-id="3b9a3-124">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="3b9a3-125">Вызов **OnNotify** может возникнуть во время звонка, которое изменяет объект или в любое время следующей.</span><span class="sxs-lookup"><span data-stu-id="3b9a3-125">The call to **OnNotify** can occur during the call that changes the object, or at any following time.</span></span> <span data-ttu-id="3b9a3-126">На компьютерах, поддерживающих многопоточной среде вызов **OnNotify** может выполняться на любой поток.</span><span class="sxs-lookup"><span data-stu-id="3b9a3-126">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="3b9a3-127">Способ включить вызов **OnNotify** , который может произойти в неподходящее время в одну, который является более безопасной обработки поставщика следует использовать функцию [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="3b9a3-127">For a way to turn a call to **OnNotify** that might happen at an inopportune time into one that is safer to handle, a provider should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="3b9a3-128">Для предоставления уведомлений, объект приемника; рекомендаций поставщика реализации **уведомлений** необходимо сохранить копию указатель _lpAdviseSink_ для этого он вызывает метод **IUnknown::AddRef** для приемник уведомлений на обслуживание указателя на объект до отмены регистрации уведомлений с помощью вызова метода [IMAPITable::Unadvise](imapitable-unadvise.md) .</span><span class="sxs-lookup"><span data-stu-id="3b9a3-128">To provide notifications, the provider implementing **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, it calls the **IUnknown::AddRef** method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMAPITable::Unadvise](imapitable-unadvise.md) method.</span></span> <span data-ttu-id="3b9a3-129">Реализации **уведомлений** следует присвоить номер подключения для регистрации уведомлений и вызов **AddRef** на этот номер подключения до возвращения в параметре _lpulConnection_ .</span><span class="sxs-lookup"><span data-stu-id="3b9a3-129">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="3b9a3-130">Поставщиков услуг можно освободить объект приемника уведомлений перед отменяется регистрация, но они не нужно освободить номер подключения до ** Unadvise ** вызова.</span><span class="sxs-lookup"><span data-stu-id="3b9a3-130">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until ** Unadvise ** has been called.</span></span> 
  
<span data-ttu-id="3b9a3-131">После вызова **уведомлений** прошло успешно и перед ** Unadvise ** была вызванный, клиенты должны быть готовы для объекта приемник уведомлений нужно освободить.</span><span class="sxs-lookup"><span data-stu-id="3b9a3-131">After a call to **Advise** has succeeded and before ** Unadvise ** has been called, clients must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="3b9a3-132">Клиент таким образом освобождать возвращается объект приемника уведомлений после **уведомлений** возвращает только при наличии его определенным длительного использования для него.</span><span class="sxs-lookup"><span data-stu-id="3b9a3-132">A client should therefore release its advise sink object after **Advise** returns unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="3b9a3-133">Из-за асинхронного поведения уведомлений реализации, измените параметры столбца в таблице могут получать уведомления со сведениями, организованных в предыдущем порядок столбцов.</span><span class="sxs-lookup"><span data-stu-id="3b9a3-133">Because of the asynchronous behavior of notification, implementations that change table column settings can receive notifications with information organized in a previous column order.</span></span> <span data-ttu-id="3b9a3-134">Например строка таблицы могут возвращаться для сообщений, который только что был удален из контейнера.</span><span class="sxs-lookup"><span data-stu-id="3b9a3-134">For instance, a table row might be returned for a message that has just been deleted from the container.</span></span> <span data-ttu-id="3b9a3-135">Такие уведомления отправляется, когда было сделано это изменение параметра столбца и сведения о нем отправляются, но эти сведения еще не были добавлены в табличном представлении уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3b9a3-135">Such a notification is sent when the column setting change has been made and information about it sent but the notification table view has not been updated with that information yet.</span></span>
  
<span data-ttu-id="3b9a3-136">Дополнительные сведения о процессе уведомления видеть [Уведомления о событии в MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="3b9a3-136">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="3b9a3-137">Сведения о таблице уведомлений содержатся [Уведомления о таблице](about-table-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="3b9a3-137">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="3b9a3-138">Сведения об использовании методов **IMAPISupport** для поддержки уведомлений [Поддерживающие уведомления о событии](supporting-event-notification.md)см.</span><span class="sxs-lookup"><span data-stu-id="3b9a3-138">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3b9a3-139">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="3b9a3-139">MFCMAPI reference</span></span>

<span data-ttu-id="3b9a3-140">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="3b9a3-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3b9a3-141">**����**</span><span class="sxs-lookup"><span data-stu-id="3b9a3-141">**File**</span></span>|<span data-ttu-id="3b9a3-142">**�������**</span><span class="sxs-lookup"><span data-stu-id="3b9a3-142">**Function**</span></span>|<span data-ttu-id="3b9a3-143">**�����������**</span><span class="sxs-lookup"><span data-stu-id="3b9a3-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3b9a3-144">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="3b9a3-144">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="3b9a3-145">CContestTableListCtrl::NotificationOn</span><span class="sxs-lookup"><span data-stu-id="3b9a3-145">CContestTableListCtrl::NotificationOn</span></span>  <br/> |<span data-ttu-id="3b9a3-146">Mfcmapi (en) использует метод **IMAPITable::Advise** для регистрации уведомлений разрешить в табличном представлении, чтобы быть в курсе.</span><span class="sxs-lookup"><span data-stu-id="3b9a3-146">MFCMAPI uses the **IMAPITable::Advise** method to register for notifications to allow the table view to stay current.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b9a3-147">См. также</span><span class="sxs-lookup"><span data-stu-id="3b9a3-147">See also</span></span>



[<span data-ttu-id="3b9a3-148">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="3b9a3-148">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="3b9a3-149">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="3b9a3-149">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="3b9a3-150">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="3b9a3-150">IMAPITable::Unadvise</span></span>](imapitable-unadvise.md)
  
[<span data-ttu-id="3b9a3-151">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="3b9a3-151">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="3b9a3-152">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3b9a3-152">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="3b9a3-153">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="3b9a3-153">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

