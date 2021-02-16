---
title: IMAPISupportNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Notify
api_type:
- COM
ms.assetid: c16c668e-2c8b-4759-bbca-d0c5662b62e9
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6160b8e75bdc9059965c2358b9fe7d296e1f66d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435938"
---
# <a name="imapisupportnotify"></a><span data-ttu-id="c2a5f-103">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="c2a5f-103">IMAPISupport::Notify</span></span>

<span data-ttu-id="c2a5f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2a5f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2a5f-105">Отправляет уведомление об указанном событии источнику консультаций, который изначально зарегистрировался для уведомления с помощью метода [IMAPISupport::Subscribe.](imapisupport-subscribe.md)</span><span class="sxs-lookup"><span data-stu-id="c2a5f-105">Sends a notification of a specified event to an advise source that originally registered for the notification through the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method.</span></span> 
  
```cpp
HRESULT Notify(
LPNOTIFKEY lpKey,
ULONG cNotification,
LPNOTIFICATION lpNotifications,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c2a5f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2a5f-106">Parameters</span></span>

<span data-ttu-id="c2a5f-107">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="c2a5f-107">_lpKey_</span></span>
  
> <span data-ttu-id="c2a5f-108">[in] Указатель на ключ уведомления для объекта источника консультации.</span><span class="sxs-lookup"><span data-stu-id="c2a5f-108">[in] A pointer to the notification key for the advise source object.</span></span> <span data-ttu-id="c2a5f-109">Параметр  _lpKey не может_ иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="c2a5f-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
<span data-ttu-id="c2a5f-110">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="c2a5f-110">_cNotification_</span></span>
  
> <span data-ttu-id="c2a5f-111">[in] Количество структур уведомлений, на которые указывает параметр _lpNotifications._</span><span class="sxs-lookup"><span data-stu-id="c2a5f-111">[in] The count of notification structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
<span data-ttu-id="c2a5f-112">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="c2a5f-112">_lpNotifications_</span></span>
  
> <span data-ttu-id="c2a5f-113">[in] Указатель на массив структур [УВЕДОМЛЕНий,](notification.md) описывающих ожидающих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c2a5f-113">[in] A pointer to an array of [NOTIFICATION](notification.md) structures that describe pending notifications.</span></span> 
    
<span data-ttu-id="c2a5f-114">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="c2a5f-114">_lpulFlags_</span></span>
  
> <span data-ttu-id="c2a5f-115">[in, out] Битоваяmas флагов, которая управляет процессом уведомления.</span><span class="sxs-lookup"><span data-stu-id="c2a5f-115">[in, out] A bitmask of flags that controls the notification process.</span></span> <span data-ttu-id="c2a5f-116">При вводе можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="c2a5f-116">On input, the following flag can be set:</span></span>
    
  - <span data-ttu-id="c2a5f-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c2a5f-117">MAPI_UNICODE</span></span> 
    
    > <span data-ttu-id="c2a5f-118">Строки в структурах уведомлений, на которые указывают  _lpNotifications,_ имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="c2a5f-118">The strings in the notification structures pointed to by  _lpNotifications_ are in Unicode format.</span></span> <span data-ttu-id="c2a5f-119">Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="c2a5f-119">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 

    <span data-ttu-id="c2a5f-120">В выходных данных MAPI может установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="c2a5f-120">On output, MAPI can set the following flag:</span></span>
        
  - <span data-ttu-id="c2a5f-121">NOTIFY_CANCELED</span><span class="sxs-lookup"><span data-stu-id="c2a5f-121">NOTIFY_CANCELED</span></span> 
    
    > <span data-ttu-id="c2a5f-122">Функция callback отменила синхронное уведомление.</span><span class="sxs-lookup"><span data-stu-id="c2a5f-122">A callback function canceled a synchronous notification.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c2a5f-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c2a5f-123">Return value</span></span>

<span data-ttu-id="c2a5f-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="c2a5f-124">S_OK</span></span> 
  
> <span data-ttu-id="c2a5f-125">Уведомления успешно созданы.</span><span class="sxs-lookup"><span data-stu-id="c2a5f-125">The notifications were successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c2a5f-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="c2a5f-126">Remarks</span></span>

<span data-ttu-id="c2a5f-127">Метод **IMAPISupport::Notify** реализован для всех объектов поддержки поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="c2a5f-127">The **IMAPISupport::Notify** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="c2a5f-128">Поставщики услуг вызывают **Notify,** чтобы попросить MAPI создать уведомление для приемника консультаций, который ранее зарегистрировался для уведомления с помощью метода **IMAPISupport::Subscribe.**</span><span class="sxs-lookup"><span data-stu-id="c2a5f-128">Service providers call **Notify** to request that MAPI generate a notification for an advise sink that has previously registered for the notification through the **IMAPISupport::Subscribe** method.</span></span> 
  
<span data-ttu-id="c2a5f-129">**Уведомление** копирует структуры, на которые указывает параметр  _lpNotifications,_ в память и вызывает метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) соответствующего приемника рекомендации.</span><span class="sxs-lookup"><span data-stu-id="c2a5f-129">**Notify** copies the structures pointed to by the  _lpNotifications_ parameter into memory and calls the appropriate advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="c2a5f-130">Когда **onNotify** завершает работу с уведомлением, освобождается задействованная память.</span><span class="sxs-lookup"><span data-stu-id="c2a5f-130">When **OnNotify** is finished with the notification, it releases the memory involved.</span></span> <span data-ttu-id="c2a5f-131">Вызываемой не нужно выделять память; MAPI выполняет все необходимые выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="c2a5f-131">The caller does not need to allocate memory; MAPI performs all necessary memory allocation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c2a5f-132">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="c2a5f-132">Notes to callers</span></span>

<span data-ttu-id="c2a5f-133">Ключ уведомления, переданный в _параметре lpKey,_ должен совпадать с ключом, переданным _в lpKey_ методу **IMAPISupport::Subscribe.**</span><span class="sxs-lookup"><span data-stu-id="c2a5f-133">The notification key passed in the  _lpKey_ parameter should be identical to the key passed in  _lpKey_ to the **IMAPISupport::Subscribe** method.</span></span> <span data-ttu-id="c2a5f-134">Многие поставщики используют идентификатор записи источника консультации в качестве ключа, но можно использовать другие данные, например путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="c2a5f-134">Many providers use the entry identifier of the advise source as the key, but other data, such as a file path, can be used.</span></span> <span data-ttu-id="c2a5f-135">MAPI использует этот ключ для поиска всех регистраций для уведомлений в заданной источнике консультаций.</span><span class="sxs-lookup"><span data-stu-id="c2a5f-135">MAPI uses this key to find all the registrations for notifications on the identified advise source.</span></span> 
  
<span data-ttu-id="c2a5f-136">Убедитесь, что для члена **lpEntryID** структуры уведомлений задан долгосрочный идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="c2a5f-136">Be sure that you set the **lpEntryID** member of the notification structure to a long-term entry identifier.</span></span> 
  
<span data-ttu-id="c2a5f-137">Если вы установите флаг NOTIFY_SYNC при вызове **Subscribe** для любого из ожидающих уведомлений,  уведомите перед возвратом вызов функции обратного вызова метода **IMAPIAdviseSink::OnNotify.**</span><span class="sxs-lookup"><span data-stu-id="c2a5f-137">If you set the NOTIFY_SYNC flag on the **Subscribe** call for any of the pending notifications, **Notify** calls the **IMAPIAdviseSink::OnNotify** method callback functions before returning.</span></span> <span data-ttu-id="c2a5f-138">Вы можете создать тактовую ведомость вручную или с помощью вызова [HrAllocAdviseSink.](hrallocadvisesink.md)</span><span class="sxs-lookup"><span data-stu-id="c2a5f-138">An advise sink can be created manually or by calling [HrAllocAdviseSink](hrallocadvisesink.md).</span></span> <span data-ttu-id="c2a5f-139">Функция **HrAllocAdviseSink** позволяет вызываемой функции указать функцию вызова, которая уведомляет о вызовах в рамках уведомления. </span><span class="sxs-lookup"><span data-stu-id="c2a5f-139">The **HrAllocAdviseSink** function allows its caller to specify a callback function that **Notify** calls as part of the notification.</span></span> <span data-ttu-id="c2a5f-140">Функция callback соответствует [прототипу NOTIFCALLBACK.](notifcallback.md)</span><span class="sxs-lookup"><span data-stu-id="c2a5f-140">The callback function conforms to the [NOTIFCALLBACK](notifcallback.md) prototype.</span></span> <span data-ttu-id="c2a5f-141">Функции обратного вызова, реализованные клиентами, всегда возвращают S_OK; Функции обратного вызова, реализованные поставщиками служб, могут возвращать CALLBACK_DISCONTINUE.</span><span class="sxs-lookup"><span data-stu-id="c2a5f-141">Callback functions implemented by clients always return S_OK; callback functions implemented by service providers can return CALLBACK_DISCONTINUE.</span></span> 
  
<span data-ttu-id="c2a5f-142">Если функция обратного вызова возвращает CALLBACK_DISCONTINUE, MAPI прекращает отправку уведомлений и NOTIFY_CANCELED в параметре _lpulFlags_ метода **Notify.**</span><span class="sxs-lookup"><span data-stu-id="c2a5f-142">If a callback function returns CALLBACK_DISCONTINUE, MAPI stops sending notifications and returns NOTIFY_CANCELED in the **Notify** method's  _lpulFlags_ parameter.</span></span> <span data-ttu-id="c2a5f-143">Можно предположить, что этот процесс неактивный, и прекратить создание уведомлений для этого процесса.</span><span class="sxs-lookup"><span data-stu-id="c2a5f-143">You can assume that the process is inactive and stop generating notifications for that process.</span></span> <span data-ttu-id="c2a5f-144">Если **notify** возвращает 0 в  _lpulFlags,_ процесс по-прежнему активен, и вы должны продолжать отправлять уведомления, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="c2a5f-144">If **Notify** returns 0 in  _lpulFlags_, the process is still active and you should continue to send notifications, as appropriate.</span></span>
  
<span data-ttu-id="c2a5f-145">При использовании синхронных уведомлений будьте осторожны, чтобы избежать ситуаций с блокировкой.</span><span class="sxs-lookup"><span data-stu-id="c2a5f-145">When you use synchronous notifications, be careful to avoid deadlock situations.</span></span>
  
<span data-ttu-id="c2a5f-146">Дополнительные сведения о процессе уведомления см. в [уведомлении о событии в MAPI.](event-notification-in-mapi.md)</span><span class="sxs-lookup"><span data-stu-id="c2a5f-146">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c2a5f-147">См. также</span><span class="sxs-lookup"><span data-stu-id="c2a5f-147">See also</span></span>

- [<span data-ttu-id="c2a5f-148">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="c2a5f-148">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)  
- [<span data-ttu-id="c2a5f-149">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="c2a5f-149">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)  
- [<span data-ttu-id="c2a5f-150">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="c2a5f-150">NOTIFCALLBACK</span></span>](notifcallback.md) 
- [<span data-ttu-id="c2a5f-151">�����������</span><span class="sxs-lookup"><span data-stu-id="c2a5f-151">NOTIFICATION</span></span>](notification.md)  
- [<span data-ttu-id="c2a5f-152">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="c2a5f-152">NOTIFKEY</span></span>](notifkey.md)  
- [<span data-ttu-id="c2a5f-153">Каноническое свойство PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="c2a5f-153">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)  
- [<span data-ttu-id="c2a5f-154">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c2a5f-154">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

