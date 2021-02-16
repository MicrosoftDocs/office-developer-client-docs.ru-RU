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
ms.openlocfilehash: 319c932862615e063a02ffac07e5541b1b20ac7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415917"
---
# <a name="adrlist"></a><span data-ttu-id="9c31c-103">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="9c31c-103">ADRLIST</span></span>

<span data-ttu-id="9c31c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c31c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c31c-105">Описывает нулевое или несколько свойств, принадлежащих одному или более получателям.</span><span class="sxs-lookup"><span data-stu-id="9c31c-105">Describes zero or more properties that belong to one or more recipients.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9c31c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9c31c-106">Header file:</span></span>  <br/> |<span data-ttu-id="9c31c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9c31c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9c31c-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="9c31c-108">Related macros:</span></span>  <br/> |<span data-ttu-id="9c31c-109">[CbADRLIST](cbadrlist.md), [CbNewADRLIST](cbnewadrlist.md), [CbNewADRLIST](cbnewadrlist.md)</span><span class="sxs-lookup"><span data-stu-id="9c31c-109">[CbADRLIST](cbadrlist.md), [CbNewADRLIST](cbnewadrlist.md), [CbNewADRLIST](cbnewadrlist.md)</span></span> <br/> |
   
```cpp
typedef struct _ADRLIST
{
  ULONG cEntries;
  ADRENTRY aEntries[MAPI_DIM];
} ADRLIST, FAR *LPADRLIST;

```

## <a name="members"></a><span data-ttu-id="9c31c-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="9c31c-110">Members</span></span>

<span data-ttu-id="9c31c-111">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="9c31c-111">**cEntries**</span></span>
  
> <span data-ttu-id="9c31c-112">Количество записей в массиве, указанном членом **aEntries.**</span><span class="sxs-lookup"><span data-stu-id="9c31c-112">Count of entries in the array specified by the **aEntries** member.</span></span> 
    
<span data-ttu-id="9c31c-113">**aEntries**</span><span class="sxs-lookup"><span data-stu-id="9c31c-113">**aEntries**</span></span>
  
> <span data-ttu-id="9c31c-114">Массив структур [ADRENTRY,](adrentry.md) по одной структуре для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="9c31c-114">Array of [ADRENTRY](adrentry.md) structures, one structure for each recipient.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9c31c-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="9c31c-115">Remarks</span></span>

<span data-ttu-id="9c31c-116">Структура **ADRLIST** содержит одну или несколько структур **ADRENTRY,** каждая из которых описывает свойства получателя.</span><span class="sxs-lookup"><span data-stu-id="9c31c-116">An **ADRLIST** structure contains one or more **ADRENTRY** structures, each describing the properties of a recipient.</span></span> <span data-ttu-id="9c31c-117">Получатель может быть разрешен.</span><span class="sxs-lookup"><span data-stu-id="9c31c-117">A recipient can be unresolved.</span></span> <span data-ttu-id="9c31c-118">Это означает, что в массиве значений свойств отсутствует идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="9c31c-118">This means that it is lacking an entry identifier in its array of property values.</span></span> <span data-ttu-id="9c31c-119">Разрешенный получатель означает, что включено свойство **\_ PR ENTRYID** ([PidTagEntryId).](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="9c31c-119">A resolved recipient means that the **PR\_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property is included.</span></span> <span data-ttu-id="9c31c-120">Как правило, у разрешенных получателей также есть адрес электронной **почты, PR_EMAIL_ADDRESS** ([PidTagEmailAddress).](pidtagemailaddress-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="9c31c-120">Typically, resolved recipients also have an email address the **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="9c31c-121">Однако адрес электронной почты не требуется.</span><span class="sxs-lookup"><span data-stu-id="9c31c-121">However, the email address is not required.</span></span> <span data-ttu-id="9c31c-122">**Структуры ADRLIST** используются, например, для описания списка получателей для исходяющих сообщений и mapI для отображения записей в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="9c31c-122">**ADRLIST** structures are used, for example, to describe the recipient list for an outgoing message and by MAPI to display the entries in the address book.</span></span> 
  
<span data-ttu-id="9c31c-123">**Структуры ADRLIST** похожи на [структуры SRowSet,](srowset.md) используемые для представления строк в таблицах.</span><span class="sxs-lookup"><span data-stu-id="9c31c-123">**ADRLIST** structures resemble [SRowSet](srowset.md) structures the structures used for representing rows in tables.</span></span> <span data-ttu-id="9c31c-124">Фактически эти две структуры разработаны таким образом, чтобы их можно было использовать взаимозаменяемо.</span><span class="sxs-lookup"><span data-stu-id="9c31c-124">In fact, these two structures are designed so that they can be used interchangeably.</span></span> <span data-ttu-id="9c31c-125">Оба свойства содержат массив структур, описывающий группу свойств, и количество значений в массиве.</span><span class="sxs-lookup"><span data-stu-id="9c31c-125">Both contain an array of structures describing a group of properties and a count of the values in the array.</span></span> <span data-ttu-id="9c31c-126">В то время как в структуре **ADRLIST** массив содержит структуры [ADRENTRY,](adrentry.md) в структуре **SRowSet** массив содержит структуры [SRow.](srow.md)</span><span class="sxs-lookup"><span data-stu-id="9c31c-126">Whereas in the **ADRLIST** structure, the array contains [ADRENTRY](adrentry.md) structures, in the **SRowSet** structure the array contains [SRow](srow.md) structures.</span></span> <span data-ttu-id="9c31c-127">**Структуры ADRENTRY** и **SRow** идентичны в макете.</span><span class="sxs-lookup"><span data-stu-id="9c31c-127">**ADRENTRY** structures and **SRow** structures are identical in layout.</span></span> <span data-ttu-id="9c31c-128">Поскольку структуры **ADRLIST** и **SRowSet** следуют тем же правилам выделения, структура **SRowSet,** извлекаемая из таблицы содержимого контейнера адресной книги, может привестися к структуре **ADRLIST** и использовать как есть.</span><span class="sxs-lookup"><span data-stu-id="9c31c-128">Because **ADRLIST** and **SRowSet** structures follow the same allocation rules, an **SRowSet** structure that is retrieved from the contents table of an address book container can be cast to an **ADRLIST** structure and used as is.</span></span> 
  
<span data-ttu-id="9c31c-129">На следующем рисунке показан макет структуры **ADRLIST.**</span><span class="sxs-lookup"><span data-stu-id="9c31c-129">The following illustration shows the layout of an **ADRLIST** structure.</span></span> 
  
<span data-ttu-id="9c31c-130">**Компоненты ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="9c31c-130">**ADRLIST components**</span></span>
  
<span data-ttu-id="9c31c-131">![Компоненты ADRLIST компоненты](media/amapi_18.gif "ADRLIST")</span><span class="sxs-lookup"><span data-stu-id="9c31c-131">![ADRLIST components](media/amapi_18.gif "ADRLIST components")</span></span>
  
<span data-ttu-id="9c31c-132">Части **ADRENTRY** и [SPropValue](spropvalue.md) в структуре **ADRLIST** должны быть выделены и освобождены независимо от других частей.</span><span class="sxs-lookup"><span data-stu-id="9c31c-132">The **ADRENTRY** and [SPropValue](spropvalue.md) portions in an **ADRLIST** structure must be allocated and freed independently of the other parts.</span></span> <span data-ttu-id="9c31c-133">То есть каждая структура **SPropValue** должна быть выделена по отдельности после того, как память для структуры **ADRENTRY** была выделена и освобождена до того, как структура **ADRENTRY** будет освобождена.</span><span class="sxs-lookup"><span data-stu-id="9c31c-133">That is, each **SPropValue** structure must be allocated individually after memory for the **ADRENTRY** structure has been allocated and freed before the **ADRENTRY** structure is freed.</span></span> <span data-ttu-id="9c31c-134">Такая независимость в обработке памяти позволяет получателям и отдельным свойствам получателей свободно добавляться или удаляться из списка адресов.</span><span class="sxs-lookup"><span data-stu-id="9c31c-134">This independence in handling memory allows recipients and individual recipient properties to be freely added or deleted from the address list.</span></span> 
  
<span data-ttu-id="9c31c-135">Функции [MAPIAllocateBuffer](mapiallocatebuffer.md) и [MAPIFreeBuffer](mapifreebuffer.md) необходимо использовать для выделения и освободить структуру **ADRLIST** и все ее части.</span><span class="sxs-lookup"><span data-stu-id="9c31c-135">The [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIFreeBuffer](mapifreebuffer.md) functions must be used to allocate and free the **ADRLIST** structure and all its parts.</span></span> 
  
<span data-ttu-id="9c31c-136">Если список получателей слишком велик, чтобы вместить его в память, клиенты могут вызвать метод [IMessage::ModifyRecipients](imessage-modifyrecipients.md) для работы с подмножеством списка.</span><span class="sxs-lookup"><span data-stu-id="9c31c-136">If a recipient list is too large to fit in memory, clients can call the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method to work with a subset of the list.</span></span> <span data-ttu-id="9c31c-137">В этой ситуации клиенты не должны использовать общие диалоги адресной книги.</span><span class="sxs-lookup"><span data-stu-id="9c31c-137">Clients should not use the address book common dialog boxes in this situation.</span></span> 
  
<span data-ttu-id="9c31c-138">Дополнительные сведения о выделении памяти для структур **ADRENTRY** см. в под управлением памятью [для ADRLIST и структур SRowSet.](managing-memory-for-adrlist-and-srowset-structures.md)</span><span class="sxs-lookup"><span data-stu-id="9c31c-138">For more information about how to allocate memory for **ADRENTRY** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9c31c-139">См. также</span><span class="sxs-lookup"><span data-stu-id="9c31c-139">See also</span></span>

- [<span data-ttu-id="9c31c-140">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="9c31c-140">ADRENTRY</span></span>](adrentry.md)  
- [<span data-ttu-id="9c31c-141">CbNewADRLIST</span><span class="sxs-lookup"><span data-stu-id="9c31c-141">CbNewADRLIST</span></span>](cbnewadrlist.md) 
- [<span data-ttu-id="9c31c-142">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="9c31c-142">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md) 
- [<span data-ttu-id="9c31c-143">SRowSet</span><span class="sxs-lookup"><span data-stu-id="9c31c-143">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="9c31c-144">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="9c31c-144">MAPI Structures</span></span>](mapi-structures.md)

