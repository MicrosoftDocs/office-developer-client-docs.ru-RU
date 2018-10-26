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
ms.openlocfilehash: 35dfc7af9852609dcfcc3fcb9d65ec2e4afa9632
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579524"
---
# <a name="imapiofflinemgrunadvise"></a><span data-ttu-id="4e9a9-103">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="4e9a9-103">IMAPIOfflineMgr::Unadvise</span></span>

  
  
<span data-ttu-id="4e9a9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e9a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e9a9-105">Отменяет обратных вызовов для объекта в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="4e9a9-105">Cancels callbacks for an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="4e9a9-106">���������</span><span class="sxs-lookup"><span data-stu-id="4e9a9-106">Parameters</span></span>

 <span data-ttu-id="4e9a9-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4e9a9-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4e9a9-108">[in] Флаги для отмены обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="4e9a9-108">[in] Flags for canceling callback.</span></span> <span data-ttu-id="4e9a9-109">Поддерживается только значение MAPIOFFLINE_UNADVISE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="4e9a9-109">Only the value MAPIOFFLINE_UNADVISE_DEFAULT is supported.</span></span>
    
 <span data-ttu-id="4e9a9-110">_ulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="4e9a9-110">_ulAdviseToken_</span></span>
  
> <span data-ttu-id="4e9a9-111">[in] Маркер уведомлений, определяющий регистрацию обратного вызова, который должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="4e9a9-111">[in] An advise token that identifies the callback registration that is to be canceled.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4e9a9-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4e9a9-112">Return value</span></span>

<span data-ttu-id="4e9a9-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="4e9a9-113">S_OK</span></span>
  
> <span data-ttu-id="4e9a9-114">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="4e9a9-114">The call was successful.</span></span> <span data-ttu-id="4e9a9-115">Этот вызов должен возвращать значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="4e9a9-115">This call must return S_OK.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4e9a9-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="4e9a9-116">Remarks</span></span>

<span data-ttu-id="4e9a9-117">Удаляет регистрацию для обратного вызова, которая была связана с *ulAdviseToken* возвращаются из предыдущего вызова **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="4e9a9-117">Removes the registration for the callback that was associated with  *ulAdviseToken*  returned from a prior call to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="4e9a9-118">Использует объект **IMAPIOfflineMgr** для освобождения ссылку на объект **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** , связанный с *ulAdviseToken* .</span><span class="sxs-lookup"><span data-stu-id="4e9a9-118">Causes the **IMAPIOfflineMgr** object to release its reference on the **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** object associated with  *ulAdviseToken*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4e9a9-119">См. также</span><span class="sxs-lookup"><span data-stu-id="4e9a9-119">See also</span></span>



[<span data-ttu-id="4e9a9-120">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="4e9a9-120">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="4e9a9-121">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="4e9a9-121">MAPI Constants</span></span>](mapi-constants.md)

