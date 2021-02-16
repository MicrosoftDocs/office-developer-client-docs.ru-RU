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
# <a name="hropenabentrywithprovideruid"></a><span data-ttu-id="4c83d-103">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="4c83d-103">HrOpenABEntryWithProviderUID</span></span>

  
  
<span data-ttu-id="4c83d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c83d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c83d-105">Открывает **entryID с** помощью адресной книги Exchange, заданной _pEmsabpUID._</span><span class="sxs-lookup"><span data-stu-id="4c83d-105">Opens the **entryID** using the Exchange Address Book identified by  _pEmsabpUID_.</span></span> <span data-ttu-id="4c83d-106">Эта функция работает аналогично [IAddrBook::OpenEntry](iaddrbook-openentry.md) за исключением того, что использование этой функции обеспечивает открытие [IAddrBook::OpenEntry](iaddrbook-openentry.md) с помощью ожидаемого поставщика адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="4c83d-106">This function works similarly to [IAddrBook::OpenEntry](iaddrbook-openentry.md) except that using this function ensures that [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4c83d-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="4c83d-107">Header file:</span></span>  <br/> |<span data-ttu-id="4c83d-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="4c83d-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="4c83d-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="4c83d-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="4c83d-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="4c83d-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="4c83d-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="4c83d-111">Called by:</span></span>  <br/> |<span data-ttu-id="4c83d-112">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="4c83d-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="4c83d-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c83d-113">Parameters</span></span>

 <span data-ttu-id="4c83d-114">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="4c83d-114">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="4c83d-115">[in] Указатель на **emsmdbUID,** который определяет службу Exchange, которая содержит поставщика адресной книги Exchange, которую эта функция должна использовать для отображения сведений об идентификаторе записи.</span><span class="sxs-lookup"><span data-stu-id="4c83d-115">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="4c83d-116">Если идентификатор входной записи не является идентификатором записи поставщика адресной книги Exchange, этот параметр игнорируется, и вызов функции ведет себя так же, как [iAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="4c83d-116">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="4c83d-117">Если этот параметр имеет значение NULL или mapIUID нулевого уровня, эта функция ведет себя как [IAddrBook::D etails.](iaddrbook-details.md)</span><span class="sxs-lookup"><span data-stu-id="4c83d-117">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="4c83d-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="4c83d-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="4c83d-119">[in] Адресная книга, используемая для открытия идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="4c83d-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="4c83d-120">Это не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="4c83d-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="4c83d-121">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="4c83d-121">_cbEntryID_</span></span>
  
> <span data-ttu-id="4c83d-122">[in] Количество ветвей идентификатора записи, заданного параметром _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="4c83d-122">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="4c83d-123">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="4c83d-123">_lpEntryID_</span></span>
  
>  <span data-ttu-id="4c83d-124">[in] Указатель на идентификатор записи, который представляет открываемую запись адресной книги.</span><span class="sxs-lookup"><span data-stu-id="4c83d-124">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="4c83d-125">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="4c83d-125">_lpInterface_</span></span>
  
> <span data-ttu-id="4c83d-126">[in] Указатель на идентификатор интерфейса, используемый для доступа к открытой записи.</span><span class="sxs-lookup"><span data-stu-id="4c83d-126">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="4c83d-127">Передача NULL возвращает стандартный интерфейс объекта.</span><span class="sxs-lookup"><span data-stu-id="4c83d-127">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="4c83d-128">Для пользователей обмена сообщениями стандартным интерфейсом [является IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="4c83d-128">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="4c83d-129">Для списков рассылки это [IDistList : IMAPIContainer,](idistlistimapicontainer.md)а для контейнеров — [IABContainer : IMAPIContainer.](iabcontainerimapicontainer.md)</span><span class="sxs-lookup"><span data-stu-id="4c83d-129">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="4c83d-130">Вызывающие могут установить  _lpInterface_ для соответствующего стандартного интерфейса или интерфейса в иерархии наследования.</span><span class="sxs-lookup"><span data-stu-id="4c83d-130">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="4c83d-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4c83d-131">_ulFlags_</span></span>
  
> <span data-ttu-id="4c83d-132">[in] Битоваяmas флагов, которая управляет тем, как открывается запись, можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="4c83d-132">[in] A bitmask of flags that controls the how the entry is opened, The following flags can be set:</span></span>
    
<span data-ttu-id="4c83d-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="4c83d-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="4c83d-134">Запрашивает открытие записи с максимальным разрешенным доступом к сети и разрешениям клиента.</span><span class="sxs-lookup"><span data-stu-id="4c83d-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="4c83d-135">Например, если у клиента есть разрешение на чтение и запись, поставщик адресной книги пытается открыть запись с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="4c83d-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="4c83d-136">Клиент может получить уровень доступа, предоставленный путем вызова метода [IMAPIProp::GetProps](imapiprop-getprops.md) открытой записи и получения свойства PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="4c83d-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="4c83d-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="4c83d-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="4c83d-138">Используйте только автономной адресной книги для разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="4c83d-138">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="4c83d-139">Например, этот флаг можно использовать, чтобы разрешить клиентского приложения открывать глобальный список адресов (GAL) в режиме кэшации exchange и получать доступ к записи в этой адресной книге из кэша без создания трафика между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="4c83d-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="4c83d-140">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="4c83d-140">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="4c83d-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="4c83d-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="4c83d-142">Позволяет добиться успешного вызова, возможно, до того, как запись будет полностью открытой и доступной, что означает, что последующие вызовы записи могут возвращать ошибку.</span><span class="sxs-lookup"><span data-stu-id="4c83d-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="4c83d-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="4c83d-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="4c83d-144">Используйте только gal для разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="4c83d-144">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="4c83d-145">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="4c83d-145">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="4c83d-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="4c83d-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="4c83d-147">Запрашивает открытие записи с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="4c83d-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="4c83d-148">Так как по умолчанию записи открываются с доступом только для чтения, клиенты не должны предполагать, что разрешение на чтение и запись было предоставлено независимо от того, MAPI_MODIFY настроены.</span><span class="sxs-lookup"><span data-stu-id="4c83d-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="4c83d-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="4c83d-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="4c83d-150">Не используйте автономной адресной книги для разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="4c83d-150">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="4c83d-151">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="4c83d-151">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="4c83d-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="4c83d-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="4c83d-153">[out] Указатель на тип открытой записи.</span><span class="sxs-lookup"><span data-stu-id="4c83d-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="4c83d-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="4c83d-154">_lppUnk_</span></span>
  
> <span data-ttu-id="4c83d-155">[out] Указатель на указатель открытой записи.</span><span class="sxs-lookup"><span data-stu-id="4c83d-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

