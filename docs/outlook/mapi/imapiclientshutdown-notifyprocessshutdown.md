---
title: Имапиклиентшутдовннотифипроцессшутдовн
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
ms.openlocfilehash: 6eef3047368caca5bd932e19738b1d996c3ff28a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351361"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a><span data-ttu-id="f8ed2-103">IMAPIClientShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="f8ed2-103">IMAPIClientShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="f8ed2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8ed2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8ed2-105">Указывает на намерение клиента MAPI выполнить завершение работы.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-105">Indicates the intention of the MAPI client to proceed with shut down.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="f8ed2-106">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8ed2-106">Return value</span></span>

<span data-ttu-id="f8ed2-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="f8ed2-107">S_OK</span></span>
  
> <span data-ttu-id="f8ed2-108">Подсистема MAPI попыталась уведомить загруженных поставщиков MAPI о том, что клиент MAPI будет выполнять быстрое завершение работы.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-108">The MAPI subsystem has attempted to notify loaded MAPI providers that the MAPI client is going to do a fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f8ed2-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="f8ed2-109">Remarks</span></span>

<span data-ttu-id="f8ed2-110">Чтобы избежать потери данных при быстром завершении работы клиента MAPI, клиенты MAPI должны вызывать методы **метод imapiclientshutdown:: нотифипроцессшутдовн** и [метод imapiclientshutdown::D офастшутдовн](imapiclientshutdown-dofastshutdown.md) на основе результата S_OK, возвращаемОГО подсистемой MAPI в метод [метод imapiclientshutdown:: QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="f8ed2-110">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the **IMAPIClientShutdown::NotifyProcessShutdown** and [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="f8ed2-111">Для получения дополнительных сведений ознакомьтесь с рекомендациями [по быстроМу завершенИю работы](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="f8ed2-111">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f8ed2-112">См. также</span><span class="sxs-lookup"><span data-stu-id="f8ed2-112">See also</span></span>



[<span data-ttu-id="f8ed2-113">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f8ed2-113">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="f8ed2-114">Завершение работы клиента в MAPI</span><span class="sxs-lookup"><span data-stu-id="f8ed2-114">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

