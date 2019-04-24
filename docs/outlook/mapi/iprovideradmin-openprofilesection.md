---
title: Ипровидерадминопенпрофилесектион
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301549"
---
# <a name="iprovideradminopenprofilesection"></a><span data-ttu-id="c5264-103">IProviderAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="c5264-103">IProviderAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="c5264-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5264-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5264-105">Открывает раздел профиля из текущего профиля и возвращает указатель [ипрофсект](iprofsectimapiprop.md) для получения дальнейших прав.</span><span class="sxs-lookup"><span data-stu-id="c5264-105">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="c5264-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c5264-106">Parameters</span></span>

 <span data-ttu-id="c5264-107">_Лпуид_</span><span class="sxs-lookup"><span data-stu-id="c5264-107">_lpUID_</span></span>
  
> <span data-ttu-id="c5264-108">возврата Указатель на структуру [мапиуид](mapiuid.md) , которая содержит уникальный идентификатор для открываемого раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="c5264-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the profile section to be opened.</span></span> <span data-ttu-id="c5264-109">Клиенты не должны передавать значение NULL для параметра _лпуид_ .</span><span class="sxs-lookup"><span data-stu-id="c5264-109">Clients must not pass NULL for the  _lpUID_ parameter.</span></span> <span data-ttu-id="c5264-110">Поставщики услуг могут передавать значение NULL, чтобы получить **мапиуид** при вызове из функций точки входа службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="c5264-110">Service providers can pass NULL to retrieve the **MAPIUID** when they call from their message service entry point functions.</span></span> 
    
 <span data-ttu-id="c5264-111">_Лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="c5264-111">_lpInterface_</span></span>
  
> <span data-ttu-id="c5264-112">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к разделу профиля.</span><span class="sxs-lookup"><span data-stu-id="c5264-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="c5264-113">Передача результатов NULL в стандартный интерфейс раздела профиля (**ипрофсект**), который возвращается.</span><span class="sxs-lookup"><span data-stu-id="c5264-113">Passing NULL results in the profile section's standard interface (**IProfSect**) being returned.</span></span> 
    
 <span data-ttu-id="c5264-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c5264-114">_ulFlags_</span></span>
  
> <span data-ttu-id="c5264-115">возврата Битовая маска флагов, которые управляют способом открытия раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="c5264-115">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="c5264-116">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="c5264-116">The following flags can be set:</span></span>
    
<span data-ttu-id="c5264-117">МАПИ_ДЕФЕРРЕД_ЕРРОРС</span><span class="sxs-lookup"><span data-stu-id="c5264-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="c5264-118">Позволяет **опенпрофилесектион** успешно возвращать значение, возможно, перед тем, как раздел профиля будет полностью доступен для вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="c5264-118">Enables **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the caller.</span></span> <span data-ttu-id="c5264-119">Если раздел profile недоступен, то при следующем вызове он может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="c5264-119">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="c5264-120">МАПИ_МОДИФИ</span><span class="sxs-lookup"><span data-stu-id="c5264-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="c5264-121">ЗаПрашивает разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="c5264-121">Requests read/write permission.</span></span> <span data-ttu-id="c5264-122">По умолчанию объекты открываются с разрешением только для чтения, а абоненты не должны работать в предположении, что предоставлено разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="c5264-122">By default, objects are opened with read-only permission, and callers should not work on the assumption that read/write permission has been granted.</span></span> <span data-ttu-id="c5264-123">Клиентам не разрешено разрешение на чтение и запись для разделов поставщика в профиле.</span><span class="sxs-lookup"><span data-stu-id="c5264-123">Clients are not allowed read/write permission to provider sections of the profile.</span></span>
    
<span data-ttu-id="c5264-124">МАПИ_ФОРЦЕ_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="c5264-124">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="c5264-125">Предоставляет доступ ко всем разделам профиля, даже к тем, которые принадлежат отдельным поставщикам услуг.</span><span class="sxs-lookup"><span data-stu-id="c5264-125">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="c5264-126">_Лпппрофсект_</span><span class="sxs-lookup"><span data-stu-id="c5264-126">_lppProfSect_</span></span>
  
> <span data-ttu-id="c5264-127">вышли Указатель на указатель на раздел профиля.</span><span class="sxs-lookup"><span data-stu-id="c5264-127">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c5264-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c5264-128">Return value</span></span>

<span data-ttu-id="c5264-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="c5264-129">S_OK</span></span> 
  
> <span data-ttu-id="c5264-130">Раздел профиля успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="c5264-130">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="c5264-131">МАПИ_Е_НО_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="c5264-131">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="c5264-132">Была предпринята попытка изменить раздел профиля, предназначенный только для чтения, или доступ к объекту, для которого у пользователя недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="c5264-132">An attempt was made to modify a read-only profile section or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="c5264-133">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="c5264-133">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="c5264-134">Запрошенный раздел профиля не существует.</span><span class="sxs-lookup"><span data-stu-id="c5264-134">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c5264-135">Замечания</span><span class="sxs-lookup"><span data-stu-id="c5264-135">Remarks</span></span>

<span data-ttu-id="c5264-136">Метод **ипровидерадмин:: опенпрофилесектион** открывает раздел профиля, что позволяет вызывающему абоненту считывать сведения из активного профиля и, возможно, записывать их.</span><span class="sxs-lookup"><span data-stu-id="c5264-136">The **IProviderAdmin::OpenProfileSection** method opens a profile section, enabling the caller to read information from and possibly write information to the active profile.</span></span> 
  
<span data-ttu-id="c5264-137">Клиенты не могут открывать разделы профилей, принадлежащие поставщикам, с помощью метода **опенпрофилесектион** .</span><span class="sxs-lookup"><span data-stu-id="c5264-137">Clients cannot open profile sections that belong to providers by using the **OpenProfileSection** method.</span></span> 
  
<span data-ttu-id="c5264-138">Несколько клиентов или поставщики услуг могут одновременно открыть раздел профиля с разрешением только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c5264-138">Multiple clients or service providers can simultaneously open a profile section with read-only permission.</span></span> <span data-ttu-id="c5264-139">Тем не менее, если раздел профиля открыт с разрешением на чтение и запись, другие вызовы не могут быть выполнены для открытия раздела независимо от типа доступа.</span><span class="sxs-lookup"><span data-stu-id="c5264-139">However, when a profile section is open with read/write permission, no other calls can be made to open the section, regardless of the type of access.</span></span> <span data-ttu-id="c5264-140">Если раздел профиля открыт с разрешением "только чтение", последующий вызов запроса на чтение и запись завершится с МАПИ_Е_НО_АКЦЕСС.</span><span class="sxs-lookup"><span data-stu-id="c5264-140">If a profile section is open with read-only permission, a subsequent call to request read/write permission will fail with MAPI_E_NO_ACCESS.</span></span> <span data-ttu-id="c5264-141">Аналогично, если раздел открыт с разрешением на чтение и запись, то при последующем вызове запроса доступа только для чтения также произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="c5264-141">Likewise, if a section is open with read/write permission, a subsequent call to request read-only permission will also fail.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c5264-142">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="c5264-142">Notes to callers</span></span>

<span data-ttu-id="c5264-143">Если вы запросите, что **опенпрофилесектион** откроет несуществующий раздел профиля, передав Мапи_модифи в _ulFlags_ и неизвестном **мапиуид** в _лпуид_, будет создан раздел профиля.</span><span class="sxs-lookup"><span data-stu-id="c5264-143">If you request that **OpenProfileSection** open a nonexistent profile section by passing MAPI_MODIFY in  _ulFlags_ and an unknown **MAPIUID** in  _lpUID_, the profile section will be created.</span></span> 
  
<span data-ttu-id="c5264-144">Если вы запросите, что **опенпрофилесектион** откроет несуществующий раздел с разрешением только для чтения, он возвращает мапи_е_нот_фаунд.</span><span class="sxs-lookup"><span data-stu-id="c5264-144">If you request that **OpenProfileSection** open a nonexistent section with read-only permission, it returns MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c5264-145">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c5264-145">MFCMAPI reference</span></span>

<span data-ttu-id="c5264-146">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="c5264-146">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c5264-147">**Файл**</span><span class="sxs-lookup"><span data-stu-id="c5264-147">**File**</span></span>|<span data-ttu-id="c5264-148">**Функция**</span><span class="sxs-lookup"><span data-stu-id="c5264-148">**Function**</span></span>|<span data-ttu-id="c5264-149">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="c5264-149">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c5264-150">Мапипрофилефунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="c5264-150">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="c5264-151">Опенпрофилесектион</span><span class="sxs-lookup"><span data-stu-id="c5264-151">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="c5264-152">MFCMAPI использует метод **ипровидерадмин:: опенпрофилесектион** , чтобы открыть раздел профиля из текущего профиля.</span><span class="sxs-lookup"><span data-stu-id="c5264-152">MFCMAPI uses the **IProviderAdmin::OpenProfileSection** method to open a profile section from the current profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c5264-153">См. также</span><span class="sxs-lookup"><span data-stu-id="c5264-153">See also</span></span>



[<span data-ttu-id="c5264-154">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c5264-154">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="c5264-155">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c5264-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="c5264-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="c5264-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="c5264-157">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c5264-157">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


[<span data-ttu-id="c5264-158">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="c5264-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

