---
title: FLATENTRYLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATENTRYLIST
api_type:
- COM
ms.assetid: b465d015-9b62-4986-b0df-118121f60602
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bc511ea4b3ec4eea9e38f744bcb8f277108085cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336899"
---
# <a name="flatentrylist"></a><span data-ttu-id="dd147-103">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="dd147-103">FLATENTRYLIST</span></span>

<span data-ttu-id="dd147-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd147-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd147-105">Содержит массив структур [флатентри](flatentry.md) .</span><span class="sxs-lookup"><span data-stu-id="dd147-105">Contains an array of [FLATENTRY](flatentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd147-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="dd147-106">Header file:</span></span>  <br/> |<span data-ttu-id="dd147-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="dd147-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="dd147-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="dd147-108">Related macros:</span></span>  <br/> |<span data-ttu-id="dd147-109">[Кбфлатентрилист](cbflatentrylist.md), [кбневфлатентрилист](cbnewflatentrylist.md)</span><span class="sxs-lookup"><span data-stu-id="dd147-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cEntries;
  ULONG cbEntries;
  BYTE abEntries[MAPI_DIM];
} FLATENTRYLIST, FAR *LPFLATENTRYLIST;

```

## <a name="members"></a><span data-ttu-id="dd147-110">Members</span><span class="sxs-lookup"><span data-stu-id="dd147-110">Members</span></span>

<span data-ttu-id="dd147-111">**Центриес**</span><span class="sxs-lookup"><span data-stu-id="dd147-111">**cEntries**</span></span>
  
> <span data-ttu-id="dd147-112">Количество структур **флатентри** в массиве, описываемом членом **абентриес** .</span><span class="sxs-lookup"><span data-stu-id="dd147-112">Count of **FLATENTRY** structures in the array described by the **abEntries** member.</span></span> 
    
<span data-ttu-id="dd147-113">**Кбентриес**</span><span class="sxs-lookup"><span data-stu-id="dd147-113">**cbEntries**</span></span>
  
> <span data-ttu-id="dd147-114">Количество байтов в массиве, описываемом **абентриес**.</span><span class="sxs-lookup"><span data-stu-id="dd147-114">Count of bytes in the array described by **abEntries**.</span></span> 
    
<span data-ttu-id="dd147-115">**Абентриес**</span><span class="sxs-lookup"><span data-stu-id="dd147-115">**abEntries**</span></span>
  
> <span data-ttu-id="dd147-116">Массив байтов, который содержит одну или несколько структур **флатентри** , упорядоченные в конец.</span><span class="sxs-lookup"><span data-stu-id="dd147-116">Byte array that contains one or more **FLATENTRY** structures, arranged end to end.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="dd147-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd147-117">Remarks</span></span>

<span data-ttu-id="dd147-118">В массиве **абентриес** каждая структура **флатентри** выровнена по естественным выровненным границам.</span><span class="sxs-lookup"><span data-stu-id="dd147-118">In the **abEntries** array, each **FLATENTRY** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="dd147-119">Дополнительные байты включаются в качестве внутренних полей, чтобы обеспечить естественное выравнивание между двумя структурами **флатентри** .</span><span class="sxs-lookup"><span data-stu-id="dd147-119">Extra bytes are included as padding to make sure natural alignment between any two **FLATENTRY** structures.</span></span> <span data-ttu-id="dd147-120">Первая структура **флатентри** в массиве всегда выровнена правильно, так как смещение элемента **абентриес** равно 8.</span><span class="sxs-lookup"><span data-stu-id="dd147-120">The first **FLATENTRY** structure in the array is always aligned correctly because the offset of the **abEntries** member is 8.</span></span> <span data-ttu-id="dd147-121">Чтобы вычислить смещение следующей структуры, используйте размер первой записи, округленной вплоть до числа до ближайшего кратного 4.</span><span class="sxs-lookup"><span data-stu-id="dd147-121">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="dd147-122">Чтобы вычислить размер структуры **флатентри** , используйте макрос [кбфлатентри](cbflatentry.md) .</span><span class="sxs-lookup"><span data-stu-id="dd147-122">Use the [CbFLATENTRY](cbflatentry.md) macro to compute the size of a **FLATENTRY** structure.</span></span> 
  
<span data-ttu-id="dd147-123">Например, вторая структура **флатентри** начинается со смещения, состоящего из смещения первой записи плюс длина первого элемента, округленного до следующих четырех байтов.</span><span class="sxs-lookup"><span data-stu-id="dd147-123">For example, the second **FLATENTRY** structure starts at an offset that consists of the offset of the first entry plus the length of the first entry rounded to the next four bytes.</span></span> <span data-ttu-id="dd147-124">Длина первой записи — это длина члена **CB** , а также длина ее элемента **абентри** .</span><span class="sxs-lookup"><span data-stu-id="dd147-124">The length of the first entry is the length of its **cb** member plus the length of its **abEntry** member.</span></span> 
  
<span data-ttu-id="dd147-125">В приведенном ниже примере кода показано, как вычислять смещения в структуре **флатентрилист** .</span><span class="sxs-lookup"><span data-stu-id="dd147-125">The following code sample indicates how to compute offsets in a **FLATENTRYLIST** structure.</span></span> <span data-ttu-id="dd147-126">Предположим, что _лпфлатентри_ является указателем на первую структуру в списке.</span><span class="sxs-lookup"><span data-stu-id="dd147-126">Assume that  _lpFlatEntry_ is a pointer to the first structure in the list.</span></span> 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a><span data-ttu-id="dd147-127">См. также</span><span class="sxs-lookup"><span data-stu-id="dd147-127">See also</span></span>

- [<span data-ttu-id="dd147-128">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="dd147-128">FLATENTRY</span></span>](flatentry.md)
- [<span data-ttu-id="dd147-129">Каноническое свойство PidTagReplyRecipientEntries</span><span class="sxs-lookup"><span data-stu-id="dd147-129">PidTagReplyRecipientEntries Canonical Property</span></span>](pidtagreplyrecipiententries-canonical-property.md)
- [<span data-ttu-id="dd147-130">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="dd147-130">MAPI Structures</span></span>](mapi-structures.md)

