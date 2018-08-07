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
ms.openlocfilehash: d9f08c13f68c7d3d9f41b9a67ac1888d6c507c34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809078"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a><span data-ttu-id="de2ca-103">IMAPIProviderShutdown::QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="de2ca-103">IMAPIProviderShutdown::QueryFastShutdown</span></span>

  
  
<span data-ttu-id="de2ca-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="de2ca-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="de2ca-105">Запросы, которые поддерживают поставщика MAPI для быстрое завершение работы.</span><span class="sxs-lookup"><span data-stu-id="de2ca-105">Queries the MAPI provider for fast shutdown support.</span></span> 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="de2ca-106">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="de2ca-106">Return value</span></span>

<span data-ttu-id="de2ca-107">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="de2ca-107">S_OK</span></span>
  
> <span data-ttu-id="de2ca-108">Поставщик MAPI поддерживает быстрое завершение работы клиента MAPI.</span><span class="sxs-lookup"><span data-stu-id="de2ca-108">The MAPI provider supports the MAPI client to do fast shutdown.</span></span>
    
<span data-ttu-id="de2ca-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="de2ca-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="de2ca-110">Поставщик MAPI не поддерживает быстрое завершение работы клиента MAPI.</span><span class="sxs-lookup"><span data-stu-id="de2ca-110">The MAPI provider does not support the MAPI client to do fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="de2ca-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="de2ca-111">Remarks</span></span>

<span data-ttu-id="de2ca-112">Поставщики MAPI, которые не должны поддерживать быстрое завершение работы клиента следует по-прежнему реализовать интерфейс [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) и метод **IMAPIProviderShutdown::QueryFastShutdown** возвращает MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="de2ca-112">MAPI providers that do not need to support client fast shutdown should still implement the [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="de2ca-113">Для Outlook как клиент MAPI в результате Outlook вынуждены ждать освобождения всех внешних ссылок освободить до его завершения.</span><span class="sxs-lookup"><span data-stu-id="de2ca-113">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="de2ca-114">В зависимости от реестра Windows пользователя политика для быстрое завершение работы не реализация интерфейса **IMAPIProviderShutdown** не обязательно быстрое завершение работы клиента.</span><span class="sxs-lookup"><span data-stu-id="de2ca-114">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="de2ca-115">См. также</span><span class="sxs-lookup"><span data-stu-id="de2ca-115">See also</span></span>



[<span data-ttu-id="de2ca-116">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="de2ca-116">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="de2ca-117">Завершение работы клиента в MAPI</span><span class="sxs-lookup"><span data-stu-id="de2ca-117">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

