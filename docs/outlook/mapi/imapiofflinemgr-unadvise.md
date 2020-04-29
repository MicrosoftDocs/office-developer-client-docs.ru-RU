---
title: имапиоффлинемгрунадвисе
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
# <a name="imapiofflinemgrunadvise"></a><span data-ttu-id="44d83-103">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="44d83-103">IMAPIOfflineMgr::Unadvise</span></span>

  
  
<span data-ttu-id="44d83-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44d83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44d83-105">Отменяет обратные вызовы для автономного объекта.</span><span class="sxs-lookup"><span data-stu-id="44d83-105">Cancels callbacks for an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="44d83-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="44d83-106">Parameters</span></span>

 <span data-ttu-id="44d83-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="44d83-107">_ulFlags_</span></span>
  
> <span data-ttu-id="44d83-108">возврата Флаги для отмены обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="44d83-108">[in] Flags for canceling callback.</span></span> <span data-ttu-id="44d83-109">Поддерживается только значение MAPIOFFLINE_UNADVISE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="44d83-109">Only the value MAPIOFFLINE_UNADVISE_DEFAULT is supported.</span></span>
    
 <span data-ttu-id="44d83-110">_уладвисетокен_</span><span class="sxs-lookup"><span data-stu-id="44d83-110">_ulAdviseToken_</span></span>
  
> <span data-ttu-id="44d83-111">возврата Токен advise, определяющий регистрацию обратного вызова, которая должна быть отменена.</span><span class="sxs-lookup"><span data-stu-id="44d83-111">[in] An advise token that identifies the callback registration that is to be canceled.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="44d83-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44d83-112">Return value</span></span>

<span data-ttu-id="44d83-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="44d83-113">S_OK</span></span>
  
> <span data-ttu-id="44d83-114">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="44d83-114">The call was successful.</span></span> <span data-ttu-id="44d83-115">Этот вызов должен возвращать S_OK.</span><span class="sxs-lookup"><span data-stu-id="44d83-115">This call must return S_OK.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="44d83-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="44d83-116">Remarks</span></span>

<span data-ttu-id="44d83-117">Удаляет регистрацию для обратного вызова, который был связан с *уладвисетокен* , возвращенный при предыдущем вызове метода **[Имапиоффлинемгр:: Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="44d83-117">Removes the registration for the callback that was associated with  *ulAdviseToken*  returned from a prior call to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="44d83-118">Заставляет объект **имапиоффлинемгр** освобождать ссылку на объект **[имапиоффлиненотифи](imapiofflinenotifyiunknown.md)** , связанный с *уладвисетокен* .</span><span class="sxs-lookup"><span data-stu-id="44d83-118">Causes the **IMAPIOfflineMgr** object to release its reference on the **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** object associated with  *ulAdviseToken*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="44d83-119">См. также</span><span class="sxs-lookup"><span data-stu-id="44d83-119">See also</span></span>



[<span data-ttu-id="44d83-120">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="44d83-120">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="44d83-121">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="44d83-121">MAPI Constants</span></span>](mapi-constants.md)

