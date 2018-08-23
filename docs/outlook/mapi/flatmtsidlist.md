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
ms.openlocfilehash: 0f1495549df751c59ab84e2b16fffbaf2f4f9fa5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574722"
---
# <a name="flatmtsidlist"></a><span data-ttu-id="779b8-103">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="779b8-103">FLATMTSIDLIST</span></span>

  
  
<span data-ttu-id="779b8-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="779b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="779b8-105">Содержит массив структур [MTSID](mtsid.md) , каждая из которых содержит идентификатор записи система X.400 сообщения транспорта.</span><span class="sxs-lookup"><span data-stu-id="779b8-105">Contains an array of [MTSID](mtsid.md) structures, each of which contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="779b8-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="779b8-106">Header file:</span></span>  <br/> |<span data-ttu-id="779b8-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="779b8-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="779b8-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="779b8-108">Related macros:</span></span>  <br/> |<span data-ttu-id="779b8-109">[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)</span><span class="sxs-lookup"><span data-stu-id="779b8-109">[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cMTSIDs;
  ULONG cbMTSIDs;
  BYTE abMTSIDs[MAPI_DIM];
} FLATMTSIDLIST, FAR *LPFLATMTSIDLIST;

```

## <a name="members"></a><span data-ttu-id="779b8-110">Members</span><span class="sxs-lookup"><span data-stu-id="779b8-110">Members</span></span>

 <span data-ttu-id="779b8-111">**cMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="779b8-111">**cMTSIDs**</span></span>
  
> <span data-ttu-id="779b8-112">Число структур **MTSID** в массиве описано участником **abMTSIDs** .</span><span class="sxs-lookup"><span data-stu-id="779b8-112">Count of **MTSID** structures in the array described by the **abMTSIDs** member.</span></span> 
    
 <span data-ttu-id="779b8-113">**cbMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="779b8-113">**cbMTSIDs**</span></span>
  
> <span data-ttu-id="779b8-114">Число байт в массиве, описываемых **abMTSIDs**.</span><span class="sxs-lookup"><span data-stu-id="779b8-114">Count of bytes in the array described by **abMTSIDs**.</span></span>
    
 <span data-ttu-id="779b8-115">**abMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="779b8-115">**abMTSIDs**</span></span>
  
> <span data-ttu-id="779b8-116">Массив байтов, который содержит один или несколько **MTSID** структуры.</span><span class="sxs-lookup"><span data-stu-id="779b8-116">Byte array that contains one or more **MTSID** structures.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="779b8-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="779b8-117">Remarks</span></span>

<span data-ttu-id="779b8-118">Использование **FLATMTSIDLIST** структуры в системе обмена сообщениями X.400 соответствует использования [FLATENTRYLIST](flatentrylist.md) структуры в системе обмена сообщениями MAPI.</span><span class="sxs-lookup"><span data-stu-id="779b8-118">The **FLATMTSIDLIST** structure's use in X.400 messaging corresponds to the [FLATENTRYLIST](flatentrylist.md) structure's use in MAPI messaging.</span></span> <span data-ttu-id="779b8-119">MAPI использует **FLATMTSIDLIST** структуры для сохранения свойств X.400 во время обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="779b8-119">MAPI uses **FLATMTSIDLIST** structures to maintain X.400 properties during message handling.</span></span> <span data-ttu-id="779b8-120">При обработке входящих и исходящих сообщений X.400 поставщиков услуг использовать структуры **FLATMTSIDLIST** .</span><span class="sxs-lookup"><span data-stu-id="779b8-120">Service providers use **FLATMTSIDLIST** structures when handling incoming and outgoing X.400 messages.</span></span> 
  
<span data-ttu-id="779b8-121">В массиве **abMTSIDs** каждого **MTSID** структура выравнивается по границе естественно выравнивания.</span><span class="sxs-lookup"><span data-stu-id="779b8-121">In the **abMTSIDs** array, each **MTSID** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="779b8-122">Дополнительные байты включены как внутренние поля, чтобы сделать проверьте естественным выравниванием между любые две структуры **MTSID** .</span><span class="sxs-lookup"><span data-stu-id="779b8-122">Extra bytes are included as padding to make sure natural alignment between any two **MTSID** structures.</span></span> <span data-ttu-id="779b8-123">Так как смещение член **abMTSIDs** 8 первого **MTSID** структуру в массиве всегда выравнивается правильно.</span><span class="sxs-lookup"><span data-stu-id="779b8-123">The first **MTSID** structure in the array is always aligned correctly because the offset of the **abMTSIDs** member is 8.</span></span> <span data-ttu-id="779b8-124">Чтобы вычислить смещение Далее структуры, используйте размер первой записи округлено до следующего несколькими 4.</span><span class="sxs-lookup"><span data-stu-id="779b8-124">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="779b8-125">Используйте макрос [CbNewMTSID](cbnewmtsid.md) для вычисления размера структуры **MTSID** .</span><span class="sxs-lookup"><span data-stu-id="779b8-125">Use the [CbNewMTSID](cbnewmtsid.md) macro to compute the size of an **MTSID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="779b8-126">См. также</span><span class="sxs-lookup"><span data-stu-id="779b8-126">See also</span></span>



[<span data-ttu-id="779b8-127">CbNewFLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="779b8-127">CbNewFLATMTSIDLIST</span></span>](cbnewflatmtsidlist.md)
  
[<span data-ttu-id="779b8-128">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="779b8-128">FLATENTRYLIST</span></span>](flatentrylist.md)
  
[<span data-ttu-id="779b8-129">MTSID</span><span class="sxs-lookup"><span data-stu-id="779b8-129">MTSID</span></span>](mtsid.md)


[<span data-ttu-id="779b8-130">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="779b8-130">MAPI Structures</span></span>](mapi-structures.md)

