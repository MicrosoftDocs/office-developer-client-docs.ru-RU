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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347826"
---
# <a name="hropenabentryusingdefaultcontext"></a><span data-ttu-id="ba215-103">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="ba215-103">HrOpenABEntryUsingDefaultContext</span></span>

  
  
<span data-ttu-id="ba215-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba215-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba215-105">Выполняет ту же функцию, что и [хропенабентривисексчанжеконтекст](hropenabentrywithexchangecontext.md) , за исключением того, что в качестве параметра _пемсмдбуид_ используется устаревший **емсмдбуид** .</span><span class="sxs-lookup"><span data-stu-id="ba215-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it uses the legacy **emsmdbUID** as the  _pEmsmdbUID_ parameter.</span></span> <span data-ttu-id="ba215-106">Эту функцию не следует использовать, если не удается получить правильную **емсмдбуид** для вызова [хропенабентривисексчанжеконтекст](hropenabentrywithexchangecontext.md).</span><span class="sxs-lookup"><span data-stu-id="ba215-106">Do not use this function unless you cannot obtain the correct **emsmdbUID** for the call to [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ba215-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ba215-107">Header file:</span></span>  <br/> |<span data-ttu-id="ba215-108">абхелп. h</span><span class="sxs-lookup"><span data-stu-id="ba215-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="ba215-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="ba215-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="ba215-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="ba215-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="ba215-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="ba215-111">Called by:</span></span>  <br/> |<span data-ttu-id="ba215-112">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="ba215-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="ba215-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba215-113">Parameters</span></span>

 <span data-ttu-id="ba215-114">_пмсесс_</span><span class="sxs-lookup"><span data-stu-id="ba215-114">_pmsess_</span></span>
  
> <span data-ttu-id="ba215-115">возврата Вошедший в систему **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="ba215-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="ba215-116">Он не может иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="ba215-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="ba215-117">_Паддрбук_</span><span class="sxs-lookup"><span data-stu-id="ba215-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="ba215-118">возврата Адресная книга, используемая для открытия идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="ba215-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="ba215-119">Он не может иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="ba215-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="ba215-120">_Кбентрид_</span><span class="sxs-lookup"><span data-stu-id="ba215-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="ba215-121">возврата Количество байт в идентификаторе записи, заданном параметром _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="ba215-121">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ba215-122">_Лпентрид_</span><span class="sxs-lookup"><span data-stu-id="ba215-122">_lpEntryID_</span></span>
  
>  <span data-ttu-id="ba215-123">возврата Указатель на идентификатор записи, представляющий запись адресной книги, которую требуется открыть.</span><span class="sxs-lookup"><span data-stu-id="ba215-123">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="ba215-124">_Лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="ba215-124">_lpInterface_</span></span>
  
> <span data-ttu-id="ba215-125">возврата Указатель на идентификатор интерфейса (IID) интерфейса, используемого для доступа к открытой записи.</span><span class="sxs-lookup"><span data-stu-id="ba215-125">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="ba215-126">При передаче значения NULL возвращается стандартный интерфейс объекта.</span><span class="sxs-lookup"><span data-stu-id="ba215-126">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="ba215-127">Для пользователей обмена сообщениями стандартный интерфейс — [имаилусер: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="ba215-127">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="ba215-128">Для списков рассылки это [идистлист: IMAPIContainer](idistlistimapicontainer.md), а для контейнеров — [иабконтаинер: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="ba215-128">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="ba215-129">Вызывающие абоненты могут установить _лпинтерфаце_ в соответствии со стандартным интерфейсом или интерфейсом в иерархии наследования.</span><span class="sxs-lookup"><span data-stu-id="ba215-129">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="ba215-130">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ba215-130">_ulFlags_</span></span>
  
> <span data-ttu-id="ba215-131">возврата Битовая маска флагов, определяющих способ открытия записи.</span><span class="sxs-lookup"><span data-stu-id="ba215-131">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="ba215-132">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="ba215-132">The following flags can be set:</span></span>
    
<span data-ttu-id="ba215-133">МАПИ_БЕСТ_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="ba215-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="ba215-134">ЗаПрашивает открытие записи с максимальным количеством разрешенных сетевых и клиентских разрешений.</span><span class="sxs-lookup"><span data-stu-id="ba215-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="ba215-135">Например, если у клиента есть разрешение на чтение и запись, то поставщик адресной книги пытается открыть запись с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="ba215-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="ba215-136">Клиент может получить уровень доступа, предоставленный путем вызова метода [IMAPIProp::](imapiprop-getprops.md) -PROPS записи Open и получения свойства Пр_акцесс_левел (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="ba215-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="ba215-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="ba215-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="ba215-138">Для разрешения имен используется только автономная адресная книга.</span><span class="sxs-lookup"><span data-stu-id="ba215-138">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="ba215-139">Например, вы можете использовать этот флаг, чтобы разрешить клиентскому приложению открывать глобальный список адресов (GAL) в режиме кэширования Exchange и получать доступ к записи в этой адресной книге из кэша, не создавая трафик между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="ba215-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="ba215-140">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="ba215-140">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="ba215-141">МАПИ_ДЕФЕРРЕД_ЕРРОРС</span><span class="sxs-lookup"><span data-stu-id="ba215-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="ba215-142">Разрешает успешный вызов, потенциально перед тем, как запись будет полностью открыта и доступна, подразумевая, что последующие вызовы записи могут возвращать ошибку.</span><span class="sxs-lookup"><span data-stu-id="ba215-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="ba215-143">МАПИ_ГАЛ_ОНЛИ</span><span class="sxs-lookup"><span data-stu-id="ba215-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="ba215-144">Использует только глобальный список адресов, чтобы выполнить разрешение имен.</span><span class="sxs-lookup"><span data-stu-id="ba215-144">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="ba215-145">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="ba215-145">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="ba215-146">МАПИ_МОДИФИ</span><span class="sxs-lookup"><span data-stu-id="ba215-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="ba215-147">ЗаПрашивает открытие записи с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="ba215-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="ba215-148">Так как записи открываются с доступом только для чтения по умолчанию, клиенты не должны предполагать, что разрешение на чтение и запись предоставлено независимо от того, задано ли МАПИ_МОДИФИ.</span><span class="sxs-lookup"><span data-stu-id="ba215-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="ba215-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="ba215-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="ba215-150">Не использует автономную адресную книгу для разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="ba215-150">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="ba215-151">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="ba215-151">This flag is supported only by the Exchange address book provider.</span></span>
    
 <span data-ttu-id="ba215-152">_Лпулобжтипе_</span><span class="sxs-lookup"><span data-stu-id="ba215-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="ba215-153">вышли Указатель на тип открытого элемента.</span><span class="sxs-lookup"><span data-stu-id="ba215-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="ba215-154">_Лппунк_</span><span class="sxs-lookup"><span data-stu-id="ba215-154">_lppUnk_</span></span>
  
> <span data-ttu-id="ba215-155">вышли Указатель на указатель открытого элемента.</span><span class="sxs-lookup"><span data-stu-id="ba215-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

