---
title: HrOpenOfflineObj
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrOpenOfflineObj
api_type:
- HeaderDef
ms.assetid: cee1a940-fe01-d364-5d7c-c9e9dfeb8979
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cc71974d841005785932cc9017d44c3c0614687d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563389"
---
# <a name="hropenofflineobj"></a><span data-ttu-id="3bad3-103">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="3bad3-103">HrOpenOfflineObj</span></span>

  
  
<span data-ttu-id="3bad3-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3bad3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3bad3-105">Открывает автономные объекта на основе заданного профиля.</span><span class="sxs-lookup"><span data-stu-id="3bad3-105">Opens an offline object based on a given profile.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3bad3-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="3bad3-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3bad3-107">Экспортировать с:</span><span class="sxs-lookup"><span data-stu-id="3bad3-107">Exported by:</span></span>  <br/> |<span data-ttu-id="3bad3-108">Msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="3bad3-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="3bad3-109">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="3bad3-109">Called by:</span></span>  <br/> |<span data-ttu-id="3bad3-110">Клиент</span><span class="sxs-lookup"><span data-stu-id="3bad3-110">Client</span></span>  <br/> |
|<span data-ttu-id="3bad3-111">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="3bad3-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="3bad3-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="3bad3-112">Outlook</span></span>  <br/> |
   
```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
      ULONG ulReserved, 
      LPCWSTR pwszProfileNameIn, 
      const GUID* pGUID, 
      const GUID* pReserved, 
      IMAPIOfflineMgr** ppOfflineObj); 

```

## <a name="parameters"></a><span data-ttu-id="3bad3-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="3bad3-113">Parameters</span></span>

 <span data-ttu-id="3bad3-114">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="3bad3-114">_ulReserved_</span></span>
  
> <span data-ttu-id="3bad3-115">[in] Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="3bad3-115">[in] This parameter is not used.</span></span> <span data-ttu-id="3bad3-116">Он должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="3bad3-116">It must be 0.</span></span>
    
 <span data-ttu-id="3bad3-117">_pwszProfileNameIn_</span><span class="sxs-lookup"><span data-stu-id="3bad3-117">_pwszProfileNameIn_</span></span>
  
> <span data-ttu-id="3bad3-118">[in] Имя профиля, автономного объекта.</span><span class="sxs-lookup"><span data-stu-id="3bad3-118">[in] The name of the profile that the offline object is for.</span></span> <span data-ttu-id="3bad3-119">Должны быть выражены в Юникод.</span><span class="sxs-lookup"><span data-stu-id="3bad3-119">It must be expressed in Unicode.</span></span> 
    
 <span data-ttu-id="3bad3-120">_pGUID_</span><span class="sxs-lookup"><span data-stu-id="3bad3-120">_pGUID_</span></span>
  
> <span data-ttu-id="3bad3-121">[in] Указатель на идентификатор GUID, который можно использовать для уникальной идентификации данного объекта от других автономных объектов.</span><span class="sxs-lookup"><span data-stu-id="3bad3-121">[in] Pointer to a GUID which can be used to uniquely identify this object from other offline objects.</span></span> <span data-ttu-id="3bad3-122">Это должен быть **GUID_GlobalState**.</span><span class="sxs-lookup"><span data-stu-id="3bad3-122">It must be **GUID_GlobalState**.</span></span>
    
 <span data-ttu-id="3bad3-123">_Сохраняются_</span><span class="sxs-lookup"><span data-stu-id="3bad3-123">_pReserved_</span></span>
  
> <span data-ttu-id="3bad3-124">[in] Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="3bad3-124">[in] This parameter is not used.</span></span> <span data-ttu-id="3bad3-125">Должен иметь **значение null**.</span><span class="sxs-lookup"><span data-stu-id="3bad3-125">It must be **null**.</span></span>
    
 <span data-ttu-id="3bad3-126">_ppOfflineObj_</span><span class="sxs-lookup"><span data-stu-id="3bad3-126">_ppOfflineObj_</span></span>
  
> <span data-ttu-id="3bad3-127">[out] Указатель на запрошенный объект автономной.</span><span class="sxs-lookup"><span data-stu-id="3bad3-127">[out] A pointer to the requested offline object.</span></span> <span data-ttu-id="3bad3-128">Абонент может использовать этот указатель для доступа к [IMAPIOfflineMgr: IMAPIOffline](imapiofflinemgrimapioffline.md) интерфейс для определения обратных вызовов, которые поддерживает этот объект и настройка обратных вызовов для него.</span><span class="sxs-lookup"><span data-stu-id="3bad3-128">The caller can use this pointer to access the [IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md) interface to find the callbacks that this object supports and to set up callbacks for it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="3bad3-129">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="3bad3-129">Return values</span></span>

<span data-ttu-id="3bad3-130">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="3bad3-130">S_OK</span></span> 
  
- <span data-ttu-id="3bad3-131">Вызов функции выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="3bad3-131">The function call is successful.</span></span>
    
<span data-ttu-id="3bad3-132">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="3bad3-132">MAPI_E_NOT_FOUND</span></span>
  
- <span data-ttu-id="3bad3-133">Сбой вызова функции.</span><span class="sxs-lookup"><span data-stu-id="3bad3-133">The function call failed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3bad3-134">Замечания</span><span class="sxs-lookup"><span data-stu-id="3bad3-134">Remarks</span></span>

<span data-ttu-id="3bad3-135">Это первый вызов, с помощью клиента, когда клиенту требуется получать уведомления о изменения состояния подключения для заданного профиля.</span><span class="sxs-lookup"><span data-stu-id="3bad3-135">This is the first call that a client makes when the client wants to be notified of any connection state changes for a given profile.</span></span> <span data-ttu-id="3bad3-136">При вызове **HrOpenOfflineObj**, клиент получает автономного объекта, который поддерживает **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="3bad3-136">Upon calling **HrOpenOfflineObj**, the client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="3bad3-137">Клиент можно проверить для видов обратных вызовов, поддерживаемые объектом (с помощью [IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)) и затем настроить обратных вызовов для него (с помощью [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)).</span><span class="sxs-lookup"><span data-stu-id="3bad3-137">The client can check for the kinds of callbacks supported by the object (by using [IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)), and then set up callbacks for it (by using [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)).</span></span>
  
<span data-ttu-id="3bad3-138">При использовании [GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx) следует искать адреса этой функции msmapi32.dll, укажите **HrOpenOfflineObj@20** в качестве имени процедуры.</span><span class="sxs-lookup"><span data-stu-id="3bad3-138">When using [GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx) to look for the address of this function in msmapi32.dll, specify **HrOpenOfflineObj@20** as the procedure name.</span></span> 
  
 <span data-ttu-id="3bad3-139">**HrOpenOfflineObj** работает только для клиентов, которые являются поставщики MAPI, COM-надстройки и расширения клиента Exchange, выполняемых в рамках процесса Outlook.</span><span class="sxs-lookup"><span data-stu-id="3bad3-139">**HrOpenOfflineObj** only works for clients that are MAPI providers, COM Add-Ins, and Exchange Client Extensions running inside the Outlook process.</span></span> <span data-ttu-id="3bad3-140">В противном случае **HrOpenOfflineObj** возвращает **MAPI_E_NOT_FOUND**.</span><span class="sxs-lookup"><span data-stu-id="3bad3-140">Otherwise, **HrOpenOfflineObj** returns **MAPI_E_NOT_FOUND**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3bad3-141">См. также</span><span class="sxs-lookup"><span data-stu-id="3bad3-141">See also</span></span>



[<span data-ttu-id="3bad3-142">IMAPIOffline : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3bad3-142">IMAPIOffline : IUnknown</span></span>](imapiofflineiunknown.md)
  
[<span data-ttu-id="3bad3-143">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="3bad3-143">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="3bad3-144">Сведения об API автономного состояния</span><span class="sxs-lookup"><span data-stu-id="3bad3-144">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="3bad3-145">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="3bad3-145">MAPI Constants</span></span>](mapi-constants.md)

