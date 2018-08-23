---
title: IMAPISessionOpenProfileSection
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
ms.openlocfilehash: feb12be5cc836a0c7ff90dd5054a34d9df4b6622
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568191"
---
# <a name="imapisessionopenprofilesection"></a><span data-ttu-id="7e2c8-103">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="7e2c8-103">IMAPISession::OpenProfileSection</span></span>

  
  
<span data-ttu-id="7e2c8-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e2c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e2c8-105">Откроется раздел текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшей доступа.</span><span class="sxs-lookup"><span data-stu-id="7e2c8-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="7e2c8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e2c8-106">Parameters</span></span>

 <span data-ttu-id="7e2c8-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="7e2c8-107">_lpUID_</span></span>
  
> <span data-ttu-id="7e2c8-108">[in] Указатель на структуру [MAPIUID](mapiuid.md) , идентифицирующий раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="7e2c8-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="7e2c8-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="7e2c8-109">_lpInterface_</span></span>
  
> <span data-ttu-id="7e2c8-110">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="7e2c8-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="7e2c8-111">Значение NULL вызывает параметр _lppProfSect_ для возврата указателя на стандартный интерфейс раздела профиля, **IProfSect**.</span><span class="sxs-lookup"><span data-stu-id="7e2c8-111">Passing NULL causes the  _lppProfSect_ parameter to return a pointer to the profile section's standard interface, **IProfSect**.</span></span>
    
 <span data-ttu-id="7e2c8-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7e2c8-112">_ulFlags_</span></span>
  
> <span data-ttu-id="7e2c8-113">[in] Битовая маска, что управляет доступом к разделу профиль флаги.</span><span class="sxs-lookup"><span data-stu-id="7e2c8-113">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="7e2c8-114">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="7e2c8-114">The following flags can be set:</span></span>
    
<span data-ttu-id="7e2c8-115">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="7e2c8-115">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="7e2c8-116">Позволяет **OpenProfileSection** для возврата успешно, возможно перед профиль раздела доступными для клиента.</span><span class="sxs-lookup"><span data-stu-id="7e2c8-116">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="7e2c8-117">Если в разделе профиль не поддерживается, последующие подключения к нему может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="7e2c8-117">If the profile section is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="7e2c8-118">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="7e2c8-118">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="7e2c8-119">Позволяет получить доступ к разделу профиля, которая не относится к поставщику.</span><span class="sxs-lookup"><span data-stu-id="7e2c8-119">Allows access to a profile section that does not belong to the provider.</span></span>
    
<span data-ttu-id="7e2c8-120">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="7e2c8-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="7e2c8-121">Запросы на разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="7e2c8-121">Requests read/write permission.</span></span> <span data-ttu-id="7e2c8-122">По умолчанию разделы профилей открываются с разрешением только для чтения и клиенты не должны работать предполагается, что что назначено разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="7e2c8-122">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="7e2c8-123">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="7e2c8-123">_lppProfSect_</span></span>
  
> <span data-ttu-id="7e2c8-124">[out] Указатель на указатель на раздел профилей.</span><span class="sxs-lookup"><span data-stu-id="7e2c8-124">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7e2c8-125">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="7e2c8-125">Return value</span></span>

<span data-ttu-id="7e2c8-126">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="7e2c8-126">S_OK</span></span> 
  
> <span data-ttu-id="7e2c8-127">В разделе профилей успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="7e2c8-127">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="7e2c8-128">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="7e2c8-128">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="7e2c8-129">Предпринята попытка получить доступ к раздела профиля, для которого вызывающий не имеет разрешений.</span><span class="sxs-lookup"><span data-stu-id="7e2c8-129">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="7e2c8-130">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="7e2c8-130">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="7e2c8-131">В разделе запрошенные профиля не существует.</span><span class="sxs-lookup"><span data-stu-id="7e2c8-131">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7e2c8-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="7e2c8-132">Remarks</span></span>

<span data-ttu-id="7e2c8-133">Метод **IMAPISession::OpenProfileSection** открывает раздела профиля или объект, который поддерживает интерфейс **IProfSect** .</span><span class="sxs-lookup"><span data-stu-id="7e2c8-133">The **IMAPISession::OpenProfileSection** method opens a profile section or object that supports the **IProfSect** interface.</span></span> <span data-ttu-id="7e2c8-134">Разделы профилей используются для чтения и записи данных в профиль сеанса.</span><span class="sxs-lookup"><span data-stu-id="7e2c8-134">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
<span data-ttu-id="7e2c8-135">Нельзя использовать **OpenProfileSection** для открытия разделов профиля, собственных поставщиков отдельные службы, если не указать MAPI_FORCE_ACCESS с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="7e2c8-135">You cannot use **OpenProfileSection** to open profile sections that individual service providers own unless you specify MAPI_FORCE_ACCESS in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7e2c8-136">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="7e2c8-136">Notes to callers</span></span>

<span data-ttu-id="7e2c8-137">Несколько клиентов могут открывать профиля с разрешением только для чтения, но только один клиент может открыть профиля с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="7e2c8-137">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="7e2c8-138">Если другой клиент имеет откройте попытаться открыть путем вызова **OpenProfileSection** с установленным флагом MAPI_MODIFY раздела профиля, вызов завершится с ошибкой, возвращая MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="7e2c8-138">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="7e2c8-139">Происходит сбой операции open только для чтения, если разделе открыт для записи.</span><span class="sxs-lookup"><span data-stu-id="7e2c8-139">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="7e2c8-140">Можно создать профиля путем вызова **OpenProfileSection** с флагом MAPI_MODIFY и несуществующий **MAPIUID** структуры с помощью параметра _lpUID_ .</span><span class="sxs-lookup"><span data-stu-id="7e2c8-140">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent **MAPIUID** structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="7e2c8-141">Не забудьте указать MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="7e2c8-141">Be sure that you specify MAPI_MODIFY.</span></span> <span data-ttu-id="7e2c8-142">Если необходимо задать _lpUID_ для указания на несуществующий **MAPIUID** и **OpenProfileSection** задано значение использовать режим по умолчанию доступа только для чтения, вызов завершится с ошибкой с MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="7e2c8-142">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7e2c8-143">См. также</span><span class="sxs-lookup"><span data-stu-id="7e2c8-143">See also</span></span>



[<span data-ttu-id="7e2c8-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7e2c8-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="7e2c8-145">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7e2c8-145">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="7e2c8-146">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="7e2c8-146">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="7e2c8-147">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="7e2c8-147">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

