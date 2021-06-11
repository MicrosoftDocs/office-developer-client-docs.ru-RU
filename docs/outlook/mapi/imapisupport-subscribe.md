---
title: IMAPISupportSubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Subscribe
api_type:
- COM
ms.assetid: e6baaff1-446e-431a-a09b-9b529153382b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5a8c288e877078ece6ab2da8c6494d96e1714ad7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419928"
---
# <a name="imapisupportsubscribe"></a><span data-ttu-id="26cf5-103">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="26cf5-103">IMAPISupport::Subscribe</span></span>

  
  
<span data-ttu-id="26cf5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26cf5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26cf5-105">Регистрирует раковину рекомендации для получения уведомлений через MAPI.</span><span class="sxs-lookup"><span data-stu-id="26cf5-105">Registers an advise sink to receive notifications through MAPI.</span></span>
  
```cpp
HRESULT Subscribe(
LPNOTIFKEY lpKey,
ULONG ulEventMask,
ULONG ulFlags,
LPMAPIADVISESINK lpAdviseSink,
ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="26cf5-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="26cf5-106">Parameters</span></span>

 <span data-ttu-id="26cf5-107">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="26cf5-107">_lpKey_</span></span>
  
> <span data-ttu-id="26cf5-108">[in] Указатель на ключ уведомлений, который представляет исходный объект консультации.</span><span class="sxs-lookup"><span data-stu-id="26cf5-108">[in] A pointer to a notification key that represents the advise source object.</span></span> <span data-ttu-id="26cf5-109">Параметр  _lpKey не_ может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="26cf5-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="26cf5-110">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="26cf5-110">_ulEventMask_</span></span>
  
> <span data-ttu-id="26cf5-111">[in] Маска значений, которые указывают типы событий уведомлений, которые интересуют вызываемого и должны быть включены в регистрацию.</span><span class="sxs-lookup"><span data-stu-id="26cf5-111">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="26cf5-112">Допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="26cf5-112">The following values are valid:</span></span>
    
 <span data-ttu-id="26cf5-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="26cf5-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="26cf5-114">Регистрирует уведомления о серьезных ошибках, например о недостаточной памяти.</span><span class="sxs-lookup"><span data-stu-id="26cf5-114">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="26cf5-115">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="26cf5-115">_fnevExtended_</span></span>
  
> <span data-ttu-id="26cf5-116">Регистрация уведомлений о событиях, определенных конкретному поставщику адресной книги или магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="26cf5-116">Registers for notifications about events specific to the particular address book or message store provider.</span></span>
    
 <span data-ttu-id="26cf5-117">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="26cf5-117">_fnevNewMail_</span></span>
  
> <span data-ttu-id="26cf5-118">Регистрация уведомлений о прибытии новых сообщений.</span><span class="sxs-lookup"><span data-stu-id="26cf5-118">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="26cf5-119">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="26cf5-119">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="26cf5-120">Регистрирует уведомления о создании нового объекта.</span><span class="sxs-lookup"><span data-stu-id="26cf5-120">Registers for notifications about the creation of a new object.</span></span>
    
 <span data-ttu-id="26cf5-121">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="26cf5-121">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="26cf5-122">Регистрация уведомлений о копировании объекта.</span><span class="sxs-lookup"><span data-stu-id="26cf5-122">Registers for notifications about an object being copied.</span></span>
    
 <span data-ttu-id="26cf5-123">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="26cf5-123">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="26cf5-124">Регистрация уведомлений об удалении объекта.</span><span class="sxs-lookup"><span data-stu-id="26cf5-124">Registers for notifications about an object being deleted.</span></span>
    
 <span data-ttu-id="26cf5-125">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="26cf5-125">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="26cf5-126">Регистры уведомлений о модифицированном объекте.</span><span class="sxs-lookup"><span data-stu-id="26cf5-126">Registers for notifications about an object being modified.</span></span>
    
 <span data-ttu-id="26cf5-127">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="26cf5-127">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="26cf5-128">Регистрация уведомлений о перемещении объекта.</span><span class="sxs-lookup"><span data-stu-id="26cf5-128">Registers for notifications about an object being moved.</span></span>
    
 <span data-ttu-id="26cf5-129">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="26cf5-129">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="26cf5-130">Регистрация уведомлений о завершении операции поиска.</span><span class="sxs-lookup"><span data-stu-id="26cf5-130">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="26cf5-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="26cf5-131">_ulFlags_</span></span>
  
> <span data-ttu-id="26cf5-132">[in] Битмашка флагов, которые контролируют, как происходит уведомление.</span><span class="sxs-lookup"><span data-stu-id="26cf5-132">[in] A bitmask of flags that controls how notification occurs.</span></span> <span data-ttu-id="26cf5-133">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="26cf5-133">The following flag can be set:</span></span>
    
<span data-ttu-id="26cf5-134">NOTIFY_SYNC</span><span class="sxs-lookup"><span data-stu-id="26cf5-134">NOTIFY_SYNC</span></span> 
  
> <span data-ttu-id="26cf5-135">Когда звонящий вызывает [метод IMAPISupport::Notify](imapisupport-notify.md) для создания уведомлений для этой раковины **рекомендации,** Сообщите должны сделать все необходимые вызовы, чтобы проконсультировать раковины перед возвращением.</span><span class="sxs-lookup"><span data-stu-id="26cf5-135">When the caller calls the [IMAPISupport::Notify](imapisupport-notify.md) method to generate notifications for this advise sink, **Notify** should make all necessary calls to advise sinks before returning.</span></span> <span data-ttu-id="26cf5-136">Если этот флаг не установлен, уведомление является асинхронным, а вызовы вызовов в очереди на процессы, которые подписаны и запущены, когда эти процессы получают контроль над ЦП.</span><span class="sxs-lookup"><span data-stu-id="26cf5-136">If this flag is not set, notification is asynchronous and callbacks are queued to the processes that have subscribed and started when those processes gain control of the CPU.</span></span> 
    
 <span data-ttu-id="26cf5-137">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="26cf5-137">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="26cf5-138">[in] Указатель на объект раковины рекомендации.</span><span class="sxs-lookup"><span data-stu-id="26cf5-138">[in] A pointer to an advise sink object.</span></span> 
    
 <span data-ttu-id="26cf5-139">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="26cf5-139">_lpulConnection_</span></span>
  
> <span data-ttu-id="26cf5-140">[вышел] Указатель на номер подключения незеро, который представляет регистрацию.</span><span class="sxs-lookup"><span data-stu-id="26cf5-140">[out] A pointer to a nonzero connection number that represents the registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="26cf5-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="26cf5-141">Return value</span></span>

<span data-ttu-id="26cf5-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="26cf5-142">S_OK</span></span> 
  
> <span data-ttu-id="26cf5-143">Регистрация уведомлений прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="26cf5-143">The notification registration was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="26cf5-144">Примечания</span><span class="sxs-lookup"><span data-stu-id="26cf5-144">Remarks</span></span>

<span data-ttu-id="26cf5-145">Метод **IMAPISupport::Subscribe** реализован для всех объектов поддержки поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="26cf5-145">The **IMAPISupport::Subscribe** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="26cf5-146">Поставщики услуг **звонят Подписка** из одного из методов **консультирования,** чтобы разрешить MAPI управлять уведомлениями.</span><span class="sxs-lookup"><span data-stu-id="26cf5-146">Service providers call **Subscribe** from one of their **Advise** methods to allow MAPI to manage the notifications.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="26cf5-147">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="26cf5-147">Notes to callers</span></span>

<span data-ttu-id="26cf5-148">Чтобы использовать методы поддержки MAPI для уведомления, создайте ключ для источника консультаций объекта, о котором должны создаваться уведомления.</span><span class="sxs-lookup"><span data-stu-id="26cf5-148">To use the MAPI support methods for notification, create a key for the advise source the object about which notifications should be generated.</span></span> <span data-ttu-id="26cf5-149">Значение ключа должно быть уникальным и легко регенерироваться каждый раз, когда объект изменяется.</span><span class="sxs-lookup"><span data-stu-id="26cf5-149">The value of the key must be unique and should be easily regenerated each time the object changes.</span></span> 
  
<span data-ttu-id="26cf5-150">MAPI использует ключ уведомления для поиска любых функций вызова, зарегистрированных через функцию [HrAllocAdviseSink](hrallocadvisesink.md) для соответствующего источника консультаций.</span><span class="sxs-lookup"><span data-stu-id="26cf5-150">MAPI uses the notification key to search for any callback functions registered through the [HrAllocAdviseSink](hrallocadvisesink.md) function for the corresponding advise source.</span></span> <span data-ttu-id="26cf5-151">Передай этот ключ **В IMAPISupport:::Notify,** когда необходимо создать уведомление для соответствующего источника консультаций.</span><span class="sxs-lookup"><span data-stu-id="26cf5-151">Pass this key to **IMAPISupport::Notify** whenever you need to generate a notification for the corresponding advise source.</span></span> 
  
<span data-ttu-id="26cf5-152">Флаг NOTIFY_SYNC влияет на работу последующих вызовов для **уведомления**.</span><span class="sxs-lookup"><span data-stu-id="26cf5-152">The NOTIFY_SYNC flag affects the operation of subsequent calls to **Notify**.</span></span> <span data-ttu-id="26cf5-153">Когда вы NOTIFY_SYNC, **Уведомление** не возвращается, пока не завершит отправку всех необходимых уведомлений.</span><span class="sxs-lookup"><span data-stu-id="26cf5-153">When you set NOTIFY_SYNC, **Notify** does not return until it has finished sending all of the necessary notifications.</span></span> <span data-ttu-id="26cf5-154">Если вы не NOTIFY_SYNC, **уведомление** работает асинхронно, возможно, возвращается до всех уведомлений были отправлены.</span><span class="sxs-lookup"><span data-stu-id="26cf5-154">When you do not set NOTIFY_SYNC, **Notify** operates asynchronously, possibly returning before all of the notifications have been sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="26cf5-155">См. также</span><span class="sxs-lookup"><span data-stu-id="26cf5-155">See also</span></span>



[<span data-ttu-id="26cf5-156">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="26cf5-156">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="26cf5-157">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="26cf5-157">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="26cf5-158">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="26cf5-158">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="26cf5-159">�����������</span><span class="sxs-lookup"><span data-stu-id="26cf5-159">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="26cf5-160">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="26cf5-160">NOTIFKEY</span></span>](notifkey.md)
  
[<span data-ttu-id="26cf5-161">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="26cf5-161">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

