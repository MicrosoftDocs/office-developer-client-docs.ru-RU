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
ms.openlocfilehash: 5c634fe200dde4bfe6f190f8bfa9e5dfa0868db4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812394"
---
# <a name="srowset"></a><span data-ttu-id="9a5a7-103">SRowSet</span><span class="sxs-lookup"><span data-stu-id="9a5a7-103">SRowSet</span></span>

  
  
<span data-ttu-id="9a5a7-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9a5a7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9a5a7-105">Содержит массив структур [SRow](srow.md) .</span><span class="sxs-lookup"><span data-stu-id="9a5a7-105">Contains an array of [SRow](srow.md) structures.</span></span> <span data-ttu-id="9a5a7-106">Структура каждого **SRow** описывает строку из таблицы.</span><span class="sxs-lookup"><span data-stu-id="9a5a7-106">Each **SRow** structure describes a row from a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9a5a7-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9a5a7-107">Header file:</span></span>  <br/> |<span data-ttu-id="9a5a7-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9a5a7-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9a5a7-109">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="9a5a7-109">Related macros:</span></span>  <br/> |<span data-ttu-id="9a5a7-110">[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md) [SizedSRowSet](sizedsrowset.md)</span><span class="sxs-lookup"><span data-stu-id="9a5a7-110">[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md)</span></span> <br/> |
   
```cpp
typedef struct _SRowSet
{
  ULONG cRows;
  SRow aRow[MAPI_DIM];
} SRowSet, FAR *LPSRowSet;

```

## <a name="members"></a><span data-ttu-id="9a5a7-111">Members</span><span class="sxs-lookup"><span data-stu-id="9a5a7-111">Members</span></span>

 <span data-ttu-id="9a5a7-112">**cRows**</span><span class="sxs-lookup"><span data-stu-id="9a5a7-112">**cRows**</span></span>
  
> <span data-ttu-id="9a5a7-113">Число структур **SRow** в элемент **aRow** .</span><span class="sxs-lookup"><span data-stu-id="9a5a7-113">Count of **SRow** structures in the **aRow** member.</span></span> 
    
 <span data-ttu-id="9a5a7-114">**aRow**</span><span class="sxs-lookup"><span data-stu-id="9a5a7-114">**aRow**</span></span>
  
> <span data-ttu-id="9a5a7-115">Массив структур **SRow** .</span><span class="sxs-lookup"><span data-stu-id="9a5a7-115">Array of **SRow** structures.</span></span> <span data-ttu-id="9a5a7-116">Существует один структуры для каждой строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="9a5a7-116">There is one structure for each row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9a5a7-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="9a5a7-117">Remarks</span></span>

<span data-ttu-id="9a5a7-118">Структура **SRowSet** используется для описания несколько строк данных из таблицы.</span><span class="sxs-lookup"><span data-stu-id="9a5a7-118">An **SRowSet** structure is used to describe multiple rows of data from a table.</span></span> <span data-ttu-id="9a5a7-119">**SRowSet** структуры используются в [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md)и [IMAPITable](imapitableiunknown.md) методов интерфейса, кроме следующих функций:</span><span class="sxs-lookup"><span data-stu-id="9a5a7-119">**SRowSet** structures are used in the [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md), and [IMAPITable](imapitableiunknown.md) interface methods, in addition to the following functions:</span></span> 
  
- [<span data-ttu-id="9a5a7-120">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="9a5a7-120">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
- [<span data-ttu-id="9a5a7-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="9a5a7-121">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="9a5a7-122">FreeProws</span><span class="sxs-lookup"><span data-stu-id="9a5a7-122">FreeProws</span></span>](freeprows.md)
    
 <span data-ttu-id="9a5a7-123">Определения структур **SRowSet** так же, как [ADRLIST](adrlist.md) структуры строк получателей таблицы и операций в список адресов, чтобы быть обрабатывается так же.</span><span class="sxs-lookup"><span data-stu-id="9a5a7-123">**SRowSet** structures are defined the same as [ADRLIST](adrlist.md) structures to allow the rows of a recipient table and the entries in an address list to be treated the same.</span></span> <span data-ttu-id="9a5a7-124">Методы, такие как [IMessage::ModifyRecipients](imessage-modifyrecipients.md) и [IAddrBook::Address](iaddrbook-address.md)могут передаваться **SRowSet** структуры и структуры **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="9a5a7-124">Both **SRowSet** structures and **ADRLIST** structures can be passed to methods such as [IMessage::ModifyRecipients](imessage-modifyrecipients.md) and [IAddrBook::Address](iaddrbook-address.md).</span></span> 
  
<span data-ttu-id="9a5a7-125">Кроме того правила для выделения памяти для структуры **SRowSet** совпадают с требованиями для структуры **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="9a5a7-125">Also, the rules for memory allocation for **SRowSet** structures are the same as for **ADRLIST** structures.</span></span> <span data-ttu-id="9a5a7-126">В целом, каждый [SPropValue](spropvalue.md) структуру в массиве по член **lpProps** каждой строки в строке, на который указывает необходимо выделить отдельно с помощью [MAPIAllocateBuffer](mapiallocatebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="9a5a7-126">To summarize, each [SPropValue](spropvalue.md) structure in the array pointed to by the **lpProps** member of each row in the row set must be allocated separately using [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span> <span data-ttu-id="9a5a7-127">Структура значение каждого свойства должна быть отменено с помощью [MAPIFreeBuffer](mapifreebuffer.md) перед освобождение структуры **SRowSet** , чтобы указатели на выделенный **SPropValue** структуры не сохраняются.</span><span class="sxs-lookup"><span data-stu-id="9a5a7-127">Each property value structure must also be deallocated using [MAPIFreeBuffer](mapifreebuffer.md) before the deallocation of its **SRowSet** structure so that pointers to the allocated **SPropValue** structures are not lost.</span></span> <span data-ttu-id="9a5a7-128">Строки выделенная объема памяти может затем сохранять и повторно использовать вне контекста **SRowSet** структуры.</span><span class="sxs-lookup"><span data-stu-id="9a5a7-128">A row's allocated memory can then be preserved and reused outside the context of the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="9a5a7-129">Дополнительные сведения о том, как следует выделить память для структуры **SRowSet** [Памяти ADRLIST и SRowSet структур](managing-memory-for-adrlist-and-srowset-structures.md)см.</span><span class="sxs-lookup"><span data-stu-id="9a5a7-129">For more information about how the memory for **SRowSet** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9a5a7-130">См. также</span><span class="sxs-lookup"><span data-stu-id="9a5a7-130">See also</span></span>



[<span data-ttu-id="9a5a7-131">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="9a5a7-131">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="9a5a7-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="9a5a7-132">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="9a5a7-133">SRow</span><span class="sxs-lookup"><span data-stu-id="9a5a7-133">SRow</span></span>](srow.md)
  
[<span data-ttu-id="9a5a7-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="9a5a7-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="9a5a7-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="9a5a7-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="9a5a7-136">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="9a5a7-136">MAPI Structures</span></span>](mapi-structures.md)

