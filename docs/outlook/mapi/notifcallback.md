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
# <a name="notifcallback"></a><span data-ttu-id="2cec9-103">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="2cec9-103">NOTIFCALLBACK</span></span>

  
  
<span data-ttu-id="2cec9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2cec9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2cec9-105">Определяет функцию callback, которую MAPI вызывает для отправки уведомления о событии.</span><span class="sxs-lookup"><span data-stu-id="2cec9-105">Defines a callback function that MAPI calls to send an event notification.</span></span> <span data-ttu-id="2cec9-106">Эту функцию вызова можно использовать только при оболочке в объекте-конвеере, созданном путем вызова функции [HrAllocAdviseSink.](hrallocadvisesink.md)</span><span class="sxs-lookup"><span data-stu-id="2cec9-106">This callback function can only be used when wrapped in an advise sink object created by calling the [HrAllocAdviseSink](hrallocadvisesink.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2cec9-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="2cec9-107">Header file:</span></span>  <br/> |<span data-ttu-id="2cec9-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2cec9-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2cec9-109">Определяемая функция, реализованная в:</span><span class="sxs-lookup"><span data-stu-id="2cec9-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="2cec9-110">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="2cec9-110">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="2cec9-111">Определяемая функция, вызванная:</span><span class="sxs-lookup"><span data-stu-id="2cec9-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="2cec9-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="2cec9-112">MAPI</span></span>  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="2cec9-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="2cec9-113">Parameters</span></span>

 <span data-ttu-id="2cec9-114">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="2cec9-114">_lpvContext_</span></span>
  
> <span data-ttu-id="2cec9-115">[in] Указатель на произвольное значение, передав его функции вызова при вызове MAPI.</span><span class="sxs-lookup"><span data-stu-id="2cec9-115">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="2cec9-116">Это значение может представлять адрес важности для клиентского приложения или поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="2cec9-116">This value can represent an address of significance to the client application or service provider.</span></span> <span data-ttu-id="2cec9-117">Обычно для кода C++ параметр  _lpvContext_ представляет указатель на объект C++.</span><span class="sxs-lookup"><span data-stu-id="2cec9-117">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="2cec9-118">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="2cec9-118">_cNotification_</span></span>
  
> <span data-ttu-id="2cec9-119">[in] Количество уведомлений о событиях в массиве, указанных параметром _lpNotifications._</span><span class="sxs-lookup"><span data-stu-id="2cec9-119">[in] Count of event notifications in the array indicated by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="2cec9-120">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="2cec9-120">_lpNotifications_</span></span>
  
> <span data-ttu-id="2cec9-121">[out] Указатель на расположение, где эта [](notification.md) функция записывает массив структур УВЕДОМЛЕНий, содержащий уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="2cec9-121">[out] Pointer to the location where this function writes an array of [NOTIFICATION](notification.md) structures that contains the event notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2cec9-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2cec9-122">Return value</span></span>

<span data-ttu-id="2cec9-123">Набор допустимых возвращаемых значений для прототипа функции **NOTIFCALLBACK** зависит от того, реализована ли функция клиентского приложения или поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="2cec9-123">The set of valid return values for the **NOTIFCALLBACK** function prototype depends on whether the function is implemented by a client application or a service provider.</span></span> <span data-ttu-id="2cec9-124">Клиенты должны всегда возвращать S_OK.</span><span class="sxs-lookup"><span data-stu-id="2cec9-124">Clients should always return S_OK.</span></span> <span data-ttu-id="2cec9-125">Поставщики могут возвращать S_OK или CALLBACK_DISCONTINUE.</span><span class="sxs-lookup"><span data-stu-id="2cec9-125">Providers can return either S_OK or CALLBACK_DISCONTINUE.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2cec9-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="2cec9-126">Remarks</span></span>

<span data-ttu-id="2cec9-127">CALLBACK_DISCONTINUE является допустимым возвращаемым значением только для синхронных функций обратного вызова; он запрашивает, чтобы MAPI немедленно остановил обработку вызовов для этого уведомления.</span><span class="sxs-lookup"><span data-stu-id="2cec9-127">CALLBACK_DISCONTINUE is a valid return value for synchronous callback functions only; it requests that MAPI immediately stop processing the callbacks for this notification.</span></span> <span data-ttu-id="2cec9-128">Когда CALLBACK_DISCONTINUE возвращается, MAPI задает для параметра  _lpUlFlags_ NOTIFY_CANCELED при возвращении из [IMAPISupport::Notify](imapisupport-notify.md).</span><span class="sxs-lookup"><span data-stu-id="2cec9-128">When CALLBACK_DISCONTINUE is returned, MAPI sets the  _lpUlFlags_ parameter to NOTIFY_CANCELED when it returns from [IMAPISupport::Notify](imapisupport-notify.md).</span></span> 
  
<span data-ttu-id="2cec9-129">Ниже действовать можно с ограничениями, которые может использовать функция синхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="2cec9-129">The following are limitations on what a synchronous callback function can do:</span></span>
  
- <span data-ttu-id="2cec9-130">Это не может привести к генерированию другого синхронного уведомления.</span><span class="sxs-lookup"><span data-stu-id="2cec9-130">It cannot cause another synchronous notification to be generated.</span></span>
    
- <span data-ttu-id="2cec9-131">Он не может отображать пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="2cec9-131">It cannot display a user interface.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2cec9-132">См. также</span><span class="sxs-lookup"><span data-stu-id="2cec9-132">See also</span></span>



[<span data-ttu-id="2cec9-133">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="2cec9-133">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)

