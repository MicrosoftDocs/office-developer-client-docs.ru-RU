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
ms.openlocfilehash: f79e5eaa3155bbe3373f5ad9c5182a4a65c62648
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572041"
---
# <a name="imapisupportnotify"></a><span data-ttu-id="78e28-103">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="78e28-103">IMAPISupport::Notify</span></span>

<span data-ttu-id="78e28-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78e28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78e28-105">Отправляет уведомление об указанном события источника уведомлений, изначально зарегистрированных для уведомления с помощью метода [IMAPISupport::Subscribe](imapisupport-subscribe.md) .</span><span class="sxs-lookup"><span data-stu-id="78e28-105">Sends a notification of a specified event to an advise source that originally registered for the notification through the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method.</span></span> 
  
```cpp
HRESULT Notify(
LPNOTIFKEY lpKey,
ULONG cNotification,
LPNOTIFICATION lpNotifications,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="78e28-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="78e28-106">Parameters</span></span>

<span data-ttu-id="78e28-107">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="78e28-107">_lpKey_</span></span>
  
> <span data-ttu-id="78e28-108">[in] Указатель на ключ уведомления для объекта источника уведомлений.</span><span class="sxs-lookup"><span data-stu-id="78e28-108">[in] A pointer to the notification key for the advise source object.</span></span> <span data-ttu-id="78e28-109">Параметр _lpKey_ не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="78e28-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
<span data-ttu-id="78e28-110">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="78e28-110">_cNotification_</span></span>
  
> <span data-ttu-id="78e28-111">[in] Количество уведомлений структуры, на который указывает параметр _lpNotifications_ .</span><span class="sxs-lookup"><span data-stu-id="78e28-111">[in] The count of notification structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
<span data-ttu-id="78e28-112">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="78e28-112">_lpNotifications_</span></span>
  
> <span data-ttu-id="78e28-113">[in] Указатель на массив структур [УВЕДОМЛЕНИЙ](notification.md) , которые описывают ожидающие уведомления.</span><span class="sxs-lookup"><span data-stu-id="78e28-113">[in] A pointer to an array of [NOTIFICATION](notification.md) structures that describe pending notifications.</span></span> 
    
<span data-ttu-id="78e28-114">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="78e28-114">_lpulFlags_</span></span>
  
> <span data-ttu-id="78e28-115">[in, out] Битовая маска флаги, который управляет процессом уведомления.</span><span class="sxs-lookup"><span data-stu-id="78e28-115">[in, out] A bitmask of flags that controls the notification process.</span></span> <span data-ttu-id="78e28-116">Для ввода данных можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="78e28-116">On input, the following flag can be set:</span></span>
    
  - <span data-ttu-id="78e28-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="78e28-117">MAPI_UNICODE</span></span> 
    
    > <span data-ttu-id="78e28-118">Строки в структур уведомлений, на который указывает _lpNotifications_ хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="78e28-118">The strings in the notification structures pointed to by  _lpNotifications_ are in Unicode format.</span></span> <span data-ttu-id="78e28-119">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="78e28-119">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 

    <span data-ttu-id="78e28-120">На выходе MAPI можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="78e28-120">On output, MAPI can set the following flag:</span></span>
        
  - <span data-ttu-id="78e28-121">NOTIFY_CANCELED</span><span class="sxs-lookup"><span data-stu-id="78e28-121">NOTIFY_CANCELED</span></span> 
    
    > <span data-ttu-id="78e28-122">Функция обратного вызова отменено синхронного уведомления.</span><span class="sxs-lookup"><span data-stu-id="78e28-122">A callback function canceled a synchronous notification.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="78e28-123">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="78e28-123">Return value</span></span>

<span data-ttu-id="78e28-124">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="78e28-124">S_OK</span></span> 
  
> <span data-ttu-id="78e28-125">Уведомления были успешно созданы.</span><span class="sxs-lookup"><span data-stu-id="78e28-125">The notifications were successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="78e28-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="78e28-126">Remarks</span></span>

<span data-ttu-id="78e28-127">Метод **IMAPISupport::Notify** применяется для всех объектов поддержки поставщика службы.</span><span class="sxs-lookup"><span data-stu-id="78e28-127">The **IMAPISupport::Notify** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="78e28-128">Поставщики услуг вызова **уведомления** для запроса, что MAPI создания уведомления для приемника уведомления, который ранее был зарегистрирован для уведомления через метод **IMAPISupport::Subscribe** .</span><span class="sxs-lookup"><span data-stu-id="78e28-128">Service providers call **Notify** to request that MAPI generate a notification for an advise sink that has previously registered for the notification through the **IMAPISupport::Subscribe** method.</span></span> 
  
<span data-ttu-id="78e28-129">**Уведомлять** копии структур указывает параметр _lpNotifications_ в память и вызывает метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) приемник соответствующих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="78e28-129">**Notify** copies the structures pointed to by the  _lpNotifications_ parameter into memory and calls the appropriate advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="78e28-130">По завершении **OnNotify** с уведомлением освобождает используемые памяти.</span><span class="sxs-lookup"><span data-stu-id="78e28-130">When **OnNotify** is finished with the notification, it releases the memory involved.</span></span> <span data-ttu-id="78e28-131">Вызывающий не нужно выделить память; MAPI выполняет все необходимые памяти.</span><span class="sxs-lookup"><span data-stu-id="78e28-131">The caller does not need to allocate memory; MAPI performs all necessary memory allocation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="78e28-132">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="78e28-132">Notes to callers</span></span>

<span data-ttu-id="78e28-133">Клавиша уведомлений, переданной в параметре _lpKey_ должен быть идентичен ключ, переданный в метод **IMAPISupport::Subscribe** _lpKey_ .</span><span class="sxs-lookup"><span data-stu-id="78e28-133">The notification key passed in the  _lpKey_ parameter should be identical to the key passed in  _lpKey_ to the **IMAPISupport::Subscribe** method.</span></span> <span data-ttu-id="78e28-134">Многие поставщики используется идентификатор записи источника уведомлений в качестве ключа, но можно использовать другие данные, такие как пути к файлу.</span><span class="sxs-lookup"><span data-stu-id="78e28-134">Many providers use the entry identifier of the advise source as the key, but other data, such as a file path, can be used.</span></span> <span data-ttu-id="78e28-135">MAPI использует этот ключ для поиска всех регистраций уведомлений на источник определенного уведомлений.</span><span class="sxs-lookup"><span data-stu-id="78e28-135">MAPI uses this key to find all the registrations for notifications on the identified advise source.</span></span> 
  
<span data-ttu-id="78e28-136">Не забудьте установить член **lpEntryID** структуры уведомления для долгосрочного идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="78e28-136">Be sure that you set the **lpEntryID** member of the notification structure to a long-term entry identifier.</span></span> 
  
<span data-ttu-id="78e28-137">Если задать флаг NOTIFY_SYNC на **подписки на** звонок для каких-либо ожидающие уведомления **Уведомлять** звонки в функции обратного вызова метода **IMAPIAdviseSink::OnNotify** перед возвращением.</span><span class="sxs-lookup"><span data-stu-id="78e28-137">If you set the NOTIFY_SYNC flag on the **Subscribe** call for any of the pending notifications, **Notify** calls the **IMAPIAdviseSink::OnNotify** method callback functions before returning.</span></span> <span data-ttu-id="78e28-138">Приемника уведомления могут создаваться вручную или посредством вызова [HrAllocAdviseSink](hrallocadvisesink.md).</span><span class="sxs-lookup"><span data-stu-id="78e28-138">An advise sink can be created manually or by calling [HrAllocAdviseSink](hrallocadvisesink.md).</span></span> <span data-ttu-id="78e28-139">Функция **HrAllocAdviseSink** позволяет указать функции обратного вызова, звонки **Уведомлять** как часть уведомления, вызывающий.</span><span class="sxs-lookup"><span data-stu-id="78e28-139">The **HrAllocAdviseSink** function allows its caller to specify a callback function that **Notify** calls as part of the notification.</span></span> <span data-ttu-id="78e28-140">Если функция обратного вызова соответствует прототип [NOTIFCALLBACK](notifcallback.md) .</span><span class="sxs-lookup"><span data-stu-id="78e28-140">The callback function conforms to the [NOTIFCALLBACK](notifcallback.md) prototype.</span></span> <span data-ttu-id="78e28-141">Функции обратного вызова, реализуемый клиентами всегда возвращает значение S_OK; функции обратного вызова, реализованные поставщиков услуг может вернуть CALLBACK_DISCONTINUE.</span><span class="sxs-lookup"><span data-stu-id="78e28-141">Callback functions implemented by clients always return S_OK; callback functions implemented by service providers can return CALLBACK_DISCONTINUE.</span></span> 
  
<span data-ttu-id="78e28-142">Если функция обратного вызова возвращает CALLBACK_DISCONTINUE, MAPI останавливает отправки уведомлений и возвращает NOTIFY_CANCELED в параметре _lpulFlags_ метод **уведомления** .</span><span class="sxs-lookup"><span data-stu-id="78e28-142">If a callback function returns CALLBACK_DISCONTINUE, MAPI stops sending notifications and returns NOTIFY_CANCELED in the **Notify** method's  _lpulFlags_ parameter.</span></span> <span data-ttu-id="78e28-143">Предполагается, что процесс неактивных и завершения создания уведомлений для этого процесса.</span><span class="sxs-lookup"><span data-stu-id="78e28-143">You can assume that the process is inactive and stop generating notifications for that process.</span></span> <span data-ttu-id="78e28-144">Если **уведомление** возвращает 0 в _lpulFlags_, процесс по-прежнему активен и должны продолжать отправлять уведомления, соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="78e28-144">If **Notify** returns 0 in  _lpulFlags_, the process is still active and you should continue to send notifications, as appropriate.</span></span>
  
<span data-ttu-id="78e28-145">При использовании синхронного уведомления, будьте внимательны, чтобы избежать подобных ситуаций.</span><span class="sxs-lookup"><span data-stu-id="78e28-145">When you use synchronous notifications, be careful to avoid deadlock situations.</span></span>
  
<span data-ttu-id="78e28-146">Дополнительные сведения о процессе уведомления содержатся в разделе [Уведомление о событии в MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="78e28-146">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="78e28-147">См. также</span><span class="sxs-lookup"><span data-stu-id="78e28-147">See also</span></span>

- [<span data-ttu-id="78e28-148">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="78e28-148">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)  
- [<span data-ttu-id="78e28-149">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="78e28-149">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)  
- [<span data-ttu-id="78e28-150">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="78e28-150">NOTIFCALLBACK</span></span>](notifcallback.md) 
- [<span data-ttu-id="78e28-151">�����������</span><span class="sxs-lookup"><span data-stu-id="78e28-151">NOTIFICATION</span></span>](notification.md)  
- [<span data-ttu-id="78e28-152">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="78e28-152">NOTIFKEY</span></span>](notifkey.md)  
- [<span data-ttu-id="78e28-153">Каноническое свойство PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="78e28-153">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)  
- [<span data-ttu-id="78e28-154">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="78e28-154">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

