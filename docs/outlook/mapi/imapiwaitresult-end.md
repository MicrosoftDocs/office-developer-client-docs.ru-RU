---
title: IMAPIWaitResult::End
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIWaitResult.End
api_type:
- COM
ms.assetid: 7463c9e8-d065-4cc3-ac01-d428b57bbc88
description: IMAPIWaitResult::End
Last modified: April 26, 2021
ms.openlocfilehash: 3432bf3b71fa7e15cb4621d461a8d4bbe962f1ba
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062034"
---
# <a name="imapiwaitresultend"></a><span data-ttu-id="d08b0-103">IMAPIWaitResult::End</span><span class="sxs-lookup"><span data-stu-id="d08b0-103">IMAPIWaitResult::End</span></span>
  
<span data-ttu-id="d08b0-104">**Применяется к**: Outlook 2013 | Outlook 2016 | 2019</span><span class="sxs-lookup"><span data-stu-id="d08b0-104">**Applies to**: Outlook 2013 | Outlook 2016 | 2019</span></span>

<span data-ttu-id="d08b0-105">Инициирует вызов BLOCKING в этом потоке, который возвращается либо после инициализации указанного числа миллисекунд, либо при инициализации MAPI.</span><span class="sxs-lookup"><span data-stu-id="d08b0-105">Initiates a BLOCKING call on this thread, which will return either when the specified number of milliseconds have elapsed or MAPI has been initialized.</span></span> <span data-ttu-id="d08b0-106">INFINITE можно использовать для бесконечного ожидания.</span><span class="sxs-lookup"><span data-stu-id="d08b0-106">INFINITE can be used to for an infinite wait.</span></span>

```cpp
HRESULT IMAPIWaitResult::End(DWORD timeout)
```

## <a name="parameters"></a><span data-ttu-id="d08b0-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="d08b0-107">Parameters</span></span>

<span data-ttu-id="d08b0-108">_timeout_</span><span class="sxs-lookup"><span data-stu-id="d08b0-108">_timeout_</span></span>
> <span data-ttu-id="d08b0-109">[in] Количество миллисекунд для ожидания инициализации MAPI можно передать INFINITE (0xFFFFFFFF), чтобы ждать вечно.</span><span class="sxs-lookup"><span data-stu-id="d08b0-109">[in] The number of millisecond to wait for MAPI to be initialized, you can pass INFINITE (0xFFFFFFFF) to wait forever.</span></span>

## <a name="return-value"></a><span data-ttu-id="d08b0-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d08b0-110">Return value</span></span>

<span data-ttu-id="d08b0-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="d08b0-111">S_OK</span></span>
> <span data-ttu-id="d08b0-112">MAPI успешно инициализирована</span><span class="sxs-lookup"><span data-stu-id="d08b0-112">MAPI has been initialized successfully</span></span>

<span data-ttu-id="d08b0-113">HRESULT_FROM_WIN32 (ERROR_TIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="d08b0-113">HRESULT_FROM_WIN32(ERROR_TIMEOUT)</span></span>
> <span data-ttu-id="d08b0-114">Если дано бесконечное время ожидания, это указывает на то, что MAPI не инициализировался в течение этого периода.</span><span class="sxs-lookup"><span data-stu-id="d08b0-114">When given a non-infinite timeout this indicates MAPI was not initialized during that period.</span></span>

## <a name="remarks"></a><span data-ttu-id="d08b0-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="d08b0-115">Remarks</span></span>
<span data-ttu-id="d08b0-116">Этот API ведет себя точно так же, как [и IMAPInitMonitor::Wait](imapiinitmonitor-wait.md).</span><span class="sxs-lookup"><span data-stu-id="d08b0-116">This API behaves exactly the same as [IMAPInitMonitor::Wait](imapiinitmonitor-wait.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d08b0-117">См. также</span><span class="sxs-lookup"><span data-stu-id="d08b0-117">See also</span></span>

[<span data-ttu-id="d08b0-118">IMAPIInitMonitor::IsInitialized</span><span class="sxs-lookup"><span data-stu-id="d08b0-118">IMAPIInitMonitor::IsInitialized</span></span>](imapiinitmonitor-isinitialized.md)

[<span data-ttu-id="d08b0-119">IMAPIInitMonitor::BeginWait</span><span class="sxs-lookup"><span data-stu-id="d08b0-119">IMAPIInitMonitor::BeginWait</span></span>](imapiinitmonitor-beginwait.md)

[<span data-ttu-id="d08b0-120">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="d08b0-120">CreateMAPIInitializationMonitor</span></span>](createmapiinitializationmonitor.md)

[<span data-ttu-id="d08b0-121">IMAPIWaitResult</span><span class="sxs-lookup"><span data-stu-id="d08b0-121">IMAPIWaitResult</span></span>](imapiwaitresultiunknown.md)
