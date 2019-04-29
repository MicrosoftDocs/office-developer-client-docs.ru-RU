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
# <a name="hropenabentrywithresolvedrow"></a><span data-ttu-id="8deaf-103">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="8deaf-103">HrOpenABEntryWithResolvedRow</span></span>

  
  
<span data-ttu-id="8deaf-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8deaf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8deaf-105">Выполняет те же функции, что и [хропенабентривисексчанжеконтекст](hropenabentrywithexchangecontext.md) , за исключением того, что он автоматически получает **емсабпуид** из разрешенной строки и открывает **entryID**.</span><span class="sxs-lookup"><span data-stu-id="8deaf-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it automatically gets the **emsabpUID** from the resolved row and opens the **entryID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8deaf-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="8deaf-106">Header file:</span></span>  <br/> |<span data-ttu-id="8deaf-107">абхелп. h</span><span class="sxs-lookup"><span data-stu-id="8deaf-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="8deaf-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="8deaf-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8deaf-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8deaf-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8deaf-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="8deaf-110">Called by:</span></span>  <br/> |<span data-ttu-id="8deaf-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="8deaf-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="8deaf-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="8deaf-112">Parameters</span></span>

 <span data-ttu-id="8deaf-113">_Првресолвед_</span><span class="sxs-lookup"><span data-stu-id="8deaf-113">_prwResolved_</span></span>
  
> <span data-ttu-id="8deaf-114">возврата Указатель на разрешенную строку, которая используется для получения **емсабпуид** и открытия **entryID**.</span><span class="sxs-lookup"><span data-stu-id="8deaf-114">[in] A pointer to the resolved row that is used to get the **emsabpUID** and open the **entryID**.</span></span>
    
 <span data-ttu-id="8deaf-115">_Паддрбук_</span><span class="sxs-lookup"><span data-stu-id="8deaf-115">_pAddrBook_</span></span>
  
> <span data-ttu-id="8deaf-116">возврата Адресная книга, используемая для открытия идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="8deaf-116">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="8deaf-117">Он не может иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="8deaf-117">It cannot be NULL.</span></span>
    
 <span data-ttu-id="8deaf-118">_Кбентрид_</span><span class="sxs-lookup"><span data-stu-id="8deaf-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="8deaf-119">возврата Количество байт в идентификаторе записи, заданном параметром _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="8deaf-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="8deaf-120">_Лпентрид_</span><span class="sxs-lookup"><span data-stu-id="8deaf-120">_lpEntryID_</span></span>
  
>  <span data-ttu-id="8deaf-121">возврата Указатель на идентификатор записи, представляющий запись адресной книги, которую требуется открыть.</span><span class="sxs-lookup"><span data-stu-id="8deaf-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="8deaf-122">_Лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="8deaf-122">_lpInterface_</span></span>
  
> <span data-ttu-id="8deaf-123">возврата Указатель на идентификатор интерфейса (IID) интерфейса, используемого для доступа к открытой записи.</span><span class="sxs-lookup"><span data-stu-id="8deaf-123">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="8deaf-124">При передаче значения NULL возвращается стандартный интерфейс объекта.</span><span class="sxs-lookup"><span data-stu-id="8deaf-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="8deaf-125">Для пользователей обмена сообщениями стандартный интерфейс — [имаилусер: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="8deaf-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="8deaf-126">Для списков рассылки это [идистлист: IMAPIContainer](idistlistimapicontainer.md)и для контейнеров, [иабконтаинер: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="8deaf-126">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="8deaf-127">Вызывающие абоненты могут установить _лпинтерфаце_ в соответствии со стандартным интерфейсом или интерфейсом в иерархии наследования.</span><span class="sxs-lookup"><span data-stu-id="8deaf-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="8deaf-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8deaf-128">_ulFlags_</span></span>
  
> <span data-ttu-id="8deaf-129">возврата Битовая маска флагов, определяющих способ открытия записи.</span><span class="sxs-lookup"><span data-stu-id="8deaf-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="8deaf-130">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="8deaf-130">The following flags can be set:</span></span>
    
<span data-ttu-id="8deaf-131">МАПИ_БЕСТ_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="8deaf-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="8deaf-132">ЗаПрашивает открытие записи с максимальным количеством разрешенных сетевых и клиентских разрешений.</span><span class="sxs-lookup"><span data-stu-id="8deaf-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="8deaf-133">Например, если у клиента есть разрешение на чтение и запись, то поставщик адресной книги пытается открыть запись с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="8deaf-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="8deaf-134">Клиент может получить уровень доступа, предоставленный путем вызова метода [IMAPIProp::](imapiprop-getprops.md) -PROPS записи Open и получения свойства Пр_акцесс_левел (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="8deaf-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="8deaf-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="8deaf-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="8deaf-136">Для разрешения имен используется только автономная адресная книга.</span><span class="sxs-lookup"><span data-stu-id="8deaf-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="8deaf-137">Например, вы можете использовать этот флаг, чтобы разрешить клиентскому приложению открывать глобальный список адресов (GAL) в режиме кэширования Exchange и получать доступ к записи в этой адресной книге из кэша, не создавая трафик между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="8deaf-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="8deaf-138">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="8deaf-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="8deaf-139">МАПИ_ДЕФЕРРЕД_ЕРРОРС</span><span class="sxs-lookup"><span data-stu-id="8deaf-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="8deaf-140">Разрешает успешный вызов, потенциально перед тем, как запись будет полностью открыта и доступна, подразумевая, что последующие вызовы записи могут возвращать ошибку.</span><span class="sxs-lookup"><span data-stu-id="8deaf-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="8deaf-141">МАПИ_ГАЛ_ОНЛИ</span><span class="sxs-lookup"><span data-stu-id="8deaf-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="8deaf-142">Использует только глобальный список адресов, чтобы выполнить разрешение имен.</span><span class="sxs-lookup"><span data-stu-id="8deaf-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="8deaf-143">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="8deaf-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="8deaf-144">МАПИ_МОДИФИ</span><span class="sxs-lookup"><span data-stu-id="8deaf-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="8deaf-145">ЗаПрашивает открытие записи с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="8deaf-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="8deaf-146">Так как записи открываются с доступом только для чтения по умолчанию, клиенты не должны предполагать, что разрешение на чтение и запись предоставлено независимо от того, задано ли МАПИ_МОДИФИ.</span><span class="sxs-lookup"><span data-stu-id="8deaf-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="8deaf-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="8deaf-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="8deaf-148">Не использует автономную адресную книгу для разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="8deaf-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="8deaf-149">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="8deaf-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="8deaf-150">_Лпулобжтипе_</span><span class="sxs-lookup"><span data-stu-id="8deaf-150">_lpulObjType_</span></span>
  
> <span data-ttu-id="8deaf-151">вышли Указатель на тип открытого элемента.</span><span class="sxs-lookup"><span data-stu-id="8deaf-151">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="8deaf-152">_Лппунк_</span><span class="sxs-lookup"><span data-stu-id="8deaf-152">_lppUnk_</span></span>
  
> <span data-ttu-id="8deaf-153">вышли Указатель на указатель открытого элемента.</span><span class="sxs-lookup"><span data-stu-id="8deaf-153">[out] A pointer to a pointer of the opened entry.</span></span>
    

