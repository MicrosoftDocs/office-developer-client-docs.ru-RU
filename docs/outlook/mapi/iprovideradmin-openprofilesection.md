---
title: IProviderAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: b73cf770-8817-4a23-bd14-7b76fedef214
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b3ac1b2cf8335c5e0953fdcf61b2b5d466fbb724
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405662"
---
# <a name="iprovideradminopenprofilesection"></a><span data-ttu-id="018fb-103">IProviderAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="018fb-103">IProviderAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="018fb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="018fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="018fb-105">Открывает раздел профиля из текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="018fb-105">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="018fb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="018fb-106">Parameters</span></span>

 <span data-ttu-id="018fb-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="018fb-107">_lpUID_</span></span>
  
> <span data-ttu-id="018fb-108">[in] Указатель на структуру [MAPIUID,](mapiuid.md) которая содержит уникальный идентификатор открываемого раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="018fb-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the profile section to be opened.</span></span> <span data-ttu-id="018fb-109">Клиенты не должны передавать NULL для _параметра lpUID._</span><span class="sxs-lookup"><span data-stu-id="018fb-109">Clients must not pass NULL for the  _lpUID_ parameter.</span></span> <span data-ttu-id="018fb-110">Поставщики услуг могут передавать NULL для получения **MAPIUID** при вызове из функций точки входа службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="018fb-110">Service providers can pass NULL to retrieve the **MAPIUID** when they call from their message service entry point functions.</span></span> 
    
 <span data-ttu-id="018fb-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="018fb-111">_lpInterface_</span></span>
  
> <span data-ttu-id="018fb-112">[in] Указатель на идентификатор интерфейса( IID), который представляет интерфейс, используемый для доступа к разделу профиля.</span><span class="sxs-lookup"><span data-stu-id="018fb-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="018fb-113">Передача NULL приводит к возвращению стандартного интерфейса раздела профиля **(IProfSect).**</span><span class="sxs-lookup"><span data-stu-id="018fb-113">Passing NULL results in the profile section's standard interface (**IProfSect**) being returned.</span></span> 
    
 <span data-ttu-id="018fb-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="018fb-114">_ulFlags_</span></span>
  
> <span data-ttu-id="018fb-115">[in] Битоваяmas флагов, которая управляет открытием раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="018fb-115">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="018fb-116">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="018fb-116">The following flags can be set:</span></span>
    
<span data-ttu-id="018fb-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="018fb-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="018fb-118">Позволяет **openProfileSection** успешно возвращаться, возможно, до того, как раздел профиля будет полностью доступен вызываемой.</span><span class="sxs-lookup"><span data-stu-id="018fb-118">Enables **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the caller.</span></span> <span data-ttu-id="018fb-119">Если раздел профиля не доступен, последующий вызов может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="018fb-119">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="018fb-120">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="018fb-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="018fb-121">Запрашивает разрешение на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="018fb-121">Requests read/write permission.</span></span> <span data-ttu-id="018fb-122">По умолчанию объекты открываются с разрешением только для чтения, и звоня таким объектам не следует работать при предположении, что разрешение на чтение и записи предоставлено.</span><span class="sxs-lookup"><span data-stu-id="018fb-122">By default, objects are opened with read-only permission, and callers should not work on the assumption that read/write permission has been granted.</span></span> <span data-ttu-id="018fb-123">Клиентам не разрешено разрешение на чтение и записи для разделов профиля поставщика.</span><span class="sxs-lookup"><span data-stu-id="018fb-123">Clients are not allowed read/write permission to provider sections of the profile.</span></span>
    
<span data-ttu-id="018fb-124">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="018fb-124">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="018fb-125">Разрешает доступ ко всем разделам профилей, даже тем, которые принадлежат отдельным поставщикам услуг.</span><span class="sxs-lookup"><span data-stu-id="018fb-125">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="018fb-126">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="018fb-126">_lppProfSect_</span></span>
  
> <span data-ttu-id="018fb-127">[out] Указатель на указатель на раздел профиля.</span><span class="sxs-lookup"><span data-stu-id="018fb-127">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="018fb-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="018fb-128">Return value</span></span>

<span data-ttu-id="018fb-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="018fb-129">S_OK</span></span> 
  
> <span data-ttu-id="018fb-130">Раздел профиля успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="018fb-130">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="018fb-131">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="018fb-131">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="018fb-132">Предпринята попытка изменить раздел профиля, доступный только для чтения, или получить доступ к объекту, у которого у пользователя недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="018fb-132">An attempt was made to modify a read-only profile section or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="018fb-133">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="018fb-133">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="018fb-134">Запрашиваемая часть профиля не существует.</span><span class="sxs-lookup"><span data-stu-id="018fb-134">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="018fb-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="018fb-135">Remarks</span></span>

<span data-ttu-id="018fb-136">Метод **IProviderAdmin::OpenProfileSection** открывает раздел профиля, позволяя звоняшему считывать сведения из активного профиля и, возможно, записывать данные в него.</span><span class="sxs-lookup"><span data-stu-id="018fb-136">The **IProviderAdmin::OpenProfileSection** method opens a profile section, enabling the caller to read information from and possibly write information to the active profile.</span></span> 
  
<span data-ttu-id="018fb-137">Клиенты не могут открывать разделы профилей, принадлежащие поставщикам, с помощью метода **OpenProfileSection.**</span><span class="sxs-lookup"><span data-stu-id="018fb-137">Clients cannot open profile sections that belong to providers by using the **OpenProfileSection** method.</span></span> 
  
<span data-ttu-id="018fb-138">Несколько клиентов или поставщиков услуг могут одновременно открывать раздел профиля с разрешением только для чтения.</span><span class="sxs-lookup"><span data-stu-id="018fb-138">Multiple clients or service providers can simultaneously open a profile section with read-only permission.</span></span> <span data-ttu-id="018fb-139">Однако, когда раздел профиля открыт с разрешением на чтение и записи, никакие другие вызовы не могут быть сделаны для открытия раздела, независимо от типа доступа.</span><span class="sxs-lookup"><span data-stu-id="018fb-139">However, when a profile section is open with read/write permission, no other calls can be made to open the section, regardless of the type of access.</span></span> <span data-ttu-id="018fb-140">Если раздел профиля открыт с разрешением только для чтения, последующий вызов запроса разрешения на чтение и записи не будет MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="018fb-140">If a profile section is open with read-only permission, a subsequent call to request read/write permission will fail with MAPI_E_NO_ACCESS.</span></span> <span data-ttu-id="018fb-141">Аналогично, если раздел открыт с разрешением на чтение и записи, последующий вызов запроса разрешения только для чтения также не удастся.</span><span class="sxs-lookup"><span data-stu-id="018fb-141">Likewise, if a section is open with read/write permission, a subsequent call to request read-only permission will also fail.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="018fb-142">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="018fb-142">Notes to callers</span></span>

<span data-ttu-id="018fb-143">Если вы запросили **openProfileSection** открыть несуществов раздел профиля, передав MAPI_MODIFY в  _ulFlags_ и неизвестный **MAPIUID** в  _lpUID,_ будет создан раздел профиля.</span><span class="sxs-lookup"><span data-stu-id="018fb-143">If you request that **OpenProfileSection** open a nonexistent profile section by passing MAPI_MODIFY in  _ulFlags_ and an unknown **MAPIUID** in  _lpUID_, the profile section will be created.</span></span> 
  
<span data-ttu-id="018fb-144">Если вы запросили, чтобы **OpenProfileSection** открывал несущестуальный раздел с разрешением только для чтения, оно возвращает MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="018fb-144">If you request that **OpenProfileSection** open a nonexistent section with read-only permission, it returns MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="018fb-145">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="018fb-145">MFCMAPI reference</span></span>

<span data-ttu-id="018fb-146">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="018fb-146">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="018fb-147">**Файл**</span><span class="sxs-lookup"><span data-stu-id="018fb-147">**File**</span></span>|<span data-ttu-id="018fb-148">**Функция**</span><span class="sxs-lookup"><span data-stu-id="018fb-148">**Function**</span></span>|<span data-ttu-id="018fb-149">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="018fb-149">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="018fb-150">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="018fb-150">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="018fb-151">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="018fb-151">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="018fb-152">MFCMAPI использует метод **IProviderAdmin::OpenProfileSection** для открытия раздела профиля из текущего профиля.</span><span class="sxs-lookup"><span data-stu-id="018fb-152">MFCMAPI uses the **IProviderAdmin::OpenProfileSection** method to open a profile section from the current profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="018fb-153">См. также</span><span class="sxs-lookup"><span data-stu-id="018fb-153">See also</span></span>



[<span data-ttu-id="018fb-154">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="018fb-154">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="018fb-155">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="018fb-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="018fb-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="018fb-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="018fb-157">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="018fb-157">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


[<span data-ttu-id="018fb-158">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="018fb-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

