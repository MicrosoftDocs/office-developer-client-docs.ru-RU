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
ms.openlocfilehash: b52dcd87c8714ad59db560a5ae4a8300f9cc83ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809008"
---
# <a name="imapiofflinemgrunadvise"></a><span data-ttu-id="e0304-103">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="e0304-103">IMAPIOfflineMgr::Unadvise</span></span>

  
  
<span data-ttu-id="e0304-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e0304-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e0304-105">Отменяет обратных вызовов для объекта в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="e0304-105">Cancels callbacks for an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="e0304-106">���������</span><span class="sxs-lookup"><span data-stu-id="e0304-106">Parameters</span></span>

 <span data-ttu-id="e0304-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e0304-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e0304-108">[in] Флаги для отмены обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="e0304-108">[in] Flags for canceling callback.</span></span> <span data-ttu-id="e0304-109">Поддерживается только значение MAPIOFFLINE_UNADVISE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="e0304-109">Only the value MAPIOFFLINE_UNADVISE_DEFAULT is supported.</span></span>
    
 <span data-ttu-id="e0304-110">_ulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="e0304-110">_ulAdviseToken_</span></span>
  
> <span data-ttu-id="e0304-111">[in] Маркер уведомлений, определяющий регистрацию обратного вызова, который должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="e0304-111">[in] An advise token that identifies the callback registration that is to be canceled.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e0304-112">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="e0304-112">Return value</span></span>

<span data-ttu-id="e0304-113">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="e0304-113">S_OK</span></span>
  
> <span data-ttu-id="e0304-114">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="e0304-114">The call was successful.</span></span> <span data-ttu-id="e0304-115">Этот вызов должен возвращать значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="e0304-115">This call must return S_OK.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e0304-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="e0304-116">Remarks</span></span>

<span data-ttu-id="e0304-117">Удаляет регистрацию для обратного вызова, которая была связана с *ulAdviseToken* возвращаются из предыдущего вызова **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="e0304-117">Removes the registration for the callback that was associated with  *ulAdviseToken*  returned from a prior call to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="e0304-118">Использует объект **IMAPIOfflineMgr** для освобождения ссылку на объект **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** , связанный с *ulAdviseToken* .</span><span class="sxs-lookup"><span data-stu-id="e0304-118">Causes the **IMAPIOfflineMgr** object to release its reference on the **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** object associated with  *ulAdviseToken*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e0304-119">См. также</span><span class="sxs-lookup"><span data-stu-id="e0304-119">See also</span></span>



[<span data-ttu-id="e0304-120">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="e0304-120">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="e0304-121">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="e0304-121">MAPI Constants</span></span>](mapi-constants.md)

