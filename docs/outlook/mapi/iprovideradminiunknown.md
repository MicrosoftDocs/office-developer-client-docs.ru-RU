---
title: Ипровидерадмин IUnknown
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
ms.openlocfilehash: bedec72e8371d0e8aa69415d2f0dc77b4c62ff76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437534"
---
# <a name="iprovideradmin--iunknown"></a><span data-ttu-id="963b8-103">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="963b8-103">IProviderAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="963b8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="963b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="963b8-105">Работает с поставщиками услуг в службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="963b8-105">Works with service providers in a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="963b8-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="963b8-106">Header file:</span></span>  <br/> |<span data-ttu-id="963b8-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="963b8-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="963b8-108">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="963b8-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="963b8-109">Объекты администрирования поставщика</span><span class="sxs-lookup"><span data-stu-id="963b8-109">Provider administration objects</span></span>  <br/> |
|<span data-ttu-id="963b8-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="963b8-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="963b8-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="963b8-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="963b8-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="963b8-112">Called by:</span></span>  <br/> |<span data-ttu-id="963b8-113">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="963b8-113">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="963b8-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="963b8-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="963b8-115">Иид_ипровидерадмин</span><span class="sxs-lookup"><span data-stu-id="963b8-115">IID_IProviderAdmin</span></span>  <br/> |
|<span data-ttu-id="963b8-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="963b8-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="963b8-117">ЛППРОВИДЕРАДМИН</span><span class="sxs-lookup"><span data-stu-id="963b8-117">LPPROVIDERADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="963b8-118">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="963b8-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="963b8-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="963b8-119">GetLastError</span></span>](iprovideradmin-getlasterror.md) <br/> |<span data-ttu-id="963b8-120">Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущей ошибке, произошедшей для объекта администрирования поставщика.</span><span class="sxs-lookup"><span data-stu-id="963b8-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to the provider administration object.</span></span>  <br/> |
|[<span data-ttu-id="963b8-121">Жетпровидертабле</span><span class="sxs-lookup"><span data-stu-id="963b8-121">GetProviderTable</span></span>](iprovideradmin-getprovidertable.md) <br/> |<span data-ttu-id="963b8-122">Предоставляет доступ к таблице поставщика службы сообщений, список поставщиков служб в службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="963b8-122">Provides access to the message service's provider table, a list of the service providers in the message service.</span></span>  <br/> |
|[<span data-ttu-id="963b8-123">Креатепровидер</span><span class="sxs-lookup"><span data-stu-id="963b8-123">CreateProvider</span></span>](iprovideradmin-createprovider.md) <br/> |<span data-ttu-id="963b8-124">Добавляет поставщика услуг в службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="963b8-124">Adds a service provider to the message service.</span></span>  <br/> |
|[<span data-ttu-id="963b8-125">Делетепровидер</span><span class="sxs-lookup"><span data-stu-id="963b8-125">DeleteProvider</span></span>](iprovideradmin-deleteprovider.md) <br/> |<span data-ttu-id="963b8-126">Удаляет поставщика услуг из службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="963b8-126">Deletes a service provider from the message service.</span></span>  <br/> |
|[<span data-ttu-id="963b8-127">Опенпрофилесектион</span><span class="sxs-lookup"><span data-stu-id="963b8-127">OpenProfileSection</span></span>](iprovideradmin-openprofilesection.md) <br/> |<span data-ttu-id="963b8-128">Открывает раздел профиля из текущего профиля и возвращает указатель [ипрофсект](iprofsectimapiprop.md) для получения дальнейших прав.</span><span class="sxs-lookup"><span data-stu-id="963b8-128">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="963b8-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="963b8-129">Remarks</span></span>

<span data-ttu-id="963b8-130">Клиенты могут получить указатель на интерфейс **ипровидерадмин** , вызвав метод [Имсгсервицеадмин:: админпровидерс](imsgserviceadmin-adminproviders.md) ; поставщики услуг передаются в качестве указателя **ипровидерадмин** при вызове функции точки входа для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="963b8-130">Clients can get a pointer to an **IProviderAdmin** interface by calling the [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) method; service providers are passed an **IProviderAdmin** pointer when their message service's entry point function is called.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="963b8-131">См. также</span><span class="sxs-lookup"><span data-stu-id="963b8-131">See also</span></span>



[<span data-ttu-id="963b8-132">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="963b8-132">MAPI Interfaces</span></span>](mapi-interfaces.md)

