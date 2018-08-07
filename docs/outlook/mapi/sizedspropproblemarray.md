---
title: SizedSPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropProblemArray
api_type:
- COM
ms.assetid: 2fc3febb-8c69-4315-a112-a28eee98013d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b8521172b441bd26a6562aa28f836d453544928f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812304"
---
# <a name="sizedspropproblemarray"></a><span data-ttu-id="959e8-103">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="959e8-103">SizedSPropProblemArray</span></span>

<span data-ttu-id="959e8-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="959e8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="959e8-105">Создает структуру [SPropProblemArray](spropproblemarray.md) именованные, содержащий указанное число [SPropProblem](spropproblem.md) структуры.</span><span class="sxs-lookup"><span data-stu-id="959e8-105">Creates a named [SPropProblemArray](spropproblemarray.md) structure that contains a specified number of [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="959e8-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="959e8-106">Header file:</span></span>  <br/> |<span data-ttu-id="959e8-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="959e8-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="959e8-108">Связанные структуры:</span><span class="sxs-lookup"><span data-stu-id="959e8-108">Related structure:</span></span>  <br/> |<span data-ttu-id="959e8-109">**SPropProblemArray**</span><span class="sxs-lookup"><span data-stu-id="959e8-109">**SPropProblemArray**</span></span> <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a><span data-ttu-id="959e8-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="959e8-110">Parameters</span></span>

<span data-ttu-id="959e8-111">__cprob_</span><span class="sxs-lookup"><span data-stu-id="959e8-111">__cprob_</span></span>
  
> <span data-ttu-id="959e8-112">Число структур **SPropProblem** должны быть включены в новой структуры.</span><span class="sxs-lookup"><span data-stu-id="959e8-112">Count of **SPropProblem** structures to be included in the new structure.</span></span> 
    
<span data-ttu-id="959e8-113">_имя_</span><span class="sxs-lookup"><span data-stu-id="959e8-113">__name_</span></span>
  
> <span data-ttu-id="959e8-114">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="959e8-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="959e8-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="959e8-115">Remarks</span></span>

<span data-ttu-id="959e8-116">Используйте макрос **SizedSPropProblemArray** для создания массива проблема свойства с помощью явных границы.</span><span class="sxs-lookup"><span data-stu-id="959e8-116">Use the **SizedSPropProblemArray** macro to create a property problem array with explicit bounds.</span></span> <span data-ttu-id="959e8-117">Для применения новой структуры, результаты из макроса **SizedSPropProblemArray** как указатель на структуру **SPropProblemArray** , выполните следующие приведения.</span><span class="sxs-lookup"><span data-stu-id="959e8-117">To use the new structure that results from the **SizedSPropProblemArray** macro as a pointer to an **SPropProblemArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a><span data-ttu-id="959e8-118">См. также</span><span class="sxs-lookup"><span data-stu-id="959e8-118">See also</span></span>

- [<span data-ttu-id="959e8-119">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="959e8-119">SPropProblemArray</span></span>](spropproblemarray.md)
- [<span data-ttu-id="959e8-120">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="959e8-120">SPropProblem</span></span>](spropproblem.md)
- [<span data-ttu-id="959e8-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="959e8-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

