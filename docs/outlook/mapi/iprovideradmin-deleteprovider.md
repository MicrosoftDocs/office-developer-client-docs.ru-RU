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
# <a name="iprovideradmindeleteprovider"></a><span data-ttu-id="bfaff-103">IProviderAdmin::DeleteProvider</span><span class="sxs-lookup"><span data-stu-id="bfaff-103">IProviderAdmin::DeleteProvider</span></span>

  
  
<span data-ttu-id="bfaff-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bfaff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bfaff-105">Удаляет поставщика службы из службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="bfaff-105">Deletes a service provider from the message service.</span></span>
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a><span data-ttu-id="bfaff-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bfaff-106">Parameters</span></span>

 <span data-ttu-id="bfaff-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="bfaff-107">_lpUID_</span></span>
  
> <span data-ttu-id="bfaff-108">[in, out] Указатель на структуру [MAPIUID,](mapiuid.md) которая содержит уникальный идентификатор, который представляет удаляемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="bfaff-108">[in, out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bfaff-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bfaff-109">Return value</span></span>

<span data-ttu-id="bfaff-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="bfaff-110">S_OK</span></span> 
  
> <span data-ttu-id="bfaff-111">Поставщик был успешно удален из службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="bfaff-111">The provider was successfully deleted from the message service.</span></span>
    
<span data-ttu-id="bfaff-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="bfaff-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="bfaff-113">**MAPIUID, на** который указывает _параметр lpUID,_ не распознан.</span><span class="sxs-lookup"><span data-stu-id="bfaff-113">The **MAPIUID** pointed to by the  _lpUID_ parameter was not recognized.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="bfaff-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="bfaff-114">Remarks</span></span>

<span data-ttu-id="bfaff-115">Метод **IProviderAdmin::D eleteProvider** удаляет поставщика службы из службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="bfaff-115">The **IProviderAdmin::DeleteProvider** method deletes a service provider from the message service.</span></span> <span data-ttu-id="bfaff-116">**DeleteProvider** определяет удаляемого поставщика услуг путем совпадения структуры **MAPIUID,** на который указывает  _lpUID,_ с набором идентификаторов, зарегистрированных активными поставщиками услуг.</span><span class="sxs-lookup"><span data-stu-id="bfaff-116">**DeleteProvider** determines the service provider to delete by matching the **MAPIUID** structure pointed to by  _lpUID_ with the set of identifiers registered by the active service providers.</span></span> 
  
<span data-ttu-id="bfaff-117">Большинство служб сообщений не позволяют удалять поставщиков, пока используется профиль.</span><span class="sxs-lookup"><span data-stu-id="bfaff-117">Most message services do not allow providers to be deleted while the profile is in use.</span></span> <span data-ttu-id="bfaff-118">Если поставщик, который необходимо удалить, используется, **DeleteProvider** пометит его для удаления, а не немедленно удаляет его и возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="bfaff-118">If the provider to delete is in use, **DeleteProvider** marks it for deletion instead of removing it immediately and returns S_OK.</span></span> <span data-ttu-id="bfaff-119">Если поставщик больше не используется, он удаляется.</span><span class="sxs-lookup"><span data-stu-id="bfaff-119">When the provider is no longer being used, it is deleted.</span></span> 
  
 <span data-ttu-id="bfaff-120">**DeleteProvider** вызывает функцию точки входа службы сообщений перед удалением поставщика из службы.</span><span class="sxs-lookup"><span data-stu-id="bfaff-120">**DeleteProvider** calls the message service's entry point function before the provider is removed from the service.</span></span> <span data-ttu-id="bfaff-121">Для  _параметра ulContext_ установлено MSG_SERVICE_PROVIDER_DELETE.</span><span class="sxs-lookup"><span data-stu-id="bfaff-121">The  _ulContext_ parameter is set to MSG_SERVICE_PROVIDER_DELETE.</span></span> <span data-ttu-id="bfaff-122">Функция точки входа службы сообщений выполняет следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="bfaff-122">The message service entry point function performs the following tasks:</span></span> 
  
- <span data-ttu-id="bfaff-123">Удаляет поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="bfaff-123">Deletes the service provider.</span></span>
    
- <span data-ttu-id="bfaff-124">Удаляет раздел профиля поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="bfaff-124">Deletes the service provider's profile section.</span></span>
    
<span data-ttu-id="bfaff-125">Функция точки входа службы сообщений не будет повторно вызвана после удаления поставщика.</span><span class="sxs-lookup"><span data-stu-id="bfaff-125">The message service entry point function is not called again after the provider has been deleted.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bfaff-126">См. также</span><span class="sxs-lookup"><span data-stu-id="bfaff-126">See also</span></span>



[<span data-ttu-id="bfaff-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="bfaff-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="bfaff-128">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="bfaff-128">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="bfaff-129">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bfaff-129">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

