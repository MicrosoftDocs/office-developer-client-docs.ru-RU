---
title: Имсгсервицеадминмсгсервицетранспортордер
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310005"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a><span data-ttu-id="5db8e-103">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="5db8e-103">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>

  
  
<span data-ttu-id="5db8e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5db8e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5db8e-105">Задает порядок, в котором будут вызываться поставщики транспорта для доставки сообщения.</span><span class="sxs-lookup"><span data-stu-id="5db8e-105">Sets the order in which transport providers are called to deliver a message.</span></span>
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a><span data-ttu-id="5db8e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5db8e-106">Parameters</span></span>

 <span data-ttu-id="5db8e-107">_Куид_</span><span class="sxs-lookup"><span data-stu-id="5db8e-107">_cUID_</span></span>
  
> <span data-ttu-id="5db8e-108">возврата Количество уникальных идентификаторов в параметре _лпуидлист_ .</span><span class="sxs-lookup"><span data-stu-id="5db8e-108">[in] The count of unique identifiers in the  _lpUIDList_ parameter.</span></span> 
    
 <span data-ttu-id="5db8e-109">_Лпуидлист_</span><span class="sxs-lookup"><span data-stu-id="5db8e-109">_lpUIDList_</span></span>
  
> <span data-ttu-id="5db8e-110">возврата Указатель на массив уникальных идентификаторов, представляющих поставщики транспорта.</span><span class="sxs-lookup"><span data-stu-id="5db8e-110">[in] A pointer to an array of unique identifiers that represent transport providers.</span></span> <span data-ttu-id="5db8e-111">Массив содержит один идентификатор для каждого поставщика транспорта, настроенного в текущем профиле.</span><span class="sxs-lookup"><span data-stu-id="5db8e-111">The array contains one identifier for each transport provider configured in the current profile.</span></span>
    
 <span data-ttu-id="5db8e-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5db8e-112">_ulFlags_</span></span>
  
> <span data-ttu-id="5db8e-113">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="5db8e-113">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5db8e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5db8e-114">Return value</span></span>

<span data-ttu-id="5db8e-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="5db8e-115">S_OK</span></span> 
  
> <span data-ttu-id="5db8e-116">Транспортный заказ успешно установлен.</span><span class="sxs-lookup"><span data-stu-id="5db8e-116">The transport order was set successfully.</span></span>
    
<span data-ttu-id="5db8e-117">МАПИ_Е_БУСИ</span><span class="sxs-lookup"><span data-stu-id="5db8e-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="5db8e-118">Значение параметра _куид_ отличается от количества поставщиков транспорта в профиле.</span><span class="sxs-lookup"><span data-stu-id="5db8e-118">The value in the  _cUID_ parameter differs from the number of transport providers actually in the profile.</span></span> 
    
<span data-ttu-id="5db8e-119">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="5db8e-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="5db8e-120">Одна или несколько структур [мапиуид](mapiuid.md) , переданных в параметре _лпуидлист_ , не ссылаются на поставщика транспорта, находящихся в данный момент в профиле.</span><span class="sxs-lookup"><span data-stu-id="5db8e-120">One or more of the [MAPIUID](mapiuid.md) structures passed in the  _lpUIDList_ parameter do not refer to a transport provider currently in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5db8e-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="5db8e-121">Remarks</span></span>

<span data-ttu-id="5db8e-122">Метод **имсгсервицеадмин:: мсгсервицетранспортордер** устанавливает порядок доставки поставщиков транспорта в профиле.</span><span class="sxs-lookup"><span data-stu-id="5db8e-122">The **IMsgServiceAdmin::MsgServiceTransportOrder** method sets the delivery order of transport providers in a profile.</span></span> <span data-ttu-id="5db8e-123">Параметр _лпуидлист_ должен содержать отсортированный список идентификаторов записей поставщика транспорта, полученных из свойства **пр_провидер_уид** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) таблицы, возвращаемой из [имсгсервицеадмин:: Метод Жетпровидертабле](imsgserviceadmin-getprovidertable.md) .</span><span class="sxs-lookup"><span data-stu-id="5db8e-123">The  _lpUIDList_ parameter must contain a sorted list of transport-provider entry identifiers obtained from the **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) property of the table returned from the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="5db8e-124">Клиентское приложение должно передать полный список в _лпуидлист_.</span><span class="sxs-lookup"><span data-stu-id="5db8e-124">A client application must pass the complete list in  _lpUIDList_.</span></span>
  
 <span data-ttu-id="5db8e-125">**Сеттранспортордер** переопределяет параметры поставщика транспорта, такие как флаг статус_ксп_префер_ласт, установленный в свойстве \*\*пр_ресаурце_флагс\*\* ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5db8e-125">**SetTransportOrder** overrides transport provider preferences such as the STATUS_XP_PREFER_LAST flag set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5db8e-126">См. также</span><span class="sxs-lookup"><span data-stu-id="5db8e-126">See also</span></span>



[<span data-ttu-id="5db8e-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="5db8e-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="5db8e-128">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5db8e-128">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

