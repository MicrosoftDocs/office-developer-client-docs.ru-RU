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
# <a name="mapioffline_notify"></a><span data-ttu-id="cb8b1-103">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="cb8b1-103">MAPIOFFLINE_NOTIFY</span></span>

<span data-ttu-id="cb8b1-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb8b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb8b1-105">Это уведомление об изменении состояния подключения.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-105">This is the notification for a change in the connection state.</span></span> <span data-ttu-id="cb8b1-106">Он указывает часть измененного состояния подключения, старое состояние подключения и новое состояние подключения.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-106">It indicates the part of the connection state that has changed, the old connection state, and the new connection state.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="cb8b1-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="cb8b1-107">Quick info</span></span>

<span data-ttu-id="cb8b1-108">См. **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-108">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
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

## <a name="members"></a><span data-ttu-id="cb8b1-109">"Участники"</span><span class="sxs-lookup"><span data-stu-id="cb8b1-109">Members</span></span>

 <span data-ttu-id="cb8b1-110">_ulSize_</span><span class="sxs-lookup"><span data-stu-id="cb8b1-110">_ulSize_</span></span>
  
> <span data-ttu-id="cb8b1-111">Размер структуры **MAPIOFFLINE_NOTIFY.**</span><span class="sxs-lookup"><span data-stu-id="cb8b1-111">Size of the **MAPIOFFLINE_NOTIFY** structure.</span></span> 
    
 <span data-ttu-id="cb8b1-112">_NotifyType_</span><span class="sxs-lookup"><span data-stu-id="cb8b1-112">_NotifyType_</span></span>
  
> <span data-ttu-id="cb8b1-113">Тип уведомления.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-113">Type of notification.</span></span> <span data-ttu-id="cb8b1-114">Обратите внимание, что поддерживается только уведомление об изменении состояния подключения; единственными поддерживаемыми значениями являются:</span><span class="sxs-lookup"><span data-stu-id="cb8b1-114">Note that only notification on change of the connection state is supported; the only supported values are:</span></span>
    
   - <span data-ttu-id="cb8b1-115">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START</span><span class="sxs-lookup"><span data-stu-id="cb8b1-115">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START</span></span>
    
   - <span data-ttu-id="cb8b1-116">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE</span><span class="sxs-lookup"><span data-stu-id="cb8b1-116">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE</span></span>
    
   - <span data-ttu-id="cb8b1-117">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE</span><span class="sxs-lookup"><span data-stu-id="cb8b1-117">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE</span></span>
    
 <span data-ttu-id="cb8b1-118">_ulClientToken_</span><span class="sxs-lookup"><span data-stu-id="cb8b1-118">_ulClientToken_</span></span>
  
> <span data-ttu-id="cb8b1-119">Маркер, определенный клиентом в **[структуре MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-119">A token defined by the client in the **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** structure in **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> 
    
 <span data-ttu-id="cb8b1-120">_ulMask_</span><span class="sxs-lookup"><span data-stu-id="cb8b1-120">_ulMask_</span></span>
  
> <span data-ttu-id="cb8b1-121">Измененная часть состояния подключения.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-121">The part of the connection state that has changed.</span></span> <span data-ttu-id="cb8b1-122">Единственное поддерживаемые значения — MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-122">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="cb8b1-123">_ulStateOld_</span><span class="sxs-lookup"><span data-stu-id="cb8b1-123">_ulStateOld_</span></span>
  
> <span data-ttu-id="cb8b1-124">Старое состояние подключения.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-124">The old connection state.</span></span> <span data-ttu-id="cb8b1-125">Единственными поддерживаемыми значениями являются:</span><span class="sxs-lookup"><span data-stu-id="cb8b1-125">The only supported values are:</span></span>
    
   - <span data-ttu-id="cb8b1-126">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="cb8b1-126">MAPIOFFLINE_STATE_OFFLINE</span></span>
    
   - <span data-ttu-id="cb8b1-127">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="cb8b1-127">MAPIOFFLINE_STATE_ONLINE</span></span>
    
 <span data-ttu-id="cb8b1-128">_ulStateNew_</span><span class="sxs-lookup"><span data-stu-id="cb8b1-128">_ulStateNew_</span></span>
  
> <span data-ttu-id="cb8b1-129">Новое состояние подключения.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-129">The new connection state.</span></span> <span data-ttu-id="cb8b1-130">Единственными поддерживаемыми значениями являются:</span><span class="sxs-lookup"><span data-stu-id="cb8b1-130">The only supported values are:</span></span>
    
   - <span data-ttu-id="cb8b1-131">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="cb8b1-131">MAPIOFFLINE_STATE_OFFLINE</span></span>
    
   - <span data-ttu-id="cb8b1-132">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="cb8b1-132">MAPIOFFLINE_STATE_ONLINE</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cb8b1-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="cb8b1-133">Remarks</span></span>

<span data-ttu-id="cb8b1-134">API состояния автономного доступа поддерживает только уведомления об изменениях в режиме online/offline.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-134">The Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="cb8b1-135">Клиент должен проверить, Outlook возвращает следующие значения, прежде чем исследовать фактическое изменение:</span><span class="sxs-lookup"><span data-stu-id="cb8b1-135">A client must check that Outlook returns the following values before examining the actual change:</span></span>
  
1.  <span data-ttu-id="cb8b1-136">*NotifyType*  имеет значение MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE или MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-136">*NotifyType*  has the value MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE, or MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE.</span></span> <span data-ttu-id="cb8b1-137">В этом случае клиент может предположить, что изменение является изменением состояния подключения, а *Info* — структурой *StateChange.*</span><span class="sxs-lookup"><span data-stu-id="cb8b1-137">In this case, the client can assume that the change is a connection state change, and  *Info*  is of the structure  *StateChange*  .</span></span> 
    
2.  <span data-ttu-id="cb8b1-138">*ulMask*  имеет значение MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-138">*ulMask*  has the value MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span> <span data-ttu-id="cb8b1-139">В этом случае клиент может предположить, что изменение является изменением состояния подключения в режиме online/offline и может продолжить изучение *ulStateOld* и *ulStateNew.*</span><span class="sxs-lookup"><span data-stu-id="cb8b1-139">In this case, the client can assume that the change is an online/offline connection state change, and can proceed with examining  *ulStateOld*  and  *ulStateNew*  .</span></span> 
    
<span data-ttu-id="cb8b1-140">Не исключено, что Outlook клиента о других изменениях, которые не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-140">It is possible that Outlook notifies a client of other changes that are not supported.</span></span> <span data-ttu-id="cb8b1-141">В таких случаях  *NotifyType*  не будет одним из трех значений, о чем говорилось ранее, или  *ulMask*  не будет MAPIOFFLINE_STATE_OFFLINE_MASK, и клиент должен игнорировать остальные данные в  *Info*  .</span><span class="sxs-lookup"><span data-stu-id="cb8b1-141">In such cases,  *NotifyType*  would not be any one of the three values stated previously, or  *ulMask*  would not be MAPIOFFLINE_STATE_OFFLINE_MASK, and the client must ignore the rest of the data in  *Info*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cb8b1-142">См. также</span><span class="sxs-lookup"><span data-stu-id="cb8b1-142">See also</span></span>

- [<span data-ttu-id="cb8b1-143">Об API автономного режима</span><span class="sxs-lookup"><span data-stu-id="cb8b1-143">About the Offline State API</span></span>](about-the-offline-state-api.md)  
- [<span data-ttu-id="cb8b1-144">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="cb8b1-144">MAPI Constants</span></span>](mapi-constants.md)  
- [<span data-ttu-id="cb8b1-145">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="cb8b1-145">MAPIOFFLINE_NOTIFY_TYPE</span></span>](mapioffline_notify_type.md)

