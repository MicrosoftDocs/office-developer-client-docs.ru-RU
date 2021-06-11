---
title: SRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRowSet
api_type:
- COM
ms.assetid: 7e3761be-afd6-46cb-9a08-25e9016c1241
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 63cef6ef2bb26e8b723c60fe01dd6771aa070ae8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407258"
---
# <a name="srowset"></a><span data-ttu-id="97fd4-103">SRowSet</span><span class="sxs-lookup"><span data-stu-id="97fd4-103">SRowSet</span></span>

  
  
<span data-ttu-id="97fd4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97fd4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97fd4-105">Содержит массив [структур SRow.](srow.md)</span><span class="sxs-lookup"><span data-stu-id="97fd4-105">Contains an array of [SRow](srow.md) structures.</span></span> <span data-ttu-id="97fd4-106">Каждая **структура SRow** описывает строку из таблицы.</span><span class="sxs-lookup"><span data-stu-id="97fd4-106">Each **SRow** structure describes a row from a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="97fd4-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="97fd4-107">Header file:</span></span>  <br/> |<span data-ttu-id="97fd4-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="97fd4-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="97fd4-109">Связанные макрос:</span><span class="sxs-lookup"><span data-stu-id="97fd4-109">Related macros:</span></span>  <br/> |<span data-ttu-id="97fd4-110">[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md)</span><span class="sxs-lookup"><span data-stu-id="97fd4-110">[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md)</span></span> <br/> |
   
```cpp
typedef struct _SRowSet
{
  ULONG cRows;
  SRow aRow[MAPI_DIM];
} SRowSet, FAR *LPSRowSet;

```

## <a name="members"></a><span data-ttu-id="97fd4-111">"Участники"</span><span class="sxs-lookup"><span data-stu-id="97fd4-111">Members</span></span>

 <span data-ttu-id="97fd4-112">**cRows**</span><span class="sxs-lookup"><span data-stu-id="97fd4-112">**cRows**</span></span>
  
> <span data-ttu-id="97fd4-113">Количество **структур SRow** в **члене aRow.**</span><span class="sxs-lookup"><span data-stu-id="97fd4-113">Count of **SRow** structures in the **aRow** member.</span></span> 
    
 <span data-ttu-id="97fd4-114">**aRow**</span><span class="sxs-lookup"><span data-stu-id="97fd4-114">**aRow**</span></span>
  
> <span data-ttu-id="97fd4-115">Массив **структур SRow.**</span><span class="sxs-lookup"><span data-stu-id="97fd4-115">Array of **SRow** structures.</span></span> <span data-ttu-id="97fd4-116">Каждая строка в таблице имеет одну структуру.</span><span class="sxs-lookup"><span data-stu-id="97fd4-116">There is one structure for each row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="97fd4-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="97fd4-117">Remarks</span></span>

<span data-ttu-id="97fd4-118">Структура **SRowSet** используется для описания нескольких строк данных из таблицы.</span><span class="sxs-lookup"><span data-stu-id="97fd4-118">An **SRowSet** structure is used to describe multiple rows of data from a table.</span></span> <span data-ttu-id="97fd4-119">**Структуры SRowSet** используются в [методах интерфейса IAddrBook,](iaddrbookimapiprop.md) [ITableData](itabledataiunknown.md)и [IMAPITable,](imapitableiunknown.md) а также в следующих функциях:</span><span class="sxs-lookup"><span data-stu-id="97fd4-119">**SRowSet** structures are used in the [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md), and [IMAPITable](imapitableiunknown.md) interface methods, in addition to the following functions:</span></span> 
  
- [<span data-ttu-id="97fd4-120">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="97fd4-120">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
- [<span data-ttu-id="97fd4-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="97fd4-121">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="97fd4-122">FreeProws</span><span class="sxs-lookup"><span data-stu-id="97fd4-122">FreeProws</span></span>](freeprows.md)
    
 <span data-ttu-id="97fd4-123">**Структуры SRowSet** определяются так же, как структуры [ADRLIST,](adrlist.md) что позволяет рассматривать строки таблицы получателей и записи в списке адресов.</span><span class="sxs-lookup"><span data-stu-id="97fd4-123">**SRowSet** structures are defined the same as [ADRLIST](adrlist.md) structures to allow the rows of a recipient table and the entries in an address list to be treated the same.</span></span> <span data-ttu-id="97fd4-124">Как **структуры SRowSet,** так и **структуры ADRLIST** можно передать таким методам, как [IMessage::ModifyRecipients](imessage-modifyrecipients.md) и [IAddrBook::Address.](iaddrbook-address.md)</span><span class="sxs-lookup"><span data-stu-id="97fd4-124">Both **SRowSet** structures and **ADRLIST** structures can be passed to methods such as [IMessage::ModifyRecipients](imessage-modifyrecipients.md) and [IAddrBook::Address](iaddrbook-address.md).</span></span> 
  
<span data-ttu-id="97fd4-125">Кроме того, правила распределения памяти для **структур SRowSet** такие же, как и для **структур ADRLIST.**</span><span class="sxs-lookup"><span data-stu-id="97fd4-125">Also, the rules for memory allocation for **SRowSet** structures are the same as for **ADRLIST** structures.</span></span> <span data-ttu-id="97fd4-126">Чтобы резюмировать, каждая структура [SPropValue](spropvalue.md) в массиве, на который указывает член **lpProps** каждой строки в наборе строк, должна быть выделена отдельно с помощью [MAPIAllocateBuffer](mapiallocatebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="97fd4-126">To summarize, each [SPropValue](spropvalue.md) structure in the array pointed to by the **lpProps** member of each row in the row set must be allocated separately using [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span> <span data-ttu-id="97fd4-127">Каждая структура значения свойств также должна быть расположена с помощью [MAPIFreeBuffer](mapifreebuffer.md) перед сделкой структуры **SRowSet,** чтобы не потерять указатели на выделенные **структуры SPropValue.**</span><span class="sxs-lookup"><span data-stu-id="97fd4-127">Each property value structure must also be deallocated using [MAPIFreeBuffer](mapifreebuffer.md) before the deallocation of its **SRowSet** structure so that pointers to the allocated **SPropValue** structures are not lost.</span></span> <span data-ttu-id="97fd4-128">Выделенная память строки может быть сохранена и повторно использоваться вне контекста **структуры SRowSet.**</span><span class="sxs-lookup"><span data-stu-id="97fd4-128">A row's allocated memory can then be preserved and reused outside the context of the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="97fd4-129">Дополнительные сведения о выделении памяти для структур **SRowSet** см. в статью Управление памятью [для структур ADRLIST и SRowSet.](managing-memory-for-adrlist-and-srowset-structures.md)</span><span class="sxs-lookup"><span data-stu-id="97fd4-129">For more information about how the memory for **SRowSet** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="97fd4-130">См. также</span><span class="sxs-lookup"><span data-stu-id="97fd4-130">See also</span></span>



[<span data-ttu-id="97fd4-131">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="97fd4-131">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="97fd4-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="97fd4-132">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="97fd4-133">SRow</span><span class="sxs-lookup"><span data-stu-id="97fd4-133">SRow</span></span>](srow.md)
  
[<span data-ttu-id="97fd4-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="97fd4-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="97fd4-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="97fd4-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="97fd4-136">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="97fd4-136">MAPI Structures</span></span>](mapi-structures.md)

