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
description: 'Последнее изменение: 01 февраля 2013 г.'
ms.openlocfilehash: fa279962043f6f7cb7a134b624000c9c7e65369f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/21/2018
ms.locfileid: "19808771"
---
# <a name="iaddrbookopenentry"></a><span data-ttu-id="4b22b-103">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="4b22b-103">IAddrBook::OpenEntry</span></span>

<span data-ttu-id="4b22b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4b22b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4b22b-105">Открывает запись книги и возвращает указатель на интерфейс, который можно использовать для доступа к операции.</span><span class="sxs-lookup"><span data-stu-id="4b22b-105">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="4b22b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b22b-106">Parameters</span></span>

<span data-ttu-id="4b22b-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="4b22b-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="4b22b-108">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="4b22b-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="4b22b-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="4b22b-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="4b22b-110">[in] Указатель на идентификатор записи, который представляет записи адресной книги, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="4b22b-110">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
<span data-ttu-id="4b22b-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="4b22b-111">_lpInterface_</span></span>
  
> <span data-ttu-id="4b22b-112">[in] Указатель на интерфейс идентификатор (ИД интерфейса) интерфейс, который будет использоваться для доступа к открытой операцией.</span><span class="sxs-lookup"><span data-stu-id="4b22b-112">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="4b22b-113">Передача NULL Возвращает стандартный интерфейс объекта.</span><span class="sxs-lookup"><span data-stu-id="4b22b-113">Passing NULL returns the object's standard interface.</span></span> <span data-ttu-id="4b22b-114">Для пользователей, обмена мгновенными сообщениями, — это стандартный интерфейс [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="4b22b-114">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="4b22b-115">Для списков рассылки — это [IDistList: IMAPIContainer](idistlistimapicontainer.md) и для контейнеров, это [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="4b22b-115">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md) and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="4b22b-116">Вызывающие объекты можно задать _lpInterface_ соответствующий стандартный интерфейс или интерфейс в иерархии наследования.</span><span class="sxs-lookup"><span data-stu-id="4b22b-116">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
<span data-ttu-id="4b22b-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4b22b-117">_ulFlags_</span></span>
  
> <span data-ttu-id="4b22b-118">[in] Битовая маска флаги, который определяет, как открыть запись.</span><span class="sxs-lookup"><span data-stu-id="4b22b-118">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="4b22b-119">Можно задать следующие флаги.</span><span class="sxs-lookup"><span data-stu-id="4b22b-119">The following flags can be set.</span></span>
    
<span data-ttu-id="4b22b-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="4b22b-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="4b22b-121">Запросы, что операция открываются с максимальное допустимое разрешения сети и клиента.</span><span class="sxs-lookup"><span data-stu-id="4b22b-121">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="4b22b-122">Например если клиент имеет разрешение на чтение и запись, поставщик адресной книги следует попытаться открыть запись с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="4b22b-122">For example, if the client has read/write permission, the address book provider should attempt to open the entry with read/write permission.</span></span> <span data-ttu-id="4b22b-123">Можно получить уровень доступа, который был предоставлен путем вызова метода open запись [IMAPIProp::GetProps](imapiprop-getprops.md) и извлечение свойства **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4b22b-123">The client can retrieve the access level that was granted by calling the open entry's [IMAPIProp::GetProps](imapiprop-getprops.md) method and retrieving the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="4b22b-124">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="4b22b-124">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="4b22b-125">Открывает запись книги и обращается к нему только из кэша.</span><span class="sxs-lookup"><span data-stu-id="4b22b-125">Opens an address book entry and accesses it only from the cache.</span></span> <span data-ttu-id="4b22b-126">Например можно использовать этот флаг позволяет открыть глобальный список адресов (GAL) в режиме кэширования данных exchange и получить доступ к записи в этот список адресов из кэша без создания трафика между клиентом и сервером клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="4b22b-126">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="4b22b-127">Этот флаг поддерживается только поставщик Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="4b22b-127">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="4b22b-128">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="4b22b-128">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="4b22b-129">Разрешает вызов для успешного выполнения, потенциально перед словом полностью open и доступны, подразумевает, что более поздние вызовов записи могут завершиться ошибкой.</span><span class="sxs-lookup"><span data-stu-id="4b22b-129">Allows the call to succeed, potentially before the entry is fully open and available, implying that later calls to the entry might return an error.</span></span>
    
<span data-ttu-id="4b22b-130">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="4b22b-130">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="4b22b-131">Для выполнения разрешения имен используйте только глобальный список адресов.</span><span class="sxs-lookup"><span data-stu-id="4b22b-131">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="4b22b-132">Этот флаг поддерживается только поставщик Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="4b22b-132">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="4b22b-133">_UlFlags_ MAPI_GAL_ONLY не могут быть определены в файле загружаемых заголовка в настоящий момент, в этом случае можно добавить его в код с помощью следующее значение: >`#define MAPI_GAL_ONLY (0x00000080)`</span><span class="sxs-lookup"><span data-stu-id="4b22b-133">The  _ulFlags_ MAPI_GAL_ONLY might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define MAPI_GAL_ONLY (0x00000080)`</span></span>
  
<span data-ttu-id="4b22b-134">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="4b22b-134">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="4b22b-135">Запросы, которые словом открывать с разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="4b22b-135">Requests that the entry be opened with read/write permission.</span></span> <span data-ttu-id="4b22b-136">Поскольку записи открываются с доступом только для чтения по умолчанию, клиенты не следует предполагать, независимо от того, является ли MAPI_MODIFY имеет значение были предоставлены разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="4b22b-136">Because entries are opened with read-only access by default, clients should not assume that read/write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="4b22b-137">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="4b22b-137">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="4b22b-138">Не используйте автономной адресной книги для разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="4b22b-138">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="4b22b-139">Этот флаг поддерживается только поставщик Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="4b22b-139">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="4b22b-140">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="4b22b-140">_lpulObjType_</span></span>
  
> <span data-ttu-id="4b22b-141">[out] Указатель на тип открыт записи.</span><span class="sxs-lookup"><span data-stu-id="4b22b-141">[out] A pointer to the type of the opened entry.</span></span>
    
<span data-ttu-id="4b22b-142">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="4b22b-142">_lppUnk_</span></span>
  
> <span data-ttu-id="4b22b-143">[out] Указатель на указатель открыт записи.</span><span class="sxs-lookup"><span data-stu-id="4b22b-143">[out] A pointer to a pointer to the opened entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4b22b-144">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="4b22b-144">Return value</span></span>

<span data-ttu-id="4b22b-145">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="4b22b-145">S_OK</span></span> 
  
> <span data-ttu-id="4b22b-146">Операция успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="4b22b-146">The entry was successfully opened.</span></span>
    
<span data-ttu-id="4b22b-147">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="4b22b-147">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="4b22b-148">Предпринята попытка открыть запись, для которой пользователь имеет недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="4b22b-148">An attempt was made to open an entry for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="4b22b-149">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="4b22b-149">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="4b22b-150">Запись, представленного _lpEntryID_ не существует.</span><span class="sxs-lookup"><span data-stu-id="4b22b-150">The entry represented by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="4b22b-151">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4b22b-151">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="4b22b-152">Идентификатор записи, указанной в _lpEntryID_ не распознается.</span><span class="sxs-lookup"><span data-stu-id="4b22b-152">The entry identifier specified in  _lpEntryID_ is not recognized.</span></span> <span data-ttu-id="4b22b-153">Это значение возвращается как правило, если поставщик адресной книги, ответственный за запись не открыта.</span><span class="sxs-lookup"><span data-stu-id="4b22b-153">This value is typically returned if the address book provider responsible for the corresponding entry is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4b22b-154">Замечания</span><span class="sxs-lookup"><span data-stu-id="4b22b-154">Remarks</span></span>

<span data-ttu-id="4b22b-155">Клиенты и поставщики услуг вызовите метод **IAddrBook::OpenEntry** для открытия записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="4b22b-155">Clients and service providers call the **IAddrBook::OpenEntry** method to open an address book entry.</span></span> <span data-ttu-id="4b22b-156">MAPI перенаправляет вызов соответствующего доступа к адресной книге, на основе структуры [MAPIUID](mapiuid.md) , включенные в идентификатор записи, переданной в параметре _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="4b22b-156">MAPI forwards the call to the appropriate address book provider, based on the [MAPIUID](mapiuid.md) structure included in the entry identifier passed in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="4b22b-157">Поставщик адресной книги открывает записи с доступом только для чтения, если не задан флаг MAPI_MODIFY или MAPI_BEST_ACCESS с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="4b22b-157">The address book provider opens the entry as read-only unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter is set.</span></span> <span data-ttu-id="4b22b-158">Тем не менее эти флаги, предложения.</span><span class="sxs-lookup"><span data-stu-id="4b22b-158">However, these flags are suggestions.</span></span> <span data-ttu-id="4b22b-159">Если поставщик адресной книги не допускает изменения для записи в запросе, возвращается MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="4b22b-159">If the address book provider does not allow modification for the entry requested, it returns MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="4b22b-160">Параметр _lpInterface_ указывает интерфейс, который должен использоваться для доступа к открытой записи.</span><span class="sxs-lookup"><span data-stu-id="4b22b-160">The  _lpInterface_ parameter indicates which interface should be used to access the opened entry.</span></span> <span data-ttu-id="4b22b-161">Указать значение NULL для _lpInterface_ указывает, что следует использовать стандартный интерфейс MAPI для этого типа записи.</span><span class="sxs-lookup"><span data-stu-id="4b22b-161">Passing NULL in  _lpInterface_ indicates the standard MAPI interface for that type of entry should be used.</span></span> <span data-ttu-id="4b22b-162">Так как поставщик адресной книги может вернуть другой интерфейс, отличной от предложенных с помощью параметра _lpInterface_ , вызывающий объект должен проверить, значение, возвращенное в параметре _lpulObjType_ , чтобы определить, является ли тип объекта, возвращенного ожидаемым.</span><span class="sxs-lookup"><span data-stu-id="4b22b-162">Because the address book provider might return a different interface than the one suggested by the  _lpInterface_ parameter, the caller should check the value returned in the  _lpulObjType_ parameter to determine whether the object type returned is what was expected.</span></span> <span data-ttu-id="4b22b-163">Если тип объекта не типа, вызывающего можно привести параметр _lppUnk_ в тип, который является более корректно.</span><span class="sxs-lookup"><span data-stu-id="4b22b-163">If the object type is not of the type expected, the caller can cast the  _lppUnk_ parameter to a type that is more appropriate.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4b22b-164">См. также</span><span class="sxs-lookup"><span data-stu-id="4b22b-164">See also</span></span>

- [<span data-ttu-id="4b22b-165">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4b22b-165">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

