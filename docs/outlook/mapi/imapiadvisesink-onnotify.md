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
ms.openlocfilehash: 73eb92b0c1b88e114775231695b91157a3d26a2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808812"
---
# <a name="imapiadvisesinkonnotify"></a><span data-ttu-id="24919-103">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="24919-103">IMAPIAdviseSink::OnNotify</span></span>

  
  
<span data-ttu-id="24919-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="24919-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="24919-105">Отвечает на уведомление при выполнении одного или нескольких задач.</span><span class="sxs-lookup"><span data-stu-id="24919-105">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="24919-106">Задачи, выполняемые зависят от типа события и объект, который создает уведомления.</span><span class="sxs-lookup"><span data-stu-id="24919-106">The tasks performed depend on the type of event and the object that generates the notification.</span></span> 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="24919-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="24919-107">Parameters</span></span>

 <span data-ttu-id="24919-108">_cNotif_</span><span class="sxs-lookup"><span data-stu-id="24919-108">_cNotif_</span></span>
  
> <span data-ttu-id="24919-109">[in] Количество [УВЕДОМЛЕНИЙ](notification.md) структуры, на который указывает параметр _lpNotifications_ .</span><span class="sxs-lookup"><span data-stu-id="24919-109">[in] The count of [NOTIFICATION](notification.md) structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="24919-110">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="24919-110">_lpNotifications_</span></span>
  
> <span data-ttu-id="24919-111">[in] Указатель на один или несколько **УВЕДОМЛЕНИЙ** структуры, содержащие сведения о событиях, которые происходили.</span><span class="sxs-lookup"><span data-stu-id="24919-111">[in] A pointer to one or more **NOTIFICATION** structures that provide information about the events that have occurred.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="24919-112">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="24919-112">Return value</span></span>

<span data-ttu-id="24919-113">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="24919-113">S_OK</span></span> 
  
> <span data-ttu-id="24919-114">Уведомление обработан успешно.</span><span class="sxs-lookup"><span data-stu-id="24919-114">The notification was processed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="24919-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="24919-115">Remarks</span></span>

<span data-ttu-id="24919-116">Уведомление процесс запускается после клиента или MAPI вызывает метод **уведомлений** поставщика услуг для получения уведомлений для определенного объекта определенного типа.</span><span class="sxs-lookup"><span data-stu-id="24919-116">The notification process starts when a client or MAPI makes a call to a service provider's **Advise** method to register to receive a notification of a particular type for a particular object.</span></span> <span data-ttu-id="24919-117">Один из параметров для метода **уведомлений** является указатель на объект приемника уведомлений, который реализует интерфейс [IMAPIAdviseSink](imapiadvisesinkiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="24919-117">One of the parameters to the **Advise** method is a pointer to an advise sink object that implements the [IMAPIAdviseSink](imapiadvisesinkiunknown.md) interface.</span></span> <span data-ttu-id="24919-118">Когда возникает событие целевой объект, который соответствует зарегистрированного уведомления поставщика услуг, прямо или косвенно через MAPI, вызывает метод **OnNotify** приемник уведомлений.</span><span class="sxs-lookup"><span data-stu-id="24919-118">When an event occurs to the target object that corresponds to the registered notification, the service provider, either directly or indirectly through MAPI, calls the advise sink's **OnNotify** method.</span></span> 
  
<span data-ttu-id="24919-119">Вызов **OnNotify** может возникнуть во время вызова MAPI, который вызывает событие или позднее.</span><span class="sxs-lookup"><span data-stu-id="24919-119">The call to **OnNotify** can occur either during the MAPI call that is causing the event or at some later time.</span></span> <span data-ttu-id="24919-120">На компьютерах, поддерживающих многопоточной среде **OnNotify** может быть вызван в том же потоке, который использовался для регистрации или в другом потоке.</span><span class="sxs-lookup"><span data-stu-id="24919-120">On systems that support multiple threads of execution, **OnNotify** can be called either on the same thread that was used for registration or on a different thread.</span></span> <span data-ttu-id="24919-121">Клиенты могут убедитесь в том, что **OnNotify** вызов же потока, используемый для вызова **уведомлений** , создав приемник уведомлений, который они передать **уведомлений** с помощью функции [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="24919-121">Clients can make sure that the **OnNotify** call is made on the same thread used to call **Advise** by creating the advise sink that they pass to **Advise** with the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="24919-122">Параметр _lpNotifications_ указывает одного или нескольких структур **УВЕДОМЛЕНИЙ** , которые описывают, что был изменен во время события.</span><span class="sxs-lookup"><span data-stu-id="24919-122">The  _lpNotifications_ parameter points to one or more **NOTIFICATION** structures that describe what has changed during the event.</span></span> <span data-ttu-id="24919-123">Существует другой тип структуры **УВЕДОМЛЕНИЙ** для каждого типа события.</span><span class="sxs-lookup"><span data-stu-id="24919-123">There is a different type of **NOTIFICATION** structure for each type of event.</span></span> 
  
<span data-ttu-id="24919-124">В следующей таблице приведены значения, используемые для представления возможных типов событий и структур, связанные с каждым из значений:</span><span class="sxs-lookup"><span data-stu-id="24919-124">The following table lists the values that are used to represent the possible types of events and the structures associated with each value:</span></span>
  
|<span data-ttu-id="24919-125">**Тип события уведомления**</span><span class="sxs-lookup"><span data-stu-id="24919-125">**Notification event type**</span></span>|<span data-ttu-id="24919-126">**Соответствующий структуры**</span><span class="sxs-lookup"><span data-stu-id="24919-126">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="24919-127">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="24919-127">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="24919-128">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="24919-128">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="24919-129">**fnevNewMail**</span><span class="sxs-lookup"><span data-stu-id="24919-129">**fnevNewMail**</span></span> <br/> |[<span data-ttu-id="24919-130">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="24919-130">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="24919-131">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="24919-131">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="24919-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="24919-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="24919-133">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="24919-133">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="24919-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="24919-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="24919-135">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="24919-135">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="24919-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="24919-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="24919-137">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="24919-137">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="24919-138">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="24919-138">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="24919-139">**fnevSearchComplete**</span><span class="sxs-lookup"><span data-stu-id="24919-139">**fnevSearchComplete**</span></span> <br/> |[<span data-ttu-id="24919-140">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="24919-140">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="24919-141">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="24919-141">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="24919-142">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="24919-142">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
|<span data-ttu-id="24919-143">**fnevStatusObjectModified**</span><span class="sxs-lookup"><span data-stu-id="24919-143">**fnevStatusObjectModified**</span></span> <br/> |[<span data-ttu-id="24919-144">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="24919-144">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
|<span data-ttu-id="24919-145">**fnevExtended**</span><span class="sxs-lookup"><span data-stu-id="24919-145">**fnevExtended**</span></span> <br/> |[<span data-ttu-id="24919-146">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="24919-146">EXTENDED_NOTIFICATION</span></span>](extended_notification.md) <br/> |
   
<span data-ttu-id="24919-147">Дополнительные сведения о том, как настроить и остановите уведомлений просмотра операций ссылку для **уведомлений** и **Unadvise** методов для каких-либо следующие интерфейсы: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [ IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md)и [IMSLogon](imslogoniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="24919-147">For more information about how to set up and stop notifications, see the reference entries for the **Advise** and **Unadvise** methods for any of the following interfaces: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md), and [IMSLogon](imslogoniunknown.md).</span></span> 
  
<span data-ttu-id="24919-148">Общие сведения о процессе уведомления содержатся в разделе [Уведомление о событии в MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="24919-148">For general information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="24919-149">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="24919-149">Notes to implementers</span></span>

<span data-ttu-id="24919-150">Реализация **OnNotify** обычно будет состоять из одного или нескольких блоков кода для каждого типа согласно прогнозу, будут получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="24919-150">Your **OnNotify** implementation will typically consist of one or more blocks of code for each type of notification you expect to receive.</span></span> <span data-ttu-id="24919-151">В этих блоках кода выполнения задач, которые необходимо учитывать необходимые как ответ на уведомление.</span><span class="sxs-lookup"><span data-stu-id="24919-151">Within these blocks of code, perform any tasks that you consider necessary as a response to the notification.</span></span> <span data-ttu-id="24919-152">Например предположим, что Зарегистрируйтесь для получения уведомлений о **fnevObjectModified** на папку, включенную в поле показано диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="24919-152">For example, suppose you register to receive **fnevObjectModified** notifications on a folder that is included in a dialog box display.</span></span> <span data-ttu-id="24919-153">В блоке кода, включение в методе **OnNotify** для обработки уведомлений **fnevObjectModified** может отправить сообщение Windows к диалоговому окну, чтобы запросить обновленные отображения.</span><span class="sxs-lookup"><span data-stu-id="24919-153">In the block of code that you include in your **OnNotify** method to handle **fnevObjectModified** notifications, you might send a Windows message to the dialog box to request an updated display.</span></span> 
  
<span data-ttu-id="24919-154">Не изменяйте и не освободить структура **УВЕДОМЛЕНИЙ** , переданной в **OnNotify**.</span><span class="sxs-lookup"><span data-stu-id="24919-154">Do not modify or free the **NOTIFICATION** structure passed to **OnNotify**.</span></span> <span data-ttu-id="24919-155">Данные в структуре действителен только в том случае, пока возвращает **OnNotify** .</span><span class="sxs-lookup"><span data-stu-id="24919-155">The data in the structure is valid only until **OnNotify** returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="24919-156">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="24919-156">Notes to callers</span></span>

<span data-ttu-id="24919-157">При внесении изменений в несколько объектов, может уведомлять приемник зарегистрированных уведомлений в одном вызове **OnNotify** или в различных вызовов в зависимости от доступной памяти.</span><span class="sxs-lookup"><span data-stu-id="24919-157">When changes occur to multiple objects, you can notify a registered advise sink in a single call to **OnNotify** or in multiple calls depending on memory constraints.</span></span> <span data-ttu-id="24919-158">Это значение true, независимо от того, является ли изменения, в результате вызова метода один или несколько.</span><span class="sxs-lookup"><span data-stu-id="24919-158">This is true regardless of whether the changes are the result of one method call or several.</span></span> <span data-ttu-id="24919-159">Например вызов [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) могут повлиять на нескольких сообщений и папок.</span><span class="sxs-lookup"><span data-stu-id="24919-159">For example, a call to [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) can affect multiple messages and folders.</span></span> <span data-ttu-id="24919-160">Как поставщик хранилища сообщений можно сделать один вызов **OnNotify** с типом событий **fnevObjectModified** для целевой папке или много вызовов, другая — для каждого сообщения влияет.</span><span class="sxs-lookup"><span data-stu-id="24919-160">As a message store provider, you can make one call to **OnNotify** with an **fnevObjectModified** event type for the target folder or many calls, one for each affect messages.</span></span> <span data-ttu-id="24919-161">Аналогично Если клиент создает повторяющиеся вызовы [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), эти вызовы можно объединены в одно событие **fnevObjectModified** для папки или разделить на отдельные **fnevObjectCreated** событий для каждого нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="24919-161">Similarly, if a client makes repeated calls to [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), these calls can be combined into one **fnevObjectModified** event for the folder or separated into individual **fnevObjectCreated** events for each new message.</span></span> 
  
<span data-ttu-id="24919-162">Дополнительные сведения о том, как и когда следует создавать уведомления в разделе [Уведомление о событии в MAPI](event-notification-in-mapi.md) и [Поддержка уведомлений о событиях](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="24919-162">For more information about how and when to generate notifications, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="24919-163">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="24919-163">MFCMAPI reference</span></span>

<span data-ttu-id="24919-164">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="24919-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="24919-165">**����**</span><span class="sxs-lookup"><span data-stu-id="24919-165">**File**</span></span>|<span data-ttu-id="24919-166">**�������**</span><span class="sxs-lookup"><span data-stu-id="24919-166">**Function**</span></span>|<span data-ttu-id="24919-167">**�����������**</span><span class="sxs-lookup"><span data-stu-id="24919-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="24919-168">AdviseSink.h и AdviseSink.cpp</span><span class="sxs-lookup"><span data-stu-id="24919-168">AdviseSink.h and AdviseSink.cpp</span></span>  <br/> |<span data-ttu-id="24919-169">CAdviseSink::OnNotifyDesc</span><span class="sxs-lookup"><span data-stu-id="24919-169">CAdviseSink::OnNotifyDesc</span></span>  <br/> |<span data-ttu-id="24919-170">Класс CAdviseSink реализуется для обработки всех уведомлений в mfcmapi (en).</span><span class="sxs-lookup"><span data-stu-id="24919-170">The CAdviseSink class is implemented to handle all notifications in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="24919-171">См. также</span><span class="sxs-lookup"><span data-stu-id="24919-171">See also</span></span>



[<span data-ttu-id="24919-172">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="24919-172">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="24919-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="24919-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="24919-174">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="24919-174">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="24919-175">�����������</span><span class="sxs-lookup"><span data-stu-id="24919-175">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="24919-176">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="24919-176">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)


[<span data-ttu-id="24919-177">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="24919-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

