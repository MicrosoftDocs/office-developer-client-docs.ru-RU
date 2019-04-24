---
title: Имапипровидершутдовнкуерифастшутдовн
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338488"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a><span data-ttu-id="9f9bb-103">IMAPIProviderShutdown::QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="9f9bb-103">IMAPIProviderShutdown::QueryFastShutdown</span></span>

  
  
<span data-ttu-id="9f9bb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f9bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f9bb-105">ЗаПрашивает у поставщика MAPI поддержку быстрого завершения работы.</span><span class="sxs-lookup"><span data-stu-id="9f9bb-105">Queries the MAPI provider for fast shutdown support.</span></span> 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="9f9bb-106">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f9bb-106">Return value</span></span>

<span data-ttu-id="9f9bb-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="9f9bb-107">S_OK</span></span>
  
> <span data-ttu-id="9f9bb-108">Поставщик MAPI поддерживает клиент MAPI для быстрого завершения работы.</span><span class="sxs-lookup"><span data-stu-id="9f9bb-108">The MAPI provider supports the MAPI client to do fast shutdown.</span></span>
    
<span data-ttu-id="9f9bb-109">МАПИ_Е_НО_СУППОРТ</span><span class="sxs-lookup"><span data-stu-id="9f9bb-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="9f9bb-110">Поставщик MAPI не поддерживает быстрое завершение работы клиента MAPI.</span><span class="sxs-lookup"><span data-stu-id="9f9bb-110">The MAPI provider does not support the MAPI client to do fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9f9bb-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f9bb-111">Remarks</span></span>

<span data-ttu-id="9f9bb-112">Поставщики MAPI, которые не нуждаются в поддержке быстрого завершения работы клиента, по-прежнему должны реализовывать интерфейс [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) и иметь метод **IMAPIProviderShutdown:: QueryFastShutdown** , возвращающий мапи_е_но_суппорт.</span><span class="sxs-lookup"><span data-stu-id="9f9bb-112">MAPI providers that do not need to support client fast shutdown should still implement the [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="9f9bb-113">Для Outlook в качестве клиента MAPI это приводит к тому, что Outlook ждет, пока все внешние ссылки будут сняты до завершения работы.</span><span class="sxs-lookup"><span data-stu-id="9f9bb-113">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="9f9bb-114">В зависимости от параметра реестра Windows для быстрого завершения работы, отсутствие реализации интерфейса **IMAPIProviderShutdown** не обязательно препятствует быстрому завершению работы клиента.</span><span class="sxs-lookup"><span data-stu-id="9f9bb-114">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9f9bb-115">См. также</span><span class="sxs-lookup"><span data-stu-id="9f9bb-115">See also</span></span>



[<span data-ttu-id="9f9bb-116">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9f9bb-116">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="9f9bb-117">Завершение работы клиента в MAPI</span><span class="sxs-lookup"><span data-stu-id="9f9bb-117">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

