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
ms.openlocfilehash: ffac4328401b8afbc07eb650ea6c08da5f9c51b2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594497"
---
# <a name="mapiofflinecreateinfo"></a><span data-ttu-id="83769-103">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="83769-103">MAPIOFFLINE_CREATEINFO</span></span>

  
  
<span data-ttu-id="83769-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83769-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83769-105">Эта структура используется с [HrCreateOfflineObj](hrcreateofflineobj.md).</span><span class="sxs-lookup"><span data-stu-id="83769-105">This structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span>
  
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

## <a name="members"></a><span data-ttu-id="83769-106">Members</span><span class="sxs-lookup"><span data-stu-id="83769-106">Members</span></span>

 <span data-ttu-id="83769-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="83769-107">**ulSize**</span></span>
  
> <span data-ttu-id="83769-108">Размер структуры.</span><span class="sxs-lookup"><span data-stu-id="83769-108">The size of structure.</span></span>
    
 <span data-ttu-id="83769-109">**ulCreateFlags**</span><span class="sxs-lookup"><span data-stu-id="83769-109">**ulCreateFlags**</span></span>
  
> <span data-ttu-id="83769-110">Он должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="83769-110">It must be 0.</span></span>
    
 <span data-ttu-id="83769-111">**pwszProfileName**</span><span class="sxs-lookup"><span data-stu-id="83769-111">**pwszProfileName**</span></span>
  
> <span data-ttu-id="83769-112">Имя профиля.</span><span class="sxs-lookup"><span data-stu-id="83769-112">The name of the profile.</span></span>
    
 <span data-ttu-id="83769-113">**ulCapabilities**</span><span class="sxs-lookup"><span data-stu-id="83769-113">**ulCapabilities**</span></span>
  
> <span data-ttu-id="83769-114">Битовая маска следующие флаги возможностей.</span><span class="sxs-lookup"><span data-stu-id="83769-114">A bit mask of the following capability flags.</span></span>
    
|||
|:-----|:-----|
|<span data-ttu-id="83769-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="83769-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>  <br/> |<span data-ttu-id="83769-116">Автономные объекта можно перейти в автономный режим.</span><span class="sxs-lookup"><span data-stu-id="83769-116">The offline object is capable of going offline.</span></span>  <br/> |
|<span data-ttu-id="83769-117">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="83769-117">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>  <br/> |<span data-ttu-id="83769-118">Автономные объект способен подключение.</span><span class="sxs-lookup"><span data-stu-id="83769-118">The offline object is capable of going online.</span></span>  <br/> |
   
 <span data-ttu-id="83769-119">**pGUID**</span><span class="sxs-lookup"><span data-stu-id="83769-119">**pGUID**</span></span>
  
> <span data-ttu-id="83769-120">Указатель на идентификатор GUID, который используется для уникальной идентификации этого типа автономных объектов из других автономных объектов.</span><span class="sxs-lookup"><span data-stu-id="83769-120">Pointer to a GUID that is used to uniquely identify this type of offline object from other offline objects.</span></span> <span data-ttu-id="83769-121">GUID_GlobalState ссылается на глобальный объект автономной, объекты можно использовать в качестве родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="83769-121">GUID_GlobalState refers to the global offline object that objects can use as a parent object.</span></span>
    
 <span data-ttu-id="83769-122">**pInstance**</span><span class="sxs-lookup"><span data-stu-id="83769-122">**pInstance**</span></span>
  
> <span data-ttu-id="83769-123">Указатель на идентификатор GUID, который уникальным образом определяет автономной объект.</span><span class="sxs-lookup"><span data-stu-id="83769-123">Pointer to GUID that uniquely identifies this offline object.</span></span> <span data-ttu-id="83769-124">Он используется для однозначного определения этой автономной объектов из других объектов.</span><span class="sxs-lookup"><span data-stu-id="83769-124">It is used to disambiguate this offline objects from other objects.</span></span>
    
 <span data-ttu-id="83769-125">**pParent**</span><span class="sxs-lookup"><span data-stu-id="83769-125">**pParent**</span></span>
  
> <span data-ttu-id="83769-126">Указатель автономной объект, являющийся родительским объектом автономной, для которых будет наследовать этот объект автономные изменения.</span><span class="sxs-lookup"><span data-stu-id="83769-126">Pointer to offline object that is the parent of this offline object and whose changes this offline object will inherit.</span></span>
    
 <span data-ttu-id="83769-127">**pMAPISupport**</span><span class="sxs-lookup"><span data-stu-id="83769-127">**pMAPISupport**</span></span>
  
>  <span data-ttu-id="83769-128">Определяет, что этот автономной объект, который будет использовать объект поддержки MAPI.</span><span class="sxs-lookup"><span data-stu-id="83769-128">Identifies the MAPI support object that that will use this offline object.</span></span> <span data-ttu-id="83769-129">К примеру при автономной объект используется для отслеживания в хранилище автономный режим и состояние online, то это магазины поддержки объекта.</span><span class="sxs-lookup"><span data-stu-id="83769-129">For example, if this offline object is used to keep track of a store's offline and online state, then this is the stores support object.</span></span> <span data-ttu-id="83769-130">Тем не менее если это автономные объект для объекта с помощью объекта без поддержки затем она может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="83769-130">However, if this is an offline object for an object with no support object then it can be NULL.</span></span> 
    
 <span data-ttu-id="83769-131">**pAggregateInfo**</span><span class="sxs-lookup"><span data-stu-id="83769-131">**pAggregateInfo**</span></span>
  
> <span data-ttu-id="83769-132">Указатель на структуру MAPIOFFLINE_AGGREGATEINFO.</span><span class="sxs-lookup"><span data-stu-id="83769-132">A pointer to a MAPIOFFLINE_AGGREGATEINFO structure.</span></span> <span data-ttu-id="83769-133">Для получения дополнительных сведений см [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).</span><span class="sxs-lookup"><span data-stu-id="83769-133">For more information, see [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).</span></span>
    
 <span data-ttu-id="83769-134">**pConnectInfo**</span><span class="sxs-lookup"><span data-stu-id="83769-134">**pConnectInfo**</span></span>
  
> <span data-ttu-id="83769-135">Должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="83769-135">Must be null.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="83769-136">См. также</span><span class="sxs-lookup"><span data-stu-id="83769-136">See also</span></span>



[<span data-ttu-id="83769-137">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="83769-137">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="83769-138">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="83769-138">MAPIOFFLINE_AGGREGATEINFO</span></span>](mapioffline_aggregateinfo.md)

