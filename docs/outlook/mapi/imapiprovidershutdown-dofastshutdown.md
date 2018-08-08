---
title: IMAPIProviderShutdownDoFastShutdown
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
ms.openlocfilehash: 7c38f0650315495875357862f5fa7fe138d2c61b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809031"
---
# <a name="imapiprovidershutdowndofastshutdown"></a><span data-ttu-id="3ed61-103">IMAPIProviderShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="3ed61-103">IMAPIProviderShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="3ed61-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3ed61-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3ed61-105">Указывает поставщика MAPI немедленно, выходе клиент MAPI, чтобы поставщик MAPI будут сохранены и отобразятся изменения, чтобы предотвратить потерю данных.</span><span class="sxs-lookup"><span data-stu-id="3ed61-105">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="3ed61-106">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="3ed61-106">Return value</span></span>

<span data-ttu-id="3ed61-107">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="3ed61-107">S_OK</span></span>
  
> <span data-ttu-id="3ed61-108">Клиент MAPI выйти из сразу же готов поставщика MAPI.</span><span class="sxs-lookup"><span data-stu-id="3ed61-108">The MAPI provider is ready for the MAPI client to exit immediately.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="3ed61-109">См. также</span><span class="sxs-lookup"><span data-stu-id="3ed61-109">See also</span></span>



[<span data-ttu-id="3ed61-110">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3ed61-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="3ed61-111">Завершение работы клиента в MAPI</span><span class="sxs-lookup"><span data-stu-id="3ed61-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

