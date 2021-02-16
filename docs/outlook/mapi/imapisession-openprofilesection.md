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
# <a name="imapisessionopenprofilesection"></a><span data-ttu-id="0faba-103">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="0faba-103">IMAPISession::OpenProfileSection</span></span>

  
  
<span data-ttu-id="0faba-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0faba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0faba-105">Открывает раздел текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="0faba-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="0faba-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0faba-106">Parameters</span></span>

 <span data-ttu-id="0faba-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="0faba-107">_lpUID_</span></span>
  
> <span data-ttu-id="0faba-108">[in] Указатель на структуру [MAPIUID,](mapiuid.md) которая определяет раздел профиля.</span><span class="sxs-lookup"><span data-stu-id="0faba-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="0faba-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="0faba-109">_lpInterface_</span></span>
  
> <span data-ttu-id="0faba-110">[in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, который будет использоваться для доступа к разделу профиля.</span><span class="sxs-lookup"><span data-stu-id="0faba-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="0faba-111">При передаче NULL параметр _lppProfSect_ возвращает указатель на стандартный интерфейс раздела профиля **IProfSect.**</span><span class="sxs-lookup"><span data-stu-id="0faba-111">Passing NULL causes the  _lppProfSect_ parameter to return a pointer to the profile section's standard interface, **IProfSect**.</span></span>
    
 <span data-ttu-id="0faba-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0faba-112">_ulFlags_</span></span>
  
> <span data-ttu-id="0faba-113">[in] Битоваяmas флагов, которая управляет доступом к разделу профиля.</span><span class="sxs-lookup"><span data-stu-id="0faba-113">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="0faba-114">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="0faba-114">The following flags can be set:</span></span>
    
<span data-ttu-id="0faba-115">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="0faba-115">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="0faba-116">Позволяет **OpenProfileSection** успешно возвращаться, возможно, до того, как раздел профиля будет полностью доступен вызываемому клиенту.</span><span class="sxs-lookup"><span data-stu-id="0faba-116">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="0faba-117">Если раздел профиля не доступен, последующий вызов может привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="0faba-117">If the profile section is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="0faba-118">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="0faba-118">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="0faba-119">Разрешает доступ к разделу профиля, который не принадлежит поставщику.</span><span class="sxs-lookup"><span data-stu-id="0faba-119">Allows access to a profile section that does not belong to the provider.</span></span>
    
<span data-ttu-id="0faba-120">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="0faba-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="0faba-121">Запрашивает разрешение на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="0faba-121">Requests read/write permission.</span></span> <span data-ttu-id="0faba-122">По умолчанию разделы профилей открываются с разрешением только на чтение, и клиенты не должны работать при предположении, что разрешение на чтение и записи предоставлено.</span><span class="sxs-lookup"><span data-stu-id="0faba-122">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="0faba-123">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="0faba-123">_lppProfSect_</span></span>
  
> <span data-ttu-id="0faba-124">[out] Указатель на указатель на раздел профиля.</span><span class="sxs-lookup"><span data-stu-id="0faba-124">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0faba-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0faba-125">Return value</span></span>

<span data-ttu-id="0faba-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="0faba-126">S_OK</span></span> 
  
> <span data-ttu-id="0faba-127">Раздел профиля успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="0faba-127">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="0faba-128">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="0faba-128">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="0faba-129">Предпринята попытка доступа к разделу профиля, для которого у вызываемого пользователя недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="0faba-129">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="0faba-130">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="0faba-130">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="0faba-131">Запрашиваемая часть профиля не существует.</span><span class="sxs-lookup"><span data-stu-id="0faba-131">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0faba-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="0faba-132">Remarks</span></span>

<span data-ttu-id="0faba-133">Метод **IMAPISession::OpenProfileSection** открывает раздел профиля или объект, который поддерживает **интерфейс IProfSect.**</span><span class="sxs-lookup"><span data-stu-id="0faba-133">The **IMAPISession::OpenProfileSection** method opens a profile section or object that supports the **IProfSect** interface.</span></span> <span data-ttu-id="0faba-134">Разделы профиля используются для чтения сведений из профиля сеанса и записи в него.</span><span class="sxs-lookup"><span data-stu-id="0faba-134">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
<span data-ttu-id="0faba-135">**OpenProfileSection** нельзя использовать для открытия разделов профилей, которые принадлежат отдельным поставщикам услуг, если не указать MAPI_FORCE_ACCESS в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="0faba-135">You cannot use **OpenProfileSection** to open profile sections that individual service providers own unless you specify MAPI_FORCE_ACCESS in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0faba-136">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="0faba-136">Notes to callers</span></span>

<span data-ttu-id="0faba-137">Несколько клиентов могут открывать раздел профиля с разрешением только на чтение, но только один клиент может открыть раздел профиля с разрешением на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="0faba-137">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="0faba-138">Если другой клиент открывает раздел профиля, который вы попытаетесь открыть, вызывая **OpenProfileSection** с установленным флагом MAPI_MODIFY, вызов не удастся, и MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="0faba-138">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="0faba-139">Операция открытия только для чтения не удастся, если раздел открыт для записи.</span><span class="sxs-lookup"><span data-stu-id="0faba-139">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="0faba-140">Можно создать раздел профиля, вызывая **OpenProfileSection** с флагом MAPI_MODIFY и несущестукой структурой **MAPIUID** в параметре _lpUID._</span><span class="sxs-lookup"><span data-stu-id="0faba-140">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent **MAPIUID** structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="0faba-141">Обязательно укажите MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="0faba-141">Be sure that you specify MAPI_MODIFY.</span></span> <span data-ttu-id="0faba-142">Если вы установите  _для lpUID_ значение, указывав на несущесту **mapIUID,** а **OpenProfileSection** будет использовать режим доступа только для чтения по умолчанию, вызов не будет MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="0faba-142">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0faba-143">См. также</span><span class="sxs-lookup"><span data-stu-id="0faba-143">See also</span></span>



[<span data-ttu-id="0faba-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0faba-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="0faba-145">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0faba-145">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="0faba-146">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="0faba-146">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="0faba-147">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0faba-147">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

