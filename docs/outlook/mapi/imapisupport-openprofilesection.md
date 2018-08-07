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
ms.openlocfilehash: 2f45028219f0f5f4cc881db3bc512626b3ad2f4c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809149"
---
# <a name="imapisupportopenprofilesection"></a><span data-ttu-id="a3b4b-103">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="a3b4b-103">IMAPISupport::OpenProfileSection</span></span>

  
  
<span data-ttu-id="a3b4b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a3b4b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a3b4b-105">Откроется раздел текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшей доступа.</span><span class="sxs-lookup"><span data-stu-id="a3b4b-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a><span data-ttu-id="a3b4b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3b4b-106">Parameters</span></span>

 <span data-ttu-id="a3b4b-107">_lpUid_</span><span class="sxs-lookup"><span data-stu-id="a3b4b-107">_lpUid_</span></span>
  
> <span data-ttu-id="a3b4b-108">[in] Указатель на структуру [MAPIUID](mapiuid.md) , который определяет раздел профилей, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="a3b4b-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section to be opened.</span></span> <span data-ttu-id="a3b4b-109">Значение NULL для параметра _lpUid_ откроется раздел профилей вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="a3b4b-109">Passing NULL for the  _lpUid_ parameter opens the caller's profile section.</span></span> 
    
 <span data-ttu-id="a3b4b-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a3b4b-110">_ulFlags_</span></span>
  
> <span data-ttu-id="a3b4b-111">[in] Битовая маска флаги, который управляет способа открытия раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="a3b4b-111">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="a3b4b-112">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="a3b4b-112">The following flags can be set:</span></span>
    
<span data-ttu-id="a3b4b-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="a3b4b-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="a3b4b-114">Позволяет **OpenProfileSection** для возврата успешно, возможно перед профиль раздел полностью доступен для вызова.</span><span class="sxs-lookup"><span data-stu-id="a3b4b-114">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully accessible to the caller.</span></span> <span data-ttu-id="a3b4b-115">Если недоступен в разделе профилей, вызов последующих объектов может привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="a3b4b-115">If the profile section is not accessible, making a subsequent object call can result in an error.</span></span> 
    
<span data-ttu-id="a3b4b-116">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="a3b4b-116">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="a3b4b-117">Запросы на разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="a3b4b-117">Requests read/write permission.</span></span> <span data-ttu-id="a3b4b-118">По умолчанию объекты открываются только для чтения и звонящие не должны работать предполагается, что что назначено разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="a3b4b-118">By default, objects are opened as read-only, and callers should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="a3b4b-119">_lppProfileObj_</span><span class="sxs-lookup"><span data-stu-id="a3b4b-119">_lppProfileObj_</span></span>
  
> <span data-ttu-id="a3b4b-120">[out] Указатель на указатель на раздел открыт профилей.</span><span class="sxs-lookup"><span data-stu-id="a3b4b-120">[out] A pointer to a pointer to the opened profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a3b4b-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1">Return value</span></span>

<span data-ttu-id="a3b4b-122">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="a3b4b-122">S_OK</span></span> 
  
> <span data-ttu-id="a3b4b-123">В разделе профилей успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="a3b4b-123">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="a3b4b-124">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="a3b4b-124">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="a3b4b-125">Предпринята попытка изменения раздела профиля только для чтения или для доступа к объекту, для которого вызывающий не имеет разрешений.</span><span class="sxs-lookup"><span data-stu-id="a3b4b-125">An attempt was made to modify a read-only profile section or to access an object for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="a3b4b-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a3b4b-126">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="a3b4b-127">Раздел профиля, связанный с идентификатором записи, переданные в _lpEntryID_не существует.</span><span class="sxs-lookup"><span data-stu-id="a3b4b-127">There is not a profile section associated with the entry identifier passed in  _lpEntryID_.</span></span>
    
<span data-ttu-id="a3b4b-128">MAPI_E_UNKNOWN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a3b4b-128">MAPI_E_UNKNOWN_FLAGS</span></span> 
  
> <span data-ttu-id="a3b4b-129">Зарезервированные или неподдерживаемые флаги использовались и, таким образом, операция не завершена.</span><span class="sxs-lookup"><span data-stu-id="a3b4b-129">Reserved or unsupported flags were used and, therefore, the operation did not complete.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a3b4b-130">Замечания</span><span class="sxs-lookup"><span data-stu-id="a3b4b-130">Remarks</span></span>

<span data-ttu-id="a3b4b-131">Метод **IMAPISupport::OpenProfileSection** применяется для всех объектов поддержки.</span><span class="sxs-lookup"><span data-stu-id="a3b4b-131">The **IMAPISupport::OpenProfileSection** method is implemented for all support objects.</span></span> <span data-ttu-id="a3b4b-132">Поставщики службы и службы сообщений вызов **OpenProfileSection** открытие раздела профиля и получить указатель на его реализация интерфейса **IProfSect** .</span><span class="sxs-lookup"><span data-stu-id="a3b4b-132">Service providers and message services call **OpenProfileSection** to open a profile section and retrieve a pointer to its **IProfSect** interface implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a3b4b-133">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="a3b4b-133">Notes to callers</span></span>

 <span data-ttu-id="a3b4b-134">**OpenProfileSection** открывает разделах профиля с доступом только для чтения, если не задан флаг MAPI_MODIFY в параметре _ulFlags_ и разрешение является достаточным.</span><span class="sxs-lookup"><span data-stu-id="a3b4b-134">**OpenProfileSection** opens profile sections as read-only, unless you set the MAPI_MODIFY flag in the  _ulFlags_ parameter and your permission is sufficient.</span></span> <span data-ttu-id="a3b4b-135">Этот флаг установлен не гарантирует разрешение на чтение и запись. разрешения, которые будут предоставлены зависят от вам уровень доступа и объект.</span><span class="sxs-lookup"><span data-stu-id="a3b4b-135">Setting this flag does not guarantee read/write permission; the permissions that you are granted depend on your access level and the object.</span></span> 
  
<span data-ttu-id="a3b4b-136">Если **OpenProfileSection** пытается открыть несуществующий профилей раздел только для чтения, возвращает MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="a3b4b-136">If **OpenProfileSection** attempts to open a nonexistent profile section as read-only, it returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="a3b4b-137">Если **OpenProfileSection** пытается открыть несуществующий профилей раздел для чтения и записи, он создает в разделе профилей и возвращает указатель **IProfSect** .</span><span class="sxs-lookup"><span data-stu-id="a3b4b-137">If **OpenProfileSection** attempts to open a nonexistent profile section as read/write, it creates the profile section and returns the **IProfSect** pointer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a3b4b-138">См. также</span><span class="sxs-lookup"><span data-stu-id="a3b4b-138">See also</span></span>



[<span data-ttu-id="a3b4b-139">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a3b4b-139">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="a3b4b-140">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a3b4b-140">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="a3b4b-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="a3b4b-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="a3b4b-142">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a3b4b-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

