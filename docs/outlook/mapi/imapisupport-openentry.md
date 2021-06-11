---
title: IMAPISupportOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenEntry
api_type:
- COM
ms.assetid: 84662230-6a25-4403-b87e-871427a40c6e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: cfbb799336aa1e75fa36e03e55d82c3af3409f10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409617"
---
# <a name="imapisupportopenentry"></a><span data-ttu-id="ac198-103">IMAPISupport::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="ac198-103">IMAPISupport::OpenEntry</span></span>

  
  
<span data-ttu-id="ac198-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac198-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac198-105">Открывает объект и возвращает указатель интерфейса для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="ac198-105">Opens an object and returns an interface pointer for further access.</span></span> 
  
```cpp
HRESULT OpenEntry(
ULONG cbEntryID,
LPENTRYID lpEntryID,
LPCIID lpInterface,
ULONG ulOpenFlags,
ULONG FAR * lpulObjType,
LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="ac198-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ac198-106">Parameters</span></span>

 <span data-ttu-id="ac198-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ac198-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="ac198-108">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="ac198-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ac198-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="ac198-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="ac198-110">[in] Указатель на идентификатор входа объекта для открытия.</span><span class="sxs-lookup"><span data-stu-id="ac198-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    
 <span data-ttu-id="ac198-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="ac198-111">_lpInterface_</span></span>
  
> <span data-ttu-id="ac198-112">[in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, используемый для доступа к объекту.</span><span class="sxs-lookup"><span data-stu-id="ac198-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="ac198-113">Передача NULL приводит к возвращению стандартного интерфейса объекта.</span><span class="sxs-lookup"><span data-stu-id="ac198-113">Passing NULL results in the object's standard interface being returned.</span></span> <span data-ttu-id="ac198-114">Например, если объект, который будет открыт, является сообщением, стандартным интерфейсом [является IMessage;](imessageimapiprop.md) для папок это [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="ac198-114">For example, if the object to be opened is a message, the standard interface is [IMessage](imessageimapiprop.md); for folders, it is [IMAPIFolder](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="ac198-115">Стандартными интерфейсами для объектов адресной книги являются [IDistList](idistlistimapicontainer.md) для списка рассылки и [IMailUser](imailuserimapiprop.md) для пользователя обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ac198-115">The standard interfaces for address book objects are [IDistList](idistlistimapicontainer.md) for a distribution list and [IMailUser](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="ac198-116">_ulOpenFlags_</span><span class="sxs-lookup"><span data-stu-id="ac198-116">_ulOpenFlags_</span></span>
  
> <span data-ttu-id="ac198-117">[in] Битмашка флагов, контролируемая тем, как открывается объект.</span><span class="sxs-lookup"><span data-stu-id="ac198-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="ac198-118">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="ac198-118">The following flags can be set:</span></span>
    
<span data-ttu-id="ac198-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="ac198-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="ac198-120">Запрашивает, чтобы объект был открыт с максимальным разрешением сети, разрешенным для вызываемой.</span><span class="sxs-lookup"><span data-stu-id="ac198-120">Requests that the object be opened with the maximum network permissions allowed for the caller.</span></span> <span data-ttu-id="ac198-121">Например, если у вызываемой вызываемой двери есть разрешение на чтение и записи, объект должен быть открыт в качестве чтения или записи; если у вызываемого имеется разрешение только для чтения, объект должен быть открыт только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ac198-121">For example, if the caller has read/write permission, the object should be opened as read/write; if the caller has read-only permission, the object should be opened as read-only.</span></span> 
    
<span data-ttu-id="ac198-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="ac198-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="ac198-123">Позволяет **OpenEntry** успешно возвращаться, возможно, до полного доступности объекта для вызываемой.</span><span class="sxs-lookup"><span data-stu-id="ac198-123">Allows **OpenEntry** to return successfully, possibly before the object is fully accessible to the caller.</span></span> <span data-ttu-id="ac198-124">Если объект не доступен, последующий вызов объекта может привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="ac198-124">If the object is not accessible, making a subsequent object call can result in an error.</span></span> 
    
<span data-ttu-id="ac198-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="ac198-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="ac198-126">Запросы на чтение и написание разрешений.</span><span class="sxs-lookup"><span data-stu-id="ac198-126">Requests read/write permission.</span></span> <span data-ttu-id="ac198-127">По умолчанию объекты открываются только для чтения, и звонителям не следует работать с предположением о том, что разрешение на чтение и записи было предоставлено.</span><span class="sxs-lookup"><span data-stu-id="ac198-127">By default, objects are opened as read-only, and callers should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="ac198-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="ac198-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="ac198-129">[вышел] Указатель на тип открываемого объекта.</span><span class="sxs-lookup"><span data-stu-id="ac198-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="ac198-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="ac198-130">_lppUnk_</span></span>
  
> <span data-ttu-id="ac198-131">[вышел] Указатель на указатель на открытый объект.</span><span class="sxs-lookup"><span data-stu-id="ac198-131">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ac198-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac198-132">Return value</span></span>

<span data-ttu-id="ac198-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac198-133">S_OK</span></span> 
  
> <span data-ttu-id="ac198-134">Объект был успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="ac198-134">The object was successfully opened.</span></span>
    
<span data-ttu-id="ac198-135">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="ac198-135">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="ac198-136">Была предпринята попытка изменить объект только для чтения, или была предпринята попытка доступа к объекту, для которого у пользователя недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="ac198-136">An attempt was made to modify a read-only object, or an attempt was made to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="ac198-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ac198-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ac198-138">В параметре  _lpEntryID_ не существует объекта, связанного с идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="ac198-138">There is not an object associated with the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="ac198-139">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ac198-139">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="ac198-140">Идентификатор записи, переданный в  _параметре lpEntryID,_ находится в неузнаваемом формате.</span><span class="sxs-lookup"><span data-stu-id="ac198-140">The entry identifier passed in the  _lpEntryID_ parameter is in an unrecognizable format.</span></span> <span data-ttu-id="ac198-141">Обычно это значение возвращается, если поставщик адресной книги, содержащий объект, не открыт.</span><span class="sxs-lookup"><span data-stu-id="ac198-141">This value is typically returned if the address book provider that contains the object is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ac198-142">Примечания</span><span class="sxs-lookup"><span data-stu-id="ac198-142">Remarks</span></span>

<span data-ttu-id="ac198-143">Метод **IMAPISupport::OpenEntry** реализован для всех объектов поддержки поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="ac198-143">The **IMAPISupport::OpenEntry** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="ac198-144">Поставщики услуг звонят **по вызову IMAPISupport::OpenEntry,** чтобы получить указатель в интерфейс, который можно использовать для доступа к определенному объекту.</span><span class="sxs-lookup"><span data-stu-id="ac198-144">Service providers call **IMAPISupport::OpenEntry** to retrieve a pointer to an interface that can be used to access a particular object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ac198-145">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="ac198-145">Notes to callers</span></span>

<span data-ttu-id="ac198-146">Вызов **IMAPISupport::OpenEntry** только в том случае, если вы не знаете, какой объект вы открываете.</span><span class="sxs-lookup"><span data-stu-id="ac198-146">Call **IMAPISupport::OpenEntry** only when you do not know what kind of object you are opening.</span></span> <span data-ttu-id="ac198-147">Если вы знаете, что открываете папку или сообщение, вместо этого позвоните [в IMsgStore::OpenEntry.](imsgstore-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="ac198-147">If you know you are opening a folder or a message, call [IMsgStore::OpenEntry](imsgstore-openentry.md) instead.</span></span> <span data-ttu-id="ac198-148">Если вы знаете, что открываете контейнер адресной книги, пользователя обмена сообщениями или список рассылки, позвоните [в IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="ac198-148">If you know you are opening an address book container, a messaging user, or a distribution list, call [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="ac198-149">Эти более конкретные методы быстрее, чем **IMAPISupport::OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="ac198-149">These more specific methods are faster than **IMAPISupport::OpenEntry**.</span></span> 
  
 <span data-ttu-id="ac198-150">**IMAPISupport::OpenEntry** открывает все объекты только для чтения, если только вы не установите флаг MAPI_MODIFY или MAPI_BEST_ACCESS в параметре  _ulFlags_ и ваши разрешения будут достаточными.</span><span class="sxs-lookup"><span data-stu-id="ac198-150">**IMAPISupport::OpenEntry** opens all objects as read-only, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter and your permissions are sufficient.</span></span> <span data-ttu-id="ac198-151">Установка одного из этих флагов не гарантирует определенный тип доступа; выданные разрешения зависят от уровня доступа, объекта и поставщика услуг, который владеет объектом.</span><span class="sxs-lookup"><span data-stu-id="ac198-151">Setting one of these flags does not guarantee a particular type of access; the permissions that you are granted depend on your access level, the object, and the service provider that owns the object.</span></span> <span data-ttu-id="ac198-152">Чтобы определить уровень доступа открываемого  объекта, PR_ACCESS_LEVEL[(PidTagAccessLevel).](pidtagaccesslevel-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="ac198-152">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="ac198-153">Проверьте значение, возвращаемого в  _параметре lpulObjType,_ чтобы определить, что возвращенный тип объекта является ожидаемым.</span><span class="sxs-lookup"><span data-stu-id="ac198-153">Check the value returned in the  _lpulObjType_ parameter to determine that the object type returned is what you expected.</span></span> <span data-ttu-id="ac198-154">Если тип объекта является ожидаемым, отведите указатель из параметра  _lppUnk_ в указатель соответствующего типа.</span><span class="sxs-lookup"><span data-stu-id="ac198-154">If the object type is as expected, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="ac198-155">Например, если вы открываете папку, введите  _lppUnk_ в указатель типа LPMAPIFOLDER.</span><span class="sxs-lookup"><span data-stu-id="ac198-155">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type LPMAPIFOLDER.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ac198-156">См. также</span><span class="sxs-lookup"><span data-stu-id="ac198-156">See also</span></span>



[<span data-ttu-id="ac198-157">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ac198-157">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

