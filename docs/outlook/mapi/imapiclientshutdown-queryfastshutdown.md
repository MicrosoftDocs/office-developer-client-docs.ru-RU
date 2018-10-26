---
title: IMAPIClientShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: b743b5b6-4a7c-46b8-99eb-afd13ee947db
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 784a2f497811ba7c4ba0abf260ff32fde75de76a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584935"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a><span data-ttu-id="a4494-103">IMAPIClientShutdown::QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="a4494-103">IMAPIClientShutdown::QueryFastShutdown</span></span>

  
  
<span data-ttu-id="a4494-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4494-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4494-105">Запросы в подсистеме MAPI для быстрое завершение работы поддерживают, предоставленные загруженных поставщики MAPI.</span><span class="sxs-lookup"><span data-stu-id="a4494-105">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="a4494-106">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4494-106">Return value</span></span>

<span data-ttu-id="a4494-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="a4494-107">S_OK</span></span>
  
> <span data-ttu-id="a4494-108">Подсистема MAPI поддерживает быстрое завершение работы клиента MAPI.</span><span class="sxs-lookup"><span data-stu-id="a4494-108">The MAPI subsystem supports the MAPI client to do fast shutdown.</span></span>
    
<span data-ttu-id="a4494-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="a4494-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="a4494-110">Поставщик MAPI не поддерживает быстрое завершение работы клиента MAPI.</span><span class="sxs-lookup"><span data-stu-id="a4494-110">The MAPI provider does not support the MAPI client to do fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a4494-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="a4494-111">Remarks</span></span>

<span data-ttu-id="a4494-112">Поддерживает ли подсистемы MAPI клиенту MAPI быстрое завершение работы зависит от параметры реестра Windows и поведение по умолчанию для быстрое завершение работы клиента MAPI.</span><span class="sxs-lookup"><span data-stu-id="a4494-112">Whether the MAPI subsystem supports the MAPI client to do fast shutdown depends on the user's Windows registry setting or the default behavior of the MAPI client for fast shutdown.</span></span> <span data-ttu-id="a4494-113">Он также зависит от возможность загрузки поставщики MAPI поддерживает быстрое завершение работы.</span><span class="sxs-lookup"><span data-stu-id="a4494-113">It also depends on the ability of the loaded MAPI providers to support fast shutdown.</span></span> <span data-ttu-id="a4494-114">Для получения дополнительных сведений см [Fast параметры завершения работы пользователя](fast-shutdown-user-options.md).</span><span class="sxs-lookup"><span data-stu-id="a4494-114">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a4494-115">См. также</span><span class="sxs-lookup"><span data-stu-id="a4494-115">See also</span></span>



[<span data-ttu-id="a4494-116">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a4494-116">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="a4494-117">Завершение работы клиента в MAPI</span><span class="sxs-lookup"><span data-stu-id="a4494-117">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

