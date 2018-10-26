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
ms.openlocfilehash: 699e77479e0d09e7549c0d2741d5ba54ecc8ce33
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572034"
---
# <a name="imapiofflinegetcapabilities"></a><span data-ttu-id="591d7-103">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="591d7-103">IMAPIOffline::GetCapabilities</span></span>

  
  
<span data-ttu-id="591d7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="591d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="591d7-105">Получает условия, для которых обратные вызовы поддерживаются автономной объектом.</span><span class="sxs-lookup"><span data-stu-id="591d7-105">Gets the conditions for which callbacks are supported by an offline object.</span></span>
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a><span data-ttu-id="591d7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="591d7-106">Parameters</span></span>

 <span data-ttu-id="591d7-107">_pulCapablities_</span><span class="sxs-lookup"><span data-stu-id="591d7-107">_pulCapablities_</span></span>
  
> <span data-ttu-id="591d7-108">[out] Битовая маска флагов следующих возможностей:</span><span class="sxs-lookup"><span data-stu-id="591d7-108">[out] A bitmask of the following capability flags:</span></span>
    
<span data-ttu-id="591d7-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="591d7-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>
  
> <span data-ttu-id="591d7-110">Автономные объект может предоставить автономной уведомлений.</span><span class="sxs-lookup"><span data-stu-id="591d7-110">The offline object is capable of providing offline notifications.</span></span>
    
<span data-ttu-id="591d7-111">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="591d7-111">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>
  
> <span data-ttu-id="591d7-112">Автономные объект может предоставить online уведомлений.</span><span class="sxs-lookup"><span data-stu-id="591d7-112">The offline object is capable of providing online notifications.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="591d7-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="591d7-113">Remarks</span></span>

<span data-ttu-id="591d7-114">При открытии автономного объекта с помощью **[HrOpenOfflineObj](hropenofflineobj.md)** клиента можно запросить на [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) , чтобы получить указатель на интерфейс **IMAPIOffline** и вызовите **IMAPIOffline::GetCapabilities** , чтобы узнать, поддерживается обратные вызовы с помощью объекта.</span><span class="sxs-lookup"><span data-stu-id="591d7-114">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client can query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) to obtain a pointer to an **IMAPIOffline** interface, and call **IMAPIOffline::GetCapabilities** to find out the callbacks supported by the object.</span></span> <span data-ttu-id="591d7-115">Клиент затем можно настроить обратных вызовов с помощью **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="591d7-115">The client can then choose to set up callbacks by using **IMAPIOfflineMgr**.</span></span>
  
<span data-ttu-id="591d7-116">Обратите внимание, что в зависимости от почтового сервера для автономного объекта, объект, который поддерживает обратных вызовов для подключение не поддерживает обязательно обратных вызовов для перейти в автономный режим.</span><span class="sxs-lookup"><span data-stu-id="591d7-116">Note that, depending on the mail server for an offline object, an object that supports callbacks for going online does not necessarily support callbacks for going offline.</span></span>
  
<span data-ttu-id="591d7-117">Также Обратите внимание, что при автономной объекта могут поддерживать обратных вызовов для изменения, отличный от онлайновом/интерактивном режиме, автономного состояния API поддерживает только онлайновом/интерактивном режиме изменения и клиенты должен проверять наличие только такие возможности.</span><span class="sxs-lookup"><span data-stu-id="591d7-117">Also note that, while an offline object may support callbacks for changes other than online/offline, the Offline State API supports only online/offline changes, and clients must check for only such capabilities.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="591d7-118">См. также</span><span class="sxs-lookup"><span data-stu-id="591d7-118">See also</span></span>



[<span data-ttu-id="591d7-119">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="591d7-119">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)
  
[<span data-ttu-id="591d7-120">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="591d7-120">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)
  
[<span data-ttu-id="591d7-121">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="591d7-121">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="591d7-122">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="591d7-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="591d7-123">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="591d7-123">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

