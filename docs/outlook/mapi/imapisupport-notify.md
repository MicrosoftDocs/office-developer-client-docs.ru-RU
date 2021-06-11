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
# <a name="imapisupportnotify"></a><span data-ttu-id="460c7-103">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="460c7-103">IMAPISupport::Notify</span></span>

<span data-ttu-id="460c7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="460c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="460c7-105">Отправляет уведомление о указанном событии источнику консультаций, который первоначально зарегистрировался для уведомления с помощью [метода IMAPISupport::Subscribe.](imapisupport-subscribe.md)</span><span class="sxs-lookup"><span data-stu-id="460c7-105">Sends a notification of a specified event to an advise source that originally registered for the notification through the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method.</span></span> 
  
```cpp
HRESULT Notify(
LPNOTIFKEY lpKey,
ULONG cNotification,
LPNOTIFICATION lpNotifications,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="460c7-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="460c7-106">Parameters</span></span>

<span data-ttu-id="460c7-107">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="460c7-107">_lpKey_</span></span>
  
> <span data-ttu-id="460c7-108">[in] Указатель на ключ уведомления для объекта-источника консультации.</span><span class="sxs-lookup"><span data-stu-id="460c7-108">[in] A pointer to the notification key for the advise source object.</span></span> <span data-ttu-id="460c7-109">Параметр  _lpKey не_ может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="460c7-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
<span data-ttu-id="460c7-110">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="460c7-110">_cNotification_</span></span>
  
> <span data-ttu-id="460c7-111">[in] Количество структур уведомлений, на которые указывает параметр _lpNotifications._</span><span class="sxs-lookup"><span data-stu-id="460c7-111">[in] The count of notification structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
<span data-ttu-id="460c7-112">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="460c7-112">_lpNotifications_</span></span>
  
> <span data-ttu-id="460c7-113">[in] Указатель на массив структур [УВЕДОМЛЕНий,](notification.md) описывающих ожидающих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="460c7-113">[in] A pointer to an array of [NOTIFICATION](notification.md) structures that describe pending notifications.</span></span> 
    
<span data-ttu-id="460c7-114">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="460c7-114">_lpulFlags_</span></span>
  
> <span data-ttu-id="460c7-115">[in, out] Битмашка флагов, которые контролируют процесс уведомления.</span><span class="sxs-lookup"><span data-stu-id="460c7-115">[in, out] A bitmask of flags that controls the notification process.</span></span> <span data-ttu-id="460c7-116">На входе можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="460c7-116">On input, the following flag can be set:</span></span>
    
  - <span data-ttu-id="460c7-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="460c7-117">MAPI_UNICODE</span></span> 
    
    > <span data-ttu-id="460c7-118">Строки в структурах уведомлений, на которые указывают  _lpNotifications,_ находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="460c7-118">The strings in the notification structures pointed to by  _lpNotifications_ are in Unicode format.</span></span> <span data-ttu-id="460c7-119">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="460c7-119">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 

    <span data-ttu-id="460c7-120">На выходе MAPI может установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="460c7-120">On output, MAPI can set the following flag:</span></span>
        
  - <span data-ttu-id="460c7-121">NOTIFY_CANCELED</span><span class="sxs-lookup"><span data-stu-id="460c7-121">NOTIFY_CANCELED</span></span> 
    
    > <span data-ttu-id="460c7-122">Функция вызова отменяет синхронное уведомление.</span><span class="sxs-lookup"><span data-stu-id="460c7-122">A callback function canceled a synchronous notification.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="460c7-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="460c7-123">Return value</span></span>

<span data-ttu-id="460c7-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="460c7-124">S_OK</span></span> 
  
> <span data-ttu-id="460c7-125">Уведомления были успешно сгенерированы.</span><span class="sxs-lookup"><span data-stu-id="460c7-125">The notifications were successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="460c7-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="460c7-126">Remarks</span></span>

<span data-ttu-id="460c7-127">Метод **IMAPISupport::Notify** реализован для всех объектов поддержки поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="460c7-127">The **IMAPISupport::Notify** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="460c7-128">Поставщики услуг  вызывают Уведомление о том, что MAPI создает уведомление для приемника консультаций, который ранее зарегистрировался для уведомления с помощью **метода IMAPISupport::Subscribe.**</span><span class="sxs-lookup"><span data-stu-id="460c7-128">Service providers call **Notify** to request that MAPI generate a notification for an advise sink that has previously registered for the notification through the **IMAPISupport::Subscribe** method.</span></span> 
  
<span data-ttu-id="460c7-129">**Уведомите** копии структур, на которые указывает параметр _lpNotifications,_ в память и вызывает соответствующий метод [IMAPIAdviseSink::OnNotify.](imapiadvisesink-onnotify.md)</span><span class="sxs-lookup"><span data-stu-id="460c7-129">**Notify** copies the structures pointed to by the  _lpNotifications_ parameter into memory and calls the appropriate advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="460c7-130">Когда **OnNotify** завершается с уведомлением, он освобождает участвуют памяти.</span><span class="sxs-lookup"><span data-stu-id="460c7-130">When **OnNotify** is finished with the notification, it releases the memory involved.</span></span> <span data-ttu-id="460c7-131">Вызываемой не требуется выделять память; MAPI выполняет все необходимые выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="460c7-131">The caller does not need to allocate memory; MAPI performs all necessary memory allocation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="460c7-132">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="460c7-132">Notes to callers</span></span>

<span data-ttu-id="460c7-133">Ключ уведомления, переданный в _параметре lpKey,_ должен быть идентичен клавише, переданной _в lpKey_ методу **IMAPISupport::Subscribe.**</span><span class="sxs-lookup"><span data-stu-id="460c7-133">The notification key passed in the  _lpKey_ parameter should be identical to the key passed in  _lpKey_ to the **IMAPISupport::Subscribe** method.</span></span> <span data-ttu-id="460c7-134">Многие поставщики используют идентификатор входа источника консультаций в качестве ключа, но другие данные, например путь к файлу, можно использовать.</span><span class="sxs-lookup"><span data-stu-id="460c7-134">Many providers use the entry identifier of the advise source as the key, but other data, such as a file path, can be used.</span></span> <span data-ttu-id="460c7-135">MAPI использует этот ключ, чтобы найти все регистрации для уведомлений в выявленных источниках консультаций.</span><span class="sxs-lookup"><span data-stu-id="460c7-135">MAPI uses this key to find all the registrations for notifications on the identified advise source.</span></span> 
  
<span data-ttu-id="460c7-136">Убедитесь, что участник **lpEntryID** в структуре уведомлений был настроен на долгосрочный идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="460c7-136">Be sure that you set the **lpEntryID** member of the notification structure to a long-term entry identifier.</span></span> 
  
<span data-ttu-id="460c7-137">Если вы установите флаг NOTIFY_SYNC в вызове **Подписка** для любого из ожидающих уведомлений,  перед возвращением уведомите об этом функции обратного вызова метода **IMAPIAdviseSink::OnNotify.**</span><span class="sxs-lookup"><span data-stu-id="460c7-137">If you set the NOTIFY_SYNC flag on the **Subscribe** call for any of the pending notifications, **Notify** calls the **IMAPIAdviseSink::OnNotify** method callback functions before returning.</span></span> <span data-ttu-id="460c7-138">Раковина рекомендации может быть создана вручную или по вызову [HrAllocAdviseSink](hrallocadvisesink.md).</span><span class="sxs-lookup"><span data-stu-id="460c7-138">An advise sink can be created manually or by calling [HrAllocAdviseSink](hrallocadvisesink.md).</span></span> <span data-ttu-id="460c7-139">Функция **HrAllocAdviseSink** позволяет вызываемой функции указать функцию вызова, уведомляемую о вызовах в рамках уведомления. </span><span class="sxs-lookup"><span data-stu-id="460c7-139">The **HrAllocAdviseSink** function allows its caller to specify a callback function that **Notify** calls as part of the notification.</span></span> <span data-ttu-id="460c7-140">Функция вызова соответствует прототипу [NOTIFCALLBACK.](notifcallback.md)</span><span class="sxs-lookup"><span data-stu-id="460c7-140">The callback function conforms to the [NOTIFCALLBACK](notifcallback.md) prototype.</span></span> <span data-ttu-id="460c7-141">Функции обратного вызова, реализованные клиентами, всегда возвращаются S_OK; Функции обратного вызова, реализованные поставщиками услуг, могут CALLBACK_DISCONTINUE.</span><span class="sxs-lookup"><span data-stu-id="460c7-141">Callback functions implemented by clients always return S_OK; callback functions implemented by service providers can return CALLBACK_DISCONTINUE.</span></span> 
  
<span data-ttu-id="460c7-142">Если функция обратного вызова возвращается CALLBACK_DISCONTINUE, MAPI прекращает отправку уведомлений и возвращает NOTIFY_CANCELED в _параметре lpulFlags_ метода **Notify.**</span><span class="sxs-lookup"><span data-stu-id="460c7-142">If a callback function returns CALLBACK_DISCONTINUE, MAPI stops sending notifications and returns NOTIFY_CANCELED in the **Notify** method's  _lpulFlags_ parameter.</span></span> <span data-ttu-id="460c7-143">Можно предположить, что процесс неактивный, и прекратить создание уведомлений для этого процесса.</span><span class="sxs-lookup"><span data-stu-id="460c7-143">You can assume that the process is inactive and stop generating notifications for that process.</span></span> <span data-ttu-id="460c7-144">Если **Уведомление** возвращает 0 в  _lpulFlags,_ процесс по-прежнему активен, и вы должны продолжать отправлять уведомления, как это необходимо.</span><span class="sxs-lookup"><span data-stu-id="460c7-144">If **Notify** returns 0 in  _lpulFlags_, the process is still active and you should continue to send notifications, as appropriate.</span></span>
  
<span data-ttu-id="460c7-145">При использовании синхронных уведомлений будьте осторожны, чтобы избежать ситуаций с затором.</span><span class="sxs-lookup"><span data-stu-id="460c7-145">When you use synchronous notifications, be careful to avoid deadlock situations.</span></span>
  
<span data-ttu-id="460c7-146">Дополнительные сведения о процессе уведомления см. в сообщении [события в MAPI.](event-notification-in-mapi.md)</span><span class="sxs-lookup"><span data-stu-id="460c7-146">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="460c7-147">См. также</span><span class="sxs-lookup"><span data-stu-id="460c7-147">See also</span></span>

- [<span data-ttu-id="460c7-148">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="460c7-148">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)  
- [<span data-ttu-id="460c7-149">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="460c7-149">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)  
- [<span data-ttu-id="460c7-150">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="460c7-150">NOTIFCALLBACK</span></span>](notifcallback.md) 
- [<span data-ttu-id="460c7-151">�����������</span><span class="sxs-lookup"><span data-stu-id="460c7-151">NOTIFICATION</span></span>](notification.md)  
- [<span data-ttu-id="460c7-152">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="460c7-152">NOTIFKEY</span></span>](notifkey.md)  
- [<span data-ttu-id="460c7-153">Каноническое свойство PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="460c7-153">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)  
- [<span data-ttu-id="460c7-154">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="460c7-154">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

