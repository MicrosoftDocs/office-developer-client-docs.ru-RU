---
title: Имапиоффлинесеткуррентстате
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321212"
---
# <a name="imapiofflinesetcurrentstate"></a><span data-ttu-id="03949-103">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="03949-103">IMAPIOffline::SetCurrentState</span></span>

  
  
<span data-ttu-id="03949-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03949-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03949-105">Задает текущее состояние автономного объекта: Online или offline.</span><span class="sxs-lookup"><span data-stu-id="03949-105">Sets the current state of an offline object to online or offline.</span></span>
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a><span data-ttu-id="03949-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="03949-106">Parameters</span></span>

 <span data-ttu-id="03949-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="03949-107">_ulFlags_</span></span>
  
> <span data-ttu-id="03949-108">возврата Изменяет поведение этого вызова.</span><span class="sxs-lookup"><span data-stu-id="03949-108">[in] Modifies the behavior of this call.</span></span> <span data-ttu-id="03949-109">Поддерживаются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="03949-109">The supported values are:</span></span>
    
<span data-ttu-id="03949-110">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="03949-110">MAPIOFFLINE_FLAG_BLOCK</span></span>
  
> <span data-ttu-id="03949-111">Если задать для параметра _ulFlags_ значение this, вызов **сеткуррентстате** будет заблокирован до завершения изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="03949-111">Setting  _ulFlags_ to this value will block the **SetCurrentState** call until the state change is complete.</span></span> <span data-ttu-id="03949-112">По умолчанию переход выполняется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="03949-112">By default the transition takes place asynchronously.</span></span> <span data-ttu-id="03949-113">Когда происходит асинхронный переход, все вызовы **сеткуррентстате** будут возвращать **е_пендинг** до завершения изменения.</span><span class="sxs-lookup"><span data-stu-id="03949-113">When the transition is occuring asynchronously, all **SetCurrentState** calls will return **E_PENDING** until the change is complete.</span></span> 
    
<span data-ttu-id="03949-114">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="03949-114">MAPIOFFLINE_FLAG_DEFAULT</span></span>
  
> <span data-ttu-id="03949-115">Задает текущее состояние без блокировки.</span><span class="sxs-lookup"><span data-stu-id="03949-115">Sets the current state without blocking.</span></span>
    
 <span data-ttu-id="03949-116">_Улмаск_</span><span class="sxs-lookup"><span data-stu-id="03949-116">_ulMask_</span></span>
  
> <span data-ttu-id="03949-117">возврата Часть состояния, которую необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="03949-117">[in] The part of the state to change.</span></span> <span data-ttu-id="03949-118">Единственное поддерживаемое значение — МАПИОФФЛИНЕ_СТАТЕ_ОФФЛИНЕ_МАСК.</span><span class="sxs-lookup"><span data-stu-id="03949-118">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="03949-119">_Улстате_</span><span class="sxs-lookup"><span data-stu-id="03949-119">_ulState_</span></span>
  
> <span data-ttu-id="03949-120">возврата Состояние, в которое нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="03949-120">[in] The state to change to.</span></span> <span data-ttu-id="03949-121">Оно должно быть одним из следующих двух значений:</span><span class="sxs-lookup"><span data-stu-id="03949-121">It must be one of these two values:</span></span>
    
<span data-ttu-id="03949-122">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="03949-122">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="03949-123">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="03949-123">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
 <span data-ttu-id="03949-124">_Сохранен_</span><span class="sxs-lookup"><span data-stu-id="03949-124">_pReserved_</span></span>
  
> <span data-ttu-id="03949-125">Этот параметр зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="03949-125">This parameter is reserved for Outlook internal use and is not supported.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="03949-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="03949-126">Return value</span></span>

<span data-ttu-id="03949-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="03949-127">S_OK</span></span>
  
> <span data-ttu-id="03949-128">Состояние автономного объекта успешно изменено.</span><span class="sxs-lookup"><span data-stu-id="03949-128">The state of the offline object has been changed successfully.</span></span>
    
<span data-ttu-id="03949-129">Е_ПЕНДИНГ</span><span class="sxs-lookup"><span data-stu-id="03949-129">E_PENDING</span></span>
  
> <span data-ttu-id="03949-130">Это указывает на то, что состояние автономного объекта изменяется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="03949-130">This indicates that the state of the offline object is changing asynchronously.</span></span> <span data-ttu-id="03949-131">Это происходит, когда _ulFlags_ имеет значение мапиоффлине_флаг_блокк в предыдущем вызове **сеткуррентстате** , а все последующие вызовы **сеткуррентстате** будут возвращать это значение до завершения асинхронного изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="03949-131">This occurs when  _ulFlags_ is set to MAPIOFFLINE_FLAG_BLOCK in an earlier **SetCurrentState** call, and any subsequent **SetCurrentState** call will return this value until the asynchronous state change is complete.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="03949-132">См. также</span><span class="sxs-lookup"><span data-stu-id="03949-132">See also</span></span>



[<span data-ttu-id="03949-133">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="03949-133">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="03949-134">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="03949-134">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)


[<span data-ttu-id="03949-135">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="03949-135">MAPI Constants</span></span>](mapi-constants.md)

