---
title: IMAPIOfflineSetCurrentState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.SetCurrentState
api_type:
- COM
ms.assetid: c0aa0df2-79f9-2558-7eb6-accae9bef4b2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 0b6837b51b09ecd9a60630c613e1806cb10c1d87
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421741"
---
# <a name="imapiofflinesetcurrentstate"></a><span data-ttu-id="0d67a-103">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="0d67a-103">IMAPIOffline::SetCurrentState</span></span>

  
  
<span data-ttu-id="0d67a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d67a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d67a-105">Задает текущее состояние автономного объекта в режиме online или автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="0d67a-105">Sets the current state of an offline object to online or offline.</span></span>
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a><span data-ttu-id="0d67a-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="0d67a-106">Parameters</span></span>

 <span data-ttu-id="0d67a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0d67a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0d67a-108">[in] Изменяет поведение этого вызова.</span><span class="sxs-lookup"><span data-stu-id="0d67a-108">[in] Modifies the behavior of this call.</span></span> <span data-ttu-id="0d67a-109">Поддерживаются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0d67a-109">The supported values are:</span></span>
    
<span data-ttu-id="0d67a-110">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="0d67a-110">MAPIOFFLINE_FLAG_BLOCK</span></span>
  
> <span data-ttu-id="0d67a-111">Настройка  _ulFlags к_ этому значению блокирует вызов **SetCurrentState** до завершения изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="0d67a-111">Setting  _ulFlags_ to this value will block the **SetCurrentState** call until the state change is complete.</span></span> <span data-ttu-id="0d67a-112">По умолчанию переход происходит асинхронно.</span><span class="sxs-lookup"><span data-stu-id="0d67a-112">By default the transition takes place asynchronously.</span></span> <span data-ttu-id="0d67a-113">Когда переход происходит асинхронно, **все** вызовы **SetCurrentState** возвращаются E_PENDING до завершения изменения.</span><span class="sxs-lookup"><span data-stu-id="0d67a-113">When the transition is occuring asynchronously, all **SetCurrentState** calls will return **E_PENDING** until the change is complete.</span></span> 
    
<span data-ttu-id="0d67a-114">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="0d67a-114">MAPIOFFLINE_FLAG_DEFAULT</span></span>
  
> <span data-ttu-id="0d67a-115">Задает текущее состояние без блокировки.</span><span class="sxs-lookup"><span data-stu-id="0d67a-115">Sets the current state without blocking.</span></span>
    
 <span data-ttu-id="0d67a-116">_ulMask_</span><span class="sxs-lookup"><span data-stu-id="0d67a-116">_ulMask_</span></span>
  
> <span data-ttu-id="0d67a-117">[in] Изменение части состояния.</span><span class="sxs-lookup"><span data-stu-id="0d67a-117">[in] The part of the state to change.</span></span> <span data-ttu-id="0d67a-118">Единственное поддерживаемые значения — MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="0d67a-118">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="0d67a-119">_ulState_</span><span class="sxs-lookup"><span data-stu-id="0d67a-119">_ulState_</span></span>
  
> <span data-ttu-id="0d67a-120">[in] Состояние, на который необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="0d67a-120">[in] The state to change to.</span></span> <span data-ttu-id="0d67a-121">Это должно быть одно из этих двух значений:</span><span class="sxs-lookup"><span data-stu-id="0d67a-121">It must be one of these two values:</span></span>
    
<span data-ttu-id="0d67a-122">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="0d67a-122">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="0d67a-123">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="0d67a-123">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
 <span data-ttu-id="0d67a-124">_pReserved_</span><span class="sxs-lookup"><span data-stu-id="0d67a-124">_pReserved_</span></span>
  
> <span data-ttu-id="0d67a-125">Этот параметр зарезервирован для Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0d67a-125">This parameter is reserved for Outlook internal use and is not supported.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0d67a-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0d67a-126">Return value</span></span>

<span data-ttu-id="0d67a-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="0d67a-127">S_OK</span></span>
  
> <span data-ttu-id="0d67a-128">Состояние автономного объекта успешно изменено.</span><span class="sxs-lookup"><span data-stu-id="0d67a-128">The state of the offline object has been changed successfully.</span></span>
    
<span data-ttu-id="0d67a-129">E_PENDING</span><span class="sxs-lookup"><span data-stu-id="0d67a-129">E_PENDING</span></span>
  
> <span data-ttu-id="0d67a-130">Это означает, что состояние автономного объекта меняется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="0d67a-130">This indicates that the state of the offline object is changing asynchronously.</span></span> <span data-ttu-id="0d67a-131">Это происходит, когда  _значение ulFlags_ MAPIOFFLINE_FLAG_BLOCK более ранним вызовом **SetCurrentState,** и любой последующий вызов **SetCurrentState** возвращает это значение до завершения асинхронного изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="0d67a-131">This occurs when  _ulFlags_ is set to MAPIOFFLINE_FLAG_BLOCK in an earlier **SetCurrentState** call, and any subsequent **SetCurrentState** call will return this value until the asynchronous state change is complete.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="0d67a-132">См. также</span><span class="sxs-lookup"><span data-stu-id="0d67a-132">See also</span></span>



[<span data-ttu-id="0d67a-133">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="0d67a-133">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="0d67a-134">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="0d67a-134">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)


[<span data-ttu-id="0d67a-135">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="0d67a-135">MAPI Constants</span></span>](mapi-constants.md)

