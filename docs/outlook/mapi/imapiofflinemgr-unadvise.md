---
title: Имапиоффлинемгрунадвисе
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321219"
---
# <a name="imapiofflinemgrunadvise"></a><span data-ttu-id="1ad1b-103">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="1ad1b-103">IMAPIOfflineMgr::Unadvise</span></span>

  
  
<span data-ttu-id="1ad1b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ad1b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ad1b-105">ОтМеняет обратные вызовы для автономного объекта.</span><span class="sxs-lookup"><span data-stu-id="1ad1b-105">Cancels callbacks for an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="1ad1b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ad1b-106">Parameters</span></span>

 <span data-ttu-id="1ad1b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1ad1b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1ad1b-108">возврата Флаги для отмены обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="1ad1b-108">[in] Flags for canceling callback.</span></span> <span data-ttu-id="1ad1b-109">Поддерживается только значение МАПИОФФЛИНЕ_УНАДВИСЕ_ДЕФАУЛТ.</span><span class="sxs-lookup"><span data-stu-id="1ad1b-109">Only the value MAPIOFFLINE_UNADVISE_DEFAULT is supported.</span></span>
    
 <span data-ttu-id="1ad1b-110">_Уладвисетокен_</span><span class="sxs-lookup"><span data-stu-id="1ad1b-110">_ulAdviseToken_</span></span>
  
> <span data-ttu-id="1ad1b-111">возврата Токен advise, определяющий регистрацию обратного вызова, которая должна быть отменена.</span><span class="sxs-lookup"><span data-stu-id="1ad1b-111">[in] An advise token that identifies the callback registration that is to be canceled.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1ad1b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ad1b-112">Return value</span></span>

<span data-ttu-id="1ad1b-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="1ad1b-113">S_OK</span></span>
  
> <span data-ttu-id="1ad1b-114">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="1ad1b-114">The call was successful.</span></span> <span data-ttu-id="1ad1b-115">Этот вызов должен возвращать значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="1ad1b-115">This call must return S_OK.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1ad1b-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="1ad1b-116">Remarks</span></span>

<span data-ttu-id="1ad1b-117">Удаляет регистрацию для обратного вызова, который был связан с *уладвисетокен* , возвращенный при предыдущем вызове метода **[Имапиоффлинемгр:: Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="1ad1b-117">Removes the registration for the callback that was associated with  *ulAdviseToken*  returned from a prior call to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="1ad1b-118">Заставляет объект **имапиоффлинемгр** освобождать ссылку на объект **[имапиоффлиненотифи](imapiofflinenotifyiunknown.md)** , связанный с *уладвисетокен* .</span><span class="sxs-lookup"><span data-stu-id="1ad1b-118">Causes the **IMAPIOfflineMgr** object to release its reference on the **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** object associated with  *ulAdviseToken*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1ad1b-119">См. также</span><span class="sxs-lookup"><span data-stu-id="1ad1b-119">See also</span></span>



[<span data-ttu-id="1ad1b-120">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="1ad1b-120">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="1ad1b-121">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="1ad1b-121">MAPI Constants</span></span>](mapi-constants.md)

