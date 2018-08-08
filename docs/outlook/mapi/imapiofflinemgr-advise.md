---
title: IMAPIOfflineMgrAdvise
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
ms.openlocfilehash: 53fa6bd49190bb88daeb0438dc0112e34322383e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809002"
---
# <a name="imapiofflinemgradvise"></a><span data-ttu-id="80cdf-103">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="80cdf-103">IMAPIOfflineMgr::Advise</span></span>

  
  
<span data-ttu-id="80cdf-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="80cdf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="80cdf-105">Регистрация клиента для получения обратных вызовов для автономного объекта.</span><span class="sxs-lookup"><span data-stu-id="80cdf-105">Registers a client to receive callbacks on an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="80cdf-106">���������</span><span class="sxs-lookup"><span data-stu-id="80cdf-106">Parameters</span></span>

 <span data-ttu-id="80cdf-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="80cdf-107">_ulFlags_</span></span>
  
>  <span data-ttu-id="80cdf-108">[in] Флаги, которые изменяют поведение.</span><span class="sxs-lookup"><span data-stu-id="80cdf-108">[in] Flags that modify behavior.</span></span> <span data-ttu-id="80cdf-109">Поддерживается только значение MAPIOFFLINE_ADVISE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="80cdf-109">Only the value MAPIOFFLINE_ADVISE_DEFAULT is supported.</span></span> 
    
 <span data-ttu-id="80cdf-110">_pAdviseInfo_</span><span class="sxs-lookup"><span data-stu-id="80cdf-110">_pAdviseInfo_</span></span>
  
> <span data-ttu-id="80cdf-111">[in] Сведения о типе обратного вызова, когда получать обратного вызова, интерфейс обратного вызова для вызывающего абонента и другие сведения.</span><span class="sxs-lookup"><span data-stu-id="80cdf-111">[in] Information about the type of callback, when to receive a callback, a callback interface for the caller, and other details.</span></span> <span data-ttu-id="80cdf-112">Он также содержит маркер клиента, который использует Outlook при отправке обратных вызовов последующим уведомлением вызывающего клиента.</span><span class="sxs-lookup"><span data-stu-id="80cdf-112">It also contains a client token that Outlook uses in sending subsequent notification callbacks to the client caller.</span></span>
    
 <span data-ttu-id="80cdf-113">_pulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="80cdf-113">_pulAdviseToken_</span></span>
  
> <span data-ttu-id="80cdf-114">[out] Маркер уведомлений, возвращаются вызывающему клиента для впоследствии Отмена обратного вызова для объекта.</span><span class="sxs-lookup"><span data-stu-id="80cdf-114">[out] An advise token returned to the client caller for subsequently canceling callback for the object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="80cdf-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="80cdf-115">Return value</span></span>

<span data-ttu-id="80cdf-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="80cdf-116">S_OK</span></span>
  
> <span data-ttu-id="80cdf-117">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="80cdf-117">The call was successful.</span></span>
    
<span data-ttu-id="80cdf-118">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="80cdf-118">E_INVALIDARG</span></span>
  
> <span data-ttu-id="80cdf-119">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="80cdf-119">An invalid parameter has been specified.</span></span>
    
<span data-ttu-id="80cdf-120">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="80cdf-120">E_NOINTERFACE</span></span>
  
> <span data-ttu-id="80cdf-121">Недопустимый интерфейс обратного вызова, указанного в *pAdviseInfo* .</span><span class="sxs-lookup"><span data-stu-id="80cdf-121">The callback interface specified in  *pAdviseInfo*  is not valid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="80cdf-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="80cdf-122">Remarks</span></span>

<span data-ttu-id="80cdf-123">При открытии автономного объекта с помощью **[HrOpenOfflineObj](hropenofflineobj.md)**, клиент получает автономного объекта, который поддерживает **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="80cdf-123">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="80cdf-124">Клиент можно проверить наличие видов поддерживается объектом с помощью **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** обратных вызовов.</span><span class="sxs-lookup"><span data-stu-id="80cdf-124">The client can check for the kinds of callbacks supported by the object by using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> <span data-ttu-id="80cdf-125">Клиент можно определить тип и другие сведения о обратного вызова, он хочет, а затем вызвать **IMAPIOfflineMgr::Advise** для получения таких обратных вызовов об объекте.</span><span class="sxs-lookup"><span data-stu-id="80cdf-125">The client can determine the type and other details about the callback it wants, and then call **IMAPIOfflineMgr::Advise** to register to receive such callbacks about the object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="80cdf-126">См. также</span><span class="sxs-lookup"><span data-stu-id="80cdf-126">See also</span></span>



[<span data-ttu-id="80cdf-127">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="80cdf-127">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="80cdf-128">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="80cdf-128">IMAPIOfflineMgr::Unadvise</span></span>](imapiofflinemgr-unadvise.md)


[<span data-ttu-id="80cdf-129">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="80cdf-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="80cdf-130">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="80cdf-130">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

