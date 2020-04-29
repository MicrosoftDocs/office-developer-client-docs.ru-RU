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
# <a name="mapioffline_createinfo"></a><span data-ttu-id="5b24a-103">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="5b24a-103">MAPIOFFLINE_CREATEINFO</span></span>

  
  
<span data-ttu-id="5b24a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b24a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b24a-105">Эта структура используется с [хркреатеоффлинеобж](hrcreateofflineobj.md).</span><span class="sxs-lookup"><span data-stu-id="5b24a-105">This structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span>
  
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

## <a name="members"></a><span data-ttu-id="5b24a-106">"Участники"</span><span class="sxs-lookup"><span data-stu-id="5b24a-106">Members</span></span>

 <span data-ttu-id="5b24a-107">**улсизе**</span><span class="sxs-lookup"><span data-stu-id="5b24a-107">**ulSize**</span></span>
  
> <span data-ttu-id="5b24a-108">Размер структуры.</span><span class="sxs-lookup"><span data-stu-id="5b24a-108">The size of structure.</span></span>
    
 <span data-ttu-id="5b24a-109">**улкреатефлагс**</span><span class="sxs-lookup"><span data-stu-id="5b24a-109">**ulCreateFlags**</span></span>
  
> <span data-ttu-id="5b24a-110">Значение должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="5b24a-110">It must be 0.</span></span>
    
 <span data-ttu-id="5b24a-111">**пвсзпрофиленаме**</span><span class="sxs-lookup"><span data-stu-id="5b24a-111">**pwszProfileName**</span></span>
  
> <span data-ttu-id="5b24a-112">Имя профиля.</span><span class="sxs-lookup"><span data-stu-id="5b24a-112">The name of the profile.</span></span>
    
 <span data-ttu-id="5b24a-113">**улкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="5b24a-113">**ulCapabilities**</span></span>
  
> <span data-ttu-id="5b24a-114">Битовая маска следующих флагов возможностей.</span><span class="sxs-lookup"><span data-stu-id="5b24a-114">A bit mask of the following capability flags.</span></span>
    
|||
|:-----|:-----|
|<span data-ttu-id="5b24a-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="5b24a-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>  <br/> |<span data-ttu-id="5b24a-116">Автономный объект способен переходить в автономный режим.</span><span class="sxs-lookup"><span data-stu-id="5b24a-116">The offline object is capable of going offline.</span></span>  <br/> |
|<span data-ttu-id="5b24a-117">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="5b24a-117">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>  <br/> |<span data-ttu-id="5b24a-118">Автономный объект способен работать в сети.</span><span class="sxs-lookup"><span data-stu-id="5b24a-118">The offline object is capable of going online.</span></span>  <br/> |
   
 <span data-ttu-id="5b24a-119">**пгуид**</span><span class="sxs-lookup"><span data-stu-id="5b24a-119">**pGUID**</span></span>
  
> <span data-ttu-id="5b24a-120">Указатель на GUID, используемый для уникальной идентификации этого типа автономных объектов из других автономных объектов.</span><span class="sxs-lookup"><span data-stu-id="5b24a-120">Pointer to a GUID that is used to uniquely identify this type of offline object from other offline objects.</span></span> <span data-ttu-id="5b24a-121">GUID_GlobalState относится к глобальному автономному объекту, который объекты могут использовать в качестве родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="5b24a-121">GUID_GlobalState refers to the global offline object that objects can use as a parent object.</span></span>
    
 <span data-ttu-id="5b24a-122">**пинстанце**</span><span class="sxs-lookup"><span data-stu-id="5b24a-122">**pInstance**</span></span>
  
> <span data-ttu-id="5b24a-123">Указатель на GUID, который уникально идентифицирует данный автономный объект.</span><span class="sxs-lookup"><span data-stu-id="5b24a-123">Pointer to GUID that uniquely identifies this offline object.</span></span> <span data-ttu-id="5b24a-124">Он используется для определения неоднозначности автономных объектов из других объектов.</span><span class="sxs-lookup"><span data-stu-id="5b24a-124">It is used to disambiguate this offline objects from other objects.</span></span>
    
 <span data-ttu-id="5b24a-125">**ппарент**</span><span class="sxs-lookup"><span data-stu-id="5b24a-125">**pParent**</span></span>
  
> <span data-ttu-id="5b24a-126">Указатель на автономный объект, который является родительским для этого автономного объекта и изменения, которые наследуются этим автономным объектом.</span><span class="sxs-lookup"><span data-stu-id="5b24a-126">Pointer to offline object that is the parent of this offline object and whose changes this offline object will inherit.</span></span>
    
 <span data-ttu-id="5b24a-127">**пмаписуппорт**</span><span class="sxs-lookup"><span data-stu-id="5b24a-127">**pMAPISupport**</span></span>
  
>  <span data-ttu-id="5b24a-128">Определяет объект поддержки MAPI, который будет использовать этот автономный объект.</span><span class="sxs-lookup"><span data-stu-id="5b24a-128">Identifies the MAPI support object that that will use this offline object.</span></span> <span data-ttu-id="5b24a-129">Например, если этот автономный объект используется для отслеживания состояния автономного и Интернет-хранилища, то это объект поддержки хранилищ.</span><span class="sxs-lookup"><span data-stu-id="5b24a-129">For example, if this offline object is used to keep track of a store's offline and online state, then this is the stores support object.</span></span> <span data-ttu-id="5b24a-130">Однако если это автономный объект для объекта без объекта support, он может иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="5b24a-130">However, if this is an offline object for an object with no support object then it can be NULL.</span></span> 
    
 <span data-ttu-id="5b24a-131">**паггрегатеинфо**</span><span class="sxs-lookup"><span data-stu-id="5b24a-131">**pAggregateInfo**</span></span>
  
> <span data-ttu-id="5b24a-132">Указатель на структуру MAPIOFFLINE_AGGREGATEINFO.</span><span class="sxs-lookup"><span data-stu-id="5b24a-132">A pointer to a MAPIOFFLINE_AGGREGATEINFO structure.</span></span> <span data-ttu-id="5b24a-133">Дополнительные сведения см. в разделе [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).</span><span class="sxs-lookup"><span data-stu-id="5b24a-133">For more information, see [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).</span></span>
    
 <span data-ttu-id="5b24a-134">**пконнектинфо**</span><span class="sxs-lookup"><span data-stu-id="5b24a-134">**pConnectInfo**</span></span>
  
> <span data-ttu-id="5b24a-135">Должно иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="5b24a-135">Must be null.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5b24a-136">См. также</span><span class="sxs-lookup"><span data-stu-id="5b24a-136">See also</span></span>



[<span data-ttu-id="5b24a-137">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="5b24a-137">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="5b24a-138">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="5b24a-138">MAPIOFFLINE_AGGREGATEINFO</span></span>](mapioffline_aggregateinfo.md)

