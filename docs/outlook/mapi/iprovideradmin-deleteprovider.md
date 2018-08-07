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
ms.openlocfilehash: e0f8dc1beeb669532e3731b38a4f03966403f76c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809519"
---
# <a name="iprovideradmindeleteprovider"></a><span data-ttu-id="e9d75-103">IProviderAdmin::DeleteProvider</span><span class="sxs-lookup"><span data-stu-id="e9d75-103">IProviderAdmin::DeleteProvider</span></span>

  
  
<span data-ttu-id="e9d75-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e9d75-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e9d75-105">Удаляет поставщика услуг службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="e9d75-105">Deletes a service provider from the message service.</span></span>
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a><span data-ttu-id="e9d75-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9d75-106">Parameters</span></span>

 <span data-ttu-id="e9d75-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="e9d75-107">_lpUID_</span></span>
  
> <span data-ttu-id="e9d75-108">[in, out] Указатель на структуру [MAPIUID](mapiuid.md) , содержащую уникальный идентификатор, представляющий поставщика для удаления.</span><span class="sxs-lookup"><span data-stu-id="e9d75-108">[in, out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e9d75-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9">Return value</span></span>

<span data-ttu-id="e9d75-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="e9d75-110">S_OK</span></span> 
  
> <span data-ttu-id="e9d75-111">Поставщик успешно удален из службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="e9d75-111">The provider was successfully deleted from the message service.</span></span>
    
<span data-ttu-id="e9d75-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="e9d75-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="e9d75-113">**MAPIUID** указывает параметр _lpUID_ не распознается.</span><span class="sxs-lookup"><span data-stu-id="e9d75-113">The **MAPIUID** pointed to by the  _lpUID_ parameter was not recognized.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e9d75-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="e9d75-114">Remarks</span></span>

<span data-ttu-id="e9d75-115">Метод **IProviderAdmin::DeleteProvider** удаляет поставщик службы от службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="e9d75-115">The **IProviderAdmin::DeleteProvider** method deletes a service provider from the message service.</span></span> <span data-ttu-id="e9d75-116">**DeleteProvider** определяет поставщик услуг для удаления, сопоставляя структура **MAPIUID** указывает _lpUID_ с набором идентификаторов зарегистрирована поставщиками услуг активный.</span><span class="sxs-lookup"><span data-stu-id="e9d75-116">**DeleteProvider** determines the service provider to delete by matching the **MAPIUID** structure pointed to by  _lpUID_ with the set of identifiers registered by the active service providers.</span></span> 
  
<span data-ttu-id="e9d75-117">Большинство служб сообщения не разрешать поставщиков для удаления во время профиля.</span><span class="sxs-lookup"><span data-stu-id="e9d75-117">Most message services do not allow providers to be deleted while the profile is in use.</span></span> <span data-ttu-id="e9d75-118">Если используется поставщик для удаления **DeleteProvider** помечает для удаления вместо немедленно и возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="e9d75-118">If the provider to delete is in use, **DeleteProvider** marks it for deletion instead of removing it immediately and returns S_OK.</span></span> <span data-ttu-id="e9d75-119">Если поставщик больше не используется, она удаляется.</span><span class="sxs-lookup"><span data-stu-id="e9d75-119">When the provider is no longer being used, it is deleted.</span></span> 
  
 <span data-ttu-id="e9d75-120">**DeleteProvider** вызывает функцию точки входа службы сообщений, перед удалением из службы поставщика.</span><span class="sxs-lookup"><span data-stu-id="e9d75-120">**DeleteProvider** calls the message service's entry point function before the provider is removed from the service.</span></span> <span data-ttu-id="e9d75-121">Параметр _ulContext_ имеет значение MSG_SERVICE_PROVIDER_DELETE.</span><span class="sxs-lookup"><span data-stu-id="e9d75-121">The  _ulContext_ parameter is set to MSG_SERVICE_PROVIDER_DELETE.</span></span> <span data-ttu-id="e9d75-122">Функция точки входа службы сообщение выполняет следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="e9d75-122">The message service entry point function performs the following tasks:</span></span> 
  
- <span data-ttu-id="e9d75-123">Удаляет поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="e9d75-123">Deletes the service provider.</span></span>
    
- <span data-ttu-id="e9d75-124">Удаление раздела профиля поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="e9d75-124">Deletes the service provider's profile section.</span></span>
    
<span data-ttu-id="e9d75-125">После удаления поставщика функции точки входа службы сообщений не вызывает еще раз.</span><span class="sxs-lookup"><span data-stu-id="e9d75-125">The message service entry point function is not called again after the provider has been deleted.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e9d75-126">См. также</span><span class="sxs-lookup"><span data-stu-id="e9d75-126">See also</span></span>



[<span data-ttu-id="e9d75-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="e9d75-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="e9d75-128">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="e9d75-128">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="e9d75-129">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e9d75-129">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

