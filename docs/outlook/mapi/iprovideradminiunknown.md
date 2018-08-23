---
title: IProviderAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin
api_type:
- COM
ms.assetid: bdb4cdca-8dfd-4f90-9467-ec31cea3f518
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 559680b9ca4ea5be85718d8f9692df93f77b0edf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585754"
---
# <a name="iprovideradmin--iunknown"></a><span data-ttu-id="87f79-103">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="87f79-103">IProviderAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="87f79-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87f79-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87f79-105">Работа с поставщиков услуг службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="87f79-105">Works with service providers in a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87f79-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="87f79-106">Header file:</span></span>  <br/> |<span data-ttu-id="87f79-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="87f79-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="87f79-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="87f79-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="87f79-109">Объекты администрирования поставщика</span><span class="sxs-lookup"><span data-stu-id="87f79-109">Provider administration objects</span></span>  <br/> |
|<span data-ttu-id="87f79-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="87f79-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="87f79-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="87f79-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="87f79-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="87f79-112">Called by:</span></span>  <br/> |<span data-ttu-id="87f79-113">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="87f79-113">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="87f79-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="87f79-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="87f79-115">IID_IProviderAdmin</span><span class="sxs-lookup"><span data-stu-id="87f79-115">IID_IProviderAdmin</span></span>  <br/> |
|<span data-ttu-id="87f79-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="87f79-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="87f79-117">LPPROVIDERADMIN</span><span class="sxs-lookup"><span data-stu-id="87f79-117">LPPROVIDERADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="87f79-118">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="87f79-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="87f79-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="87f79-119">GetLastError</span></span>](iprovideradmin-getlasterror.md) <br/> |<span data-ttu-id="87f79-120">Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о предыдущем ошибки, которые произошли объект администрирования поставщика.</span><span class="sxs-lookup"><span data-stu-id="87f79-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to the provider administration object.</span></span>  <br/> |
|[<span data-ttu-id="87f79-121">GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="87f79-121">GetProviderTable</span></span>](iprovideradmin-getprovidertable.md) <br/> |<span data-ttu-id="87f79-122">Предоставляет доступ к таблице поставщика службы сообщений, список поставщиков услуг службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="87f79-122">Provides access to the message service's provider table, a list of the service providers in the message service.</span></span>  <br/> |
|[<span data-ttu-id="87f79-123">CreateProvider</span><span class="sxs-lookup"><span data-stu-id="87f79-123">CreateProvider</span></span>](iprovideradmin-createprovider.md) <br/> |<span data-ttu-id="87f79-124">Добавление поставщика услуг службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="87f79-124">Adds a service provider to the message service.</span></span>  <br/> |
|[<span data-ttu-id="87f79-125">DeleteProvider</span><span class="sxs-lookup"><span data-stu-id="87f79-125">DeleteProvider</span></span>](iprovideradmin-deleteprovider.md) <br/> |<span data-ttu-id="87f79-126">Удаляет поставщика услуг службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="87f79-126">Deletes a service provider from the message service.</span></span>  <br/> |
|[<span data-ttu-id="87f79-127">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="87f79-127">OpenProfileSection</span></span>](iprovideradmin-openprofilesection.md) <br/> |<span data-ttu-id="87f79-128">Открывает профиля из текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшей доступа.</span><span class="sxs-lookup"><span data-stu-id="87f79-128">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87f79-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="87f79-129">Remarks</span></span>

<span data-ttu-id="87f79-130">Клиенты могут получить указатель на интерфейс **IProviderAdmin** путем вызова метода [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) ; Поставщики услуг, передаются указатель **IProviderAdmin** при вызове функции точки входа их службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="87f79-130">Clients can get a pointer to an **IProviderAdmin** interface by calling the [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) method; service providers are passed an **IProviderAdmin** pointer when their message service's entry point function is called.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="87f79-131">См. также</span><span class="sxs-lookup"><span data-stu-id="87f79-131">See also</span></span>



[<span data-ttu-id="87f79-132">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="87f79-132">MAPI Interfaces</span></span>](mapi-interfaces.md)

