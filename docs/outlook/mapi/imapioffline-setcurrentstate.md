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
# <a name="imapiofflinesetcurrentstate"></a><span data-ttu-id="28e03-103">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="28e03-103">IMAPIOffline::SetCurrentState</span></span>

  
  
<span data-ttu-id="28e03-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="28e03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="28e03-105">Задает текущее состояние автономного объекта в сетевом или автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="28e03-105">Sets the current state of an offline object to online or offline.</span></span>
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a><span data-ttu-id="28e03-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="28e03-106">Parameters</span></span>

 <span data-ttu-id="28e03-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="28e03-107">_ulFlags_</span></span>
  
> <span data-ttu-id="28e03-108">[in] Изменяет поведение этого вызова.</span><span class="sxs-lookup"><span data-stu-id="28e03-108">[in] Modifies the behavior of this call.</span></span> <span data-ttu-id="28e03-109">Поддерживаются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="28e03-109">The supported values are:</span></span>
    
<span data-ttu-id="28e03-110">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="28e03-110">MAPIOFFLINE_FLAG_BLOCK</span></span>
  
> <span data-ttu-id="28e03-111">Установка  _этого значения для ulFlags_ блокирует вызов **SetCurrentState** до тех пор, пока не будет завершено изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="28e03-111">Setting  _ulFlags_ to this value will block the **SetCurrentState** call until the state change is complete.</span></span> <span data-ttu-id="28e03-112">По умолчанию переход происходит асинхронно.</span><span class="sxs-lookup"><span data-stu-id="28e03-112">By default the transition takes place asynchronously.</span></span> <span data-ttu-id="28e03-113">Когда переход происходит асинхронно, все вызовы **SetCurrentState** возвращаются E_PENDING до завершения изменения. </span><span class="sxs-lookup"><span data-stu-id="28e03-113">When the transition is occuring asynchronously, all **SetCurrentState** calls will return **E_PENDING** until the change is complete.</span></span> 
    
<span data-ttu-id="28e03-114">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="28e03-114">MAPIOFFLINE_FLAG_DEFAULT</span></span>
  
> <span data-ttu-id="28e03-115">Задает текущее состояние без блокировки.</span><span class="sxs-lookup"><span data-stu-id="28e03-115">Sets the current state without blocking.</span></span>
    
 <span data-ttu-id="28e03-116">_ulMask_</span><span class="sxs-lookup"><span data-stu-id="28e03-116">_ulMask_</span></span>
  
> <span data-ttu-id="28e03-117">[in] Часть состояния, который необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="28e03-117">[in] The part of the state to change.</span></span> <span data-ttu-id="28e03-118">Единственное поддерживаемые значения — MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="28e03-118">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="28e03-119">_ulState_</span><span class="sxs-lookup"><span data-stu-id="28e03-119">_ulState_</span></span>
  
> <span data-ttu-id="28e03-120">[in] Состояние, на который необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="28e03-120">[in] The state to change to.</span></span> <span data-ttu-id="28e03-121">Это должно быть одно из этих двух значений:</span><span class="sxs-lookup"><span data-stu-id="28e03-121">It must be one of these two values:</span></span>
    
<span data-ttu-id="28e03-122">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="28e03-122">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="28e03-123">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="28e03-123">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
 <span data-ttu-id="28e03-124">_pReserved_</span><span class="sxs-lookup"><span data-stu-id="28e03-124">_pReserved_</span></span>
  
> <span data-ttu-id="28e03-125">Этот параметр зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="28e03-125">This parameter is reserved for Outlook internal use and is not supported.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="28e03-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28e03-126">Return value</span></span>

<span data-ttu-id="28e03-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="28e03-127">S_OK</span></span>
  
> <span data-ttu-id="28e03-128">Состояние автономного объекта успешно изменено.</span><span class="sxs-lookup"><span data-stu-id="28e03-128">The state of the offline object has been changed successfully.</span></span>
    
<span data-ttu-id="28e03-129">E_PENDING</span><span class="sxs-lookup"><span data-stu-id="28e03-129">E_PENDING</span></span>
  
> <span data-ttu-id="28e03-130">Это означает, что состояние автономного объекта асинхронно изменяется.</span><span class="sxs-lookup"><span data-stu-id="28e03-130">This indicates that the state of the offline object is changing asynchronously.</span></span> <span data-ttu-id="28e03-131">Это происходит, когда для  _ulFlags_ установлено значение MAPIOFFLINE_FLAG_BLOCK в более ранних **вызовах SetCurrentState,** и любой последующий вызов **SetCurrentState** возвращает это значение до завершения асинхронного изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="28e03-131">This occurs when  _ulFlags_ is set to MAPIOFFLINE_FLAG_BLOCK in an earlier **SetCurrentState** call, and any subsequent **SetCurrentState** call will return this value until the asynchronous state change is complete.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="28e03-132">См. также</span><span class="sxs-lookup"><span data-stu-id="28e03-132">See also</span></span>



[<span data-ttu-id="28e03-133">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="28e03-133">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="28e03-134">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="28e03-134">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)


[<span data-ttu-id="28e03-135">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="28e03-135">MAPI Constants</span></span>](mapi-constants.md)

