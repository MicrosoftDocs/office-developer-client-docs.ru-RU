---
title: Имаписуппортнотифи
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
# <a name="imapisupportnotify"></a><span data-ttu-id="42b2f-103">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="42b2f-103">IMAPISupport::Notify</span></span>

<span data-ttu-id="42b2f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42b2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42b2f-105">Отправляет уведомление об указанном событии источнику уведомлений, который был изначально зарегистрирован для уведомления с помощью метода [имаписуппорт:: Subscribe](imapisupport-subscribe.md) .</span><span class="sxs-lookup"><span data-stu-id="42b2f-105">Sends a notification of a specified event to an advise source that originally registered for the notification through the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method.</span></span> 
  
```cpp
HRESULT Notify(
LPNOTIFKEY lpKey,
ULONG cNotification,
LPNOTIFICATION lpNotifications,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="42b2f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="42b2f-106">Parameters</span></span>

<span data-ttu-id="42b2f-107">_Лпкэй_</span><span class="sxs-lookup"><span data-stu-id="42b2f-107">_lpKey_</span></span>
  
> <span data-ttu-id="42b2f-108">возврата Указатель на ключ уведомления для исходного объекта Advise.</span><span class="sxs-lookup"><span data-stu-id="42b2f-108">[in] A pointer to the notification key for the advise source object.</span></span> <span data-ttu-id="42b2f-109">Параметр _лпкэй_ не может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="42b2f-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
<span data-ttu-id="42b2f-110">_Кнотификатион_</span><span class="sxs-lookup"><span data-stu-id="42b2f-110">_cNotification_</span></span>
  
> <span data-ttu-id="42b2f-111">возврата Количество структур уведомлений, на которые указывает параметр _лпнотификатионс_ .</span><span class="sxs-lookup"><span data-stu-id="42b2f-111">[in] The count of notification structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
<span data-ttu-id="42b2f-112">_Лпнотификатионс_</span><span class="sxs-lookup"><span data-stu-id="42b2f-112">_lpNotifications_</span></span>
  
> <span data-ttu-id="42b2f-113">возврата Указатель на массив структур [уведомлений](notification.md) , описывающих ожидающие уведомления.</span><span class="sxs-lookup"><span data-stu-id="42b2f-113">[in] A pointer to an array of [NOTIFICATION](notification.md) structures that describe pending notifications.</span></span> 
    
<span data-ttu-id="42b2f-114">_Лпулфлагс_</span><span class="sxs-lookup"><span data-stu-id="42b2f-114">_lpulFlags_</span></span>
  
> <span data-ttu-id="42b2f-115">[вход, выход] Битовая маска флагов, управляющих процессом уведомления.</span><span class="sxs-lookup"><span data-stu-id="42b2f-115">[in, out] A bitmask of flags that controls the notification process.</span></span> <span data-ttu-id="42b2f-116">На входе можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="42b2f-116">On input, the following flag can be set:</span></span>
    
  - <span data-ttu-id="42b2f-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="42b2f-117">MAPI_UNICODE</span></span> 
    
    > <span data-ttu-id="42b2f-118">Строки в структурах уведомлений, на которые указывает _лпнотификатионс_ , представлены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="42b2f-118">The strings in the notification structures pointed to by  _lpNotifications_ are in Unicode format.</span></span> <span data-ttu-id="42b2f-119">Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="42b2f-119">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 

    <span data-ttu-id="42b2f-120">В выходных данных MAPI может установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="42b2f-120">On output, MAPI can set the following flag:</span></span>
        
  - <span data-ttu-id="42b2f-121">НОТИФИ_КАНЦЕЛЕД</span><span class="sxs-lookup"><span data-stu-id="42b2f-121">NOTIFY_CANCELED</span></span> 
    
    > <span data-ttu-id="42b2f-122">Функция обратного вызова отменила синхронное уведомление.</span><span class="sxs-lookup"><span data-stu-id="42b2f-122">A callback function canceled a synchronous notification.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="42b2f-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42b2f-123">Return value</span></span>

<span data-ttu-id="42b2f-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="42b2f-124">S_OK</span></span> 
  
> <span data-ttu-id="42b2f-125">Уведомления успешно созданы.</span><span class="sxs-lookup"><span data-stu-id="42b2f-125">The notifications were successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="42b2f-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="42b2f-126">Remarks</span></span>

<span data-ttu-id="42b2f-127">Метод **имаписуппорт:: notify** реализован для всех объектов поддержки поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="42b2f-127">The **IMAPISupport::Notify** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="42b2f-128">Поставщики услуг вызывают **уведомление** , чтобы запросить создание уведомления для приемника уведомлений, который ранее был зарегистрирован для получения уведомлений с помощью метода **Имаписуппорт:: Subscribe** .</span><span class="sxs-lookup"><span data-stu-id="42b2f-128">Service providers call **Notify** to request that MAPI generate a notification for an advise sink that has previously registered for the notification through the **IMAPISupport::Subscribe** method.</span></span> 
  
<span data-ttu-id="42b2f-129">**Notify** копирует структуры, на которые указывает параметр _лпнотификатионс_ , в память и вызывает соответствующий метод [имапиадвисесинк:: OnNotify](imapiadvisesink-onnotify.md) приемника уведомлений.</span><span class="sxs-lookup"><span data-stu-id="42b2f-129">**Notify** copies the structures pointed to by the  _lpNotifications_ parameter into memory and calls the appropriate advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="42b2f-130">Когда \*\*\*\* уведомление OnNotify завершается с уведомлением, оно освобождает используемую память.</span><span class="sxs-lookup"><span data-stu-id="42b2f-130">When **OnNotify** is finished with the notification, it releases the memory involved.</span></span> <span data-ttu-id="42b2f-131">Вызывающему объекту не требуется выделять память; MAPI выполняет все необходимое выделение памяти.</span><span class="sxs-lookup"><span data-stu-id="42b2f-131">The caller does not need to allocate memory; MAPI performs all necessary memory allocation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="42b2f-132">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="42b2f-132">Notes to callers</span></span>

<span data-ttu-id="42b2f-133">Ключ уведомления, переданный в параметре _лпкэй_ , должен совпадать с ключом, переданным в _лпкэй_ , в метод **Subscribe:: Subscribe** .</span><span class="sxs-lookup"><span data-stu-id="42b2f-133">The notification key passed in the  _lpKey_ parameter should be identical to the key passed in  _lpKey_ to the **IMAPISupport::Subscribe** method.</span></span> <span data-ttu-id="42b2f-134">Многие поставщики используют идентификатор записи источника advise в качестве ключа, но другие данные, например путь к файлу, можно использовать.</span><span class="sxs-lookup"><span data-stu-id="42b2f-134">Many providers use the entry identifier of the advise source as the key, but other data, such as a file path, can be used.</span></span> <span data-ttu-id="42b2f-135">MAPI использует этот ключ для поиска всех регистраций для уведомлений по указанному источнику рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="42b2f-135">MAPI uses this key to find all the registrations for notifications on the identified advise source.</span></span> 
  
<span data-ttu-id="42b2f-136">Убедитесь, что для элемента **лпентрид** структуры уведомлений задан долгосрочный идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="42b2f-136">Be sure that you set the **lpEntryID** member of the notification structure to a long-term entry identifier.</span></span> 
  
<span data-ttu-id="42b2f-137">Если установить флаг НОТИФИ_СИНК для вызова **Subscribe** для любого из ожидающих уведомлений, **уведомление** вызывает функции обратного вызова метода **имапиадвисесинк:: OnNotify** перед возвратом.</span><span class="sxs-lookup"><span data-stu-id="42b2f-137">If you set the NOTIFY_SYNC flag on the **Subscribe** call for any of the pending notifications, **Notify** calls the **IMAPIAdviseSink::OnNotify** method callback functions before returning.</span></span> <span data-ttu-id="42b2f-138">Приемник уведомлений можно создать вручную или с помощью вызова [храллокадвисесинк](hrallocadvisesink.md).</span><span class="sxs-lookup"><span data-stu-id="42b2f-138">An advise sink can be created manually or by calling [HrAllocAdviseSink](hrallocadvisesink.md).</span></span> <span data-ttu-id="42b2f-139">Функция **храллокадвисесинк** позволяет своему абоненту указать функцию обратного вызова, \*\*\*\* которая уведомляет вызовы как часть уведомления.</span><span class="sxs-lookup"><span data-stu-id="42b2f-139">The **HrAllocAdviseSink** function allows its caller to specify a callback function that **Notify** calls as part of the notification.</span></span> <span data-ttu-id="42b2f-140">Функция обратного вызова соответствует прототипу [нотифкаллбакк](notifcallback.md) .</span><span class="sxs-lookup"><span data-stu-id="42b2f-140">The callback function conforms to the [NOTIFCALLBACK](notifcallback.md) prototype.</span></span> <span data-ttu-id="42b2f-141">Функции обратного вызова, реализованные клиентами, всегда возвращают значение S_OK; функции обратного вызова, реализованные поставщиками услуг, могут возвращать КАЛЛБАКК_ДИСКОНТИНУЕ.</span><span class="sxs-lookup"><span data-stu-id="42b2f-141">Callback functions implemented by clients always return S_OK; callback functions implemented by service providers can return CALLBACK_DISCONTINUE.</span></span> 
  
<span data-ttu-id="42b2f-142">Если функция обратного вызова возвращает КАЛЛБАКК_ДИСКОНТИНУЕ, MAPI перестает отправлять уведомления и возвращает НОТИФИ_КАНЦЕЛЕД в параметре _лпулфлагс_ метода **Notify** .</span><span class="sxs-lookup"><span data-stu-id="42b2f-142">If a callback function returns CALLBACK_DISCONTINUE, MAPI stops sending notifications and returns NOTIFY_CANCELED in the **Notify** method's  _lpulFlags_ parameter.</span></span> <span data-ttu-id="42b2f-143">Вы можете предположить, что этот процесс неактивен и не будет создавать уведомления для этого процесса.</span><span class="sxs-lookup"><span data-stu-id="42b2f-143">You can assume that the process is inactive and stop generating notifications for that process.</span></span> <span data-ttu-id="42b2f-144">Если **Notify** возвращает 0 в _лпулфлагс_, процесс все еще активен и вы должны продолжать отправлять уведомления по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="42b2f-144">If **Notify** returns 0 in  _lpulFlags_, the process is still active and you should continue to send notifications, as appropriate.</span></span>
  
<span data-ttu-id="42b2f-145">При использовании синхронных уведомлений следите, чтобы избежать ситуаций взаимоблокировки.</span><span class="sxs-lookup"><span data-stu-id="42b2f-145">When you use synchronous notifications, be careful to avoid deadlock situations.</span></span>
  
<span data-ttu-id="42b2f-146">Дополнительные сведения о процессе уведомления можно найти в статье [уведомление о событии в MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="42b2f-146">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="42b2f-147">См. также</span><span class="sxs-lookup"><span data-stu-id="42b2f-147">See also</span></span>

- [<span data-ttu-id="42b2f-148">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="42b2f-148">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)  
- [<span data-ttu-id="42b2f-149">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="42b2f-149">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)  
- [<span data-ttu-id="42b2f-150">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="42b2f-150">NOTIFCALLBACK</span></span>](notifcallback.md) 
- [<span data-ttu-id="42b2f-151">�����������</span><span class="sxs-lookup"><span data-stu-id="42b2f-151">NOTIFICATION</span></span>](notification.md)  
- [<span data-ttu-id="42b2f-152">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="42b2f-152">NOTIFKEY</span></span>](notifkey.md)  
- [<span data-ttu-id="42b2f-153">Каноническое свойство PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="42b2f-153">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)  
- [<span data-ttu-id="42b2f-154">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="42b2f-154">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

