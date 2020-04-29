---
title: имаписуппортопенпрофилесектион
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
# <a name="imapisupportopenprofilesection"></a><span data-ttu-id="87acd-103">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="87acd-103">IMAPISupport::OpenProfileSection</span></span>

  
  
<span data-ttu-id="87acd-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87acd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87acd-105">Открывает раздел текущего профиля и возвращает указатель [ипрофсект](iprofsectimapiprop.md) для получения дальнейших прав.</span><span class="sxs-lookup"><span data-stu-id="87acd-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a><span data-ttu-id="87acd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="87acd-106">Parameters</span></span>

 <span data-ttu-id="87acd-107">_лпуид_</span><span class="sxs-lookup"><span data-stu-id="87acd-107">_lpUid_</span></span>
  
> <span data-ttu-id="87acd-108">возврата Указатель на структуру [мапиуид](mapiuid.md) , которая определяет раздел профиля, который требуется открыть.</span><span class="sxs-lookup"><span data-stu-id="87acd-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section to be opened.</span></span> <span data-ttu-id="87acd-109">При передаче значения NULL для параметра _лпуид_ открывается раздел профиля вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="87acd-109">Passing NULL for the  _lpUid_ parameter opens the caller's profile section.</span></span> 
    
 <span data-ttu-id="87acd-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="87acd-110">_ulFlags_</span></span>
  
> <span data-ttu-id="87acd-111">возврата Битовая маска флагов, которые управляют способом открытия раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="87acd-111">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="87acd-112">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="87acd-112">The following flags can be set:</span></span>
    
<span data-ttu-id="87acd-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="87acd-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="87acd-114">Разрешает успешное возвращение **опенпрофилесектион** , возможно, перед тем, как раздел профиля будет полностью доступен для вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="87acd-114">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully accessible to the caller.</span></span> <span data-ttu-id="87acd-115">Если раздел профиля недоступен, то выполнение следующего вызова объекта может привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="87acd-115">If the profile section is not accessible, making a subsequent object call can result in an error.</span></span> 
    
<span data-ttu-id="87acd-116">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="87acd-116">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="87acd-117">Запрашивает разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="87acd-117">Requests read/write permission.</span></span> <span data-ttu-id="87acd-118">По умолчанию объекты открываются как доступные только для чтения, и абоненты не должны работать в предположении, что предоставлено разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="87acd-118">By default, objects are opened as read-only, and callers should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="87acd-119">_лпппрофилеобж_</span><span class="sxs-lookup"><span data-stu-id="87acd-119">_lppProfileObj_</span></span>
  
> <span data-ttu-id="87acd-120">вышли Указатель на указатель на открытый раздел профиля.</span><span class="sxs-lookup"><span data-stu-id="87acd-120">[out] A pointer to a pointer to the opened profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="87acd-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87acd-121">Return value</span></span>

<span data-ttu-id="87acd-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="87acd-122">S_OK</span></span> 
  
> <span data-ttu-id="87acd-123">Раздел профиля успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="87acd-123">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="87acd-124">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="87acd-124">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="87acd-125">Предпринята попытка изменить раздел профиля, предназначенный только для чтения, или доступ к объекту, для которого вызывающая сторона не имеет достаточных разрешений.</span><span class="sxs-lookup"><span data-stu-id="87acd-125">An attempt was made to modify a read-only profile section or to access an object for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="87acd-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="87acd-126">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="87acd-127">Отсутствует раздел профиля, связанный с идентификатором записи, переданным в _лпентрид_.</span><span class="sxs-lookup"><span data-stu-id="87acd-127">There is not a profile section associated with the entry identifier passed in  _lpEntryID_.</span></span>
    
<span data-ttu-id="87acd-128">MAPI_E_UNKNOWN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="87acd-128">MAPI_E_UNKNOWN_FLAGS</span></span> 
  
> <span data-ttu-id="87acd-129">Используются зарезервированные или неподдерживаемые флаги, поэтому операция не выполнена.</span><span class="sxs-lookup"><span data-stu-id="87acd-129">Reserved or unsupported flags were used and, therefore, the operation did not complete.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="87acd-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="87acd-130">Remarks</span></span>

<span data-ttu-id="87acd-131">Метод **имаписуппорт:: опенпрофилесектион** реализован для всех объектов поддержки.</span><span class="sxs-lookup"><span data-stu-id="87acd-131">The **IMAPISupport::OpenProfileSection** method is implemented for all support objects.</span></span> <span data-ttu-id="87acd-132">Поставщики услуг и службы сообщений вызывают **опенпрофилесектион** , чтобы открыть раздел профиля и получить указатель на его реализацию интерфейса **ипрофсект** .</span><span class="sxs-lookup"><span data-stu-id="87acd-132">Service providers and message services call **OpenProfileSection** to open a profile section and retrieve a pointer to its **IProfSect** interface implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="87acd-133">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="87acd-133">Notes to callers</span></span>

 <span data-ttu-id="87acd-134">**Опенпрофилесектион** открывает разделы профиля только для чтения, если не установлен флаг MAPI_MODIFY в параметре _ulFlags_ , а разрешение недостаточно.</span><span class="sxs-lookup"><span data-stu-id="87acd-134">**OpenProfileSection** opens profile sections as read-only, unless you set the MAPI_MODIFY flag in the  _ulFlags_ parameter and your permission is sufficient.</span></span> <span data-ttu-id="87acd-135">Установка этого флага не гарантирует разрешения на чтение и запись; предоставленные разрешения зависят от уровня доступа и объекта.</span><span class="sxs-lookup"><span data-stu-id="87acd-135">Setting this flag does not guarantee read/write permission; the permissions that you are granted depend on your access level and the object.</span></span> 
  
<span data-ttu-id="87acd-136">Если **опенпрофилесектион** пытается открыть несуществующий раздел профиля как доступный только для чтения, он возвращает MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="87acd-136">If **OpenProfileSection** attempts to open a nonexistent profile section as read-only, it returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="87acd-137">Если **опенпрофилесектион** пытается открыть несуществующий раздел профиля как доступный для чтения и записи, он создает раздел профиля и возвращает указатель **ипрофсект** .</span><span class="sxs-lookup"><span data-stu-id="87acd-137">If **OpenProfileSection** attempts to open a nonexistent profile section as read/write, it creates the profile section and returns the **IProfSect** pointer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="87acd-138">См. также</span><span class="sxs-lookup"><span data-stu-id="87acd-138">See also</span></span>



[<span data-ttu-id="87acd-139">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="87acd-139">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="87acd-140">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="87acd-140">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="87acd-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="87acd-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="87acd-142">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="87acd-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

