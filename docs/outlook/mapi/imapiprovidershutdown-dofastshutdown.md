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
ms.openlocfilehash: faa061ae323dd744d12e4f9abec713c71379feba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563473"
---
# <a name="imapiprovidershutdowndofastshutdown"></a><span data-ttu-id="fa7bb-103">IMAPIProviderShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="fa7bb-103">IMAPIProviderShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="fa7bb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa7bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa7bb-105">Указывает поставщика MAPI немедленно, выходе клиент MAPI, чтобы поставщик MAPI будут сохранены и отобразятся изменения, чтобы предотвратить потерю данных.</span><span class="sxs-lookup"><span data-stu-id="fa7bb-105">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="fa7bb-106">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa7bb-106">Return value</span></span>

<span data-ttu-id="fa7bb-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="fa7bb-107">S_OK</span></span>
  
> <span data-ttu-id="fa7bb-108">Клиент MAPI выйти из сразу же готов поставщика MAPI.</span><span class="sxs-lookup"><span data-stu-id="fa7bb-108">The MAPI provider is ready for the MAPI client to exit immediately.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="fa7bb-109">См. также</span><span class="sxs-lookup"><span data-stu-id="fa7bb-109">See also</span></span>



[<span data-ttu-id="fa7bb-110">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fa7bb-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="fa7bb-111">Завершение работы клиента в MAPI</span><span class="sxs-lookup"><span data-stu-id="fa7bb-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

