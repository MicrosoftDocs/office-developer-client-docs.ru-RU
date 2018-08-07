---
title: IMsgServiceAdminMsgServiceTransportOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.MsgServiceTransportOrder
api_type:
- COM
ms.assetid: c57ada0e-b9a1-496b-8548-75686d8cba4e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5b96a45bab4cd00d23604d0b0b25f3e772277395
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809372"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a><span data-ttu-id="cfb70-103">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="cfb70-103">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>

  
  
<span data-ttu-id="cfb70-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cfb70-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cfb70-105">Задает порядок вызова поставщиков какие транспорта доставить сообщение.</span><span class="sxs-lookup"><span data-stu-id="cfb70-105">Sets the order in which transport providers are called to deliver a message.</span></span>
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a><span data-ttu-id="cfb70-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cfb70-106">Parameters</span></span>

 <span data-ttu-id="cfb70-107">_cUID_</span><span class="sxs-lookup"><span data-stu-id="cfb70-107">_cUID_</span></span>
  
> <span data-ttu-id="cfb70-108">[in] Число уникальных идентификаторов с помощью параметра _lpUIDList_ .</span><span class="sxs-lookup"><span data-stu-id="cfb70-108">[in] The count of unique identifiers in the  _lpUIDList_ parameter.</span></span> 
    
 <span data-ttu-id="cfb70-109">_lpUIDList_</span><span class="sxs-lookup"><span data-stu-id="cfb70-109">_lpUIDList_</span></span>
  
> <span data-ttu-id="cfb70-110">[in] Указатель на массив уникальные идентификаторы, представляющие поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="cfb70-110">[in] A pointer to an array of unique identifiers that represent transport providers.</span></span> <span data-ttu-id="cfb70-111">Массив содержит один идентификатор для каждого поставщика транспорта, настроенных в текущий профиль.</span><span class="sxs-lookup"><span data-stu-id="cfb70-111">The array contains one identifier for each transport provider configured in the current profile.</span></span>
    
 <span data-ttu-id="cfb70-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cfb70-112">_ulFlags_</span></span>
  
> <span data-ttu-id="cfb70-113">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="cfb70-113">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cfb70-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4">Return value</span></span>

<span data-ttu-id="cfb70-115">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="cfb70-115">S_OK</span></span> 
  
> <span data-ttu-id="cfb70-116">Порядок транспорта успешно установлены.</span><span class="sxs-lookup"><span data-stu-id="cfb70-116">The transport order was set successfully.</span></span>
    
<span data-ttu-id="cfb70-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="cfb70-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="cfb70-118">Значение параметра _cUID_ отличается от числа поставщиками транспорта фактически в профиле.</span><span class="sxs-lookup"><span data-stu-id="cfb70-118">The value in the  _cUID_ parameter differs from the number of transport providers actually in the profile.</span></span> 
    
<span data-ttu-id="cfb70-119">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="cfb70-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="cfb70-120">Одно или несколько из структур [MAPIUID](mapiuid.md) , переданной в параметре _lpUIDList_ относится к поставщика транспорта в настоящее время в профиле.</span><span class="sxs-lookup"><span data-stu-id="cfb70-120">One or more of the [MAPIUID](mapiuid.md) structures passed in the  _lpUIDList_ parameter do not refer to a transport provider currently in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cfb70-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="cfb70-121">Remarks</span></span>

<span data-ttu-id="cfb70-122">Метод **IMsgServiceAdmin::MsgServiceTransportOrder** задает порядок доставки поставщиками транспорта в профиле.</span><span class="sxs-lookup"><span data-stu-id="cfb70-122">The **IMsgServiceAdmin::MsgServiceTransportOrder** method sets the delivery order of transport providers in a profile.</span></span> <span data-ttu-id="cfb70-123">Параметр _lpUIDList_ должен содержать отсортированный список идентификаторов запись поставщика транспорта, полученного из свойства **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) в таблице, возвращенный из [IMsgServiceAdmin:: GetProviderTable](imsgserviceadmin-getprovidertable.md) метод.</span><span class="sxs-lookup"><span data-stu-id="cfb70-123">The  _lpUIDList_ parameter must contain a sorted list of transport-provider entry identifiers obtained from the **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) property of the table returned from the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="cfb70-124">Клиентское приложение должно передавать полный список в _lpUIDList_.</span><span class="sxs-lookup"><span data-stu-id="cfb70-124">A client application must pass the complete list in  _lpUIDList_.</span></span>
  
 <span data-ttu-id="cfb70-125">**SetTransportOrder** переопределений транспорта параметры поставщика, такие как флаг STATUS_XP_PREFER_LAST в свойстве **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="cfb70-125">**SetTransportOrder** overrides transport provider preferences such as the STATUS_XP_PREFER_LAST flag set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cfb70-126">См. также</span><span class="sxs-lookup"><span data-stu-id="cfb70-126">See also</span></span>



[<span data-ttu-id="cfb70-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="cfb70-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="cfb70-128">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cfb70-128">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

