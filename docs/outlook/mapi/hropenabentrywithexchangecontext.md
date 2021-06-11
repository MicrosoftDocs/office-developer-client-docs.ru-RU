---
title: HrOpenABEntryWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b640a5aa-4e36-4983-bf11-9428809e830b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 415d108f7fd9e84ba2a9090658bc0923550390f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434055"
---
# <a name="hropenabentrywithexchangecontext"></a><span data-ttu-id="c9c4c-103">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="c9c4c-103">HrOpenABEntryWithExchangeContext</span></span>

  
  
<span data-ttu-id="c9c4c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9c4c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9c4c-105">Открывает **entryID** с помощью Exchange адресной книги, идентифицированной **pEmsmdbUID.**</span><span class="sxs-lookup"><span data-stu-id="c9c4c-105">Opens the **entryID** using the Exchange Address Book identified by **pEmsmdbUID**.</span></span> <span data-ttu-id="c9c4c-106">Эта функция работает аналогично [IAddrBook::D etails,](iaddrbook-details.md) за исключением того, что использование этой функции обеспечивает открытие [IAddrBook::OpenEntry](iaddrbook-openentry.md) с помощью ожидаемого поставщика адресных книг Exchange.</span><span class="sxs-lookup"><span data-stu-id="c9c4c-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) except that using this function ensures that the [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book Provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c9c4c-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c9c4c-107">Header file:</span></span>  <br/> |<span data-ttu-id="c9c4c-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="c9c4c-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="c9c4c-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="c9c4c-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="c9c4c-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="c9c4c-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="c9c4c-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="c9c4c-111">Called by:</span></span>  <br/> |<span data-ttu-id="c9c4c-112">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="c9c4c-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDoABDetailsWithExchangeContext(
  LPMAPISESSION pmsess,
  const MAPIUID *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c9c4c-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="c9c4c-113">Parameters</span></span>

 <span data-ttu-id="c9c4c-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="c9c4c-114">_pmsess_</span></span>
  
> <span data-ttu-id="c9c4c-115">[in] Журнал на **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="c9c4c-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="c9c4c-116">Это не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="c9c4c-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="c9c4c-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="c9c4c-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="c9c4c-118">[in] Указатель на **emsmdbUID,** который идентифицирует службу Exchange, которая содержит поставщик адресных книг Exchange, который эта функция должна использовать для отображения сведений об идентификаторе записи.</span><span class="sxs-lookup"><span data-stu-id="c9c4c-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="c9c4c-119">Если идентификатор входной записи не является идентификатором Exchange поставщика адресных книг, этот параметр игнорируется, и вызов функции ведет себя так же, как [iAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="c9c4c-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="c9c4c-120">Если этот параметр является NULL или нулевой MAPIUID, эта функция ведет себя как [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="c9c4c-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="c9c4c-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="c9c4c-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="c9c4c-122">[in] Адресная книга, используемая для открытия идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="c9c4c-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="c9c4c-123">Это не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="c9c4c-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="c9c4c-124">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="c9c4c-124">_cbEntryID_</span></span>
  
> <span data-ttu-id="c9c4c-125">[in] Byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span><span class="sxs-lookup"><span data-stu-id="c9c4c-125">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="c9c4c-126">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="c9c4c-126">_lpEntryID_</span></span>
  
>  <span data-ttu-id="c9c4c-127">[in] Указатель на идентификатор записи, который представляет открытую запись адресной книги.</span><span class="sxs-lookup"><span data-stu-id="c9c4c-127">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="c9c4c-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c9c4c-128">_ulFlags_</span></span>
  
> <span data-ttu-id="c9c4c-129">[in] Битмашка флагов, контролируемая тем, как открывается запись.</span><span class="sxs-lookup"><span data-stu-id="c9c4c-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="c9c4c-130">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="c9c4c-130">The following flags can be set:</span></span>
    
<span data-ttu-id="c9c4c-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="c9c4c-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="c9c4c-132">Запросы на открытие записи с максимально разрешенными сетевыми и клиентными разрешениями.</span><span class="sxs-lookup"><span data-stu-id="c9c4c-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="c9c4c-133">Например, если клиент имеет разрешение на чтение и запись, поставщик адресной книги пытается открыть запись с разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="c9c4c-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="c9c4c-134">Клиент может получить уровень доступа, который был предоставлен, позвонив [методу IMAPIProp::GetProps](imapiprop-getprops.md) открытой записи и извлекая свойство PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="c9c4c-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="c9c4c-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="c9c4c-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="c9c4c-136">Для выполнения разрешения имен используется только офлайн-адресная книга.</span><span class="sxs-lookup"><span data-stu-id="c9c4c-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="c9c4c-137">Например, этот флаг можно использовать, чтобы разрешить клиентской приложению открывать глобальный список адресов (GAL) в кэшном режиме обмена и получать доступ к записи в этой адресной книге из кэша без создания трафика между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="c9c4c-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="c9c4c-138">Этот флаг поддерживается только поставщиком Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="c9c4c-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="c9c4c-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="c9c4c-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="c9c4c-140">Позволяет добиться успеха вызова, потенциально до того, как запись будет полностью открыта и доступна, что означает, что последующие вызовы в запись могут привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="c9c4c-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="c9c4c-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="c9c4c-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="c9c4c-142">Для выполнения разрешения имен используется только GAL.</span><span class="sxs-lookup"><span data-stu-id="c9c4c-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="c9c4c-143">Этот флаг поддерживается только поставщиком Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="c9c4c-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="c9c4c-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="c9c4c-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="c9c4c-145">Запросы на открытие записи с разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="c9c4c-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="c9c4c-146">Поскольку записи открываются с доступом только для чтения по умолчанию, клиенты не должны предполагать, что разрешение на чтение и запись было предоставлено независимо от того, MAPI_MODIFY установлено.</span><span class="sxs-lookup"><span data-stu-id="c9c4c-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="c9c4c-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="c9c4c-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="c9c4c-148">Не использует автономной адресной книги для выполнения разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="c9c4c-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="c9c4c-149">Этот флаг поддерживается только поставщиком Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="c9c4c-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    

