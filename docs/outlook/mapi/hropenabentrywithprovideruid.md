---
title: HrOpenABEntryWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83821a86-abff-460c-bb8e-9fd9d232dc6b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 20344185ffcbd90017fa3c3493218bd9b3ddfd74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408896"
---
# <a name="hropenabentrywithprovideruid"></a><span data-ttu-id="bde3e-103">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="bde3e-103">HrOpenABEntryWithProviderUID</span></span>

  
  
<span data-ttu-id="bde3e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bde3e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bde3e-105">Открывает **entryID** с помощью Exchange адресной книги, идентифицированной _pEmsabpUID._</span><span class="sxs-lookup"><span data-stu-id="bde3e-105">Opens the **entryID** using the Exchange Address Book identified by  _pEmsabpUID_.</span></span> <span data-ttu-id="bde3e-106">Эта функция работает аналогично [IAddrBook::OpenEntry,](iaddrbook-openentry.md) за исключением того, что использование этой функции обеспечивает открытие [IAddrBook::OpenEntry](iaddrbook-openentry.md) с помощью ожидаемого поставщика адресной книги Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="bde3e-106">This function works similarly to [IAddrBook::OpenEntry](iaddrbook-openentry.md) except that using this function ensures that [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bde3e-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="bde3e-107">Header file:</span></span>  <br/> |<span data-ttu-id="bde3e-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="bde3e-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="bde3e-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="bde3e-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="bde3e-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="bde3e-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="bde3e-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="bde3e-111">Called by:</span></span>  <br/> |<span data-ttu-id="bde3e-112">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="bde3e-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithProviderUID(
  const MAPIUID *pEmsabpUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="bde3e-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="bde3e-113">Parameters</span></span>

 <span data-ttu-id="bde3e-114">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="bde3e-114">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="bde3e-115">[in] Указатель на **emsmdbUID,** который идентифицирует службу Exchange, которая содержит поставщик адресных книг Exchange, который эта функция должна использовать для отображения сведений об идентификаторе записи.</span><span class="sxs-lookup"><span data-stu-id="bde3e-115">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="bde3e-116">Если идентификатор входной записи не является идентификатором Exchange поставщика адресных книг, этот параметр игнорируется, и вызов функции ведет себя так же, как [iAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="bde3e-116">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="bde3e-117">Если этот параметр является NULL или нулевой MAPIUID, эта функция ведет себя как [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="bde3e-117">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="bde3e-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="bde3e-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="bde3e-119">[in] Адресная книга, используемая для открытия идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="bde3e-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="bde3e-120">Это не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="bde3e-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="bde3e-121">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="bde3e-121">_cbEntryID_</span></span>
  
> <span data-ttu-id="bde3e-122">[in] Byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span><span class="sxs-lookup"><span data-stu-id="bde3e-122">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="bde3e-123">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="bde3e-123">_lpEntryID_</span></span>
  
>  <span data-ttu-id="bde3e-124">[in] Указатель на идентификатор записи, который представляет открытую запись адресной книги.</span><span class="sxs-lookup"><span data-stu-id="bde3e-124">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="bde3e-125">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="bde3e-125">_lpInterface_</span></span>
  
> <span data-ttu-id="bde3e-126">[in] Указатель на идентификатор интерфейса (IID) интерфейса, который используется для доступа к открытой записи.</span><span class="sxs-lookup"><span data-stu-id="bde3e-126">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="bde3e-127">Передача NULL возвращает стандартный интерфейс объекта.</span><span class="sxs-lookup"><span data-stu-id="bde3e-127">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="bde3e-128">Для пользователей обмена сообщениями стандартным интерфейсом [является IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="bde3e-128">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="bde3e-129">Для списков рассылки это [IDistList: IMAPIContainer,](idistlistimapicontainer.md)а для контейнеров — [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="bde3e-129">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="bde3e-130">Звонители могут настроить  _lpInterface_ для соответствующего стандартного интерфейса или интерфейса в иерархии наследования.</span><span class="sxs-lookup"><span data-stu-id="bde3e-130">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="bde3e-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bde3e-131">_ulFlags_</span></span>
  
> <span data-ttu-id="bde3e-132">[in] Битмашка флагов, контролируемая тем, как открывается запись, можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="bde3e-132">[in] A bitmask of flags that controls the how the entry is opened, The following flags can be set:</span></span>
    
<span data-ttu-id="bde3e-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="bde3e-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="bde3e-134">Запросы на открытие записи с максимально разрешенными сетевыми и клиентными разрешениями.</span><span class="sxs-lookup"><span data-stu-id="bde3e-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="bde3e-135">Например, если клиент имеет разрешение на чтение и запись, поставщик адресной книги пытается открыть запись с разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="bde3e-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="bde3e-136">Клиент может получить уровень доступа, который был предоставлен, позвонив [методу IMAPIProp::GetProps](imapiprop-getprops.md) открытой записи и извлекая свойство PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="bde3e-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="bde3e-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="bde3e-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="bde3e-138">Для выполнения разрешения имен используйте только офлайн-адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="bde3e-138">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="bde3e-139">Например, этот флаг можно использовать, чтобы разрешить клиентской приложению открывать глобальный список адресов (GAL) в кэшном режиме обмена и получать доступ к записи в этой адресной книге из кэша без создания трафика между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="bde3e-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="bde3e-140">Этот флаг поддерживается только поставщиком Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="bde3e-140">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="bde3e-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="bde3e-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="bde3e-142">Позволяет добиться успеха вызова, потенциально до того, как запись будет полностью открыта и доступна, что означает, что последующие вызовы в запись могут привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="bde3e-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="bde3e-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="bde3e-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="bde3e-144">Для выполнения разрешения имен используйте только GAL.</span><span class="sxs-lookup"><span data-stu-id="bde3e-144">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="bde3e-145">Этот флаг поддерживается только поставщиком Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="bde3e-145">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="bde3e-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="bde3e-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="bde3e-147">Запросы на открытие записи с разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="bde3e-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="bde3e-148">Поскольку записи открываются с доступом только для чтения по умолчанию, клиенты не должны предполагать, что разрешение на чтение и запись было предоставлено независимо от того, MAPI_MODIFY установлено.</span><span class="sxs-lookup"><span data-stu-id="bde3e-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="bde3e-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="bde3e-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="bde3e-150">Не используйте офлайн-адресную книгу для выполнения разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="bde3e-150">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="bde3e-151">Этот флаг поддерживается только поставщиком Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="bde3e-151">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="bde3e-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="bde3e-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="bde3e-153">[вышел] Указатель на тип открываемой записи.</span><span class="sxs-lookup"><span data-stu-id="bde3e-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="bde3e-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="bde3e-154">_lppUnk_</span></span>
  
> <span data-ttu-id="bde3e-155">[вышел] Указатель на указатель открываемой записи.</span><span class="sxs-lookup"><span data-stu-id="bde3e-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

