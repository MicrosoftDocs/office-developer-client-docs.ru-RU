---
title: Имапипровидершутдовннотифипроцессшутдовн
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326392"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a><span data-ttu-id="c959c-103">IMAPIProviderShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="c959c-103">IMAPIProviderShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="c959c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c959c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c959c-105">Указывает поставщику MAPI, что клиент MAPI планирует выполнить быстрое завершение работы, чтобы поставщик мог выполнять действия для предотвращения потери данных.</span><span class="sxs-lookup"><span data-stu-id="c959c-105">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="c959c-106">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c959c-106">Return value</span></span>

<span data-ttu-id="c959c-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="c959c-107">S_OK</span></span>
  
> <span data-ttu-id="c959c-108">Поставщик MAPI принимает действия по предотвращению потери данных при завершении работы клиента MAPI.</span><span class="sxs-lookup"><span data-stu-id="c959c-108">The MAPI provider is taking actions to prevent data loss when the MAPI client shuts down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c959c-109">См. также</span><span class="sxs-lookup"><span data-stu-id="c959c-109">See also</span></span>



[<span data-ttu-id="c959c-110">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c959c-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="c959c-111">Завершение работы клиента в MAPI</span><span class="sxs-lookup"><span data-stu-id="c959c-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

