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
ms.openlocfilehash: 954dc467a0d83466b1b16a3ead5b6404d372ecab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809355"
---
# <a name="imsgserviceadminopenprofilesection"></a><span data-ttu-id="e53bc-103">IMsgServiceAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="e53bc-103">IMsgServiceAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="e53bc-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e53bc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e53bc-105">Откроется раздел текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшей доступа.</span><span class="sxs-lookup"><span data-stu-id="e53bc-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="e53bc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e53bc-106">Parameters</span></span>

 <span data-ttu-id="e53bc-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="e53bc-107">_lpUID_</span></span>
  
> <span data-ttu-id="e53bc-108">Указатель на структуру [MAPIUID](mapiuid.md) , идентифицирующий раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="e53bc-108">A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="e53bc-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="e53bc-109">_lpInterface_</span></span>
  
> <span data-ttu-id="e53bc-110">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="e53bc-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="e53bc-111">Передача значение NULL, приводит к указатель на его стандартный интерфейс, возвращаемых в параметре _lppProfSect_ .</span><span class="sxs-lookup"><span data-stu-id="e53bc-111">Passing NULL results in a pointer to its standard interface being returned in the  _lppProfSect_ parameter.</span></span> <span data-ttu-id="e53bc-112">Стандартный интерфейс для профиля — **IProfSect**.</span><span class="sxs-lookup"><span data-stu-id="e53bc-112">The standard interface for a profile section is **IProfSect**.</span></span>
    
 <span data-ttu-id="e53bc-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e53bc-113">_ulFlags_</span></span>
  
> <span data-ttu-id="e53bc-114">[in] Битовая маска, что управляет доступом к разделу профиль флаги.</span><span class="sxs-lookup"><span data-stu-id="e53bc-114">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="e53bc-115">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="e53bc-115">The following flags can be set:</span></span>
    
<span data-ttu-id="e53bc-116">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="e53bc-116">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="e53bc-117">Позволяет **OpenProfileSection** для возврата успешно, возможно перед профиль раздела доступными для клиента.</span><span class="sxs-lookup"><span data-stu-id="e53bc-117">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="e53bc-118">Если в разделе профиль не поддерживается, последующие подключения к нему может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="e53bc-118">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="e53bc-119">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="e53bc-119">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="e53bc-120">Запросы на разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e53bc-120">Requests read/write permission.</span></span> <span data-ttu-id="e53bc-121">По умолчанию разделы профилей открываются с разрешением только для чтения и клиенты не должны работать предполагается, что что назначено разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e53bc-121">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="e53bc-122">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="e53bc-122">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="e53bc-123">Разрешает доступ всех разделах профилей, даже теми, поставщиками отдельные службы.</span><span class="sxs-lookup"><span data-stu-id="e53bc-123">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="e53bc-124">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="e53bc-124">_lppProfSect_</span></span>
  
> <span data-ttu-id="e53bc-125">[out] Указатель на указатель на раздел профилей.</span><span class="sxs-lookup"><span data-stu-id="e53bc-125">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e53bc-126">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="e53bc-126">Return value</span></span>

<span data-ttu-id="e53bc-127">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="e53bc-127">S_OK</span></span> 
  
> <span data-ttu-id="e53bc-128">В разделе профилей успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="e53bc-128">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="e53bc-129">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="e53bc-129">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="e53bc-130">Предпринята попытка получить доступ к раздела профиля, для которого вызывающий не имеет разрешений.</span><span class="sxs-lookup"><span data-stu-id="e53bc-130">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="e53bc-131">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="e53bc-131">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="e53bc-132">В разделе запрошенные профиля не существует.</span><span class="sxs-lookup"><span data-stu-id="e53bc-132">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e53bc-133">Замечания</span><span class="sxs-lookup"><span data-stu-id="e53bc-133">Remarks</span></span>

<span data-ttu-id="e53bc-134">Метод **IMsgServiceAdmin::OpenProfileSection** открывает раздел профиля, объект, который поддерживает интерфейс [IProfSect](iprofsectimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="e53bc-134">The **IMsgServiceAdmin::OpenProfileSection** method opens a profile section, an object that supports the [IProfSect](iprofsectimapiprop.md) interface.</span></span> <span data-ttu-id="e53bc-135">Разделы профилей используются для чтения и записи данных в профиль сеанса.</span><span class="sxs-lookup"><span data-stu-id="e53bc-135">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
 <span data-ttu-id="e53bc-136">**OpenProfileSection** не может использоваться для открытия разделов профиля, принадлежащие отдельные службы поставщиков, если не используется MAPI_FORCE_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="e53bc-136">**OpenProfileSection** cannot be used to open profile sections owned by individual service providers unless MAPI_FORCE_ACCESS is used.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e53bc-137">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="e53bc-137">Notes to callers</span></span>

<span data-ttu-id="e53bc-138">Несколько клиентов могут открывать профиля с разрешением только для чтения, но только один клиент может открыть профиля с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="e53bc-138">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="e53bc-139">Если другой клиент имеет откройте попытаться открыть путем вызова **OpenProfileSection** с установленным флагом MAPI_MODIFY раздела профиля, вызов завершится с ошибкой, возвращая MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="e53bc-139">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="e53bc-140">Происходит сбой операции open только для чтения, если разделе открыт для записи.</span><span class="sxs-lookup"><span data-stu-id="e53bc-140">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="e53bc-141">Можно создать профиля путем вызова **OpenProfileSection** с флагом MAPI_MODIFY и несуществующий [MAPIUID](mapiuid.md) структуры с помощью параметра _lpUID_ .</span><span class="sxs-lookup"><span data-stu-id="e53bc-141">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent [MAPIUID](mapiuid.md) structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="e53bc-142">Убедитесь, что вы установили MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="e53bc-142">Be sure you specify MAPI_MODIFY.</span></span> <span data-ttu-id="e53bc-143">Если необходимо задать _lpUID_ для указания на несуществующий **MAPIUID** и **OpenProfileSection** задано значение использовать режим по умолчанию доступа только для чтения, вызов завершится с ошибкой с MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="e53bc-143">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e53bc-144">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="e53bc-144">MFCMAPI reference</span></span>

<span data-ttu-id="e53bc-145">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="e53bc-145">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e53bc-146">**����**</span><span class="sxs-lookup"><span data-stu-id="e53bc-146">**File**</span></span>|<span data-ttu-id="e53bc-147">**�������**</span><span class="sxs-lookup"><span data-stu-id="e53bc-147">**Function**</span></span>|<span data-ttu-id="e53bc-148">**�����������**</span><span class="sxs-lookup"><span data-stu-id="e53bc-148">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e53bc-149">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="e53bc-149">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="e53bc-150">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="e53bc-150">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="e53bc-151">Mfcmapi (en) использует метод **IMsgServiceAdmin::OpenProfileSection** для открытия профиля.</span><span class="sxs-lookup"><span data-stu-id="e53bc-151">MFCMAPI uses the **IMsgServiceAdmin::OpenProfileSection** method to open a profile section.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e53bc-152">См. также</span><span class="sxs-lookup"><span data-stu-id="e53bc-152">See also</span></span>



[<span data-ttu-id="e53bc-153">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e53bc-153">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="e53bc-154">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="e53bc-154">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="e53bc-155">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e53bc-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="e53bc-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="e53bc-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="e53bc-157">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e53bc-157">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="e53bc-158">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="e53bc-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

