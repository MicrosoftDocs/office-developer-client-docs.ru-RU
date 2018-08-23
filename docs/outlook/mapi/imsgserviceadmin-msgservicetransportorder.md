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
ms.openlocfilehash: 559f1c609000608d0eb920a0240ac8848e4bc2a7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570795"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a><span data-ttu-id="025d1-103">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="025d1-103">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>

  
  
<span data-ttu-id="025d1-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="025d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="025d1-105">Задает порядок вызова поставщиков какие транспорта доставить сообщение.</span><span class="sxs-lookup"><span data-stu-id="025d1-105">Sets the order in which transport providers are called to deliver a message.</span></span>
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a><span data-ttu-id="025d1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="025d1-106">Parameters</span></span>

 <span data-ttu-id="025d1-107">_cUID_</span><span class="sxs-lookup"><span data-stu-id="025d1-107">_cUID_</span></span>
  
> <span data-ttu-id="025d1-108">[in] Число уникальных идентификаторов с помощью параметра _lpUIDList_ .</span><span class="sxs-lookup"><span data-stu-id="025d1-108">[in] The count of unique identifiers in the  _lpUIDList_ parameter.</span></span> 
    
 <span data-ttu-id="025d1-109">_lpUIDList_</span><span class="sxs-lookup"><span data-stu-id="025d1-109">_lpUIDList_</span></span>
  
> <span data-ttu-id="025d1-110">[in] Указатель на массив уникальные идентификаторы, представляющие поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="025d1-110">[in] A pointer to an array of unique identifiers that represent transport providers.</span></span> <span data-ttu-id="025d1-111">Массив содержит один идентификатор для каждого поставщика транспорта, настроенных в текущий профиль.</span><span class="sxs-lookup"><span data-stu-id="025d1-111">The array contains one identifier for each transport provider configured in the current profile.</span></span>
    
 <span data-ttu-id="025d1-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="025d1-112">_ulFlags_</span></span>
  
> <span data-ttu-id="025d1-113">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="025d1-113">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="025d1-114">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="025d1-114">Return value</span></span>

<span data-ttu-id="025d1-115">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="025d1-115">S_OK</span></span> 
  
> <span data-ttu-id="025d1-116">Порядок транспорта успешно установлены.</span><span class="sxs-lookup"><span data-stu-id="025d1-116">The transport order was set successfully.</span></span>
    
<span data-ttu-id="025d1-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="025d1-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="025d1-118">Значение параметра _cUID_ отличается от числа поставщиками транспорта фактически в профиле.</span><span class="sxs-lookup"><span data-stu-id="025d1-118">The value in the  _cUID_ parameter differs from the number of transport providers actually in the profile.</span></span> 
    
<span data-ttu-id="025d1-119">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="025d1-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="025d1-120">Одно или несколько из структур [MAPIUID](mapiuid.md) , переданной в параметре _lpUIDList_ относится к поставщика транспорта в настоящее время в профиле.</span><span class="sxs-lookup"><span data-stu-id="025d1-120">One or more of the [MAPIUID](mapiuid.md) structures passed in the  _lpUIDList_ parameter do not refer to a transport provider currently in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="025d1-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="025d1-121">Remarks</span></span>

<span data-ttu-id="025d1-122">Метод **IMsgServiceAdmin::MsgServiceTransportOrder** задает порядок доставки поставщиками транспорта в профиле.</span><span class="sxs-lookup"><span data-stu-id="025d1-122">The **IMsgServiceAdmin::MsgServiceTransportOrder** method sets the delivery order of transport providers in a profile.</span></span> <span data-ttu-id="025d1-123">Параметр _lpUIDList_ должен содержать отсортированный список идентификаторов запись поставщика транспорта, полученного из свойства **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) в таблице, возвращенный из [IMsgServiceAdmin:: GetProviderTable](imsgserviceadmin-getprovidertable.md) метод.</span><span class="sxs-lookup"><span data-stu-id="025d1-123">The  _lpUIDList_ parameter must contain a sorted list of transport-provider entry identifiers obtained from the **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) property of the table returned from the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="025d1-124">Клиентское приложение должно передавать полный список в _lpUIDList_.</span><span class="sxs-lookup"><span data-stu-id="025d1-124">A client application must pass the complete list in  _lpUIDList_.</span></span>
  
 <span data-ttu-id="025d1-125">**SetTransportOrder** переопределений транспорта параметры поставщика, такие как флаг STATUS_XP_PREFER_LAST в свойстве **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="025d1-125">**SetTransportOrder** overrides transport provider preferences such as the STATUS_XP_PREFER_LAST flag set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="025d1-126">См. также</span><span class="sxs-lookup"><span data-stu-id="025d1-126">See also</span></span>



[<span data-ttu-id="025d1-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="025d1-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="025d1-128">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="025d1-128">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

