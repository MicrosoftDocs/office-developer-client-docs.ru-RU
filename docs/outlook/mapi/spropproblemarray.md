---
title: SPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropProblemArray
api_type:
- COM
ms.assetid: 3fbaa77a-be43-4fce-af67-1826ee101799
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e71658922b6cb80dadc7e034a51c10189c4207ed
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568499"
---
# <a name="spropproblemarray"></a><span data-ttu-id="90c4a-103">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="90c4a-103">SPropProblemArray</span></span>

  
  
<span data-ttu-id="90c4a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90c4a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90c4a-105">Содержит массив из одного или нескольких структур [SPropProblem](spropproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="90c4a-105">Contains an array of one or more [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="90c4a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="90c4a-106">Header file:</span></span>  <br/> |<span data-ttu-id="90c4a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="90c4a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="90c4a-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="90c4a-108">Related macros:</span></span>  <br/> |[<span data-ttu-id="90c4a-109">CbNewSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="90c4a-109">CbNewSPropProblemArray</span></span>](cbnewspropproblemarray.md) <br/> [<span data-ttu-id="90c4a-110">CbSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="90c4a-110">CbSPropProblemArray</span></span>](cbspropproblemarray.md) <br/> [<span data-ttu-id="90c4a-111">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="90c4a-111">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
   
```cpp
typedef struct _SPropProblemArray
{
  ULONG cProblem;
  SPropProblem aProblem[MAPI_DIM];
} SPropProblemArray, FAR *LPSPropProblemArray;

```

## <a name="members"></a><span data-ttu-id="90c4a-112">Members</span><span class="sxs-lookup"><span data-stu-id="90c4a-112">Members</span></span>

 <span data-ttu-id="90c4a-113">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="90c4a-113">**cProblem**</span></span>
  
> <span data-ttu-id="90c4a-114">Число структур [SPropProblem](spropproblem.md) в массиве, указанный в параметре члена **aProblem** .</span><span class="sxs-lookup"><span data-stu-id="90c4a-114">Count of [SPropProblem](spropproblem.md) structures in the array indicated by the **aProblem** member.</span></span> 
    
 <span data-ttu-id="90c4a-115">**aProblem**</span><span class="sxs-lookup"><span data-stu-id="90c4a-115">**aProblem**</span></span>
  
> <span data-ttu-id="90c4a-116">Массив структур **SPropProblem** каждого описывает ошибку свойство.</span><span class="sxs-lookup"><span data-stu-id="90c4a-116">Array of **SPropProblem** structures, each describing a property error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="90c4a-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="90c4a-117">Remarks</span></span>

<span data-ttu-id="90c4a-118">Дополнительные сведения о работе структур **SPropProblem** и **SPropProblemArray** при этом возникают ошибки, связанные с свойства в разделе [Свойства с именем MAPI](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="90c4a-118">For more information about how the **SPropProblem** and **SPropProblemArray** structures work with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="90c4a-119">См. также</span><span class="sxs-lookup"><span data-stu-id="90c4a-119">See also</span></span>



[<span data-ttu-id="90c4a-120">SCODE</span><span class="sxs-lookup"><span data-stu-id="90c4a-120">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="90c4a-121">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="90c4a-121">SPropProblem</span></span>](spropproblem.md)


[<span data-ttu-id="90c4a-122">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="90c4a-122">MAPI Structures</span></span>](mapi-structures.md)

