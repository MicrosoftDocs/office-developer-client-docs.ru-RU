---
title: HrOpenABEntryUsingDefaultContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17cba69b-2b25-4b99-99d9-ec68fb8a35b5
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 74660de551d43c589cb903b5c3852136f2f18269
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808684"
---
# <a name="hropenabentryusingdefaultcontext"></a><span data-ttu-id="01886-103">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="01886-103">HrOpenABEntryUsingDefaultContext</span></span>

  
  
<span data-ttu-id="01886-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="01886-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="01886-105">Выполняет те же функции, что [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) , за исключением того, что он использует прежних версий **emsmdbUID** и параметр _pEmsmdbUID_ .</span><span class="sxs-lookup"><span data-stu-id="01886-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it uses the legacy **emsmdbUID** as the  _pEmsmdbUID_ parameter.</span></span> <span data-ttu-id="01886-106">Не используйте эту функцию, если не удается получить правильный **emsmdbUID** для вызова [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).</span><span class="sxs-lookup"><span data-stu-id="01886-106">Do not use this function unless you cannot obtain the correct **emsmdbUID** for the call to [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="01886-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="01886-107">Header file:</span></span>  <br/> |<span data-ttu-id="01886-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="01886-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="01886-109">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="01886-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="01886-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="01886-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="01886-111">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="01886-111">Called by:</span></span>  <br/> |<span data-ttu-id="01886-112">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="01886-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="01886-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="01886-113">Parameters</span></span>

 <span data-ttu-id="01886-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="01886-114">_pmsess_</span></span>
  
> <span data-ttu-id="01886-115">[in] Система на **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="01886-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="01886-116">Он не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="01886-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="01886-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="01886-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="01886-118">[in] В адресной книге используется для открытия идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="01886-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="01886-119">Он не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="01886-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="01886-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="01886-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="01886-121">[in] Количество байтов идентификатор записи, указанные с помощью параметра _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="01886-121">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="01886-122">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="01886-122">_lpEntryID_</span></span>
  
>  <span data-ttu-id="01886-123">[in] Указатель на идентификатор записи, который представляет записи адресной книги, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="01886-123">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="01886-124">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="01886-124">_lpInterface_</span></span>
  
> <span data-ttu-id="01886-125">[in] Указатель на интерфейс идентификатор (ИД интерфейса) интерфейс, который используется для доступа к открытой операцией.</span><span class="sxs-lookup"><span data-stu-id="01886-125">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="01886-126">Передача NULL Возвращает стандартный интерфейс объекта.</span><span class="sxs-lookup"><span data-stu-id="01886-126">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="01886-127">Для пользователей, обмена мгновенными сообщениями, — это стандартный интерфейс [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="01886-127">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="01886-128">Для списков рассылки, он является [IDistList: IMAPIContainer](idistlistimapicontainer.md)и для контейнеров, это [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="01886-128">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="01886-129">Вызывающие объекты можно задать _lpInterface_ соответствующий стандартный интерфейс или интерфейс в иерархии наследования.</span><span class="sxs-lookup"><span data-stu-id="01886-129">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="01886-130">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="01886-130">_ulFlags_</span></span>
  
> <span data-ttu-id="01886-131">[in] Битовая маска флаги, который определяет, как открыть запись.</span><span class="sxs-lookup"><span data-stu-id="01886-131">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="01886-132">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="01886-132">The following flags can be set:</span></span>
    
<span data-ttu-id="01886-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="01886-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="01886-134">Запросы, что операция открываются с максимальное допустимое разрешения сети и клиента.</span><span class="sxs-lookup"><span data-stu-id="01886-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="01886-135">Например если клиент чтение и запись, поставщик адресной книги пытается открыть запись с чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="01886-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="01886-136">Можно получить уровень доступа, который был предоставлен путем вызова метода [IMAPIProp::GetProps](imapiprop-getprops.md) open записи и извлечение свойства PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="01886-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="01886-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="01886-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="01886-138">Для выполнения разрешения имен с помощью автономной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="01886-138">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="01886-139">Например можно использовать этот флаг позволяет открыть глобальный список адресов (GAL) в режиме кэширования данных exchange и получить доступ к записи в этот список адресов из кэша без создания трафика между клиентом и сервером клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="01886-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="01886-140">Этот флаг поддерживается только поставщик Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="01886-140">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="01886-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="01886-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="01886-142">Разрешает вызов для успешного выполнения, потенциально перед словом полностью open и доступны, подразумевает, что последующие вызовы записи могут завершиться ошибкой.</span><span class="sxs-lookup"><span data-stu-id="01886-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="01886-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="01886-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="01886-144">Для выполнения разрешения имен используется только глобальный список адресов.</span><span class="sxs-lookup"><span data-stu-id="01886-144">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="01886-145">Этот флаг поддерживается только поставщик Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="01886-145">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="01886-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="01886-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="01886-147">Запросы, которые словом открывать с чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="01886-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="01886-148">Поскольку записи открываются с доступом только для чтения по умолчанию, клиенты не следует предполагать, чтение и запись, независимо от того, является ли задать MAPI_MODIFY были предоставлены разрешения.</span><span class="sxs-lookup"><span data-stu-id="01886-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="01886-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="01886-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="01886-150">Не используйте автономной адресной книги для разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="01886-150">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="01886-151">Этот флаг поддерживается только поставщик Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="01886-151">This flag is supported only by the Exchange address book provider.</span></span>
    
 <span data-ttu-id="01886-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="01886-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="01886-153">[out] Указатель на тип открыт записи.</span><span class="sxs-lookup"><span data-stu-id="01886-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="01886-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="01886-154">_lppUnk_</span></span>
  
> <span data-ttu-id="01886-155">[out] Указатель на указатель открыт записи.</span><span class="sxs-lookup"><span data-stu-id="01886-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

