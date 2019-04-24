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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347819"
---
# <a name="hropenabentrywithprovideruid"></a><span data-ttu-id="649d7-103">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="649d7-103">HrOpenABEntryWithProviderUID</span></span>

  
  
<span data-ttu-id="649d7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="649d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="649d7-105">Открывает идентификатор **entryID** , используя адресную книгу Exchange, определенную в _пемсабпуид_.</span><span class="sxs-lookup"><span data-stu-id="649d7-105">Opens the **entryID** using the Exchange Address Book identified by  _pEmsabpUID_.</span></span> <span data-ttu-id="649d7-106">Эта функция работает аналогично [IAddrBook:: OpenEntry](iaddrbook-openentry.md) , за исключением того, что с помощью этой функции гарантируется, что [IAddrBook:: OpenEntry](iaddrbook-openentry.md) открывается с использованием ожидаемОго поставщика адресных книг Exchange.</span><span class="sxs-lookup"><span data-stu-id="649d7-106">This function works similarly to [IAddrBook::OpenEntry](iaddrbook-openentry.md) except that using this function ensures that [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="649d7-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="649d7-107">Header file:</span></span>  <br/> |<span data-ttu-id="649d7-108">абхелп. h</span><span class="sxs-lookup"><span data-stu-id="649d7-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="649d7-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="649d7-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="649d7-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="649d7-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="649d7-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="649d7-111">Called by:</span></span>  <br/> |<span data-ttu-id="649d7-112">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="649d7-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="649d7-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="649d7-113">Parameters</span></span>

 <span data-ttu-id="649d7-114">_Пемсмдбуид_</span><span class="sxs-lookup"><span data-stu-id="649d7-114">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="649d7-115">возврата Указатель на **емсмдбуид** , определяющий службу Exchange, которая содержит поставщика адресных книг Exchange, которую эта функция должна использовать для отображения сведений об идентификаторе записи.</span><span class="sxs-lookup"><span data-stu-id="649d7-115">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="649d7-116">Если входящий идентификатор записи не является идентификатором записи поставщика адресных книг Exchange, этот параметр игнорируется, а вызов функции работает так же, как [IAddrBook::D етаилс](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="649d7-116">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="649d7-117">Если этот параметр имеет значение NULL или нулевой МАПИУИД, эта функция ведет себя так же, как [IAddrBook::D етаилс](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="649d7-117">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="649d7-118">_Паддрбук_</span><span class="sxs-lookup"><span data-stu-id="649d7-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="649d7-119">возврата Адресная книга, используемая для открытия идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="649d7-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="649d7-120">Он не может иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="649d7-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="649d7-121">_Кбентрид_</span><span class="sxs-lookup"><span data-stu-id="649d7-121">_cbEntryID_</span></span>
  
> <span data-ttu-id="649d7-122">возврата Количество байт в идентификаторе записи, заданном параметром _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="649d7-122">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="649d7-123">_Лпентрид_</span><span class="sxs-lookup"><span data-stu-id="649d7-123">_lpEntryID_</span></span>
  
>  <span data-ttu-id="649d7-124">возврата Указатель на идентификатор записи, представляющий запись адресной книги, которую требуется открыть.</span><span class="sxs-lookup"><span data-stu-id="649d7-124">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="649d7-125">_Лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="649d7-125">_lpInterface_</span></span>
  
> <span data-ttu-id="649d7-126">возврата Указатель на идентификатор интерфейса (IID) интерфейса, используемого для доступа к открытой записи.</span><span class="sxs-lookup"><span data-stu-id="649d7-126">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="649d7-127">При передаче значения NULL возвращается стандартный интерфейс объекта.</span><span class="sxs-lookup"><span data-stu-id="649d7-127">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="649d7-128">Для пользователей обмена сообщениями стандартный интерфейс — [имаилусер: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="649d7-128">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="649d7-129">Для списков рассылки это [идистлист: IMAPIContainer](idistlistimapicontainer.md)и для контейнеров, [иабконтаинер: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="649d7-129">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="649d7-130">Вызывающие абоненты могут установить _лпинтерфаце_ в соответствии со стандартным интерфейсом или интерфейсом в иерархии наследования.</span><span class="sxs-lookup"><span data-stu-id="649d7-130">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="649d7-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="649d7-131">_ulFlags_</span></span>
  
> <span data-ttu-id="649d7-132">возврата Битовая маска флагов, определяющих способ открытия записи, можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="649d7-132">[in] A bitmask of flags that controls the how the entry is opened, The following flags can be set:</span></span>
    
<span data-ttu-id="649d7-133">МАПИ_БЕСТ_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="649d7-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="649d7-134">ЗаПрашивает открытие записи с максимальным количеством разрешенных сетевых и клиентских разрешений.</span><span class="sxs-lookup"><span data-stu-id="649d7-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="649d7-135">Например, если у клиента есть разрешение на чтение и запись, то поставщик адресной книги пытается открыть запись с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="649d7-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="649d7-136">Клиент может получить уровень доступа, предоставленный путем вызова метода [IMAPIProp::](imapiprop-getprops.md) -PROPS записи Open и получения свойства Пр_акцесс_левел (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="649d7-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="649d7-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="649d7-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="649d7-138">Для разрешения имен используйте только автономную адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="649d7-138">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="649d7-139">Например, вы можете использовать этот флаг, чтобы разрешить клиентскому приложению открывать глобальный список адресов (GAL) в режиме кэширования Exchange и получать доступ к записи в этой адресной книге из кэша, не создавая трафик между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="649d7-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="649d7-140">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="649d7-140">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="649d7-141">МАПИ_ДЕФЕРРЕД_ЕРРОРС</span><span class="sxs-lookup"><span data-stu-id="649d7-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="649d7-142">Разрешает успешный вызов, потенциально перед тем, как запись будет полностью открыта и доступна, подразумевая, что последующие вызовы записи могут возвращать ошибку.</span><span class="sxs-lookup"><span data-stu-id="649d7-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="649d7-143">МАПИ_ГАЛ_ОНЛИ</span><span class="sxs-lookup"><span data-stu-id="649d7-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="649d7-144">Для разрешения имен используйте только глобальный список адресов.</span><span class="sxs-lookup"><span data-stu-id="649d7-144">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="649d7-145">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="649d7-145">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="649d7-146">МАПИ_МОДИФИ</span><span class="sxs-lookup"><span data-stu-id="649d7-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="649d7-147">ЗаПрашивает открытие записи с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="649d7-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="649d7-148">Так как записи открываются с доступом только для чтения по умолчанию, клиенты не должны предполагать, что разрешение на чтение и запись предоставлено независимо от того, задано ли МАПИ_МОДИФИ.</span><span class="sxs-lookup"><span data-stu-id="649d7-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="649d7-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="649d7-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="649d7-150">Не используйте автономную адресную книгу для разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="649d7-150">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="649d7-151">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="649d7-151">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="649d7-152">_Лпулобжтипе_</span><span class="sxs-lookup"><span data-stu-id="649d7-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="649d7-153">вышли Указатель на тип открытого элемента.</span><span class="sxs-lookup"><span data-stu-id="649d7-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="649d7-154">_Лппунк_</span><span class="sxs-lookup"><span data-stu-id="649d7-154">_lppUnk_</span></span>
  
> <span data-ttu-id="649d7-155">вышли Указатель на указатель открытого элемента.</span><span class="sxs-lookup"><span data-stu-id="649d7-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

