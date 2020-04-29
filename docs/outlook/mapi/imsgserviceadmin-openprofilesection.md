---
title: имсгсервицеадминопенпрофилесектион
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
# <a name="imsgserviceadminopenprofilesection"></a><span data-ttu-id="ff982-103">IMsgServiceAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="ff982-103">IMsgServiceAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="ff982-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff982-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff982-105">Открывает раздел текущего профиля и возвращает указатель [ипрофсект](iprofsectimapiprop.md) для получения дальнейших прав.</span><span class="sxs-lookup"><span data-stu-id="ff982-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="ff982-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff982-106">Parameters</span></span>

 <span data-ttu-id="ff982-107">_лпуид_</span><span class="sxs-lookup"><span data-stu-id="ff982-107">_lpUID_</span></span>
  
> <span data-ttu-id="ff982-108">Указатель на структуру [мапиуид](mapiuid.md) , которая идентифицирует раздел профиля.</span><span class="sxs-lookup"><span data-stu-id="ff982-108">A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="ff982-109">_лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="ff982-109">_lpInterface_</span></span>
  
> <span data-ttu-id="ff982-110">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к разделу профиля.</span><span class="sxs-lookup"><span data-stu-id="ff982-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="ff982-111">При передаче значения NULL в указатель на стандартный интерфейс, возвращаемый в параметре _лпппрофсект_ .</span><span class="sxs-lookup"><span data-stu-id="ff982-111">Passing NULL results in a pointer to its standard interface being returned in the  _lppProfSect_ parameter.</span></span> <span data-ttu-id="ff982-112">Стандартный интерфейс для раздела профиля — **ипрофсект**.</span><span class="sxs-lookup"><span data-stu-id="ff982-112">The standard interface for a profile section is **IProfSect**.</span></span>
    
 <span data-ttu-id="ff982-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ff982-113">_ulFlags_</span></span>
  
> <span data-ttu-id="ff982-114">возврата Битовая маска флагов, которые управляют доступом к разделу профиля.</span><span class="sxs-lookup"><span data-stu-id="ff982-114">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="ff982-115">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="ff982-115">The following flags can be set:</span></span>
    
<span data-ttu-id="ff982-116">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="ff982-116">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="ff982-117">Разрешает успешное возвращение **опенпрофилесектион** , возможно, перед тем, как раздел профиля будет полностью доступен для вызывающего клиента.</span><span class="sxs-lookup"><span data-stu-id="ff982-117">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="ff982-118">Если раздел profile недоступен, то при следующем вызове он может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="ff982-118">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="ff982-119">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="ff982-119">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="ff982-120">Запрашивает разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="ff982-120">Requests read/write permission.</span></span> <span data-ttu-id="ff982-121">По умолчанию разделы профиля открываются с разрешением "только чтение", и клиенты не должны работать в предположении, что предоставлено разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="ff982-121">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="ff982-122">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="ff982-122">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="ff982-123">Предоставляет доступ ко всем разделам профиля, даже к тем, которые принадлежат отдельным поставщикам услуг.</span><span class="sxs-lookup"><span data-stu-id="ff982-123">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="ff982-124">_лпппрофсект_</span><span class="sxs-lookup"><span data-stu-id="ff982-124">_lppProfSect_</span></span>
  
> <span data-ttu-id="ff982-125">вышли Указатель на указатель на раздел профиля.</span><span class="sxs-lookup"><span data-stu-id="ff982-125">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ff982-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff982-126">Return value</span></span>

<span data-ttu-id="ff982-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="ff982-127">S_OK</span></span> 
  
> <span data-ttu-id="ff982-128">Раздел профиля успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="ff982-128">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="ff982-129">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="ff982-129">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="ff982-130">Предпринята попытка доступа к разделу профиля, для которого вызывающая сторона не имеет достаточных разрешений.</span><span class="sxs-lookup"><span data-stu-id="ff982-130">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="ff982-131">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ff982-131">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ff982-132">Запрошенный раздел профиля не существует.</span><span class="sxs-lookup"><span data-stu-id="ff982-132">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ff982-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="ff982-133">Remarks</span></span>

<span data-ttu-id="ff982-134">Метод **имсгсервицеадмин:: опенпрофилесектион** открывает раздел profile (объект, который поддерживает интерфейс [ипрофсект](iprofsectimapiprop.md) ).</span><span class="sxs-lookup"><span data-stu-id="ff982-134">The **IMsgServiceAdmin::OpenProfileSection** method opens a profile section, an object that supports the [IProfSect](iprofsectimapiprop.md) interface.</span></span> <span data-ttu-id="ff982-135">Разделы профиля используются для чтения и записи информации в профиль сеанса.</span><span class="sxs-lookup"><span data-stu-id="ff982-135">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
 <span data-ttu-id="ff982-136">**Опенпрофилесектион** не может использоваться для открытия разделов профилей, принадлежащих индивидуальным поставщикам услуг, если не используется MAPI_FORCE_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="ff982-136">**OpenProfileSection** cannot be used to open profile sections owned by individual service providers unless MAPI_FORCE_ACCESS is used.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ff982-137">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="ff982-137">Notes to callers</span></span>

<span data-ttu-id="ff982-138">Несколько клиентов могут открыть раздел профиля с разрешением только для чтения, но только один клиент может открыть раздел профиля с разрешениями на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="ff982-138">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="ff982-139">Если для другого клиента открылся раздел профиля, который вы пытаетесь открыть, вызвав **опенпрофилесектион** с установленным флагом MAPI_MODIFY, вызов завершится неудачей, возвращая MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="ff982-139">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="ff982-140">Если раздел открыт для записи, то операция открытия, доступная только для чтения, завершается с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="ff982-140">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="ff982-141">Вы можете создать раздел профиля, вызвав **опенпрофилесектион** с флагом MAPI_MODIFY и несуществующей структурой [мапиуид](mapiuid.md) в параметре _лпуид_ .</span><span class="sxs-lookup"><span data-stu-id="ff982-141">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent [MAPIUID](mapiuid.md) structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="ff982-142">Убедитесь, что вы указали MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="ff982-142">Be sure you specify MAPI_MODIFY.</span></span> <span data-ttu-id="ff982-143">Если вы настроили _лпуид_ на несуществующий **Мапиуид** , а **опенпрофилесектион** задано использовать режим доступа только для чтения по умолчанию, вызов завершится с MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="ff982-143">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ff982-144">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ff982-144">MFCMAPI reference</span></span>

<span data-ttu-id="ff982-145">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="ff982-145">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ff982-146">**Файл**</span><span class="sxs-lookup"><span data-stu-id="ff982-146">**File**</span></span>|<span data-ttu-id="ff982-147">**Функция**</span><span class="sxs-lookup"><span data-stu-id="ff982-147">**Function**</span></span>|<span data-ttu-id="ff982-148">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="ff982-148">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ff982-149">Мапипрофилефунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="ff982-149">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="ff982-150">опенпрофилесектион</span><span class="sxs-lookup"><span data-stu-id="ff982-150">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="ff982-151">MFCMAPI использует метод **имсгсервицеадмин:: опенпрофилесектион** , чтобы открыть раздел профиля.</span><span class="sxs-lookup"><span data-stu-id="ff982-151">MFCMAPI uses the **IMsgServiceAdmin::OpenProfileSection** method to open a profile section.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ff982-152">См. также</span><span class="sxs-lookup"><span data-stu-id="ff982-152">See also</span></span>



[<span data-ttu-id="ff982-153">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ff982-153">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="ff982-154">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="ff982-154">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="ff982-155">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ff982-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="ff982-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="ff982-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="ff982-157">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ff982-157">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="ff982-158">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="ff982-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

