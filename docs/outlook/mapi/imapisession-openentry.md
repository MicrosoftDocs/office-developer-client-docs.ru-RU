---
title: IMAPISessionOpenEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenEntry
api_type:
- COM
ms.assetid: a4df4860-cf4f-4e97-97c4-fcd89b7f1f91
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 10992fdf53c416c473b90b5748b9c5fa4f65cffc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426389"
---
# <a name="imapisessionopenentry"></a><span data-ttu-id="53de8-103">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="53de8-103">IMAPISession::OpenEntry</span></span>

  
  
<span data-ttu-id="53de8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53de8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53de8-105">Открывает объект и возвращает указатель интерфейса для дополнительного доступа.</span><span class="sxs-lookup"><span data-stu-id="53de8-105">Opens an object and returns an interface pointer for additional access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="53de8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="53de8-106">Parameters</span></span>

 <span data-ttu-id="53de8-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="53de8-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="53de8-108">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="53de8-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="53de8-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="53de8-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="53de8-110">[in] Указатель на идентификатор записи объекта, который необходимо открыть.</span><span class="sxs-lookup"><span data-stu-id="53de8-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    
 <span data-ttu-id="53de8-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="53de8-111">_lpInterface_</span></span>
  
> <span data-ttu-id="53de8-112">[in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, используемый для доступа к открытому объекту.</span><span class="sxs-lookup"><span data-stu-id="53de8-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the opened object.</span></span> <span data-ttu-id="53de8-113">Передача NULL возвращает стандартный интерфейс объекта.</span><span class="sxs-lookup"><span data-stu-id="53de8-113">Passing NULL returns the object's standard interface.</span></span> <span data-ttu-id="53de8-114">Например, если объект, который необходимо открыть, является сообщением, стандартным интерфейсом будет [IMessage;](imessageimapiprop.md) для папок это [IMAPIFolder.](imapifolderimapicontainer.md)</span><span class="sxs-lookup"><span data-stu-id="53de8-114">For example, if the object to be opened is a message, the standard interface is [IMessage](imessageimapiprop.md); for folders, it is [IMAPIFolder](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="53de8-115">Стандартными интерфейсами для объектов адресной книги являются [IDistList](idistlistimapicontainer.md) для списка рассылки и [IMailUser](imailuserimapiprop.md) для пользователя обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="53de8-115">The standard interfaces for address book objects are [IDistList](idistlistimapicontainer.md) for a distribution list and [IMailUser](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="53de8-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="53de8-116">_ulFlags_</span></span>
  
> <span data-ttu-id="53de8-117">[in] Битоваяmas флагов, которая управляет открытием объекта.</span><span class="sxs-lookup"><span data-stu-id="53de8-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="53de8-118">Можно использовать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="53de8-118">The following flags can be used:</span></span>
    
<span data-ttu-id="53de8-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="53de8-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="53de8-120">Запрашивает открытие объекта с использованием максимального разрешения сети, разрешенного для пользователя, и максимального доступа клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="53de8-120">Requests that the object be opened by using the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="53de8-121">Например, если у клиента есть разрешение на чтение и записи, объект должен быть открыт с разрешением на чтение и записи; если у клиента есть разрешение только для чтения, объект должен быть открыт с разрешением только для чтения.</span><span class="sxs-lookup"><span data-stu-id="53de8-121">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only permission, the object should be opened with read-only permission.</span></span> 
    
<span data-ttu-id="53de8-122">MAPI_CACHE_OK</span><span class="sxs-lookup"><span data-stu-id="53de8-122">MAPI_CACHE_OK</span></span>
  
> <span data-ttu-id="53de8-123">Используйте все средства, включая автономные адресные книги, для разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="53de8-123">Use all means, including offline address books, to perform name resolution.</span></span>
    
<span data-ttu-id="53de8-124">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="53de8-124">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="53de8-125">Используйте только автономной адресной книги для разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="53de8-125">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="53de8-126">Например, этот флаг можно использовать, чтобы разрешить клиентского приложения открывать глобальный список адресов (GAL) в режиме кэшации exchange и получать доступ к записи в этой адресной книге из кэша без создания трафика между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="53de8-126">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="53de8-127">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="53de8-127">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="53de8-128">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="53de8-128">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="53de8-129">Позволяет **OpenEntry** успешно возвращаться, возможно, до того, как объект будет полностью доступен вызываемому клиенту.</span><span class="sxs-lookup"><span data-stu-id="53de8-129">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="53de8-130">Если объект не доступен, последующий вызов объекта может привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="53de8-130">If the object is not available, making a subsequent object call can cause an error.</span></span> 
    
<span data-ttu-id="53de8-131">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="53de8-131">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="53de8-132">Запрашивает разрешение на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="53de8-132">Requests read/write permission.</span></span> <span data-ttu-id="53de8-133">По умолчанию объекты открываются с разрешением только на чтение, и клиенты не должны работать при предположении, что разрешение на чтение и чтение предоставлено.</span><span class="sxs-lookup"><span data-stu-id="53de8-133">By default, objects are opened with read-only permission, and clients should not work on the assumption that read/write permission is granted.</span></span> 
    
<span data-ttu-id="53de8-134">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="53de8-134">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="53de8-135">Не используйте автономной адресной книги для разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="53de8-135">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="53de8-136">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="53de8-136">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="53de8-137">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="53de8-137">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="53de8-138">Показать элементы, которые в настоящее время помечены как "мягко удаленные" (то есть находятся на этапе хранения удаленных элементов).</span><span class="sxs-lookup"><span data-stu-id="53de8-138">Show items that are currently marked as soft deleted (that is, they are in the deleted item retention time phase).</span></span>
    
 <span data-ttu-id="53de8-139">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="53de8-139">_lpulObjType_</span></span>
  
> <span data-ttu-id="53de8-140">[out] Указатель на тип открытого объекта.</span><span class="sxs-lookup"><span data-stu-id="53de8-140">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="53de8-141">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="53de8-141">_lppUnk_</span></span>
  
> <span data-ttu-id="53de8-142">[out] Указатель на указатель на открытый объект.</span><span class="sxs-lookup"><span data-stu-id="53de8-142">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="53de8-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53de8-143">Return value</span></span>

<span data-ttu-id="53de8-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="53de8-144">S_OK</span></span> 
  
> <span data-ttu-id="53de8-145">Объект был успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="53de8-145">The object was opened successfully.</span></span>
    
<span data-ttu-id="53de8-146">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="53de8-146">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="53de8-147">Предпринята попытка изменить объект, доступный только для чтения, или попытка доступа к объекту, у которого у пользователя недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="53de8-147">An attempt was made to modify a read-only object or an attempt was made to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="53de8-148">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="53de8-148">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="53de8-149">Объект, связанный с идентификатором записи, переданным в  _параметре lpEntryID, не_ существует.</span><span class="sxs-lookup"><span data-stu-id="53de8-149">There is not an object associated with the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="53de8-150">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="53de8-150">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="53de8-151">Идентификатор записи, переданный в  _параметре lpEntryID,_ имеет неизвестный формат.</span><span class="sxs-lookup"><span data-stu-id="53de8-151">The entry identifier passed in the  _lpEntryID_ parameter is in an unrecognizable format.</span></span> <span data-ttu-id="53de8-152">Обычно это значение возвращается, если поставщик услуг, содержащий объект, не открыт.</span><span class="sxs-lookup"><span data-stu-id="53de8-152">This value is typically returned if the service provider that contains the object is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="53de8-153">Примечания</span><span class="sxs-lookup"><span data-stu-id="53de8-153">Remarks</span></span>

<span data-ttu-id="53de8-154">Метод **IMAPISession::OpenEntry** открывает хранилище сообщений или объект адресной книги, возвращая указатель на интерфейс, который можно использовать для доступа к объекту.</span><span class="sxs-lookup"><span data-stu-id="53de8-154">The **IMAPISession::OpenEntry** method opens a message store or address book object, returning a pointer to an interface that can be used to access the object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="53de8-155">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="53de8-155">Notes to callers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="53de8-156">При открытии записей в общедоступных магазинах, таких как папки и сообщения, используйте [IMsgStore::OpenEntry](imsgstore-openentry.md) вместо **IMAPISession::OpenEntry.**</span><span class="sxs-lookup"><span data-stu-id="53de8-156">When opening folder entries on a public store, such as folders and messages, use [IMsgStore::OpenEntry](imsgstore-openentry.md) instead of **IMAPISession::OpenEntry**.</span></span> <span data-ttu-id="53de8-157">Это гарантирует правильную работу общедоступных папок, если в профиле определено несколько учетных записей Exchange.</span><span class="sxs-lookup"><span data-stu-id="53de8-157">This ensures that public folders function correctly when multiple Exchange accounts are defined in a profile.</span></span> 
  
<span data-ttu-id="53de8-158">Вызовите **IMAPISession::OpenEntry** только в том случае, если вы не знаете, какой объект открывается.</span><span class="sxs-lookup"><span data-stu-id="53de8-158">Call **IMAPISession::OpenEntry** only when you do not know what kind of object that you are opening.</span></span> <span data-ttu-id="53de8-159">Если вы знаете, что открываете папку или сообщение, вызовите [IMsgStore::OpenEntry.](imsgstore-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="53de8-159">If you know that you are opening a folder or a message, call [IMsgStore::OpenEntry](imsgstore-openentry.md).</span></span> <span data-ttu-id="53de8-160">Если вы знаете, что вы открываете контейнер адресной книги, пользователя обмена сообщениями или список рассылки, вызовите [IAddrBook::OpenEntry.](iaddrbook-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="53de8-160">If you know that you are opening an address book container, a messaging user, or a distribution list, call [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="53de8-161">Эти более конкретные методы **быстрее, чем IMAPISession::OpenEntry.**</span><span class="sxs-lookup"><span data-stu-id="53de8-161">These more specific methods are faster than **IMAPISession::OpenEntry**.</span></span> 
  
<span data-ttu-id="53de8-162">MAPI открывает все объекты с разрешением только для чтения, если вы не MAPI_MODIFY или MAPI_BEST_ACCESS флага в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="53de8-162">MAPI opens all objects with read-only permission, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="53de8-163">Установка одного из этих флагов не гарантирует определенный тип доступа; Предоставленные разрешения зависят от поставщика услуг, уровня доступа и объекта.</span><span class="sxs-lookup"><span data-stu-id="53de8-163">Setting one of these flags does not guarantee a particular type of access; the permissions that are granted depend on the service provider, the access level, and the object.</span></span> <span data-ttu-id="53de8-164">Чтобы определить уровень доступа открытого объекта, извлекаете **его PR_ACCESS_LEVEL** ([PidTagAccessLevel).](pidtagaccesslevel-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="53de8-164">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="53de8-165">Вызов **IMAPISession::OpenEntry** и настройка  _lpEntryID_ для ссылки на идентификатор записи в хранилище сообщений это то же, что вызов метода [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) с установленным флагом MDB_NO_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="53de8-165">Calling **IMAPISession::OpenEntry** and setting  _lpEntryID_ to point to the entry identifier of a message store is the same as calling the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method with the MDB_NO_DIALOG flag set.</span></span> <span data-ttu-id="53de8-166">Параметры флага также эквивалентны, за исключением того, что для запроса разрешения на чтение и записи в **OpenMsgStore** необходимо установить флаг MDB_WRITE, а не MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="53de8-166">The flag settings are also equivalent, except that to request read/write permission with **OpenMsgStore**, you must set the MDB_WRITE flag instead of MAPI_MODIFY.</span></span> 
  
<span data-ttu-id="53de8-167">Проверьте значение, возвращаемого в  _параметре lpulObjType,_ чтобы определить, является ли возвращаемого типа объекта ожидаемым.</span><span class="sxs-lookup"><span data-stu-id="53de8-167">Check the value returned in the  _lpulObjType_ parameter to determine whether the object type returned is what you expected.</span></span> <span data-ttu-id="53de8-168">Если тип объекта не тот, который вы ожидали, приведите указатель из параметра  _lppUnk_ к указателю соответствующего типа.</span><span class="sxs-lookup"><span data-stu-id="53de8-168">If the object type is not the type that you expected, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="53de8-169">Например, если вы открываете папку, приведите  _lppUnk_ к указателю типа LPMAPIFOLDER.</span><span class="sxs-lookup"><span data-stu-id="53de8-169">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type LPMAPIFOLDER.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="53de8-170">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="53de8-170">MFCMAPI reference</span></span>

<span data-ttu-id="53de8-171">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="53de8-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="53de8-172">**Файл**</span><span class="sxs-lookup"><span data-stu-id="53de8-172">**File**</span></span>|<span data-ttu-id="53de8-173">**Функция**</span><span class="sxs-lookup"><span data-stu-id="53de8-173">**Function**</span></span>|<span data-ttu-id="53de8-174">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="53de8-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="53de8-175">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="53de8-175">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="53de8-176">CallOpenEntry</span><span class="sxs-lookup"><span data-stu-id="53de8-176">CallOpenEntry</span></span>  <br/> |<span data-ttu-id="53de8-177">MFCMAPI использует метод **IMAPISession::OpenEntry** для открытия объекта.</span><span class="sxs-lookup"><span data-stu-id="53de8-177">MFCMAPI uses the **IMAPISession::OpenEntry** method to open an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="53de8-178">См. также</span><span class="sxs-lookup"><span data-stu-id="53de8-178">See also</span></span>



[<span data-ttu-id="53de8-179">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="53de8-179">IAddrBook::OpenEntry</span></span>](iaddrbook-openentry.md)
  
[<span data-ttu-id="53de8-180">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="53de8-180">IDistList : IMAPIContainer</span></span>](idistlistimapicontainer.md)
  
[<span data-ttu-id="53de8-181">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="53de8-181">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md)
  
[<span data-ttu-id="53de8-182">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="53de8-182">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="53de8-183">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="53de8-183">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="53de8-184">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="53de8-184">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
  
[<span data-ttu-id="53de8-185">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="53de8-185">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="53de8-186">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="53de8-186">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="53de8-187">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="53de8-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

