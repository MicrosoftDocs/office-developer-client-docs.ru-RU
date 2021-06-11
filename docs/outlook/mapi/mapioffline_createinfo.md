---
title: MAPIOFFLINE_CREATEINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 539aa31d-7dec-4dbb-93f7-fa060c43565a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a9b11b134f5d4a32a5a55008f557821d74b474bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429567"
---
# <a name="mapioffline_createinfo"></a><span data-ttu-id="b1fe8-103">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="b1fe8-103">MAPIOFFLINE_CREATEINFO</span></span>

  
  
<span data-ttu-id="b1fe8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1fe8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1fe8-105">Эта структура используется в [HrCreateOfflineObj](hrcreateofflineobj.md).</span><span class="sxs-lookup"><span data-stu-id="b1fe8-105">This structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span>
  
```cpp
typedef struct
{
  ULONG      ulSize;
  ULONG      ulCreateFlags;
  LPCWSTR      pwszProfileName;
  ULONG      ulCapabilities;
  const GUID*      pGUID;
  const GUID*      pInstance;
  IMAPIOfflineMgr*    pParent;
  IUnknown*      pMAPISupport;
  MAPIOFFLINE_AGGREGATEINFO*  pAggregateInfo;
  MAPIOFFLINE_CONNECTINFO*  pConnectInfo;
} MAPIOFFLINE_CREATEINFO;
```

## <a name="members"></a><span data-ttu-id="b1fe8-106">"Участники"</span><span class="sxs-lookup"><span data-stu-id="b1fe8-106">Members</span></span>

 <span data-ttu-id="b1fe8-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="b1fe8-107">**ulSize**</span></span>
  
> <span data-ttu-id="b1fe8-108">Размер структуры.</span><span class="sxs-lookup"><span data-stu-id="b1fe8-108">The size of structure.</span></span>
    
 <span data-ttu-id="b1fe8-109">**ulCreateFlags**</span><span class="sxs-lookup"><span data-stu-id="b1fe8-109">**ulCreateFlags**</span></span>
  
> <span data-ttu-id="b1fe8-110">Должно быть 0.</span><span class="sxs-lookup"><span data-stu-id="b1fe8-110">It must be 0.</span></span>
    
 <span data-ttu-id="b1fe8-111">**pwszProfileName**</span><span class="sxs-lookup"><span data-stu-id="b1fe8-111">**pwszProfileName**</span></span>
  
> <span data-ttu-id="b1fe8-112">Имя профиля.</span><span class="sxs-lookup"><span data-stu-id="b1fe8-112">The name of the profile.</span></span>
    
 <span data-ttu-id="b1fe8-113">**ulCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b1fe8-113">**ulCapabilities**</span></span>
  
> <span data-ttu-id="b1fe8-114">Немного маски из следующих флагов возможностей.</span><span class="sxs-lookup"><span data-stu-id="b1fe8-114">A bit mask of the following capability flags.</span></span>
    
|||
|:-----|:-----|
|<span data-ttu-id="b1fe8-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="b1fe8-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>  <br/> |<span data-ttu-id="b1fe8-116">Автономный объект может работать в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="b1fe8-116">The offline object is capable of going offline.</span></span>  <br/> |
|<span data-ttu-id="b1fe8-117">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="b1fe8-117">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>  <br/> |<span data-ttu-id="b1fe8-118">Автономный объект может работать в Интернете.</span><span class="sxs-lookup"><span data-stu-id="b1fe8-118">The offline object is capable of going online.</span></span>  <br/> |
   
 <span data-ttu-id="b1fe8-119">**pGUID**</span><span class="sxs-lookup"><span data-stu-id="b1fe8-119">**pGUID**</span></span>
  
> <span data-ttu-id="b1fe8-120">Указатель на GUID, который используется для уникальной идентификации этого типа автономного объекта из других автономных объектов.</span><span class="sxs-lookup"><span data-stu-id="b1fe8-120">Pointer to a GUID that is used to uniquely identify this type of offline object from other offline objects.</span></span> <span data-ttu-id="b1fe8-121">GUID_GlobalState относится к глобальному автономному объекту, который объекты могут использовать в качестве родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="b1fe8-121">GUID_GlobalState refers to the global offline object that objects can use as a parent object.</span></span>
    
 <span data-ttu-id="b1fe8-122">**pInstance**</span><span class="sxs-lookup"><span data-stu-id="b1fe8-122">**pInstance**</span></span>
  
> <span data-ttu-id="b1fe8-123">Указатель на GUID, который уникально определяет этот автономный объект.</span><span class="sxs-lookup"><span data-stu-id="b1fe8-123">Pointer to GUID that uniquely identifies this offline object.</span></span> <span data-ttu-id="b1fe8-124">Он используется для неосмысленности этого автономного объекта от других объектов.</span><span class="sxs-lookup"><span data-stu-id="b1fe8-124">It is used to disambiguate this offline objects from other objects.</span></span>
    
 <span data-ttu-id="b1fe8-125">**pParent**</span><span class="sxs-lookup"><span data-stu-id="b1fe8-125">**pParent**</span></span>
  
> <span data-ttu-id="b1fe8-126">Указатель на автономный объект, который является родителем этого автономного объекта и изменения которого этот автономный объект будет наследовать.</span><span class="sxs-lookup"><span data-stu-id="b1fe8-126">Pointer to offline object that is the parent of this offline object and whose changes this offline object will inherit.</span></span>
    
 <span data-ttu-id="b1fe8-127">**pMAPISupport**</span><span class="sxs-lookup"><span data-stu-id="b1fe8-127">**pMAPISupport**</span></span>
  
>  <span data-ttu-id="b1fe8-128">Определяет объект поддержки MAPI, который будет использовать этот автономный объект.</span><span class="sxs-lookup"><span data-stu-id="b1fe8-128">Identifies the MAPI support object that that will use this offline object.</span></span> <span data-ttu-id="b1fe8-129">Например, если этот автономный объект используется для отслеживания состояния автономного и сетевого состояния магазина, то это объект поддержки магазинов.</span><span class="sxs-lookup"><span data-stu-id="b1fe8-129">For example, if this offline object is used to keep track of a store's offline and online state, then this is the stores support object.</span></span> <span data-ttu-id="b1fe8-130">Однако, если это автономный объект для объекта без объекта поддержки, он может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="b1fe8-130">However, if this is an offline object for an object with no support object then it can be NULL.</span></span> 
    
 <span data-ttu-id="b1fe8-131">**pAggregateInfo**</span><span class="sxs-lookup"><span data-stu-id="b1fe8-131">**pAggregateInfo**</span></span>
  
> <span data-ttu-id="b1fe8-132">Указатель на структуру MAPIOFFLINE_AGGREGATEINFO.</span><span class="sxs-lookup"><span data-stu-id="b1fe8-132">A pointer to a MAPIOFFLINE_AGGREGATEINFO structure.</span></span> <span data-ttu-id="b1fe8-133">Дополнительные сведения см. [в MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).</span><span class="sxs-lookup"><span data-stu-id="b1fe8-133">For more information, see [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).</span></span>
    
 <span data-ttu-id="b1fe8-134">**pConnectInfo**</span><span class="sxs-lookup"><span data-stu-id="b1fe8-134">**pConnectInfo**</span></span>
  
> <span data-ttu-id="b1fe8-135">Должно быть null.</span><span class="sxs-lookup"><span data-stu-id="b1fe8-135">Must be null.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b1fe8-136">См. также</span><span class="sxs-lookup"><span data-stu-id="b1fe8-136">See also</span></span>



[<span data-ttu-id="b1fe8-137">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="b1fe8-137">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="b1fe8-138">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="b1fe8-138">MAPIOFFLINE_AGGREGATEINFO</span></span>](mapioffline_aggregateinfo.md)

