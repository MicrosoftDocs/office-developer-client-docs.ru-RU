---
title: IMAPIOfflineMgrUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Unadvise
api_type:
- COM
ms.assetid: 250b9137-facb-81a2-41b1-96a57366c04e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 800f79179f999ba193d4177abb7341095b8b896d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404857"
---
# <a name="imapiofflinemgrunadvise"></a><span data-ttu-id="a2488-103">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="a2488-103">IMAPIOfflineMgr::Unadvise</span></span>

  
  
<span data-ttu-id="a2488-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2488-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2488-105">Отменяет вызовы для автономного объекта.</span><span class="sxs-lookup"><span data-stu-id="a2488-105">Cancels callbacks for an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="a2488-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="a2488-106">Parameters</span></span>

 <span data-ttu-id="a2488-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a2488-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a2488-108">[in] Флаги для отмены вызова.</span><span class="sxs-lookup"><span data-stu-id="a2488-108">[in] Flags for canceling callback.</span></span> <span data-ttu-id="a2488-109">Поддерживается только MAPIOFFLINE_UNADVISE_DEFAULT значение.</span><span class="sxs-lookup"><span data-stu-id="a2488-109">Only the value MAPIOFFLINE_UNADVISE_DEFAULT is supported.</span></span>
    
 <span data-ttu-id="a2488-110">_ulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="a2488-110">_ulAdviseToken_</span></span>
  
> <span data-ttu-id="a2488-111">[in] Маркер рекомендации, идентифицирует отменяемую регистрацию вызова.</span><span class="sxs-lookup"><span data-stu-id="a2488-111">[in] An advise token that identifies the callback registration that is to be canceled.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a2488-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a2488-112">Return value</span></span>

<span data-ttu-id="a2488-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="a2488-113">S_OK</span></span>
  
> <span data-ttu-id="a2488-114">Вызов был успешным.</span><span class="sxs-lookup"><span data-stu-id="a2488-114">The call was successful.</span></span> <span data-ttu-id="a2488-115">Этот вызов должен вернуться S_OK.</span><span class="sxs-lookup"><span data-stu-id="a2488-115">This call must return S_OK.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a2488-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="a2488-116">Remarks</span></span>

<span data-ttu-id="a2488-117">Удаляет регистрацию обратного вызова, связанного с  *ulAdviseToken,*  возвращаемого по предварительному вызову **[в IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="a2488-117">Removes the registration for the callback that was associated with  *ulAdviseToken*  returned from a prior call to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="a2488-118">Вызывает **объект IMAPIOfflineMgr** для выпуска ссылки на **[объект IMAPIOfflineNotify,](imapiofflinenotifyiunknown.md)** связанный с *ulAdviseToken.*</span><span class="sxs-lookup"><span data-stu-id="a2488-118">Causes the **IMAPIOfflineMgr** object to release its reference on the **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** object associated with  *ulAdviseToken*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a2488-119">См. также</span><span class="sxs-lookup"><span data-stu-id="a2488-119">See also</span></span>



[<span data-ttu-id="a2488-120">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="a2488-120">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="a2488-121">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="a2488-121">MAPI Constants</span></span>](mapi-constants.md)

