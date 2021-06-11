---
title: imapiinitmonitor-beginwait
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIINITMONITOR.BeginWait
api_type:
- COM
ms.assetid: 71f565a9-651c-42b5-9102-91b728b681ae
description: IMAPIInitMonitor::BeginWait"
Last modified: April 26, 2021
ms.openlocfilehash: 43a88507cbfc23b3b842f51e69eb4bd791bcfda8
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062020"
---
# <a name="imapiinitmonitorbeginwait"></a><span data-ttu-id="45c9d-103">IMAPIInitMonitor::BeginWait</span><span class="sxs-lookup"><span data-stu-id="45c9d-103">IMAPIInitMonitor::BeginWait</span></span>
  
<span data-ttu-id="45c9d-104">**Применяется к**: Outlook 2016 | 2019</span><span class="sxs-lookup"><span data-stu-id="45c9d-104">**Applies to**: Outlook 2016 | 2019</span></span>
  
<span data-ttu-id="45c9d-105">Начните ожидание инициализации MAPI или указанного числа миллисекунд, которые должны сойти.</span><span class="sxs-lookup"><span data-stu-id="45c9d-105">Start a wait for MAPI initialization or the specified number of milliseconds to elapse.</span></span> <span data-ttu-id="45c9d-106">Это возвращает интерфейс IMAPIWaitResult, который должен иметь **IMAPIWaitResult::End,** чтобы инициировать ожидание.</span><span class="sxs-lookup"><span data-stu-id="45c9d-106">This returns an IMAPIWaitResult interface which should have **IMAPIWaitResult::End** called in order initiate the wait.</span></span> <span data-ttu-id="45c9d-107">Это позволяет звонячему управлять тем, какой поток заблокирован во время ожидания.</span><span class="sxs-lookup"><span data-stu-id="45c9d-107">This allows the caller to control which thread is blocked while we are waiting.</span></span>

```cpp
HRESULT IMAPIInitMonitor::BeginWait(DWORD timeout, IMAPIWaitResult** ppResult)
```

## <a name="parameters"></a><span data-ttu-id="45c9d-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="45c9d-108">Parameters</span></span>
<span data-ttu-id="45c9d-109">_timeout_</span><span class="sxs-lookup"><span data-stu-id="45c9d-109">_timeout_</span></span>
><span data-ttu-id="45c9d-110">[in] Количество миллисекунд, которые нужно ждать инициализации MAPI, можно задать бесконечное ожидание инициализации навсегда.</span><span class="sxs-lookup"><span data-stu-id="45c9d-110">[in] The number of millisecond to wait for MAPI initialization, this can set to INFINITE to wait forever for the initialization to happen.</span></span>

<span data-ttu-id="45c9d-111">_ppResult_</span><span class="sxs-lookup"><span data-stu-id="45c9d-111">_ppResult_</span></span>
><span data-ttu-id="45c9d-112">[вышел] Указатель для получения нового интерфейса ожидания.</span><span class="sxs-lookup"><span data-stu-id="45c9d-112">[out] A pointer to recieve the newly create wait interface.</span></span>

## <a name="return-value"></a><span data-ttu-id="45c9d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="45c9d-113">Return value</span></span>
<span data-ttu-id="45c9d-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="45c9d-114">S_OK</span></span>
><span data-ttu-id="45c9d-115">Успешно началась операция ожидания.</span><span class="sxs-lookup"><span data-stu-id="45c9d-115">A wait operation was successfully started.</span></span>

<span data-ttu-id="45c9d-116">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="45c9d-116">E_OUTOFMEMORY</span></span>
><span data-ttu-id="45c9d-117">Для создания нового объекта не хватило памяти</span><span class="sxs-lookup"><span data-stu-id="45c9d-117">There was not enough memory to create a new object</span></span>

## <a name="remarks"></a><span data-ttu-id="45c9d-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="45c9d-118">Remarks</span></span>
<span data-ttu-id="45c9d-119">Этот API предоставил вызываемого пользователя интерфейс (безопасный для потоков), который можно использовать для инициализации блокировки для инициализации MAPI.</span><span class="sxs-lookup"><span data-stu-id="45c9d-119">This API provided the caller with an interface (which is thread-safe) which can be used initiate a blocking wait for MAPI initialization.</span></span> <span data-ttu-id="45c9d-120">Это позволяет потребителю отпугивать наилучшее ожидание для их приложения.</span><span class="sxs-lookup"><span data-stu-id="45c9d-120">This allows the consumer to deterime the best wait to wait for thier application.</span></span>   <span data-ttu-id="45c9d-121">Поведение вызова IMAPIWaitResult:::End идентично вызову IMAPIInitMonitor::Wait.</span><span class="sxs-lookup"><span data-stu-id="45c9d-121">The behavior of calling IMAPIWaitResult::End is identical to calling IMAPIInitMonitor::Wait.</span></span>

## <a name="see-also"></a><span data-ttu-id="45c9d-122">См. также</span><span class="sxs-lookup"><span data-stu-id="45c9d-122">See also</span></span>

[<span data-ttu-id="45c9d-123">IMAPIInitMonitor</span><span class="sxs-lookup"><span data-stu-id="45c9d-123">IMAPIInitMonitor</span></span>](imapiinitmonitoriunknown.md)

[<span data-ttu-id="45c9d-124">IMAPIInitMonitor::IsInitialized</span><span class="sxs-lookup"><span data-stu-id="45c9d-124">IMAPIInitMonitor::IsInitialized</span></span>](imapiinitmonitor-isinitialized.md)

[<span data-ttu-id="45c9d-125">IMAPIInitMonitor::Wait</span><span class="sxs-lookup"><span data-stu-id="45c9d-125">IMAPIInitMonitor::Wait</span></span>](imapiinitmonitor-wait.md)

[<span data-ttu-id="45c9d-126">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="45c9d-126">CreateMAPIInitializationMonitor</span></span>](createmapiinitializationmonitor.md)

[<span data-ttu-id="45c9d-127">IMAPIWaitResult</span><span class="sxs-lookup"><span data-stu-id="45c9d-127">IMAPIWaitResult</span></span>](imapiwaitresultiunknown.md)
