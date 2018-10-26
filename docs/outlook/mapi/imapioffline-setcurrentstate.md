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
ms.openlocfilehash: 13a4cf401cf51241a52401668eef008d65aa5459
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567141"
---
# <a name="imapiofflinesetcurrentstate"></a><span data-ttu-id="203c5-103">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="203c5-103">IMAPIOffline::SetCurrentState</span></span>

  
  
<span data-ttu-id="203c5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="203c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="203c5-105">Задает текущее состояние автономной объекта в сети или в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="203c5-105">Sets the current state of an offline object to online or offline.</span></span>
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a><span data-ttu-id="203c5-106">���������</span><span class="sxs-lookup"><span data-stu-id="203c5-106">Parameters</span></span>

 <span data-ttu-id="203c5-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="203c5-107">_ulFlags_</span></span>
  
> <span data-ttu-id="203c5-108">[in] Изменение поведения этот вызов.</span><span class="sxs-lookup"><span data-stu-id="203c5-108">[in] Modifies the behavior of this call.</span></span> <span data-ttu-id="203c5-109">Приведены поддерживаемые значения.</span><span class="sxs-lookup"><span data-stu-id="203c5-109">The supported values are:</span></span>
    
<span data-ttu-id="203c5-110">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="203c5-110">MAPIOFFLINE_FLAG_BLOCK</span></span>
  
> <span data-ttu-id="203c5-111">Установка _ulFlags_ для этого значения будет блокировать вызов **SetCurrentState** до завершения изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="203c5-111">Setting  _ulFlags_ to this value will block the **SetCurrentState** call until the state change is complete.</span></span> <span data-ttu-id="203c5-112">По умолчанию переход происходит асинхронно.</span><span class="sxs-lookup"><span data-stu-id="203c5-112">By default the transition takes place asynchronously.</span></span> <span data-ttu-id="203c5-113">При переходе отмену асинхронно, все вызовы **SetCurrentState** возвращает **E_PENDING** до завершения изменения.</span><span class="sxs-lookup"><span data-stu-id="203c5-113">When the transition is occuring asynchronously, all **SetCurrentState** calls will return **E_PENDING** until the change is complete.</span></span> 
    
<span data-ttu-id="203c5-114">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="203c5-114">MAPIOFFLINE_FLAG_DEFAULT</span></span>
  
> <span data-ttu-id="203c5-115">Задает текущее состояние без блокировки.</span><span class="sxs-lookup"><span data-stu-id="203c5-115">Sets the current state without blocking.</span></span>
    
 <span data-ttu-id="203c5-116">_ulMask_</span><span class="sxs-lookup"><span data-stu-id="203c5-116">_ulMask_</span></span>
  
> <span data-ttu-id="203c5-117">[in] Часть состояния для изменения.</span><span class="sxs-lookup"><span data-stu-id="203c5-117">[in] The part of the state to change.</span></span> <span data-ttu-id="203c5-118">Поддерживается только значение — MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="203c5-118">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="203c5-119">_ulState_</span><span class="sxs-lookup"><span data-stu-id="203c5-119">_ulState_</span></span>
  
> <span data-ttu-id="203c5-120">[in] Чтобы изменить на состояние.</span><span class="sxs-lookup"><span data-stu-id="203c5-120">[in] The state to change to.</span></span> <span data-ttu-id="203c5-121">Оно должно быть одно из следующих двух значений:</span><span class="sxs-lookup"><span data-stu-id="203c5-121">It must be one of these two values:</span></span>
    
<span data-ttu-id="203c5-122">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="203c5-122">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="203c5-123">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="203c5-123">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
 <span data-ttu-id="203c5-124">_Сохраняются_</span><span class="sxs-lookup"><span data-stu-id="203c5-124">_pReserved_</span></span>
  
> <span data-ttu-id="203c5-125">Этот параметр зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="203c5-125">This parameter is reserved for Outlook internal use and is not supported.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="203c5-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="203c5-126">Return value</span></span>

<span data-ttu-id="203c5-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="203c5-127">S_OK</span></span>
  
> <span data-ttu-id="203c5-128">Состояние объекта автономной успешно изменены.</span><span class="sxs-lookup"><span data-stu-id="203c5-128">The state of the offline object has been changed successfully.</span></span>
    
<span data-ttu-id="203c5-129">E_PENDING</span><span class="sxs-lookup"><span data-stu-id="203c5-129">E_PENDING</span></span>
  
> <span data-ttu-id="203c5-130">Это указывает на то асинхронно изменение состояния автономного объекта.</span><span class="sxs-lookup"><span data-stu-id="203c5-130">This indicates that the state of the offline object is changing asynchronously.</span></span> <span data-ttu-id="203c5-131">Происходит, когда _ulFlags_ задано значение MAPIOFFLINE_FLAG_BLOCK в более ранних вызова **SetCurrentState** , а все последующие вызова **SetCurrentState** возвращает это значение до завершения изменений состояния асинхронной.</span><span class="sxs-lookup"><span data-stu-id="203c5-131">This occurs when  _ulFlags_ is set to MAPIOFFLINE_FLAG_BLOCK in an earlier **SetCurrentState** call, and any subsequent **SetCurrentState** call will return this value until the asynchronous state change is complete.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="203c5-132">См. также</span><span class="sxs-lookup"><span data-stu-id="203c5-132">See also</span></span>



[<span data-ttu-id="203c5-133">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="203c5-133">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="203c5-134">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="203c5-134">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)


[<span data-ttu-id="203c5-135">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="203c5-135">MAPI Constants</span></span>](mapi-constants.md)

