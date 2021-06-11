---
title: IProviderAdminDeleteProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.DeleteProvider
api_type:
- COM
ms.assetid: 0065b50f-95f6-4af1-81c2-a73e5111eecf
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 28dbbb98c9810bb688b9ecdd730ef6c4ada5f60b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404864"
---
# <a name="iprovideradmindeleteprovider"></a><span data-ttu-id="0c299-103">IProviderAdmin::DeleteProvider</span><span class="sxs-lookup"><span data-stu-id="0c299-103">IProviderAdmin::DeleteProvider</span></span>

  
  
<span data-ttu-id="0c299-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c299-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c299-105">Удаляет поставщика услуг из службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="0c299-105">Deletes a service provider from the message service.</span></span>
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a><span data-ttu-id="0c299-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="0c299-106">Parameters</span></span>

 <span data-ttu-id="0c299-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="0c299-107">_lpUID_</span></span>
  
> <span data-ttu-id="0c299-108">[in, out] Указатель на структуру [MAPIUID,](mapiuid.md) которая содержит уникальный идентификатор, который представляет поставщика для удаления.</span><span class="sxs-lookup"><span data-stu-id="0c299-108">[in, out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0c299-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0c299-109">Return value</span></span>

<span data-ttu-id="0c299-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="0c299-110">S_OK</span></span> 
  
> <span data-ttu-id="0c299-111">Поставщик был успешно удален из службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="0c299-111">The provider was successfully deleted from the message service.</span></span>
    
<span data-ttu-id="0c299-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="0c299-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="0c299-113">**MapIUID,** на который указывает _параметр lpUID,_ не был распознан.</span><span class="sxs-lookup"><span data-stu-id="0c299-113">The **MAPIUID** pointed to by the  _lpUID_ parameter was not recognized.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0c299-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0c299-114">Remarks</span></span>

<span data-ttu-id="0c299-115">Метод **IProviderAdmin::D eleteProvider** удаляет поставщика услуг из службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="0c299-115">The **IProviderAdmin::DeleteProvider** method deletes a service provider from the message service.</span></span> <span data-ttu-id="0c299-116">**DeleteProvider** определяет поставщика услуг для удаления путем совпадения структуры **MAPIUID,** на которые указывает  _lpUID,_ с набором идентификаторов, зарегистрированных активными поставщиками услуг.</span><span class="sxs-lookup"><span data-stu-id="0c299-116">**DeleteProvider** determines the service provider to delete by matching the **MAPIUID** structure pointed to by  _lpUID_ with the set of identifiers registered by the active service providers.</span></span> 
  
<span data-ttu-id="0c299-117">Большинство служб сообщений не позволяют удалять поставщиков во время использования профиля.</span><span class="sxs-lookup"><span data-stu-id="0c299-117">Most message services do not allow providers to be deleted while the profile is in use.</span></span> <span data-ttu-id="0c299-118">Если поставщик для удаления используется, **DeleteProvider** пометит его для удаления, а не удалить его немедленно и возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="0c299-118">If the provider to delete is in use, **DeleteProvider** marks it for deletion instead of removing it immediately and returns S_OK.</span></span> <span data-ttu-id="0c299-119">Если поставщик больше не используется, он удаляется.</span><span class="sxs-lookup"><span data-stu-id="0c299-119">When the provider is no longer being used, it is deleted.</span></span> 
  
 <span data-ttu-id="0c299-120">**DeleteProvider** вызывает функцию точки входа службы сообщений перед удалением поставщика из службы.</span><span class="sxs-lookup"><span data-stu-id="0c299-120">**DeleteProvider** calls the message service's entry point function before the provider is removed from the service.</span></span> <span data-ttu-id="0c299-121">Параметр  _ulContext_ задан для MSG_SERVICE_PROVIDER_DELETE.</span><span class="sxs-lookup"><span data-stu-id="0c299-121">The  _ulContext_ parameter is set to MSG_SERVICE_PROVIDER_DELETE.</span></span> <span data-ttu-id="0c299-122">Функция точки входа службы сообщений выполняет следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="0c299-122">The message service entry point function performs the following tasks:</span></span> 
  
- <span data-ttu-id="0c299-123">Удаляет поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="0c299-123">Deletes the service provider.</span></span>
    
- <span data-ttu-id="0c299-124">Удаляет раздел профилей поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="0c299-124">Deletes the service provider's profile section.</span></span>
    
<span data-ttu-id="0c299-125">Функция точки входа службы сообщений после удаления поставщика не будет снова вызвана.</span><span class="sxs-lookup"><span data-stu-id="0c299-125">The message service entry point function is not called again after the provider has been deleted.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0c299-126">См. также</span><span class="sxs-lookup"><span data-stu-id="0c299-126">See also</span></span>



[<span data-ttu-id="0c299-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="0c299-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="0c299-128">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="0c299-128">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="0c299-129">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0c299-129">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

