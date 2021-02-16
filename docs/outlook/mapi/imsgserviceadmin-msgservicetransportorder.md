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
ms.openlocfilehash: 3d532e0eb46daa412711344421936a58da309b7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420096"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a><span data-ttu-id="d7013-103">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="d7013-103">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>

  
  
<span data-ttu-id="d7013-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7013-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7013-105">Задает порядок, в котором будут вызваны поставщики транспорта для доставки сообщения.</span><span class="sxs-lookup"><span data-stu-id="d7013-105">Sets the order in which transport providers are called to deliver a message.</span></span>
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a><span data-ttu-id="d7013-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7013-106">Parameters</span></span>

 <span data-ttu-id="d7013-107">_cUID_</span><span class="sxs-lookup"><span data-stu-id="d7013-107">_cUID_</span></span>
  
> <span data-ttu-id="d7013-108">[in] Количество уникальных идентификаторов в параметре _lpUIDList._</span><span class="sxs-lookup"><span data-stu-id="d7013-108">[in] The count of unique identifiers in the  _lpUIDList_ parameter.</span></span> 
    
 <span data-ttu-id="d7013-109">_lpUIDList_</span><span class="sxs-lookup"><span data-stu-id="d7013-109">_lpUIDList_</span></span>
  
> <span data-ttu-id="d7013-110">[in] Указатель на массив уникальных идентификаторов, которые представляют поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="d7013-110">[in] A pointer to an array of unique identifiers that represent transport providers.</span></span> <span data-ttu-id="d7013-111">Массив содержит один идентификатор для каждого поставщика транспорта, настроенного в текущем профиле.</span><span class="sxs-lookup"><span data-stu-id="d7013-111">The array contains one identifier for each transport provider configured in the current profile.</span></span>
    
 <span data-ttu-id="d7013-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d7013-112">_ulFlags_</span></span>
  
> <span data-ttu-id="d7013-113">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="d7013-113">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d7013-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7013-114">Return value</span></span>

<span data-ttu-id="d7013-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="d7013-115">S_OK</span></span> 
  
> <span data-ttu-id="d7013-116">Порядок транспорта успешно установлен.</span><span class="sxs-lookup"><span data-stu-id="d7013-116">The transport order was set successfully.</span></span>
    
<span data-ttu-id="d7013-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="d7013-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="d7013-118">Значение параметра  _cUID_ отличается от числа поставщиков транспорта в профиле.</span><span class="sxs-lookup"><span data-stu-id="d7013-118">The value in the  _cUID_ parameter differs from the number of transport providers actually in the profile.</span></span> 
    
<span data-ttu-id="d7013-119">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d7013-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="d7013-120">Одна или несколько структур [MAPIUID,](mapiuid.md) переданных в  _параметре lpUIDList,_ не ссылаются на поставщика транспорта, который в данный момент находится в профиле.</span><span class="sxs-lookup"><span data-stu-id="d7013-120">One or more of the [MAPIUID](mapiuid.md) structures passed in the  _lpUIDList_ parameter do not refer to a transport provider currently in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d7013-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="d7013-121">Remarks</span></span>

<span data-ttu-id="d7013-122">Метод **IMsgServiceAdmin::MsgServiceTransportOrder** задает порядок доставки поставщиков транспорта в профиле.</span><span class="sxs-lookup"><span data-stu-id="d7013-122">The **IMsgServiceAdmin::MsgServiceTransportOrder** method sets the delivery order of transport providers in a profile.</span></span> <span data-ttu-id="d7013-123">Параметр _lpUIDList_ должен содержать отсортируемый список идентификаторов записей поставщика транспорта, полученных из свойства **PR_PROVIDER_UID** ([PidTagProviderUid)](pidtagprovideruid-canonical-property.md)таблицы, возвращаемой методом [IMsgServiceAdmin::GetProviderTable.](imsgserviceadmin-getprovidertable.md)</span><span class="sxs-lookup"><span data-stu-id="d7013-123">The  _lpUIDList_ parameter must contain a sorted list of transport-provider entry identifiers obtained from the **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) property of the table returned from the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="d7013-124">Клиентские приложения должны передавать полный список  _в lpUIDList_.</span><span class="sxs-lookup"><span data-stu-id="d7013-124">A client application must pass the complete list in  _lpUIDList_.</span></span>
  
 <span data-ttu-id="d7013-125">**SetTransportOrder** переопределяет параметры поставщика транспорта, такие как флаг STATUS_XP_PREFER_LAST, установленный в свойстве **PR_RESOURCE_FLAGS** ([PidTagResourceFlags).](pidtagresourceflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="d7013-125">**SetTransportOrder** overrides transport provider preferences such as the STATUS_XP_PREFER_LAST flag set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d7013-126">См. также</span><span class="sxs-lookup"><span data-stu-id="d7013-126">See also</span></span>



[<span data-ttu-id="d7013-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="d7013-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="d7013-128">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d7013-128">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

