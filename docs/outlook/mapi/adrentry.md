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
ms.openlocfilehash: 36e0218c9e4e312a138bef7517242f74079212c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421440"
---
# <a name="adrentry"></a><span data-ttu-id="86821-103">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="86821-103">ADRENTRY</span></span>

  
  
<span data-ttu-id="86821-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86821-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86821-105">Описывает ноль или более свойств, принадлежащих получателю.</span><span class="sxs-lookup"><span data-stu-id="86821-105">Describes zero or more properties that belong to a recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="86821-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="86821-106">Header file:</span></span>  <br/> |<span data-ttu-id="86821-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="86821-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _ADRENTRY
{
  ULONG ulReserved1;
  ULONG cValues;
  LPSPropValue rgPropVals;
} ADRENTRY, FAR *LPADRENTRY;

```

## <a name="members"></a><span data-ttu-id="86821-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="86821-108">Members</span></span>

 <span data-ttu-id="86821-109">**ulReserved1**</span><span class="sxs-lookup"><span data-stu-id="86821-109">**ulReserved1**</span></span>
  
> <span data-ttu-id="86821-110">Резервирования должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="86821-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="86821-111">**квалуес**</span><span class="sxs-lookup"><span data-stu-id="86821-111">**cValues**</span></span>
  
> <span data-ttu-id="86821-112">Количество свойств в массиве значений свойств, на которое указывает элемент **ргпропвалс** .</span><span class="sxs-lookup"><span data-stu-id="86821-112">Count of properties in the property value array pointed to by the **rgPropVals** member.</span></span> <span data-ttu-id="86821-113">Элемент **квалуес** может иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="86821-113">The **cValues** member can be zero.</span></span> 
    
 <span data-ttu-id="86821-114">**ргпропвалс**</span><span class="sxs-lookup"><span data-stu-id="86821-114">**rgPropVals**</span></span>
  
> <span data-ttu-id="86821-115">Указатель на массив значений свойств, описывающий свойства получателя.</span><span class="sxs-lookup"><span data-stu-id="86821-115">Pointer to a property value array describing the properties for the recipient.</span></span> <span data-ttu-id="86821-116">Элемент **ргпропвалс** может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="86821-116">The **rgPropVals** member can be NULL.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="86821-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="86821-117">Remarks</span></span>

<span data-ttu-id="86821-118">Структура **адрентри** описывает свойства, принадлежащие одному получателю.</span><span class="sxs-lookup"><span data-stu-id="86821-118">An **ADRENTRY** structure describes properties that belong to a single recipient.</span></span> <span data-ttu-id="86821-119">Ниже перечислены свойства, которые обычно используются для описания получателя.</span><span class="sxs-lookup"><span data-stu-id="86821-119">The properties that are typically used to describe a recipient include the following:</span></span> 
  
 <span data-ttu-id="86821-120">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="86821-120">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
  
 <span data-ttu-id="86821-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="86821-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
  
 <span data-ttu-id="86821-122">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="86821-122">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
  
 <span data-ttu-id="86821-123">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="86821-123">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
  
<span data-ttu-id="86821-124">Если в массиве [спропвалуе](spropvalue.md) для получателя отображается идентификатор записи или свойство **PR_ENTRYID** , это означает, что получатель разрешен.</span><span class="sxs-lookup"><span data-stu-id="86821-124">When an entry identifier or **PR_ENTRYID** property appears in the [SPropValue](spropvalue.md) array for a recipient, this indicates that the recipient has been resolved.</span></span> <span data-ttu-id="86821-125">Клиенты вызывают метод [IAddrBook:: ресолвенаме](iaddrbook-resolvename.md) , чтобы убедиться, что все получатели в списке получателей исходящих сообщений разрешены.</span><span class="sxs-lookup"><span data-stu-id="86821-125">Clients call the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method to make sure that all recipients in the recipient list of an outgoing message have been resolved.</span></span> <span data-ttu-id="86821-126">С сообщениями можно отправлять только разрешенных получателей.</span><span class="sxs-lookup"><span data-stu-id="86821-126">Only resolved recipients can be sent with messages.</span></span> 
  
 <span data-ttu-id="86821-127">Структуры **адрентри** , как правило, объединены в виде массива для элемента **аентриес** структуры [ADRLIST](adrlist.md) .</span><span class="sxs-lookup"><span data-stu-id="86821-127">**ADRENTRY** structures are typically combined to form an array for the **aEntries** member of an [ADRLIST](adrlist.md) structure.</span></span> 
  
 <span data-ttu-id="86821-128">Структуры **адрентри** и структуры [сров](srow.md) идентичны, так как они содержат зарезервированный элемент, массив значений свойств и число значений в массиве.</span><span class="sxs-lookup"><span data-stu-id="86821-128">**ADRENTRY** structures and [SRow](srow.md) structures are identical because they both contain a reserved member, an array of property values, and a count of values in the array.</span></span> <span data-ttu-id="86821-129">В то время как структуры **адрентри** объединены для формирования элемента **аентриес** структуры **ADRLIST** , структуры **сров** объединяются для создания **аров** члена структуры [SRowSet](srowset.md) .</span><span class="sxs-lookup"><span data-stu-id="86821-129">Whereas **ADRENTRY** structures are combined to form the **aEntries** member of an **ADRLIST** structure, **SRow** structures are combined to form the **aRow** member of an [SRowSet](srowset.md) structure.</span></span> <span data-ttu-id="86821-130">Оба типа структур следуют одним и тем же правилам выделения, подразумевая, что структура **SRowSet** , получаемая из таблицы содержимого контейнера адресной книги, может быть приведена к структуре **ADRLIST** и использоваться как есть.</span><span class="sxs-lookup"><span data-stu-id="86821-130">Both types of structures follow the same allocation rules, implying that an **SRowSet** structure that is retrieved from the contents table of an address book container can be cast to an **ADRLIST** structure and used as is.</span></span> 
  
<span data-ttu-id="86821-131">Структура **адрентри** может быть пустой.</span><span class="sxs-lookup"><span data-stu-id="86821-131">An **ADRENTRY** structure can be empty.</span></span> <span data-ttu-id="86821-132">Например, структура **адрентри** , которая находится в структуре **ADRLIST** , на которую указывает параметр _лппадрлист_ при вызове **IAddrBook:: Address** может быть пустым при удалении получателя.</span><span class="sxs-lookup"><span data-stu-id="86821-132">For example, an **ADRENTRY** structure that is contained in the **ADRLIST** structure pointed to by the  _lppAdrList_ parameter in a call to **IAddrBook::Address** can be empty when a recipient is being removed.</span></span> 
  
<span data-ttu-id="86821-133">Дополнительные сведения о том, как выделить память для структур **адрентри** , можно узнать в статье [Управление памятью для структур ADRLIST и SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="86821-133">For more information about how to allocate memory for **ADRENTRY** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="86821-134">См. также</span><span class="sxs-lookup"><span data-stu-id="86821-134">See also</span></span>



[<span data-ttu-id="86821-135">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="86821-135">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="86821-136">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="86821-136">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="86821-137">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="86821-137">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="86821-138">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="86821-138">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="86821-139">SRow</span><span class="sxs-lookup"><span data-stu-id="86821-139">SRow</span></span>](srow.md)
  
[<span data-ttu-id="86821-140">SRowSet</span><span class="sxs-lookup"><span data-stu-id="86821-140">SRowSet</span></span>](srowset.md)


[<span data-ttu-id="86821-141">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="86821-141">MAPI Structures</span></span>](mapi-structures.md)

