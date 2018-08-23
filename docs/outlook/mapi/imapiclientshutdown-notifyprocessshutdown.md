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
ms.openlocfilehash: 1c66032788758b04558a37a4c35ff4dd6c702fa2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568268"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a><span data-ttu-id="df0a3-103">IMAPIClientShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="df0a3-103">IMAPIClientShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="df0a3-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df0a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df0a3-105">Показывает завершена намерения клиент MAPI для продолжения.</span><span class="sxs-lookup"><span data-stu-id="df0a3-105">Indicates the intention of the MAPI client to proceed with shut down.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="df0a3-106">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="df0a3-106">Return value</span></span>

<span data-ttu-id="df0a3-107">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="df0a3-107">S_OK</span></span>
  
> <span data-ttu-id="df0a3-108">Подсистема MAPI пытается уведомить загруженных поставщики MAPI, что клиент MAPI требуется выполнить быстрое завершение работы.</span><span class="sxs-lookup"><span data-stu-id="df0a3-108">The MAPI subsystem has attempted to notify loaded MAPI providers that the MAPI client is going to do a fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="df0a3-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="df0a3-109">Remarks</span></span>

<span data-ttu-id="df0a3-110">Чтобы избежать потери данных из быстрое завершение работы клиента MAPI, клиенты MAPI должны вызывать методы **IMAPIClientShutdown::NotifyProcessShutdown** и [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) , основанные на значение S_OK результата, возвращаемого в подсистеме MAPI в метод [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="df0a3-110">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the **IMAPIClientShutdown::NotifyProcessShutdown** and [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="df0a3-111">Для получения дополнительных сведений см [Советы и рекомендации по быстрое завершение работы](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="df0a3-111">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="df0a3-112">См. также</span><span class="sxs-lookup"><span data-stu-id="df0a3-112">See also</span></span>



[<span data-ttu-id="df0a3-113">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="df0a3-113">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="df0a3-114">Завершение работы клиента в MAPI</span><span class="sxs-lookup"><span data-stu-id="df0a3-114">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

