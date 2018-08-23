---
title: ADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRLIST
api_type:
- COM
ms.assetid: 85f0d8a5-6dd3-4f33-b31a-246d286d6286
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 87b91b66807ce79533029a8d5b5c4956bc4d5ce9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565769"
---
# <a name="adrlist"></a><span data-ttu-id="03106-103">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="03106-103">ADRLIST</span></span>

<span data-ttu-id="03106-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03106-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03106-105">Описание ноль или больше свойств, относящихся к одному или нескольким получателям.</span><span class="sxs-lookup"><span data-stu-id="03106-105">Describes zero or more properties that belong to one or more recipients.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="03106-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="03106-106">Header file:</span></span>  <br/> |<span data-ttu-id="03106-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="03106-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="03106-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="03106-108">Related macros:</span></span>  <br/> |<span data-ttu-id="03106-109">[CbADRLIST](cbadrlist.md), [CbNewADRLIST](cbnewadrlist.md) [CbNewADRLIST](cbnewadrlist.md)</span><span class="sxs-lookup"><span data-stu-id="03106-109">[CbADRLIST](cbadrlist.md), [CbNewADRLIST](cbnewadrlist.md), [CbNewADRLIST](cbnewadrlist.md)</span></span> <br/> |
   
```cpp
typedef struct _ADRLIST
{
  ULONG cEntries;
  ADRENTRY aEntries[MAPI_DIM];
} ADRLIST, FAR *LPADRLIST;

```

## <a name="members"></a><span data-ttu-id="03106-110">Members</span><span class="sxs-lookup"><span data-stu-id="03106-110">Members</span></span>

<span data-ttu-id="03106-111">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="03106-111">**cEntries**</span></span>
  
> <span data-ttu-id="03106-112">Число записей в массива, указанного параметром члена **aEntries** .</span><span class="sxs-lookup"><span data-stu-id="03106-112">Count of entries in the array specified by the **aEntries** member.</span></span> 
    
<span data-ttu-id="03106-113">**aEntries**</span><span class="sxs-lookup"><span data-stu-id="03106-113">**aEntries**</span></span>
  
> <span data-ttu-id="03106-114">Массив структур [ADRENTRY](adrentry.md) одной структуры для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="03106-114">Array of [ADRENTRY](adrentry.md) structures, one structure for each recipient.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="03106-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="03106-115">Remarks</span></span>

<span data-ttu-id="03106-116">Структуру **ADRLIST** содержит один или несколько **ADRENTRY** структуры, каждый описанием свойства получателя.</span><span class="sxs-lookup"><span data-stu-id="03106-116">An **ADRLIST** structure contains one or more **ADRENTRY** structures, each describing the properties of a recipient.</span></span> <span data-ttu-id="03106-117">Получатель может быть нерешенные.</span><span class="sxs-lookup"><span data-stu-id="03106-117">A recipient can be unresolved.</span></span> <span data-ttu-id="03106-118">Это означает, что она хватает идентификатор записи в его массив значений свойств.</span><span class="sxs-lookup"><span data-stu-id="03106-118">This means that it is lacking an entry identifier in its array of property values.</span></span> <span data-ttu-id="03106-119">Разрешить получателя означает, что **связей с Общественностью\_ENTRYID** включено это свойство ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="03106-119">A resolved recipient means that the **PR\_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property is included.</span></span> <span data-ttu-id="03106-120">Как правило разрешенных получатели также быть сообщения электронной почты адрес свойство **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="03106-120">Typically, resolved recipients also have an email address the **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="03106-121">Тем не менее адреса электронной почты не требуется.</span><span class="sxs-lookup"><span data-stu-id="03106-121">However, the email address is not required.</span></span> <span data-ttu-id="03106-122">**ADRLIST** структуры используются, например, для описания списка получателей для исходящих сообщений и MAPI для отображения записей в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="03106-122">**ADRLIST** structures are used, for example, to describe the recipient list for an outgoing message and by MAPI to display the entries in the address book.</span></span> 
  
<span data-ttu-id="03106-123">**ADRLIST** структуры напоминать структур [SRowSet](srowset.md) структуры, используемые для представления строки в таблицах.</span><span class="sxs-lookup"><span data-stu-id="03106-123">**ADRLIST** structures resemble [SRowSet](srowset.md) structures the structures used for representing rows in tables.</span></span> <span data-ttu-id="03106-124">На самом деле эти две структуры построены таким образом, чтобы они являются взаимозаменяемыми.</span><span class="sxs-lookup"><span data-stu-id="03106-124">In fact, these two structures are designed so that they can be used interchangeably.</span></span> <span data-ttu-id="03106-125">Оба содержать массив структур, описывающих группы свойств и количество значений в массиве.</span><span class="sxs-lookup"><span data-stu-id="03106-125">Both contain an array of structures describing a group of properties and a count of the values in the array.</span></span> <span data-ttu-id="03106-126">В то время как в структуре **ADRLIST** массив содержит [ADRENTRY](adrentry.md) структуры, в структуре **SRowSet** массив содержит [SRow](srow.md) структуры.</span><span class="sxs-lookup"><span data-stu-id="03106-126">Whereas in the **ADRLIST** structure, the array contains [ADRENTRY](adrentry.md) structures, in the **SRowSet** structure the array contains [SRow](srow.md) structures.</span></span> <span data-ttu-id="03106-127">**ADRENTRY** структуры и структуры **SRow** идентичны в макете.</span><span class="sxs-lookup"><span data-stu-id="03106-127">**ADRENTRY** structures and **SRow** structures are identical in layout.</span></span> <span data-ttu-id="03106-128">Так как **ADRLIST** и **SRowSet** структур выполните те же правила распределения, структуру **SRowSet** , полученной из таблицы содержимого контейнера адресной книги можно привести к структуре **ADRLIST** и использовать.</span><span class="sxs-lookup"><span data-stu-id="03106-128">Because **ADRLIST** and **SRowSet** structures follow the same allocation rules, an **SRowSet** structure that is retrieved from the contents table of an address book container can be cast to an **ADRLIST** structure and used as is.</span></span> 
  
<span data-ttu-id="03106-129">На следующем рисунке показана структура **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="03106-129">The following illustration shows the layout of an **ADRLIST** structure.</span></span> 
  
<span data-ttu-id="03106-130">**Компоненты ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="03106-130">**ADRLIST components**</span></span>
  
<span data-ttu-id="03106-131">![Компоненты ADRLIST] (media/amapi_18.gif "Компоненты ADRLIST")</span><span class="sxs-lookup"><span data-stu-id="03106-131">![ADRLIST components](media/amapi_18.gif "ADRLIST components")</span></span>
  
<span data-ttu-id="03106-132">**ADRENTRY** и [SPropValue](spropvalue.md) частями в структуре **ADRLIST** необходимо выделить и освободить независимо от других частей.</span><span class="sxs-lookup"><span data-stu-id="03106-132">The **ADRENTRY** and [SPropValue](spropvalue.md) portions in an **ADRLIST** structure must be allocated and freed independently of the other parts.</span></span> <span data-ttu-id="03106-133">То есть каждая структура **SPropValue** необходимо выделить по отдельности, после памяти для структуры **ADRENTRY** выделить и освободить перед освобождается структуры **ADRENTRY** .</span><span class="sxs-lookup"><span data-stu-id="03106-133">That is, each **SPropValue** structure must be allocated individually after memory for the **ADRENTRY** structure has been allocated and freed before the **ADRENTRY** structure is freed.</span></span> <span data-ttu-id="03106-134">Эта независимость в обработке памяти позволяет свободно добавить или удалить из списка адресов получателей и отдельных параметров учетной записи получателя.</span><span class="sxs-lookup"><span data-stu-id="03106-134">This independence in handling memory allows recipients and individual recipient properties to be freely added or deleted from the address list.</span></span> 
  
<span data-ttu-id="03106-135">Функции [MAPIAllocateBuffer](mapiallocatebuffer.md) и [MAPIFreeBuffer](mapifreebuffer.md) должен использоваться выделять и освобождать структуры **ADRLIST** и все его части.</span><span class="sxs-lookup"><span data-stu-id="03106-135">The [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIFreeBuffer](mapifreebuffer.md) functions must be used to allocate and free the **ADRLIST** structure and all its parts.</span></span> 
  
<span data-ttu-id="03106-136">Если список получателей слишком велик для размещения в памяти, клиенты могут вызывать метод [IMessage::ModifyRecipients](imessage-modifyrecipients.md) для работы с подмножество списка.</span><span class="sxs-lookup"><span data-stu-id="03106-136">If a recipient list is too large to fit in memory, clients can call the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method to work with a subset of the list.</span></span> <span data-ttu-id="03106-137">Клиенты не следует использовать адресной книги окон в этой ситуации.</span><span class="sxs-lookup"><span data-stu-id="03106-137">Clients should not use the address book common dialog boxes in this situation.</span></span> 
  
<span data-ttu-id="03106-138">Дополнительные сведения о том, как выделить память для структуры **ADRENTRY** можно [Памяти ADRLIST и SRowSet структур](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="03106-138">For more information about how to allocate memory for **ADRENTRY** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="03106-139">См. также</span><span class="sxs-lookup"><span data-stu-id="03106-139">See also</span></span>

- [<span data-ttu-id="03106-140">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="03106-140">ADRENTRY</span></span>](adrentry.md)  
- [<span data-ttu-id="03106-141">CbNewADRLIST</span><span class="sxs-lookup"><span data-stu-id="03106-141">CbNewADRLIST</span></span>](cbnewadrlist.md) 
- [<span data-ttu-id="03106-142">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="03106-142">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md) 
- [<span data-ttu-id="03106-143">SRowSet</span><span class="sxs-lookup"><span data-stu-id="03106-143">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="03106-144">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="03106-144">MAPI Structures</span></span>](mapi-structures.md)

