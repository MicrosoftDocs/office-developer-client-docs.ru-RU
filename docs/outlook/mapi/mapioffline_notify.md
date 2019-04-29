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
# <a name="mapiofflinenotify"></a><span data-ttu-id="1e148-103">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="1e148-103">MAPIOFFLINE_NOTIFY</span></span>

<span data-ttu-id="1e148-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e148-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e148-105">Это уведомление об изменении состояния подключения.</span><span class="sxs-lookup"><span data-stu-id="1e148-105">This is the notification for a change in the connection state.</span></span> <span data-ttu-id="1e148-106">Он указывает часть состояния подключения, которая изменилась, старое состояние подключения и новое состояние подключения.</span><span class="sxs-lookup"><span data-stu-id="1e148-106">It indicates the part of the connection state that has changed, the old connection state, and the new connection state.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1e148-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="1e148-107">Quick info</span></span>

<span data-ttu-id="1e148-108">Обратитесь к разделу **[имапиоффлиненотифи](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="1e148-108">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
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

## <a name="members"></a><span data-ttu-id="1e148-109">Members</span><span class="sxs-lookup"><span data-stu-id="1e148-109">Members</span></span>

 <span data-ttu-id="1e148-110">_Улсизе_</span><span class="sxs-lookup"><span data-stu-id="1e148-110">_ulSize_</span></span>
  
> <span data-ttu-id="1e148-111">Размер структуры **мапиоффлине_нотифи** .</span><span class="sxs-lookup"><span data-stu-id="1e148-111">Size of the **MAPIOFFLINE_NOTIFY** structure.</span></span> 
    
 <span data-ttu-id="1e148-112">_Нотифитипе_</span><span class="sxs-lookup"><span data-stu-id="1e148-112">_NotifyType_</span></span>
  
> <span data-ttu-id="1e148-113">Тип уведомления.</span><span class="sxs-lookup"><span data-stu-id="1e148-113">Type of notification.</span></span> <span data-ttu-id="1e148-114">Обратите внимание, что поддерживается только уведомление при изменении состояния подключения; поддерживаются только следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1e148-114">Note that only notification on change of the connection state is supported; the only supported values are:</span></span>
    
   - <span data-ttu-id="1e148-115">МАПИОФФЛИНЕ_НОТИФИ_ТИПЕ_СТАТЕЧАНЖЕ_СТАРТ</span><span class="sxs-lookup"><span data-stu-id="1e148-115">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START</span></span>
    
   - <span data-ttu-id="1e148-116">МАПИОФФЛИНЕ_НОТИФИ_ТИПЕ_СТАТЕЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="1e148-116">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE</span></span>
    
   - <span data-ttu-id="1e148-117">МАПИОФФЛИНЕ_НОТИФИ_ТИПЕ_СТАТЕЧАНЖЕ_ДОНЕ</span><span class="sxs-lookup"><span data-stu-id="1e148-117">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE</span></span>
    
 <span data-ttu-id="1e148-118">_Улклиенттокен_</span><span class="sxs-lookup"><span data-stu-id="1e148-118">_ulClientToken_</span></span>
  
> <span data-ttu-id="1e148-119">Маркер, определенный клиентом в структуре **[мапиоффлине_адвисеинфо](mapioffline_adviseinfo.md)** в **[Имапиоффлинемгр:: Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="1e148-119">A token defined by the client in the **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** structure in **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> 
    
 <span data-ttu-id="1e148-120">_Улмаск_</span><span class="sxs-lookup"><span data-stu-id="1e148-120">_ulMask_</span></span>
  
> <span data-ttu-id="1e148-121">Часть состояния подключения, которая изменилась.</span><span class="sxs-lookup"><span data-stu-id="1e148-121">The part of the connection state that has changed.</span></span> <span data-ttu-id="1e148-122">Единственное поддерживаемое значение — МАПИОФФЛИНЕ_СТАТЕ_ОФФЛИНЕ_МАСК.</span><span class="sxs-lookup"><span data-stu-id="1e148-122">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="1e148-123">_Улстатеолд_</span><span class="sxs-lookup"><span data-stu-id="1e148-123">_ulStateOld_</span></span>
  
> <span data-ttu-id="1e148-124">Старое состояние подключения.</span><span class="sxs-lookup"><span data-stu-id="1e148-124">The old connection state.</span></span> <span data-ttu-id="1e148-125">Поддерживаются только следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1e148-125">The only supported values are:</span></span>
    
   - <span data-ttu-id="1e148-126">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="1e148-126">MAPIOFFLINE_STATE_OFFLINE</span></span>
    
   - <span data-ttu-id="1e148-127">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="1e148-127">MAPIOFFLINE_STATE_ONLINE</span></span>
    
 <span data-ttu-id="1e148-128">_Улстатенев_</span><span class="sxs-lookup"><span data-stu-id="1e148-128">_ulStateNew_</span></span>
  
> <span data-ttu-id="1e148-129">Новое состояние подключения.</span><span class="sxs-lookup"><span data-stu-id="1e148-129">The new connection state.</span></span> <span data-ttu-id="1e148-130">Поддерживаются только следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1e148-130">The only supported values are:</span></span>
    
   - <span data-ttu-id="1e148-131">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="1e148-131">MAPIOFFLINE_STATE_OFFLINE</span></span>
    
   - <span data-ttu-id="1e148-132">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="1e148-132">MAPIOFFLINE_STATE_ONLINE</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1e148-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="1e148-133">Remarks</span></span>

<span data-ttu-id="1e148-134">API автономного состояния поддерживает только уведомления об изменениях в Интернете и в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="1e148-134">The Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="1e148-135">Клиент должен проверить, что Outlook возвращает следующие значения перед изучением фактического изменения:</span><span class="sxs-lookup"><span data-stu-id="1e148-135">A client must check that Outlook returns the following values before examining the actual change:</span></span>
  
1.  <span data-ttu-id="1e148-136">*Нотифитипе* имеет значение МАПИОФФЛИНЕ_НОТИФИ_ТИПЕ_СТАТЕЧАНЖЕ_СТАРТ, МАПИОФФЛИНЕ_НОТИФИ_ТИПЕ_СТАТЕЧАНЖЕ или MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE.</span><span class="sxs-lookup"><span data-stu-id="1e148-136">*NotifyType*  has the value MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE, or MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE.</span></span> <span data-ttu-id="1e148-137">В этом случае клиент может предположить, что изменение является изменением состояния подключения, а *сведения* — с помощью структуры *статечанже* .</span><span class="sxs-lookup"><span data-stu-id="1e148-137">In this case, the client can assume that the change is a connection state change, and  *Info*  is of the structure  *StateChange*  .</span></span> 
    
2.  <span data-ttu-id="1e148-138">*улмаск* имеет значение мапиоффлине_стате_оффлине_маск.</span><span class="sxs-lookup"><span data-stu-id="1e148-138">*ulMask*  has the value MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span> <span data-ttu-id="1e148-139">В этом случае клиент может предположить, что изменение является изменением состояния подключения к сети или сети, и может продолжить изучение *улстатеолд* и *улстатенев* .</span><span class="sxs-lookup"><span data-stu-id="1e148-139">In this case, the client can assume that the change is an online/offline connection state change, and can proceed with examining  *ulStateOld*  and  *ulStateNew*  .</span></span> 
    
<span data-ttu-id="1e148-140">Outlook может уведомить клиента о других неподдерживаемых изменениях.</span><span class="sxs-lookup"><span data-stu-id="1e148-140">It is possible that Outlook notifies a client of other changes that are not supported.</span></span> <span data-ttu-id="1e148-141">В таких случаях *нотифитипе* не будет содержать одно из трех значений, упомянутых выше, или *УЛМАСК* не будет мапиоффлине_стате_оффлине_маск, и клиент должен проигнорировать оставшуюся часть данных в *info* .</span><span class="sxs-lookup"><span data-stu-id="1e148-141">In such cases,  *NotifyType*  would not be any one of the three values stated previously, or  *ulMask*  would not be MAPIOFFLINE_STATE_OFFLINE_MASK, and the client must ignore the rest of the data in  *Info*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1e148-142">См. также</span><span class="sxs-lookup"><span data-stu-id="1e148-142">See also</span></span>

- [<span data-ttu-id="1e148-143">Об API автономного режима</span><span class="sxs-lookup"><span data-stu-id="1e148-143">About the Offline State API</span></span>](about-the-offline-state-api.md)  
- [<span data-ttu-id="1e148-144">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="1e148-144">MAPI Constants</span></span>](mapi-constants.md)  
- [<span data-ttu-id="1e148-145">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="1e148-145">MAPIOFFLINE_NOTIFY_TYPE</span></span>](mapioffline_notify_type.md)

