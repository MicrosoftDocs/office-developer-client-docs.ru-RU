---
title: IMsgServiceAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: 7f24910a-e14e-44a1-8477-d8968130ba74
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 32ebdea3a594b5adf5d46dc081098d3628ae145b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437114"
---
# <a name="imsgserviceadminopenprofilesection"></a><span data-ttu-id="af607-103">IMsgServiceAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="af607-103">IMsgServiceAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="af607-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af607-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af607-105">Открывает раздел текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="af607-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="af607-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="af607-106">Parameters</span></span>

 <span data-ttu-id="af607-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="af607-107">_lpUID_</span></span>
  
> <span data-ttu-id="af607-108">Указатель на [структуру MAPIUID,](mapiuid.md) идентифицируемую в разделе профилей.</span><span class="sxs-lookup"><span data-stu-id="af607-108">A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="af607-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="af607-109">_lpInterface_</span></span>
  
> <span data-ttu-id="af607-110">[in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, используемый для доступа к разделу профилей.</span><span class="sxs-lookup"><span data-stu-id="af607-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="af607-111">Передача NULL приводит к возвращению указателя к стандартному интерфейсу в _параметре lppProfSect._</span><span class="sxs-lookup"><span data-stu-id="af607-111">Passing NULL results in a pointer to its standard interface being returned in the  _lppProfSect_ parameter.</span></span> <span data-ttu-id="af607-112">Стандартным интерфейсом для раздела профилей **является IProfSect**.</span><span class="sxs-lookup"><span data-stu-id="af607-112">The standard interface for a profile section is **IProfSect**.</span></span>
    
 <span data-ttu-id="af607-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="af607-113">_ulFlags_</span></span>
  
> <span data-ttu-id="af607-114">[in] Битмаска флагов, которые контролируют доступ к разделу профилей.</span><span class="sxs-lookup"><span data-stu-id="af607-114">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="af607-115">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="af607-115">The following flags can be set:</span></span>
    
<span data-ttu-id="af607-116">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="af607-116">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="af607-117">Позволяет **OpenProfileSection** успешно возвращаться, возможно, до того, как профильный раздел будет полностью доступен клиенту вызова.</span><span class="sxs-lookup"><span data-stu-id="af607-117">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="af607-118">Если раздел профилей не доступен, последующий вызов может привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="af607-118">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="af607-119">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="af607-119">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="af607-120">Запросы на чтение и написание разрешений.</span><span class="sxs-lookup"><span data-stu-id="af607-120">Requests read/write permission.</span></span> <span data-ttu-id="af607-121">По умолчанию разделы профилей открываются с разрешения только для чтения, и клиенты не должны работать с предположением о том, что разрешение на чтение и записи было предоставлено.</span><span class="sxs-lookup"><span data-stu-id="af607-121">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="af607-122">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="af607-122">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="af607-123">Позволяет получить доступ ко всем разделам профилей, даже к разделам, которые принадлежат отдельным поставщикам услуг.</span><span class="sxs-lookup"><span data-stu-id="af607-123">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="af607-124">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="af607-124">_lppProfSect_</span></span>
  
> <span data-ttu-id="af607-125">[вышел] Указатель на указатель в разделе профиль.</span><span class="sxs-lookup"><span data-stu-id="af607-125">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="af607-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="af607-126">Return value</span></span>

<span data-ttu-id="af607-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="af607-127">S_OK</span></span> 
  
> <span data-ttu-id="af607-128">Раздел профилей был успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="af607-128">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="af607-129">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="af607-129">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="af607-130">Была предпринята попытка получить доступ к разделу профилей, для которого вызываемая не имеет достаточных разрешений.</span><span class="sxs-lookup"><span data-stu-id="af607-130">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="af607-131">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="af607-131">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="af607-132">Запрашиваемая часть профиля не существует.</span><span class="sxs-lookup"><span data-stu-id="af607-132">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="af607-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="af607-133">Remarks</span></span>

<span data-ttu-id="af607-134">Метод **IMsgServiceAdmin::OpenProfileSection** открывает профильный раздел, объект, который поддерживает [интерфейс IProfSect.](iprofsectimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="af607-134">The **IMsgServiceAdmin::OpenProfileSection** method opens a profile section, an object that supports the [IProfSect](iprofsectimapiprop.md) interface.</span></span> <span data-ttu-id="af607-135">Разделы профилей используются для чтения сведений из профиля сеанса и записи в него.</span><span class="sxs-lookup"><span data-stu-id="af607-135">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
 <span data-ttu-id="af607-136">**OpenProfileSection** нельзя использовать для открытия разделов профилей, которые принадлежат отдельным поставщикам услуг, если MAPI_FORCE_ACCESS не используется.</span><span class="sxs-lookup"><span data-stu-id="af607-136">**OpenProfileSection** cannot be used to open profile sections owned by individual service providers unless MAPI_FORCE_ACCESS is used.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="af607-137">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="af607-137">Notes to callers</span></span>

<span data-ttu-id="af607-138">Несколько клиентов могут открыть раздел профилей с разрешения только для чтения, но только один клиент может открыть раздел профилей с разрешения на чтение и написание.</span><span class="sxs-lookup"><span data-stu-id="af607-138">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="af607-139">Если у другого клиента открыт раздел профилей, который вы попытаетесь открыть, позвонив **в OpenProfileSection** с набором флага MAPI_MODIFY, вызов не удастся, возвращая MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="af607-139">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="af607-140">Открытая операция только для чтения сбой, если раздел открыт для записи.</span><span class="sxs-lookup"><span data-stu-id="af607-140">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="af607-141">Вы можете создать раздел профилей, позвонив **в OpenProfileSection** с флагом MAPI_MODIFY и несуществовацией [структуры MAPIUID](mapiuid.md) в параметре _lpUID._</span><span class="sxs-lookup"><span data-stu-id="af607-141">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent [MAPIUID](mapiuid.md) structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="af607-142">Обязательно укажите MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="af607-142">Be sure you specify MAPI_MODIFY.</span></span> <span data-ttu-id="af607-143">Если  _установлено, что lpUID_ будет указать на несуществовую **MAPIUID,** а **OpenProfileSection** будет использовать режим доступа только для чтения по умолчанию, вызов сбой MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="af607-143">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="af607-144">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="af607-144">MFCMAPI reference</span></span>

<span data-ttu-id="af607-145">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="af607-145">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="af607-146">**Файл**</span><span class="sxs-lookup"><span data-stu-id="af607-146">**File**</span></span>|<span data-ttu-id="af607-147">**Функция**</span><span class="sxs-lookup"><span data-stu-id="af607-147">**Function**</span></span>|<span data-ttu-id="af607-148">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="af607-148">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="af607-149">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="af607-149">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="af607-150">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="af607-150">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="af607-151">MFCMAPI использует **метод IMsgServiceAdmin::OpenProfileSection** для открытия раздела профилей.</span><span class="sxs-lookup"><span data-stu-id="af607-151">MFCMAPI uses the **IMsgServiceAdmin::OpenProfileSection** method to open a profile section.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="af607-152">См. также</span><span class="sxs-lookup"><span data-stu-id="af607-152">See also</span></span>



[<span data-ttu-id="af607-153">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="af607-153">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="af607-154">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="af607-154">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="af607-155">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="af607-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="af607-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="af607-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="af607-157">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="af607-157">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="af607-158">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="af607-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

