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
ms.openlocfilehash: 0f917989d9bac403f2bea5b2d6699b7a1caf2008
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573014"
---
# <a name="iprovideradminopenprofilesection"></a><span data-ttu-id="47b7b-103">IProviderAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="47b7b-103">IProviderAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="47b7b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47b7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47b7b-105">Открывает профиля из текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшей доступа.</span><span class="sxs-lookup"><span data-stu-id="47b7b-105">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="47b7b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="47b7b-106">Parameters</span></span>

 <span data-ttu-id="47b7b-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="47b7b-107">_lpUID_</span></span>
  
> <span data-ttu-id="47b7b-108">[in] Указатель на структуру [MAPIUID](mapiuid.md) , который содержит уникальный идентификатор для профиля раздел, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="47b7b-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the profile section to be opened.</span></span> <span data-ttu-id="47b7b-109">Клиенты не должны передать значение NULL для параметра _lpUID_ .</span><span class="sxs-lookup"><span data-stu-id="47b7b-109">Clients must not pass NULL for the  _lpUID_ parameter.</span></span> <span data-ttu-id="47b7b-110">Поставщиков услуг можно передать значение NULL для получения **MAPIUID** , когда он совершает вызов из их функций точки входа службы сообщения.</span><span class="sxs-lookup"><span data-stu-id="47b7b-110">Service providers can pass NULL to retrieve the **MAPIUID** when they call from their message service entry point functions.</span></span> 
    
 <span data-ttu-id="47b7b-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="47b7b-111">_lpInterface_</span></span>
  
> <span data-ttu-id="47b7b-112">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="47b7b-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="47b7b-113">В разделе профиль стандартный интерфейс (**IProfSect**), возвращаемых результатов передаче значения NULL.</span><span class="sxs-lookup"><span data-stu-id="47b7b-113">Passing NULL results in the profile section's standard interface (**IProfSect**) being returned.</span></span> 
    
 <span data-ttu-id="47b7b-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="47b7b-114">_ulFlags_</span></span>
  
> <span data-ttu-id="47b7b-115">[in] Битовая маска флаги, который управляет способа открытия раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="47b7b-115">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="47b7b-116">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="47b7b-116">The following flags can be set:</span></span>
    
<span data-ttu-id="47b7b-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="47b7b-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="47b7b-118">Позволяет **OpenProfileSection** для возврата успешно, возможно до раздела профиля доступными для вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="47b7b-118">Enables **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the caller.</span></span> <span data-ttu-id="47b7b-119">Если в разделе профиль не поддерживается, последующие подключения к нему может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="47b7b-119">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="47b7b-120">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="47b7b-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="47b7b-121">Запросы на разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="47b7b-121">Requests read/write permission.</span></span> <span data-ttu-id="47b7b-122">По умолчанию объекты открываются с разрешением только для чтения и звонящие не должны работать предполагается, что что назначено разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="47b7b-122">By default, objects are opened with read-only permission, and callers should not work on the assumption that read/write permission has been granted.</span></span> <span data-ttu-id="47b7b-123">Клиенты не разрешены разрешение на чтение и запись к разделам поставщика профиля.</span><span class="sxs-lookup"><span data-stu-id="47b7b-123">Clients are not allowed read/write permission to provider sections of the profile.</span></span>
    
<span data-ttu-id="47b7b-124">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="47b7b-124">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="47b7b-125">Разрешает доступ всех разделах профилей, даже теми, поставщиками отдельные службы.</span><span class="sxs-lookup"><span data-stu-id="47b7b-125">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="47b7b-126">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="47b7b-126">_lppProfSect_</span></span>
  
> <span data-ttu-id="47b7b-127">[out] Указатель на указатель на раздел профилей.</span><span class="sxs-lookup"><span data-stu-id="47b7b-127">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="47b7b-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="47b7b-128">Return value</span></span>

<span data-ttu-id="47b7b-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="47b7b-129">S_OK</span></span> 
  
> <span data-ttu-id="47b7b-130">В разделе профилей успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="47b7b-130">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="47b7b-131">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="47b7b-131">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="47b7b-132">Предпринята попытка изменения раздела профиля только для чтения или для доступа к объекту, для которого пользователь имеет недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="47b7b-132">An attempt was made to modify a read-only profile section or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="47b7b-133">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="47b7b-133">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="47b7b-134">В разделе запрошенные профиля не существует.</span><span class="sxs-lookup"><span data-stu-id="47b7b-134">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="47b7b-135">Замечания</span><span class="sxs-lookup"><span data-stu-id="47b7b-135">Remarks</span></span>

<span data-ttu-id="47b7b-136">Метод **IProviderAdmin::OpenProfileSection** открывает раздел профилей, включение вызывающего абонента для чтения данных из и возможно записи сведений о текущей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="47b7b-136">The **IProviderAdmin::OpenProfileSection** method opens a profile section, enabling the caller to read information from and possibly write information to the active profile.</span></span> 
  
<span data-ttu-id="47b7b-137">Клиенты не могут открывать профилей разделов, относящихся к поставщиков с помощью метода **OpenProfileSection** .</span><span class="sxs-lookup"><span data-stu-id="47b7b-137">Clients cannot open profile sections that belong to providers by using the **OpenProfileSection** method.</span></span> 
  
<span data-ttu-id="47b7b-138">Несколько клиентов или поставщиков услуг можно одновременно открыть профиля с разрешением только для чтения.</span><span class="sxs-lookup"><span data-stu-id="47b7b-138">Multiple clients or service providers can simultaneously open a profile section with read-only permission.</span></span> <span data-ttu-id="47b7b-139">Тем не менее при открытии получившие разрешение на чтение и запись профиля нет других вызовов невозможны откройте раздел, независимо от типа доступа.</span><span class="sxs-lookup"><span data-stu-id="47b7b-139">However, when a profile section is open with read/write permission, no other calls can be made to open the section, regardless of the type of access.</span></span> <span data-ttu-id="47b7b-140">Если раздел профилей открыт с разрешением только для чтения, следующий вызов метода, запрашивающих разрешение на чтение и запись завершится с MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="47b7b-140">If a profile section is open with read-only permission, a subsequent call to request read/write permission will fail with MAPI_E_NO_ACCESS.</span></span> <span data-ttu-id="47b7b-141">Аналогичным образом Если раздел открыт с разрешением на чтение и запись, следующий вызов метода, запрашивающих разрешение на чтение также не будет работать.</span><span class="sxs-lookup"><span data-stu-id="47b7b-141">Likewise, if a section is open with read/write permission, a subsequent call to request read-only permission will also fail.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="47b7b-142">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="47b7b-142">Notes to callers</span></span>

<span data-ttu-id="47b7b-143">Если запрос, который **OpenProfileSection** открыть несуществующий профиля, передав MAPI_MODIFY в _ulFlags_ и будет создана Неизвестная **MAPIUID** в _lpUID_, в разделе профилей.</span><span class="sxs-lookup"><span data-stu-id="47b7b-143">If you request that **OpenProfileSection** open a nonexistent profile section by passing MAPI_MODIFY in  _ulFlags_ and an unknown **MAPIUID** in  _lpUID_, the profile section will be created.</span></span> 
  
<span data-ttu-id="47b7b-144">При запросе, **OpenProfileSection** открыть несуществующий раздел с разрешением только для чтения, возвращает MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="47b7b-144">If you request that **OpenProfileSection** open a nonexistent section with read-only permission, it returns MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="47b7b-145">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="47b7b-145">MFCMAPI reference</span></span>

<span data-ttu-id="47b7b-146">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="47b7b-146">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="47b7b-147">**Файл**</span><span class="sxs-lookup"><span data-stu-id="47b7b-147">**File**</span></span>|<span data-ttu-id="47b7b-148">**Функция**</span><span class="sxs-lookup"><span data-stu-id="47b7b-148">**Function**</span></span>|<span data-ttu-id="47b7b-149">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="47b7b-149">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="47b7b-150">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="47b7b-150">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="47b7b-151">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="47b7b-151">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="47b7b-152">Mfcmapi (en) использует метод **IProviderAdmin::OpenProfileSection** для открытия профиля из текущего профиля.</span><span class="sxs-lookup"><span data-stu-id="47b7b-152">MFCMAPI uses the **IProviderAdmin::OpenProfileSection** method to open a profile section from the current profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="47b7b-153">См. также</span><span class="sxs-lookup"><span data-stu-id="47b7b-153">See also</span></span>



[<span data-ttu-id="47b7b-154">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="47b7b-154">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="47b7b-155">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="47b7b-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="47b7b-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="47b7b-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="47b7b-157">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="47b7b-157">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


[<span data-ttu-id="47b7b-158">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="47b7b-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

