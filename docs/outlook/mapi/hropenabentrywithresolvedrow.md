---
title: HrOpenABEntryWithResolvedRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ce3a583c-16a9-4268-9476-926d2780eae5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2eb643e0002e2159e3197d66e021aba0bb8c126f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429910"
---
# <a name="hropenabentrywithresolvedrow"></a><span data-ttu-id="96df3-103">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="96df3-103">HrOpenABEntryWithResolvedRow</span></span>

  
  
<span data-ttu-id="96df3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96df3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96df3-105">Выполняет ту же функцию, что и [HrOpenABEntryWithExchangeContext,](hropenabentrywithexchangecontext.md) за исключением того, что она автоматически получает **emsabpUID** из разрешенной строки и открывает **entryID**.</span><span class="sxs-lookup"><span data-stu-id="96df3-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it automatically gets the **emsabpUID** from the resolved row and opens the **entryID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="96df3-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="96df3-106">Header file:</span></span>  <br/> |<span data-ttu-id="96df3-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="96df3-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="96df3-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="96df3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="96df3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="96df3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="96df3-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="96df3-110">Called by:</span></span>  <br/> |<span data-ttu-id="96df3-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="96df3-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithResolvedRow(
  LPSRow prwResolved,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="96df3-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="96df3-112">Parameters</span></span>

 <span data-ttu-id="96df3-113">_prwResolved_</span><span class="sxs-lookup"><span data-stu-id="96df3-113">_prwResolved_</span></span>
  
> <span data-ttu-id="96df3-114">[in] Указатель на разрешенную строку, которая используется для получения **emsabpUID** и открытия **entryID.**</span><span class="sxs-lookup"><span data-stu-id="96df3-114">[in] A pointer to the resolved row that is used to get the **emsabpUID** and open the **entryID**.</span></span>
    
 <span data-ttu-id="96df3-115">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="96df3-115">_pAddrBook_</span></span>
  
> <span data-ttu-id="96df3-116">[in] Адресная книга, используемая для открытия идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="96df3-116">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="96df3-117">Это не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="96df3-117">It cannot be NULL.</span></span>
    
 <span data-ttu-id="96df3-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="96df3-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="96df3-119">[in] Количество ветвей идентификатора записи, заданного параметром _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="96df3-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="96df3-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="96df3-120">_lpEntryID_</span></span>
  
>  <span data-ttu-id="96df3-121">[in] Указатель на идентификатор записи, который представляет открываемую запись адресной книги.</span><span class="sxs-lookup"><span data-stu-id="96df3-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="96df3-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="96df3-122">_lpInterface_</span></span>
  
> <span data-ttu-id="96df3-123">[in] Указатель на идентификатор интерфейса, используемый для доступа к открытой записи.</span><span class="sxs-lookup"><span data-stu-id="96df3-123">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="96df3-124">Передача NULL возвращает стандартный интерфейс объекта.</span><span class="sxs-lookup"><span data-stu-id="96df3-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="96df3-125">Для пользователей обмена сообщениями стандартным интерфейсом [является IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="96df3-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="96df3-126">Для списков рассылки это [IDistList : IMAPIContainer,](idistlistimapicontainer.md)а для контейнеров — [IABContainer : IMAPIContainer.](iabcontainerimapicontainer.md)</span><span class="sxs-lookup"><span data-stu-id="96df3-126">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="96df3-127">Вызывающие могут установить  _lpInterface_ для соответствующего стандартного интерфейса или интерфейса в иерархии наследования.</span><span class="sxs-lookup"><span data-stu-id="96df3-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="96df3-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="96df3-128">_ulFlags_</span></span>
  
> <span data-ttu-id="96df3-129">[in] Битоваяmas флагов, которая управляет открытием записи.</span><span class="sxs-lookup"><span data-stu-id="96df3-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="96df3-130">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="96df3-130">The following flags can be set:</span></span>
    
<span data-ttu-id="96df3-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="96df3-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="96df3-132">Запрашивает открытие записи с максимальным разрешенным доступом к сети и разрешениям клиента.</span><span class="sxs-lookup"><span data-stu-id="96df3-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="96df3-133">Например, если у клиента есть разрешение на чтение и запись, поставщик адресной книги пытается открыть запись с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="96df3-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="96df3-134">Клиент может получить уровень доступа, предоставленный путем вызова метода [IMAPIProp::GetProps](imapiprop-getprops.md) открытой записи и получения свойства PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="96df3-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="96df3-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="96df3-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="96df3-136">Для разрешения имен используется только автономной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="96df3-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="96df3-137">Например, этот флаг можно использовать, чтобы разрешить клиентского приложения открывать глобальный список адресов (GAL) в режиме кэшации exchange и получать доступ к записи в этой адресной книге из кэша без создания трафика между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="96df3-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="96df3-138">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="96df3-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="96df3-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="96df3-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="96df3-140">Позволяет добиться успешного вызова, возможно, до того, как запись будет полностью открытой и доступной, что означает, что последующие вызовы записи могут возвращать ошибку.</span><span class="sxs-lookup"><span data-stu-id="96df3-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="96df3-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="96df3-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="96df3-142">Для разрешения имен используется только gal.</span><span class="sxs-lookup"><span data-stu-id="96df3-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="96df3-143">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="96df3-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="96df3-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="96df3-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="96df3-145">Запрашивает открытие записи с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="96df3-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="96df3-146">Так как по умолчанию записи открываются с доступом только для чтения, клиенты не должны предполагать, что разрешение на чтение и запись было предоставлено независимо от того, MAPI_MODIFY настроены.</span><span class="sxs-lookup"><span data-stu-id="96df3-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="96df3-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="96df3-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="96df3-148">Не использует автономной адресной книги для разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="96df3-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="96df3-149">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="96df3-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="96df3-150">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="96df3-150">_lpulObjType_</span></span>
  
> <span data-ttu-id="96df3-151">[out] Указатель на тип открытой записи.</span><span class="sxs-lookup"><span data-stu-id="96df3-151">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="96df3-152">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="96df3-152">_lppUnk_</span></span>
  
> <span data-ttu-id="96df3-153">[out] Указатель на указатель открытой записи.</span><span class="sxs-lookup"><span data-stu-id="96df3-153">[out] A pointer to a pointer of the opened entry.</span></span>
    

