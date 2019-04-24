---
title: Имаписуппортсубскрибе
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328968"
---
# <a name="imapisupportsubscribe"></a><span data-ttu-id="a7bdd-103">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="a7bdd-103">IMAPISupport::Subscribe</span></span>

  
  
<span data-ttu-id="a7bdd-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7bdd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7bdd-105">Регистрирует приемник уведомлений для получения уведомлений через MAPI.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-105">Registers an advise sink to receive notifications through MAPI.</span></span>
  
```cpp
HRESULT Subscribe(
LPNOTIFKEY lpKey,
ULONG ulEventMask,
ULONG ulFlags,
LPMAPIADVISESINK lpAdviseSink,
ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="a7bdd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7bdd-106">Parameters</span></span>

 <span data-ttu-id="a7bdd-107">_Лпкэй_</span><span class="sxs-lookup"><span data-stu-id="a7bdd-107">_lpKey_</span></span>
  
> <span data-ttu-id="a7bdd-108">возврата Указатель на ключ уведомления, представляющий исходный объект Advise.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-108">[in] A pointer to a notification key that represents the advise source object.</span></span> <span data-ttu-id="a7bdd-109">Параметр _лпкэй_ не может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="a7bdd-110">_Улевентмаск_</span><span class="sxs-lookup"><span data-stu-id="a7bdd-110">_ulEventMask_</span></span>
  
> <span data-ttu-id="a7bdd-111">возврата Маска значений, указывающая типы событий уведомлений, в которых заинтересован вызывающий абонент, которые необходимо включить в регистрацию.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-111">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="a7bdd-112">Допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a7bdd-112">The following values are valid:</span></span>
    
 <span data-ttu-id="a7bdd-113">_Фневкритикалеррор_</span><span class="sxs-lookup"><span data-stu-id="a7bdd-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="a7bdd-114">Регистрирует уведомления о серьезных ошибках, таких как недостаток памяти.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-114">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="a7bdd-115">_Фневекстендед_</span><span class="sxs-lookup"><span data-stu-id="a7bdd-115">_fnevExtended_</span></span>
  
> <span data-ttu-id="a7bdd-116">Регистрирует уведомления о событиях, относящихся к определенной адресной книге или поставщику хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-116">Registers for notifications about events specific to the particular address book or message store provider.</span></span>
    
 <span data-ttu-id="a7bdd-117">_Фневневмаил_</span><span class="sxs-lookup"><span data-stu-id="a7bdd-117">_fnevNewMail_</span></span>
  
> <span data-ttu-id="a7bdd-118">Регистрирует уведомления о поступлении новых сообщений.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-118">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="a7bdd-119">_Фневобжекткреатед_</span><span class="sxs-lookup"><span data-stu-id="a7bdd-119">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="a7bdd-120">Регистрирует уведомления о создании нового объекта.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-120">Registers for notifications about the creation of a new object.</span></span>
    
 <span data-ttu-id="a7bdd-121">_Фневобжекткопиед_</span><span class="sxs-lookup"><span data-stu-id="a7bdd-121">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="a7bdd-122">Регистрирует уведомления о копируемом объекте.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-122">Registers for notifications about an object being copied.</span></span>
    
 <span data-ttu-id="a7bdd-123">_Фневобжектделетед_</span><span class="sxs-lookup"><span data-stu-id="a7bdd-123">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="a7bdd-124">Регистрирует уведомления об удалении объекта.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-124">Registers for notifications about an object being deleted.</span></span>
    
 <span data-ttu-id="a7bdd-125">_Фневобжектмодифиед_</span><span class="sxs-lookup"><span data-stu-id="a7bdd-125">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="a7bdd-126">Регистрирует уведомления об изменяемом объекте.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-126">Registers for notifications about an object being modified.</span></span>
    
 <span data-ttu-id="a7bdd-127">_Фневобжектмовед_</span><span class="sxs-lookup"><span data-stu-id="a7bdd-127">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="a7bdd-128">Регистрирует уведомления об перемещении объекта.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-128">Registers for notifications about an object being moved.</span></span>
    
 <span data-ttu-id="a7bdd-129">_Фневсеарчкомплете_</span><span class="sxs-lookup"><span data-stu-id="a7bdd-129">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="a7bdd-130">Регистрирует уведомления о завершении операции поиска.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-130">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="a7bdd-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a7bdd-131">_ulFlags_</span></span>
  
> <span data-ttu-id="a7bdd-132">возврата Битовая маска флагов, определяющих, как происходит уведомление.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-132">[in] A bitmask of flags that controls how notification occurs.</span></span> <span data-ttu-id="a7bdd-133">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="a7bdd-133">The following flag can be set:</span></span>
    
<span data-ttu-id="a7bdd-134">НОТИФИ_СИНК</span><span class="sxs-lookup"><span data-stu-id="a7bdd-134">NOTIFY_SYNC</span></span> 
  
> <span data-ttu-id="a7bdd-135">Когда вызывающий абонент вызывает метод [имаписуппорт:: notify](imapisupport-notify.md) для создания уведомлений для этого приемника уведомлений \*\*\*\* , при уведомлении необходимо выполнить все необходимые вызовы для уведомлений о приемниках перед возвратом.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-135">When the caller calls the [IMAPISupport::Notify](imapisupport-notify.md) method to generate notifications for this advise sink, **Notify** should make all necessary calls to advise sinks before returning.</span></span> <span data-ttu-id="a7bdd-136">Если этот флаг не установлен, то уведомление будет асинхронным и обратными вызовами помещаются в очередь для процессов, которые подписаны и запущены, когда эти процессы получают контроль над ЦП.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-136">If this flag is not set, notification is asynchronous and callbacks are queued to the processes that have subscribed and started when those processes gain control of the CPU.</span></span> 
    
 <span data-ttu-id="a7bdd-137">_Лпадвисесинк_</span><span class="sxs-lookup"><span data-stu-id="a7bdd-137">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="a7bdd-138">возврата Указатель на объект приемника уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-138">[in] A pointer to an advise sink object.</span></span> 
    
 <span data-ttu-id="a7bdd-139">_Лпулконнектион_</span><span class="sxs-lookup"><span data-stu-id="a7bdd-139">_lpulConnection_</span></span>
  
> <span data-ttu-id="a7bdd-140">вышли Указатель на ненулевый номер подключения, представляющий регистрацию.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-140">[out] A pointer to a nonzero connection number that represents the registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a7bdd-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a7bdd-141">Return value</span></span>

<span data-ttu-id="a7bdd-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="a7bdd-142">S_OK</span></span> 
  
> <span data-ttu-id="a7bdd-143">Успешная регистрация уведомления.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-143">The notification registration was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a7bdd-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a7bdd-144">Remarks</span></span>

<span data-ttu-id="a7bdd-145">Метод **имаписуппорт:: Subscribe** реализован для всех объектов поддержки поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-145">The **IMAPISupport::Subscribe** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="a7bdd-146">Поставщики услуг выполняют **подписку** на один из методов **advise** , чтобы разрешить MAPI управлять уведомлениями.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-146">Service providers call **Subscribe** from one of their **Advise** methods to allow MAPI to manage the notifications.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a7bdd-147">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="a7bdd-147">Notes to callers</span></span>

<span data-ttu-id="a7bdd-148">Чтобы использовать методы поддержки MAPI для уведомлений, создайте ключ для источника рекомендаций объект, для которого необходимо создать уведомления.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-148">To use the MAPI support methods for notification, create a key for the advise source the object about which notifications should be generated.</span></span> <span data-ttu-id="a7bdd-149">Значение ключа должно быть уникальным и должно быть легко воссоздано при каждом изменении объекта.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-149">The value of the key must be unique and should be easily regenerated each time the object changes.</span></span> 
  
<span data-ttu-id="a7bdd-150">MAPI использует ключ уведомления для поиска всех функций обратного вызова, зарегистрированных с помощью функции [храллокадвисесинк](hrallocadvisesink.md) , для соответствующего источника уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-150">MAPI uses the notification key to search for any callback functions registered through the [HrAllocAdviseSink](hrallocadvisesink.md) function for the corresponding advise source.</span></span> <span data-ttu-id="a7bdd-151">Передайте этот ключ в **имаписуппорт:: уведомлять** каждый раз, когда необходимо создать уведомление для соответствующего источника уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-151">Pass this key to **IMAPISupport::Notify** whenever you need to generate a notification for the corresponding advise source.</span></span> 
  
<span data-ttu-id="a7bdd-152">Флаг НОТИФИ_СИНК влияет на работу последующих вызовов для **уведомления**.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-152">The NOTIFY_SYNC flag affects the operation of subsequent calls to **Notify**.</span></span> <span data-ttu-id="a7bdd-153">При установке НОТИФИ_СИНК **уведомление** не возвращается, пока не закончится отправка всех необходимых уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-153">When you set NOTIFY_SYNC, **Notify** does not return until it has finished sending all of the necessary notifications.</span></span> <span data-ttu-id="a7bdd-154">Если вы не настраиваете НОТИФИ_СИНК, то **Notify** работает асинхронно, возможно, после того, как все уведомления будут отправлены.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-154">When you do not set NOTIFY_SYNC, **Notify** operates asynchronously, possibly returning before all of the notifications have been sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a7bdd-155">См. также</span><span class="sxs-lookup"><span data-stu-id="a7bdd-155">See also</span></span>



[<span data-ttu-id="a7bdd-156">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="a7bdd-156">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="a7bdd-157">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="a7bdd-157">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="a7bdd-158">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="a7bdd-158">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="a7bdd-159">�����������</span><span class="sxs-lookup"><span data-stu-id="a7bdd-159">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="a7bdd-160">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="a7bdd-160">NOTIFKEY</span></span>](notifkey.md)
  
[<span data-ttu-id="a7bdd-161">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a7bdd-161">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

