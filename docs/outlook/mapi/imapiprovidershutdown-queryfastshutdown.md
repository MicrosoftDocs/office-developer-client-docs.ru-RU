---
title: IMAPIProviderShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: 12069912-4b87-4945-9123-51106e0d2d54
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 50b49761cf5923b11a450cbce7b7991f5ddd4d82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418220"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a><span data-ttu-id="1a392-103">IMAPIProviderShutdown::QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="1a392-103">IMAPIProviderShutdown::QueryFastShutdown</span></span>

  
  
<span data-ttu-id="1a392-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a392-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a392-105">Запрашивает у поставщика MAPI поддержку быстрого завершения работы.</span><span class="sxs-lookup"><span data-stu-id="1a392-105">Queries the MAPI provider for fast shutdown support.</span></span> 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="1a392-106">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a392-106">Return value</span></span>

<span data-ttu-id="1a392-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="1a392-107">S_OK</span></span>
  
> <span data-ttu-id="1a392-108">Поставщик MAPI поддерживает клиент MAPI для быстрого завершения работы.</span><span class="sxs-lookup"><span data-stu-id="1a392-108">The MAPI provider supports the MAPI client to do fast shutdown.</span></span>
    
<span data-ttu-id="1a392-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="1a392-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="1a392-110">Поставщик MAPI не поддерживает клиент MAPI для быстрого завершения работы.</span><span class="sxs-lookup"><span data-stu-id="1a392-110">The MAPI provider does not support the MAPI client to do fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1a392-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="1a392-111">Remarks</span></span>

<span data-ttu-id="1a392-112">Поставщики MAPI, которые не нуждаются в поддержке быстрого завершения работы клиента, по-прежнему должны реализовать интерфейс [IMAPIProviderShutdown,](imapiprovidershutdowniunknown.md) а метод **IMAPIProviderShutdown::QueryFastShutdown** должен возвращать MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="1a392-112">MAPI providers that do not need to support client fast shutdown should still implement the [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="1a392-113">Для Outlook в качестве клиента MAPI это приводит к ожиданию выпуска всех внешних ссылок перед выходом из outlook.</span><span class="sxs-lookup"><span data-stu-id="1a392-113">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="1a392-114">В зависимости от параметра реестра Windows пользователя для быстрого завершения работы не реализация интерфейса **IMAPIProviderShutdown** не обязательно препятствует быстрому отключению клиента.</span><span class="sxs-lookup"><span data-stu-id="1a392-114">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1a392-115">См. также</span><span class="sxs-lookup"><span data-stu-id="1a392-115">See also</span></span>



[<span data-ttu-id="1a392-116">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1a392-116">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="1a392-117">Завершение работы клиента в MAPI</span><span class="sxs-lookup"><span data-stu-id="1a392-117">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

