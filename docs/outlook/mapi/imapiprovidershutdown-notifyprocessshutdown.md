---
title: IMAPIProviderShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: a00d71b1-d705-40d5-b667-f91b57db85da
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4b18cfc2191ffee936e1056d9bb656a7ad7dd3ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405249"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a><span data-ttu-id="72e2e-103">IMAPIProviderShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="72e2e-103">IMAPIProviderShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="72e2e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72e2e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72e2e-105">Указывает поставщику MAPI, что клиент MAPI собирается сделать быстрое отключение, чтобы поставщик может принять меры для предотвращения потери данных.</span><span class="sxs-lookup"><span data-stu-id="72e2e-105">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="72e2e-106">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="72e2e-106">Return value</span></span>

<span data-ttu-id="72e2e-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="72e2e-107">S_OK</span></span>
  
> <span data-ttu-id="72e2e-108">Поставщик MAPI принимает меры для предотвращения потери данных при закрытии клиента MAPI.</span><span class="sxs-lookup"><span data-stu-id="72e2e-108">The MAPI provider is taking actions to prevent data loss when the MAPI client shuts down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="72e2e-109">См. также</span><span class="sxs-lookup"><span data-stu-id="72e2e-109">See also</span></span>



[<span data-ttu-id="72e2e-110">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="72e2e-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="72e2e-111">Завершение работы клиента в MAPI</span><span class="sxs-lookup"><span data-stu-id="72e2e-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

