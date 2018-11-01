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
ms.openlocfilehash: beeca6ba958c38e12fba7dbc2884c81e58bdf3c4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590122"
---
# <a name="imapisupportsubscribe"></a><span data-ttu-id="d5d25-103">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="d5d25-103">IMAPISupport::Subscribe</span></span>

  
  
<span data-ttu-id="d5d25-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5d25-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5d25-105">Регистрирует приемника уведомления для получения уведомлений через MAPI.</span><span class="sxs-lookup"><span data-stu-id="d5d25-105">Registers an advise sink to receive notifications through MAPI.</span></span>
  
```cpp
HRESULT Subscribe(
LPNOTIFKEY lpKey,
ULONG ulEventMask,
ULONG ulFlags,
LPMAPIADVISESINK lpAdviseSink,
ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="d5d25-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5d25-106">Parameters</span></span>

 <span data-ttu-id="d5d25-107">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="d5d25-107">_lpKey_</span></span>
  
> <span data-ttu-id="d5d25-108">[in] Указатель на ключ уведомлений, представляющий объект источника уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d5d25-108">[in] A pointer to a notification key that represents the advise source object.</span></span> <span data-ttu-id="d5d25-109">Параметр _lpKey_ не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="d5d25-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="d5d25-110">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="d5d25-110">_ulEventMask_</span></span>
  
> <span data-ttu-id="d5d25-111">[in] Маска значения, которые указывают на тип события уведомлений, вызывающего заинтересована в и должно быть включено в регистрации.</span><span class="sxs-lookup"><span data-stu-id="d5d25-111">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="d5d25-112">Допустимыми являются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d5d25-112">The following values are valid:</span></span>
    
 <span data-ttu-id="d5d25-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="d5d25-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="d5d25-114">Регистрирует уведомлений о серьезной ошибки, например недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="d5d25-114">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="d5d25-115">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="d5d25-115">_fnevExtended_</span></span>
  
> <span data-ttu-id="d5d25-116">Поставщик хранилища регистрирует для уведомлений о событиях, характерные для определенного адресной книги или сообщения.</span><span class="sxs-lookup"><span data-stu-id="d5d25-116">Registers for notifications about events specific to the particular address book or message store provider.</span></span>
    
 <span data-ttu-id="d5d25-117">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="d5d25-117">_fnevNewMail_</span></span>
  
> <span data-ttu-id="d5d25-118">Регистрирует уведомлений о появлении нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="d5d25-118">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="d5d25-119">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="d5d25-119">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="d5d25-120">Регистрирует уведомлений о создании нового объекта.</span><span class="sxs-lookup"><span data-stu-id="d5d25-120">Registers for notifications about the creation of a new object.</span></span>
    
 <span data-ttu-id="d5d25-121">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="d5d25-121">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="d5d25-122">Регистрирует для уведомлений об объекте копируются.</span><span class="sxs-lookup"><span data-stu-id="d5d25-122">Registers for notifications about an object being copied.</span></span>
    
 <span data-ttu-id="d5d25-123">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="d5d25-123">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="d5d25-124">Регистрирует для уведомлений об объекте удаляются.</span><span class="sxs-lookup"><span data-stu-id="d5d25-124">Registers for notifications about an object being deleted.</span></span>
    
 <span data-ttu-id="d5d25-125">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="d5d25-125">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="d5d25-126">Регистрирует для уведомлений об объекте изменяется.</span><span class="sxs-lookup"><span data-stu-id="d5d25-126">Registers for notifications about an object being modified.</span></span>
    
 <span data-ttu-id="d5d25-127">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="d5d25-127">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="d5d25-128">Регистрирует для уведомлений об объекте происходит перемещение.</span><span class="sxs-lookup"><span data-stu-id="d5d25-128">Registers for notifications about an object being moved.</span></span>
    
 <span data-ttu-id="d5d25-129">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="d5d25-129">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="d5d25-130">Регистрирует для уведомлений о завершении операции поиска.</span><span class="sxs-lookup"><span data-stu-id="d5d25-130">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="d5d25-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d5d25-131">_ulFlags_</span></span>
  
> <span data-ttu-id="d5d25-132">[in] Битовая маска флаги, определяющее, как выполняется уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d5d25-132">[in] A bitmask of flags that controls how notification occurs.</span></span> <span data-ttu-id="d5d25-133">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="d5d25-133">The following flag can be set:</span></span>
    
<span data-ttu-id="d5d25-134">NOTIFY_SYNC</span><span class="sxs-lookup"><span data-stu-id="d5d25-134">NOTIFY_SYNC</span></span> 
  
> <span data-ttu-id="d5d25-135">Когда вызывающего вызывает метод [IMAPISupport::Notify](imapisupport-notify.md) для создания уведомлений для этой приемник уведомлений, **Уведомлять** должна вызывать все необходимые приемников уведомлений перед возвращением.</span><span class="sxs-lookup"><span data-stu-id="d5d25-135">When the caller calls the [IMAPISupport::Notify](imapisupport-notify.md) method to generate notifications for this advise sink, **Notify** should make all necessary calls to advise sinks before returning.</span></span> <span data-ttu-id="d5d25-136">Если этот флаг не установлен, уведомление является асинхронным и обратных вызовов в очереди для процессов, которые подписаны и при этих процессов регулировка процессора.</span><span class="sxs-lookup"><span data-stu-id="d5d25-136">If this flag is not set, notification is asynchronous and callbacks are queued to the processes that have subscribed and started when those processes gain control of the CPU.</span></span> 
    
 <span data-ttu-id="d5d25-137">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="d5d25-137">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="d5d25-138">[in] Указатель на объект приемник уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d5d25-138">[in] A pointer to an advise sink object.</span></span> 
    
 <span data-ttu-id="d5d25-139">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="d5d25-139">_lpulConnection_</span></span>
  
> <span data-ttu-id="d5d25-140">[out] Указатель на подключение ненулевое число, представляющее регистрации.</span><span class="sxs-lookup"><span data-stu-id="d5d25-140">[out] A pointer to a nonzero connection number that represents the registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d5d25-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5d25-141">Return value</span></span>

<span data-ttu-id="d5d25-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="d5d25-142">S_OK</span></span> 
  
> <span data-ttu-id="d5d25-143">Уведомление о регистрации прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="d5d25-143">The notification registration was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d5d25-144">Замечания</span><span class="sxs-lookup"><span data-stu-id="d5d25-144">Remarks</span></span>

<span data-ttu-id="d5d25-145">Метод **IMAPISupport::Subscribe** применяется для всех объектов поддержки поставщика службы.</span><span class="sxs-lookup"><span data-stu-id="d5d25-145">The **IMAPISupport::Subscribe** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="d5d25-146">**Подписки на** вызова поставщиков услуг от одного из своих **уведомлений** методы, позволяющие MAPI для управления уведомления.</span><span class="sxs-lookup"><span data-stu-id="d5d25-146">Service providers call **Subscribe** from one of their **Advise** methods to allow MAPI to manage the notifications.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d5d25-147">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="d5d25-147">Notes to callers</span></span>

<span data-ttu-id="d5d25-148">Чтобы использовать методы поддержки MAPI для уведомлений, создание ключа источника уведомлений, будет создан объект о уведомления, которое.</span><span class="sxs-lookup"><span data-stu-id="d5d25-148">To use the MAPI support methods for notification, create a key for the advise source the object about which notifications should be generated.</span></span> <span data-ttu-id="d5d25-149">Значение ключа должно быть уникальным и должны быть легко ключа при каждом изменении объекта.</span><span class="sxs-lookup"><span data-stu-id="d5d25-149">The value of the key must be unique and should be easily regenerated each time the object changes.</span></span> 
  
<span data-ttu-id="d5d25-150">MAPI использует уведомления ключ для поиска функций обратного вызова, зарегистрированных в функцию [HrAllocAdviseSink](hrallocadvisesink.md) для соответствующий источник уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d5d25-150">MAPI uses the notification key to search for any callback functions registered through the [HrAllocAdviseSink](hrallocadvisesink.md) function for the corresponding advise source.</span></span> <span data-ttu-id="d5d25-151">Передайте этот ключ **IMAPISupport::Notify** каждый раз, когда должны получать уведомления о соответствующий источник уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d5d25-151">Pass this key to **IMAPISupport::Notify** whenever you need to generate a notification for the corresponding advise source.</span></span> 
  
<span data-ttu-id="d5d25-152">Флаг NOTIFY_SYNC влияет на операции последующие вызовы **уведомлений**.</span><span class="sxs-lookup"><span data-stu-id="d5d25-152">The NOTIFY_SYNC flag affects the operation of subsequent calls to **Notify**.</span></span> <span data-ttu-id="d5d25-153">При установке NOTIFY_SYNC **Уведомлять** не возвращается до завершения отправки все необходимые уведомления.</span><span class="sxs-lookup"><span data-stu-id="d5d25-153">When you set NOTIFY_SYNC, **Notify** does not return until it has finished sending all of the necessary notifications.</span></span> <span data-ttu-id="d5d25-154">Если NOTIFY_SYNC не задано, **Уведомлять** работает асинхронно, возможно, с возвращаемым перед все уведомления было отправлено.</span><span class="sxs-lookup"><span data-stu-id="d5d25-154">When you do not set NOTIFY_SYNC, **Notify** operates asynchronously, possibly returning before all of the notifications have been sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d5d25-155">См. также</span><span class="sxs-lookup"><span data-stu-id="d5d25-155">See also</span></span>



[<span data-ttu-id="d5d25-156">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="d5d25-156">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="d5d25-157">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="d5d25-157">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="d5d25-158">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="d5d25-158">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="d5d25-159">�����������</span><span class="sxs-lookup"><span data-stu-id="d5d25-159">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="d5d25-160">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="d5d25-160">NOTIFKEY</span></span>](notifkey.md)
  
[<span data-ttu-id="d5d25-161">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d5d25-161">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

