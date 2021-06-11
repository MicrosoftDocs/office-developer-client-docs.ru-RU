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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413859"
---
# <a name="flatentrylist"></a><span data-ttu-id="20e4a-103">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="20e4a-103">FLATENTRYLIST</span></span>

<span data-ttu-id="20e4a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20e4a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20e4a-105">Содержит массив [структур FLATENTRY.](flatentry.md)</span><span class="sxs-lookup"><span data-stu-id="20e4a-105">Contains an array of [FLATENTRY](flatentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="20e4a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="20e4a-106">Header file:</span></span>  <br/> |<span data-ttu-id="20e4a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="20e4a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="20e4a-108">Связанные макрос:</span><span class="sxs-lookup"><span data-stu-id="20e4a-108">Related macros:</span></span>  <br/> |<span data-ttu-id="20e4a-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span><span class="sxs-lookup"><span data-stu-id="20e4a-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cEntries;
  ULONG cbEntries;
  BYTE abEntries[MAPI_DIM];
} FLATENTRYLIST, FAR *LPFLATENTRYLIST;

```

## <a name="members"></a><span data-ttu-id="20e4a-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="20e4a-110">Members</span></span>

<span data-ttu-id="20e4a-111">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="20e4a-111">**cEntries**</span></span>
  
> <span data-ttu-id="20e4a-112">Количество структур **FLATENTRY** в массиве, описанного участником **abEntries.**</span><span class="sxs-lookup"><span data-stu-id="20e4a-112">Count of **FLATENTRY** structures in the array described by the **abEntries** member.</span></span> 
    
<span data-ttu-id="20e4a-113">**cbEntries**</span><span class="sxs-lookup"><span data-stu-id="20e4a-113">**cbEntries**</span></span>
  
> <span data-ttu-id="20e4a-114">Количество bytes в массиве, описанного **abEntries**.</span><span class="sxs-lookup"><span data-stu-id="20e4a-114">Count of bytes in the array described by **abEntries**.</span></span> 
    
<span data-ttu-id="20e4a-115">**abEntries**</span><span class="sxs-lookup"><span data-stu-id="20e4a-115">**abEntries**</span></span>
  
> <span data-ttu-id="20e4a-116">Массив Byte, содержащий одну или несколько структур **FLATENTRY,** расположены от конца до конца.</span><span class="sxs-lookup"><span data-stu-id="20e4a-116">Byte array that contains one or more **FLATENTRY** structures, arranged end to end.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="20e4a-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="20e4a-117">Remarks</span></span>

<span data-ttu-id="20e4a-118">В **массиве abEntries** каждая структура **FLATENTRY** выравнивается на естественно выровненной границе.</span><span class="sxs-lookup"><span data-stu-id="20e4a-118">In the **abEntries** array, each **FLATENTRY** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="20e4a-119">Дополнительные байты включены в качестве обивки, чтобы убедиться в естественном выравнивании между двумя **структурами FLATENTRY.**</span><span class="sxs-lookup"><span data-stu-id="20e4a-119">Extra bytes are included as padding to make sure natural alignment between any two **FLATENTRY** structures.</span></span> <span data-ttu-id="20e4a-120">Первая структура **FLATENTRY** в массиве всегда выравнивается правильно, так как смещение члена **abEntries** — 8.</span><span class="sxs-lookup"><span data-stu-id="20e4a-120">The first **FLATENTRY** structure in the array is always aligned correctly because the offset of the **abEntries** member is 8.</span></span> <span data-ttu-id="20e4a-121">Чтобы вычислить смещение следующей структуры, используйте размер первой записи, округленной до следующей несколько из 4.</span><span class="sxs-lookup"><span data-stu-id="20e4a-121">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="20e4a-122">Чтобы вычислить размер структуры **FLATENTRY,** используйте макрос [CbFLATENTRY.](cbflatentry.md)</span><span class="sxs-lookup"><span data-stu-id="20e4a-122">Use the [CbFLATENTRY](cbflatentry.md) macro to compute the size of a **FLATENTRY** structure.</span></span> 
  
<span data-ttu-id="20e4a-123">Например, вторая структура **FLATENTRY** начинается с смещения, состоящего из смещения первой записи плюс длина первого входа, округленного до следующих четырех bytes.</span><span class="sxs-lookup"><span data-stu-id="20e4a-123">For example, the second **FLATENTRY** structure starts at an offset that consists of the offset of the first entry plus the length of the first entry rounded to the next four bytes.</span></span> <span data-ttu-id="20e4a-124">Длина первой записи — это длина члена **cb** плюс длина **абЕнтрийского** члена.</span><span class="sxs-lookup"><span data-stu-id="20e4a-124">The length of the first entry is the length of its **cb** member plus the length of its **abEntry** member.</span></span> 
  
<span data-ttu-id="20e4a-125">В следующем примере кода указывается, как вычислять смещения в структуре **FLATENTRYLIST.**</span><span class="sxs-lookup"><span data-stu-id="20e4a-125">The following code sample indicates how to compute offsets in a **FLATENTRYLIST** structure.</span></span> <span data-ttu-id="20e4a-126">Предположим,  _что lpFlatEntry_ является указателем на первую структуру в списке.</span><span class="sxs-lookup"><span data-stu-id="20e4a-126">Assume that  _lpFlatEntry_ is a pointer to the first structure in the list.</span></span> 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a><span data-ttu-id="20e4a-127">См. также</span><span class="sxs-lookup"><span data-stu-id="20e4a-127">See also</span></span>

- [<span data-ttu-id="20e4a-128">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="20e4a-128">FLATENTRY</span></span>](flatentry.md)
- [<span data-ttu-id="20e4a-129">Каноническое свойство PidTagReplyRecipientEntries</span><span class="sxs-lookup"><span data-stu-id="20e4a-129">PidTagReplyRecipientEntries Canonical Property</span></span>](pidtagreplyrecipiententries-canonical-property.md)
- [<span data-ttu-id="20e4a-130">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="20e4a-130">MAPI Structures</span></span>](mapi-structures.md)

