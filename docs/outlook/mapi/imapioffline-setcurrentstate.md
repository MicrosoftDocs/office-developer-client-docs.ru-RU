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
ms.openlocfilehash: 15e2d5c2aca595c3a06d215cd069c23da3e48125
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808997"
---
# <a name="imapiofflinesetcurrentstate"></a><span data-ttu-id="ef727-103">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="ef727-103">IMAPIOffline::SetCurrentState</span></span>

  
  
<span data-ttu-id="ef727-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ef727-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ef727-105">Задает текущее состояние автономной объекта в сети или в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="ef727-105">Sets the current state of an offline object to online or offline.</span></span>
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a><span data-ttu-id="ef727-106">���������</span><span class="sxs-lookup"><span data-stu-id="ef727-106">Parameters</span></span>

 <span data-ttu-id="ef727-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ef727-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ef727-108">[in] Изменение поведения этот вызов.</span><span class="sxs-lookup"><span data-stu-id="ef727-108">[in] Modifies the behavior of this call.</span></span> <span data-ttu-id="ef727-109">Приведены поддерживаемые значения.</span><span class="sxs-lookup"><span data-stu-id="ef727-109">The supported values are:</span></span>
    
<span data-ttu-id="ef727-110">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="ef727-110">MAPIOFFLINE_FLAG_BLOCK</span></span>
  
> <span data-ttu-id="ef727-111">Установка _ulFlags_ для этого значения будет блокировать вызов **SetCurrentState** до завершения изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="ef727-111">Setting  _ulFlags_ to this value will block the **SetCurrentState** call until the state change is complete.</span></span> <span data-ttu-id="ef727-112">По умолчанию переход происходит асинхронно.</span><span class="sxs-lookup"><span data-stu-id="ef727-112">By default the transition takes place asynchronously.</span></span> <span data-ttu-id="ef727-113">При переходе отмену асинхронно, все вызовы **SetCurrentState** возвращает **E_PENDING** до завершения изменения.</span><span class="sxs-lookup"><span data-stu-id="ef727-113">When the transition is occuring asynchronously, all **SetCurrentState** calls will return **E_PENDING** until the change is complete.</span></span> 
    
<span data-ttu-id="ef727-114">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ef727-114">MAPIOFFLINE_FLAG_DEFAULT</span></span>
  
> <span data-ttu-id="ef727-115">Задает текущее состояние без блокировки.</span><span class="sxs-lookup"><span data-stu-id="ef727-115">Sets the current state without blocking.</span></span>
    
 <span data-ttu-id="ef727-116">_ulMask_</span><span class="sxs-lookup"><span data-stu-id="ef727-116">_ulMask_</span></span>
  
> <span data-ttu-id="ef727-117">[in] Часть состояния для изменения.</span><span class="sxs-lookup"><span data-stu-id="ef727-117">[in] The part of the state to change.</span></span> <span data-ttu-id="ef727-118">Поддерживается только значение — MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="ef727-118">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="ef727-119">_ulState_</span><span class="sxs-lookup"><span data-stu-id="ef727-119">_ulState_</span></span>
  
> <span data-ttu-id="ef727-120">[in] Чтобы изменить на состояние.</span><span class="sxs-lookup"><span data-stu-id="ef727-120">[in] The state to change to.</span></span> <span data-ttu-id="ef727-121">Оно должно быть одно из следующих двух значений:</span><span class="sxs-lookup"><span data-stu-id="ef727-121">It must be one of these two values:</span></span>
    
<span data-ttu-id="ef727-122">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="ef727-122">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="ef727-123">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="ef727-123">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
 <span data-ttu-id="ef727-124">_Сохраняются_</span><span class="sxs-lookup"><span data-stu-id="ef727-124">_pReserved_</span></span>
  
> <span data-ttu-id="ef727-125">Этот параметр зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ef727-125">This parameter is reserved for Outlook internal use and is not supported.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ef727-126">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="ef727-126">Return value</span></span>

<span data-ttu-id="ef727-127">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="ef727-127">S_OK</span></span>
  
> <span data-ttu-id="ef727-128">Состояние объекта автономной успешно изменены.</span><span class="sxs-lookup"><span data-stu-id="ef727-128">The state of the offline object has been changed successfully.</span></span>
    
<span data-ttu-id="ef727-129">E_PENDING</span><span class="sxs-lookup"><span data-stu-id="ef727-129">E_PENDING</span></span>
  
> <span data-ttu-id="ef727-130">Это указывает на то асинхронно изменение состояния автономного объекта.</span><span class="sxs-lookup"><span data-stu-id="ef727-130">This indicates that the state of the offline object is changing asynchronously.</span></span> <span data-ttu-id="ef727-131">Происходит, когда _ulFlags_ задано значение MAPIOFFLINE_FLAG_BLOCK в более ранних вызова **SetCurrentState** , а все последующие вызова **SetCurrentState** возвращает это значение до завершения изменений состояния асинхронной.</span><span class="sxs-lookup"><span data-stu-id="ef727-131">This occurs when  _ulFlags_ is set to MAPIOFFLINE_FLAG_BLOCK in an earlier **SetCurrentState** call, and any subsequent **SetCurrentState** call will return this value until the asynchronous state change is complete.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="ef727-132">См. также</span><span class="sxs-lookup"><span data-stu-id="ef727-132">See also</span></span>



[<span data-ttu-id="ef727-133">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="ef727-133">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="ef727-134">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="ef727-134">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)


[<span data-ttu-id="ef727-135">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="ef727-135">MAPI Constants</span></span>](mapi-constants.md)

