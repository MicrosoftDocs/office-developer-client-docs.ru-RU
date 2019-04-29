---
title: Имаписуппортопенпрофилесектион
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
# <a name="imapisupportopenprofilesection"></a><span data-ttu-id="99fcf-103">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="99fcf-103">IMAPISupport::OpenProfileSection</span></span>

  
  
<span data-ttu-id="99fcf-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99fcf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99fcf-105">Открывает раздел текущего профиля и возвращает указатель [ипрофсект](iprofsectimapiprop.md) для получения дальнейших прав.</span><span class="sxs-lookup"><span data-stu-id="99fcf-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a><span data-ttu-id="99fcf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="99fcf-106">Parameters</span></span>

 <span data-ttu-id="99fcf-107">_Лпуид_</span><span class="sxs-lookup"><span data-stu-id="99fcf-107">_lpUid_</span></span>
  
> <span data-ttu-id="99fcf-108">возврата Указатель на структуру [мапиуид](mapiuid.md) , которая определяет раздел профиля, который требуется открыть.</span><span class="sxs-lookup"><span data-stu-id="99fcf-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section to be opened.</span></span> <span data-ttu-id="99fcf-109">При передаче значения NULL для параметра _лпуид_ открывается раздел профиля вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="99fcf-109">Passing NULL for the  _lpUid_ parameter opens the caller's profile section.</span></span> 
    
 <span data-ttu-id="99fcf-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="99fcf-110">_ulFlags_</span></span>
  
> <span data-ttu-id="99fcf-111">возврата Битовая маска флагов, которые управляют способом открытия раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="99fcf-111">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="99fcf-112">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="99fcf-112">The following flags can be set:</span></span>
    
<span data-ttu-id="99fcf-113">МАПИ_ДЕФЕРРЕД_ЕРРОРС</span><span class="sxs-lookup"><span data-stu-id="99fcf-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="99fcf-114">Разрешает успешное возвращение **опенпрофилесектион** , возможно, перед тем, как раздел профиля будет полностью доступен для вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="99fcf-114">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully accessible to the caller.</span></span> <span data-ttu-id="99fcf-115">Если раздел профиля недоступен, то выполнение следующего вызова объекта может привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="99fcf-115">If the profile section is not accessible, making a subsequent object call can result in an error.</span></span> 
    
<span data-ttu-id="99fcf-116">МАПИ_МОДИФИ</span><span class="sxs-lookup"><span data-stu-id="99fcf-116">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="99fcf-117">ЗаПрашивает разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="99fcf-117">Requests read/write permission.</span></span> <span data-ttu-id="99fcf-118">По умолчанию объекты открываются как доступные только для чтения, и абоненты не должны работать в предположении, что предоставлено разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="99fcf-118">By default, objects are opened as read-only, and callers should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="99fcf-119">_Лпппрофилеобж_</span><span class="sxs-lookup"><span data-stu-id="99fcf-119">_lppProfileObj_</span></span>
  
> <span data-ttu-id="99fcf-120">вышли Указатель на указатель на открытый раздел профиля.</span><span class="sxs-lookup"><span data-stu-id="99fcf-120">[out] A pointer to a pointer to the opened profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="99fcf-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="99fcf-121">Return value</span></span>

<span data-ttu-id="99fcf-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="99fcf-122">S_OK</span></span> 
  
> <span data-ttu-id="99fcf-123">Раздел профиля успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="99fcf-123">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="99fcf-124">МАПИ_Е_НО_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="99fcf-124">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="99fcf-125">Предпринята попытка изменить раздел профиля, предназначенный только для чтения, или доступ к объекту, для которого вызывающая сторона не имеет достаточных разрешений.</span><span class="sxs-lookup"><span data-stu-id="99fcf-125">An attempt was made to modify a read-only profile section or to access an object for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="99fcf-126">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="99fcf-126">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="99fcf-127">Отсутствует раздел профиля, связанный с идентификатором записи, переданным в _лпентрид_.</span><span class="sxs-lookup"><span data-stu-id="99fcf-127">There is not a profile section associated with the entry identifier passed in  _lpEntryID_.</span></span>
    
<span data-ttu-id="99fcf-128">МАПИ_Е_УНКНОВН_ФЛАГС</span><span class="sxs-lookup"><span data-stu-id="99fcf-128">MAPI_E_UNKNOWN_FLAGS</span></span> 
  
> <span data-ttu-id="99fcf-129">Используются заРезервированные или неподдерживаемые флаги, поэтому операция не выполнена.</span><span class="sxs-lookup"><span data-stu-id="99fcf-129">Reserved or unsupported flags were used and, therefore, the operation did not complete.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="99fcf-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="99fcf-130">Remarks</span></span>

<span data-ttu-id="99fcf-131">Метод **имаписуппорт:: опенпрофилесектион** реализован для всех объектов поддержки.</span><span class="sxs-lookup"><span data-stu-id="99fcf-131">The **IMAPISupport::OpenProfileSection** method is implemented for all support objects.</span></span> <span data-ttu-id="99fcf-132">Поставщики услуг и службы сообщений вызывают **опенпрофилесектион** , чтобы открыть раздел профиля и получить указатель на его реализацию интерфейса **ипрофсект** .</span><span class="sxs-lookup"><span data-stu-id="99fcf-132">Service providers and message services call **OpenProfileSection** to open a profile section and retrieve a pointer to its **IProfSect** interface implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="99fcf-133">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="99fcf-133">Notes to callers</span></span>

 <span data-ttu-id="99fcf-134">**Опенпрофилесектион** открывает разделы профиля только для чтения, если не установлен флаг мапи_модифи в параметре _ulFlags_ , и у вас недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="99fcf-134">**OpenProfileSection** opens profile sections as read-only, unless you set the MAPI_MODIFY flag in the  _ulFlags_ parameter and your permission is sufficient.</span></span> <span data-ttu-id="99fcf-135">Установка этого флага не гарантирует разрешения на чтение и запись; предоставленные разрешения зависят от уровня доступа и объекта.</span><span class="sxs-lookup"><span data-stu-id="99fcf-135">Setting this flag does not guarantee read/write permission; the permissions that you are granted depend on your access level and the object.</span></span> 
  
<span data-ttu-id="99fcf-136">Если **опенпрофилесектион** пытается открыть несуществующий раздел профиля как доступное только для чтения, он возвращает мапи_е_нот_фаунд.</span><span class="sxs-lookup"><span data-stu-id="99fcf-136">If **OpenProfileSection** attempts to open a nonexistent profile section as read-only, it returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="99fcf-137">Если **опенпрофилесектион** пытается открыть несуществующий раздел профиля как доступный для чтения и записи, он создает раздел профиля и возвращает указатель **ипрофсект** .</span><span class="sxs-lookup"><span data-stu-id="99fcf-137">If **OpenProfileSection** attempts to open a nonexistent profile section as read/write, it creates the profile section and returns the **IProfSect** pointer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="99fcf-138">См. также</span><span class="sxs-lookup"><span data-stu-id="99fcf-138">See also</span></span>



[<span data-ttu-id="99fcf-139">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="99fcf-139">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="99fcf-140">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="99fcf-140">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="99fcf-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="99fcf-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="99fcf-142">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="99fcf-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

