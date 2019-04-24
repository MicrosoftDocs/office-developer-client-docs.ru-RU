---
title: Имаписессионопенпрофилесектион
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenProfileSection
api_type:
- COM
ms.assetid: e2757028-27e7-4fc0-9674-e8e30737ef1d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9d7c1693dfb22ae89afed8cbe1426c1e186f8b2d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329409"
---
# <a name="imapisessionopenprofilesection"></a><span data-ttu-id="e35fe-103">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="e35fe-103">IMAPISession::OpenProfileSection</span></span>

  
  
<span data-ttu-id="e35fe-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e35fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e35fe-105">Открывает раздел текущего профиля и возвращает указатель [ипрофсект](iprofsectimapiprop.md) для получения дальнейших прав.</span><span class="sxs-lookup"><span data-stu-id="e35fe-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="e35fe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e35fe-106">Parameters</span></span>

 <span data-ttu-id="e35fe-107">_Лпуид_</span><span class="sxs-lookup"><span data-stu-id="e35fe-107">_lpUID_</span></span>
  
> <span data-ttu-id="e35fe-108">возврата Указатель на структуру [мапиуид](mapiuid.md) , которая идентифицирует раздел профиля.</span><span class="sxs-lookup"><span data-stu-id="e35fe-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="e35fe-109">_Лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="e35fe-109">_lpInterface_</span></span>
  
> <span data-ttu-id="e35fe-110">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к разделу профиля.</span><span class="sxs-lookup"><span data-stu-id="e35fe-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="e35fe-111">При передаче значения NULL параметр _лпппрофсект_ возвращает указатель на стандартный интерфейс раздела профиля **ипрофсект**.</span><span class="sxs-lookup"><span data-stu-id="e35fe-111">Passing NULL causes the  _lppProfSect_ parameter to return a pointer to the profile section's standard interface, **IProfSect**.</span></span>
    
 <span data-ttu-id="e35fe-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e35fe-112">_ulFlags_</span></span>
  
> <span data-ttu-id="e35fe-113">возврата Битовая маска флагов, которые управляют доступом к разделу профиля.</span><span class="sxs-lookup"><span data-stu-id="e35fe-113">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="e35fe-114">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="e35fe-114">The following flags can be set:</span></span>
    
<span data-ttu-id="e35fe-115">МАПИ_ДЕФЕРРЕД_ЕРРОРС</span><span class="sxs-lookup"><span data-stu-id="e35fe-115">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="e35fe-116">Разрешает успешное возвращение **опенпрофилесектион** , возможно, перед тем, как раздел профиля будет полностью доступен для вызывающего клиента.</span><span class="sxs-lookup"><span data-stu-id="e35fe-116">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="e35fe-117">Если раздел профиля недоступен, то выполнение последующего вызова этого метода может привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="e35fe-117">If the profile section is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="e35fe-118">МАПИ_ФОРЦЕ_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="e35fe-118">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="e35fe-119">Разрешает доступ к разделу профиля, который не принадлежит поставщику.</span><span class="sxs-lookup"><span data-stu-id="e35fe-119">Allows access to a profile section that does not belong to the provider.</span></span>
    
<span data-ttu-id="e35fe-120">МАПИ_МОДИФИ</span><span class="sxs-lookup"><span data-stu-id="e35fe-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="e35fe-121">ЗаПрашивает разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="e35fe-121">Requests read/write permission.</span></span> <span data-ttu-id="e35fe-122">По умолчанию разделы профиля открываются с разрешением "только чтение", и клиенты не должны работать в предположении, что предоставлено разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="e35fe-122">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="e35fe-123">_Лпппрофсект_</span><span class="sxs-lookup"><span data-stu-id="e35fe-123">_lppProfSect_</span></span>
  
> <span data-ttu-id="e35fe-124">вышли Указатель на указатель на раздел профиля.</span><span class="sxs-lookup"><span data-stu-id="e35fe-124">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e35fe-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e35fe-125">Return value</span></span>

<span data-ttu-id="e35fe-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="e35fe-126">S_OK</span></span> 
  
> <span data-ttu-id="e35fe-127">Раздел профиля успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="e35fe-127">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="e35fe-128">МАПИ_Е_НО_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="e35fe-128">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="e35fe-129">Предпринята попытка доступа к разделу профиля, для которого вызывающая сторона не имеет достаточных разрешений.</span><span class="sxs-lookup"><span data-stu-id="e35fe-129">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="e35fe-130">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="e35fe-130">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="e35fe-131">Запрошенный раздел профиля не существует.</span><span class="sxs-lookup"><span data-stu-id="e35fe-131">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e35fe-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e35fe-132">Remarks</span></span>

<span data-ttu-id="e35fe-133">Метод **IMAPISession:: опенпрофилесектион** открывает раздел профиля или объект, который поддерживает интерфейс **ипрофсект** .</span><span class="sxs-lookup"><span data-stu-id="e35fe-133">The **IMAPISession::OpenProfileSection** method opens a profile section or object that supports the **IProfSect** interface.</span></span> <span data-ttu-id="e35fe-134">Разделы профиля используются для чтения и записи информации в профиль сеанса.</span><span class="sxs-lookup"><span data-stu-id="e35fe-134">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
<span data-ttu-id="e35fe-135">Вы не можете использовать **опенпрофилесектион** для открытия разделов профилей, которыми владеют Индивидуальные поставщики услуг, если вы не укажете мапи_форце_акцесс в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="e35fe-135">You cannot use **OpenProfileSection** to open profile sections that individual service providers own unless you specify MAPI_FORCE_ACCESS in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e35fe-136">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="e35fe-136">Notes to callers</span></span>

<span data-ttu-id="e35fe-137">Несколько клиентов могут открыть раздел профиля с разрешением только для чтения, но только один клиент может открыть раздел профиля с разрешениями на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="e35fe-137">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="e35fe-138">Если для другого клиента открыт раздел профиля, который вы пытаетесь открыть с помощью вызова **опенпрофилесектион** с установленным флагом мапи_модифи, вызов завершится неудачей, возвращая мапи_е_но_акцесс.</span><span class="sxs-lookup"><span data-stu-id="e35fe-138">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="e35fe-139">Если раздел открыт для записи, то операция открытия, доступная только для чтения, завершается С ошибкой.</span><span class="sxs-lookup"><span data-stu-id="e35fe-139">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="e35fe-140">Вы можете создать раздел профиля, вызвав **опенпрофилесектион** с флагом мапи_модифи и несуществующей структурой **мапиуид** в параметре _лпуид_ .</span><span class="sxs-lookup"><span data-stu-id="e35fe-140">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent **MAPIUID** structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="e35fe-141">Убедитесь, что вы указали МАПИ_МОДИФИ.</span><span class="sxs-lookup"><span data-stu-id="e35fe-141">Be sure that you specify MAPI_MODIFY.</span></span> <span data-ttu-id="e35fe-142">Если вы настроили _лпуид_ на несуществующий **мапиуид** , и для **опенпрофилесектион** задано использование режима доступа "только чтение" по умолчанию, вызов завершится с мапи_е_нот_фаунд.</span><span class="sxs-lookup"><span data-stu-id="e35fe-142">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e35fe-143">См. также</span><span class="sxs-lookup"><span data-stu-id="e35fe-143">See also</span></span>



[<span data-ttu-id="e35fe-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e35fe-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="e35fe-145">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e35fe-145">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="e35fe-146">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="e35fe-146">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="e35fe-147">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e35fe-147">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

