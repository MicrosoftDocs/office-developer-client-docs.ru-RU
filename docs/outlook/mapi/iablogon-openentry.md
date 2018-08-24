---
title: IABLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenEntry
api_type:
- COM
ms.assetid: 1cfb82f7-5215-4faa-af25-5b1da7e31209
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: bf6386ae3a7d835c8748e332235d8737c7a502e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589471"
---
# <a name="iablogonopenentry"></a><span data-ttu-id="1203b-103">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="1203b-103">IABLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="1203b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1203b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1203b-105">Открывает контейнер, системы обмена сообщениями пользователя или список рассылки и возвращает указатель на реализацию интерфейса для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="1203b-105">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="1203b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1203b-106">Parameters</span></span>

 <span data-ttu-id="1203b-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="1203b-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="1203b-108">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="1203b-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="1203b-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="1203b-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="1203b-110">[in] Указатель на идентификатор записи контейнера, системы обмена сообщениями пользователя или список рассылки, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="1203b-110">[in] A pointer to the entry identifier of the container, messaging user, or distribution list to open.</span></span>
    
 <span data-ttu-id="1203b-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="1203b-111">_lpInterface_</span></span>
  
> <span data-ttu-id="1203b-112">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к объекту open.</span><span class="sxs-lookup"><span data-stu-id="1203b-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the open object.</span></span> <span data-ttu-id="1203b-113">Передача NULL возвращает идентификатор на стандартный интерфейс объекта.</span><span class="sxs-lookup"><span data-stu-id="1203b-113">Passing NULL returns the identifier for the object's standard interface.</span></span> <span data-ttu-id="1203b-114">Для контейнеров, — это стандартный интерфейс [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="1203b-114">For containers, the standard interface is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="1203b-115">Стандартные интерфейсы для объектов адресной книги [IDistList: IMAPIContainer](idistlistimapicontainer.md) для списка рассылки и [IMailUser: IMAPIProp](imailuserimapiprop.md) для обмена сообщениями пользователя.</span><span class="sxs-lookup"><span data-stu-id="1203b-115">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="1203b-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1203b-116">_ulFlags_</span></span>
  
> <span data-ttu-id="1203b-117">[in] Битовая маска флаги, который определяет способ открытия объекта.</span><span class="sxs-lookup"><span data-stu-id="1203b-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="1203b-118">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="1203b-118">The following flags can be set:</span></span>
    
<span data-ttu-id="1203b-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="1203b-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="1203b-120">Запрашивает открыть объект с разрешениями максимальное сети, разрешенных для пользователя и приложения максимальное клиентского доступа.</span><span class="sxs-lookup"><span data-stu-id="1203b-120">Requests that the object be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="1203b-121">Например если клиент имеет разрешение на чтение и запись, объект должен быть открыт получившие разрешение на чтение и запись; Если клиент имеет разрешение на чтение, объект должен быть открыт с разрешением только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1203b-121">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only permission, the object should be opened with read-only permission.</span></span>
    
<span data-ttu-id="1203b-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="1203b-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="1203b-123">Разрешает метод **OpenEntry** для возврата успешно, возможно вызывающего клиента полностью для доступа к объекту.</span><span class="sxs-lookup"><span data-stu-id="1203b-123">Allows the **OpenEntry** method to return successfully, possibly before the calling client has fully accessed the object.</span></span> <span data-ttu-id="1203b-124">Если объект не осуществляется, вызов последующих объектов может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="1203b-124">If the object is not accessed, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="1203b-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="1203b-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="1203b-126">Запросы на разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="1203b-126">Requests read/write permission.</span></span> <span data-ttu-id="1203b-127">По умолчанию объекты открываются с доступом только для чтения, и клиенты не должны предполагать, что предоставлены разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="1203b-127">By default, objects are opened with read-only access, and clients should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="1203b-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="1203b-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="1203b-129">[out] Указатель на тип объекта открыт.</span><span class="sxs-lookup"><span data-stu-id="1203b-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="1203b-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="1203b-130">_lppUnk_</span></span>
  
> <span data-ttu-id="1203b-131">[out] Указатель на указатель на объект открыт.</span><span class="sxs-lookup"><span data-stu-id="1203b-131">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1203b-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="1203b-132">Remarks</span></span>

<span data-ttu-id="1203b-133">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="1203b-133">S_OK</span></span> 
  
> <span data-ttu-id="1203b-134">Объект был успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="1203b-134">The object was successfully opened.</span></span>
    
<span data-ttu-id="1203b-135">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="1203b-135">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="1203b-136">Либо пользователь не имеет разрешений на открытие объекта, либо попытка открыть объект только для чтения с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="1203b-136">Either the user has insufficient permissions to open the object, or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="1203b-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="1203b-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="1203b-138">Идентификатор записи, указанного идентификатором _lpEntryID_ не представляет объект.</span><span class="sxs-lookup"><span data-stu-id="1203b-138">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="1203b-139">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1203b-139">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="1203b-140">Идентификатор записи в параметре _lpEntryID_ не формата, распознаваемых поставщик адресной книги.</span><span class="sxs-lookup"><span data-stu-id="1203b-140">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1203b-141">Замечания</span><span class="sxs-lookup"><span data-stu-id="1203b-141">Remarks</span></span>

<span data-ttu-id="1203b-142">MAPI вызывает метод **OpenEntry** , чтобы открыть container, системы обмена сообщениями пользователя или список рассылки.</span><span class="sxs-lookup"><span data-stu-id="1203b-142">MAPI calls the **OpenEntry** method to open a container, messaging user, or distribution list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1203b-143">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="1203b-143">Notes to implementers</span></span>

<span data-ttu-id="1203b-144">Перед MAPI вызывает метод **OpenEntry** , он определяет, что идентификатор записи в параметре _lpEntryID_ относится к вам, а не к другой поставщик.</span><span class="sxs-lookup"><span data-stu-id="1203b-144">Before MAPI calls your **OpenEntry** method, it determines that the entry identifier in the  _lpEntryID_ parameter belongs to you and not to another provider.</span></span> <span data-ttu-id="1203b-145">MAPI осуществляется путем сопоставления структуры [MAPIUID](mapiuid.md) в идентификатор записи с **MAPIUID** , которую вы зарегистрировали путем вызова метода [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) при запуске системы.</span><span class="sxs-lookup"><span data-stu-id="1203b-145">MAPI does this by matching the [MAPIUID](mapiuid.md) structure in the entry identifier with the **MAPIUID** that you registered by calling the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method at startup.</span></span> 
  
<span data-ttu-id="1203b-146">Откройте объект с доступом только для чтения, пока флаг MAPI_MODIFY или MAPI_BEST_ACCESS будет выполнен с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="1203b-146">Open the object as read-only, unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="1203b-147">Если не разрешать изменения для запрошенного объекта, не открывается объект и вернуться MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="1203b-147">If you do not allow modification for the requested object, do not open the object at all and return MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="1203b-148">Если MAPI передает значение NULL для _lpEntryID_, откройте корневой контейнер в иерархии контейнеров.</span><span class="sxs-lookup"><span data-stu-id="1203b-148">If MAPI passes NULL for  _lpEntryID_, open the root container in your container hierarchy.</span></span>
  
<span data-ttu-id="1203b-149">Объект, который требуется открыть возможно объекта, скопированного из другого поставщика.</span><span class="sxs-lookup"><span data-stu-id="1203b-149">The object that you are being asked to open might be an object copied from another provider.</span></span> <span data-ttu-id="1203b-150">В этом случае он будет поддерживать свойство **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1203b-150">In this case, it will support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> <span data-ttu-id="1203b-151">Если объект поддерживает это свойство, вызовите метод [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) для привязки к коду для этой записи внешнего поставщика, передав в параметр _lpTemplateID_ и 0 в _ulTemplateFlags **PR_TEMPLATEID** _параметр.</span><span class="sxs-lookup"><span data-stu-id="1203b-151">If the object does support this property, call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method to bind to code for this entry in the foreign provider, passing **PR_TEMPLATEID** in the  _lpTemplateID_ parameter and 0 in the  _ulTemplateFlags_ parameter.</span></span> <span data-ttu-id="1203b-152">**IMAPISupport::OpenTemplateID** передает эти сведения внешнего поставщика в вызов метода [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) внешнего поставщика.</span><span class="sxs-lookup"><span data-stu-id="1203b-152">**IMAPISupport::OpenTemplateID** passes this information to the foreign provider in a call to the foreign provider's [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) method.</span></span> <span data-ttu-id="1203b-153">Если **IMAPISupport::OpenTemplateID** вызывает ошибку, обычно так как внешнего поставщика, недоступен или не включены в профиле, попробуйте для продолжения по обработке свободной записи с доступом только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1203b-153">If **IMAPISupport::OpenTemplateID** raises an error, usually because the foreign provider is unavailable or not included in the profile, try to continue by treating the unbound entry as read-only.</span></span> <span data-ttu-id="1203b-154">Дополнительные сведения об открытии внешнего адресной книги можно [действовать как поставщик адресной книги](acting-as-a-host-address-book-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1203b-154">For more information about opening foreign address book entries, see [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1203b-155">См. также</span><span class="sxs-lookup"><span data-stu-id="1203b-155">See also</span></span>



[<span data-ttu-id="1203b-156">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1203b-156">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

