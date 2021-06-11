---
title: IMAPIClientShutdownDoFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: 310cba9a-a343-484d-a029-fcd51b731460
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 32a0051207ae34f919523fbfe3e01601b7ea5d2a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408686"
---
# <a name="imapiclientshutdowndofastshutdown"></a><span data-ttu-id="24c3e-103">IMAPIClientShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="24c3e-103">IMAPIClientShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="24c3e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24c3e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24c3e-105">Указывает намерение клиента MAPI немедленно выйти из клиентского процесса.</span><span class="sxs-lookup"><span data-stu-id="24c3e-105">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="24c3e-106">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24c3e-106">Return value</span></span>

<span data-ttu-id="24c3e-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="24c3e-107">S_OK</span></span>
  
> <span data-ttu-id="24c3e-108">Подсистема MAPI указала загруженным поставщикам MAPI, что клиент MAPI немедленно выходит, и поставщики MAPI готовы к выходу клиента.</span><span class="sxs-lookup"><span data-stu-id="24c3e-108">The MAPI subsystem has indicated to loaded MAPI providers that the MAPI client is exiting immediately, and the MAPI providers are ready for the client exit.</span></span>
    
<span data-ttu-id="24c3e-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="24c3e-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="24c3e-110">Подсистема MAPI не поддерживает быстрое отключение клиента.</span><span class="sxs-lookup"><span data-stu-id="24c3e-110">The MAPI subsystem does not support client fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="24c3e-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="24c3e-111">Remarks</span></span>

<span data-ttu-id="24c3e-112">Чтобы избежать потери данных при быстром закрытии клиента MAPI, клиенты MAPI должны вызвать [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) и **IMAPIClientShutdown::D oFastShutdown** на основе результата S_OK, возвращенного подсистемой MAPI в методе [IMAPIClientShutdown:QueryFastShutdown.](imapiclientshutdown-queryfastshutdown.md)</span><span class="sxs-lookup"><span data-stu-id="24c3e-112">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) and **IMAPIClientShutdown::DoFastShutdown** methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="24c3e-113">Дополнительные сведения см. в [дополнительных сведениях о лучших практиках быстрого отключения.](best-practices-for-fast-shutdown.md)</span><span class="sxs-lookup"><span data-stu-id="24c3e-113">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="24c3e-114">См. также</span><span class="sxs-lookup"><span data-stu-id="24c3e-114">See also</span></span>



[<span data-ttu-id="24c3e-115">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="24c3e-115">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="24c3e-116">Завершение работы клиента в MAPI</span><span class="sxs-lookup"><span data-stu-id="24c3e-116">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

