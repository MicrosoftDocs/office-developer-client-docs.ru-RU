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
# <a name="imapiofflinemgrunadvise"></a><span data-ttu-id="044db-103">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="044db-103">IMAPIOfflineMgr::Unadvise</span></span>

  
  
<span data-ttu-id="044db-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="044db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="044db-105">Отменяет вызовы для автономного объекта.</span><span class="sxs-lookup"><span data-stu-id="044db-105">Cancels callbacks for an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="044db-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="044db-106">Parameters</span></span>

 <span data-ttu-id="044db-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="044db-107">_ulFlags_</span></span>
  
> <span data-ttu-id="044db-108">[in] Флаги для отмены вызова.</span><span class="sxs-lookup"><span data-stu-id="044db-108">[in] Flags for canceling callback.</span></span> <span data-ttu-id="044db-109">Поддерживается только MAPIOFFLINE_UNADVISE_DEFAULT значение.</span><span class="sxs-lookup"><span data-stu-id="044db-109">Only the value MAPIOFFLINE_UNADVISE_DEFAULT is supported.</span></span>
    
 <span data-ttu-id="044db-110">_ulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="044db-110">_ulAdviseToken_</span></span>
  
> <span data-ttu-id="044db-111">[in] Маркер консультации, определяя отменяемую регистрацию вызова.</span><span class="sxs-lookup"><span data-stu-id="044db-111">[in] An advise token that identifies the callback registration that is to be canceled.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="044db-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="044db-112">Return value</span></span>

<span data-ttu-id="044db-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="044db-113">S_OK</span></span>
  
> <span data-ttu-id="044db-114">Вызов был успешным.</span><span class="sxs-lookup"><span data-stu-id="044db-114">The call was successful.</span></span> <span data-ttu-id="044db-115">Этот вызов должен возвращать S_OK.</span><span class="sxs-lookup"><span data-stu-id="044db-115">This call must return S_OK.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="044db-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="044db-116">Remarks</span></span>

<span data-ttu-id="044db-117">Удаляет регистрацию обратного вызова, связанного с *ulAdviseToken,* возвращенного при предыдущем вызове **[IMAPIOfflineMgr::Advise.](imapiofflinemgr-advise.md)**</span><span class="sxs-lookup"><span data-stu-id="044db-117">Removes the registration for the callback that was associated with  *ulAdviseToken*  returned from a prior call to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="044db-118">Заставляет объект **IMAPIOfflineMgr** освободить ссылку на объект **[IMAPIOfflineNotify,](imapiofflinenotifyiunknown.md)** связанный с *ulAdviseToken.*</span><span class="sxs-lookup"><span data-stu-id="044db-118">Causes the **IMAPIOfflineMgr** object to release its reference on the **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** object associated with  *ulAdviseToken*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="044db-119">См. также</span><span class="sxs-lookup"><span data-stu-id="044db-119">See also</span></span>



[<span data-ttu-id="044db-120">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="044db-120">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="044db-121">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="044db-121">MAPI Constants</span></span>](mapi-constants.md)

