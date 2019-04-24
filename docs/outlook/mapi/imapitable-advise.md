---
title: Имапитаблеадвисе
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329022"
---
# <a name="imapitableadvise"></a><span data-ttu-id="f44bd-103">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="f44bd-103">IMAPITable::Advise</span></span>

  
  
<span data-ttu-id="f44bd-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f44bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f44bd-105">Регистрирует объект приемника уведомлений, чтобы получать уведомления о событиях, заданных на таблицу.</span><span class="sxs-lookup"><span data-stu-id="f44bd-105">Registers an advise sink object to receive notification of specified events affecting the table.</span></span>
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="f44bd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f44bd-106">Parameters</span></span>

 <span data-ttu-id="f44bd-107">_Улевентмаск_</span><span class="sxs-lookup"><span data-stu-id="f44bd-107">_ulEventMask_</span></span>
  
> <span data-ttu-id="f44bd-108">возврата Значение, указывающее тип события, которое будет создавать уведомление.</span><span class="sxs-lookup"><span data-stu-id="f44bd-108">[in] Value indicating the type of event that will generate the notification.</span></span> <span data-ttu-id="f44bd-109">Допустимы только следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f44bd-109">Only the following value is valid:</span></span>
    
 `fnevTableModified`
  
 <span data-ttu-id="f44bd-110">_Лпадвисесинк_</span><span class="sxs-lookup"><span data-stu-id="f44bd-110">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="f44bd-111">возврата Указатель на объект приемника уведомлений, чтобы получить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="f44bd-111">[in] Pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="f44bd-112">Этот объект приемника уведомлений должен быть уже выделен.</span><span class="sxs-lookup"><span data-stu-id="f44bd-112">This advise sink object must have been already allocated.</span></span>
    
 <span data-ttu-id="f44bd-113">_Лпулконнектион_</span><span class="sxs-lookup"><span data-stu-id="f44bd-113">_lpulConnection_</span></span>
  
> <span data-ttu-id="f44bd-114">вышли Указатель на ненулевое значение, представляющее успешную регистрацию уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f44bd-114">[out] Pointer to a nonzero value that represents the successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f44bd-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f44bd-115">Return value</span></span>

<span data-ttu-id="f44bd-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="f44bd-116">S_OK</span></span> 
  
> <span data-ttu-id="f44bd-117">Регистрация уведомления успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="f44bd-117">The notification registration successfully completed.</span></span>
    
<span data-ttu-id="f44bd-118">МАПИ_Е_НО_СУППОРТ</span><span class="sxs-lookup"><span data-stu-id="f44bd-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="f44bd-119">Реализация таблицы либо не поддерживает изменения строк и столбцов, либо не поддерживает уведомление.</span><span class="sxs-lookup"><span data-stu-id="f44bd-119">The table implementation either does not support changes to its rows and columns or does not support notification.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f44bd-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f44bd-120">Remarks</span></span>

<span data-ttu-id="f44bd-121">С помощью метода **IMAPITable:: Advise** можно зарегистрировать объект таблицы, реализованный в поставщике, для обратных вызовов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f44bd-121">Use the **IMAPITable::Advise** method to register a table object implemented in the provider for notification callbacks.</span></span> <span data-ttu-id="f44bd-122">При каждом изменении объекта Table поставщик проверяет, какой бит маски события был задан в параметре _улевентмаск_ , и, соответственно, тип изменения.</span><span class="sxs-lookup"><span data-stu-id="f44bd-122">Whenever a change occurs to the table object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and thus what type of change occurred.</span></span> <span data-ttu-id="f44bd-123">Если задан бит, то поставщик вызывает метод [имапиадвисесинк:: OnNotify](imapiadvisesink-onnotify.md) для объекта приемника уведомлений, указанного параметром _лпадвисесинк_ , чтобы сообщить о событии.</span><span class="sxs-lookup"><span data-stu-id="f44bd-123">If a bit is set, then the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="f44bd-124">Данные, переданные в структуру уведомлений в \*\*\*\* подпрограмму OnNotify, описывают событие.</span><span class="sxs-lookup"><span data-stu-id="f44bd-124">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="f44bd-125">Вызов onNotify \*\*\*\* может происходить во время вызова, в котором изменяется объект, или в любое время в следующий раз.</span><span class="sxs-lookup"><span data-stu-id="f44bd-125">The call to **OnNotify** can occur during the call that changes the object, or at any following time.</span></span> <span data-ttu-id="f44bd-126">В системах, поддерживающих несколько потоков выполнения, вызов onNotify \*\*\*\* может выполняться в любом потоке.</span><span class="sxs-lookup"><span data-stu-id="f44bd-126">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="f44bd-127">Чтобы включить функцию onNotify, которая может \*\*\*\* быть выполнена в иноппортуне, более безопасной для обработки, поставщик должен использовать функцию [хрсиссреададвисесинк](hrthisthreadadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="f44bd-127">For a way to turn a call to **OnNotify** that might happen at an inopportune time into one that is safer to handle, a provider should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="f44bd-128">Для предоставления уведомлений поставщик, реализующий \*\*\*\* предложение, должен хранить копию указателя на объект приемника уведомлений _лпадвисесинк_ ; для этого он вызывает метод **IUnknown:: AddRef** для приемника уведомлений, чтобы сохранить указатель на объект до тех пор, пока регистрация уведомлений не будет отменена с помощью вызова метода [IMAPITable:: unadvise](imapitable-unadvise.md) .</span><span class="sxs-lookup"><span data-stu-id="f44bd-128">To provide notifications, the provider implementing **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, it calls the **IUnknown::AddRef** method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMAPITable::Unadvise](imapitable-unadvise.md) method.</span></span> <span data-ttu-id="f44bd-129">При реализации **рекомендаций** необходимо назначить номер подключения для регистрации уведомлений и **AddRef** вызовов для этого номера подключения, прежде чем возвратить его в параметре _лпулконнектион_ .</span><span class="sxs-lookup"><span data-stu-id="f44bd-129">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="f44bd-130">Поставщики услуг могут освободить объект приемника уведомлений, прежде чем регистрация будет отменена, но не должна освобождать номер подключения, пока не будет вызван \* \* unadvise \* \*.</span><span class="sxs-lookup"><span data-stu-id="f44bd-130">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until \*\* Unadvise \*\* has been called.</span></span> 
  
<span data-ttu-id="f44bd-131">После успешного выполнения вызова **advise** и перед вызовом \* \* unadvise \* \* клиенты должны подготовиться к выпуску объекта приемника уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f44bd-131">After a call to **Advise** has succeeded and before \*\* Unadvise \*\* has been called, clients must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="f44bd-132">Клиент должен освободить объект приемника уведомлений после возврата, \*\*\*\* если он не имеет определенного долгосрочного использования.</span><span class="sxs-lookup"><span data-stu-id="f44bd-132">A client should therefore release its advise sink object after **Advise** returns unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="f44bd-133">Из-за асинхронного поведения уведомлений реализации, которые изменяют параметры столбца таблицы, могут получать уведомления с информацией, организованной в предыдущем порядке столбцов.</span><span class="sxs-lookup"><span data-stu-id="f44bd-133">Because of the asynchronous behavior of notification, implementations that change table column settings can receive notifications with information organized in a previous column order.</span></span> <span data-ttu-id="f44bd-134">Например, для сообщения, которое было только что удалено из контейнера, может быть возвращена строка таблицы.</span><span class="sxs-lookup"><span data-stu-id="f44bd-134">For instance, a table row might be returned for a message that has just been deleted from the container.</span></span> <span data-ttu-id="f44bd-135">Такое уведомление отправляется, когда изменяется значение параметра столбца и сведения о нем отправлены, но представление таблицы уведомлений еще не обновлялось.</span><span class="sxs-lookup"><span data-stu-id="f44bd-135">Such a notification is sent when the column setting change has been made and information about it sent but the notification table view has not been updated with that information yet.</span></span>
  
<span data-ttu-id="f44bd-136">Более подробную информацию о процессе уведомления можно узнать [в статье уведомление о событии в MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="f44bd-136">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="f44bd-137">Конкретные сведения о табличных уведомлениях см [](about-table-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="f44bd-137">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="f44bd-138">Сведения о том, как использовать методы **имаписуппорт** для поддержки уведомлений, можно узнать в разделе [Поддержка уведомлений о событиях](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="f44bd-138">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f44bd-139">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f44bd-139">MFCMAPI reference</span></span>

<span data-ttu-id="f44bd-140">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="f44bd-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f44bd-141">**Файл**</span><span class="sxs-lookup"><span data-stu-id="f44bd-141">**File**</span></span>|<span data-ttu-id="f44bd-142">**Функция**</span><span class="sxs-lookup"><span data-stu-id="f44bd-142">**Function**</span></span>|<span data-ttu-id="f44bd-143">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="f44bd-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f44bd-144">Контентстаблелистктрл. cpp</span><span class="sxs-lookup"><span data-stu-id="f44bd-144">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="f44bd-145">Кконтесттаблелистктрл:: Нотификатионон</span><span class="sxs-lookup"><span data-stu-id="f44bd-145">CContestTableListCtrl::NotificationOn</span></span>  <br/> |<span data-ttu-id="f44bd-146">MFCMAPI использует метод **IMAPITable:: Advise** для регистрации уведомлений, чтобы представление таблицы оставалось актуальным.</span><span class="sxs-lookup"><span data-stu-id="f44bd-146">MFCMAPI uses the **IMAPITable::Advise** method to register for notifications to allow the table view to stay current.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f44bd-147">См. также</span><span class="sxs-lookup"><span data-stu-id="f44bd-147">See also</span></span>



[<span data-ttu-id="f44bd-148">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="f44bd-148">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="f44bd-149">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="f44bd-149">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="f44bd-150">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="f44bd-150">IMAPITable::Unadvise</span></span>](imapitable-unadvise.md)
  
[<span data-ttu-id="f44bd-151">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f44bd-151">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="f44bd-152">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f44bd-152">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="f44bd-153">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="f44bd-153">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

