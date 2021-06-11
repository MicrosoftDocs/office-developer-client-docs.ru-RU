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
ms.openlocfilehash: dbf9f9f73d9e3860b482f81fb942673e6d373267
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439613"
---
# <a name="imapigetsessiongetmapisession"></a><span data-ttu-id="7b122-103">IMAPIGetSession::GetMAPISession</span><span class="sxs-lookup"><span data-stu-id="7b122-103">IMAPIGetSession::GetMAPISession</span></span>

  
  
<span data-ttu-id="7b122-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b122-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b122-105">Возвращает указатель на сеанс MAPI, связанный с объектом поддержки MAPI.</span><span class="sxs-lookup"><span data-stu-id="7b122-105">Returns a pointer to the MAPI session associated with the MAPI support object.</span></span>
  
```cpp
HRESULT GetMAPISession(
  LPUNKNOWN *  lppSession
);
```

## <a name="parameters"></a><span data-ttu-id="7b122-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="7b122-106">Parameters</span></span>

 <span data-ttu-id="7b122-107">_lppSession_</span><span class="sxs-lookup"><span data-stu-id="7b122-107">_lppSession_</span></span>
  
> <span data-ttu-id="7b122-108">[вышел] Указатель на текущий сеанс MAPI.</span><span class="sxs-lookup"><span data-stu-id="7b122-108">[out] A pointer to the current MAPI session.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b122-109">См. также</span><span class="sxs-lookup"><span data-stu-id="7b122-109">See also</span></span>



[<span data-ttu-id="7b122-110">IMAPIGetSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7b122-110">IMAPIGetSession : IUnknown</span></span>](imapigetsessioniunknown.md)


[<span data-ttu-id="7b122-111">Обзор объектов поддержки</span><span class="sxs-lookup"><span data-stu-id="7b122-111">Support Object Overview</span></span>](support-object-overview.md)

