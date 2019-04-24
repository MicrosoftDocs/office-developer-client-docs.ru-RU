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
ms.openlocfilehash: 3ef929bf778fabc4350f553d185838dd5cb2cf0b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347749"
---
# <a name="hropenofflineobj"></a><span data-ttu-id="7c038-103">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="7c038-103">HrOpenOfflineObj</span></span>

  
  
<span data-ttu-id="7c038-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c038-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c038-105">Открывает автономный объект на основе заданных профилей.</span><span class="sxs-lookup"><span data-stu-id="7c038-105">Opens an offline object based on a given profile.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7c038-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="7c038-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7c038-107">Экспортировано:</span><span class="sxs-lookup"><span data-stu-id="7c038-107">Exported by:</span></span>  <br/> |<span data-ttu-id="7c038-108">MSMapi32. dll</span><span class="sxs-lookup"><span data-stu-id="7c038-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="7c038-109">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="7c038-109">Called by:</span></span>  <br/> |<span data-ttu-id="7c038-110">Клиент</span><span class="sxs-lookup"><span data-stu-id="7c038-110">Client</span></span>  <br/> |
|<span data-ttu-id="7c038-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="7c038-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="7c038-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="7c038-112">Outlook</span></span>  <br/> |
   
```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
      ULONG ulReserved, 
      LPCWSTR pwszProfileNameIn, 
      const GUID* pGUID, 
      const GUID* pReserved, 
      IMAPIOfflineMgr** ppOfflineObj); 

```

## <a name="parameters"></a><span data-ttu-id="7c038-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c038-113">Parameters</span></span>

 <span data-ttu-id="7c038-114">_Улресервед_</span><span class="sxs-lookup"><span data-stu-id="7c038-114">_ulReserved_</span></span>
  
> <span data-ttu-id="7c038-115">возврата Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="7c038-115">[in] This parameter is not used.</span></span> <span data-ttu-id="7c038-116">Значение должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="7c038-116">It must be 0.</span></span>
    
 <span data-ttu-id="7c038-117">_Пвсзпрофиленамеин_</span><span class="sxs-lookup"><span data-stu-id="7c038-117">_pwszProfileNameIn_</span></span>
  
> <span data-ttu-id="7c038-118">возврата Имя профиля, для которого предназначен автономный объект.</span><span class="sxs-lookup"><span data-stu-id="7c038-118">[in] The name of the profile that the offline object is for.</span></span> <span data-ttu-id="7c038-119">Он должен быть выражен в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="7c038-119">It must be expressed in Unicode.</span></span> 
    
 <span data-ttu-id="7c038-120">_Пгуид_</span><span class="sxs-lookup"><span data-stu-id="7c038-120">_pGUID_</span></span>
  
> <span data-ttu-id="7c038-121">возврата Указатель на GUID, который можно использовать для уникальной идентификации этого объекта из других автономных объектов.</span><span class="sxs-lookup"><span data-stu-id="7c038-121">[in] Pointer to a GUID which can be used to uniquely identify this object from other offline objects.</span></span> <span data-ttu-id="7c038-122">Он должен быть **гуид_глобалстате**.</span><span class="sxs-lookup"><span data-stu-id="7c038-122">It must be **GUID_GlobalState**.</span></span>
    
 <span data-ttu-id="7c038-123">_Сохранен_</span><span class="sxs-lookup"><span data-stu-id="7c038-123">_pReserved_</span></span>
  
> <span data-ttu-id="7c038-124">возврата Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="7c038-124">[in] This parameter is not used.</span></span> <span data-ttu-id="7c038-125">Он должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="7c038-125">It must be **null**.</span></span>
    
 <span data-ttu-id="7c038-126">_Ппоффлинеобж_</span><span class="sxs-lookup"><span data-stu-id="7c038-126">_ppOfflineObj_</span></span>
  
> <span data-ttu-id="7c038-127">вышли Указатель на запрошенный автономный объект.</span><span class="sxs-lookup"><span data-stu-id="7c038-127">[out] A pointer to the requested offline object.</span></span> <span data-ttu-id="7c038-128">Вызывающий абонент может использовать этот указатель для доступа к интерфейсу [имапиоффлинемгр: имапиоффлине](imapiofflinemgrimapioffline.md) для поиска обратных вызовов, поддерживаемых этим объектом, а также для настройки обратных вызовов для него.</span><span class="sxs-lookup"><span data-stu-id="7c038-128">The caller can use this pointer to access the [IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md) interface to find the callbacks that this object supports and to set up callbacks for it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="7c038-129">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="7c038-129">Return values</span></span>

<span data-ttu-id="7c038-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="7c038-130">S_OK</span></span> 
  
- <span data-ttu-id="7c038-131">Вызов функции выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="7c038-131">The function call is successful.</span></span>
    
<span data-ttu-id="7c038-132">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="7c038-132">MAPI_E_NOT_FOUND</span></span>
  
- <span data-ttu-id="7c038-133">Сбой при вызове функции.</span><span class="sxs-lookup"><span data-stu-id="7c038-133">The function call failed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7c038-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="7c038-134">Remarks</span></span>

<span data-ttu-id="7c038-135">Это первый вызов, который выполняет клиент, когда клиент хочет получать уведомления о любых изменениях состояния подключения для данного профиля.</span><span class="sxs-lookup"><span data-stu-id="7c038-135">This is the first call that a client makes when the client wants to be notified of any connection state changes for a given profile.</span></span> <span data-ttu-id="7c038-136">При вызове **хропеноффлинеобж**клиент получает автономный объект, поддерживающий **имапиоффлинемгр**.</span><span class="sxs-lookup"><span data-stu-id="7c038-136">Upon calling **HrOpenOfflineObj**, the client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="7c038-137">Клиент может проверить виды обратных вызовов, поддерживаемые объектом (с помощью [имапиоффлине::-Capabilities](imapioffline-getcapabilities.md)), а затем настроить для него обратные вызовы (с помощью [Имапиоффлинемгр:: Advise](imapiofflinemgr-advise.md)).</span><span class="sxs-lookup"><span data-stu-id="7c038-137">The client can check for the kinds of callbacks supported by the object (by using [IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)), and then set up callbacks for it (by using [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)).</span></span>
  
<span data-ttu-id="7c038-138">При использовании [GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx) для поиска адреса этой функции в MSMapi32. dll укажите **хропеноффлинеобж @ 20** в качестве имени процедуры.</span><span class="sxs-lookup"><span data-stu-id="7c038-138">When using [GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx) to look for the address of this function in msmapi32.dll, specify **HrOpenOfflineObj@20** as the procedure name.</span></span> 
  
 <span data-ttu-id="7c038-139">**Хропеноффлинеобж** работает только для клиентов, которые являются поставщиками MAPI, надстройками COM и клиентскими расширениями Exchange, запущенными в процессе Outlook.</span><span class="sxs-lookup"><span data-stu-id="7c038-139">**HrOpenOfflineObj** only works for clients that are MAPI providers, COM Add-Ins, and Exchange Client Extensions running inside the Outlook process.</span></span> <span data-ttu-id="7c038-140">В противном случае **хропеноффлинеобж** возвращает **мапи_е_нот_фаунд**.</span><span class="sxs-lookup"><span data-stu-id="7c038-140">Otherwise, **HrOpenOfflineObj** returns **MAPI_E_NOT_FOUND**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7c038-141">См. также</span><span class="sxs-lookup"><span data-stu-id="7c038-141">See also</span></span>



[<span data-ttu-id="7c038-142">IMAPIOffline : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7c038-142">IMAPIOffline : IUnknown</span></span>](imapiofflineiunknown.md)
  
[<span data-ttu-id="7c038-143">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="7c038-143">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="7c038-144">Об API автономного режима</span><span class="sxs-lookup"><span data-stu-id="7c038-144">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="7c038-145">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="7c038-145">MAPI Constants</span></span>](mapi-constants.md)

