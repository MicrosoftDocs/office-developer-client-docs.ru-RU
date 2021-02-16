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
# <a name="flatentrylist"></a><span data-ttu-id="f29b2-103">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="f29b2-103">FLATENTRYLIST</span></span>

<span data-ttu-id="f29b2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f29b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f29b2-105">Содержит массив структур [FLATENTRY.](flatentry.md)</span><span class="sxs-lookup"><span data-stu-id="f29b2-105">Contains an array of [FLATENTRY](flatentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f29b2-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f29b2-106">Header file:</span></span>  <br/> |<span data-ttu-id="f29b2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f29b2-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f29b2-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="f29b2-108">Related macros:</span></span>  <br/> |<span data-ttu-id="f29b2-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span><span class="sxs-lookup"><span data-stu-id="f29b2-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cEntries;
  ULONG cbEntries;
  BYTE abEntries[MAPI_DIM];
} FLATENTRYLIST, FAR *LPFLATENTRYLIST;

```

## <a name="members"></a><span data-ttu-id="f29b2-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="f29b2-110">Members</span></span>

<span data-ttu-id="f29b2-111">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="f29b2-111">**cEntries**</span></span>
  
> <span data-ttu-id="f29b2-112">Количество структур **FLATENTRY** в массиве, описываемом членом **abEntries.**</span><span class="sxs-lookup"><span data-stu-id="f29b2-112">Count of **FLATENTRY** structures in the array described by the **abEntries** member.</span></span> 
    
<span data-ttu-id="f29b2-113">**cbEntries**</span><span class="sxs-lookup"><span data-stu-id="f29b2-113">**cbEntries**</span></span>
  
> <span data-ttu-id="f29b2-114">Количество в массиве, описываемом **abEntries.**</span><span class="sxs-lookup"><span data-stu-id="f29b2-114">Count of bytes in the array described by **abEntries**.</span></span> 
    
<span data-ttu-id="f29b2-115">**abEntries**</span><span class="sxs-lookup"><span data-stu-id="f29b2-115">**abEntries**</span></span>
  
> <span data-ttu-id="f29b2-116">Массив byte, содержащий одну или несколько **структур FLATENTRY,** устроив их до конца.</span><span class="sxs-lookup"><span data-stu-id="f29b2-116">Byte array that contains one or more **FLATENTRY** structures, arranged end to end.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f29b2-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="f29b2-117">Remarks</span></span>

<span data-ttu-id="f29b2-118">В **массиве abEntries** каждая **структура FLATENTRY** выравнивается по границам, естественно выровненным.</span><span class="sxs-lookup"><span data-stu-id="f29b2-118">In the **abEntries** array, each **FLATENTRY** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="f29b2-119">Дополнительные байты включаются в качестве заполнения, чтобы убедиться в естественном выравнивании между двумя структурами **FLATENTRY.**</span><span class="sxs-lookup"><span data-stu-id="f29b2-119">Extra bytes are included as padding to make sure natural alignment between any two **FLATENTRY** structures.</span></span> <span data-ttu-id="f29b2-120">Первая структура **FLATENTRY** в массиве всегда выравнивается правильно, так как смещение члена **abEntries** составляет 8.</span><span class="sxs-lookup"><span data-stu-id="f29b2-120">The first **FLATENTRY** structure in the array is always aligned correctly because the offset of the **abEntries** member is 8.</span></span> <span data-ttu-id="f29b2-121">Чтобы вычислить смещение следующей структуры, используйте размер первой записи, округленной до следующего кратного 4.</span><span class="sxs-lookup"><span data-stu-id="f29b2-121">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="f29b2-122">Используйте [макрос CbFLATENTRY](cbflatentry.md) для вычисления размера структуры **FLATENTRY.**</span><span class="sxs-lookup"><span data-stu-id="f29b2-122">Use the [CbFLATENTRY](cbflatentry.md) macro to compute the size of a **FLATENTRY** structure.</span></span> 
  
<span data-ttu-id="f29b2-123">Например, вторая структура **FLATENTRY** начинается со смещения, которое состоит из смещения первой записи и длины первой записи, округленной до следующих четырехбайт.</span><span class="sxs-lookup"><span data-stu-id="f29b2-123">For example, the second **FLATENTRY** structure starts at an offset that consists of the offset of the first entry plus the length of the first entry rounded to the next four bytes.</span></span> <span data-ttu-id="f29b2-124">Длина первой записи — это длина члена **cb** и длина члена **abEntry.**</span><span class="sxs-lookup"><span data-stu-id="f29b2-124">The length of the first entry is the length of its **cb** member plus the length of its **abEntry** member.</span></span> 
  
<span data-ttu-id="f29b2-125">Следующий пример кода показывает, как вычислять смещения в структуре **FLATENTRYLIST.**</span><span class="sxs-lookup"><span data-stu-id="f29b2-125">The following code sample indicates how to compute offsets in a **FLATENTRYLIST** structure.</span></span> <span data-ttu-id="f29b2-126">_Предположим, что lpFlatEntry —_ это указатель на первую структуру в списке.</span><span class="sxs-lookup"><span data-stu-id="f29b2-126">Assume that  _lpFlatEntry_ is a pointer to the first structure in the list.</span></span> 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a><span data-ttu-id="f29b2-127">См. также</span><span class="sxs-lookup"><span data-stu-id="f29b2-127">See also</span></span>

- [<span data-ttu-id="f29b2-128">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="f29b2-128">FLATENTRY</span></span>](flatentry.md)
- [<span data-ttu-id="f29b2-129">Каноническое свойство PidTagReplyRecipientEntries</span><span class="sxs-lookup"><span data-stu-id="f29b2-129">PidTagReplyRecipientEntries Canonical Property</span></span>](pidtagreplyrecipiententries-canonical-property.md)
- [<span data-ttu-id="f29b2-130">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="f29b2-130">MAPI Structures</span></span>](mapi-structures.md)

