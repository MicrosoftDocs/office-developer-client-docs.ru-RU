---
title: IMAPIOfflineGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.GetCapabilities
api_type:
- COM
ms.assetid: aa8dc48b-9e1c-8da0-9579-10b7174e99de
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 48d59d17d81da2ae78348a57ad8b1cb75486b1a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433376"
---
# <a name="imapiofflinegetcapabilities"></a><span data-ttu-id="a5d17-103">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="a5d17-103">IMAPIOffline::GetCapabilities</span></span>

  
  
<span data-ttu-id="a5d17-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5d17-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5d17-105">Получает условия, для которых автономный объект поддерживает вызовы.</span><span class="sxs-lookup"><span data-stu-id="a5d17-105">Gets the conditions for which callbacks are supported by an offline object.</span></span>
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a><span data-ttu-id="a5d17-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5d17-106">Parameters</span></span>

 <span data-ttu-id="a5d17-107">_pulCapablities_</span><span class="sxs-lookup"><span data-stu-id="a5d17-107">_pulCapablities_</span></span>
  
> <span data-ttu-id="a5d17-108">[out] Битоваяmas следующих флагов возможностей:</span><span class="sxs-lookup"><span data-stu-id="a5d17-108">[out] A bitmask of the following capability flags:</span></span>
    
<span data-ttu-id="a5d17-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="a5d17-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>
  
> <span data-ttu-id="a5d17-110">Автономный объект может предоставлять автономные уведомления.</span><span class="sxs-lookup"><span data-stu-id="a5d17-110">The offline object is capable of providing offline notifications.</span></span>
    
<span data-ttu-id="a5d17-111">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="a5d17-111">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>
  
> <span data-ttu-id="a5d17-112">Автономный объект может предоставлять интерактивные уведомления.</span><span class="sxs-lookup"><span data-stu-id="a5d17-112">The offline object is capable of providing online notifications.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a5d17-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="a5d17-113">Remarks</span></span>

<span data-ttu-id="a5d17-114">Открыв автономный объект с помощью **[HrOpenOfflineObj,](hropenofflineobj.md)** клиент может запросить у [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) указатель на интерфейс **IMAPIOffline** и вызвать **IMAPIOffline::GetCapabilities,** чтобы узнать, поддерживаются ли объектом вызовы.</span><span class="sxs-lookup"><span data-stu-id="a5d17-114">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client can query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) to obtain a pointer to an **IMAPIOffline** interface, and call **IMAPIOffline::GetCapabilities** to find out the callbacks supported by the object.</span></span> <span data-ttu-id="a5d17-115">Затем клиент может настроить вызовы с помощью **IMAPIOfflineMgr.**</span><span class="sxs-lookup"><span data-stu-id="a5d17-115">The client can then choose to set up callbacks by using **IMAPIOfflineMgr**.</span></span>
  
<span data-ttu-id="a5d17-116">Обратите внимание, что в зависимости от почтового сервера для автономного объекта объект, поддерживаюющий вызовы для работы в сети, не обязательно поддерживает вызовы для работы в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="a5d17-116">Note that, depending on the mail server for an offline object, an object that supports callbacks for going online does not necessarily support callbacks for going offline.</span></span>
  
<span data-ttu-id="a5d17-117">Кроме того, обратите внимание, что, хотя автономный объект может поддерживать функции вызова для изменений, кроме сетевых или автономных, API автономного состояния поддерживает только изменения в сети или автономном режиме, и клиенты должны проверять только такие возможности.</span><span class="sxs-lookup"><span data-stu-id="a5d17-117">Also note that, while an offline object may support callbacks for changes other than online/offline, the Offline State API supports only online/offline changes, and clients must check for only such capabilities.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a5d17-118">См. также</span><span class="sxs-lookup"><span data-stu-id="a5d17-118">See also</span></span>



[<span data-ttu-id="a5d17-119">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="a5d17-119">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)
  
[<span data-ttu-id="a5d17-120">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="a5d17-120">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)
  
[<span data-ttu-id="a5d17-121">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="a5d17-121">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="a5d17-122">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="a5d17-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="a5d17-123">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="a5d17-123">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

