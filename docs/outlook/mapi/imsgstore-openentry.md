---
title: имсгстореопенентри
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
ms.openlocfilehash: 07667558a21a9110d684164d2e6c143d6a519368
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409337"
---
# <a name="imsgstoreopenentry"></a><span data-ttu-id="7d157-103">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="7d157-103">IMsgStore::OpenEntry</span></span>

  
  
<span data-ttu-id="7d157-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d157-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d157-105">Открывает папку или сообщение и возвращает указатель интерфейса для получения дальнейших прав.</span><span class="sxs-lookup"><span data-stu-id="7d157-105">Opens a folder or message and returns an interface pointer for further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="7d157-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d157-106">Parameters</span></span>

 <span data-ttu-id="7d157-107">_кбентрид_</span><span class="sxs-lookup"><span data-stu-id="7d157-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="7d157-108">возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ _._</span><span class="sxs-lookup"><span data-stu-id="7d157-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter  _._</span></span>
    
 <span data-ttu-id="7d157-109">_лпентрид_</span><span class="sxs-lookup"><span data-stu-id="7d157-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="7d157-110">возврата Указатель на идентификатор записи объекта, который требуется открыть, или значение NULL.</span><span class="sxs-lookup"><span data-stu-id="7d157-110">[in] A pointer to the entry identifier of the object to open, or NULL.</span></span> <span data-ttu-id="7d157-111">Если для _лпентрид_ ЗАДАНО значение null, **OpenEntry** открывает корневую папку для хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="7d157-111">If  _lpEntryID_ is set to NULL, **OpenEntry** opens the root folder for the message store.</span></span> 
    
 <span data-ttu-id="7d157-112">_лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="7d157-112">_lpInterface_</span></span>
  
> <span data-ttu-id="7d157-113">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к открытому объекту.</span><span class="sxs-lookup"><span data-stu-id="7d157-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the opened object.</span></span> <span data-ttu-id="7d157-114">При передаче значений NULL в стандартном интерфейсе объекта ([IMAPIFolder](imapifolderimapicontainer.md) для папок и [iMessage](imessageimapiprop.md) для сообщений) возвращается.</span><span class="sxs-lookup"><span data-stu-id="7d157-114">Passing NULL results in the object's standard interface ([IMAPIFolder](imapifolderimapicontainer.md) for folders and [IMessage](imessageimapiprop.md) for messages) being returned.</span></span> 
    
 <span data-ttu-id="7d157-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7d157-115">_ulFlags_</span></span>
  
> <span data-ttu-id="7d157-116">возврата Битовая маска флагов, определяющих способ открытия объекта.</span><span class="sxs-lookup"><span data-stu-id="7d157-116">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="7d157-117">Можно использовать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="7d157-117">The following flags can be used:</span></span>
    
<span data-ttu-id="7d157-118">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="7d157-118">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="7d157-119">Запрос на открытие объекта с использованием максимальных сетевых разрешений, разрешенных для пользователя, и максимального доступа к клиентскому приложению.</span><span class="sxs-lookup"><span data-stu-id="7d157-119">Requests that the object be opened by using the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="7d157-120">Например, если у клиента есть разрешение на чтение и запись, объект должен быть открыт с помощью разрешения на чтение и запись; Если клиент имеет разрешение только на чтение, этот объект должен быть открыт с помощью разрешения "только чтение".</span><span class="sxs-lookup"><span data-stu-id="7d157-120">For example, if the client has read/write permission, the object should be opened by using read/write permission; if the client has read-only permission, the object should be opened by using read-only permission.</span></span> 
    
<span data-ttu-id="7d157-121">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="7d157-121">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="7d157-122">Разрешает успешное возвращение **OpenEntry** , возможно, перед тем, как объект будет полностью доступен для вызывающего клиента.</span><span class="sxs-lookup"><span data-stu-id="7d157-122">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="7d157-123">Если объект недоступен, то выполнение следующего вызова объекта может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="7d157-123">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="7d157-124">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="7d157-124">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="7d157-125">Запрашивает разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="7d157-125">Requests read/write permission.</span></span> <span data-ttu-id="7d157-126">По умолчанию объекты открываются с разрешением только для чтения, и клиенты не должны работать в предположении, что предоставлено разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="7d157-126">By default, objects are opened with read-only permission, and clients should not work on the assumption that read/write permission is granted.</span></span> 
    
 <span data-ttu-id="7d157-127">_лпулобжтипе_</span><span class="sxs-lookup"><span data-stu-id="7d157-127">_lpulObjType_</span></span>
  
> <span data-ttu-id="7d157-128">вышли Указатель на тип открытого объекта.</span><span class="sxs-lookup"><span data-stu-id="7d157-128">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="7d157-129">_лппунк_</span><span class="sxs-lookup"><span data-stu-id="7d157-129">_lppUnk_</span></span>
  
> <span data-ttu-id="7d157-130">вышли Указатель на указатель на открытый объект.</span><span class="sxs-lookup"><span data-stu-id="7d157-130">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7d157-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d157-131">Return value</span></span>

<span data-ttu-id="7d157-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="7d157-132">S_OK</span></span> 
  
> <span data-ttu-id="7d157-133">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="7d157-133">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="7d157-134">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="7d157-134">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="7d157-135">Предпринята попытка изменить объект, предназначенный только для чтения, или доступ к объекту, для которого у пользователя недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="7d157-135">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="7d157-136">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="7d157-136">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="7d157-137">Когда хранилище открывается в режиме кэширования, клиент или поставщик услуг может вызвать **IMsgStore:: OpenEntry**, установив флаг MAPI_NO_CACHE, чтобы открыть элемент или папку в удаленном хранилище.</span><span class="sxs-lookup"><span data-stu-id="7d157-137">When a store is opened in cached mode, a client or service provider can call **IMsgStore::OpenEntry**, setting the MAPI_NO_CACHE flag to open an item or a folder on the remote store.</span></span> <span data-ttu-id="7d157-138">Если вы откроете хранилище сообщений с флагом MDB_ONLINE на удаленном сервере, не нужно использовать флаг MAPI_NO_CACHE.</span><span class="sxs-lookup"><span data-stu-id="7d157-138">If you open the message store with the MDB_ONLINE flag on the remote server, you do not have to use the MAPI_NO_CACHE flag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7d157-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="7d157-139">Remarks</span></span>

<span data-ttu-id="7d157-140">Метод **IMsgStore:: OpenEntry** открывает папку или сообщение и возвращает указатель на интерфейс, который можно использовать для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="7d157-140">The **IMsgStore::OpenEntry** method opens a folder or message and returns a pointer to an interface that can be used for further access.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="7d157-141">При открытии записей папки в общедоступном хранилище, например папках и сообщениях, используйте **IMsgStore:: OpenEntry** вместо [IMAPISession:: OpenEntry](imapisession-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="7d157-141">When opening folder entries on a public store, such as folders and messages, use **IMsgStore::OpenEntry** instead of [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span> <span data-ttu-id="7d157-142">Это гарантирует корректное функционирование общедоступных папок, если в профиле определено несколько учетных записей Exchange.</span><span class="sxs-lookup"><span data-stu-id="7d157-142">This ensures that public folders function correctly when multiple Exchange accounts are defined in a profile.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7d157-143">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="7d157-143">Notes to callers</span></span>

<span data-ttu-id="7d157-144">Папки и сообщения автоматически открываются с разрешением только для чтения, если не установлен флаг MAPI_MODIFY или MAPI_BEST_ACCESS в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="7d157-144">Folders and messages are automatically opened with read-only permission, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="7d157-145">Установка одного из этих флагов не гарантирует определенный тип разрешения; предоставленные разрешения зависят от поставщика хранилища сообщений, уровня доступа и объекта.</span><span class="sxs-lookup"><span data-stu-id="7d157-145">Setting one of these flags does not guarantee a particular type of permission; the permissions that you are granted depend on the message store provider, your access level, and the object.</span></span> <span data-ttu-id="7d157-146">Чтобы определить уровень доступа открытого объекта, извлеките его свойство **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7d157-146">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="7d157-147">Несмотря на то, что **IMsgStore:: OpenEntry** можно использовать для открытия любой папки или сообщения, обычно быстрее использовать метод [IMAPIContainer:: OpenEntry](imapicontainer-openentry.md) , если у вас есть доступ к родительской папке открываемой папки или сообщения.</span><span class="sxs-lookup"><span data-stu-id="7d157-147">Although **IMsgStore::OpenEntry** can be used to open any folder or message, it is usually faster to use the [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) method if you have access to the parent folder of the folder or message to be opened.</span></span> 
  
<span data-ttu-id="7d157-148">Проверьте значение, возвращенное в параметре _лпулобжтипе_ , чтобы определить, является ли возвращаемый тип объекта ожидаемым.</span><span class="sxs-lookup"><span data-stu-id="7d157-148">Check the value returned in the  _lpulObjType_ parameter to determine whether the returned object type is what you expected.</span></span> <span data-ttu-id="7d157-149">Если тип объекта не является ожидаемым, приведите указатель из параметра _лппунк_ к указателю соответствующего типа.</span><span class="sxs-lookup"><span data-stu-id="7d157-149">If the object type is not the expected type, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="7d157-150">Например, если вы открываете папку, приведите _лппунк_ к указателю типа **лпмапифолдер**.</span><span class="sxs-lookup"><span data-stu-id="7d157-150">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type **LPMAPIFOLDER**.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7d157-151">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7d157-151">MFCMAPI reference</span></span>

<span data-ttu-id="7d157-152">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="7d157-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7d157-153">**Файл**</span><span class="sxs-lookup"><span data-stu-id="7d157-153">**File**</span></span>|<span data-ttu-id="7d157-154">**Функция**</span><span class="sxs-lookup"><span data-stu-id="7d157-154">**Function**</span></span>|<span data-ttu-id="7d157-155">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="7d157-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7d157-156">Мапифунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="7d157-156">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="7d157-157">каллопенентри</span><span class="sxs-lookup"><span data-stu-id="7d157-157">CallOpenEntry</span></span>  <br/> |<span data-ttu-id="7d157-158">MFCMAPI использует метод **IMsgStore:: OpenEntry** , чтобы открыть объект, связанный с идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="7d157-158">MFCMAPI uses the **IMsgStore::OpenEntry** method to open the object associated with an entry ID.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7d157-159">См. также</span><span class="sxs-lookup"><span data-stu-id="7d157-159">See also</span></span>



[<span data-ttu-id="7d157-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="7d157-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="7d157-161">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7d157-161">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="7d157-162">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="7d157-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

