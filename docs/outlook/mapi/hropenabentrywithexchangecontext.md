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
ms.openlocfilehash: fcedaf689db8280b4649662ba61c8468d0f98305
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808683"
---
# <a name="hropenabentrywithexchangecontext"></a><span data-ttu-id="4ea73-103">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="4ea73-103">HrOpenABEntryWithExchangeContext</span></span>

  
  
<span data-ttu-id="4ea73-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4ea73-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4ea73-105">Открывает **entryID** , с помощью адресная книга Exchange, определяемую средством **pEmsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="4ea73-105">Opens the **entryID** using the Exchange Address Book identified by **pEmsmdbUID**.</span></span> <span data-ttu-id="4ea73-106">Эта функция работает так же [IAddrBook::Details](iaddrbook-details.md) за исключением того, что с помощью этой функции гарантирует, что [IAddrBook::OpenEntry](iaddrbook-openentry.md) открыто с помощью ожидаемый Exchange доступа к адресной книге.</span><span class="sxs-lookup"><span data-stu-id="4ea73-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) except that using this function ensures that the [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book Provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4ea73-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="4ea73-107">Header file:</span></span>  <br/> |<span data-ttu-id="4ea73-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="4ea73-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="4ea73-109">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="4ea73-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="4ea73-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="4ea73-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="4ea73-111">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="4ea73-111">Called by:</span></span>  <br/> |<span data-ttu-id="4ea73-112">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="4ea73-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="4ea73-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ea73-113">Parameters</span></span>

 <span data-ttu-id="4ea73-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="4ea73-114">_pmsess_</span></span>
  
> <span data-ttu-id="4ea73-115">[in] Система на **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="4ea73-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="4ea73-116">Он не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="4ea73-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="4ea73-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="4ea73-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="4ea73-118">[in] Указатель на **emsmdbUID** , который определяет службу Exchange, которая содержит поставщик адресной книги Exchange, который следует использовать эту функцию для отображения сведений на идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="4ea73-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="4ea73-119">Если входящий идентификатор записи не идентификатор записи Exchange поставщик адресной книги, этот параметр игнорируется и вызов функции действует как [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="4ea73-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="4ea73-120">Если этот параметр имеет значение NULL или ноль MAPIUID, эта функция действует как [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="4ea73-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="4ea73-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="4ea73-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="4ea73-122">[in] В адресной книге используется для открытия идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="4ea73-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="4ea73-123">Он не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="4ea73-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="4ea73-124">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="4ea73-124">_cbEntryID_</span></span>
  
> <span data-ttu-id="4ea73-125">[in] Количество байтов идентификатор записи, указанные с помощью параметра _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="4ea73-125">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="4ea73-126">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="4ea73-126">_lpEntryID_</span></span>
  
>  <span data-ttu-id="4ea73-127">[in] Указатель на идентификатор записи, который представляет записи адресной книги, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="4ea73-127">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="4ea73-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4ea73-128">_ulFlags_</span></span>
  
> <span data-ttu-id="4ea73-129">[in] Битовая маска флаги, который определяет, как открыть запись.</span><span class="sxs-lookup"><span data-stu-id="4ea73-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="4ea73-130">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="4ea73-130">The following flags can be set:</span></span>
    
<span data-ttu-id="4ea73-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="4ea73-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="4ea73-132">Запросы, что операция открываются с максимальное допустимое разрешения сети и клиента.</span><span class="sxs-lookup"><span data-stu-id="4ea73-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="4ea73-133">Например если клиент чтение и запись, поставщик адресной книги пытается открыть запись с чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="4ea73-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="4ea73-134">Можно получить уровень доступа, который был предоставлен путем вызова метода [IMAPIProp::GetProps](imapiprop-getprops.md) open записи и извлечение свойства PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="4ea73-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="4ea73-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="4ea73-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="4ea73-136">Для выполнения разрешения имен с помощью автономной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="4ea73-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="4ea73-137">Например можно использовать этот флаг позволяет открыть глобальный список адресов (GAL) в режиме кэширования данных exchange и получить доступ к записи в этот список адресов из кэша без создания трафика между клиентом и сервером клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="4ea73-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="4ea73-138">Этот флаг поддерживается только поставщик Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="4ea73-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="4ea73-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="4ea73-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="4ea73-140">Разрешает вызов для успешного выполнения, потенциально перед словом полностью open и доступны, подразумевает, что последующие вызовы записи могут завершиться ошибкой.</span><span class="sxs-lookup"><span data-stu-id="4ea73-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="4ea73-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="4ea73-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="4ea73-142">Для выполнения разрешения имен используется только глобальный список адресов.</span><span class="sxs-lookup"><span data-stu-id="4ea73-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="4ea73-143">Этот флаг поддерживается только поставщик Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="4ea73-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="4ea73-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="4ea73-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="4ea73-145">Запросы, которые словом открывать с чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="4ea73-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="4ea73-146">Поскольку записи открываются с доступом только для чтения по умолчанию, клиенты не следует предполагать, чтение и запись, независимо от того, является ли задать MAPI_MODIFY были предоставлены разрешения.</span><span class="sxs-lookup"><span data-stu-id="4ea73-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="4ea73-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="4ea73-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="4ea73-148">Не используйте автономной адресной книги для разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="4ea73-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="4ea73-149">Этот флаг поддерживается только поставщик Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="4ea73-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    

