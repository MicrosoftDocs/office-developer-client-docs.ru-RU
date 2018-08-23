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
ms.openlocfilehash: cd93866ae8823eb5897318fc2dda4e8432d974b0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578467"
---
# <a name="imapicontaineropenentry"></a><span data-ttu-id="928bb-103">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="928bb-103">IMAPIContainer::OpenEntry</span></span>

  
  
<span data-ttu-id="928bb-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="928bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="928bb-105">Открывает объект в контейнере, возвращает указатель интерфейса для дальнейшей доступа.</span><span class="sxs-lookup"><span data-stu-id="928bb-105">Opens an object in the container, returning an interface pointer for further access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="928bb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="928bb-106">Parameters</span></span>

 <span data-ttu-id="928bb-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="928bb-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="928bb-108">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="928bb-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="928bb-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="928bb-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="928bb-110">[in] Указатель на запись идентификатор объекта для открытия.</span><span class="sxs-lookup"><span data-stu-id="928bb-110">[in] A pointer to the entry identifier of the object to open.</span></span> <span data-ttu-id="928bb-111">Если _lpEntryID_ имеет значение NULL, открывается контейнером верхнего уровня в иерархии контейнеров.</span><span class="sxs-lookup"><span data-stu-id="928bb-111">If  _lpEntryID_ is set to NULL, the top-level container in the container's hierarchy is opened.</span></span> 
    
 <span data-ttu-id="928bb-112">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="928bb-112">_lpInterface_</span></span>
  
> <span data-ttu-id="928bb-113">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к объекту.</span><span class="sxs-lookup"><span data-stu-id="928bb-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="928bb-114">В идентификатор для объекта стандартный интерфейс, возвращаемых результатов передаче значения NULL.</span><span class="sxs-lookup"><span data-stu-id="928bb-114">Passing NULL results in the identifier for the object's standard interface being returned.</span></span> <span data-ttu-id="928bb-115">Для сообщений, — это стандартный интерфейс [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md); для папок, это [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="928bb-115">For messages, the standard interface is [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md); for folders, it is [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="928bb-116">Стандартные интерфейсы для объектов адресной книги [IDistList: IMAPIContainer](idistlistimapicontainer.md) для списка рассылки и [IMailUser: IMAPIProp](imailuserimapiprop.md) для обмена сообщениями пользователя.</span><span class="sxs-lookup"><span data-stu-id="928bb-116">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="928bb-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="928bb-117">_ulFlags_</span></span>
  
> <span data-ttu-id="928bb-118">[in] Битовая маска флаги, который определяет способ открытия объекта.</span><span class="sxs-lookup"><span data-stu-id="928bb-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="928bb-119">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="928bb-119">The following flags can be set:</span></span>
    
<span data-ttu-id="928bb-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="928bb-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="928bb-121">Запросы, что объект будет открыт с разрешениями максимальное сети, разрешенных для пользователя и приложения максимальное клиентского доступа.</span><span class="sxs-lookup"><span data-stu-id="928bb-121">Requests that the object will be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="928bb-122">Например если клиент имеет разрешение на чтение и запись, объект должен быть открыт получившие разрешение на чтение и запись; Если клиент имеет доступ только для чтения, объект должен быть открыт с доступом только для чтения.</span><span class="sxs-lookup"><span data-stu-id="928bb-122">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only access, the object should be opened with read-only access.</span></span> 
    
<span data-ttu-id="928bb-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="928bb-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="928bb-124">Позволяет **OpenEntry** для возврата успешно, возможно перед объект полностью доступен для клиента.</span><span class="sxs-lookup"><span data-stu-id="928bb-124">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="928bb-125">Если объект недоступен, вызов последующих объектов может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="928bb-125">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="928bb-126">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="928bb-126">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="928bb-127">Запросы на разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="928bb-127">Requests read/write permission.</span></span> <span data-ttu-id="928bb-128">По умолчанию объекты открываются с доступом только для чтения, и клиенты не должны работать предполагается, что чтение и запись, назначено разрешение.</span><span class="sxs-lookup"><span data-stu-id="928bb-128">By default, objects are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="928bb-129">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="928bb-129">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="928bb-130">Отображает элементы, которые в настоящее время помечены как программных удалены, то есть, они находятся в хранения удаленных элементов этап времени.</span><span class="sxs-lookup"><span data-stu-id="928bb-130">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="928bb-131">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="928bb-131">_lpulObjType_</span></span>
  
> <span data-ttu-id="928bb-132">[out] Указатель на тип открытого объекта.</span><span class="sxs-lookup"><span data-stu-id="928bb-132">[out] A pointer to the opened object's type.</span></span>
    
 <span data-ttu-id="928bb-133">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="928bb-133">_lppUnk_</span></span>
  
> <span data-ttu-id="928bb-134">[out] Указатель на указатель на реализации интерфейса для доступа к объекту open.</span><span class="sxs-lookup"><span data-stu-id="928bb-134">[out] A pointer to a pointer to the interface implementation to use to access the open object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="928bb-135">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="928bb-135">Return value</span></span>

<span data-ttu-id="928bb-136">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="928bb-136">S_OK</span></span> 
  
> <span data-ttu-id="928bb-137">Объект был успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="928bb-137">The object was successfully opened.</span></span>
    
<span data-ttu-id="928bb-138">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="928bb-138">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="928bb-139">Либо пользователь не имеет разрешений на открытие объекта или попытка открыть объект только для чтения с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="928bb-139">Either the user has insufficient permissions to open the object or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="928bb-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="928bb-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="928bb-141">Идентификатор записи, указанного идентификатором _lpEntryID_ не представляет объект.</span><span class="sxs-lookup"><span data-stu-id="928bb-141">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="928bb-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="928bb-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="928bb-143">Идентификатор записи в параметре _lpEntryID_ не распознаваемых контейнер формата.</span><span class="sxs-lookup"><span data-stu-id="928bb-143">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="928bb-144">Замечания</span><span class="sxs-lookup"><span data-stu-id="928bb-144">Remarks</span></span>

<span data-ttu-id="928bb-145">Метод **IMAPIContainer::OpenEntry** открывает объект во всем контейнером и возвращает указатель на реализацию интерфейса для дальнейшей доступа.</span><span class="sxs-lookup"><span data-stu-id="928bb-145">The **IMAPIContainer::OpenEntry** method opens an object throughout a container and returns a pointer to an interface implementation to use for further access.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="928bb-146">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="928bb-146">Notes to callers</span></span>

<span data-ttu-id="928bb-147">Так как для возврата реализация интерфейса типа, указанного идентификатором интерфейса с помощью параметра _lpInterface_ не требуется поставщиков услуг, проверьте значение указывает параметр _lpulObjType_ .</span><span class="sxs-lookup"><span data-stu-id="928bb-147">Because service providers are not required to return an interface implementation of the type specified by the interface identifier in the  _lpInterface_ parameter, check the value pointed to by the  _lpulObjType_ parameter.</span></span> <span data-ttu-id="928bb-148">При необходимости привести указатель, возвращаемых в _lppUnk_ указатель соответствующего типа.</span><span class="sxs-lookup"><span data-stu-id="928bb-148">If necessary, cast the pointer returned in  _lppUnk_ to a pointer of the appropriate type.</span></span> 
  
<span data-ttu-id="928bb-149">По умолчанию поставщиков услуг открыть объекты с доступом только для чтения, если не задан параметр MAPI_MODIFY или MAPI_BEST_ACCESS флаг.</span><span class="sxs-lookup"><span data-stu-id="928bb-149">By default, service providers open objects with read-only access unless you set either the MAPI_MODIFY or MAPI_BEST_ACCESS flag.</span></span> <span data-ttu-id="928bb-150">Если один из этих флагов возвратить объект можно изменить попытаться поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="928bb-150">When one of these flags is set, service providers attempt to return a modifiable object.</span></span> <span data-ttu-id="928bb-151">Тем не менее не следует считать, потому что вы запросили изменяемый объект, что открыт объект имеет разрешение на чтение/запись.</span><span class="sxs-lookup"><span data-stu-id="928bb-151">However, do not assume that because you requested a modifiable object that the opened object has read/write permission.</span></span> <span data-ttu-id="928bb-152">Либо планирование вероятность последующие изменения не работают или получить свойство **PR_ACCESS_LEVEL** объекта для определения уровня доступа предоставляются по **OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="928bb-152">Either plan for the chance of a subsequent modification to fail or retrieve the object's **PR_ACCESS_LEVEL** property to determine the access level granted by **OpenEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="928bb-153">См. также</span><span class="sxs-lookup"><span data-stu-id="928bb-153">See also</span></span>



[<span data-ttu-id="928bb-154">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="928bb-154">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)

