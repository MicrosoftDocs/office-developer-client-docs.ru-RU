---
title: MAPIOFFLINE_NOTIFY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e03c5a87-4513-2133-ae0a-11d242f80e4b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6c5480a8f5e008c01c7ab8141317f5f19547ab10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414769"
---
# <a name="mapioffline_notify"></a><span data-ttu-id="7dd7d-103">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="7dd7d-103">MAPIOFFLINE_NOTIFY</span></span>

<span data-ttu-id="7dd7d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7dd7d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7dd7d-105">Это уведомление об изменении состояния подключения.</span><span class="sxs-lookup"><span data-stu-id="7dd7d-105">This is the notification for a change in the connection state.</span></span> <span data-ttu-id="7dd7d-106">Он указывает измененную часть состояния подключения, старое и новое состояние подключения.</span><span class="sxs-lookup"><span data-stu-id="7dd7d-106">It indicates the part of the connection state that has changed, the old connection state, and the new connection state.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7dd7d-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="7dd7d-107">Quick info</span></span>

<span data-ttu-id="7dd7d-108">См. **[IMAPIOfflineNotify.](imapiofflinenotifyiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="7dd7d-108">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
```cpp
typedef struct  
{ 
      ULONG ulSize; 
      MAPIOFFLINE_NOTIFY_TYPE NotifyType; 
      ULONG ulClientToken; 
      union { 
         struct 
           { 
           ULONG ulMask; 
           ULONG ulStateOld; 
           ULONG ulStateNew; 
           } StateChange; 
             } Info; 
} MAPIOFFLINE_NOTIFY;
```

## <a name="members"></a><span data-ttu-id="7dd7d-109">"Участники"</span><span class="sxs-lookup"><span data-stu-id="7dd7d-109">Members</span></span>

 <span data-ttu-id="7dd7d-110">_ulSize_</span><span class="sxs-lookup"><span data-stu-id="7dd7d-110">_ulSize_</span></span>
  
> <span data-ttu-id="7dd7d-111">Размер **MAPIOFFLINE_NOTIFY** структуры.</span><span class="sxs-lookup"><span data-stu-id="7dd7d-111">Size of the **MAPIOFFLINE_NOTIFY** structure.</span></span> 
    
 <span data-ttu-id="7dd7d-112">_NotifyType_</span><span class="sxs-lookup"><span data-stu-id="7dd7d-112">_NotifyType_</span></span>
  
> <span data-ttu-id="7dd7d-113">Тип уведомления.</span><span class="sxs-lookup"><span data-stu-id="7dd7d-113">Type of notification.</span></span> <span data-ttu-id="7dd7d-114">Обратите внимание, что поддерживается только уведомление об изменении состояния подключения; Поддерживаются только такие значения:</span><span class="sxs-lookup"><span data-stu-id="7dd7d-114">Note that only notification on change of the connection state is supported; the only supported values are:</span></span>
    
   - <span data-ttu-id="7dd7d-115">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START</span><span class="sxs-lookup"><span data-stu-id="7dd7d-115">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START</span></span>
    
   - <span data-ttu-id="7dd7d-116">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE</span><span class="sxs-lookup"><span data-stu-id="7dd7d-116">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE</span></span>
    
   - <span data-ttu-id="7dd7d-117">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE</span><span class="sxs-lookup"><span data-stu-id="7dd7d-117">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE</span></span>
    
 <span data-ttu-id="7dd7d-118">_ulClientToken_</span><span class="sxs-lookup"><span data-stu-id="7dd7d-118">_ulClientToken_</span></span>
  
> <span data-ttu-id="7dd7d-119">Маркер, определенный клиентом **[](mapioffline_adviseinfo.md)** в структуре MAPIOFFLINE_ADVISEINFO **[IMAPIOfflineMgr::Advise.](imapiofflinemgr-advise.md)**</span><span class="sxs-lookup"><span data-stu-id="7dd7d-119">A token defined by the client in the **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** structure in **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> 
    
 <span data-ttu-id="7dd7d-120">_ulMask_</span><span class="sxs-lookup"><span data-stu-id="7dd7d-120">_ulMask_</span></span>
  
> <span data-ttu-id="7dd7d-121">Измененная часть состояния подключения.</span><span class="sxs-lookup"><span data-stu-id="7dd7d-121">The part of the connection state that has changed.</span></span> <span data-ttu-id="7dd7d-122">Единственное поддерживаемые значения — MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="7dd7d-122">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="7dd7d-123">_ulStateOld_</span><span class="sxs-lookup"><span data-stu-id="7dd7d-123">_ulStateOld_</span></span>
  
> <span data-ttu-id="7dd7d-124">Старое состояние подключения.</span><span class="sxs-lookup"><span data-stu-id="7dd7d-124">The old connection state.</span></span> <span data-ttu-id="7dd7d-125">Поддерживаются только такие значения:</span><span class="sxs-lookup"><span data-stu-id="7dd7d-125">The only supported values are:</span></span>
    
   - <span data-ttu-id="7dd7d-126">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="7dd7d-126">MAPIOFFLINE_STATE_OFFLINE</span></span>
    
   - <span data-ttu-id="7dd7d-127">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="7dd7d-127">MAPIOFFLINE_STATE_ONLINE</span></span>
    
 <span data-ttu-id="7dd7d-128">_ulStateNew_</span><span class="sxs-lookup"><span data-stu-id="7dd7d-128">_ulStateNew_</span></span>
  
> <span data-ttu-id="7dd7d-129">Новое состояние подключения.</span><span class="sxs-lookup"><span data-stu-id="7dd7d-129">The new connection state.</span></span> <span data-ttu-id="7dd7d-130">Поддерживаются только такие значения:</span><span class="sxs-lookup"><span data-stu-id="7dd7d-130">The only supported values are:</span></span>
    
   - <span data-ttu-id="7dd7d-131">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="7dd7d-131">MAPIOFFLINE_STATE_OFFLINE</span></span>
    
   - <span data-ttu-id="7dd7d-132">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="7dd7d-132">MAPIOFFLINE_STATE_ONLINE</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7dd7d-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="7dd7d-133">Remarks</span></span>

<span data-ttu-id="7dd7d-134">API автономного состояния поддерживает только уведомления об изменениях в сети или автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="7dd7d-134">The Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="7dd7d-135">Перед проверкой фактического изменения клиент должен проверить, возвращает ли Outlook следующие значения:</span><span class="sxs-lookup"><span data-stu-id="7dd7d-135">A client must check that Outlook returns the following values before examining the actual change:</span></span>
  
1.  <span data-ttu-id="7dd7d-136">*NotifyType*  имеет значение MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE или MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE.</span><span class="sxs-lookup"><span data-stu-id="7dd7d-136">*NotifyType*  has the value MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE, or MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE.</span></span> <span data-ttu-id="7dd7d-137">В этом случае клиент может предположить, что изменение является изменением состояния подключения, а *сведения* — структурой *StateChange.*</span><span class="sxs-lookup"><span data-stu-id="7dd7d-137">In this case, the client can assume that the change is a connection state change, and  *Info*  is of the structure  *StateChange*  .</span></span> 
    
2.  <span data-ttu-id="7dd7d-138">*ulMask*  имеет значение MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="7dd7d-138">*ulMask*  has the value MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span> <span data-ttu-id="7dd7d-139">В этом случае клиент может предположить, что это изменение сетевого/автономного состояния подключения, и продолжить изучение *ulStateOld* и *ulStateNew.*</span><span class="sxs-lookup"><span data-stu-id="7dd7d-139">In this case, the client can assume that the change is an online/offline connection state change, and can proceed with examining  *ulStateOld*  and  *ulStateNew*  .</span></span> 
    
<span data-ttu-id="7dd7d-140">Вполне возможно, что Outlook извеирует клиента о других изменениях, которые не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="7dd7d-140">It is possible that Outlook notifies a client of other changes that are not supported.</span></span> <span data-ttu-id="7dd7d-141">В таких случаях *NotifyType* не будет одним из трех значений, которые были заранее задеклины, или *ulMask* не будет MAPIOFFLINE_STATE_OFFLINE_MASK, и клиент должен игнорировать остальные данные в *сведениях.*</span><span class="sxs-lookup"><span data-stu-id="7dd7d-141">In such cases,  *NotifyType*  would not be any one of the three values stated previously, or  *ulMask*  would not be MAPIOFFLINE_STATE_OFFLINE_MASK, and the client must ignore the rest of the data in  *Info*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7dd7d-142">См. также</span><span class="sxs-lookup"><span data-stu-id="7dd7d-142">See also</span></span>

- [<span data-ttu-id="7dd7d-143">Об API автономного режима</span><span class="sxs-lookup"><span data-stu-id="7dd7d-143">About the Offline State API</span></span>](about-the-offline-state-api.md)  
- [<span data-ttu-id="7dd7d-144">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="7dd7d-144">MAPI Constants</span></span>](mapi-constants.md)  
- [<span data-ttu-id="7dd7d-145">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="7dd7d-145">MAPIOFFLINE_NOTIFY_TYPE</span></span>](mapioffline_notify_type.md)

