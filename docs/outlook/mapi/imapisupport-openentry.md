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
ms.openlocfilehash: 8b122c98715bd2f6916fe6302fc0b7a01d2cc936
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584613"
---
# <a name="imapisupportopenentry"></a><span data-ttu-id="c488e-103">IMAPISupport::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="c488e-103">IMAPISupport::OpenEntry</span></span>

  
  
<span data-ttu-id="c488e-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c488e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c488e-105">Открывает объект и возвращает указатель интерфейса для дальнейшей доступа.</span><span class="sxs-lookup"><span data-stu-id="c488e-105">Opens an object and returns an interface pointer for further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="c488e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c488e-106">Parameters</span></span>

 <span data-ttu-id="c488e-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="c488e-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="c488e-108">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="c488e-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="c488e-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="c488e-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="c488e-110">[in] Указатель на запись идентификатор объекта для открытия.</span><span class="sxs-lookup"><span data-stu-id="c488e-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    
 <span data-ttu-id="c488e-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="c488e-111">_lpInterface_</span></span>
  
> <span data-ttu-id="c488e-112">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к объекту.</span><span class="sxs-lookup"><span data-stu-id="c488e-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="c488e-113">В стандартный интерфейс объекта, возвращаемых результатов передаче значения NULL.</span><span class="sxs-lookup"><span data-stu-id="c488e-113">Passing NULL results in the object's standard interface being returned.</span></span> <span data-ttu-id="c488e-114">Например если к объекту, чтобы открыть сообщение, стандартный интерфейс будет [IMessage](imessageimapiprop.md); для папок это [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="c488e-114">For example, if the object to be opened is a message, the standard interface is [IMessage](imessageimapiprop.md); for folders, it is [IMAPIFolder](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="c488e-115">Стандартные интерфейсы для объектов адресной книги — [IDistList](idistlistimapicontainer.md) для списка рассылки, а также [IMailUser](imailuserimapiprop.md) для обмена сообщениями пользователя.</span><span class="sxs-lookup"><span data-stu-id="c488e-115">The standard interfaces for address book objects are [IDistList](idistlistimapicontainer.md) for a distribution list and [IMailUser](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="c488e-116">_ulOpenFlags_</span><span class="sxs-lookup"><span data-stu-id="c488e-116">_ulOpenFlags_</span></span>
  
> <span data-ttu-id="c488e-117">[in] Битовая маска флаги, который определяет способ открытия объекта.</span><span class="sxs-lookup"><span data-stu-id="c488e-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="c488e-118">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="c488e-118">The following flags can be set:</span></span>
    
<span data-ttu-id="c488e-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="c488e-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="c488e-120">Запрашивает открыть объект с разрешениями максимальное сети, разрешенных для вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="c488e-120">Requests that the object be opened with the maximum network permissions allowed for the caller.</span></span> <span data-ttu-id="c488e-121">Например если вызывающий объект имеет разрешение на чтение/запись, объект должен быть открыт для чтения и записи; Если вызывающий объект имеет разрешение только на чтение, объект должен быть открыт только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c488e-121">For example, if the caller has read/write permission, the object should be opened as read/write; if the caller has read-only permission, the object should be opened as read-only.</span></span> 
    
<span data-ttu-id="c488e-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="c488e-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="c488e-123">Позволяет **OpenEntry** для возврата успешно, возможно перед объект является полностью доступен для вызова.</span><span class="sxs-lookup"><span data-stu-id="c488e-123">Allows **OpenEntry** to return successfully, possibly before the object is fully accessible to the caller.</span></span> <span data-ttu-id="c488e-124">Если объект недоступен, вызов последующих объектов может привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="c488e-124">If the object is not accessible, making a subsequent object call can result in an error.</span></span> 
    
<span data-ttu-id="c488e-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="c488e-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="c488e-126">Запросы на разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="c488e-126">Requests read/write permission.</span></span> <span data-ttu-id="c488e-127">По умолчанию объекты открываются только для чтения и звонящие не должны работать предполагается, что что назначено разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="c488e-127">By default, objects are opened as read-only, and callers should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="c488e-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="c488e-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="c488e-129">[out] Указатель на тип объекта открыт.</span><span class="sxs-lookup"><span data-stu-id="c488e-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="c488e-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="c488e-130">_lppUnk_</span></span>
  
> <span data-ttu-id="c488e-131">[out] Указатель на указатель на объект открыт.</span><span class="sxs-lookup"><span data-stu-id="c488e-131">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c488e-132">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="c488e-132">Return value</span></span>

<span data-ttu-id="c488e-133">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="c488e-133">S_OK</span></span> 
  
> <span data-ttu-id="c488e-134">Объект был успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="c488e-134">The object was successfully opened.</span></span>
    
<span data-ttu-id="c488e-135">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="c488e-135">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="c488e-136">Попытка изменить объект только для чтения или предпринята попытка получить доступ к объекту, для которого пользователь имеет недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="c488e-136">An attempt was made to modify a read-only object, or an attempt was made to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="c488e-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c488e-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="c488e-138">Объект, связанный с идентификатором записи, переданной в параметре _lpEntryID_ не существует.</span><span class="sxs-lookup"><span data-stu-id="c488e-138">There is not an object associated with the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="c488e-139">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c488e-139">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="c488e-140">Идентификатор записи, переданной в параметре _lpEntryID_ имеет неопознанный формат.</span><span class="sxs-lookup"><span data-stu-id="c488e-140">The entry identifier passed in the  _lpEntryID_ parameter is in an unrecognizable format.</span></span> <span data-ttu-id="c488e-141">Это значение возвращается как правило, если поставщик адресной книги, содержащее объект не открыт.</span><span class="sxs-lookup"><span data-stu-id="c488e-141">This value is typically returned if the address book provider that contains the object is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c488e-142">Замечания</span><span class="sxs-lookup"><span data-stu-id="c488e-142">Remarks</span></span>

<span data-ttu-id="c488e-143">Метод **IMAPISupport::OpenEntry** применяется для всех объектов поддержки поставщика службы.</span><span class="sxs-lookup"><span data-stu-id="c488e-143">The **IMAPISupport::OpenEntry** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="c488e-144">Поставщики услуг вызовите **IMAPISupport::OpenEntry** , чтобы получить указатель на интерфейс, который можно использовать для доступа к определенному объекту.</span><span class="sxs-lookup"><span data-stu-id="c488e-144">Service providers call **IMAPISupport::OpenEntry** to retrieve a pointer to an interface that can be used to access a particular object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c488e-145">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="c488e-145">Notes to callers</span></span>

<span data-ttu-id="c488e-146">Вызов **IMAPISupport::OpenEntry** только в том случае, если вы не знаете, открыв вид объекта.</span><span class="sxs-lookup"><span data-stu-id="c488e-146">Call **IMAPISupport::OpenEntry** only when you do not know what kind of object you are opening.</span></span> <span data-ttu-id="c488e-147">Если вы знаете, что открывается в папку или сообщение, вызовите [IMsgStore::OpenEntry](imsgstore-openentry.md) .</span><span class="sxs-lookup"><span data-stu-id="c488e-147">If you know you are opening a folder or a message, call [IMsgStore::OpenEntry](imsgstore-openentry.md) instead.</span></span> <span data-ttu-id="c488e-148">Если вы знаете, что открывается контейнер адресной книги, обмена мгновенными сообщениями пользователя или список рассылки, вызовите [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="c488e-148">If you know you are opening an address book container, a messaging user, or a distribution list, call [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="c488e-149">Эти дополнительные методы выполняются быстрее, чем **IMAPISupport::OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="c488e-149">These more specific methods are faster than **IMAPISupport::OpenEntry**.</span></span> 
  
 <span data-ttu-id="c488e-150">**IMAPISupport::OpenEntry** открывает все объекты с доступом только для чтения, если не задан флаг MAPI_MODIFY или MAPI_BEST_ACCESS в параметре _ulFlags_ и достаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="c488e-150">**IMAPISupport::OpenEntry** opens all objects as read-only, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter and your permissions are sufficient.</span></span> <span data-ttu-id="c488e-151">Настройка одного из этих флагов не гарантирует определенным типом доступа; разрешения, которые будут предоставлены зависят от вам уровень доступа, объект и поставщика услуг, которому принадлежит объект.</span><span class="sxs-lookup"><span data-stu-id="c488e-151">Setting one of these flags does not guarantee a particular type of access; the permissions that you are granted depend on your access level, the object, and the service provider that owns the object.</span></span> <span data-ttu-id="c488e-152">Чтобы определить уровень доступа для открытого объекта, получения его свойство **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c488e-152">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="c488e-153">Проверьте значение, возвращенное в параметре _lpulObjType_ , чтобы определить, что тип объекта, возвращенного ожидаемого.</span><span class="sxs-lookup"><span data-stu-id="c488e-153">Check the value returned in the  _lpulObjType_ parameter to determine that the object type returned is what you expected.</span></span> <span data-ttu-id="c488e-154">Если тип объекта является, как ожидалось, приведены указатель с помощью параметра _lppUnk_ указатель соответствующего типа.</span><span class="sxs-lookup"><span data-stu-id="c488e-154">If the object type is as expected, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="c488e-155">Например при открытии папки привести _lppUnk_ для указателя типа LPMAPIFOLDER.</span><span class="sxs-lookup"><span data-stu-id="c488e-155">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type LPMAPIFOLDER.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c488e-156">См. также</span><span class="sxs-lookup"><span data-stu-id="c488e-156">See also</span></span>



[<span data-ttu-id="c488e-157">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c488e-157">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

