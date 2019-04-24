---
title: FLATMTSIDLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATMTSIDLIST
api_type:
- COM
ms.assetid: b66c2815-72bc-4535-b34c-899bb830f29e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bd9bfe4d1411b84a7811235aa68728afaefe64ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327309"
---
# <a name="flatmtsidlist"></a><span data-ttu-id="7e6b4-103">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="7e6b4-103">FLATMTSIDLIST</span></span>

  
  
<span data-ttu-id="7e6b4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e6b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e6b4-105">Содержит массив структур [мтсид](mtsid.md) , каждый из которых содержит идентификатор записи MTS (X. 400 Message transporting System).</span><span class="sxs-lookup"><span data-stu-id="7e6b4-105">Contains an array of [MTSID](mtsid.md) structures, each of which contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7e6b4-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="7e6b4-106">Header file:</span></span>  <br/> |<span data-ttu-id="7e6b4-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="7e6b4-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7e6b4-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="7e6b4-108">Related macros:</span></span>  <br/> |<span data-ttu-id="7e6b4-109">[Кбфлатмтсидлист](cbflatmtsidlist.md), [кбневфлатмтсидлист](cbnewflatmtsidlist.md)</span><span class="sxs-lookup"><span data-stu-id="7e6b4-109">[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cMTSIDs;
  ULONG cbMTSIDs;
  BYTE abMTSIDs[MAPI_DIM];
} FLATMTSIDLIST, FAR *LPFLATMTSIDLIST;

```

## <a name="members"></a><span data-ttu-id="7e6b4-110">Members</span><span class="sxs-lookup"><span data-stu-id="7e6b4-110">Members</span></span>

 <span data-ttu-id="7e6b4-111">**Кмтсидс**</span><span class="sxs-lookup"><span data-stu-id="7e6b4-111">**cMTSIDs**</span></span>
  
> <span data-ttu-id="7e6b4-112">Количество структур **мтсид** в массиве, описываемом членом **абмтсидс** .</span><span class="sxs-lookup"><span data-stu-id="7e6b4-112">Count of **MTSID** structures in the array described by the **abMTSIDs** member.</span></span> 
    
 <span data-ttu-id="7e6b4-113">**Кбмтсидс**</span><span class="sxs-lookup"><span data-stu-id="7e6b4-113">**cbMTSIDs**</span></span>
  
> <span data-ttu-id="7e6b4-114">Количество байтов в массиве, описываемом **абмтсидс**.</span><span class="sxs-lookup"><span data-stu-id="7e6b4-114">Count of bytes in the array described by **abMTSIDs**.</span></span>
    
 <span data-ttu-id="7e6b4-115">**Абмтсидс**</span><span class="sxs-lookup"><span data-stu-id="7e6b4-115">**abMTSIDs**</span></span>
  
> <span data-ttu-id="7e6b4-116">Массив байтов, который содержит одну или несколько структур **мтсид** .</span><span class="sxs-lookup"><span data-stu-id="7e6b4-116">Byte array that contains one or more **MTSID** structures.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7e6b4-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="7e6b4-117">Remarks</span></span>

<span data-ttu-id="7e6b4-118">Использование структуры **флатмтсидлист** в сообщениях X. 400 соответствует использованию структуры [флатентрилист](flatentrylist.md) в сообщениях MAPI.</span><span class="sxs-lookup"><span data-stu-id="7e6b4-118">The **FLATMTSIDLIST** structure's use in X.400 messaging corresponds to the [FLATENTRYLIST](flatentrylist.md) structure's use in MAPI messaging.</span></span> <span data-ttu-id="7e6b4-119">В MAPI используются структуры **флатмтсидлист** для хранения свойств X. 400 во время обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="7e6b4-119">MAPI uses **FLATMTSIDLIST** structures to maintain X.400 properties during message handling.</span></span> <span data-ttu-id="7e6b4-120">Поставщики услуг используют структуры **флатмтсидлист** при обработке входящих и исходящих сообщений X. 400.</span><span class="sxs-lookup"><span data-stu-id="7e6b4-120">Service providers use **FLATMTSIDLIST** structures when handling incoming and outgoing X.400 messages.</span></span> 
  
<span data-ttu-id="7e6b4-121">В массиве **абмтсидс** каждая структура **мтсид** выровнена по естественным выровненным границам.</span><span class="sxs-lookup"><span data-stu-id="7e6b4-121">In the **abMTSIDs** array, each **MTSID** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="7e6b4-122">Дополнительные байты включаются в качестве внутренних полей, чтобы обеспечить естественное выравнивание между двумя структурами **мтсид** .</span><span class="sxs-lookup"><span data-stu-id="7e6b4-122">Extra bytes are included as padding to make sure natural alignment between any two **MTSID** structures.</span></span> <span data-ttu-id="7e6b4-123">Первая структура **мтсид** в массиве всегда выровнена правильно, так как смещение элемента **абмтсидс** равно 8.</span><span class="sxs-lookup"><span data-stu-id="7e6b4-123">The first **MTSID** structure in the array is always aligned correctly because the offset of the **abMTSIDs** member is 8.</span></span> <span data-ttu-id="7e6b4-124">Чтобы вычислить смещение следующей структуры, используйте размер первой записи, округленной вплоть до числа до ближайшего кратного 4.</span><span class="sxs-lookup"><span data-stu-id="7e6b4-124">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="7e6b4-125">Чтобы вычислить размер структуры **мтсид** , используйте макрос [кбневмтсид](cbnewmtsid.md) .</span><span class="sxs-lookup"><span data-stu-id="7e6b4-125">Use the [CbNewMTSID](cbnewmtsid.md) macro to compute the size of an **MTSID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7e6b4-126">См. также</span><span class="sxs-lookup"><span data-stu-id="7e6b4-126">See also</span></span>



[<span data-ttu-id="7e6b4-127">CbNewFLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="7e6b4-127">CbNewFLATMTSIDLIST</span></span>](cbnewflatmtsidlist.md)
  
[<span data-ttu-id="7e6b4-128">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="7e6b4-128">FLATENTRYLIST</span></span>](flatentrylist.md)
  
[<span data-ttu-id="7e6b4-129">MTSID</span><span class="sxs-lookup"><span data-stu-id="7e6b4-129">MTSID</span></span>](mtsid.md)


[<span data-ttu-id="7e6b4-130">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="7e6b4-130">MAPI Structures</span></span>](mapi-structures.md)

