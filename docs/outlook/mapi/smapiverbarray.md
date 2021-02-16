---
title: SMAPIVerbArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIVerbArray
api_type:
- COM
ms.assetid: 8736f75c-3e95-42dd-9bc1-2f0bd23c4a02
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7cba5dce60ce15ddb12776d619143849298aac9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433915"
---
# <a name="smapiverbarray"></a><span data-ttu-id="c24f2-103">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="c24f2-103">SMAPIVerbArray</span></span>

  
  
<span data-ttu-id="c24f2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c24f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c24f2-105">Содержит массив структур [SMAPIVerb,](smapiverb.md) описывая команды MAPI.</span><span class="sxs-lookup"><span data-stu-id="c24f2-105">Contains an array of [SMAPIVerb](smapiverb.md) structures that describe MAPI verbs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c24f2-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c24f2-106">Header file:</span></span>  <br/> |<span data-ttu-id="c24f2-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="c24f2-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="c24f2-108">Связанный макрос:</span><span class="sxs-lookup"><span data-stu-id="c24f2-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="c24f2-109">CbMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="c24f2-109">CbMAPIVerbArray</span></span>](cbmapiverbarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMAPIVerb;
  SMAPIVerb aMAPIVerb[MAPI_DIM];
} SMAPIVerbArray, FAR * LPMAPIVERBARRAY;

```

## <a name="members"></a><span data-ttu-id="c24f2-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="c24f2-110">Members</span></span>

 <span data-ttu-id="c24f2-111">**cForms**</span><span class="sxs-lookup"><span data-stu-id="c24f2-111">**cForms**</span></span>
  
> <span data-ttu-id="c24f2-112">Количество глаголов в массиве.</span><span class="sxs-lookup"><span data-stu-id="c24f2-112">Count of verbs in the array.</span></span>
    
 <span data-ttu-id="c24f2-113">**aFormInfo**</span><span class="sxs-lookup"><span data-stu-id="c24f2-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="c24f2-114">Массив глаголов MAPI.</span><span class="sxs-lookup"><span data-stu-id="c24f2-114">Array of MAPI verbs.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c24f2-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="c24f2-115">Remarks</span></span>

<span data-ttu-id="c24f2-116">Структура **SMAPIVerbArray** передается в качестве параметра в [методе IMAPIFormInfo::CalcVerbSet.](imapiforminfo-calcverbset.md)</span><span class="sxs-lookup"><span data-stu-id="c24f2-116">The **SMAPIVerbArray** structure is passed as a parameter in the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c24f2-117">См. также</span><span class="sxs-lookup"><span data-stu-id="c24f2-117">See also</span></span>



[<span data-ttu-id="c24f2-118">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="c24f2-118">SMAPIVerb</span></span>](smapiverb.md)


[<span data-ttu-id="c24f2-119">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="c24f2-119">MAPI Structures</span></span>](mapi-structures.md)

