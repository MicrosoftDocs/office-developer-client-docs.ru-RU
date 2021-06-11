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
ms.openlocfilehash: 70f61ef553350f08eed96c1ee4e9ab790359d1fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409232"
---
# <a name="iablogonopenentry"></a><span data-ttu-id="33d27-103">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="33d27-103">IABLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="33d27-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33d27-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33d27-105">Открывает контейнер, пользователя обмена сообщениями или список рассылки и возвращает указатель в реализацию интерфейса, чтобы обеспечить дополнительный доступ.</span><span class="sxs-lookup"><span data-stu-id="33d27-105">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="33d27-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="33d27-106">Parameters</span></span>

 <span data-ttu-id="33d27-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="33d27-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="33d27-108">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="33d27-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="33d27-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="33d27-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="33d27-110">[in] Указатель на идентификатор входа для открываемого контейнера, пользователя обмена сообщениями или списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="33d27-110">[in] A pointer to the entry identifier of the container, messaging user, or distribution list to open.</span></span>
    
 <span data-ttu-id="33d27-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="33d27-111">_lpInterface_</span></span>
  
> <span data-ttu-id="33d27-112">[in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, используемый для доступа к открытому объекту.</span><span class="sxs-lookup"><span data-stu-id="33d27-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the open object.</span></span> <span data-ttu-id="33d27-113">Передача NULL возвращает идентификатор для стандартного интерфейса объекта.</span><span class="sxs-lookup"><span data-stu-id="33d27-113">Passing NULL returns the identifier for the object's standard interface.</span></span> <span data-ttu-id="33d27-114">Для контейнеров стандартным интерфейсом [является IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="33d27-114">For containers, the standard interface is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="33d27-115">Стандартными интерфейсами для объектов адресной книги являются [IDistList: IMAPIContainer](idistlistimapicontainer.md) для списка рассылки и [IMailUser: IMAPIProp](imailuserimapiprop.md) для пользователя обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="33d27-115">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="33d27-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="33d27-116">_ulFlags_</span></span>
  
> <span data-ttu-id="33d27-117">[in] Битмашка флагов, контролируемая тем, как открывается объект.</span><span class="sxs-lookup"><span data-stu-id="33d27-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="33d27-118">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="33d27-118">The following flags can be set:</span></span>
    
<span data-ttu-id="33d27-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="33d27-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="33d27-120">Запрашивает, чтобы объект был открыт с максимальным разрешением сети, разрешенным для пользователя, и максимальным доступом к приложению клиента.</span><span class="sxs-lookup"><span data-stu-id="33d27-120">Requests that the object be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="33d27-121">Например, если у клиента есть разрешение на чтение и записи, объект должен быть открыт с разрешения на чтение и записи; если у клиента есть разрешение только для чтения, объект должен быть открыт только для чтения.</span><span class="sxs-lookup"><span data-stu-id="33d27-121">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only permission, the object should be opened with read-only permission.</span></span>
    
<span data-ttu-id="33d27-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="33d27-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="33d27-123">Позволяет **методу OpenEntry** успешно возвращаться, возможно, до полного доступа к объекту клиент-вызов.</span><span class="sxs-lookup"><span data-stu-id="33d27-123">Allows the **OpenEntry** method to return successfully, possibly before the calling client has fully accessed the object.</span></span> <span data-ttu-id="33d27-124">Если объект не имеет доступа, при последующем вызове объекта может быть допущена ошибка.</span><span class="sxs-lookup"><span data-stu-id="33d27-124">If the object is not accessed, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="33d27-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="33d27-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="33d27-126">Запросы на чтение и написание разрешений.</span><span class="sxs-lookup"><span data-stu-id="33d27-126">Requests read/write permission.</span></span> <span data-ttu-id="33d27-127">По умолчанию объекты открываются с доступом только для чтения, и клиенты не должны предполагать, что разрешение на чтение и записи было предоставлено.</span><span class="sxs-lookup"><span data-stu-id="33d27-127">By default, objects are opened with read-only access, and clients should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="33d27-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="33d27-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="33d27-129">[вышел] Указатель на тип открываемого объекта.</span><span class="sxs-lookup"><span data-stu-id="33d27-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="33d27-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="33d27-130">_lppUnk_</span></span>
  
> <span data-ttu-id="33d27-131">[вышел] Указатель на указатель на открытый объект.</span><span class="sxs-lookup"><span data-stu-id="33d27-131">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="33d27-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="33d27-132">Remarks</span></span>

<span data-ttu-id="33d27-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="33d27-133">S_OK</span></span> 
  
> <span data-ttu-id="33d27-134">Объект был успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="33d27-134">The object was successfully opened.</span></span>
    
<span data-ttu-id="33d27-135">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="33d27-135">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="33d27-136">Либо у пользователя недостаточно разрешений на открытие объекта, либо была предпринята попытка открыть объект только для чтения с разрешения на чтение и написание.</span><span class="sxs-lookup"><span data-stu-id="33d27-136">Either the user has insufficient permissions to open the object, or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="33d27-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="33d27-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="33d27-138">Идентификатор записи, указанный  _lpEntryID,_ не представляет объекта.</span><span class="sxs-lookup"><span data-stu-id="33d27-138">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="33d27-139">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="33d27-139">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="33d27-140">Идентификатор записи в параметре  _lpEntryID_ не имеет формата, распознаемого поставщиком адресной книги.</span><span class="sxs-lookup"><span data-stu-id="33d27-140">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="33d27-141">Примечания</span><span class="sxs-lookup"><span data-stu-id="33d27-141">Remarks</span></span>

<span data-ttu-id="33d27-142">MAPI вызывает метод **OpenEntry** для открытия контейнера, пользователя обмена сообщениями или списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="33d27-142">MAPI calls the **OpenEntry** method to open a container, messaging user, or distribution list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="33d27-143">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="33d27-143">Notes to implementers</span></span>

<span data-ttu-id="33d27-144">Прежде чем MAPI вызывает метод **OpenEntry,** он определяет, что идентификатор входа в  _параметре lpEntryID_ принадлежит вам, а не другому поставщику.</span><span class="sxs-lookup"><span data-stu-id="33d27-144">Before MAPI calls your **OpenEntry** method, it determines that the entry identifier in the  _lpEntryID_ parameter belongs to you and not to another provider.</span></span> <span data-ttu-id="33d27-145">MAPI делает это путем совпадения структуры [MAPIUID](mapiuid.md) в идентификаторе входа с **MAPIUID,** который вы зарегистрировали, позвонив [методу IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) при запуске.</span><span class="sxs-lookup"><span data-stu-id="33d27-145">MAPI does this by matching the [MAPIUID](mapiuid.md) structure in the entry identifier with the **MAPIUID** that you registered by calling the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method at startup.</span></span> 
  
<span data-ttu-id="33d27-146">Откройте объект только для чтения, если MAPI_MODIFY или MAPI_BEST_ACCESS в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="33d27-146">Open the object as read-only, unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="33d27-147">Если вы не разрешаете изменение запрашиваемой цели, не открывайте объект вообще и возвращайте MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="33d27-147">If you do not allow modification for the requested object, do not open the object at all and return MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="33d27-148">Если MAPI передает NULL для  _lpEntryID,_ откройте корневой контейнер в иерархии контейнеров.</span><span class="sxs-lookup"><span data-stu-id="33d27-148">If MAPI passes NULL for  _lpEntryID_, open the root container in your container hierarchy.</span></span>
  
<span data-ttu-id="33d27-149">Объект, который требуется открыть, может быть объектом, скопированным у другого поставщика.</span><span class="sxs-lookup"><span data-stu-id="33d27-149">The object that you are being asked to open might be an object copied from another provider.</span></span> <span data-ttu-id="33d27-150">В этом случае он будет поддерживать свойство **PR_TEMPLATEID** [(PidTagTemplateid).](pidtagtemplateid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="33d27-150">In this case, it will support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> <span data-ttu-id="33d27-151">Если объект поддерживает это свойство, позвоните по методу [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) для привязки  к коду для этой записи в иностранном поставщике, PR_TEMPLATEID в _параметре lpTemplateID_ и 0 в _параметре ulTemplateFlags._</span><span class="sxs-lookup"><span data-stu-id="33d27-151">If the object does support this property, call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method to bind to code for this entry in the foreign provider, passing **PR_TEMPLATEID** in the  _lpTemplateID_ parameter and 0 in the  _ulTemplateFlags_ parameter.</span></span> <span data-ttu-id="33d27-152">**IMAPISupport::OpenTemplateID** передает эти сведения иностранному поставщику по вызову метода [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) иностранного поставщика.</span><span class="sxs-lookup"><span data-stu-id="33d27-152">**IMAPISupport::OpenTemplateID** passes this information to the foreign provider in a call to the foreign provider's [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) method.</span></span> <span data-ttu-id="33d27-153">Если **IMAPISupport::OpenTemplateID** вызывает ошибку, как правило, потому, что иностранный поставщик недоступен или не включен в профиль, попробуйте продолжить, обрабатывая неограниченную запись только для чтения.</span><span class="sxs-lookup"><span data-stu-id="33d27-153">If **IMAPISupport::OpenTemplateID** raises an error, usually because the foreign provider is unavailable or not included in the profile, try to continue by treating the unbound entry as read-only.</span></span> <span data-ttu-id="33d27-154">Дополнительные сведения об открытии записей иностранных адресных книг см. в [статьях Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span><span class="sxs-lookup"><span data-stu-id="33d27-154">For more information about opening foreign address book entries, see [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="33d27-155">См. также</span><span class="sxs-lookup"><span data-stu-id="33d27-155">See also</span></span>



[<span data-ttu-id="33d27-156">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="33d27-156">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

