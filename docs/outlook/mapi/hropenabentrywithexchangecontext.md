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
# <a name="hropenabentrywithexchangecontext"></a><span data-ttu-id="99665-103">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="99665-103">HrOpenABEntryWithExchangeContext</span></span>

  
  
<span data-ttu-id="99665-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99665-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99665-105">Открывает идентификатор **entryID** , используя адресную книгу Exchange, определенную в **пемсмдбуид**.</span><span class="sxs-lookup"><span data-stu-id="99665-105">Opens the **entryID** using the Exchange Address Book identified by **pEmsmdbUID**.</span></span> <span data-ttu-id="99665-106">Эта функция работает аналогично [IAddrBook::D етаилс](iaddrbook-details.md) , за исключением того, что с помощью этой функции обеспечивается открытие [IAddrBook:: OpenEntry](iaddrbook-openentry.md) с использованием ожидаемОго поставщика адресных книг Exchange.</span><span class="sxs-lookup"><span data-stu-id="99665-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) except that using this function ensures that the [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book Provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="99665-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="99665-107">Header file:</span></span>  <br/> |<span data-ttu-id="99665-108">абхелп. h</span><span class="sxs-lookup"><span data-stu-id="99665-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="99665-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="99665-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="99665-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="99665-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="99665-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="99665-111">Called by:</span></span>  <br/> |<span data-ttu-id="99665-112">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="99665-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="99665-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="99665-113">Parameters</span></span>

 <span data-ttu-id="99665-114">_пмсесс_</span><span class="sxs-lookup"><span data-stu-id="99665-114">_pmsess_</span></span>
  
> <span data-ttu-id="99665-115">возврата Вошедший в систему **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="99665-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="99665-116">Он не может иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="99665-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="99665-117">_Пемсмдбуид_</span><span class="sxs-lookup"><span data-stu-id="99665-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="99665-118">возврата Указатель на **емсмдбуид** , определяющий службу Exchange, которая содержит поставщика адресных книг Exchange, которую эта функция должна использовать для отображения сведений об идентификаторе записи.</span><span class="sxs-lookup"><span data-stu-id="99665-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="99665-119">Если входящий идентификатор записи не является идентификатором записи поставщика адресных книг Exchange, этот параметр игнорируется, а вызов функции работает так же, как [IAddrBook::D етаилс](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="99665-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="99665-120">Если этот параметр имеет значение NULL или нулевой МАПИУИД, эта функция ведет себя так же, как [IAddrBook::D етаилс](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="99665-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="99665-121">_Паддрбук_</span><span class="sxs-lookup"><span data-stu-id="99665-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="99665-122">возврата Адресная книга, используемая для открытия идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="99665-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="99665-123">Он не может иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="99665-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="99665-124">_Кбентрид_</span><span class="sxs-lookup"><span data-stu-id="99665-124">_cbEntryID_</span></span>
  
> <span data-ttu-id="99665-125">возврата Количество байт в идентификаторе записи, заданном параметром _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="99665-125">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="99665-126">_Лпентрид_</span><span class="sxs-lookup"><span data-stu-id="99665-126">_lpEntryID_</span></span>
  
>  <span data-ttu-id="99665-127">возврата Указатель на идентификатор записи, представляющий запись адресной книги, которую требуется открыть.</span><span class="sxs-lookup"><span data-stu-id="99665-127">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="99665-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="99665-128">_ulFlags_</span></span>
  
> <span data-ttu-id="99665-129">возврата Битовая маска флагов, определяющих способ открытия записи.</span><span class="sxs-lookup"><span data-stu-id="99665-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="99665-130">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="99665-130">The following flags can be set:</span></span>
    
<span data-ttu-id="99665-131">МАПИ_БЕСТ_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="99665-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="99665-132">ЗаПрашивает открытие записи с максимальным количеством разрешенных сетевых и клиентских разрешений.</span><span class="sxs-lookup"><span data-stu-id="99665-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="99665-133">Например, если у клиента есть разрешение на чтение и запись, то поставщик адресной книги пытается открыть запись с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="99665-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="99665-134">Клиент может получить уровень доступа, предоставленный путем вызова метода [IMAPIProp::](imapiprop-getprops.md) -PROPS записи Open и получения свойства Пр_акцесс_левел (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="99665-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="99665-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="99665-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="99665-136">Для разрешения имен используется только автономная адресная книга.</span><span class="sxs-lookup"><span data-stu-id="99665-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="99665-137">Например, вы можете использовать этот флаг, чтобы разрешить клиентскому приложению открывать глобальный список адресов (GAL) в режиме кэширования Exchange и получать доступ к записи в этой адресной книге из кэша, не создавая трафик между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="99665-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="99665-138">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="99665-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="99665-139">МАПИ_ДЕФЕРРЕД_ЕРРОРС</span><span class="sxs-lookup"><span data-stu-id="99665-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="99665-140">Разрешает успешный вызов, потенциально перед тем, как запись будет полностью открыта и доступна, подразумевая, что последующие вызовы записи могут возвращать ошибку.</span><span class="sxs-lookup"><span data-stu-id="99665-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="99665-141">МАПИ_ГАЛ_ОНЛИ</span><span class="sxs-lookup"><span data-stu-id="99665-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="99665-142">Использует только глобальный список адресов, чтобы выполнить разрешение имен.</span><span class="sxs-lookup"><span data-stu-id="99665-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="99665-143">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="99665-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="99665-144">МАПИ_МОДИФИ</span><span class="sxs-lookup"><span data-stu-id="99665-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="99665-145">ЗаПрашивает открытие записи с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="99665-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="99665-146">Так как записи открываются с доступом только для чтения по умолчанию, клиенты не должны предполагать, что разрешение на чтение и запись предоставлено независимо от того, задано ли МАПИ_МОДИФИ.</span><span class="sxs-lookup"><span data-stu-id="99665-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="99665-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="99665-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="99665-148">Не использует автономную адресную книгу для разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="99665-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="99665-149">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="99665-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    

