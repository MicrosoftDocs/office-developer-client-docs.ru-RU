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
ms.openlocfilehash: 41c4ee65ce6ae8f2e0d978f1e2bd95adb4f5872a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575177"
---
# <a name="imapiclientshutdowndofastshutdown"></a><span data-ttu-id="b8a26-103">IMAPIClientShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="b8a26-103">IMAPIClientShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="b8a26-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8a26-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8a26-105">Указывает намерения клиент MAPI, чтобы выйти из клиентского процесса немедленно.</span><span class="sxs-lookup"><span data-stu-id="b8a26-105">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="b8a26-106">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8a26-106">Return value</span></span>

<span data-ttu-id="b8a26-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="b8a26-107">S_OK</span></span>
  
> <span data-ttu-id="b8a26-108">Подсистема MAPI указал для загруженных поставщики MAPI, что немедленно завершает работу клиент MAPI и поставщики MAPI все готово для выхода клиента.</span><span class="sxs-lookup"><span data-stu-id="b8a26-108">The MAPI subsystem has indicated to loaded MAPI providers that the MAPI client is exiting immediately, and the MAPI providers are ready for the client exit.</span></span>
    
<span data-ttu-id="b8a26-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="b8a26-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="b8a26-110">Подсистема MAPI не поддерживает быстрое завершение работы клиента.</span><span class="sxs-lookup"><span data-stu-id="b8a26-110">The MAPI subsystem does not support client fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b8a26-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="b8a26-111">Remarks</span></span>

<span data-ttu-id="b8a26-112">Чтобы избежать потери данных из быстрое завершение работы клиента MAPI, клиенты MAPI должны вызывать методы [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) и **IMAPIClientShutdown::DoFastShutdown** , основанные на значение S_OK результата, возвращаемого в подсистеме MAPI в метод [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="b8a26-112">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) and **IMAPIClientShutdown::DoFastShutdown** methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="b8a26-113">Для получения дополнительных сведений см [Советы и рекомендации по быстрое завершение работы](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="b8a26-113">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b8a26-114">См. также</span><span class="sxs-lookup"><span data-stu-id="b8a26-114">See also</span></span>



[<span data-ttu-id="b8a26-115">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b8a26-115">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="b8a26-116">Завершение работы клиента в MAPI</span><span class="sxs-lookup"><span data-stu-id="b8a26-116">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

