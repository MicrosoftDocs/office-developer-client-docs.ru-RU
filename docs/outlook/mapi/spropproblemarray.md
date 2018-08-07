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
ms.openlocfilehash: 3fd61828cd631c4abc0131da867ca213a3c44d20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812374"
---
# <a name="spropproblemarray"></a><span data-ttu-id="78663-103">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="78663-103">SPropProblemArray</span></span>

  
  
<span data-ttu-id="78663-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="78663-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="78663-105">Содержит массив из одного или нескольких структур [SPropProblem](spropproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="78663-105">Contains an array of one or more [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="78663-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="78663-106">Header file:</span></span>  <br/> |<span data-ttu-id="78663-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="78663-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="78663-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="78663-108">Related macros:</span></span>  <br/> |[<span data-ttu-id="78663-109">CbNewSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="78663-109">CbNewSPropProblemArray</span></span>](cbnewspropproblemarray.md) <br/> [<span data-ttu-id="78663-110">CbSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="78663-110">CbSPropProblemArray</span></span>](cbspropproblemarray.md) <br/> [<span data-ttu-id="78663-111">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="78663-111">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
   
```cpp
typedef struct _SPropProblemArray
{
  ULONG cProblem;
  SPropProblem aProblem[MAPI_DIM];
} SPropProblemArray, FAR *LPSPropProblemArray;

```

## <a name="members"></a><span data-ttu-id="78663-112">Members</span><span class="sxs-lookup"><span data-stu-id="78663-112">Members</span></span>

 <span data-ttu-id="78663-113">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="78663-113">**cProblem**</span></span>
  
> <span data-ttu-id="78663-114">Число структур [SPropProblem](spropproblem.md) в массиве, указанный в параметре члена **aProblem** .</span><span class="sxs-lookup"><span data-stu-id="78663-114">Count of [SPropProblem](spropproblem.md) structures in the array indicated by the **aProblem** member.</span></span> 
    
 <span data-ttu-id="78663-115">**aProblem**</span><span class="sxs-lookup"><span data-stu-id="78663-115">**aProblem**</span></span>
  
> <span data-ttu-id="78663-116">Массив структур **SPropProblem** каждого описывает ошибку свойство.</span><span class="sxs-lookup"><span data-stu-id="78663-116">Array of **SPropProblem** structures, each describing a property error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="78663-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="78663-117">Remarks</span></span>

<span data-ttu-id="78663-118">Дополнительные сведения о работе структур **SPropProblem** и **SPropProblemArray** при этом возникают ошибки, связанные с свойства в разделе [Свойства с именем MAPI](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="78663-118">For more information about how the **SPropProblem** and **SPropProblemArray** structures work with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="78663-119">См. также</span><span class="sxs-lookup"><span data-stu-id="78663-119">See also</span></span>



[<span data-ttu-id="78663-120">SCODE</span><span class="sxs-lookup"><span data-stu-id="78663-120">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="78663-121">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="78663-121">SPropProblem</span></span>](spropproblem.md)


[<span data-ttu-id="78663-122">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="78663-122">MAPI Structures</span></span>](mapi-structures.md)

