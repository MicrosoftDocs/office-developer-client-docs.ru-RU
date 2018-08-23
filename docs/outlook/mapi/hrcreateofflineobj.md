---
title: HrCreateOfflineObj
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 04d57c1d-ce91-42ce-9f0f-00563092f6f4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f86266f192ffb1c86ca48f0fd5f99559737a9e76
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576486"
---
# <a name="hrcreateofflineobj"></a><span data-ttu-id="4fed8-103">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="4fed8-103">HrCreateOfflineObj</span></span>

<span data-ttu-id="4fed8-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fed8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="4fed8-105">Создает объект автономной MAPI, используемый поставщиком и хранилища для уведомления MAPI после выхода автономный режим и Интернет-версия</span><span class="sxs-lookup"><span data-stu-id="4fed8-105">Creates a MAPI offline object that is used by the provider and store in order to notify MAPI when the object goes online and offline,</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4fed8-106">Экспортировать с:</span><span class="sxs-lookup"><span data-stu-id="4fed8-106">Exported by:</span></span>  <br/> |<span data-ttu-id="4fed8-107">Msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="4fed8-107">Msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="4fed8-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="4fed8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4fed8-109">Outlook</span><span class="sxs-lookup"><span data-stu-id="4fed8-109">Outlook</span></span>  <br/> |
|<span data-ttu-id="4fed8-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="4fed8-110">Called by:</span></span>  <br/> |<span data-ttu-id="4fed8-111">Клиент</span><span class="sxs-lookup"><span data-stu-id="4fed8-111">Client</span></span>  <br/> |
   
```cpp
STDAPI HrCreateOfflineObj(
ULONG ulFlags,
MAPIOFFLINE_CREATEINFO* pCreateInfo,
IMAPIOfflineMgr** ppOffline
);
```

## <a name="parameters"></a><span data-ttu-id="4fed8-112">���������</span><span class="sxs-lookup"><span data-stu-id="4fed8-112">Parameters</span></span>

<span data-ttu-id="4fed8-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4fed8-113">_ulFlags_</span></span>
  
> <span data-ttu-id="4fed8-114">[in] Он должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="4fed8-114">[in] It must be 0.</span></span>
    
<span data-ttu-id="4fed8-115">_pCreateInfo_</span><span class="sxs-lookup"><span data-stu-id="4fed8-115">_pCreateInfo_</span></span>
  
> <span data-ttu-id="4fed8-116">[in] Указатель на структуру **MAPIOFFLINE_CREATEINFO** , который содержит сведения, необходимые для создания автономного объекта.</span><span class="sxs-lookup"><span data-stu-id="4fed8-116">[in] A pointer to a **MAPIOFFLINE_CREATEINFO** structure that contains the information needed to create the offline object.</span></span> 
    
<span data-ttu-id="4fed8-117">_ppOffline_</span><span class="sxs-lookup"><span data-stu-id="4fed8-117">_ppOffline_</span></span>
  
> <span data-ttu-id="4fed8-118">[out] Указатель на интерфейс **IMAPIOfflineMgr** .</span><span class="sxs-lookup"><span data-stu-id="4fed8-118">[out] A pointer to the **IMAPIOfflineMgr** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4fed8-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4fed8-119">Return value</span></span>

<span data-ttu-id="4fed8-120">Нет.</span><span class="sxs-lookup"><span data-stu-id="4fed8-120">None.</span></span>
  
<span data-ttu-id="4fed8-121">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="4fed8-121">HrOpenOfflineObj</span></span>
  
## <a name="example"></a><span data-ttu-id="4fed8-122">Пример</span><span class="sxs-lookup"><span data-stu-id="4fed8-122">Example</span></span>

```cpp
// create/get global offline object to use as parent.
 ZeroMemory(&OfflineCreateInfo, sizeof(OfflineCreateInfo));
  OfflineCreateInfo.ulSize = sizeof(OfflineCreateInfo);
  OfflineCreateInfo.ulCreateFlags = 0;
  OfflineCreateInfo.pwszProfileName = pszProfileName;
  OfflineCreateInfo.ulCapabilities = ulCapabilities;
  OfflineCreateInfo.pGUID = &GUID_GlobalState;
  OfflineCreateInfo.pInstance = NULL;
  OfflineCreateInfo.pParent = NULL;
  OfflineCreateInfo.pMAPISupport = NULL;
  OfflineCreateInfo.pAggregateInfo = NULL;
  OfflineCreateInfo.pConnectInfo = NULL;
// Create an offline object for the provider with global as parent.
  ZeroMemory(&OfflineCreateInfo, sizeof(OfflineCreateInfo));
  OfflineCreateInfo.ulSize = sizeof(OfflineCreateInfo);
  OfflineCreateInfo.ulCreateFlags = 0;
  OfflineCreateInfo.pwszProfileName = pszProfileName;
  OfflineCreateInfo.ulCapabilities = ulCapabilities;
  OfflineCreateInfo.pGUID = pGuid;
  OfflineCreateInfo.pInstance = pInstance;
  OfflineCreateInfo.pParent = pGlobalOfflineMgr;
  OfflineCreateInfo.pMAPISupport = NULL;
  OfflineCreateInfo.pAggregateInfo = NULL;
  OfflineCreateInfo.pConnectInfo = NULL;
  // create store offline object which aggregates with the store object and has provider offline object as parent.
  ZeroMemory(&OfflineCreateInfo, sizeof(OfflineCreateInfo));
  OfflineCreateInfo.ulSize = sizeof(OfflineCreateInfo);
  OfflineCreateInfo.ulCreateFlags = 0;
  OfflineCreateInfo.pwszProfileName = pszProfileName;
  OfflineCreateInfo.ulCapabilities = ulCapabilities;
  OfflineCreateInfo.pGUID = NULL;
  OfflineCreateInfo.pInstance = NULL;
  OfflineCreateInfo.pParent = m_pProviderOfflineMgr;
  OfflineCreateInfo.pMAPISupport = pMAPISup;
  OfflineCreateInfo.pAggregateInfo = &AggregateInfo;
  OfflineCreateInfo.pConnectInfo = NULL;
  ZeroMemory(&AggregateInfo, sizeof(AggregateInfo));
  AggregateInfo.ulSize = sizeof(AggregateInfo);
  AggregateInfo.pOuterObj = (IMsgStore *)this;
  AggregateInfo.pRefTrackRoot = NULL;

```

## <a name="see-also"></a><span data-ttu-id="4fed8-123">См. также</span><span class="sxs-lookup"><span data-stu-id="4fed8-123">See also</span></span>

- [<span data-ttu-id="4fed8-124">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="4fed8-124">MAPIOFFLINE_AGGREGATEINFO</span></span>](mapioffline_aggregateinfo.md)
- [<span data-ttu-id="4fed8-125">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="4fed8-125">MAPIOFFLINE_CREATEINFO</span></span>](mapioffline_createinfo.md)

