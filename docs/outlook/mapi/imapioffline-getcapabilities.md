---
title: имапиоффлинежеткапабилитиес
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
# <a name="imapiofflinegetcapabilities"></a><span data-ttu-id="b05f4-103">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="b05f4-103">IMAPIOffline::GetCapabilities</span></span>

  
  
<span data-ttu-id="b05f4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b05f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b05f4-105">Получает условия, для которых в автономном объекте поддерживаются обратные вызовы.</span><span class="sxs-lookup"><span data-stu-id="b05f4-105">Gets the conditions for which callbacks are supported by an offline object.</span></span>
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a><span data-ttu-id="b05f4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b05f4-106">Parameters</span></span>

 <span data-ttu-id="b05f4-107">_пулкапаблитиес_</span><span class="sxs-lookup"><span data-stu-id="b05f4-107">_pulCapablities_</span></span>
  
> <span data-ttu-id="b05f4-108">вышли Битовая маска следующих флагов возможностей:</span><span class="sxs-lookup"><span data-stu-id="b05f4-108">[out] A bitmask of the following capability flags:</span></span>
    
<span data-ttu-id="b05f4-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="b05f4-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>
  
> <span data-ttu-id="b05f4-110">Автономный объект способен предоставлять уведомления в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="b05f4-110">The offline object is capable of providing offline notifications.</span></span>
    
<span data-ttu-id="b05f4-111">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="b05f4-111">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>
  
> <span data-ttu-id="b05f4-112">Автономный объект способен предоставлять интерактивные уведомления.</span><span class="sxs-lookup"><span data-stu-id="b05f4-112">The offline object is capable of providing online notifications.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b05f4-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="b05f4-113">Remarks</span></span>

<span data-ttu-id="b05f4-114">При открытии автономного объекта с помощью **[хропеноффлинеобж](hropenofflineobj.md)** клиент может запросить [имапиоффлинемгр](imapiofflinemgrimapioffline.md) , чтобы получить указатель на интерфейс **имапиоффлине** , и вызвать **имапиоффлине::** GetObject, чтобы узнать, какие обратные вызовы поддерживаются объектом.</span><span class="sxs-lookup"><span data-stu-id="b05f4-114">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client can query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) to obtain a pointer to an **IMAPIOffline** interface, and call **IMAPIOffline::GetCapabilities** to find out the callbacks supported by the object.</span></span> <span data-ttu-id="b05f4-115">После этого клиент может выбрать настройку обратных вызовов с помощью **имапиоффлинемгр**.</span><span class="sxs-lookup"><span data-stu-id="b05f4-115">The client can then choose to set up callbacks by using **IMAPIOfflineMgr**.</span></span>
  
<span data-ttu-id="b05f4-116">Обратите внимание, что в зависимости от почтового сервера для автономного объекта объект, который поддерживает обратные вызовы для подключения к сети, не обязательно поддерживает обратные вызовы при переходе в автономный режим.</span><span class="sxs-lookup"><span data-stu-id="b05f4-116">Note that, depending on the mail server for an offline object, an object that supports callbacks for going online does not necessarily support callbacks for going offline.</span></span>
  
<span data-ttu-id="b05f4-117">Обратите внимание, что в то время как автономный объект может поддерживать обратные вызовы для изменений, отличных от Online и offline, API автономного состояния поддерживает только изменения в сети и вне сети, а клиенты должны проверять только такие возможности.</span><span class="sxs-lookup"><span data-stu-id="b05f4-117">Also note that, while an offline object may support callbacks for changes other than online/offline, the Offline State API supports only online/offline changes, and clients must check for only such capabilities.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b05f4-118">См. также</span><span class="sxs-lookup"><span data-stu-id="b05f4-118">See also</span></span>



[<span data-ttu-id="b05f4-119">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="b05f4-119">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)
  
[<span data-ttu-id="b05f4-120">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="b05f4-120">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)
  
[<span data-ttu-id="b05f4-121">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="b05f4-121">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="b05f4-122">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="b05f4-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="b05f4-123">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="b05f4-123">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

