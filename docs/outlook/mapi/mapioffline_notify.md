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
ms.openlocfilehash: b18a4ae4ee25898d1100d9763714e5be21c69fd8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580728"
---
# <a name="mapiofflinenotify"></a><span data-ttu-id="e9c06-103">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="e9c06-103">MAPIOFFLINE_NOTIFY</span></span>

<span data-ttu-id="e9c06-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9c06-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9c06-105">Это уведомление, чтобы внести изменения в состоянии подключения.</span><span class="sxs-lookup"><span data-stu-id="e9c06-105">This is the notification for a change in the connection state.</span></span> <span data-ttu-id="e9c06-106">Он указывает часть состояния подключения, который был изменен, старый состояние подключения и новое состояние подключения.</span><span class="sxs-lookup"><span data-stu-id="e9c06-106">It indicates the part of the connection state that has changed, the old connection state, and the new connection state.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e9c06-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="e9c06-107">Quick info</span></span>

<span data-ttu-id="e9c06-108">В разделе **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="e9c06-108">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
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

## <a name="members"></a><span data-ttu-id="e9c06-109">Members</span><span class="sxs-lookup"><span data-stu-id="e9c06-109">Members</span></span>

 <span data-ttu-id="e9c06-110">_ulSize_</span><span class="sxs-lookup"><span data-stu-id="e9c06-110">_ulSize_</span></span>
  
> <span data-ttu-id="e9c06-111">Размер структуры **MAPIOFFLINE_NOTIFY** .</span><span class="sxs-lookup"><span data-stu-id="e9c06-111">Size of the **MAPIOFFLINE_NOTIFY** structure.</span></span> 
    
 <span data-ttu-id="e9c06-112">_NotifyType_</span><span class="sxs-lookup"><span data-stu-id="e9c06-112">_NotifyType_</span></span>
  
> <span data-ttu-id="e9c06-113">Тип уведомления.</span><span class="sxs-lookup"><span data-stu-id="e9c06-113">Type of notification.</span></span> <span data-ttu-id="e9c06-114">Обратите внимание на то, что поддерживается только уведомлений на изменения состояния подключения; поддерживаются только поддерживаемые значения:</span><span class="sxs-lookup"><span data-stu-id="e9c06-114">Note that only notification on change of the connection state is supported; the only supported values are:</span></span>
    
   - <span data-ttu-id="e9c06-115">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START</span><span class="sxs-lookup"><span data-stu-id="e9c06-115">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START</span></span>
    
   - <span data-ttu-id="e9c06-116">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE</span><span class="sxs-lookup"><span data-stu-id="e9c06-116">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE</span></span>
    
   - <span data-ttu-id="e9c06-117">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE</span><span class="sxs-lookup"><span data-stu-id="e9c06-117">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE</span></span>
    
 <span data-ttu-id="e9c06-118">_ulClientToken_</span><span class="sxs-lookup"><span data-stu-id="e9c06-118">_ulClientToken_</span></span>
  
> <span data-ttu-id="e9c06-119">Маркер, определенные в клиенте в структуре **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** в **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="e9c06-119">A token defined by the client in the **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** structure in **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> 
    
 <span data-ttu-id="e9c06-120">_ulMask_</span><span class="sxs-lookup"><span data-stu-id="e9c06-120">_ulMask_</span></span>
  
> <span data-ttu-id="e9c06-121">Часть состояния подключения, который был изменен.</span><span class="sxs-lookup"><span data-stu-id="e9c06-121">The part of the connection state that has changed.</span></span> <span data-ttu-id="e9c06-122">Поддерживается только значение — MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="e9c06-122">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="e9c06-123">_ulStateOld_</span><span class="sxs-lookup"><span data-stu-id="e9c06-123">_ulStateOld_</span></span>
  
> <span data-ttu-id="e9c06-124">Старый состояние подключения.</span><span class="sxs-lookup"><span data-stu-id="e9c06-124">The old connection state.</span></span> <span data-ttu-id="e9c06-125">Поддерживаются только поддерживаемые значения:</span><span class="sxs-lookup"><span data-stu-id="e9c06-125">The only supported values are:</span></span>
    
   - <span data-ttu-id="e9c06-126">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="e9c06-126">MAPIOFFLINE_STATE_OFFLINE</span></span>
    
   - <span data-ttu-id="e9c06-127">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="e9c06-127">MAPIOFFLINE_STATE_ONLINE</span></span>
    
 <span data-ttu-id="e9c06-128">_ulStateNew_</span><span class="sxs-lookup"><span data-stu-id="e9c06-128">_ulStateNew_</span></span>
  
> <span data-ttu-id="e9c06-129">Новое состояние подключения.</span><span class="sxs-lookup"><span data-stu-id="e9c06-129">The new connection state.</span></span> <span data-ttu-id="e9c06-130">Поддерживаются только поддерживаемые значения:</span><span class="sxs-lookup"><span data-stu-id="e9c06-130">The only supported values are:</span></span>
    
   - <span data-ttu-id="e9c06-131">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="e9c06-131">MAPIOFFLINE_STATE_OFFLINE</span></span>
    
   - <span data-ttu-id="e9c06-132">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="e9c06-132">MAPIOFFLINE_STATE_ONLINE</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e9c06-133">Замечания</span><span class="sxs-lookup"><span data-stu-id="e9c06-133">Remarks</span></span>

<span data-ttu-id="e9c06-134">Автономные состояния API поддерживает только уведомления онлайновом/интерактивном режиме изменения.</span><span class="sxs-lookup"><span data-stu-id="e9c06-134">The Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="e9c06-135">Клиент должен проверить, что Outlook возвращает следующие значения перед изучением реальное изменение:</span><span class="sxs-lookup"><span data-stu-id="e9c06-135">A client must check that Outlook returns the following values before examining the actual change:</span></span>
  
1.  <span data-ttu-id="e9c06-136">*NotifyType* имеет значение MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE или MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE.</span><span class="sxs-lookup"><span data-stu-id="e9c06-136">*NotifyType*  has the value MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE, or MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE.</span></span> <span data-ttu-id="e9c06-137">В этом случае клиента можно предполагается, что изменения — это изменение состояния подключения и *информация* является структуры *StateChange используется* .</span><span class="sxs-lookup"><span data-stu-id="e9c06-137">In this case, the client can assume that the change is a connection state change, and  *Info*  is of the structure  *StateChange*  .</span></span> 
    
2.  <span data-ttu-id="e9c06-138">*ulMask* имеет значение MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="e9c06-138">*ulMask*  has the value MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span> <span data-ttu-id="e9c06-139">В этом случае клиент может предполагается, что изменения изменение состояния онлайновом/интерактивном режиме подключения и можно перейти с проверки *ulStateOld* и *ulStateNew* .</span><span class="sxs-lookup"><span data-stu-id="e9c06-139">In this case, the client can assume that the change is an online/offline connection state change, and can proceed with examining  *ulStateOld*  and  *ulStateNew*  .</span></span> 
    
<span data-ttu-id="e9c06-140">Существует возможность, что Outlook уведомляет клиента о других изменений, которые не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="e9c06-140">It is possible that Outlook notifies a client of other changes that are not supported.</span></span> <span data-ttu-id="e9c06-141">В таких случаях одно из трех значений, уже было указано ранее, не приведет к *NotifyType* или *ulMask* не будет MAPIOFFLINE_STATE_OFFLINE_MASK и клиента необходимо игнорировать остальную часть данных в *сведения* .</span><span class="sxs-lookup"><span data-stu-id="e9c06-141">In such cases,  *NotifyType*  would not be any one of the three values stated previously, or  *ulMask*  would not be MAPIOFFLINE_STATE_OFFLINE_MASK, and the client must ignore the rest of the data in  *Info*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e9c06-142">См. также</span><span class="sxs-lookup"><span data-stu-id="e9c06-142">See also</span></span>

- [<span data-ttu-id="e9c06-143">Сведения об API автономного состояния</span><span class="sxs-lookup"><span data-stu-id="e9c06-143">About the Offline State API</span></span>](about-the-offline-state-api.md)  
- [<span data-ttu-id="e9c06-144">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="e9c06-144">MAPI Constants</span></span>](mapi-constants.md)  
- [<span data-ttu-id="e9c06-145">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="e9c06-145">MAPIOFFLINE_NOTIFY_TYPE</span></span>](mapioffline_notify_type.md)

