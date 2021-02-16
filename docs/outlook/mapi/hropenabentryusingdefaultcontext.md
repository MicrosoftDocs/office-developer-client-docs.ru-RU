---
title: HrOpenABEntryUsingDefaultContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17cba69b-2b25-4b99-99d9-ec68fb8a35b5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f60c4d3761694439d10b073fda5bc36443c13e43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434342"
---
# <a name="hropenabentryusingdefaultcontext"></a><span data-ttu-id="1caa2-103">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="1caa2-103">HrOpenABEntryUsingDefaultContext</span></span>

  
  
<span data-ttu-id="1caa2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1caa2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1caa2-105">Выполняет ту же функцию, что и [HrOpenABEntryWithExchangeContext,](hropenabentrywithexchangecontext.md) за исключением того, что в качестве параметра _pEmsmdbUID_ используется устаревшая версия **emsmdbUID.**</span><span class="sxs-lookup"><span data-stu-id="1caa2-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it uses the legacy **emsmdbUID** as the  _pEmsmdbUID_ parameter.</span></span> <span data-ttu-id="1caa2-106">Не используйте эту функцию, если не удается получить правильный **emsmdbUID** для вызова [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).</span><span class="sxs-lookup"><span data-stu-id="1caa2-106">Do not use this function unless you cannot obtain the correct **emsmdbUID** for the call to [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1caa2-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="1caa2-107">Header file:</span></span>  <br/> |<span data-ttu-id="1caa2-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="1caa2-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="1caa2-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="1caa2-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="1caa2-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="1caa2-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="1caa2-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="1caa2-111">Called by:</span></span>  <br/> |<span data-ttu-id="1caa2-112">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="1caa2-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryUsingDefaultContext(
  LPMAPISESSION pmsess,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="1caa2-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="1caa2-113">Parameters</span></span>

 <span data-ttu-id="1caa2-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="1caa2-114">_pmsess_</span></span>
  
> <span data-ttu-id="1caa2-115">[in] Во время входа в **систему IMAPISession.**</span><span class="sxs-lookup"><span data-stu-id="1caa2-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="1caa2-116">Это не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="1caa2-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="1caa2-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="1caa2-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="1caa2-118">[in] Адресная книга, используемая для открытия идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="1caa2-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="1caa2-119">Это не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="1caa2-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="1caa2-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="1caa2-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="1caa2-121">[in] Количество ветвей идентификатора записи, заданного параметром _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="1caa2-121">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="1caa2-122">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="1caa2-122">_lpEntryID_</span></span>
  
>  <span data-ttu-id="1caa2-123">[in] Указатель на идентификатор записи, который представляет открываемую запись адресной книги.</span><span class="sxs-lookup"><span data-stu-id="1caa2-123">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="1caa2-124">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="1caa2-124">_lpInterface_</span></span>
  
> <span data-ttu-id="1caa2-125">[in] Указатель на идентификатор интерфейса, используемый для доступа к открытой записи.</span><span class="sxs-lookup"><span data-stu-id="1caa2-125">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="1caa2-126">Передача NULL возвращает стандартный интерфейс объекта.</span><span class="sxs-lookup"><span data-stu-id="1caa2-126">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="1caa2-127">Для пользователей обмена сообщениями стандартным интерфейсом [является IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="1caa2-127">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="1caa2-128">Для списков рассылки это [IDistList : IMAPIContainer,](idistlistimapicontainer.md)а для контейнеров — [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="1caa2-128">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="1caa2-129">Вызывающие могут установить  _lpInterface_ для соответствующего стандартного интерфейса или интерфейса в иерархии наследования.</span><span class="sxs-lookup"><span data-stu-id="1caa2-129">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="1caa2-130">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1caa2-130">_ulFlags_</span></span>
  
> <span data-ttu-id="1caa2-131">[in] Битоваяmas флагов, которая управляет открытием записи.</span><span class="sxs-lookup"><span data-stu-id="1caa2-131">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="1caa2-132">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="1caa2-132">The following flags can be set:</span></span>
    
<span data-ttu-id="1caa2-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="1caa2-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="1caa2-134">Запрашивает открытие записи с максимальным разрешенным доступом к сети и разрешениям клиента.</span><span class="sxs-lookup"><span data-stu-id="1caa2-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="1caa2-135">Например, если у клиента есть разрешение на чтение и запись, поставщик адресной книги пытается открыть запись с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="1caa2-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="1caa2-136">Клиент может получить уровень доступа, предоставленный путем вызова метода [IMAPIProp::GetProps](imapiprop-getprops.md) открытой записи и получения свойства PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="1caa2-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="1caa2-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="1caa2-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="1caa2-138">Для разрешения имен используется только автономной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="1caa2-138">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="1caa2-139">Например, этот флаг можно использовать, чтобы разрешить клиентского приложения открывать глобальный список адресов (GAL) в режиме кэшации exchange и получать доступ к записи в этой адресной книге из кэша без создания трафика между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="1caa2-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="1caa2-140">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="1caa2-140">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="1caa2-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="1caa2-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="1caa2-142">Позволяет добиться успешного вызова, возможно, до того, как запись будет полностью открытой и доступной, что означает, что последующие вызовы записи могут возвращать ошибку.</span><span class="sxs-lookup"><span data-stu-id="1caa2-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="1caa2-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="1caa2-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="1caa2-144">Для разрешения имен используется только gal.</span><span class="sxs-lookup"><span data-stu-id="1caa2-144">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="1caa2-145">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="1caa2-145">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="1caa2-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="1caa2-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="1caa2-147">Запрашивает открытие записи с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="1caa2-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="1caa2-148">Так как по умолчанию записи открываются с доступом только для чтения, клиенты не должны предполагать, что разрешение на чтение и запись было предоставлено независимо от того, MAPI_MODIFY настроены.</span><span class="sxs-lookup"><span data-stu-id="1caa2-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="1caa2-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="1caa2-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="1caa2-150">Не использует автономной адресной книги для разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="1caa2-150">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="1caa2-151">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="1caa2-151">This flag is supported only by the Exchange address book provider.</span></span>
    
 <span data-ttu-id="1caa2-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="1caa2-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="1caa2-153">[out] Указатель на тип открытой записи.</span><span class="sxs-lookup"><span data-stu-id="1caa2-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="1caa2-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="1caa2-154">_lppUnk_</span></span>
  
> <span data-ttu-id="1caa2-155">[out] Указатель на указатель открытой записи.</span><span class="sxs-lookup"><span data-stu-id="1caa2-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

