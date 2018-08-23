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
# <a name="imapiofflinemgrunadvise"></a><span data-ttu-id="ccfbc-103">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="ccfbc-103">IMAPIOfflineMgr::Unadvise</span></span>

  
  
<span data-ttu-id="ccfbc-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ccfbc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ccfbc-105">Отменяет обратных вызовов для объекта в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="ccfbc-105">Cancels callbacks for an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="ccfbc-106">���������</span><span class="sxs-lookup"><span data-stu-id="ccfbc-106">Parameters</span></span>

 <span data-ttu-id="ccfbc-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ccfbc-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ccfbc-108">[in] Флаги для отмены обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="ccfbc-108">[in] Flags for canceling callback.</span></span> <span data-ttu-id="ccfbc-109">Поддерживается только значение MAPIOFFLINE_UNADVISE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="ccfbc-109">Only the value MAPIOFFLINE_UNADVISE_DEFAULT is supported.</span></span>
    
 <span data-ttu-id="ccfbc-110">_ulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="ccfbc-110">_ulAdviseToken_</span></span>
  
> <span data-ttu-id="ccfbc-111">[in] Маркер уведомлений, определяющий регистрацию обратного вызова, который должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="ccfbc-111">[in] An advise token that identifies the callback registration that is to be canceled.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ccfbc-112">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="ccfbc-112">Return value</span></span>

<span data-ttu-id="ccfbc-113">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="ccfbc-113">S_OK</span></span>
  
> <span data-ttu-id="ccfbc-114">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="ccfbc-114">The call was successful.</span></span> <span data-ttu-id="ccfbc-115">Этот вызов должен возвращать значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="ccfbc-115">This call must return S_OK.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ccfbc-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="ccfbc-116">Remarks</span></span>

<span data-ttu-id="ccfbc-117">Удаляет регистрацию для обратного вызова, которая была связана с *ulAdviseToken* возвращаются из предыдущего вызова **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="ccfbc-117">Removes the registration for the callback that was associated with  *ulAdviseToken*  returned from a prior call to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="ccfbc-118">Использует объект **IMAPIOfflineMgr** для освобождения ссылку на объект **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** , связанный с *ulAdviseToken* .</span><span class="sxs-lookup"><span data-stu-id="ccfbc-118">Causes the **IMAPIOfflineMgr** object to release its reference on the **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** object associated with  *ulAdviseToken*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ccfbc-119">См. также</span><span class="sxs-lookup"><span data-stu-id="ccfbc-119">See also</span></span>



[<span data-ttu-id="ccfbc-120">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="ccfbc-120">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="ccfbc-121">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="ccfbc-121">MAPI Constants</span></span>](mapi-constants.md)

