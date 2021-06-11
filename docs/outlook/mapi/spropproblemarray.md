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
ms.openlocfilehash: f78e0ed939e190a9855ea4b040d18c01cfecc91d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406859"
---
# <a name="spropproblemarray"></a><span data-ttu-id="19d1d-103">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="19d1d-103">SPropProblemArray</span></span>

  
  
<span data-ttu-id="19d1d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19d1d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19d1d-105">Содержит массив одной или более [структур SPropProblem.](spropproblem.md)</span><span class="sxs-lookup"><span data-stu-id="19d1d-105">Contains an array of one or more [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="19d1d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="19d1d-106">Header file:</span></span>  <br/> |<span data-ttu-id="19d1d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="19d1d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="19d1d-108">Связанные макрос:</span><span class="sxs-lookup"><span data-stu-id="19d1d-108">Related macros:</span></span>  <br/> |[<span data-ttu-id="19d1d-109">CbNewSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="19d1d-109">CbNewSPropProblemArray</span></span>](cbnewspropproblemarray.md) <br/> [<span data-ttu-id="19d1d-110">CbSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="19d1d-110">CbSPropProblemArray</span></span>](cbspropproblemarray.md) <br/> [<span data-ttu-id="19d1d-111">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="19d1d-111">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
   
```cpp
typedef struct _SPropProblemArray
{
  ULONG cProblem;
  SPropProblem aProblem[MAPI_DIM];
} SPropProblemArray, FAR *LPSPropProblemArray;

```

## <a name="members"></a><span data-ttu-id="19d1d-112">"Участники"</span><span class="sxs-lookup"><span data-stu-id="19d1d-112">Members</span></span>

 <span data-ttu-id="19d1d-113">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="19d1d-113">**cProblem**</span></span>
  
> <span data-ttu-id="19d1d-114">Count of [SPropProblem](spropproblem.md) structures in the array indicated by **the aProblem** member.</span><span class="sxs-lookup"><span data-stu-id="19d1d-114">Count of [SPropProblem](spropproblem.md) structures in the array indicated by the **aProblem** member.</span></span> 
    
 <span data-ttu-id="19d1d-115">**aProblem**</span><span class="sxs-lookup"><span data-stu-id="19d1d-115">**aProblem**</span></span>
  
> <span data-ttu-id="19d1d-116">Массив **структур SPropProblem,** каждый из которых описывает ошибку свойства.</span><span class="sxs-lookup"><span data-stu-id="19d1d-116">Array of **SPropProblem** structures, each describing a property error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="19d1d-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="19d1d-117">Remarks</span></span>

<span data-ttu-id="19d1d-118">Дополнительные сведения о том, как структуры **SPropProblem** и **SPropProblemArray** работают с ошибками, связанными с свойствами, см. в рублях [MAPI Named Properties](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="19d1d-118">For more information about how the **SPropProblem** and **SPropProblemArray** structures work with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="19d1d-119">См. также</span><span class="sxs-lookup"><span data-stu-id="19d1d-119">See also</span></span>



[<span data-ttu-id="19d1d-120">SCODE</span><span class="sxs-lookup"><span data-stu-id="19d1d-120">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="19d1d-121">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="19d1d-121">SPropProblem</span></span>](spropproblem.md)


[<span data-ttu-id="19d1d-122">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="19d1d-122">MAPI Structures</span></span>](mapi-structures.md)

