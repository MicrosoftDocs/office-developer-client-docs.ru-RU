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
ms.openlocfilehash: a8f17c3cf3d3d00930f87acd004b24f683a3fc8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808448"
---
# <a name="flatentrylist"></a><span data-ttu-id="4f27c-103">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="4f27c-103">FLATENTRYLIST</span></span>

<span data-ttu-id="4f27c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4f27c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4f27c-105">Содержит массив структур [FLATENTRY](flatentry.md) .</span><span class="sxs-lookup"><span data-stu-id="4f27c-105">Contains an array of [FLATENTRY](flatentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4f27c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="4f27c-106">Header file:</span></span>  <br/> |<span data-ttu-id="4f27c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4f27c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4f27c-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="4f27c-108">Related macros:</span></span>  <br/> |<span data-ttu-id="4f27c-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span><span class="sxs-lookup"><span data-stu-id="4f27c-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cEntries;
  ULONG cbEntries;
  BYTE abEntries[MAPI_DIM];
} FLATENTRYLIST, FAR *LPFLATENTRYLIST;

```

## <a name="members"></a><span data-ttu-id="4f27c-110">Members</span><span class="sxs-lookup"><span data-stu-id="4f27c-110">Members</span></span>

<span data-ttu-id="4f27c-111">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="4f27c-111">**cEntries**</span></span>
  
> <span data-ttu-id="4f27c-112">Число структур **FLATENTRY** в массиве описано участником **abEntries** .</span><span class="sxs-lookup"><span data-stu-id="4f27c-112">Count of **FLATENTRY** structures in the array described by the **abEntries** member.</span></span> 
    
<span data-ttu-id="4f27c-113">**cbEntries**</span><span class="sxs-lookup"><span data-stu-id="4f27c-113">**cbEntries**</span></span>
  
> <span data-ttu-id="4f27c-114">Число байт в массиве, описываемых **abEntries**.</span><span class="sxs-lookup"><span data-stu-id="4f27c-114">Count of bytes in the array described by **abEntries**.</span></span> 
    
<span data-ttu-id="4f27c-115">**abEntries**</span><span class="sxs-lookup"><span data-stu-id="4f27c-115">**abEntries**</span></span>
  
> <span data-ttu-id="4f27c-116">Массив байтов, который содержит один или несколько **FLATENTRY** структуры, организованы конечных конец.</span><span class="sxs-lookup"><span data-stu-id="4f27c-116">Byte array that contains one or more **FLATENTRY** structures, arranged end to end.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4f27c-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="4f27c-117">Remarks</span></span>

<span data-ttu-id="4f27c-118">В массиве **abEntries** каждого **FLATENTRY** структура выравнивается по границе естественно выравнивания.</span><span class="sxs-lookup"><span data-stu-id="4f27c-118">In the **abEntries** array, each **FLATENTRY** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="4f27c-119">Дополнительные байты включены как внутренние поля, чтобы сделать проверьте естественным выравниванием между любые две структуры **FLATENTRY** .</span><span class="sxs-lookup"><span data-stu-id="4f27c-119">Extra bytes are included as padding to make sure natural alignment between any two **FLATENTRY** structures.</span></span> <span data-ttu-id="4f27c-120">Так как смещение член **abEntries** 8 первого **FLATENTRY** структуру в массиве всегда выравнивается правильно.</span><span class="sxs-lookup"><span data-stu-id="4f27c-120">The first **FLATENTRY** structure in the array is always aligned correctly because the offset of the **abEntries** member is 8.</span></span> <span data-ttu-id="4f27c-121">Чтобы вычислить смещение Далее структуры, используйте размер первой записи округлено до следующего несколькими 4.</span><span class="sxs-lookup"><span data-stu-id="4f27c-121">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="4f27c-122">Используйте макрос [CbFLATENTRY](cbflatentry.md) для вычисления размер структуры **FLATENTRY** .</span><span class="sxs-lookup"><span data-stu-id="4f27c-122">Use the [CbFLATENTRY](cbflatentry.md) macro to compute the size of a **FLATENTRY** structure.</span></span> 
  
<span data-ttu-id="4f27c-123">К примеру второй структура **FLATENTRY** начинается со смещением, состоящее из смещение первой записи, а также длина первой записи, округленное до следующие четыре байта.</span><span class="sxs-lookup"><span data-stu-id="4f27c-123">For example, the second **FLATENTRY** structure starts at an offset that consists of the offset of the first entry plus the length of the first entry rounded to the next four bytes.</span></span> <span data-ttu-id="4f27c-124">Длина первой записи — длина его элементом **Сертификация** плюс длина его **abEntry** элементом.</span><span class="sxs-lookup"><span data-stu-id="4f27c-124">The length of the first entry is the length of its **cb** member plus the length of its **abEntry** member.</span></span> 
  
<span data-ttu-id="4f27c-125">В следующем примере кода указывает способ вычисления смещения в структуре **FLATENTRYLIST** .</span><span class="sxs-lookup"><span data-stu-id="4f27c-125">The following code sample indicates how to compute offsets in a **FLATENTRYLIST** structure.</span></span> <span data-ttu-id="4f27c-126">Предположим, что _lpFlatEntry_ — это указатель на структуру первой в списке.</span><span class="sxs-lookup"><span data-stu-id="4f27c-126">Assume that  _lpFlatEntry_ is a pointer to the first structure in the list.</span></span> 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a><span data-ttu-id="4f27c-127">См. также</span><span class="sxs-lookup"><span data-stu-id="4f27c-127">See also</span></span>

- [<span data-ttu-id="4f27c-128">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="4f27c-128">FLATENTRY</span></span>](flatentry.md)
- [<span data-ttu-id="4f27c-129">Каноническое свойство PidTagReplyRecipientEntries</span><span class="sxs-lookup"><span data-stu-id="4f27c-129">PidTagReplyRecipientEntries Canonical Property</span></span>](pidtagreplyrecipiententries-canonical-property.md)
- [<span data-ttu-id="4f27c-130">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="4f27c-130">MAPI Structures</span></span>](mapi-structures.md)

