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
# <a name="imapisupportopenentry"></a><span data-ttu-id="4f1a3-103">IMAPISupport::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="4f1a3-103">IMAPISupport::OpenEntry</span></span>

  
  
<span data-ttu-id="4f1a3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f1a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f1a3-105">Открывает объект и возвращает указатель интерфейса для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="4f1a3-105">Opens an object and returns an interface pointer for further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="4f1a3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f1a3-106">Parameters</span></span>

 <span data-ttu-id="4f1a3-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="4f1a3-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="4f1a3-108">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="4f1a3-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="4f1a3-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="4f1a3-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="4f1a3-110">[in] Указатель на идентификатор записи объекта, который необходимо открыть.</span><span class="sxs-lookup"><span data-stu-id="4f1a3-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    
 <span data-ttu-id="4f1a3-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="4f1a3-111">_lpInterface_</span></span>
  
> <span data-ttu-id="4f1a3-112">[in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, который будет использоваться для доступа к объекту.</span><span class="sxs-lookup"><span data-stu-id="4f1a3-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="4f1a3-113">Передача NULL приводит к возвращению стандартного интерфейса объекта.</span><span class="sxs-lookup"><span data-stu-id="4f1a3-113">Passing NULL results in the object's standard interface being returned.</span></span> <span data-ttu-id="4f1a3-114">Например, если объект, который необходимо открыть, является сообщением, стандартным интерфейсом будет [IMessage;](imessageimapiprop.md) для папок это [IMAPIFolder.](imapifolderimapicontainer.md)</span><span class="sxs-lookup"><span data-stu-id="4f1a3-114">For example, if the object to be opened is a message, the standard interface is [IMessage](imessageimapiprop.md); for folders, it is [IMAPIFolder](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="4f1a3-115">Стандартными интерфейсами для объектов адресной книги являются [IDistList](idistlistimapicontainer.md) для списка рассылки и [IMailUser](imailuserimapiprop.md) для пользователя обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="4f1a3-115">The standard interfaces for address book objects are [IDistList](idistlistimapicontainer.md) for a distribution list and [IMailUser](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="4f1a3-116">_ulOpenFlags_</span><span class="sxs-lookup"><span data-stu-id="4f1a3-116">_ulOpenFlags_</span></span>
  
> <span data-ttu-id="4f1a3-117">[in] Битоваяmas флагов, которая управляет открытием объекта.</span><span class="sxs-lookup"><span data-stu-id="4f1a3-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="4f1a3-118">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="4f1a3-118">The following flags can be set:</span></span>
    
<span data-ttu-id="4f1a3-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="4f1a3-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="4f1a3-120">Запрашивает открытие объекта с максимальным доступом к сети, разрешенным для вызываемой.</span><span class="sxs-lookup"><span data-stu-id="4f1a3-120">Requests that the object be opened with the maximum network permissions allowed for the caller.</span></span> <span data-ttu-id="4f1a3-121">Например, если у вызываемой есть разрешение на чтение и записи, объект должен быть открыт как чтение и записи; Если у вызываемого объекта есть разрешение только на чтение, объект должен быть открыт как только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4f1a3-121">For example, if the caller has read/write permission, the object should be opened as read/write; if the caller has read-only permission, the object should be opened as read-only.</span></span> 
    
<span data-ttu-id="4f1a3-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="4f1a3-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="4f1a3-123">Позволяет **OpenEntry** успешно возвращаться, возможно, до того, как объект будет полностью доступен вызываемой.</span><span class="sxs-lookup"><span data-stu-id="4f1a3-123">Allows **OpenEntry** to return successfully, possibly before the object is fully accessible to the caller.</span></span> <span data-ttu-id="4f1a3-124">Если объект не доступен, последующий вызов объекта может привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="4f1a3-124">If the object is not accessible, making a subsequent object call can result in an error.</span></span> 
    
<span data-ttu-id="4f1a3-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="4f1a3-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="4f1a3-126">Запрашивает разрешение на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="4f1a3-126">Requests read/write permission.</span></span> <span data-ttu-id="4f1a3-127">По умолчанию объекты открываются как объекты только для чтения, и вызывающим не следует работать при предположении, что разрешение на чтение и записи предоставлено.</span><span class="sxs-lookup"><span data-stu-id="4f1a3-127">By default, objects are opened as read-only, and callers should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="4f1a3-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="4f1a3-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="4f1a3-129">[out] Указатель на тип открытого объекта.</span><span class="sxs-lookup"><span data-stu-id="4f1a3-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="4f1a3-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="4f1a3-130">_lppUnk_</span></span>
  
> <span data-ttu-id="4f1a3-131">[out] Указатель на указатель на открытый объект.</span><span class="sxs-lookup"><span data-stu-id="4f1a3-131">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4f1a3-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4f1a3-132">Return value</span></span>

<span data-ttu-id="4f1a3-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="4f1a3-133">S_OK</span></span> 
  
> <span data-ttu-id="4f1a3-134">Объект успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="4f1a3-134">The object was successfully opened.</span></span>
    
<span data-ttu-id="4f1a3-135">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="4f1a3-135">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="4f1a3-136">Предпринята попытка изменить объект, доступный только для чтения, или попытка доступа к объекту, у которого у пользователя недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="4f1a3-136">An attempt was made to modify a read-only object, or an attempt was made to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="4f1a3-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="4f1a3-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="4f1a3-138">Объект, связанный с идентификатором записи, переданным в  _параметре lpEntryID, не_ существует.</span><span class="sxs-lookup"><span data-stu-id="4f1a3-138">There is not an object associated with the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="4f1a3-139">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4f1a3-139">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="4f1a3-140">Идентификатор записи, переданный в  _параметре lpEntryID,_ имеет неизвестный формат.</span><span class="sxs-lookup"><span data-stu-id="4f1a3-140">The entry identifier passed in the  _lpEntryID_ parameter is in an unrecognizable format.</span></span> <span data-ttu-id="4f1a3-141">Обычно это значение возвращается, если поставщик адресной книги, содержащий объект, не открыт.</span><span class="sxs-lookup"><span data-stu-id="4f1a3-141">This value is typically returned if the address book provider that contains the object is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4f1a3-142">Примечания</span><span class="sxs-lookup"><span data-stu-id="4f1a3-142">Remarks</span></span>

<span data-ttu-id="4f1a3-143">Метод **IMAPISupport::OpenEntry** реализован для всех объектов поддержки поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="4f1a3-143">The **IMAPISupport::OpenEntry** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="4f1a3-144">Поставщики услуг **звонят IMAPISupport::OpenEntry,** чтобы получить указатель на интерфейс, который можно использовать для доступа к определенному объекту.</span><span class="sxs-lookup"><span data-stu-id="4f1a3-144">Service providers call **IMAPISupport::OpenEntry** to retrieve a pointer to an interface that can be used to access a particular object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4f1a3-145">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="4f1a3-145">Notes to callers</span></span>

<span data-ttu-id="4f1a3-146">Вызовите **IMAPISupport::OpenEntry** только в том случае, если вы не знаете, какой объект вы открываете.</span><span class="sxs-lookup"><span data-stu-id="4f1a3-146">Call **IMAPISupport::OpenEntry** only when you do not know what kind of object you are opening.</span></span> <span data-ttu-id="4f1a3-147">Если вы знаете, что открываете папку или сообщение, вызовите [IMsgStore::OpenEntry.](imsgstore-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="4f1a3-147">If you know you are opening a folder or a message, call [IMsgStore::OpenEntry](imsgstore-openentry.md) instead.</span></span> <span data-ttu-id="4f1a3-148">Если вы знаете, что открываете контейнер адресной книги, пользователя обмена сообщениями или список рассылки, вызовите [IAddrBook::OpenEntry.](iaddrbook-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="4f1a3-148">If you know you are opening an address book container, a messaging user, or a distribution list, call [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="4f1a3-149">Эти более конкретные методы **быстрее, чем IMAPISupport::OpenEntry.**</span><span class="sxs-lookup"><span data-stu-id="4f1a3-149">These more specific methods are faster than **IMAPISupport::OpenEntry**.</span></span> 
  
 <span data-ttu-id="4f1a3-150">**IMAPISupport::OpenEntry** открывает все объекты только для чтения, если вы не установите флаг MAPI_MODIFY или MAPI_BEST_ACCESS в параметре  _ulFlags_ и ваши разрешения будут достаточными.</span><span class="sxs-lookup"><span data-stu-id="4f1a3-150">**IMAPISupport::OpenEntry** opens all objects as read-only, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter and your permissions are sufficient.</span></span> <span data-ttu-id="4f1a3-151">Установка одного из этих флагов не гарантирует определенный тип доступа; предоставленные разрешения зависят от уровня доступа, объекта и поставщика услуг, который является владельцем объекта.</span><span class="sxs-lookup"><span data-stu-id="4f1a3-151">Setting one of these flags does not guarantee a particular type of access; the permissions that you are granted depend on your access level, the object, and the service provider that owns the object.</span></span> <span data-ttu-id="4f1a3-152">Чтобы определить уровень доступа открытого объекта, извлекаете **его PR_ACCESS_LEVEL** ([PidTagAccessLevel).](pidtagaccesslevel-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="4f1a3-152">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="4f1a3-153">Проверьте значение, возвращаемого в  _параметре lpulObjType,_ чтобы определить, что возвращаемого типа объекта является ожидаемым.</span><span class="sxs-lookup"><span data-stu-id="4f1a3-153">Check the value returned in the  _lpulObjType_ parameter to determine that the object type returned is what you expected.</span></span> <span data-ttu-id="4f1a3-154">Если тип объекта является ожидаемым, приведите указатель из параметра  _lppUnk_ к указателю соответствующего типа.</span><span class="sxs-lookup"><span data-stu-id="4f1a3-154">If the object type is as expected, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="4f1a3-155">Например, если вы открываете папку, приведите  _lppUnk_ к указателю типа LPMAPIFOLDER.</span><span class="sxs-lookup"><span data-stu-id="4f1a3-155">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type LPMAPIFOLDER.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4f1a3-156">См. также</span><span class="sxs-lookup"><span data-stu-id="4f1a3-156">See also</span></span>



[<span data-ttu-id="4f1a3-157">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4f1a3-157">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

