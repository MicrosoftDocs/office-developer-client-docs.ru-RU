---
title: IMAPISessionOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenProfileSection
api_type:
- COM
ms.assetid: e2757028-27e7-4fc0-9674-e8e30737ef1d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9d7c1693dfb22ae89afed8cbe1426c1e186f8b2d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439921"
---
# <a name="imapisessionopenprofilesection"></a><span data-ttu-id="68eeb-103">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="68eeb-103">IMAPISession::OpenProfileSection</span></span>

  
  
<span data-ttu-id="68eeb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68eeb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68eeb-105">Открывает раздел текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="68eeb-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="68eeb-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="68eeb-106">Parameters</span></span>

 <span data-ttu-id="68eeb-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="68eeb-107">_lpUID_</span></span>
  
> <span data-ttu-id="68eeb-108">[in] Указатель на [структуру MAPIUID,](mapiuid.md) идентифицируемую в разделе профилей.</span><span class="sxs-lookup"><span data-stu-id="68eeb-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="68eeb-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="68eeb-109">_lpInterface_</span></span>
  
> <span data-ttu-id="68eeb-110">[in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, используемый для доступа к разделу профилей.</span><span class="sxs-lookup"><span data-stu-id="68eeb-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="68eeb-111">Передача NULL заставляет _параметр lppProfSect_ возвращать указатель в стандартный интерфейс **профиля IProfSect.**</span><span class="sxs-lookup"><span data-stu-id="68eeb-111">Passing NULL causes the  _lppProfSect_ parameter to return a pointer to the profile section's standard interface, **IProfSect**.</span></span>
    
 <span data-ttu-id="68eeb-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="68eeb-112">_ulFlags_</span></span>
  
> <span data-ttu-id="68eeb-113">[in] Битмаска флагов, которые контролируют доступ к разделу профилей.</span><span class="sxs-lookup"><span data-stu-id="68eeb-113">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="68eeb-114">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="68eeb-114">The following flags can be set:</span></span>
    
<span data-ttu-id="68eeb-115">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="68eeb-115">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="68eeb-116">Позволяет **OpenProfileSection** успешно возвращаться, возможно, до того, как профильный раздел будет полностью доступен клиенту вызова.</span><span class="sxs-lookup"><span data-stu-id="68eeb-116">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="68eeb-117">Если раздел профилей не доступен, последующий вызов может привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="68eeb-117">If the profile section is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="68eeb-118">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="68eeb-118">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="68eeb-119">Разрешает доступ к разделу профилей, который не принадлежит поставщику.</span><span class="sxs-lookup"><span data-stu-id="68eeb-119">Allows access to a profile section that does not belong to the provider.</span></span>
    
<span data-ttu-id="68eeb-120">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="68eeb-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="68eeb-121">Запросы на чтение и написание разрешений.</span><span class="sxs-lookup"><span data-stu-id="68eeb-121">Requests read/write permission.</span></span> <span data-ttu-id="68eeb-122">По умолчанию разделы профилей открываются с разрешения только для чтения, и клиенты не должны работать с предположением о том, что разрешение на чтение и записи было предоставлено.</span><span class="sxs-lookup"><span data-stu-id="68eeb-122">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="68eeb-123">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="68eeb-123">_lppProfSect_</span></span>
  
> <span data-ttu-id="68eeb-124">[вышел] Указатель на указатель в разделе профиль.</span><span class="sxs-lookup"><span data-stu-id="68eeb-124">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="68eeb-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68eeb-125">Return value</span></span>

<span data-ttu-id="68eeb-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="68eeb-126">S_OK</span></span> 
  
> <span data-ttu-id="68eeb-127">Раздел профилей был успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="68eeb-127">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="68eeb-128">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="68eeb-128">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="68eeb-129">Была предпринята попытка получить доступ к разделу профилей, для которого вызываемая не имеет достаточных разрешений.</span><span class="sxs-lookup"><span data-stu-id="68eeb-129">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="68eeb-130">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="68eeb-130">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="68eeb-131">Запрашиваемая часть профиля не существует.</span><span class="sxs-lookup"><span data-stu-id="68eeb-131">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="68eeb-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="68eeb-132">Remarks</span></span>

<span data-ttu-id="68eeb-133">Метод **IMAPISession::OpenProfileSection** открывает профильный раздел или объект, который поддерживает **интерфейс IProfSect.**</span><span class="sxs-lookup"><span data-stu-id="68eeb-133">The **IMAPISession::OpenProfileSection** method opens a profile section or object that supports the **IProfSect** interface.</span></span> <span data-ttu-id="68eeb-134">Разделы профилей используются для чтения сведений из профиля сеанса и записи в него.</span><span class="sxs-lookup"><span data-stu-id="68eeb-134">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
<span data-ttu-id="68eeb-135">Вы не можете использовать **OpenProfileSection** для открытия разделов профилей, которые принадлежат отдельным поставщикам услуг, если вы не MAPI_FORCE_ACCESS в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="68eeb-135">You cannot use **OpenProfileSection** to open profile sections that individual service providers own unless you specify MAPI_FORCE_ACCESS in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="68eeb-136">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="68eeb-136">Notes to callers</span></span>

<span data-ttu-id="68eeb-137">Несколько клиентов могут открыть раздел профилей с разрешения только для чтения, но только один клиент может открыть раздел профилей с разрешения на чтение и написание.</span><span class="sxs-lookup"><span data-stu-id="68eeb-137">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="68eeb-138">Если у другого клиента открыт раздел профилей, который вы попытаетесь открыть, позвонив **в OpenProfileSection** с набором флага MAPI_MODIFY, вызов не удастся, возвращая MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="68eeb-138">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="68eeb-139">Открытая операция только для чтения сбой, если раздел открыт для записи.</span><span class="sxs-lookup"><span data-stu-id="68eeb-139">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="68eeb-140">Вы можете создать раздел профилей, позвонив **в OpenProfileSection** с флагом MAPI_MODIFY и несуществовацией **структуры MAPIUID** в параметре _lpUID._</span><span class="sxs-lookup"><span data-stu-id="68eeb-140">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent **MAPIUID** structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="68eeb-141">Убедитесь, что вы указываете MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="68eeb-141">Be sure that you specify MAPI_MODIFY.</span></span> <span data-ttu-id="68eeb-142">Если  _установлено, что lpUID_ будет указать на несуществовую **MAPIUID,** а **OpenProfileSection** будет использовать режим доступа только для чтения по умолчанию, вызов сбой MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="68eeb-142">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="68eeb-143">См. также</span><span class="sxs-lookup"><span data-stu-id="68eeb-143">See also</span></span>



[<span data-ttu-id="68eeb-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="68eeb-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="68eeb-145">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="68eeb-145">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="68eeb-146">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="68eeb-146">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="68eeb-147">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="68eeb-147">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

