---
title: IMAPIClientShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: 42dd7889-5e00-419a-91e7-8350be4efd35
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 04a9b631c3a4f33282bce44e06d92e089349c76b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808815"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a><span data-ttu-id="ac600-103">IMAPIClientShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="ac600-103">IMAPIClientShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="ac600-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ac600-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ac600-105">Показывает завершена намерения клиент MAPI для продолжения.</span><span class="sxs-lookup"><span data-stu-id="ac600-105">Indicates the intention of the MAPI client to proceed with shut down.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="ac600-106">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="ac600-106">Return value</span></span>

<span data-ttu-id="ac600-107">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="ac600-107">S_OK</span></span>
  
> <span data-ttu-id="ac600-108">Подсистема MAPI пытается уведомить загруженных поставщики MAPI, что клиент MAPI требуется выполнить быстрое завершение работы.</span><span class="sxs-lookup"><span data-stu-id="ac600-108">The MAPI subsystem has attempted to notify loaded MAPI providers that the MAPI client is going to do a fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ac600-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="ac600-109">Remarks</span></span>

<span data-ttu-id="ac600-110">Чтобы избежать потери данных из быстрое завершение работы клиента MAPI, клиенты MAPI должны вызывать методы **IMAPIClientShutdown::NotifyProcessShutdown** и [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) , основанные на значение S_OK результата, возвращаемого в подсистеме MAPI в метод [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="ac600-110">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the **IMAPIClientShutdown::NotifyProcessShutdown** and [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="ac600-111">Для получения дополнительных сведений см [Советы и рекомендации по быстрое завершение работы](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="ac600-111">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ac600-112">См. также</span><span class="sxs-lookup"><span data-stu-id="ac600-112">See also</span></span>



[<span data-ttu-id="ac600-113">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ac600-113">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="ac600-114">Завершение работы клиента в MAPI</span><span class="sxs-lookup"><span data-stu-id="ac600-114">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

