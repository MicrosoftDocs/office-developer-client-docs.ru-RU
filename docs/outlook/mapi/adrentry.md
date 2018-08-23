---
title: ADRENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRENTRY
api_type:
- COM
ms.assetid: 5fa091a4-3a84-4881-91b3-e34fd9ca6f38
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f3a62f6783e3b1a0a0423a08c7f5e866b42b81f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569178"
---
# <a name="adrentry"></a><span data-ttu-id="4caaf-103">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="4caaf-103">ADRENTRY</span></span>

  
  
<span data-ttu-id="4caaf-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4caaf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4caaf-105">Описание ноль или больше свойств, относящихся к получателя.</span><span class="sxs-lookup"><span data-stu-id="4caaf-105">Describes zero or more properties that belong to a recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4caaf-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="4caaf-106">Header file:</span></span>  <br/> |<span data-ttu-id="4caaf-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4caaf-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _ADRENTRY
{
  ULONG ulReserved1;
  ULONG cValues;
  LPSPropValue rgPropVals;
} ADRENTRY, FAR *LPADRENTRY;

```

## <a name="members"></a><span data-ttu-id="4caaf-108">Members</span><span class="sxs-lookup"><span data-stu-id="4caaf-108">Members</span></span>

 <span data-ttu-id="4caaf-109">**ulReserved1**</span><span class="sxs-lookup"><span data-stu-id="4caaf-109">**ulReserved1**</span></span>
  
> <span data-ttu-id="4caaf-110">Зарезервировано; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="4caaf-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="4caaf-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="4caaf-111">**cValues**</span></span>
  
> <span data-ttu-id="4caaf-112">Число свойств в массиве значение свойства, на который указывает член **rgPropVals** .</span><span class="sxs-lookup"><span data-stu-id="4caaf-112">Count of properties in the property value array pointed to by the **rgPropVals** member.</span></span> <span data-ttu-id="4caaf-113">Член **cValues** может быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="4caaf-113">The **cValues** member can be zero.</span></span> 
    
 <span data-ttu-id="4caaf-114">**rgPropVals**</span><span class="sxs-lookup"><span data-stu-id="4caaf-114">**rgPropVals**</span></span>
  
> <span data-ttu-id="4caaf-115">Указатель на массив значений свойства, описывающие свойства для получателя.</span><span class="sxs-lookup"><span data-stu-id="4caaf-115">Pointer to a property value array describing the properties for the recipient.</span></span> <span data-ttu-id="4caaf-116">Элемент **rgPropVals** может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="4caaf-116">The **rgPropVals** member can be NULL.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4caaf-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="4caaf-117">Remarks</span></span>

<span data-ttu-id="4caaf-118">Структура с **ADRENTRY** описание свойств, относящихся к одного получателя.</span><span class="sxs-lookup"><span data-stu-id="4caaf-118">An **ADRENTRY** structure describes properties that belong to a single recipient.</span></span> <span data-ttu-id="4caaf-119">Следующие свойства, которые обычно используются для описания получателя.</span><span class="sxs-lookup"><span data-stu-id="4caaf-119">The properties that are typically used to describe a recipient include the following:</span></span> 
  
 <span data-ttu-id="4caaf-120">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4caaf-120">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
  
 <span data-ttu-id="4caaf-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4caaf-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
  
 <span data-ttu-id="4caaf-122">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4caaf-122">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
  
 <span data-ttu-id="4caaf-123">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4caaf-123">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
  
<span data-ttu-id="4caaf-124">Если идентификатор записи или свойство **PR_ENTRYID** появится в массиве [SPropValue](spropvalue.md) для получателя, это значит, что получатель была устранена.</span><span class="sxs-lookup"><span data-stu-id="4caaf-124">When an entry identifier or **PR_ENTRYID** property appears in the [SPropValue](spropvalue.md) array for a recipient, this indicates that the recipient has been resolved.</span></span> <span data-ttu-id="4caaf-125">Клиенты вызовите метод [IAddrBook::ResolveName](iaddrbook-resolvename.md) для убедитесь в том, что всех получателей в списке получателей исходящих сообщений, устранены.</span><span class="sxs-lookup"><span data-stu-id="4caaf-125">Clients call the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method to make sure that all recipients in the recipient list of an outgoing message have been resolved.</span></span> <span data-ttu-id="4caaf-126">Только разрешения получателей можно отправить с сообщениями.</span><span class="sxs-lookup"><span data-stu-id="4caaf-126">Only resolved recipients can be sent with messages.</span></span> 
  
 <span data-ttu-id="4caaf-127">**ADRENTRY** структуры обычно объединяются для создания массива для элемента **aEntries** структуры [ADRLIST](adrlist.md) .</span><span class="sxs-lookup"><span data-stu-id="4caaf-127">**ADRENTRY** structures are typically combined to form an array for the **aEntries** member of an [ADRLIST](adrlist.md) structure.</span></span> 
  
 <span data-ttu-id="4caaf-128">**ADRENTRY** структуры и структуры [SRow](srow.md) идентичны, так как они содержали зарезервированного элемента, массив значений свойств и количество значений в массиве.</span><span class="sxs-lookup"><span data-stu-id="4caaf-128">**ADRENTRY** structures and [SRow](srow.md) structures are identical because they both contain a reserved member, an array of property values, and a count of values in the array.</span></span> <span data-ttu-id="4caaf-129">В то время как структуры **ADRENTRY** объединяются для создания члена **aEntries** структуры **ADRLIST** , **SRow** структуры объединяются для создания члена **aRow** структуры [SRowSet](srowset.md) .</span><span class="sxs-lookup"><span data-stu-id="4caaf-129">Whereas **ADRENTRY** structures are combined to form the **aEntries** member of an **ADRLIST** structure, **SRow** structures are combined to form the **aRow** member of an [SRowSet](srowset.md) structure.</span></span> <span data-ttu-id="4caaf-130">Обоих типов структур следуйте этим правилам для распределения, подразумевает, что структуру **SRowSet** , полученной из таблицы содержимого контейнера адресной книги может привести к структуре **ADRLIST** и использовать.</span><span class="sxs-lookup"><span data-stu-id="4caaf-130">Both types of structures follow the same allocation rules, implying that an **SRowSet** structure that is retrieved from the contents table of an address book container can be cast to an **ADRLIST** structure and used as is.</span></span> 
  
<span data-ttu-id="4caaf-131">Структура с **ADRENTRY** может быть пустым.</span><span class="sxs-lookup"><span data-stu-id="4caaf-131">An **ADRENTRY** structure can be empty.</span></span> <span data-ttu-id="4caaf-132">Например структуру **ADRENTRY** , содержащихся в структуре **ADRLIST** указывает параметр _lppAdrList_ в вызове **IAddrBook::Address** может быть пустым при удалении получателя.</span><span class="sxs-lookup"><span data-stu-id="4caaf-132">For example, an **ADRENTRY** structure that is contained in the **ADRLIST** structure pointed to by the  _lppAdrList_ parameter in a call to **IAddrBook::Address** can be empty when a recipient is being removed.</span></span> 
  
<span data-ttu-id="4caaf-133">Дополнительные сведения о том, как выделить память для структуры **ADRENTRY** можно [Памяти ADRLIST и SRowSet структур](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="4caaf-133">For more information about how to allocate memory for **ADRENTRY** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4caaf-134">См. также</span><span class="sxs-lookup"><span data-stu-id="4caaf-134">See also</span></span>



[<span data-ttu-id="4caaf-135">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="4caaf-135">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="4caaf-136">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="4caaf-136">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="4caaf-137">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="4caaf-137">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="4caaf-138">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="4caaf-138">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="4caaf-139">SRow</span><span class="sxs-lookup"><span data-stu-id="4caaf-139">SRow</span></span>](srow.md)
  
[<span data-ttu-id="4caaf-140">SRowSet</span><span class="sxs-lookup"><span data-stu-id="4caaf-140">SRowSet</span></span>](srowset.md)


[<span data-ttu-id="4caaf-141">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="4caaf-141">MAPI Structures</span></span>](mapi-structures.md)

