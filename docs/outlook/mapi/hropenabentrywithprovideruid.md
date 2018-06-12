---
title: HrOpenABEntryWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83821a86-abff-460c-bb8e-9fd9d232dc6b
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: e33e656e70802437ab8b8717c5e175e2a13e384e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808680"
---
# <a name="hropenabentrywithprovideruid"></a><span data-ttu-id="07df9-103">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="07df9-103">HrOpenABEntryWithProviderUID</span></span>

  
  
<span data-ttu-id="07df9-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="07df9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="07df9-105">Открывает **entryID** , с помощью адресная книга Exchange, определяемую средством _pEmsabpUID_.</span><span class="sxs-lookup"><span data-stu-id="07df9-105">Opens the **entryID** using the Exchange Address Book identified by  _pEmsabpUID_.</span></span> <span data-ttu-id="07df9-106">Эта функция работает так же [IAddrBook::OpenEntry](iaddrbook-openentry.md) за исключением того, что с помощью этой функции гарантирует, что [IAddrBook::OpenEntry](iaddrbook-openentry.md) открыто с помощью ожидаемый поставщик адресной книги для Exchange.</span><span class="sxs-lookup"><span data-stu-id="07df9-106">This function works similarly to [IAddrBook::OpenEntry](iaddrbook-openentry.md) except that using this function ensures that [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="07df9-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="07df9-107">Header file:</span></span>  <br/> |<span data-ttu-id="07df9-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="07df9-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="07df9-109">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="07df9-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="07df9-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="07df9-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="07df9-111">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="07df9-111">Called by:</span></span>  <br/> |<span data-ttu-id="07df9-112">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="07df9-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="07df9-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="07df9-113">Parameters</span></span>

 <span data-ttu-id="07df9-114">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="07df9-114">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="07df9-115">[in] Указатель на **emsmdbUID** , который определяет службу Exchange, которая содержит поставщик адресной книги Exchange, который следует использовать эту функцию для отображения сведений на идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="07df9-115">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="07df9-116">Если входящий идентификатор записи не идентификатор записи Exchange поставщик адресной книги, этот параметр игнорируется и вызов функции действует как [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="07df9-116">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="07df9-117">Если этот параметр имеет значение NULL или ноль MAPIUID, эта функция действует как [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="07df9-117">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="07df9-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="07df9-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="07df9-119">[in] В адресной книге используется для открытия идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="07df9-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="07df9-120">Он не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="07df9-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="07df9-121">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="07df9-121">_cbEntryID_</span></span>
  
> <span data-ttu-id="07df9-122">[in] Количество байтов идентификатор записи, указанные с помощью параметра _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="07df9-122">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="07df9-123">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="07df9-123">_lpEntryID_</span></span>
  
>  <span data-ttu-id="07df9-124">[in] Указатель на идентификатор записи, который представляет записи адресной книги, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="07df9-124">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="07df9-125">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="07df9-125">_lpInterface_</span></span>
  
> <span data-ttu-id="07df9-126">[in] Указатель на интерфейс идентификатор (ИД интерфейса) интерфейс, который используется для доступа к открытой операцией.</span><span class="sxs-lookup"><span data-stu-id="07df9-126">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="07df9-127">Передача NULL Возвращает стандартный интерфейс объекта.</span><span class="sxs-lookup"><span data-stu-id="07df9-127">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="07df9-128">Для пользователей, обмена мгновенными сообщениями, — это стандартный интерфейс [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="07df9-128">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="07df9-129">Для списков рассылки — это [IDistList: IMAPIContainer](idistlistimapicontainer.md)и для контейнеров, это [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="07df9-129">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="07df9-130">Вызывающие объекты можно задать _lpInterface_ соответствующий стандартный интерфейс или интерфейс в иерархии наследования.</span><span class="sxs-lookup"><span data-stu-id="07df9-130">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="07df9-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="07df9-131">_ulFlags_</span></span>
  
> <span data-ttu-id="07df9-132">[in] Битовая маска флагов, как открыть словом, можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="07df9-132">[in] A bitmask of flags that controls the how the entry is opened, The following flags can be set:</span></span>
    
<span data-ttu-id="07df9-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="07df9-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="07df9-134">Запросы, что операция открываются с максимальное допустимое разрешения сети и клиента.</span><span class="sxs-lookup"><span data-stu-id="07df9-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="07df9-135">Например если клиент чтение и запись, поставщик адресной книги пытается открыть запись с чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="07df9-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="07df9-136">Можно получить уровень доступа, который был предоставлен путем вызова метода [IMAPIProp::GetProps](imapiprop-getprops.md) open записи и извлечение свойства PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="07df9-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="07df9-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="07df9-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="07df9-138">Для выполнения разрешения имен используйте автономной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="07df9-138">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="07df9-139">Например можно использовать этот флаг позволяет открыть глобальный список адресов (GAL) в режиме кэширования данных exchange и получить доступ к записи в этот список адресов из кэша без создания трафика между клиентом и сервером клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="07df9-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="07df9-140">Этот флаг поддерживается только поставщик Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="07df9-140">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="07df9-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="07df9-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="07df9-142">Разрешает вызов для успешного выполнения, потенциально перед словом полностью open и доступны, подразумевает, что последующие вызовы записи могут завершиться ошибкой.</span><span class="sxs-lookup"><span data-stu-id="07df9-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="07df9-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="07df9-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="07df9-144">Для выполнения разрешения имен используйте только глобальный список адресов.</span><span class="sxs-lookup"><span data-stu-id="07df9-144">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="07df9-145">Этот флаг поддерживается только поставщик Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="07df9-145">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="07df9-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="07df9-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="07df9-147">Запросы, которые словом открывать с чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="07df9-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="07df9-148">Поскольку записи открываются с доступом только для чтения по умолчанию, клиенты не следует предполагать, чтение и запись, независимо от того, является ли задать MAPI_MODIFY были предоставлены разрешения.</span><span class="sxs-lookup"><span data-stu-id="07df9-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="07df9-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="07df9-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="07df9-150">Не используйте автономной адресной книги для разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="07df9-150">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="07df9-151">Этот флаг поддерживается только поставщик Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="07df9-151">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="07df9-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="07df9-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="07df9-153">[out] Указатель на тип открыт записи.</span><span class="sxs-lookup"><span data-stu-id="07df9-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="07df9-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="07df9-154">_lppUnk_</span></span>
  
> <span data-ttu-id="07df9-155">[out] Указатель на указатель открыт записи.</span><span class="sxs-lookup"><span data-stu-id="07df9-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

