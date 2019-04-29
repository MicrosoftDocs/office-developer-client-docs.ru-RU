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
# <a name="adrlist"></a><span data-ttu-id="c32f3-103">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="c32f3-103">ADRLIST</span></span>

<span data-ttu-id="c32f3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c32f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c32f3-105">Описывает ноль или более свойств, относящихся к одному или нескольким получателям.</span><span class="sxs-lookup"><span data-stu-id="c32f3-105">Describes zero or more properties that belong to one or more recipients.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c32f3-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c32f3-106">Header file:</span></span>  <br/> |<span data-ttu-id="c32f3-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="c32f3-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c32f3-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="c32f3-108">Related macros:</span></span>  <br/> |<span data-ttu-id="c32f3-109">[Кбадрлист](cbadrlist.md), [кбневадрлист](cbnewadrlist.md), [кбневадрлист](cbnewadrlist.md)</span><span class="sxs-lookup"><span data-stu-id="c32f3-109">[CbADRLIST](cbadrlist.md), [CbNewADRLIST](cbnewadrlist.md), [CbNewADRLIST](cbnewadrlist.md)</span></span> <br/> |
   
```cpp
typedef struct _ADRLIST
{
  ULONG cEntries;
  ADRENTRY aEntries[MAPI_DIM];
} ADRLIST, FAR *LPADRLIST;

```

## <a name="members"></a><span data-ttu-id="c32f3-110">Members</span><span class="sxs-lookup"><span data-stu-id="c32f3-110">Members</span></span>

<span data-ttu-id="c32f3-111">**Центриес**</span><span class="sxs-lookup"><span data-stu-id="c32f3-111">**cEntries**</span></span>
  
> <span data-ttu-id="c32f3-112">Количество записей в массиве, указанном элементом **аентриес** .</span><span class="sxs-lookup"><span data-stu-id="c32f3-112">Count of entries in the array specified by the **aEntries** member.</span></span> 
    
<span data-ttu-id="c32f3-113">**Аентриес**</span><span class="sxs-lookup"><span data-stu-id="c32f3-113">**aEntries**</span></span>
  
> <span data-ttu-id="c32f3-114">Массив структур [адрентри](adrentry.md) , одна структура для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="c32f3-114">Array of [ADRENTRY](adrentry.md) structures, one structure for each recipient.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c32f3-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="c32f3-115">Remarks</span></span>

<span data-ttu-id="c32f3-116">Структура **ADRLIST** содержит одну или несколько структур **адрентри** , каждый из которых описывает свойства получателя.</span><span class="sxs-lookup"><span data-stu-id="c32f3-116">An **ADRLIST** structure contains one or more **ADRENTRY** structures, each describing the properties of a recipient.</span></span> <span data-ttu-id="c32f3-117">Получатель может быть неразрешимым.</span><span class="sxs-lookup"><span data-stu-id="c32f3-117">A recipient can be unresolved.</span></span> <span data-ttu-id="c32f3-118">Это означает, что в массиве значений свойств отсутствует идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="c32f3-118">This means that it is lacking an entry identifier in its array of property values.</span></span> <span data-ttu-id="c32f3-119">Разрешенный получатель означает, что включено свойство (код **\_EntryID** ([PidTagEntryId](pidtagentryid-canonical-property.md))).</span><span class="sxs-lookup"><span data-stu-id="c32f3-119">A resolved recipient means that the **PR\_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property is included.</span></span> <span data-ttu-id="c32f3-120">Как правило, у разрешенных получателей также есть адрес электронной почты для свойства **пр_емаил_аддресс** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c32f3-120">Typically, resolved recipients also have an email address the **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="c32f3-121">Однако адрес электронной почты не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c32f3-121">However, the email address is not required.</span></span> <span data-ttu-id="c32f3-122">Структуры **ADRLIST** используются, например, для описания списка получателей исходящих сообщений и MAPI для отображения записей в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="c32f3-122">**ADRLIST** structures are used, for example, to describe the recipient list for an outgoing message and by MAPI to display the entries in the address book.</span></span> 
  
<span data-ttu-id="c32f3-123">Структуры **ADRLIST** похожи на структуры [SRowSet](srowset.md) структуры, используемые для представления строк в таблицах.</span><span class="sxs-lookup"><span data-stu-id="c32f3-123">**ADRLIST** structures resemble [SRowSet](srowset.md) structures the structures used for representing rows in tables.</span></span> <span data-ttu-id="c32f3-124">На самом деле эти две структуры разрабатываются так, чтобы их можно было использовать в качестве взаимозаменяемых.</span><span class="sxs-lookup"><span data-stu-id="c32f3-124">In fact, these two structures are designed so that they can be used interchangeably.</span></span> <span data-ttu-id="c32f3-125">Оба содержат массив структур, описывающих группу свойств, и число значений в массиве.</span><span class="sxs-lookup"><span data-stu-id="c32f3-125">Both contain an array of structures describing a group of properties and a count of the values in the array.</span></span> <span data-ttu-id="c32f3-126">В отличие от структуры **ADRLIST** , массив содержит структуры [адрентри](adrentry.md) , в структуре **SRowSet** массив содержит [сров](srow.md) структуры.</span><span class="sxs-lookup"><span data-stu-id="c32f3-126">Whereas in the **ADRLIST** structure, the array contains [ADRENTRY](adrentry.md) structures, in the **SRowSet** structure the array contains [SRow](srow.md) structures.</span></span> <span data-ttu-id="c32f3-127">Структуры **адрентри** и структуры **сров** идентичны в макете.</span><span class="sxs-lookup"><span data-stu-id="c32f3-127">**ADRENTRY** structures and **SRow** structures are identical in layout.</span></span> <span data-ttu-id="c32f3-128">Так как структуры **ADRLIST** и **SRowSet** следуют одним и тем же правилам выделения, то структура **SRowSet** , полученная из таблицы содержимого контейнера адресной книги, может быть приведена к структуре **ADRLIST** и использоваться как есть.</span><span class="sxs-lookup"><span data-stu-id="c32f3-128">Because **ADRLIST** and **SRowSet** structures follow the same allocation rules, an **SRowSet** structure that is retrieved from the contents table of an address book container can be cast to an **ADRLIST** structure and used as is.</span></span> 
  
<span data-ttu-id="c32f3-129">На следующем рисунке показан макет структуры **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="c32f3-129">The following illustration shows the layout of an **ADRLIST** structure.</span></span> 
  
<span data-ttu-id="c32f3-130">**Компоненты ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="c32f3-130">**ADRLIST components**</span></span>
  
<span data-ttu-id="c32f3-131">![Компоненты ADRLIST] (media/amapi_18.gif "Компоненты ADRLIST")</span><span class="sxs-lookup"><span data-stu-id="c32f3-131">![ADRLIST components](media/amapi_18.gif "ADRLIST components")</span></span>
  
<span data-ttu-id="c32f3-132">Части **адрентри** и [Спропвалуе](spropvalue.md) в структуре **ADRLIST** должны быть распределены и освобождены независимо от других частей.</span><span class="sxs-lookup"><span data-stu-id="c32f3-132">The **ADRENTRY** and [SPropValue](spropvalue.md) portions in an **ADRLIST** structure must be allocated and freed independently of the other parts.</span></span> <span data-ttu-id="c32f3-133">То есть каждая структура **спропвалуе** должна выделяться отдельно после того, как память для структуры **адрентри** была выделена и освобождена до высвобождения структуры **адрентри** .</span><span class="sxs-lookup"><span data-stu-id="c32f3-133">That is, each **SPropValue** structure must be allocated individually after memory for the **ADRENTRY** structure has been allocated and freed before the **ADRENTRY** structure is freed.</span></span> <span data-ttu-id="c32f3-134">Такая независимость при обработке памяти позволяет получателям и свойствам получателей свободно добавляться или удаляться из списка адресов.</span><span class="sxs-lookup"><span data-stu-id="c32f3-134">This independence in handling memory allows recipients and individual recipient properties to be freely added or deleted from the address list.</span></span> 
  
<span data-ttu-id="c32f3-135">Для выделения и освобождения структуры **ADRLIST** и всех ее частей необходимо использовать функции [мапиаллокатебуффер](mapiallocatebuffer.md) и [мапифрибуффер](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="c32f3-135">The [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIFreeBuffer](mapifreebuffer.md) functions must be used to allocate and free the **ADRLIST** structure and all its parts.</span></span> 
  
<span data-ttu-id="c32f3-136">Если список получателей слишком большой и не помещается в память, клиенты могут вызвать метод [iMessage:: модифиреЦипиентс](imessage-modifyrecipients.md) для работы с подмножеством списка.</span><span class="sxs-lookup"><span data-stu-id="c32f3-136">If a recipient list is too large to fit in memory, clients can call the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method to work with a subset of the list.</span></span> <span data-ttu-id="c32f3-137">В этой ситуации клиенты не должны использовать общие диалоговые окна адресной книги.</span><span class="sxs-lookup"><span data-stu-id="c32f3-137">Clients should not use the address book common dialog boxes in this situation.</span></span> 
  
<span data-ttu-id="c32f3-138">Дополнительные сведения о том, как выделить память для структур **адрентри** , можно узнать в статье [Управление памятью для структур ADRLIST и SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="c32f3-138">For more information about how to allocate memory for **ADRENTRY** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c32f3-139">См. также</span><span class="sxs-lookup"><span data-stu-id="c32f3-139">See also</span></span>

- [<span data-ttu-id="c32f3-140">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="c32f3-140">ADRENTRY</span></span>](adrentry.md)  
- [<span data-ttu-id="c32f3-141">CbNewADRLIST</span><span class="sxs-lookup"><span data-stu-id="c32f3-141">CbNewADRLIST</span></span>](cbnewadrlist.md) 
- [<span data-ttu-id="c32f3-142">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="c32f3-142">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md) 
- [<span data-ttu-id="c32f3-143">SRowSet</span><span class="sxs-lookup"><span data-stu-id="c32f3-143">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="c32f3-144">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="c32f3-144">MAPI Structures</span></span>](mapi-structures.md)

