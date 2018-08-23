---
title: IMsgStoreOpenEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.OpenEntry
api_type:
- COM
ms.assetid: a63c42cf-36af-466b-b41e-d6b53ce1c9fb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 611680db87c02b9370d6c1b3ac7a8d68b47f3050
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574029"
---
# <a name="imsgstoreopenentry"></a><span data-ttu-id="dc02e-103">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="dc02e-103">IMsgStore::OpenEntry</span></span>

  
  
<span data-ttu-id="dc02e-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc02e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc02e-105">Открывает папку или сообщение и возвращает указатель интерфейса для дальнейшей доступа.</span><span class="sxs-lookup"><span data-stu-id="dc02e-105">Opens a folder or message and returns an interface pointer for further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="dc02e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc02e-106">Parameters</span></span>

 <span data-ttu-id="dc02e-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="dc02e-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="dc02e-108">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ _._</span><span class="sxs-lookup"><span data-stu-id="dc02e-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter  _._</span></span>
    
 <span data-ttu-id="dc02e-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="dc02e-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="dc02e-110">[in] Указатель на идентификатор записи объекта, чтобы открыть или значение NULL.</span><span class="sxs-lookup"><span data-stu-id="dc02e-110">[in] A pointer to the entry identifier of the object to open, or NULL.</span></span> <span data-ttu-id="dc02e-111">Если _lpEntryID_ имеет значение NULL, **OpenEntry** откроется корневой папки для хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="dc02e-111">If  _lpEntryID_ is set to NULL, **OpenEntry** opens the root folder for the message store.</span></span> 
    
 <span data-ttu-id="dc02e-112">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="dc02e-112">_lpInterface_</span></span>
  
> <span data-ttu-id="dc02e-113">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к объекту открыт.</span><span class="sxs-lookup"><span data-stu-id="dc02e-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the opened object.</span></span> <span data-ttu-id="dc02e-114">Передача значение NULL, приводит к объекту в стандартный интерфейс ([IMAPIFolder](imapifolderimapicontainer.md) для папок) и [IMessage](imessageimapiprop.md) для сообщений, возвращаемых.</span><span class="sxs-lookup"><span data-stu-id="dc02e-114">Passing NULL results in the object's standard interface ([IMAPIFolder](imapifolderimapicontainer.md) for folders and [IMessage](imessageimapiprop.md) for messages) being returned.</span></span> 
    
 <span data-ttu-id="dc02e-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dc02e-115">_ulFlags_</span></span>
  
> <span data-ttu-id="dc02e-116">[in] Битовая маска флаги, который определяет способ открытия объекта.</span><span class="sxs-lookup"><span data-stu-id="dc02e-116">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="dc02e-117">Можно использовать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="dc02e-117">The following flags can be used:</span></span>
    
<span data-ttu-id="dc02e-118">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="dc02e-118">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="dc02e-119">Запрашивает открыть объект с помощью максимальное сетевое разрешения для пользователя и приложения максимальное клиентского доступа.</span><span class="sxs-lookup"><span data-stu-id="dc02e-119">Requests that the object be opened by using the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="dc02e-120">Например если клиент имеет разрешение на чтение и запись, объект должен быть открыт с помощью разрешение на чтение и запись. Если клиент имеет разрешение на чтение, объект должен быть открыт с помощью разрешений только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dc02e-120">For example, if the client has read/write permission, the object should be opened by using read/write permission; if the client has read-only permission, the object should be opened by using read-only permission.</span></span> 
    
<span data-ttu-id="dc02e-121">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="dc02e-121">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="dc02e-122">Позволяет **OpenEntry** для возврата успешно, возможно перед объект полностью доступен для клиента.</span><span class="sxs-lookup"><span data-stu-id="dc02e-122">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="dc02e-123">Если объект недоступен, вызов последующих объектов может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="dc02e-123">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="dc02e-124">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="dc02e-124">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="dc02e-125">Запросы на разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="dc02e-125">Requests read/write permission.</span></span> <span data-ttu-id="dc02e-126">По умолчанию объекты открываются с разрешением только для чтения, и клиенты не должны работать предполагается, что что разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="dc02e-126">By default, objects are opened with read-only permission, and clients should not work on the assumption that read/write permission is granted.</span></span> 
    
 <span data-ttu-id="dc02e-127">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="dc02e-127">_lpulObjType_</span></span>
  
> <span data-ttu-id="dc02e-128">[out] Указатель на тип объекта открыт.</span><span class="sxs-lookup"><span data-stu-id="dc02e-128">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="dc02e-129">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="dc02e-129">_lppUnk_</span></span>
  
> <span data-ttu-id="dc02e-130">[out] Указатель на указатель на объект открыт.</span><span class="sxs-lookup"><span data-stu-id="dc02e-130">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dc02e-131">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="dc02e-131">Return value</span></span>

<span data-ttu-id="dc02e-132">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="dc02e-132">S_OK</span></span> 
  
> <span data-ttu-id="dc02e-133">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="dc02e-133">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="dc02e-134">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="dc02e-134">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="dc02e-135">Предпринята попытка изменения объекта только для чтения или для доступа к объекту, для которого пользователь имеет недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="dc02e-135">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="dc02e-136">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="dc02e-136">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="dc02e-137">При открытии хранилища в режиме кэширования клиента или поставщика можно вызвать **IMsgStore::OpenEntry**, установка флага MAPI_NO_CACHE для открытия элемента или папки для удаленного хранилища.</span><span class="sxs-lookup"><span data-stu-id="dc02e-137">When a store is opened in cached mode, a client or service provider can call **IMsgStore::OpenEntry**, setting the MAPI_NO_CACHE flag to open an item or a folder on the remote store.</span></span> <span data-ttu-id="dc02e-138">При открытии хранилища сообщений с флагом MDB_ONLINE на удаленном сервере, не нужно использовать флаг MAPI_NO_CACHE.</span><span class="sxs-lookup"><span data-stu-id="dc02e-138">If you open the message store with the MDB_ONLINE flag on the remote server, you do not have to use the MAPI_NO_CACHE flag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dc02e-139">Замечания</span><span class="sxs-lookup"><span data-stu-id="dc02e-139">Remarks</span></span>

<span data-ttu-id="dc02e-140">Метод **IMsgStore::OpenEntry** открывает папку или сообщение и возвращает указатель на интерфейс, который может использоваться для дальнейшей доступа.</span><span class="sxs-lookup"><span data-stu-id="dc02e-140">The **IMsgStore::OpenEntry** method opens a folder or message and returns a pointer to an interface that can be used for further access.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="dc02e-141">При открытии записи папки для общего хранилища, например, папок и сообщений, используйте **IMsgStore::OpenEntry** вместо [IMAPISession::OpenEntry](imapisession-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="dc02e-141">When opening folder entries on a public store, such as folders and messages, use **IMsgStore::OpenEntry** instead of [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span> <span data-ttu-id="dc02e-142">Это обеспечить общедоступные папки правильное функционирование при определении нескольких учетных записей Exchange в профиле.</span><span class="sxs-lookup"><span data-stu-id="dc02e-142">This ensures that public folders function correctly when multiple Exchange accounts are defined in a profile.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="dc02e-143">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="dc02e-143">Notes to callers</span></span>

<span data-ttu-id="dc02e-144">Папки и сообщения автоматически открываются с разрешением только для чтения, если не задан флаг MAPI_MODIFY или MAPI_BEST_ACCESS в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="dc02e-144">Folders and messages are automatically opened with read-only permission, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="dc02e-145">Настройка одного из этих флагов не гарантирует определенный тип разрешений; разрешения, которые будут предоставлены зависят от поставщика хранилища сообщений, вам уровень доступа и объект.</span><span class="sxs-lookup"><span data-stu-id="dc02e-145">Setting one of these flags does not guarantee a particular type of permission; the permissions that you are granted depend on the message store provider, your access level, and the object.</span></span> <span data-ttu-id="dc02e-146">Чтобы определить уровень доступа для открытого объекта, получения его свойство **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="dc02e-146">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="dc02e-147">Несмотря на то, что **IMsgStore::OpenEntry** можно использовать для открытия любой папки или сообщения, он должен обычно быстрее, используйте метод [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) , если у вас есть доступ к папке родительской папки или сообщение, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="dc02e-147">Although **IMsgStore::OpenEntry** can be used to open any folder or message, it is usually faster to use the [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) method if you have access to the parent folder of the folder or message to be opened.</span></span> 
  
<span data-ttu-id="dc02e-148">Проверьте значение, возвращенное в параметре _lpulObjType_ , чтобы определить, является ли тип возвращаемого объекта ожидаемого.</span><span class="sxs-lookup"><span data-stu-id="dc02e-148">Check the value returned in the  _lpulObjType_ parameter to determine whether the returned object type is what you expected.</span></span> <span data-ttu-id="dc02e-149">Если тип объекта не ожидается тип, приведение указателя с помощью параметра _lppUnk_ указатель соответствующего типа.</span><span class="sxs-lookup"><span data-stu-id="dc02e-149">If the object type is not the expected type, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="dc02e-150">Например при открытии папки привести _lppUnk_ для указателя типа **LPMAPIFOLDER**.</span><span class="sxs-lookup"><span data-stu-id="dc02e-150">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type **LPMAPIFOLDER**.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="dc02e-151">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="dc02e-151">MFCMAPI reference</span></span>

<span data-ttu-id="dc02e-152">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="dc02e-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="dc02e-153">**����**</span><span class="sxs-lookup"><span data-stu-id="dc02e-153">**File**</span></span>|<span data-ttu-id="dc02e-154">**�������**</span><span class="sxs-lookup"><span data-stu-id="dc02e-154">**Function**</span></span>|<span data-ttu-id="dc02e-155">**�����������**</span><span class="sxs-lookup"><span data-stu-id="dc02e-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dc02e-156">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="dc02e-156">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="dc02e-157">CallOpenEntry</span><span class="sxs-lookup"><span data-stu-id="dc02e-157">CallOpenEntry</span></span>  <br/> |<span data-ttu-id="dc02e-158">Mfcmapi (en) использует метод **IMsgStore::OpenEntry** для открытия объекта, связанного с идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="dc02e-158">MFCMAPI uses the **IMsgStore::OpenEntry** method to open the object associated with an entry ID.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dc02e-159">См. также</span><span class="sxs-lookup"><span data-stu-id="dc02e-159">See also</span></span>



[<span data-ttu-id="dc02e-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="dc02e-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="dc02e-161">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="dc02e-161">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="dc02e-162">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="dc02e-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

