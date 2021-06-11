---
title: NOTIFCALLBACK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFCALLBACK
api_type:
- COM
ms.assetid: 416008b4-13aa-4387-8c12-f8f2ca252391
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0e2a1a582894e082722d73422fc8bafe34c4230c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434020"
---
# <a name="notifcallback"></a><span data-ttu-id="26b2e-103">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="26b2e-103">NOTIFCALLBACK</span></span>

  
  
<span data-ttu-id="26b2e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26b2e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26b2e-105">Определяет функцию вызова, вызываемую MAPI для отправки уведомления о событии.</span><span class="sxs-lookup"><span data-stu-id="26b2e-105">Defines a callback function that MAPI calls to send an event notification.</span></span> <span data-ttu-id="26b2e-106">Эту функцию вызова можно использовать только при завернутой в объект раковины рекомендации, созданный путем вызова [функции HrAllocAdviseSink.](hrallocadvisesink.md)</span><span class="sxs-lookup"><span data-stu-id="26b2e-106">This callback function can only be used when wrapped in an advise sink object created by calling the [HrAllocAdviseSink](hrallocadvisesink.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="26b2e-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="26b2e-107">Header file:</span></span>  <br/> |<span data-ttu-id="26b2e-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="26b2e-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="26b2e-109">Определенные функции, реализованные в:</span><span class="sxs-lookup"><span data-stu-id="26b2e-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="26b2e-110">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="26b2e-110">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="26b2e-111">Определенная функция, вызванная:</span><span class="sxs-lookup"><span data-stu-id="26b2e-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="26b2e-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="26b2e-112">MAPI</span></span>  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="26b2e-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="26b2e-113">Parameters</span></span>

 <span data-ttu-id="26b2e-114">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="26b2e-114">_lpvContext_</span></span>
  
> <span data-ttu-id="26b2e-115">[in] Указатель на произвольное значение, переданного функции вызова при вызове MAPI.</span><span class="sxs-lookup"><span data-stu-id="26b2e-115">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="26b2e-116">Это значение может представлять адрес, который имеет значение для клиентского приложения или поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="26b2e-116">This value can represent an address of significance to the client application or service provider.</span></span> <span data-ttu-id="26b2e-117">Как правило, для кода C++ параметр  _lpvContext_ представляет указатель на объект C++.</span><span class="sxs-lookup"><span data-stu-id="26b2e-117">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="26b2e-118">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="26b2e-118">_cNotification_</span></span>
  
> <span data-ttu-id="26b2e-119">[in] Количество уведомлений о событиях в массиве, указанных параметром _lpNotifications._</span><span class="sxs-lookup"><span data-stu-id="26b2e-119">[in] Count of event notifications in the array indicated by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="26b2e-120">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="26b2e-120">_lpNotifications_</span></span>
  
> <span data-ttu-id="26b2e-121">[вышел] Указатель на расположение, в котором [](notification.md) эта функция записывает массив структур УВЕДОМЛЕНий, содержащий уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="26b2e-121">[out] Pointer to the location where this function writes an array of [NOTIFICATION](notification.md) structures that contains the event notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="26b2e-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="26b2e-122">Return value</span></span>

<span data-ttu-id="26b2e-123">Набор допустимых значений возврата для прототипа **функции NOTIFCALLBACK** зависит от того, реализуется ли эта функция клиентом или поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="26b2e-123">The set of valid return values for the **NOTIFCALLBACK** function prototype depends on whether the function is implemented by a client application or a service provider.</span></span> <span data-ttu-id="26b2e-124">Клиенты всегда должны возвращать S_OK.</span><span class="sxs-lookup"><span data-stu-id="26b2e-124">Clients should always return S_OK.</span></span> <span data-ttu-id="26b2e-125">Поставщики могут возвращать S_OK или CALLBACK_DISCONTINUE.</span><span class="sxs-lookup"><span data-stu-id="26b2e-125">Providers can return either S_OK or CALLBACK_DISCONTINUE.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="26b2e-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="26b2e-126">Remarks</span></span>

<span data-ttu-id="26b2e-127">CALLBACK_DISCONTINUE является допустимым возвратным значением только для синхронных функций обратного вызова; он запрашивает, чтобы MAPI немедленно прекратила обработку отозвок для этого уведомления.</span><span class="sxs-lookup"><span data-stu-id="26b2e-127">CALLBACK_DISCONTINUE is a valid return value for synchronous callback functions only; it requests that MAPI immediately stop processing the callbacks for this notification.</span></span> <span data-ttu-id="26b2e-128">Когда CALLBACK_DISCONTINUE возвращается, MAPI задает параметр  _lpUlFlags_ NOTIFY_CANCELED при возвращении из [IMAPISupport:::Notify](imapisupport-notify.md).</span><span class="sxs-lookup"><span data-stu-id="26b2e-128">When CALLBACK_DISCONTINUE is returned, MAPI sets the  _lpUlFlags_ parameter to NOTIFY_CANCELED when it returns from [IMAPISupport::Notify](imapisupport-notify.md).</span></span> 
  
<span data-ttu-id="26b2e-129">Ниже 11. Ограничения, которые может сделать синхронная функция вызова:</span><span class="sxs-lookup"><span data-stu-id="26b2e-129">The following are limitations on what a synchronous callback function can do:</span></span>
  
- <span data-ttu-id="26b2e-130">Это не может привести к сгенерированию другого синхронного уведомления.</span><span class="sxs-lookup"><span data-stu-id="26b2e-130">It cannot cause another synchronous notification to be generated.</span></span>
    
- <span data-ttu-id="26b2e-131">Он не может отображать пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="26b2e-131">It cannot display a user interface.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="26b2e-132">См. также</span><span class="sxs-lookup"><span data-stu-id="26b2e-132">See also</span></span>



[<span data-ttu-id="26b2e-133">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="26b2e-133">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)

