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
ms.openlocfilehash: 6a76488f56f9d1eb1b344c01de2615627dd5d3ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418150"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a><span data-ttu-id="76b0a-103">IMAPIClientShutdown::QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="76b0a-103">IMAPIClientShutdown::QueryFastShutdown</span></span>

  
  
<span data-ttu-id="76b0a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76b0a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76b0a-105">Запрашивает подсистему MAPI для поддержки быстрого отключения, предоставляемую загруженными поставщиками MAPI.</span><span class="sxs-lookup"><span data-stu-id="76b0a-105">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="76b0a-106">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="76b0a-106">Return value</span></span>

<span data-ttu-id="76b0a-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="76b0a-107">S_OK</span></span>
  
> <span data-ttu-id="76b0a-108">Подсистема MAPI поддерживает клиента MAPI для быстрого отключения.</span><span class="sxs-lookup"><span data-stu-id="76b0a-108">The MAPI subsystem supports the MAPI client to do fast shutdown.</span></span>
    
<span data-ttu-id="76b0a-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="76b0a-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="76b0a-110">Поставщик MAPI не поддерживает клиента MAPI для быстрого отключения.</span><span class="sxs-lookup"><span data-stu-id="76b0a-110">The MAPI provider does not support the MAPI client to do fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="76b0a-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="76b0a-111">Remarks</span></span>

<span data-ttu-id="76b0a-112">Поддерживает ли подсистема MAPI клиента MAPI для быстрого отключения, зависит от параметра реестра Windows пользователя или поведения клиента MAPI по умолчанию для быстрого отключения.</span><span class="sxs-lookup"><span data-stu-id="76b0a-112">Whether the MAPI subsystem supports the MAPI client to do fast shutdown depends on the user's Windows registry setting or the default behavior of the MAPI client for fast shutdown.</span></span> <span data-ttu-id="76b0a-113">Это также зависит от способности загруженных поставщиков MAPI поддерживать быстрое отключение.</span><span class="sxs-lookup"><span data-stu-id="76b0a-113">It also depends on the ability of the loaded MAPI providers to support fast shutdown.</span></span> <span data-ttu-id="76b0a-114">Дополнительные сведения см. в [меню Fast Shutdown User Options.](fast-shutdown-user-options.md)</span><span class="sxs-lookup"><span data-stu-id="76b0a-114">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="76b0a-115">См. также</span><span class="sxs-lookup"><span data-stu-id="76b0a-115">See also</span></span>



[<span data-ttu-id="76b0a-116">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="76b0a-116">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="76b0a-117">Завершение работы клиента в MAPI</span><span class="sxs-lookup"><span data-stu-id="76b0a-117">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

