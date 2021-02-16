---
title: IMAPIContainerOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.OpenEntry
api_type:
- COM
ms.assetid: 0c46c1fb-dd63-4ac5-960e-80f68e75d8f4
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9598e0c90c16db14cdc3a46d2b2ae74e0d9a9300
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423638"
---
# <a name="imapicontaineropenentry"></a><span data-ttu-id="ac336-103">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="ac336-103">IMAPIContainer::OpenEntry</span></span>

  
  
<span data-ttu-id="ac336-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac336-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac336-105">Открывает объект в контейнере, возвращая указатель интерфейса для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="ac336-105">Opens an object in the container, returning an interface pointer for further access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="ac336-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac336-106">Parameters</span></span>

 <span data-ttu-id="ac336-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ac336-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="ac336-108">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="ac336-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ac336-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="ac336-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="ac336-110">[in] Указатель на идентификатор записи объекта, который необходимо открыть.</span><span class="sxs-lookup"><span data-stu-id="ac336-110">[in] A pointer to the entry identifier of the object to open.</span></span> <span data-ttu-id="ac336-111">Если  _для lpEntryID_ задано NULL, открывается контейнер верхнего уровня в иерархии контейнера.</span><span class="sxs-lookup"><span data-stu-id="ac336-111">If  _lpEntryID_ is set to NULL, the top-level container in the container's hierarchy is opened.</span></span> 
    
 <span data-ttu-id="ac336-112">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="ac336-112">_lpInterface_</span></span>
  
> <span data-ttu-id="ac336-113">[in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, который будет использоваться для доступа к объекту.</span><span class="sxs-lookup"><span data-stu-id="ac336-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="ac336-114">Передача NULL приводит к возвращению идентификатора стандартного интерфейса объекта.</span><span class="sxs-lookup"><span data-stu-id="ac336-114">Passing NULL results in the identifier for the object's standard interface being returned.</span></span> <span data-ttu-id="ac336-115">Для сообщений стандартным интерфейсом является [IMAPIMessageSite : IUnknown;](imapimessagesiteiunknown.md) для папок это [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="ac336-115">For messages, the standard interface is [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md); for folders, it is [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="ac336-116">Стандартными интерфейсами для объектов адресной книги являются [IDistList : IMAPIContainer](idistlistimapicontainer.md) для списка рассылки и [IMailUser : IMAPIProp](imailuserimapiprop.md) для пользователя обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ac336-116">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="ac336-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ac336-117">_ulFlags_</span></span>
  
> <span data-ttu-id="ac336-118">[in] Битоваяmas флагов, которая управляет открытием объекта.</span><span class="sxs-lookup"><span data-stu-id="ac336-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="ac336-119">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="ac336-119">The following flags can be set:</span></span>
    
<span data-ttu-id="ac336-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="ac336-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="ac336-121">Запрашивает открытие объекта с максимальным доступом к сети для пользователя и максимальным доступом клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="ac336-121">Requests that the object will be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="ac336-122">Например, если у клиента есть разрешение на чтение и записи, объект должен быть открыт с разрешением на чтение и записи; если клиент имеет доступ только для чтения, объект должен быть открыт только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ac336-122">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only access, the object should be opened with read-only access.</span></span> 
    
<span data-ttu-id="ac336-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="ac336-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="ac336-124">Позволяет **OpenEntry** успешно возвращаться, возможно, до того, как объект будет полностью доступен вызываемому клиенту.</span><span class="sxs-lookup"><span data-stu-id="ac336-124">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="ac336-125">Если объект не доступен, последующий вызов объекта может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="ac336-125">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="ac336-126">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="ac336-126">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="ac336-127">Запрашивает разрешение на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="ac336-127">Requests read/write permission.</span></span> <span data-ttu-id="ac336-128">По умолчанию объекты открываются с доступом только для чтения, и клиенты не должны работать при предположении, что разрешение на чтение и записи предоставлено.</span><span class="sxs-lookup"><span data-stu-id="ac336-128">By default, objects are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="ac336-129">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="ac336-129">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="ac336-130">Отображает элементы, которые в настоящее время помечены как "мягко удаленные", то есть находятся на этапе хранения удаленных элементов.</span><span class="sxs-lookup"><span data-stu-id="ac336-130">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="ac336-131">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="ac336-131">_lpulObjType_</span></span>
  
> <span data-ttu-id="ac336-132">[out] Указатель на тип открытого объекта.</span><span class="sxs-lookup"><span data-stu-id="ac336-132">[out] A pointer to the opened object's type.</span></span>
    
 <span data-ttu-id="ac336-133">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="ac336-133">_lppUnk_</span></span>
  
> <span data-ttu-id="ac336-134">[out] Указатель на указатель на реализацию интерфейса для доступа к открытому объекту.</span><span class="sxs-lookup"><span data-stu-id="ac336-134">[out] A pointer to a pointer to the interface implementation to use to access the open object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ac336-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac336-135">Return value</span></span>

<span data-ttu-id="ac336-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac336-136">S_OK</span></span> 
  
> <span data-ttu-id="ac336-137">Объект успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="ac336-137">The object was successfully opened.</span></span>
    
<span data-ttu-id="ac336-138">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="ac336-138">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="ac336-139">Либо у пользователя недостаточно разрешений на открытие объекта, либо попытка открыть объект только для чтения с разрешением на чтение и написание.</span><span class="sxs-lookup"><span data-stu-id="ac336-139">Either the user has insufficient permissions to open the object or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="ac336-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ac336-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ac336-141">Идентификатор записи, указанный  _lpEntryID,_ не представляет объект.</span><span class="sxs-lookup"><span data-stu-id="ac336-141">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="ac336-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ac336-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="ac336-143">Идентификатор записи в параметре  _lpEntryID_ не имеет формата, распознаемого контейнером.</span><span class="sxs-lookup"><span data-stu-id="ac336-143">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ac336-144">Примечания</span><span class="sxs-lookup"><span data-stu-id="ac336-144">Remarks</span></span>

<span data-ttu-id="ac336-145">Метод **IMAPIContainer::OpenEntry** открывает объект во всем контейнере и возвращает указатель на реализацию интерфейса для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="ac336-145">The **IMAPIContainer::OpenEntry** method opens an object throughout a container and returns a pointer to an interface implementation to use for further access.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ac336-146">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="ac336-146">Notes to callers</span></span>

<span data-ttu-id="ac336-147">Так как поставщики служб не обязаны возвращать реализацию интерфейса типа, указанного идентификатором интерфейса в параметре _lpInterface,_ проверьте значение, указанное параметром _lpulObjType._</span><span class="sxs-lookup"><span data-stu-id="ac336-147">Because service providers are not required to return an interface implementation of the type specified by the interface identifier in the  _lpInterface_ parameter, check the value pointed to by the  _lpulObjType_ parameter.</span></span> <span data-ttu-id="ac336-148">При необходимости приведите указатель, возвращенный  _lppUnk,_ к указателю соответствующего типа.</span><span class="sxs-lookup"><span data-stu-id="ac336-148">If necessary, cast the pointer returned in  _lppUnk_ to a pointer of the appropriate type.</span></span> 
  
<span data-ttu-id="ac336-149">По умолчанию поставщики услуг открывают объекты с доступом только для чтения, если вы не MAPI_MODIFY или MAPI_BEST_ACCESS флаг.</span><span class="sxs-lookup"><span data-stu-id="ac336-149">By default, service providers open objects with read-only access unless you set either the MAPI_MODIFY or MAPI_BEST_ACCESS flag.</span></span> <span data-ttu-id="ac336-150">Если один из этих флагов установлен, поставщики служб пытаются вернуть изменимый объект.</span><span class="sxs-lookup"><span data-stu-id="ac336-150">When one of these flags is set, service providers attempt to return a modifiable object.</span></span> <span data-ttu-id="ac336-151">Однако не следует предполагать, что из-за запроса модификуемого объекта открытый объект имеет разрешение на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="ac336-151">However, do not assume that because you requested a modifiable object that the opened object has read/write permission.</span></span> <span data-ttu-id="ac336-152">Запланируйте вероятность сбойного последующего изменения или извлекаете свойство **PR_ACCESS_LEVEL** объекта, чтобы определить уровень доступа, предоставленный **OpenEntry.**</span><span class="sxs-lookup"><span data-stu-id="ac336-152">Either plan for the chance of a subsequent modification to fail or retrieve the object's **PR_ACCESS_LEVEL** property to determine the access level granted by **OpenEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ac336-153">См. также</span><span class="sxs-lookup"><span data-stu-id="ac336-153">See also</span></span>



[<span data-ttu-id="ac336-154">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ac336-154">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)

