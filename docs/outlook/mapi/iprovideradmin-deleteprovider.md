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
ms.openlocfilehash: db09b44bd8eeeb3ab56513b1b9c2cab69f776002
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590087"
---
# <a name="iprovideradmindeleteprovider"></a><span data-ttu-id="2df9e-103">IProviderAdmin::DeleteProvider</span><span class="sxs-lookup"><span data-stu-id="2df9e-103">IProviderAdmin::DeleteProvider</span></span>

  
  
<span data-ttu-id="2df9e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2df9e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2df9e-105">Удаляет поставщика услуг службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="2df9e-105">Deletes a service provider from the message service.</span></span>
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a><span data-ttu-id="2df9e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2df9e-106">Parameters</span></span>

 <span data-ttu-id="2df9e-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="2df9e-107">_lpUID_</span></span>
  
> <span data-ttu-id="2df9e-108">[in, out] Указатель на структуру [MAPIUID](mapiuid.md) , содержащую уникальный идентификатор, представляющий поставщика для удаления.</span><span class="sxs-lookup"><span data-stu-id="2df9e-108">[in, out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2df9e-109">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="2df9e-109">Return value</span></span>

<span data-ttu-id="2df9e-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="2df9e-110">S_OK</span></span> 
  
> <span data-ttu-id="2df9e-111">Поставщик успешно удален из службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="2df9e-111">The provider was successfully deleted from the message service.</span></span>
    
<span data-ttu-id="2df9e-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="2df9e-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="2df9e-113">**MAPIUID** указывает параметр _lpUID_ не распознается.</span><span class="sxs-lookup"><span data-stu-id="2df9e-113">The **MAPIUID** pointed to by the  _lpUID_ parameter was not recognized.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2df9e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="2df9e-114">Remarks</span></span>

<span data-ttu-id="2df9e-115">Метод **IProviderAdmin::DeleteProvider** удаляет поставщик службы от службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="2df9e-115">The **IProviderAdmin::DeleteProvider** method deletes a service provider from the message service.</span></span> <span data-ttu-id="2df9e-116">**DeleteProvider** определяет поставщик услуг для удаления, сопоставляя структура **MAPIUID** указывает _lpUID_ с набором идентификаторов зарегистрирована поставщиками услуг активный.</span><span class="sxs-lookup"><span data-stu-id="2df9e-116">**DeleteProvider** determines the service provider to delete by matching the **MAPIUID** structure pointed to by  _lpUID_ with the set of identifiers registered by the active service providers.</span></span> 
  
<span data-ttu-id="2df9e-117">Большинство служб сообщения не разрешать поставщиков для удаления во время профиля.</span><span class="sxs-lookup"><span data-stu-id="2df9e-117">Most message services do not allow providers to be deleted while the profile is in use.</span></span> <span data-ttu-id="2df9e-118">Если используется поставщик для удаления **DeleteProvider** помечает для удаления вместо немедленно и возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="2df9e-118">If the provider to delete is in use, **DeleteProvider** marks it for deletion instead of removing it immediately and returns S_OK.</span></span> <span data-ttu-id="2df9e-119">Если поставщик больше не используется, она удаляется.</span><span class="sxs-lookup"><span data-stu-id="2df9e-119">When the provider is no longer being used, it is deleted.</span></span> 
  
 <span data-ttu-id="2df9e-120">**DeleteProvider** вызывает функцию точки входа службы сообщений, перед удалением из службы поставщика.</span><span class="sxs-lookup"><span data-stu-id="2df9e-120">**DeleteProvider** calls the message service's entry point function before the provider is removed from the service.</span></span> <span data-ttu-id="2df9e-121">Параметр _ulContext_ имеет значение MSG_SERVICE_PROVIDER_DELETE.</span><span class="sxs-lookup"><span data-stu-id="2df9e-121">The  _ulContext_ parameter is set to MSG_SERVICE_PROVIDER_DELETE.</span></span> <span data-ttu-id="2df9e-122">Функция точки входа службы сообщение выполняет следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="2df9e-122">The message service entry point function performs the following tasks:</span></span> 
  
- <span data-ttu-id="2df9e-123">Удаляет поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="2df9e-123">Deletes the service provider.</span></span>
    
- <span data-ttu-id="2df9e-124">Удаление раздела профиля поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="2df9e-124">Deletes the service provider's profile section.</span></span>
    
<span data-ttu-id="2df9e-125">После удаления поставщика функции точки входа службы сообщений не вызывает еще раз.</span><span class="sxs-lookup"><span data-stu-id="2df9e-125">The message service entry point function is not called again after the provider has been deleted.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2df9e-126">См. также</span><span class="sxs-lookup"><span data-stu-id="2df9e-126">See also</span></span>



[<span data-ttu-id="2df9e-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="2df9e-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="2df9e-128">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="2df9e-128">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="2df9e-129">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2df9e-129">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

