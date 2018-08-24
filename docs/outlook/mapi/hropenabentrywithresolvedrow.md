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
ms.openlocfilehash: 9572f44f1f4865fcce5d7aa8bd8478340b0de968
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594721"
---
# <a name="hropenabentrywithresolvedrow"></a><span data-ttu-id="e886c-103">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="e886c-103">HrOpenABEntryWithResolvedRow</span></span>

  
  
<span data-ttu-id="e886c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e886c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e886c-105">Выполняет те же функции, что [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) , за исключением того, автоматически получает **emsabpUID** из строки возможности разрешения и открывает **entryID**.</span><span class="sxs-lookup"><span data-stu-id="e886c-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it automatically gets the **emsabpUID** from the resolved row and opens the **entryID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e886c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e886c-106">Header file:</span></span>  <br/> |<span data-ttu-id="e886c-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="e886c-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="e886c-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="e886c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e886c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e886c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e886c-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="e886c-110">Called by:</span></span>  <br/> |<span data-ttu-id="e886c-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="e886c-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="e886c-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="e886c-112">Parameters</span></span>

 <span data-ttu-id="e886c-113">_prwResolved_</span><span class="sxs-lookup"><span data-stu-id="e886c-113">_prwResolved_</span></span>
  
> <span data-ttu-id="e886c-114">[in] Указатель на разрешить строку, в которой используется для получения **emsabpUID** и откройте **entryID**.</span><span class="sxs-lookup"><span data-stu-id="e886c-114">[in] A pointer to the resolved row that is used to get the **emsabpUID** and open the **entryID**.</span></span>
    
 <span data-ttu-id="e886c-115">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="e886c-115">_pAddrBook_</span></span>
  
> <span data-ttu-id="e886c-116">[in] В адресной книге используется для открытия идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="e886c-116">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="e886c-117">Он не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="e886c-117">It cannot be NULL.</span></span>
    
 <span data-ttu-id="e886c-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="e886c-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="e886c-119">[in] Количество байтов идентификатор записи, указанные с помощью параметра _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="e886c-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="e886c-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="e886c-120">_lpEntryID_</span></span>
  
>  <span data-ttu-id="e886c-121">[in] Указатель на идентификатор записи, который представляет записи адресной книги, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="e886c-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="e886c-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="e886c-122">_lpInterface_</span></span>
  
> <span data-ttu-id="e886c-123">[in] Указатель на интерфейс идентификатор (ИД интерфейса) интерфейс, который используется для доступа к открытой операцией.</span><span class="sxs-lookup"><span data-stu-id="e886c-123">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="e886c-124">Передача NULL Возвращает стандартный интерфейс объекта.</span><span class="sxs-lookup"><span data-stu-id="e886c-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="e886c-125">Для пользователей, обмена мгновенными сообщениями, — это стандартный интерфейс [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="e886c-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="e886c-126">Для списков рассылки — это [IDistList: IMAPIContainer](idistlistimapicontainer.md)и для контейнеров, это [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="e886c-126">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="e886c-127">Вызывающие объекты можно задать _lpInterface_ соответствующий стандартный интерфейс или интерфейс в иерархии наследования.</span><span class="sxs-lookup"><span data-stu-id="e886c-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="e886c-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e886c-128">_ulFlags_</span></span>
  
> <span data-ttu-id="e886c-129">[in] Битовая маска флаги, который определяет, как открыть запись.</span><span class="sxs-lookup"><span data-stu-id="e886c-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="e886c-130">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="e886c-130">The following flags can be set:</span></span>
    
<span data-ttu-id="e886c-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="e886c-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="e886c-132">Запросы, что операция открываются с максимальное допустимое разрешения сети и клиента.</span><span class="sxs-lookup"><span data-stu-id="e886c-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="e886c-133">Например если клиент чтение и запись, поставщик адресной книги пытается открыть запись с чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="e886c-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="e886c-134">Можно получить уровень доступа, который был предоставлен путем вызова метода [IMAPIProp::GetProps](imapiprop-getprops.md) open записи и извлечение свойства PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="e886c-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="e886c-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="e886c-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="e886c-136">Для выполнения разрешения имен с помощью автономной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="e886c-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="e886c-137">Например можно использовать этот флаг позволяет открыть глобальный список адресов (GAL) в режиме кэширования данных exchange и получить доступ к записи в этот список адресов из кэша без создания трафика между клиентом и сервером клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="e886c-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="e886c-138">Этот флаг поддерживается только поставщик Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="e886c-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="e886c-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="e886c-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="e886c-140">Разрешает вызов для успешного выполнения, потенциально перед словом полностью open и доступны, подразумевает, что последующие вызовы записи могут завершиться ошибкой.</span><span class="sxs-lookup"><span data-stu-id="e886c-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="e886c-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="e886c-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="e886c-142">Для выполнения разрешения имен используется только глобальный список адресов.</span><span class="sxs-lookup"><span data-stu-id="e886c-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="e886c-143">Этот флаг поддерживается только поставщик Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="e886c-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="e886c-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="e886c-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="e886c-145">Запросы, которые словом открывать с чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="e886c-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="e886c-146">Поскольку записи открываются с доступом только для чтения по умолчанию, клиенты не следует предполагать, чтение и запись, независимо от того, является ли задать MAPI_MODIFY были предоставлены разрешения.</span><span class="sxs-lookup"><span data-stu-id="e886c-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="e886c-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="e886c-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="e886c-148">Не используйте автономной адресной книги для разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="e886c-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="e886c-149">Этот флаг поддерживается только поставщик Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="e886c-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="e886c-150">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="e886c-150">_lpulObjType_</span></span>
  
> <span data-ttu-id="e886c-151">[out] Указатель на тип открыт записи.</span><span class="sxs-lookup"><span data-stu-id="e886c-151">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="e886c-152">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="e886c-152">_lppUnk_</span></span>
  
> <span data-ttu-id="e886c-153">[out] Указатель на указатель открыт записи.</span><span class="sxs-lookup"><span data-stu-id="e886c-153">[out] A pointer to a pointer of the opened entry.</span></span>
    

