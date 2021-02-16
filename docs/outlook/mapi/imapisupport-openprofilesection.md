---
title: IMAPISupportOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenProfileSection
api_type:
- COM
ms.assetid: cd1fa994-9531-46c4-94e5-505e7f90b884
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e7f13acc34a77b79057d32fd4049db7222dadf49
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411388"
---
# <a name="imapisupportopenprofilesection"></a><span data-ttu-id="6ced9-103">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="6ced9-103">IMAPISupport::OpenProfileSection</span></span>

  
  
<span data-ttu-id="6ced9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ced9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ced9-105">Открывает раздел текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="6ced9-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a><span data-ttu-id="6ced9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ced9-106">Parameters</span></span>

 <span data-ttu-id="6ced9-107">_lpUid_</span><span class="sxs-lookup"><span data-stu-id="6ced9-107">_lpUid_</span></span>
  
> <span data-ttu-id="6ced9-108">[in] Указатель на структуру [MAPIUID,](mapiuid.md) которая определяет открываемую секцию профиля.</span><span class="sxs-lookup"><span data-stu-id="6ced9-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section to be opened.</span></span> <span data-ttu-id="6ced9-109">Передача NULL для  _параметра lpUid_ открывает раздел профиля вызывающего.</span><span class="sxs-lookup"><span data-stu-id="6ced9-109">Passing NULL for the  _lpUid_ parameter opens the caller's profile section.</span></span> 
    
 <span data-ttu-id="6ced9-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6ced9-110">_ulFlags_</span></span>
  
> <span data-ttu-id="6ced9-111">[in] Битоваяmas флагов, которая управляет открытием раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="6ced9-111">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="6ced9-112">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="6ced9-112">The following flags can be set:</span></span>
    
<span data-ttu-id="6ced9-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="6ced9-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="6ced9-114">Позволяет **OpenProfileSection** успешно возвращаться, возможно, до того, как раздел профиля будет полностью доступен вызываемой.</span><span class="sxs-lookup"><span data-stu-id="6ced9-114">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully accessible to the caller.</span></span> <span data-ttu-id="6ced9-115">Если раздел профиля не доступен, последующий вызов объекта может привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="6ced9-115">If the profile section is not accessible, making a subsequent object call can result in an error.</span></span> 
    
<span data-ttu-id="6ced9-116">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="6ced9-116">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="6ced9-117">Запрашивает разрешение на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="6ced9-117">Requests read/write permission.</span></span> <span data-ttu-id="6ced9-118">По умолчанию объекты открываются как объекты только для чтения, и вызывающим не следует работать при предположении, что разрешение на чтение и записи предоставлено.</span><span class="sxs-lookup"><span data-stu-id="6ced9-118">By default, objects are opened as read-only, and callers should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="6ced9-119">_lppProfileObj_</span><span class="sxs-lookup"><span data-stu-id="6ced9-119">_lppProfileObj_</span></span>
  
> <span data-ttu-id="6ced9-120">[out] Указатель на указатель на открытый раздел профиля.</span><span class="sxs-lookup"><span data-stu-id="6ced9-120">[out] A pointer to a pointer to the opened profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6ced9-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ced9-121">Return value</span></span>

<span data-ttu-id="6ced9-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="6ced9-122">S_OK</span></span> 
  
> <span data-ttu-id="6ced9-123">Раздел профиля успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="6ced9-123">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="6ced9-124">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="6ced9-124">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="6ced9-125">Предпринята попытка изменить раздел профиля, доступный только для чтения, или получить доступ к объекту, у которого у вызываемого объекта недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="6ced9-125">An attempt was made to modify a read-only profile section or to access an object for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="6ced9-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="6ced9-126">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="6ced9-127">Раздел профиля, связанный с идентификатором записи, переданным _в lpEntryID, не существует._</span><span class="sxs-lookup"><span data-stu-id="6ced9-127">There is not a profile section associated with the entry identifier passed in  _lpEntryID_.</span></span>
    
<span data-ttu-id="6ced9-128">MAPI_E_UNKNOWN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="6ced9-128">MAPI_E_UNKNOWN_FLAGS</span></span> 
  
> <span data-ttu-id="6ced9-129">Использовались зарезервированные или неподтверченные флаги, поэтому операция не была завершена.</span><span class="sxs-lookup"><span data-stu-id="6ced9-129">Reserved or unsupported flags were used and, therefore, the operation did not complete.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6ced9-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="6ced9-130">Remarks</span></span>

<span data-ttu-id="6ced9-131">Метод **IMAPISupport::OpenProfileSection** реализован для всех объектов поддержки.</span><span class="sxs-lookup"><span data-stu-id="6ced9-131">The **IMAPISupport::OpenProfileSection** method is implemented for all support objects.</span></span> <span data-ttu-id="6ced9-132">Поставщики услуг и службы сообщений вызвать **OpenProfileSection,** чтобы открыть раздел профиля и получить указатель на реализацию интерфейса **IProfSect.**</span><span class="sxs-lookup"><span data-stu-id="6ced9-132">Service providers and message services call **OpenProfileSection** to open a profile section and retrieve a pointer to its **IProfSect** interface implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6ced9-133">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="6ced9-133">Notes to callers</span></span>

 <span data-ttu-id="6ced9-134">**OpenProfileSection** открывает разделы профиля только для чтения, если в параметре  _ulFlags_ не установлен флаг MAPI_MODIFY, а разрешения достаточно.</span><span class="sxs-lookup"><span data-stu-id="6ced9-134">**OpenProfileSection** opens profile sections as read-only, unless you set the MAPI_MODIFY flag in the  _ulFlags_ parameter and your permission is sufficient.</span></span> <span data-ttu-id="6ced9-135">Установка этого флага не гарантирует разрешение на чтение и записи; предоставленные разрешения зависят от уровня доступа и объекта.</span><span class="sxs-lookup"><span data-stu-id="6ced9-135">Setting this flag does not guarantee read/write permission; the permissions that you are granted depend on your access level and the object.</span></span> 
  
<span data-ttu-id="6ced9-136">Если **OpenProfileSection** пытается открыть несущестуный раздел профиля только для чтения, он возвращает MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="6ced9-136">If **OpenProfileSection** attempts to open a nonexistent profile section as read-only, it returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="6ced9-137">Если **OpenProfileSection** пытается открыть несущестуный раздел профиля как чтение и записи, он создает раздел профиля и возвращает **указатель IProfSect.**</span><span class="sxs-lookup"><span data-stu-id="6ced9-137">If **OpenProfileSection** attempts to open a nonexistent profile section as read/write, it creates the profile section and returns the **IProfSect** pointer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6ced9-138">См. также</span><span class="sxs-lookup"><span data-stu-id="6ced9-138">See also</span></span>



[<span data-ttu-id="6ced9-139">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6ced9-139">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="6ced9-140">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6ced9-140">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="6ced9-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="6ced9-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="6ced9-142">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6ced9-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

