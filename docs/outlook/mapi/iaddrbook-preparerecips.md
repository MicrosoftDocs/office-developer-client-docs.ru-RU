---
title: IAddrBookPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.PrepareRecips
api_type:
- COM
ms.assetid: d423f7b5-23b8-44dd-bca3-6590182dc42d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: db1c23f33e604d6aafdd8a046566c7390c281ad8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414279"
---
# <a name="iaddrbookpreparerecips"></a><span data-ttu-id="55e16-103">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="55e16-103">IAddrBook::PrepareRecips</span></span>

  
  
<span data-ttu-id="55e16-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55e16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55e16-105">Подготавливает список получателей для более позднего использования системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="55e16-105">Prepares a recipient list for later use by the messaging system.</span></span> 
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpSPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="55e16-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="55e16-106">Parameters</span></span>

 <span data-ttu-id="55e16-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="55e16-107">_ulFlags_</span></span>
  
> <span data-ttu-id="55e16-108">[in] Битмашка флагов, контролируемая тем, как открывается запись.</span><span class="sxs-lookup"><span data-stu-id="55e16-108">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="55e16-109">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="55e16-109">The following flag can be set:</span></span>
    
<span data-ttu-id="55e16-110">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="55e16-110">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="55e16-111">Для выполнения разрешения имен используйте только офлайн-адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="55e16-111">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="55e16-112">Например, этот флаг можно использовать для того, чтобы клиентская заявка открыла глобальный адресный список (GAL) в кэшировом режиме обмена и доступ к записи в этой адресной книге из кэша без создания трафика между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="55e16-112">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and to access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="55e16-113">Этот флаг поддерживается только поставщиком Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="55e16-113">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="55e16-114">_lpSPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="55e16-114">_lpSPropTagArray_</span></span>
  
> <span data-ttu-id="55e16-115">[in] Указатель на структуру [SPropTagArray,](sproptagarray.md) которая содержит массив тегов свойств, которые указывают свойства, если таковые имеются, которые требуют обновления.</span><span class="sxs-lookup"><span data-stu-id="55e16-115">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags that indicate the properties, if any, that require updating.</span></span> <span data-ttu-id="55e16-116">Параметр  _lpSPropTagArray может_ быть NULL.</span><span class="sxs-lookup"><span data-stu-id="55e16-116">The  _lpSPropTagArray_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="55e16-117">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="55e16-117">_lpRecipList_</span></span>
  
> <span data-ttu-id="55e16-118">[in] Указатель на структуру [ADRLIST,](adrlist.md) которая содержит список получателей.</span><span class="sxs-lookup"><span data-stu-id="55e16-118">[in] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="55e16-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55e16-119">Return value</span></span>

<span data-ttu-id="55e16-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="55e16-120">S_OK</span></span> 
  
> <span data-ttu-id="55e16-121">Список получателей был успешно подготовлен.</span><span class="sxs-lookup"><span data-stu-id="55e16-121">The recipient list was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="55e16-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="55e16-122">Remarks</span></span>

<span data-ttu-id="55e16-123">Клиенты и поставщики услуг звонят по **методу PrepareRecips,** чтобы сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="55e16-123">Clients and service providers call the **PrepareRecips** method to do the following:</span></span> 
  
- <span data-ttu-id="55e16-124">Убедитесь, что все получатели в  _параметре lpRecipList_ имеют долгосрочные идентификаторы записи.</span><span class="sxs-lookup"><span data-stu-id="55e16-124">Ensure that all recipients in the  _lpRecipList_ parameter have long-term entry identifiers.</span></span> 
    
- <span data-ttu-id="55e16-125">Убедитесь, что каждый получатель в параметре  _lpRecipList_ имеет свойства, указанные в параметре  _lpSPropTagArray,_ и чтобы эти свойства появились в начале списка получателей.</span><span class="sxs-lookup"><span data-stu-id="55e16-125">Ensure that each recipient in the  _lpRecipList_ parameter has the properties listed in the  _lpSPropTagArray_ parameter and that these properties appear at the start of the recipient list.</span></span> 
    
<span data-ttu-id="55e16-126">MAPI преобразует краткосрочные идентификаторы записи каждого получателя в долгосрочные идентификаторы записи.</span><span class="sxs-lookup"><span data-stu-id="55e16-126">MAPI converts each recipient's short-term entry identifiers to long-term entry identifiers.</span></span> <span data-ttu-id="55e16-127">При необходимости долгосрочные идентификаторы записей получателей извлекаются из соответствующего поставщика адресной книги, и запрашиваются дополнительные свойства.</span><span class="sxs-lookup"><span data-stu-id="55e16-127">If necessary, recipients' long-term entry identifiers are retrieved from the appropriate address book provider and any additional properties are requested.</span></span>
  
<span data-ttu-id="55e16-128">В отдельной записи получателя запрашиваются сначала запрашиваемые свойства, а затем все свойства, которые уже присутствовали для записи.</span><span class="sxs-lookup"><span data-stu-id="55e16-128">In an individual recipient entry, the requested properties are ordered first, followed by any properties that were already present for the entry.</span></span> <span data-ttu-id="55e16-129">Если одно или несколько запрашиваемого свойства в параметре  _lpSPropTagArray_ не обрабатываются соответствующим поставщиком адресной книги, их типы свойств будут заданы PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="55e16-129">If one or more of the requested properties in the  _lpSPropTagArray_ parameter are not handled by the appropriate address book provider, their property types will be set to PT_ERROR.</span></span> <span data-ttu-id="55e16-130">Их значения свойств будут задатки MAPI_E_NOT_FOUND или другому значению, которое дает более конкретную причину, по которой свойства недоступны.</span><span class="sxs-lookup"><span data-stu-id="55e16-130">Their property values will be set to either to MAPI_E_NOT_FOUND or to another value that gives a more specific reason why the properties are not available.</span></span> <span data-ttu-id="55e16-131">Каждая [структура SPropValue,](spropvalue.md) включенная в параметр  _lpRecipList,_ должна быть выделена отдельно с помощью функций [MAPIAllocateBuffer](mapiallocatebuffer.md) и [MAPIAllocateMore,](mapiallocatemore.md) чтобы ее можно было освободить по отдельности.</span><span class="sxs-lookup"><span data-stu-id="55e16-131">Each [SPropValue](spropvalue.md) structure included in the  _lpRecipList_ parameter must be separately allocated by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions so that it can be freed individually.</span></span> 
  
<span data-ttu-id="55e16-132">Сведения о PT_ERROR см. в этой PT_ERROR [типах свойств.](property-types.md)</span><span class="sxs-lookup"><span data-stu-id="55e16-132">For information about PT_ERROR, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="55e16-133">См. также</span><span class="sxs-lookup"><span data-stu-id="55e16-133">See also</span></span>



[<span data-ttu-id="55e16-134">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="55e16-134">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="55e16-135">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="55e16-135">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="55e16-136">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="55e16-136">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="55e16-137">Каноническое свойство PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="55e16-137">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="55e16-138">SPropValue</span><span class="sxs-lookup"><span data-stu-id="55e16-138">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="55e16-139">SRowSet</span><span class="sxs-lookup"><span data-stu-id="55e16-139">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="55e16-140">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="55e16-140">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

