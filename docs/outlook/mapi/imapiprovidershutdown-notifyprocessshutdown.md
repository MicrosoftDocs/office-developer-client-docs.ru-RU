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
ms.openlocfilehash: cce98dc630dd9f7fa459ca31d94d012ba9a7fd85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809052"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a><span data-ttu-id="9ae14-103">IMAPIProviderShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="9ae14-103">IMAPIProviderShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="9ae14-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9ae14-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9ae14-105">Указывает поставщика MAPI, что клиент MAPI требуется выполнить быстрое завершение работы, чтобы поставщик можно выполнять действия, чтобы предотвратить потерю данных.</span><span class="sxs-lookup"><span data-stu-id="9ae14-105">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="9ae14-106">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="9ae14-106">Return value</span></span>

<span data-ttu-id="9ae14-107">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="9ae14-107">S_OK</span></span>
  
> <span data-ttu-id="9ae14-108">Поставщик MAPI занимает действия, чтобы предотвратить потерю данных, если клиент MAPI завершает работу.</span><span class="sxs-lookup"><span data-stu-id="9ae14-108">The MAPI provider is taking actions to prevent data loss when the MAPI client shuts down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ae14-109">См. также</span><span class="sxs-lookup"><span data-stu-id="9ae14-109">See also</span></span>



[<span data-ttu-id="9ae14-110">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9ae14-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="9ae14-111">Завершение работы клиента в MAPI</span><span class="sxs-lookup"><span data-stu-id="9ae14-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

