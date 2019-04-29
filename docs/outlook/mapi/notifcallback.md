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
# <a name="notifcallback"></a><span data-ttu-id="d9528-103">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="d9528-103">NOTIFCALLBACK</span></span>

  
  
<span data-ttu-id="d9528-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9528-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9528-105">Определяет функцию обратного вызова, которая вызывает MAPI для отправки уведомления о событии.</span><span class="sxs-lookup"><span data-stu-id="d9528-105">Defines a callback function that MAPI calls to send an event notification.</span></span> <span data-ttu-id="d9528-106">Эту функцию обратного вызова можно использовать только при заключении в оболочку объекта приемника уведомлений, созданного при вызове функции [храллокадвисесинк](hrallocadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="d9528-106">This callback function can only be used when wrapped in an advise sink object created by calling the [HrAllocAdviseSink](hrallocadvisesink.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d9528-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d9528-107">Header file:</span></span>  <br/> |<span data-ttu-id="d9528-108">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="d9528-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d9528-109">Определенная функция реализована следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d9528-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="d9528-110">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="d9528-110">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="d9528-111">Определенная функция, вызываемая:</span><span class="sxs-lookup"><span data-stu-id="d9528-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="d9528-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="d9528-112">MAPI</span></span>  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="d9528-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9528-113">Parameters</span></span>

 <span data-ttu-id="d9528-114">_Лпвконтекст_</span><span class="sxs-lookup"><span data-stu-id="d9528-114">_lpvContext_</span></span>
  
> <span data-ttu-id="d9528-115">возврата Указатель на произвольное значение, переданное функции обратного вызова при ее вызове MAPI.</span><span class="sxs-lookup"><span data-stu-id="d9528-115">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="d9528-116">Это значение может представлять собой адрес важности для клиентского приложения или поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="d9528-116">This value can represent an address of significance to the client application or service provider.</span></span> <span data-ttu-id="d9528-117">Как правило, для кода C++ параметр _лпвконтекст_ представляет указатель на объект C++.</span><span class="sxs-lookup"><span data-stu-id="d9528-117">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="d9528-118">_Кнотификатион_</span><span class="sxs-lookup"><span data-stu-id="d9528-118">_cNotification_</span></span>
  
> <span data-ttu-id="d9528-119">возврата Количество уведомлений о событиях в массиве, указанном параметром _лпнотификатионс_ .</span><span class="sxs-lookup"><span data-stu-id="d9528-119">[in] Count of event notifications in the array indicated by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="d9528-120">_Лпнотификатионс_</span><span class="sxs-lookup"><span data-stu-id="d9528-120">_lpNotifications_</span></span>
  
> <span data-ttu-id="d9528-121">вышли Указатель на расположение, в котором эта функция записывает массив структуры [уведомлений](notification.md) , содержащий уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="d9528-121">[out] Pointer to the location where this function writes an array of [NOTIFICATION](notification.md) structures that contains the event notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d9528-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9528-122">Return value</span></span>

<span data-ttu-id="d9528-123">Набор допустимых возвращаемых значений для прототипа функции **нотифкаллбакк** зависит от того, реализована ли функция в клиентском приложении или поставщике услуг.</span><span class="sxs-lookup"><span data-stu-id="d9528-123">The set of valid return values for the **NOTIFCALLBACK** function prototype depends on whether the function is implemented by a client application or a service provider.</span></span> <span data-ttu-id="d9528-124">Клиенты всегда должны возвращать значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="d9528-124">Clients should always return S_OK.</span></span> <span data-ttu-id="d9528-125">Поставщики могут возвращать значение S_OK или КАЛЛБАКК_ДИСКОНТИНУЕ.</span><span class="sxs-lookup"><span data-stu-id="d9528-125">Providers can return either S_OK or CALLBACK_DISCONTINUE.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d9528-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="d9528-126">Remarks</span></span>

<span data-ttu-id="d9528-127">КАЛЛБАКК_ДИСКОНТИНУЕ — допустимое возвращаемое значение только для синхронных функций обратного вызова; Он немедленно перестает обрабатывать обратные вызовы для этого уведомления.</span><span class="sxs-lookup"><span data-stu-id="d9528-127">CALLBACK_DISCONTINUE is a valid return value for synchronous callback functions only; it requests that MAPI immediately stop processing the callbacks for this notification.</span></span> <span data-ttu-id="d9528-128">Когда возвращается КАЛЛБАКК_ДИСКОНТИНУЕ, MAPI задает для параметра _лпулфлагс_ значение нотифи_канцелед, когда он возвращается из [Имаписуппорт:: notify](imapisupport-notify.md).</span><span class="sxs-lookup"><span data-stu-id="d9528-128">When CALLBACK_DISCONTINUE is returned, MAPI sets the  _lpUlFlags_ parameter to NOTIFY_CANCELED when it returns from [IMAPISupport::Notify](imapisupport-notify.md).</span></span> 
  
<span data-ttu-id="d9528-129">Ниже приведены ограничения, которые могут выполнять синхронные функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="d9528-129">The following are limitations on what a synchronous callback function can do:</span></span>
  
- <span data-ttu-id="d9528-130">Это не может привести к созданию другого синхронного уведомления.</span><span class="sxs-lookup"><span data-stu-id="d9528-130">It cannot cause another synchronous notification to be generated.</span></span>
    
- <span data-ttu-id="d9528-131">Невозможно отобразить пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="d9528-131">It cannot display a user interface.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d9528-132">См. также</span><span class="sxs-lookup"><span data-stu-id="d9528-132">See also</span></span>



[<span data-ttu-id="d9528-133">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="d9528-133">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)

