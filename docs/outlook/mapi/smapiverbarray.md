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
ms.openlocfilehash: 1767c86cb5390572b95530060f2295034ed35f43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812349"
---
# <a name="smapiverbarray"></a><span data-ttu-id="44de8-103">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="44de8-103">SMAPIVerbArray</span></span>

  
  
<span data-ttu-id="44de8-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="44de8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="44de8-105">Содержит массив структур [SMAPIVerb](smapiverb.md) , которые описывают команд MAPI.</span><span class="sxs-lookup"><span data-stu-id="44de8-105">Contains an array of [SMAPIVerb](smapiverb.md) structures that describe MAPI verbs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="44de8-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="44de8-106">Header file:</span></span>  <br/> |<span data-ttu-id="44de8-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="44de8-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="44de8-108">Связанные макрос:</span><span class="sxs-lookup"><span data-stu-id="44de8-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="44de8-109">CbMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="44de8-109">CbMAPIVerbArray</span></span>](cbmapiverbarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMAPIVerb;
  SMAPIVerb aMAPIVerb[MAPI_DIM];
} SMAPIVerbArray, FAR * LPMAPIVERBARRAY;

```

## <a name="members"></a><span data-ttu-id="44de8-110">Members</span><span class="sxs-lookup"><span data-stu-id="44de8-110">Members</span></span>

 <span data-ttu-id="44de8-111">**cForms**</span><span class="sxs-lookup"><span data-stu-id="44de8-111">**cForms**</span></span>
  
> <span data-ttu-id="44de8-112">Число команд в массиве.</span><span class="sxs-lookup"><span data-stu-id="44de8-112">Count of verbs in the array.</span></span>
    
 <span data-ttu-id="44de8-113">**aFormInfo**</span><span class="sxs-lookup"><span data-stu-id="44de8-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="44de8-114">Массив команд MAPI.</span><span class="sxs-lookup"><span data-stu-id="44de8-114">Array of MAPI verbs.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="44de8-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="44de8-115">Remarks</span></span>

<span data-ttu-id="44de8-116">Структура **SMAPIVerbArray** передается как параметр в методе [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) .</span><span class="sxs-lookup"><span data-stu-id="44de8-116">The **SMAPIVerbArray** structure is passed as a parameter in the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="44de8-117">См. также</span><span class="sxs-lookup"><span data-stu-id="44de8-117">See also</span></span>



[<span data-ttu-id="44de8-118">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="44de8-118">SMAPIVerb</span></span>](smapiverb.md)


[<span data-ttu-id="44de8-119">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="44de8-119">MAPI Structures</span></span>](mapi-structures.md)

