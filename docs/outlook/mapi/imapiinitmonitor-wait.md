---
title: imapiinitmonitor-wait
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIINITMONITOR.Wait
api_type:
- COM
ms.assetid: ed566cae-35a2-4716-817b-54d1ba6825c6
description: IMAPIAMonitor::Wait
Last modified: April 26, 2021
ms.openlocfilehash: ee46a2744e67804c9dfdac8d7512db1d7b07f8ba
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062013"
---
# <a name="imapiinitmonitorwait"></a><span data-ttu-id="72f09-103">IMAPIInitMonitor::Wait</span><span class="sxs-lookup"><span data-stu-id="72f09-103">IMAPIInitMonitor::Wait</span></span>
  
<span data-ttu-id="72f09-104">**Применяется к**: Outlook 2013 | Outlook 2016 | 2019</span><span class="sxs-lookup"><span data-stu-id="72f09-104">**Applies to**: Outlook 2013 | Outlook 2016 | 2019</span></span>
  
<span data-ttu-id="72f09-105">Инициирует вызов BLOCKING в этом потоке, который возвращается либо после инициализации указанного числа миллисекунд, либо при инициализации MAPI.</span><span class="sxs-lookup"><span data-stu-id="72f09-105">Initiates a BLOCKING call on this thread, which will return either when the specified number of milliseconds have elapsed or MAPI has been initialized.</span></span> <span data-ttu-id="72f09-106">INFINITE можно использовать для бесконечного ожидания.</span><span class="sxs-lookup"><span data-stu-id="72f09-106">INFINITE can be used to for an infinite wait.</span></span>

```cpp
HRESULT IMAPIInitMonitor::Wait(DWORD timeout)
```

## <a name="parameters"></a><span data-ttu-id="72f09-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="72f09-107">Parameters</span></span>
<span data-ttu-id="72f09-108">_timeout_</span><span class="sxs-lookup"><span data-stu-id="72f09-108">_timeout_</span></span>
> <span data-ttu-id="72f09-109">[in] Количество миллисекунд, которые нужно ждать инициализации MAPI, можно передать INFINITE (0xFFFFFFFF), чтобы ждать вечно.</span><span class="sxs-lookup"><span data-stu-id="72f09-109">[in] The number of milliseconds to wait for MAPI to be initialized, you can pass INFINITE (0xFFFFFFFF) to wait forever.</span></span>

## <a name="return-value"></a><span data-ttu-id="72f09-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="72f09-110">Return value</span></span>

<span data-ttu-id="72f09-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="72f09-111">S_OK</span></span>
> <span data-ttu-id="72f09-112">MapI успешно инициализирована.</span><span class="sxs-lookup"><span data-stu-id="72f09-112">MAPI has been initialized successfully.</span></span>

<span data-ttu-id="72f09-113">HRESULT_FROM_WIN32 (ERROR_TIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="72f09-113">HRESULT_FROM_WIN32(ERROR_TIMEOUT)</span></span>
> <span data-ttu-id="72f09-114">Если дано бесконечное время ожидания, это указывает на то, что MAPI не инициализировался в течение этого периода.</span><span class="sxs-lookup"><span data-stu-id="72f09-114">When given a non-infinite timeout this indicates MAPI was not initialized during that period.</span></span>

## <a name="remarks"></a><span data-ttu-id="72f09-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="72f09-115">Remarks</span></span>
  
## <a name="see-also"></a><span data-ttu-id="72f09-116">См. также</span><span class="sxs-lookup"><span data-stu-id="72f09-116">See also</span></span>

[<span data-ttu-id="72f09-117">IMAPIInitMonitor</span><span class="sxs-lookup"><span data-stu-id="72f09-117">IMAPIInitMonitor</span></span>](imapiinitmonitoriunknown.md)

[<span data-ttu-id="72f09-118">IMAPIInitMonitor::IsInitialized</span><span class="sxs-lookup"><span data-stu-id="72f09-118">IMAPIInitMonitor::IsInitialized</span></span>](imapiinitmonitor-isinitialized.md)

[<span data-ttu-id="72f09-119">IMAPIInitMonitor::BeginWait</span><span class="sxs-lookup"><span data-stu-id="72f09-119">IMAPIInitMonitor::BeginWait</span></span>](imapiinitmonitor-beginwait.md)

[<span data-ttu-id="72f09-120">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="72f09-120">CreateMAPIInitializationMonitor</span></span>](createmapiinitializationmonitor.md)

[<span data-ttu-id="72f09-121">IMAPIWaitResult</span><span class="sxs-lookup"><span data-stu-id="72f09-121">IMAPIWaitResult</span></span>](imapiwaitresultiunknown.md)
