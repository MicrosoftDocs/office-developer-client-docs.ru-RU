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
ms.openlocfilehash: 371d0305f8f00e66704bae03f93857c7275b6a10
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589821"
---
# <a name="flatentrylist"></a><span data-ttu-id="acc29-103">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="acc29-103">FLATENTRYLIST</span></span>

<span data-ttu-id="acc29-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="acc29-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="acc29-105">Содержит массив структур [FLATENTRY](flatentry.md) .</span><span class="sxs-lookup"><span data-stu-id="acc29-105">Contains an array of [FLATENTRY](flatentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="acc29-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="acc29-106">Header file:</span></span>  <br/> |<span data-ttu-id="acc29-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="acc29-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="acc29-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="acc29-108">Related macros:</span></span>  <br/> |<span data-ttu-id="acc29-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span><span class="sxs-lookup"><span data-stu-id="acc29-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cEntries;
  ULONG cbEntries;
  BYTE abEntries[MAPI_DIM];
} FLATENTRYLIST, FAR *LPFLATENTRYLIST;

```

## <a name="members"></a><span data-ttu-id="acc29-110">Members</span><span class="sxs-lookup"><span data-stu-id="acc29-110">Members</span></span>

<span data-ttu-id="acc29-111">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="acc29-111">**cEntries**</span></span>
  
> <span data-ttu-id="acc29-112">Число структур **FLATENTRY** в массиве описано участником **abEntries** .</span><span class="sxs-lookup"><span data-stu-id="acc29-112">Count of **FLATENTRY** structures in the array described by the **abEntries** member.</span></span> 
    
<span data-ttu-id="acc29-113">**cbEntries**</span><span class="sxs-lookup"><span data-stu-id="acc29-113">**cbEntries**</span></span>
  
> <span data-ttu-id="acc29-114">Число байт в массиве, описываемых **abEntries**.</span><span class="sxs-lookup"><span data-stu-id="acc29-114">Count of bytes in the array described by **abEntries**.</span></span> 
    
<span data-ttu-id="acc29-115">**abEntries**</span><span class="sxs-lookup"><span data-stu-id="acc29-115">**abEntries**</span></span>
  
> <span data-ttu-id="acc29-116">Массив байтов, который содержит один или несколько **FLATENTRY** структуры, организованы конечных конец.</span><span class="sxs-lookup"><span data-stu-id="acc29-116">Byte array that contains one or more **FLATENTRY** structures, arranged end to end.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="acc29-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="acc29-117">Remarks</span></span>

<span data-ttu-id="acc29-118">В массиве **abEntries** каждого **FLATENTRY** структура выравнивается по границе естественно выравнивания.</span><span class="sxs-lookup"><span data-stu-id="acc29-118">In the **abEntries** array, each **FLATENTRY** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="acc29-119">Дополнительные байты включены как внутренние поля, чтобы сделать проверьте естественным выравниванием между любые две структуры **FLATENTRY** .</span><span class="sxs-lookup"><span data-stu-id="acc29-119">Extra bytes are included as padding to make sure natural alignment between any two **FLATENTRY** structures.</span></span> <span data-ttu-id="acc29-120">Так как смещение член **abEntries** 8 первого **FLATENTRY** структуру в массиве всегда выравнивается правильно.</span><span class="sxs-lookup"><span data-stu-id="acc29-120">The first **FLATENTRY** structure in the array is always aligned correctly because the offset of the **abEntries** member is 8.</span></span> <span data-ttu-id="acc29-121">Чтобы вычислить смещение Далее структуры, используйте размер первой записи округлено до следующего несколькими 4.</span><span class="sxs-lookup"><span data-stu-id="acc29-121">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="acc29-122">Используйте макрос [CbFLATENTRY](cbflatentry.md) для вычисления размер структуры **FLATENTRY** .</span><span class="sxs-lookup"><span data-stu-id="acc29-122">Use the [CbFLATENTRY](cbflatentry.md) macro to compute the size of a **FLATENTRY** structure.</span></span> 
  
<span data-ttu-id="acc29-123">К примеру второй структура **FLATENTRY** начинается со смещением, состоящее из смещение первой записи, а также длина первой записи, округленное до следующие четыре байта.</span><span class="sxs-lookup"><span data-stu-id="acc29-123">For example, the second **FLATENTRY** structure starts at an offset that consists of the offset of the first entry plus the length of the first entry rounded to the next four bytes.</span></span> <span data-ttu-id="acc29-124">Длина первой записи — длина его элементом **Сертификация** плюс длина его **abEntry** элементом.</span><span class="sxs-lookup"><span data-stu-id="acc29-124">The length of the first entry is the length of its **cb** member plus the length of its **abEntry** member.</span></span> 
  
<span data-ttu-id="acc29-125">В следующем примере кода указывает способ вычисления смещения в структуре **FLATENTRYLIST** .</span><span class="sxs-lookup"><span data-stu-id="acc29-125">The following code sample indicates how to compute offsets in a **FLATENTRYLIST** structure.</span></span> <span data-ttu-id="acc29-126">Предположим, что _lpFlatEntry_ — это указатель на структуру первой в списке.</span><span class="sxs-lookup"><span data-stu-id="acc29-126">Assume that  _lpFlatEntry_ is a pointer to the first structure in the list.</span></span> 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a><span data-ttu-id="acc29-127">См. также</span><span class="sxs-lookup"><span data-stu-id="acc29-127">See also</span></span>

- [<span data-ttu-id="acc29-128">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="acc29-128">FLATENTRY</span></span>](flatentry.md)
- [<span data-ttu-id="acc29-129">Каноническое свойство PidTagReplyRecipientEntries</span><span class="sxs-lookup"><span data-stu-id="acc29-129">PidTagReplyRecipientEntries Canonical Property</span></span>](pidtagreplyrecipiententries-canonical-property.md)
- [<span data-ttu-id="acc29-130">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="acc29-130">MAPI Structures</span></span>](mapi-structures.md)

