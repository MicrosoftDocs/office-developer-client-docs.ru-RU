---
title: Имапипровидершутдовндофастшутдовн
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: d2b66a8e-2e28-4c32-af95-38d345c7bbd7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4ff93ed9353d58ef6b68823bebf8b5b27a0df6e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428846"
---
# <a name="imapiprovidershutdowndofastshutdown"></a><span data-ttu-id="58a65-103">IMAPIProviderShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="58a65-103">IMAPIProviderShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="58a65-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58a65-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58a65-105">Указывает поставщику MAPI, что клиент MAPI немедленно завершает работу, поэтому поставщик MAPI сохранит изменения, чтобы предотвратить потерю данных.</span><span class="sxs-lookup"><span data-stu-id="58a65-105">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="58a65-106">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="58a65-106">Return value</span></span>

<span data-ttu-id="58a65-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="58a65-107">S_OK</span></span>
  
> <span data-ttu-id="58a65-108">Поставщик MAPI готов к немедленному завершению работы клиента MAPI.</span><span class="sxs-lookup"><span data-stu-id="58a65-108">The MAPI provider is ready for the MAPI client to exit immediately.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="58a65-109">См. также</span><span class="sxs-lookup"><span data-stu-id="58a65-109">See also</span></span>



[<span data-ttu-id="58a65-110">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="58a65-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="58a65-111">Завершение работы клиента в MAPI</span><span class="sxs-lookup"><span data-stu-id="58a65-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

