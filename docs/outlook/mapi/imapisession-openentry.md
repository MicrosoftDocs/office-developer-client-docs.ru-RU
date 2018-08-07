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
ms.openlocfilehash: f23b4855b7e2faeb599868f8c2db52ae9cbfbfd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809064"
---
# <a name="imapisessionopenentry"></a><span data-ttu-id="6acc9-103">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="6acc9-103">IMAPISession::OpenEntry</span></span>

  
  
<span data-ttu-id="6acc9-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6acc9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6acc9-105">Открывает объект и возвращает указатель интерфейса для дополнительные права доступа.</span><span class="sxs-lookup"><span data-stu-id="6acc9-105">Opens an object and returns an interface pointer for additional access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="6acc9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6acc9-106">Parameters</span></span>

 <span data-ttu-id="6acc9-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="6acc9-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="6acc9-108">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="6acc9-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="6acc9-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="6acc9-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="6acc9-110">[in] Указатель на запись идентификатор объекта для открытия.</span><span class="sxs-lookup"><span data-stu-id="6acc9-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    
 <span data-ttu-id="6acc9-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="6acc9-111">_lpInterface_</span></span>
  
> <span data-ttu-id="6acc9-112">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к объекту открыт.</span><span class="sxs-lookup"><span data-stu-id="6acc9-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the opened object.</span></span> <span data-ttu-id="6acc9-113">Передача NULL Возвращает стандартный интерфейс объекта.</span><span class="sxs-lookup"><span data-stu-id="6acc9-113">Passing NULL returns the object's standard interface.</span></span> <span data-ttu-id="6acc9-114">Например если к объекту, чтобы открыть сообщение, стандартный интерфейс будет [IMessage](imessageimapiprop.md); для папок это [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="6acc9-114">For example, if the object to be opened is a message, the standard interface is [IMessage](imessageimapiprop.md); for folders, it is [IMAPIFolder](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="6acc9-115">Стандартные интерфейсы для объектов адресной книги — [IDistList](idistlistimapicontainer.md) для списка рассылки, а также [IMailUser](imailuserimapiprop.md) для обмена сообщениями пользователя.</span><span class="sxs-lookup"><span data-stu-id="6acc9-115">The standard interfaces for address book objects are [IDistList](idistlistimapicontainer.md) for a distribution list and [IMailUser](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="6acc9-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6acc9-116">_ulFlags_</span></span>
  
> <span data-ttu-id="6acc9-117">[in] Битовая маска флаги, который определяет способ открытия объекта.</span><span class="sxs-lookup"><span data-stu-id="6acc9-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="6acc9-118">Можно использовать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="6acc9-118">The following flags can be used:</span></span>
    
<span data-ttu-id="6acc9-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="6acc9-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="6acc9-120">Запрашивает открыть объект с помощью максимальное сетевое разрешения для пользователя и приложения максимальное клиентского доступа.</span><span class="sxs-lookup"><span data-stu-id="6acc9-120">Requests that the object be opened by using the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="6acc9-121">Например если клиент имеет разрешение на чтение и запись, объект должен быть открыт получившие разрешение на чтение и запись; Если клиент имеет разрешение на чтение, объект должен быть открыт с разрешением только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6acc9-121">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only permission, the object should be opened with read-only permission.</span></span> 
    
<span data-ttu-id="6acc9-122">MAPI_CACHE_OK</span><span class="sxs-lookup"><span data-stu-id="6acc9-122">MAPI_CACHE_OK</span></span>
  
> <span data-ttu-id="6acc9-123">Для выполнения разрешения имен используйте все это значит, включая автономные адресные книги.</span><span class="sxs-lookup"><span data-stu-id="6acc9-123">Use all means, including offline address books, to perform name resolution.</span></span>
    
<span data-ttu-id="6acc9-124">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="6acc9-124">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="6acc9-125">Для выполнения разрешения имен используйте автономной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="6acc9-125">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="6acc9-126">Например можно использовать этот флаг позволяет открыть глобальный список адресов (GAL) в режиме кэширования данных exchange и получить доступ к записи в этот список адресов из кэша без создания трафика между клиентом и сервером клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="6acc9-126">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="6acc9-127">Этот флаг поддерживается только поставщик Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="6acc9-127">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="6acc9-128">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="6acc9-128">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="6acc9-129">Позволяет **OpenEntry** для возврата успешно, возможно перед объект полностью доступен для клиента.</span><span class="sxs-lookup"><span data-stu-id="6acc9-129">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="6acc9-130">Если объект недоступен, вызов последующих объектов может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="6acc9-130">If the object is not available, making a subsequent object call can cause an error.</span></span> 
    
<span data-ttu-id="6acc9-131">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="6acc9-131">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="6acc9-132">Запросы на разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="6acc9-132">Requests read/write permission.</span></span> <span data-ttu-id="6acc9-133">По умолчанию объекты открываются с разрешением только для чтения, и клиенты не должны работать предполагается, что что разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="6acc9-133">By default, objects are opened with read-only permission, and clients should not work on the assumption that read/write permission is granted.</span></span> 
    
<span data-ttu-id="6acc9-134">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="6acc9-134">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="6acc9-135">Не используйте автономной адресной книги для разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="6acc9-135">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="6acc9-136">Этот флаг поддерживается только поставщик Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="6acc9-136">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="6acc9-137">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="6acc9-137">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="6acc9-138">Отображение удаленных элементов, которые в настоящее время помечены как программных (то есть, они находятся в хранения удаленных элементов этап времени).</span><span class="sxs-lookup"><span data-stu-id="6acc9-138">Show items that are currently marked as soft deleted (that is, they are in the deleted item retention time phase).</span></span>
    
 <span data-ttu-id="6acc9-139">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="6acc9-139">_lpulObjType_</span></span>
  
> <span data-ttu-id="6acc9-140">[out] Указатель на тип объекта открыт.</span><span class="sxs-lookup"><span data-stu-id="6acc9-140">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="6acc9-141">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="6acc9-141">_lppUnk_</span></span>
  
> <span data-ttu-id="6acc9-142">[out] Указатель на указатель на объект открыт.</span><span class="sxs-lookup"><span data-stu-id="6acc9-142">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6acc9-143">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="6acc9-143">Return value</span></span>

<span data-ttu-id="6acc9-144">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="6acc9-144">S_OK</span></span> 
  
> <span data-ttu-id="6acc9-145">Объект был успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="6acc9-145">The object was opened successfully.</span></span>
    
<span data-ttu-id="6acc9-146">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="6acc9-146">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="6acc9-147">Попытка изменить объект только для чтения или предпринята попытка получить доступ к объекту, для которого пользователь имеет недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="6acc9-147">An attempt was made to modify a read-only object or an attempt was made to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="6acc9-148">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="6acc9-148">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="6acc9-149">Объект, связанный с идентификатором записи, переданной в параметре _lpEntryID_ не существует.</span><span class="sxs-lookup"><span data-stu-id="6acc9-149">There is not an object associated with the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="6acc9-150">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="6acc9-150">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="6acc9-151">Идентификатор записи, переданной в параметре _lpEntryID_ имеет неопознанный формат.</span><span class="sxs-lookup"><span data-stu-id="6acc9-151">The entry identifier passed in the  _lpEntryID_ parameter is in an unrecognizable format.</span></span> <span data-ttu-id="6acc9-152">Это значение возвращается как правило, если поставщик услуг, содержащее объект не открыт.</span><span class="sxs-lookup"><span data-stu-id="6acc9-152">This value is typically returned if the service provider that contains the object is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6acc9-153">Замечания</span><span class="sxs-lookup"><span data-stu-id="6acc9-153">Remarks</span></span>

<span data-ttu-id="6acc9-154">Открывает метод **IMAPISession::OpenEntry** сообщение хранения или адрес объекта книги, указатель возвращается интерфейс, который можно использовать для доступа к объекту.</span><span class="sxs-lookup"><span data-stu-id="6acc9-154">The **IMAPISession::OpenEntry** method opens a message store or address book object, returning a pointer to an interface that can be used to access the object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6acc9-155">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="6acc9-155">Notes to callers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6acc9-156">При открытии записи папки для общего хранилища, например, папок и сообщений, используйте [IMsgStore::OpenEntry](imsgstore-openentry.md) вместо **IMAPISession::OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="6acc9-156">When opening folder entries on a public store, such as folders and messages, use [IMsgStore::OpenEntry](imsgstore-openentry.md) instead of **IMAPISession::OpenEntry**.</span></span> <span data-ttu-id="6acc9-157">Это обеспечить общедоступные папки правильное функционирование при определении нескольких учетных записей Exchange в профиле.</span><span class="sxs-lookup"><span data-stu-id="6acc9-157">This ensures that public folders function correctly when multiple Exchange accounts are defined in a profile.</span></span> 
  
<span data-ttu-id="6acc9-158">Вызов **IMAPISession::OpenEntry** только в том случае, если вы не знаете, какой тип объекта, который открывается.</span><span class="sxs-lookup"><span data-stu-id="6acc9-158">Call **IMAPISession::OpenEntry** only when you do not know what kind of object that you are opening.</span></span> <span data-ttu-id="6acc9-159">Если вы знаете, что открывают папки или сообщения, вызовите [IMsgStore::OpenEntry](imsgstore-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="6acc9-159">If you know that you are opening a folder or a message, call [IMsgStore::OpenEntry](imsgstore-openentry.md).</span></span> <span data-ttu-id="6acc9-160">Если вы знаете, что открываемый контейнер адресной книги, обмена мгновенными сообщениями пользователя или список рассылки, вызовите [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="6acc9-160">If you know that you are opening an address book container, a messaging user, or a distribution list, call [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="6acc9-161">Эти дополнительные методы выполняются быстрее, чем **IMAPISession::OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="6acc9-161">These more specific methods are faster than **IMAPISession::OpenEntry**.</span></span> 
  
<span data-ttu-id="6acc9-162">MAPI открывает все объекты с разрешением только для чтения, если не задан флаг MAPI_MODIFY или MAPI_BEST_ACCESS в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="6acc9-162">MAPI opens all objects with read-only permission, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="6acc9-163">Настройка одного из этих флагов не гарантирует определенным типом доступа; разрешения, предоставленные зависят от поставщика услуг, уровень доступа и объект.</span><span class="sxs-lookup"><span data-stu-id="6acc9-163">Setting one of these flags does not guarantee a particular type of access; the permissions that are granted depend on the service provider, the access level, and the object.</span></span> <span data-ttu-id="6acc9-164">Чтобы определить уровень доступа для открытого объекта, получения его свойство **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6acc9-164">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="6acc9-165">Вызов **IMAPISession::OpenEntry** и параметр _lpEntryID_ для указания на идентификатор записи хранилища сообщений имеет то же, что вызов метода [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) с флагом MDB_NO_DIALOG значение.</span><span class="sxs-lookup"><span data-stu-id="6acc9-165">Calling **IMAPISession::OpenEntry** and setting  _lpEntryID_ to point to the entry identifier of a message store is the same as calling the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method with the MDB_NO_DIALOG flag set.</span></span> <span data-ttu-id="6acc9-166">Параметры флаг эквивалентны также, за исключением, для получения разрешения чтения и записи с **OpenMsgStore**, необходимо установить флаг MDB_WRITE вместо MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="6acc9-166">The flag settings are also equivalent, except that to request read/write permission with **OpenMsgStore**, you must set the MDB_WRITE flag instead of MAPI_MODIFY.</span></span> 
  
<span data-ttu-id="6acc9-167">Проверьте значение, возвращенное в параметре _lpulObjType_ , чтобы определить, является ли тип объекта, возвращенного ожидаемого.</span><span class="sxs-lookup"><span data-stu-id="6acc9-167">Check the value returned in the  _lpulObjType_ parameter to determine whether the object type returned is what you expected.</span></span> <span data-ttu-id="6acc9-168">Если тип объекта не тип, который вы неправильно, приведение указателя с помощью параметра _lppUnk_ указатель соответствующего типа.</span><span class="sxs-lookup"><span data-stu-id="6acc9-168">If the object type is not the type that you expected, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="6acc9-169">Например при открытии папки привести _lppUnk_ для указателя типа LPMAPIFOLDER.</span><span class="sxs-lookup"><span data-stu-id="6acc9-169">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type LPMAPIFOLDER.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6acc9-170">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="6acc9-170">MFCMAPI reference</span></span>

<span data-ttu-id="6acc9-171">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="6acc9-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6acc9-172">**����**</span><span class="sxs-lookup"><span data-stu-id="6acc9-172">**File**</span></span>|<span data-ttu-id="6acc9-173">**�������**</span><span class="sxs-lookup"><span data-stu-id="6acc9-173">**Function**</span></span>|<span data-ttu-id="6acc9-174">**�����������**</span><span class="sxs-lookup"><span data-stu-id="6acc9-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6acc9-175">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="6acc9-175">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="6acc9-176">CallOpenEntry</span><span class="sxs-lookup"><span data-stu-id="6acc9-176">CallOpenEntry</span></span>  <br/> |<span data-ttu-id="6acc9-177">Mfcmapi (en) использует метод **IMAPISession::OpenEntry** для открытия объекта.</span><span class="sxs-lookup"><span data-stu-id="6acc9-177">MFCMAPI uses the **IMAPISession::OpenEntry** method to open an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6acc9-178">См. также</span><span class="sxs-lookup"><span data-stu-id="6acc9-178">See also</span></span>



[<span data-ttu-id="6acc9-179">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="6acc9-179">IAddrBook::OpenEntry</span></span>](iaddrbook-openentry.md)
  
[<span data-ttu-id="6acc9-180">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="6acc9-180">IDistList : IMAPIContainer</span></span>](idistlistimapicontainer.md)
  
[<span data-ttu-id="6acc9-181">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6acc9-181">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md)
  
[<span data-ttu-id="6acc9-182">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="6acc9-182">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="6acc9-183">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="6acc9-183">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="6acc9-184">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6acc9-184">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
  
[<span data-ttu-id="6acc9-185">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="6acc9-185">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="6acc9-186">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6acc9-186">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="6acc9-187">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="6acc9-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

