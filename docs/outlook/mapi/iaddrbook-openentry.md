---
title: IAddrBookOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.OpenEntry
api_type:
- COM
ms.assetid: bd7746f4-8070-4cc5-8b8e-c527c5847545
description: 'Дата последнего изменения: 1 февраля 2013 г.'
ms.openlocfilehash: 293fe5a65c760f61ab0073e0eafc1a606c69050f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434167"
---
# <a name="iaddrbookopenentry"></a><span data-ttu-id="6ef79-103">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="6ef79-103">IAddrBook::OpenEntry</span></span>

<span data-ttu-id="6ef79-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ef79-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ef79-105">Открывает запись адресной книги и возвращает указатель в интерфейс, который можно использовать для доступа к записи.</span><span class="sxs-lookup"><span data-stu-id="6ef79-105">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="6ef79-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6ef79-106">Parameters</span></span>

<span data-ttu-id="6ef79-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="6ef79-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="6ef79-108">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="6ef79-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="6ef79-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="6ef79-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="6ef79-110">[in] Указатель на идентификатор записи, который представляет открытую запись адресной книги.</span><span class="sxs-lookup"><span data-stu-id="6ef79-110">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
<span data-ttu-id="6ef79-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="6ef79-111">_lpInterface_</span></span>
  
> <span data-ttu-id="6ef79-112">[in] Указатель на идентификатор интерфейса (IID) интерфейса, который будет использоваться для доступа к открытой записи.</span><span class="sxs-lookup"><span data-stu-id="6ef79-112">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="6ef79-113">Передача NULL возвращает стандартный интерфейс объекта.</span><span class="sxs-lookup"><span data-stu-id="6ef79-113">Passing NULL returns the object's standard interface.</span></span> <span data-ttu-id="6ef79-114">Для пользователей обмена сообщениями стандартным интерфейсом [является IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="6ef79-114">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="6ef79-115">Для списков рассылки это [IDistList: IMAPIContainer,](idistlistimapicontainer.md) а для контейнеров — [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="6ef79-115">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md) and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="6ef79-116">Звонители могут настроить  _lpInterface_ для соответствующего стандартного интерфейса или интерфейса в иерархии наследования.</span><span class="sxs-lookup"><span data-stu-id="6ef79-116">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
<span data-ttu-id="6ef79-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6ef79-117">_ulFlags_</span></span>
  
> <span data-ttu-id="6ef79-118">[in] Битмашка флагов, контролируемая тем, как открывается запись.</span><span class="sxs-lookup"><span data-stu-id="6ef79-118">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="6ef79-119">Можно установить следующие флаги.</span><span class="sxs-lookup"><span data-stu-id="6ef79-119">The following flags can be set.</span></span>
    
<span data-ttu-id="6ef79-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="6ef79-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="6ef79-121">Запросы на открытие записи с максимально разрешенными сетевыми и клиентными разрешениями.</span><span class="sxs-lookup"><span data-stu-id="6ef79-121">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="6ef79-122">Например, если у клиента есть разрешение на чтение и запись, поставщик адресной книги должен попытаться открыть запись с разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="6ef79-122">For example, if the client has read/write permission, the address book provider should attempt to open the entry with read/write permission.</span></span> <span data-ttu-id="6ef79-123">Клиент может получить уровень доступа, который был предоставлен путем вызова метода [IMAPIProp::GetProps](imapiprop-getprops.md) открытой записи и получения свойства[PR_ACCESS_LEVEL (PidTagAccessLevel).](pidtagaccesslevel-canonical-property.md) </span><span class="sxs-lookup"><span data-stu-id="6ef79-123">The client can retrieve the access level that was granted by calling the open entry's [IMAPIProp::GetProps](imapiprop-getprops.md) method and retrieving the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="6ef79-124">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="6ef79-124">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="6ef79-125">Открывает запись адресной книги и обращается к ней только из кэша.</span><span class="sxs-lookup"><span data-stu-id="6ef79-125">Opens an address book entry and accesses it only from the cache.</span></span> <span data-ttu-id="6ef79-126">Например, этот флаг можно использовать, чтобы разрешить клиентской приложению открывать глобальный список адресов (GAL) в кэшном режиме обмена и получать доступ к записи в этой адресной книге из кэша без создания трафика между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="6ef79-126">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="6ef79-127">Этот флаг поддерживается только поставщиком Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="6ef79-127">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="6ef79-128">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="6ef79-128">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="6ef79-129">Позволяет добиться успеха вызова, потенциально до того, как запись будет полностью открыта и доступна, что означает, что более поздние вызовы в запись могут привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="6ef79-129">Allows the call to succeed, potentially before the entry is fully open and available, implying that later calls to the entry might return an error.</span></span>
    
<span data-ttu-id="6ef79-130">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="6ef79-130">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="6ef79-131">Для выполнения разрешения имен используйте только GAL.</span><span class="sxs-lookup"><span data-stu-id="6ef79-131">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="6ef79-132">Этот флаг поддерживается только поставщиком Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="6ef79-132">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="6ef79-133">Значение  _ulFlags_ MAPI_GAL_ONLY не может быть определено в загружаемом файле заголовки, в котором вы в настоящее время имеете, и в этом случае его можно добавить в код, используя следующее значение: >  `#define MAPI_GAL_ONLY (0x00000080)`</span><span class="sxs-lookup"><span data-stu-id="6ef79-133">The  _ulFlags_ MAPI_GAL_ONLY might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define MAPI_GAL_ONLY (0x00000080)`</span></span>
  
<span data-ttu-id="6ef79-134">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="6ef79-134">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="6ef79-135">Запросы на открытие записи с разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="6ef79-135">Requests that the entry be opened with read/write permission.</span></span> <span data-ttu-id="6ef79-136">Поскольку записи открываются с доступом только для чтения по умолчанию, клиенты не должны предполагать, что разрешение на чтение и запись было предоставлено независимо от того, MAPI_MODIFY установлено.</span><span class="sxs-lookup"><span data-stu-id="6ef79-136">Because entries are opened with read-only access by default, clients should not assume that read/write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="6ef79-137">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="6ef79-137">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="6ef79-138">Не используйте офлайн-адресную книгу для выполнения разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="6ef79-138">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="6ef79-139">Этот флаг поддерживается только поставщиком Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="6ef79-139">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="6ef79-140">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="6ef79-140">_lpulObjType_</span></span>
  
> <span data-ttu-id="6ef79-141">[вышел] Указатель на тип открываемой записи.</span><span class="sxs-lookup"><span data-stu-id="6ef79-141">[out] A pointer to the type of the opened entry.</span></span>
    
<span data-ttu-id="6ef79-142">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="6ef79-142">_lppUnk_</span></span>
  
> <span data-ttu-id="6ef79-143">[вышел] Указатель на указатель на открытую запись.</span><span class="sxs-lookup"><span data-stu-id="6ef79-143">[out] A pointer to a pointer to the opened entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6ef79-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ef79-144">Return value</span></span>

<span data-ttu-id="6ef79-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="6ef79-145">S_OK</span></span> 
  
> <span data-ttu-id="6ef79-146">Запись была успешно открыта.</span><span class="sxs-lookup"><span data-stu-id="6ef79-146">The entry was successfully opened.</span></span>
    
<span data-ttu-id="6ef79-147">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="6ef79-147">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="6ef79-148">Была предпринята попытка открыть запись, для которой у пользователя недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="6ef79-148">An attempt was made to open an entry for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="6ef79-149">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="6ef79-149">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="6ef79-150">Запись, представленная  _lpEntryID,_ не существует.</span><span class="sxs-lookup"><span data-stu-id="6ef79-150">The entry represented by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="6ef79-151">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="6ef79-151">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="6ef79-152">Идентификатор записи, указанный в  _lpEntryID,_ не распознается.</span><span class="sxs-lookup"><span data-stu-id="6ef79-152">The entry identifier specified in  _lpEntryID_ is not recognized.</span></span> <span data-ttu-id="6ef79-153">Обычно это значение возвращается, если поставщик адресной книги, ответственный за соответствующую запись, не открыт.</span><span class="sxs-lookup"><span data-stu-id="6ef79-153">This value is typically returned if the address book provider responsible for the corresponding entry is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6ef79-154">Примечания</span><span class="sxs-lookup"><span data-stu-id="6ef79-154">Remarks</span></span>

<span data-ttu-id="6ef79-155">Клиенты и поставщики услуг звонят по методу **IAddrBook::OpenEntry,** чтобы открыть запись адресной книги.</span><span class="sxs-lookup"><span data-stu-id="6ef79-155">Clients and service providers call the **IAddrBook::OpenEntry** method to open an address book entry.</span></span> <span data-ttu-id="6ef79-156">MAPI передает вызов соответствующему поставщику адресной книги на основе структуры [MAPIUID,](mapiuid.md) включенной в идентификатор входа, переданный в _параметре lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="6ef79-156">MAPI forwards the call to the appropriate address book provider, based on the [MAPIUID](mapiuid.md) structure included in the entry identifier passed in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="6ef79-157">Поставщик адресной книги открывает запись только для чтения, если MAPI_MODIFY или MAPI_BEST_ACCESS в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="6ef79-157">The address book provider opens the entry as read-only unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter is set.</span></span> <span data-ttu-id="6ef79-158">Однако эти флаги являются предложениями.</span><span class="sxs-lookup"><span data-stu-id="6ef79-158">However, these flags are suggestions.</span></span> <span data-ttu-id="6ef79-159">Если поставщик адресной книги не разрешает изменение запрашиваемой записи, он возвращает MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="6ef79-159">If the address book provider does not allow modification for the entry requested, it returns MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="6ef79-160">Параметр  _lpInterface указывает,_ какой интерфейс следует использовать для доступа к открытой записи.</span><span class="sxs-lookup"><span data-stu-id="6ef79-160">The  _lpInterface_ parameter indicates which interface should be used to access the opened entry.</span></span> <span data-ttu-id="6ef79-161">Передача NULL в  _lpInterface_ указывает на стандартный интерфейс MAPI для этого типа записи.</span><span class="sxs-lookup"><span data-stu-id="6ef79-161">Passing NULL in  _lpInterface_ indicates the standard MAPI interface for that type of entry should be used.</span></span> <span data-ttu-id="6ef79-162">Так как поставщик адресной книги может возвращать другой интерфейс, чем тот, который предлагается параметром  _lpInterface,_ вызываемая должна проверить значение, возвращенное в  _параметре lpulObjType,_ чтобы определить, является ли возвращенный тип объекта ожидаемым.</span><span class="sxs-lookup"><span data-stu-id="6ef79-162">Because the address book provider might return a different interface than the one suggested by the  _lpInterface_ parameter, the caller should check the value returned in the  _lpulObjType_ parameter to determine whether the object type returned is what was expected.</span></span> <span data-ttu-id="6ef79-163">Если тип объекта не является ожидаемым, вызываемая может отозвать параметр  _lppUnk_ к типу, который является более подходящим.</span><span class="sxs-lookup"><span data-stu-id="6ef79-163">If the object type is not of the type expected, the caller can cast the  _lppUnk_ parameter to a type that is more appropriate.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6ef79-164">См. также</span><span class="sxs-lookup"><span data-stu-id="6ef79-164">See also</span></span>

- [<span data-ttu-id="6ef79-165">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6ef79-165">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

