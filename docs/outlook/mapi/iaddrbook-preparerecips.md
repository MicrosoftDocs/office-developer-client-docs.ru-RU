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
ms.openlocfilehash: fe3e098b2b70e77bd0c536002a4724810261bff3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19808782"
---
# <a name="iaddrbookpreparerecips"></a><span data-ttu-id="f544c-103">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="f544c-103">IAddrBook::PrepareRecips</span></span>

  
  
<span data-ttu-id="f544c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f544c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f544c-105">Подготовка списка получателей для дальнейшего использования системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="f544c-105">Prepares a recipient list for later use by the messaging system.</span></span> 
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpSPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="f544c-106">���������</span><span class="sxs-lookup"><span data-stu-id="f544c-106">Parameters</span></span>

 <span data-ttu-id="f544c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f544c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f544c-108">[in] Битовая маска флаги, который определяет, как открыть запись.</span><span class="sxs-lookup"><span data-stu-id="f544c-108">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="f544c-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="f544c-109">The following flag can be set:</span></span>
    
<span data-ttu-id="f544c-110">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="f544c-110">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="f544c-111">Для выполнения разрешения имен используйте автономной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="f544c-111">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="f544c-112">Например чтобы разрешить клиентским приложением для открытия глобальном списке адресов (GAL) в режиме кэширования данных exchange и для доступа к записи в этот список адресов из кэша без создания трафика между клиентом и сервером можно использовать этот флаг.</span><span class="sxs-lookup"><span data-stu-id="f544c-112">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and to access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="f544c-113">Этот флаг поддерживается только поставщик Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="f544c-113">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="f544c-114">_lpSPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="f544c-114">_lpSPropTagArray_</span></span>
  
> <span data-ttu-id="f544c-115">[in] Указатель на структуру [SPropTagArray](sproptagarray.md) , который содержит массив тегов свойств, которые указывают свойства, при их наличии, который требуется обновление.</span><span class="sxs-lookup"><span data-stu-id="f544c-115">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags that indicate the properties, if any, that require updating.</span></span> <span data-ttu-id="f544c-116">Параметр _lpSPropTagArray_ может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="f544c-116">The  _lpSPropTagArray_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="f544c-117">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="f544c-117">_lpRecipList_</span></span>
  
> <span data-ttu-id="f544c-118">[in] Указатель на структуру [ADRLIST](adrlist.md) , содержащий список получателей.</span><span class="sxs-lookup"><span data-stu-id="f544c-118">[in] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f544c-119">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="f544c-119">Return value</span></span>

<span data-ttu-id="f544c-120">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="f544c-120">S_OK</span></span> 
  
> <span data-ttu-id="f544c-121">Список получателей успешно подготовлен.</span><span class="sxs-lookup"><span data-stu-id="f544c-121">The recipient list was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f544c-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="f544c-122">Remarks</span></span>

<span data-ttu-id="f544c-123">Клиенты и поставщики услуг вызовите метод **PrepareRecips** для выполните следующее:</span><span class="sxs-lookup"><span data-stu-id="f544c-123">Clients and service providers call the **PrepareRecips** method to do the following:</span></span> 
  
- <span data-ttu-id="f544c-124">Убедитесь, что всех получателей с помощью параметра _lpRecipList_ имеют долгосрочного идентификаторы записей.</span><span class="sxs-lookup"><span data-stu-id="f544c-124">Ensure that all recipients in the  _lpRecipList_ parameter have long-term entry identifiers.</span></span> 
    
- <span data-ttu-id="f544c-125">Убедитесь, что каждого получателя, с помощью параметра _lpRecipList_ имеет свойства, указанные в параметре _lpSPropTagArray_ и, что эти свойства отображаются в начале списка получателей.</span><span class="sxs-lookup"><span data-stu-id="f544c-125">Ensure that each recipient in the  _lpRecipList_ parameter has the properties listed in the  _lpSPropTagArray_ parameter and that these properties appear at the start of the recipient list.</span></span> 
    
<span data-ttu-id="f544c-126">MAPI преобразует каждого получателя краткосрочных идентификаторы записей для долгосрочного идентификаторы записей.</span><span class="sxs-lookup"><span data-stu-id="f544c-126">MAPI converts each recipient's short-term entry identifiers to long-term entry identifiers.</span></span> <span data-ttu-id="f544c-127">При необходимости получателей долгосрочного идентификаторы записей извлекаются из соответствующих адресной книге и запрашиваются дополнительные свойства.</span><span class="sxs-lookup"><span data-stu-id="f544c-127">If necessary, recipients' long-term entry identifiers are retrieved from the appropriate address book provider and any additional properties are requested.</span></span>
  
<span data-ttu-id="f544c-128">В отдельную запись получателя запрошенные свойства упорядочены во-первых, следуют все свойства, которые они уже присутствуют запись.</span><span class="sxs-lookup"><span data-stu-id="f544c-128">In an individual recipient entry, the requested properties are ordered first, followed by any properties that were already present for the entry.</span></span> <span data-ttu-id="f544c-129">Если один или несколько обязательных свойств с помощью параметра _lpSPropTagArray_ не обрабатывается поставщик соответствующие адресной книги, их типы свойств будет иметь значение PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="f544c-129">If one or more of the requested properties in the  _lpSPropTagArray_ parameter are not handled by the appropriate address book provider, their property types will be set to PT_ERROR.</span></span> <span data-ttu-id="f544c-130">Значения свойств будет иметь значение MAPI_E_NOT_FOUND или другой значение, задающее более конкретные причину, почему свойства недоступны.</span><span class="sxs-lookup"><span data-stu-id="f544c-130">Their property values will be set to either to MAPI_E_NOT_FOUND or to another value that gives a more specific reason why the properties are not available.</span></span> <span data-ttu-id="f544c-131">Каждая структура [SPropValue](spropvalue.md) , включенных в параметре _lpRecipList_ необходимо отдельно выделить с помощью функции [MAPIAllocateBuffer](mapiallocatebuffer.md) и [MAPIAllocateMore](mapiallocatemore.md) , чтобы его можно освободить по отдельности.</span><span class="sxs-lookup"><span data-stu-id="f544c-131">Each [SPropValue](spropvalue.md) structure included in the  _lpRecipList_ parameter must be separately allocated by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions so that it can be freed individually.</span></span> 
  
<span data-ttu-id="f544c-132">Сведения о PT_ERROR содержатся [Типы свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="f544c-132">For information about PT_ERROR, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f544c-133">См. также</span><span class="sxs-lookup"><span data-stu-id="f544c-133">See also</span></span>



[<span data-ttu-id="f544c-134">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="f544c-134">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="f544c-135">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="f544c-135">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="f544c-136">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="f544c-136">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="f544c-137">Каноническое свойство PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="f544c-137">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="f544c-138">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f544c-138">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="f544c-139">SRowSet</span><span class="sxs-lookup"><span data-stu-id="f544c-139">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="f544c-140">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f544c-140">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

