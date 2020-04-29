---
title: имапиоффлинемградвисе
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Advise
api_type:
- COM
ms.assetid: 784b6218-548d-817a-caaa-cf9be6bc3d2f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3ca7fdc39da8d3ee8ecf6f0f253284df10a392e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426921"
---
# <a name="imapiofflinemgradvise"></a><span data-ttu-id="2976f-103">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="2976f-103">IMAPIOfflineMgr::Advise</span></span>

  
  
<span data-ttu-id="2976f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2976f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2976f-105">Регистрирует клиент для получения обратных вызовов в автономном объекте.</span><span class="sxs-lookup"><span data-stu-id="2976f-105">Registers a client to receive callbacks on an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="2976f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2976f-106">Parameters</span></span>

 <span data-ttu-id="2976f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2976f-107">_ulFlags_</span></span>
  
>  <span data-ttu-id="2976f-108">возврата Флаги, которые изменяют поведение.</span><span class="sxs-lookup"><span data-stu-id="2976f-108">[in] Flags that modify behavior.</span></span> <span data-ttu-id="2976f-109">Поддерживается только значение MAPIOFFLINE_ADVISE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="2976f-109">Only the value MAPIOFFLINE_ADVISE_DEFAULT is supported.</span></span> 
    
 <span data-ttu-id="2976f-110">_падвисеинфо_</span><span class="sxs-lookup"><span data-stu-id="2976f-110">_pAdviseInfo_</span></span>
  
> <span data-ttu-id="2976f-111">возврата Сведения о типе обратного вызова, когда для получения обратного вызова, интерфейса обратного вызова для вызывающего абонента и других сведений.</span><span class="sxs-lookup"><span data-stu-id="2976f-111">[in] Information about the type of callback, when to receive a callback, a callback interface for the caller, and other details.</span></span> <span data-ttu-id="2976f-112">Он также содержит маркер клиента, который Outlook использует при отправке последующего обратного вызова для клиентского абонента.</span><span class="sxs-lookup"><span data-stu-id="2976f-112">It also contains a client token that Outlook uses in sending subsequent notification callbacks to the client caller.</span></span>
    
 <span data-ttu-id="2976f-113">_пуладвисетокен_</span><span class="sxs-lookup"><span data-stu-id="2976f-113">_pulAdviseToken_</span></span>
  
> <span data-ttu-id="2976f-114">вышли Токен advise, возвращенный клиентскому абоненту для последовательного отмены обратного вызова для объекта.</span><span class="sxs-lookup"><span data-stu-id="2976f-114">[out] An advise token returned to the client caller for subsequently canceling callback for the object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2976f-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2976f-115">Return value</span></span>

<span data-ttu-id="2976f-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="2976f-116">S_OK</span></span>
  
> <span data-ttu-id="2976f-117">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="2976f-117">The call was successful.</span></span>
    
<span data-ttu-id="2976f-118">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="2976f-118">E_INVALIDARG</span></span>
  
> <span data-ttu-id="2976f-119">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="2976f-119">An invalid parameter has been specified.</span></span>
    
<span data-ttu-id="2976f-120">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="2976f-120">E_NOINTERFACE</span></span>
  
> <span data-ttu-id="2976f-121">Интерфейс обратного вызова, указанный в *падвисеинфо* , является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="2976f-121">The callback interface specified in  *pAdviseInfo*  is not valid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2976f-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="2976f-122">Remarks</span></span>

<span data-ttu-id="2976f-123">При открытии автономного объекта с помощью **[хропеноффлинеобж](hropenofflineobj.md)** клиент получает автономный объект, поддерживающий **имапиоффлинемгр**.</span><span class="sxs-lookup"><span data-stu-id="2976f-123">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="2976f-124">Клиент может проверить виды обратных вызовов, поддерживаемые объектом, с помощью **[имапиоффлине:: Capabilities](imapioffline-getcapabilities.md)**.</span><span class="sxs-lookup"><span data-stu-id="2976f-124">The client can check for the kinds of callbacks supported by the object by using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> <span data-ttu-id="2976f-125">Клиент может определить тип и другие сведения о обратном вызове, а затем вызвать метод **имапиоффлинемгр:: Advise** для регистрации, чтобы получать такие обратные вызовы для объекта.</span><span class="sxs-lookup"><span data-stu-id="2976f-125">The client can determine the type and other details about the callback it wants, and then call **IMAPIOfflineMgr::Advise** to register to receive such callbacks about the object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2976f-126">См. также</span><span class="sxs-lookup"><span data-stu-id="2976f-126">See also</span></span>



[<span data-ttu-id="2976f-127">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="2976f-127">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="2976f-128">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="2976f-128">IMAPIOfflineMgr::Unadvise</span></span>](imapiofflinemgr-unadvise.md)


[<span data-ttu-id="2976f-129">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="2976f-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="2976f-130">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="2976f-130">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

