---
title: иаддрбукопенентри
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
# <a name="iaddrbookopenentry"></a><span data-ttu-id="93a6f-103">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="93a6f-103">IAddrBook::OpenEntry</span></span>

<span data-ttu-id="93a6f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93a6f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93a6f-105">Открывает запись адресной книги и возвращает указатель на интерфейс, который можно использовать для доступа к записи.</span><span class="sxs-lookup"><span data-stu-id="93a6f-105">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="93a6f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="93a6f-106">Parameters</span></span>

<span data-ttu-id="93a6f-107">_кбентрид_</span><span class="sxs-lookup"><span data-stu-id="93a6f-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="93a6f-108">возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="93a6f-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="93a6f-109">_лпентрид_</span><span class="sxs-lookup"><span data-stu-id="93a6f-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="93a6f-110">возврата Указатель на идентификатор записи, представляющий запись адресной книги, которую требуется открыть.</span><span class="sxs-lookup"><span data-stu-id="93a6f-110">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
<span data-ttu-id="93a6f-111">_лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="93a6f-111">_lpInterface_</span></span>
  
> <span data-ttu-id="93a6f-112">возврата Указатель на идентификатор интерфейса (IID) интерфейса, который будет использоваться для доступа к открытой записи.</span><span class="sxs-lookup"><span data-stu-id="93a6f-112">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="93a6f-113">При передаче значения NULL возвращается стандартный интерфейс объекта.</span><span class="sxs-lookup"><span data-stu-id="93a6f-113">Passing NULL returns the object's standard interface.</span></span> <span data-ttu-id="93a6f-114">Для пользователей обмена сообщениями стандартный интерфейс — [имаилусер: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="93a6f-114">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="93a6f-115">Для списков рассылки это [идистлист: IMAPIContainer](idistlistimapicontainer.md) и для контейнеров, [иабконтаинер: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="93a6f-115">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md) and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="93a6f-116">Вызывающие абоненты могут установить _лпинтерфаце_ в соответствии со стандартным интерфейсом или интерфейсом в иерархии наследования.</span><span class="sxs-lookup"><span data-stu-id="93a6f-116">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
<span data-ttu-id="93a6f-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="93a6f-117">_ulFlags_</span></span>
  
> <span data-ttu-id="93a6f-118">возврата Битовая маска флагов, определяющих способ открытия записи.</span><span class="sxs-lookup"><span data-stu-id="93a6f-118">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="93a6f-119">Можно задать следующие флаги.</span><span class="sxs-lookup"><span data-stu-id="93a6f-119">The following flags can be set.</span></span>
    
<span data-ttu-id="93a6f-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="93a6f-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="93a6f-121">Запрашивает открытие записи с максимальным количеством разрешенных сетевых и клиентских разрешений.</span><span class="sxs-lookup"><span data-stu-id="93a6f-121">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="93a6f-122">Например, если у клиента есть разрешение на чтение и запись, поставщик адресной книги должен попытаться открыть запись с разрешениями на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="93a6f-122">For example, if the client has read/write permission, the address book provider should attempt to open the entry with read/write permission.</span></span> <span data-ttu-id="93a6f-123">Клиент может получить уровень доступа, предоставленный, вызвав метод [IMAPIProp::-PROPS](imapiprop-getprops.md) открытой записи и извлекая свойство **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="93a6f-123">The client can retrieve the access level that was granted by calling the open entry's [IMAPIProp::GetProps](imapiprop-getprops.md) method and retrieving the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="93a6f-124">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="93a6f-124">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="93a6f-125">Открывает запись адресной книги и обращается к ней только из кэша.</span><span class="sxs-lookup"><span data-stu-id="93a6f-125">Opens an address book entry and accesses it only from the cache.</span></span> <span data-ttu-id="93a6f-126">Например, вы можете использовать этот флаг, чтобы разрешить клиентскому приложению открывать глобальный список адресов (GAL) в режиме кэширования Exchange и получать доступ к записи в этой адресной книге из кэша, не создавая трафик между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="93a6f-126">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="93a6f-127">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="93a6f-127">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="93a6f-128">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="93a6f-128">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="93a6f-129">Разрешает успешный вызов, потенциально перед тем, как запись будет полностью открыта и доступна, подразумевая, что последующие вызовы записи могут возвращать ошибку.</span><span class="sxs-lookup"><span data-stu-id="93a6f-129">Allows the call to succeed, potentially before the entry is fully open and available, implying that later calls to the entry might return an error.</span></span>
    
<span data-ttu-id="93a6f-130">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="93a6f-130">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="93a6f-131">Для разрешения имен используйте только глобальный список адресов.</span><span class="sxs-lookup"><span data-stu-id="93a6f-131">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="93a6f-132">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="93a6f-132">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="93a6f-133">MAPI_GAL_ONLY _ulFlags_ могут быть не определены в текущем загружаемом файле заголовков, в этом случае вы можете добавить его в код, используя следующее значение: >`#define MAPI_GAL_ONLY (0x00000080)`</span><span class="sxs-lookup"><span data-stu-id="93a6f-133">The  _ulFlags_ MAPI_GAL_ONLY might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define MAPI_GAL_ONLY (0x00000080)`</span></span>
  
<span data-ttu-id="93a6f-134">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="93a6f-134">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="93a6f-135">Запрашивает открытие записи с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="93a6f-135">Requests that the entry be opened with read/write permission.</span></span> <span data-ttu-id="93a6f-136">Так как записи открываются с доступом только для чтения по умолчанию, клиенты не должны предполагать, что разрешение на чтение и запись предоставлено независимо от того, задано ли MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="93a6f-136">Because entries are opened with read-only access by default, clients should not assume that read/write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="93a6f-137">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="93a6f-137">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="93a6f-138">Не используйте автономную адресную книгу для разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="93a6f-138">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="93a6f-139">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="93a6f-139">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="93a6f-140">_лпулобжтипе_</span><span class="sxs-lookup"><span data-stu-id="93a6f-140">_lpulObjType_</span></span>
  
> <span data-ttu-id="93a6f-141">вышли Указатель на тип открытого элемента.</span><span class="sxs-lookup"><span data-stu-id="93a6f-141">[out] A pointer to the type of the opened entry.</span></span>
    
<span data-ttu-id="93a6f-142">_лппунк_</span><span class="sxs-lookup"><span data-stu-id="93a6f-142">_lppUnk_</span></span>
  
> <span data-ttu-id="93a6f-143">вышли Указатель на указатель на открытую запись.</span><span class="sxs-lookup"><span data-stu-id="93a6f-143">[out] A pointer to a pointer to the opened entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="93a6f-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="93a6f-144">Return value</span></span>

<span data-ttu-id="93a6f-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="93a6f-145">S_OK</span></span> 
  
> <span data-ttu-id="93a6f-146">Запись успешно открыта.</span><span class="sxs-lookup"><span data-stu-id="93a6f-146">The entry was successfully opened.</span></span>
    
<span data-ttu-id="93a6f-147">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="93a6f-147">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="93a6f-148">Предпринята попытка открыть запись, для которой у пользователя недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="93a6f-148">An attempt was made to open an entry for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="93a6f-149">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="93a6f-149">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="93a6f-150">Запись, представленная _лпентрид_ , не существует.</span><span class="sxs-lookup"><span data-stu-id="93a6f-150">The entry represented by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="93a6f-151">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="93a6f-151">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="93a6f-152">Идентификатор записи, указанный в _лпентрид_ , не распознается.</span><span class="sxs-lookup"><span data-stu-id="93a6f-152">The entry identifier specified in  _lpEntryID_ is not recognized.</span></span> <span data-ttu-id="93a6f-153">Это значение обычно возвращается, если поставщик адресных книг, ответственный за соответствующую запись, не открыт.</span><span class="sxs-lookup"><span data-stu-id="93a6f-153">This value is typically returned if the address book provider responsible for the corresponding entry is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="93a6f-154">Примечания</span><span class="sxs-lookup"><span data-stu-id="93a6f-154">Remarks</span></span>

<span data-ttu-id="93a6f-155">Клиенты и поставщики услуг вызывают метод **IAddrBook:: OpenEntry** для открытия записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="93a6f-155">Clients and service providers call the **IAddrBook::OpenEntry** method to open an address book entry.</span></span> <span data-ttu-id="93a6f-156">MAPI перенаправляет вызов соответствующему поставщику адресной книги на основе структуры [мапиуид](mapiuid.md) , включенной в идентификатор записи, переданный в параметре _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="93a6f-156">MAPI forwards the call to the appropriate address book provider, based on the [MAPIUID](mapiuid.md) structure included in the entry identifier passed in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="93a6f-157">Поставщик адресных книг открывает запись только для чтения, если не установлен флаг MAPI_MODIFY или MAPI_BEST_ACCESS в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="93a6f-157">The address book provider opens the entry as read-only unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter is set.</span></span> <span data-ttu-id="93a6f-158">Тем не менее, эти флаги являются рекомендациями.</span><span class="sxs-lookup"><span data-stu-id="93a6f-158">However, these flags are suggestions.</span></span> <span data-ttu-id="93a6f-159">Если у поставщика адресных книг нет разрешения на изменение запрошенной записи, возвращается MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="93a6f-159">If the address book provider does not allow modification for the entry requested, it returns MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="93a6f-160">Параметр _лпинтерфаце_ указывает интерфейс, который будет использоваться для доступа к открытой записи.</span><span class="sxs-lookup"><span data-stu-id="93a6f-160">The  _lpInterface_ parameter indicates which interface should be used to access the opened entry.</span></span> <span data-ttu-id="93a6f-161">При передаче значения NULL в _лпинтерфаце_ показывается использование стандартного интерфейса MAPI для этого типа записи.</span><span class="sxs-lookup"><span data-stu-id="93a6f-161">Passing NULL in  _lpInterface_ indicates the standard MAPI interface for that type of entry should be used.</span></span> <span data-ttu-id="93a6f-162">Так как поставщик адресных книг может возвращать другой интерфейс, отличный от предложенного параметром _лпинтерфаце_ , вызывающая сторона должна проверить значение, возвращенное в параметре _лпулобжтипе_ , чтобы определить, является ли возвращаемый тип объекта ожидаемым.</span><span class="sxs-lookup"><span data-stu-id="93a6f-162">Because the address book provider might return a different interface than the one suggested by the  _lpInterface_ parameter, the caller should check the value returned in the  _lpulObjType_ parameter to determine whether the object type returned is what was expected.</span></span> <span data-ttu-id="93a6f-163">Если тип объекта не является ожидаемым, вызывающий может привести параметр _лппунк_ к более подходящему типу.</span><span class="sxs-lookup"><span data-stu-id="93a6f-163">If the object type is not of the type expected, the caller can cast the  _lppUnk_ parameter to a type that is more appropriate.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="93a6f-164">См. также</span><span class="sxs-lookup"><span data-stu-id="93a6f-164">See also</span></span>

- [<span data-ttu-id="93a6f-165">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="93a6f-165">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

