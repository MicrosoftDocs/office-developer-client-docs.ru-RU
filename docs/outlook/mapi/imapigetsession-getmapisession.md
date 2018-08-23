---
title: IMAPIGetSessionGetMAPISession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIGetSession.GetMAPISession
api_type:
- COM
ms.assetid: 581db5d9-35f7-43ad-aef3-a5d5da310150
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7176f3547c18ec72e4bfc0a749b3814d1e906b7b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577039"
---
# <a name="imapigetsessiongetmapisession"></a><span data-ttu-id="a19f4-103">IMAPIGetSession::GetMAPISession</span><span class="sxs-lookup"><span data-stu-id="a19f4-103">IMAPIGetSession::GetMAPISession</span></span>

  
  
<span data-ttu-id="a19f4-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a19f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a19f4-105">Возвращает указатель на сеанс MAPI, связанного с объектом поддержки MAPI.</span><span class="sxs-lookup"><span data-stu-id="a19f4-105">Returns a pointer to the MAPI session associated with the MAPI support object.</span></span>
  
```cpp
HRESULT GetMAPISession(
  LPUNKNOWN *  lppSession
);
```

## <a name="parameters"></a><span data-ttu-id="a19f4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a19f4-106">Parameters</span></span>

 <span data-ttu-id="a19f4-107">_lppSession_</span><span class="sxs-lookup"><span data-stu-id="a19f4-107">_lppSession_</span></span>
  
> <span data-ttu-id="a19f4-108">[out] Указатель на текущий сеанс MAPI.</span><span class="sxs-lookup"><span data-stu-id="a19f4-108">[out] A pointer to the current MAPI session.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a19f4-109">См. также</span><span class="sxs-lookup"><span data-stu-id="a19f4-109">See also</span></span>



[<span data-ttu-id="a19f4-110">IMAPIGetSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a19f4-110">IMAPIGetSession : IUnknown</span></span>](imapigetsessioniunknown.md)


[<span data-ttu-id="a19f4-111">Обзор поддержки объектов</span><span class="sxs-lookup"><span data-stu-id="a19f4-111">Support Object Overview</span></span>](support-object-overview.md)

