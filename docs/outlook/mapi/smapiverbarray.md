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
ms.openlocfilehash: 7a2911779e5f9edb8c0bba7c3476a74ce410477c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569465"
---
# <a name="smapiverbarray"></a><span data-ttu-id="1e460-103">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="1e460-103">SMAPIVerbArray</span></span>

  
  
<span data-ttu-id="1e460-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e460-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e460-105">Содержит массив структур [SMAPIVerb](smapiverb.md) , которые описывают команд MAPI.</span><span class="sxs-lookup"><span data-stu-id="1e460-105">Contains an array of [SMAPIVerb](smapiverb.md) structures that describe MAPI verbs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1e460-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="1e460-106">Header file:</span></span>  <br/> |<span data-ttu-id="1e460-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="1e460-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="1e460-108">Связанные макрос:</span><span class="sxs-lookup"><span data-stu-id="1e460-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="1e460-109">CbMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="1e460-109">CbMAPIVerbArray</span></span>](cbmapiverbarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMAPIVerb;
  SMAPIVerb aMAPIVerb[MAPI_DIM];
} SMAPIVerbArray, FAR * LPMAPIVERBARRAY;

```

## <a name="members"></a><span data-ttu-id="1e460-110">Members</span><span class="sxs-lookup"><span data-stu-id="1e460-110">Members</span></span>

 <span data-ttu-id="1e460-111">**cForms**</span><span class="sxs-lookup"><span data-stu-id="1e460-111">**cForms**</span></span>
  
> <span data-ttu-id="1e460-112">Число команд в массиве.</span><span class="sxs-lookup"><span data-stu-id="1e460-112">Count of verbs in the array.</span></span>
    
 <span data-ttu-id="1e460-113">**aFormInfo**</span><span class="sxs-lookup"><span data-stu-id="1e460-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="1e460-114">Массив команд MAPI.</span><span class="sxs-lookup"><span data-stu-id="1e460-114">Array of MAPI verbs.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1e460-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="1e460-115">Remarks</span></span>

<span data-ttu-id="1e460-116">Структура **SMAPIVerbArray** передается как параметр в методе [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) .</span><span class="sxs-lookup"><span data-stu-id="1e460-116">The **SMAPIVerbArray** structure is passed as a parameter in the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1e460-117">См. также</span><span class="sxs-lookup"><span data-stu-id="1e460-117">See also</span></span>



[<span data-ttu-id="1e460-118">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="1e460-118">SMAPIVerb</span></span>](smapiverb.md)


[<span data-ttu-id="1e460-119">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="1e460-119">MAPI Structures</span></span>](mapi-structures.md)

