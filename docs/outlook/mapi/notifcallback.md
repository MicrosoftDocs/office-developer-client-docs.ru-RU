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
ms.openlocfilehash: 17b038fea2dd1614f94f005e32b9e6ba4423dbda
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566266"
---
# <a name="notifcallback"></a><span data-ttu-id="fe15f-103">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="fe15f-103">NOTIFCALLBACK</span></span>

  
  
<span data-ttu-id="fe15f-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe15f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe15f-105">Определяет функцию обратного вызова, которая вызывает MAPI для отправки уведомления о событии.</span><span class="sxs-lookup"><span data-stu-id="fe15f-105">Defines a callback function that MAPI calls to send an event notification.</span></span> <span data-ttu-id="fe15f-106">Эта функция обратного вызова используется только в том случае, если в объект приемника уведомлений, созданный с помощью вызова функции [HrAllocAdviseSink](hrallocadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="fe15f-106">This callback function can only be used when wrapped in an advise sink object created by calling the [HrAllocAdviseSink](hrallocadvisesink.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fe15f-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="fe15f-107">Header file:</span></span>  <br/> |<span data-ttu-id="fe15f-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fe15f-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="fe15f-109">Функция реализован:</span><span class="sxs-lookup"><span data-stu-id="fe15f-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="fe15f-110">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="fe15f-110">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="fe15f-111">Вызывается функция:</span><span class="sxs-lookup"><span data-stu-id="fe15f-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="fe15f-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="fe15f-112">MAPI</span></span>  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="fe15f-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe15f-113">Parameters</span></span>

 <span data-ttu-id="fe15f-114">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="fe15f-114">_lpvContext_</span></span>
  
> <span data-ttu-id="fe15f-115">[in] Указатель произвольных значение передается функции обратного вызова, когда она вызывается средствами MAPI.</span><span class="sxs-lookup"><span data-stu-id="fe15f-115">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="fe15f-116">Это значение может представлять адрес важности для клиентского приложения или поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="fe15f-116">This value can represent an address of significance to the client application or service provider.</span></span> <span data-ttu-id="fe15f-117">Обычно для кода C++ параметр _lpvContext_ представляет указатель на объект C++.</span><span class="sxs-lookup"><span data-stu-id="fe15f-117">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="fe15f-118">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="fe15f-118">_cNotification_</span></span>
  
> <span data-ttu-id="fe15f-119">[in] Количество уведомлений о событиях в массива, указанного в параметре _lpNotifications_ .</span><span class="sxs-lookup"><span data-stu-id="fe15f-119">[in] Count of event notifications in the array indicated by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="fe15f-120">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="fe15f-120">_lpNotifications_</span></span>
  
> <span data-ttu-id="fe15f-121">[out] Указатель на место, где эта функция записывает массив структур [УВЕДОМЛЕНИЙ](notification.md) , который содержит уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="fe15f-121">[out] Pointer to the location where this function writes an array of [NOTIFICATION](notification.md) structures that contains the event notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fe15f-122">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="fe15f-122">Return value</span></span>

<span data-ttu-id="fe15f-123">Набор допустимый возвращаемые значения для прототипа функции **NOTIFCALLBACK** зависит от ли реализовать функцию клиентского приложения или поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="fe15f-123">The set of valid return values for the **NOTIFCALLBACK** function prototype depends on whether the function is implemented by a client application or a service provider.</span></span> <span data-ttu-id="fe15f-124">Клиенты должны всегда возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="fe15f-124">Clients should always return S_OK.</span></span> <span data-ttu-id="fe15f-125">Поставщики могут возвращать значение S_OK или CALLBACK_DISCONTINUE.</span><span class="sxs-lookup"><span data-stu-id="fe15f-125">Providers can return either S_OK or CALLBACK_DISCONTINUE.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fe15f-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="fe15f-126">Remarks</span></span>

<span data-ttu-id="fe15f-127">CALLBACK_DISCONTINUE является допустимым возвращаемое значение для функции синхронные обратного вызова. он запрашивает, что MAPI немедленной остановки обработки обратных вызовов для этого уведомления.</span><span class="sxs-lookup"><span data-stu-id="fe15f-127">CALLBACK_DISCONTINUE is a valid return value for synchronous callback functions only; it requests that MAPI immediately stop processing the callbacks for this notification.</span></span> <span data-ttu-id="fe15f-128">При возвращении CALLBACK_DISCONTINUE MAPI задается параметр _lpUlFlags_ NOTIFY_CANCELED при возврате из [IMAPISupport::Notify](imapisupport-notify.md).</span><span class="sxs-lookup"><span data-stu-id="fe15f-128">When CALLBACK_DISCONTINUE is returned, MAPI sets the  _lpUlFlags_ parameter to NOTIFY_CANCELED when it returns from [IMAPISupport::Notify](imapisupport-notify.md).</span></span> 
  
<span data-ttu-id="fe15f-129">Ниже приведены ограничения на функцию обратного вызова синхронного действия.</span><span class="sxs-lookup"><span data-stu-id="fe15f-129">The following are limitations on what a synchronous callback function can do:</span></span>
  
- <span data-ttu-id="fe15f-130">Он не может вызывать другой синхронного уведомления был создан.</span><span class="sxs-lookup"><span data-stu-id="fe15f-130">It cannot cause another synchronous notification to be generated.</span></span>
    
- <span data-ttu-id="fe15f-131">Не может отображать пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="fe15f-131">It cannot display a user interface.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fe15f-132">См. также</span><span class="sxs-lookup"><span data-stu-id="fe15f-132">See also</span></span>



[<span data-ttu-id="fe15f-133">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="fe15f-133">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)

