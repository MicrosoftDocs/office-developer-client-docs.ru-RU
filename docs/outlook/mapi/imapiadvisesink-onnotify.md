---
title: IMAPIAdviseSinkOnNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIAdviseSink.OnNotify
api_type:
- COM
ms.assetid: 9eec90d3-2369-4340-86ed-0efa58918ed5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5983ed3229f6b0053f15a614116cf5680e942587
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407363"
---
# <a name="imapiadvisesinkonnotify"></a><span data-ttu-id="16971-103">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="16971-103">IMAPIAdviseSink::OnNotify</span></span>

  
  
<span data-ttu-id="16971-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16971-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16971-105">Отвечает на уведомление, выполняя одну или несколько задач.</span><span class="sxs-lookup"><span data-stu-id="16971-105">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="16971-106">Выполняемые задачи зависят от типа события и объекта, который создает уведомление.</span><span class="sxs-lookup"><span data-stu-id="16971-106">The tasks performed depend on the type of event and the object that generates the notification.</span></span> 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="16971-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="16971-107">Parameters</span></span>

 <span data-ttu-id="16971-108">_cNotif_</span><span class="sxs-lookup"><span data-stu-id="16971-108">_cNotif_</span></span>
  
> <span data-ttu-id="16971-109">[in] Количество структур [УВЕДОМЛЕНий,](notification.md) на которые указывает параметр _lpNotifications._</span><span class="sxs-lookup"><span data-stu-id="16971-109">[in] The count of [NOTIFICATION](notification.md) structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="16971-110">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="16971-110">_lpNotifications_</span></span>
  
> <span data-ttu-id="16971-111">[in] Указатель на одну или несколько **структур УВЕДОМЛЕНий,** которые предоставляют сведения о произошедших событиях.</span><span class="sxs-lookup"><span data-stu-id="16971-111">[in] A pointer to one or more **NOTIFICATION** structures that provide information about the events that have occurred.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="16971-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16971-112">Return value</span></span>

<span data-ttu-id="16971-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="16971-113">S_OK</span></span> 
  
> <span data-ttu-id="16971-114">Уведомление было успешно обработано.</span><span class="sxs-lookup"><span data-stu-id="16971-114">The notification was processed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="16971-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="16971-115">Remarks</span></span>

<span data-ttu-id="16971-116">Процесс уведомления начинается, когда клиент или MAPI делает  вызов методу консультирования поставщика услуг для регистрации для получения уведомления определенного типа для определенного объекта.</span><span class="sxs-lookup"><span data-stu-id="16971-116">The notification process starts when a client or MAPI makes a call to a service provider's **Advise** method to register to receive a notification of a particular type for a particular object.</span></span> <span data-ttu-id="16971-117">Один из параметров метода **Advise** — указатель на объект раковины, который реализует [интерфейс IMAPIAdviseSink.](imapiadvisesinkiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="16971-117">One of the parameters to the **Advise** method is a pointer to an advise sink object that implements the [IMAPIAdviseSink](imapiadvisesinkiunknown.md) interface.</span></span> <span data-ttu-id="16971-118">Если событие происходит с целевым объектом, соответствующим зарегистрированным уведомлениям, поставщик услуг прямо или косвенно через MAPI вызывает метод **OnNotify** раковины рекомендации.</span><span class="sxs-lookup"><span data-stu-id="16971-118">When an event occurs to the target object that corresponds to the registered notification, the service provider, either directly or indirectly through MAPI, calls the advise sink's **OnNotify** method.</span></span> 
  
<span data-ttu-id="16971-119">Вызов **OnNotify может** произойти во время вызова MAPI, вызываемом событием, или в более позднее время.</span><span class="sxs-lookup"><span data-stu-id="16971-119">The call to **OnNotify** can occur either during the MAPI call that is causing the event or at some later time.</span></span> <span data-ttu-id="16971-120">В системах, поддерживаюх несколько потоков выполнения, **OnNotify** можно назвать как по одному потоку, который использовался для регистрации, так и по другому потоку.</span><span class="sxs-lookup"><span data-stu-id="16971-120">On systems that support multiple threads of execution, **OnNotify** can be called either on the same thread that was used for registration or on a different thread.</span></span> <span data-ttu-id="16971-121">Клиенты могут убедиться, что вызов **OnNotify** выполнен  на том же потоке,  который используется для вызова "Советы", создав раковину рекомендации, которую они передают в консультацию с функцией [HrThisThreadAdviseSink.](hrthisthreadadvisesink.md)</span><span class="sxs-lookup"><span data-stu-id="16971-121">Clients can make sure that the **OnNotify** call is made on the same thread used to call **Advise** by creating the advise sink that they pass to **Advise** with the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="16971-122">Параметр  _lpNotifications_ указывает на одну или несколько структур **УВЕДОМЛЕНий,** которые описывают изменения во время события.</span><span class="sxs-lookup"><span data-stu-id="16971-122">The  _lpNotifications_ parameter points to one or more **NOTIFICATION** structures that describe what has changed during the event.</span></span> <span data-ttu-id="16971-123">Существует другой тип структуры **УВЕДОМЛЕНий** для каждого типа события.</span><span class="sxs-lookup"><span data-stu-id="16971-123">There is a different type of **NOTIFICATION** structure for each type of event.</span></span> 
  
<span data-ttu-id="16971-124">В следующей таблице перечислены значения, которые используются для представления возможных типов событий и структур, связанных с каждым значением:</span><span class="sxs-lookup"><span data-stu-id="16971-124">The following table lists the values that are used to represent the possible types of events and the structures associated with each value:</span></span>
  
|<span data-ttu-id="16971-125">**Тип события уведомлений**</span><span class="sxs-lookup"><span data-stu-id="16971-125">**Notification event type**</span></span>|<span data-ttu-id="16971-126">**Соответствующая структура**</span><span class="sxs-lookup"><span data-stu-id="16971-126">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="16971-127">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="16971-127">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="16971-128">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="16971-128">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="16971-129">**fnevNewMail**</span><span class="sxs-lookup"><span data-stu-id="16971-129">**fnevNewMail**</span></span> <br/> |[<span data-ttu-id="16971-130">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="16971-130">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="16971-131">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="16971-131">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="16971-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="16971-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="16971-133">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="16971-133">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="16971-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="16971-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="16971-135">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="16971-135">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="16971-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="16971-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="16971-137">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="16971-137">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="16971-138">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="16971-138">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="16971-139">**fnevSearchComplete**</span><span class="sxs-lookup"><span data-stu-id="16971-139">**fnevSearchComplete**</span></span> <br/> |[<span data-ttu-id="16971-140">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="16971-140">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="16971-141">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="16971-141">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="16971-142">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="16971-142">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
|<span data-ttu-id="16971-143">**fnevStatusObjectModified**</span><span class="sxs-lookup"><span data-stu-id="16971-143">**fnevStatusObjectModified**</span></span> <br/> |[<span data-ttu-id="16971-144">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="16971-144">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
|<span data-ttu-id="16971-145">**fnevExtended**</span><span class="sxs-lookup"><span data-stu-id="16971-145">**fnevExtended**</span></span> <br/> |[<span data-ttu-id="16971-146">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="16971-146">EXTENDED_NOTIFICATION</span></span>](extended_notification.md) <br/> |
   
<span data-ttu-id="16971-147">Дополнительные сведения о том, как настроить и остановить уведомления, см. в справочных записях методов Advise **и** **Unadvise** для любого из следующих интерфейсов: [IABLogon,](iablogoniunknown.md) [IAddrBook,](iaddrbookimapiprop.md) [IMAPIForm, IMAPISession,](imapisessioniunknown.md) [IMAPITable,](imapitableiunknown.md) [](imapiformiunknown.md) [IMsgStore](imsgstoreimapiprop.md)и [IMSLogon](imslogoniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="16971-147">For more information about how to set up and stop notifications, see the reference entries for the **Advise** and **Unadvise** methods for any of the following interfaces: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md), and [IMSLogon](imslogoniunknown.md).</span></span> 
  
<span data-ttu-id="16971-148">Общие сведения о процессе уведомления см. в сообщении [о событиях в MAPI.](event-notification-in-mapi.md)</span><span class="sxs-lookup"><span data-stu-id="16971-148">For general information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="16971-149">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="16971-149">Notes to implementers</span></span>

<span data-ttu-id="16971-150">Реализация **OnNotify** обычно состоит из одного или нескольких блоков кода для каждого типа уведомлений, которые вы ожидаете получить.</span><span class="sxs-lookup"><span data-stu-id="16971-150">Your **OnNotify** implementation will typically consist of one or more blocks of code for each type of notification you expect to receive.</span></span> <span data-ttu-id="16971-151">В этих блоках кода выполните любые задачи, которые вы считаете необходимыми в качестве ответа на уведомление.</span><span class="sxs-lookup"><span data-stu-id="16971-151">Within these blocks of code, perform any tasks that you consider necessary as a response to the notification.</span></span> <span data-ttu-id="16971-152">Например, предположим, что вы регистрируете для получения **уведомлений fnevObjectModified** в папке, которая включена в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="16971-152">For example, suppose you register to receive **fnevObjectModified** notifications on a folder that is included in a dialog box display.</span></span> <span data-ttu-id="16971-153">В блоке кода, который вы включаете в метод **OnNotify** для обработки уведомлений **fnevObjectModified,** можно отправить Windows в диалоговое окно для запроса обновленного отображения.</span><span class="sxs-lookup"><span data-stu-id="16971-153">In the block of code that you include in your **OnNotify** method to handle **fnevObjectModified** notifications, you might send a Windows message to the dialog box to request an updated display.</span></span> 
  
<span data-ttu-id="16971-154">Не изменять или освободить структуру **УВЕДОМЛЕНий,** переданную **OnNotify.**</span><span class="sxs-lookup"><span data-stu-id="16971-154">Do not modify or free the **NOTIFICATION** structure passed to **OnNotify**.</span></span> <span data-ttu-id="16971-155">Данные в структуре действительны только до тех пор, пока **OnNotify** не вернется.</span><span class="sxs-lookup"><span data-stu-id="16971-155">The data in the structure is valid only until **OnNotify** returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="16971-156">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="16971-156">Notes to callers</span></span>

<span data-ttu-id="16971-157">При внесении изменений в несколько объектов можно уведомить зарегистрированную раковину рекомендации в одном вызове **OnNotify** или в нескольких вызовах в зависимости от ограничений памяти.</span><span class="sxs-lookup"><span data-stu-id="16971-157">When changes occur to multiple objects, you can notify a registered advise sink in a single call to **OnNotify** or in multiple calls depending on memory constraints.</span></span> <span data-ttu-id="16971-158">Это верно независимо от того, являются ли изменения результатом одного или нескольких вызовов метода.</span><span class="sxs-lookup"><span data-stu-id="16971-158">This is true regardless of whether the changes are the result of one method call or several.</span></span> <span data-ttu-id="16971-159">Например, вызов в [IMAPIFolder::CopyMessages может](imapifolder-copymessages.md) повлиять на несколько сообщений и папок.</span><span class="sxs-lookup"><span data-stu-id="16971-159">For example, a call to [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) can affect multiple messages and folders.</span></span> <span data-ttu-id="16971-160">В качестве поставщика магазина сообщений можно сделать один вызов **onNotify** с типом **событий fnevObjectModified** для целевой папки или множеством вызовов, по одному для каждого затрагиваемого сообщения.</span><span class="sxs-lookup"><span data-stu-id="16971-160">As a message store provider, you can make one call to **OnNotify** with an **fnevObjectModified** event type for the target folder or many calls, one for each affect messages.</span></span> <span data-ttu-id="16971-161">Аналогично, если клиент совершает повторные вызовы [в IMAPIFolder::CreateMessage,](imapifolder-createmessage.md)эти вызовы можно объединить в одно **событие fnevObjectModified** для папки или разделить на отдельные **события fnevObjectCreated** для каждого нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="16971-161">Similarly, if a client makes repeated calls to [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), these calls can be combined into one **fnevObjectModified** event for the folder or separated into individual **fnevObjectCreated** events for each new message.</span></span> 
  
<span data-ttu-id="16971-162">Дополнительные сведения о том, как и когда создавать уведомления, см. в дополнительных сведениях Об уведомлении о событиях в [MAPI](event-notification-in-mapi.md) и [вспомогательном уведомлении о событиях.](supporting-event-notification.md)</span><span class="sxs-lookup"><span data-stu-id="16971-162">For more information about how and when to generate notifications, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="16971-163">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="16971-163">MFCMAPI reference</span></span>

<span data-ttu-id="16971-164">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="16971-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="16971-165">**Файл**</span><span class="sxs-lookup"><span data-stu-id="16971-165">**File**</span></span>|<span data-ttu-id="16971-166">**Функция**</span><span class="sxs-lookup"><span data-stu-id="16971-166">**Function**</span></span>|<span data-ttu-id="16971-167">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="16971-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="16971-168">AdviseSink.h и AdviseSink.cpp</span><span class="sxs-lookup"><span data-stu-id="16971-168">AdviseSink.h and AdviseSink.cpp</span></span>  <br/> |<span data-ttu-id="16971-169">CAdviseSink::OnNotifyDesc</span><span class="sxs-lookup"><span data-stu-id="16971-169">CAdviseSink::OnNotifyDesc</span></span>  <br/> |<span data-ttu-id="16971-170">Класс CAdviseSink реализуется для обработки всех уведомлений в MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="16971-170">The CAdviseSink class is implemented to handle all notifications in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="16971-171">См. также</span><span class="sxs-lookup"><span data-stu-id="16971-171">See also</span></span>



[<span data-ttu-id="16971-172">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="16971-172">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="16971-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="16971-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="16971-174">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="16971-174">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="16971-175">�����������</span><span class="sxs-lookup"><span data-stu-id="16971-175">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="16971-176">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="16971-176">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)


[<span data-ttu-id="16971-177">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="16971-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

