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
ms.openlocfilehash: b3818e5e1429c7e2b7d5f7533db733ba29e672c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418115"
---
# <a name="sizedspropproblemarray"></a><span data-ttu-id="d1e3b-103">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="d1e3b-103">SizedSPropProblemArray</span></span>

<span data-ttu-id="d1e3b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1e3b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1e3b-105">Создает структуру [SPropProblemArray](spropproblemarray.md) с заданным числом [структур SPropProblem.](spropproblem.md)</span><span class="sxs-lookup"><span data-stu-id="d1e3b-105">Creates a named [SPropProblemArray](spropproblemarray.md) structure that contains a specified number of [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d1e3b-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d1e3b-106">Header file:</span></span>  <br/> |<span data-ttu-id="d1e3b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d1e3b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d1e3b-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="d1e3b-108">Related structure:</span></span>  <br/> |<span data-ttu-id="d1e3b-109">**SPropProblemArray**</span><span class="sxs-lookup"><span data-stu-id="d1e3b-109">**SPropProblemArray**</span></span> <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a><span data-ttu-id="d1e3b-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="d1e3b-110">Parameters</span></span>

<span data-ttu-id="d1e3b-111">_ _cprob_</span><span class="sxs-lookup"><span data-stu-id="d1e3b-111">_ _cprob_</span></span>
  
> <span data-ttu-id="d1e3b-112">Количество **структур SPropProblem,** которые будут включены в новую структуру.</span><span class="sxs-lookup"><span data-stu-id="d1e3b-112">Count of **SPropProblem** structures to be included in the new structure.</span></span> 
    
<span data-ttu-id="d1e3b-113">_ _имя_</span><span class="sxs-lookup"><span data-stu-id="d1e3b-113">_ _name_</span></span>
  
> <span data-ttu-id="d1e3b-114">Имя новой структуры.</span><span class="sxs-lookup"><span data-stu-id="d1e3b-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d1e3b-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="d1e3b-115">Remarks</span></span>

<span data-ttu-id="d1e3b-116">Используйте **макрос SizedSPropProblemArray** для создания массива проблем свойств с явными границами.</span><span class="sxs-lookup"><span data-stu-id="d1e3b-116">Use the **SizedSPropProblemArray** macro to create a property problem array with explicit bounds.</span></span> <span data-ttu-id="d1e3b-117">Чтобы использовать новую структуру, которая является результатом макроса **SizedSPropProblemArray** в качестве указателя на структуру **SPropProblemArray,** выполните следующий бросок:</span><span class="sxs-lookup"><span data-stu-id="d1e3b-117">To use the new structure that results from the **SizedSPropProblemArray** macro as a pointer to an **SPropProblemArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a><span data-ttu-id="d1e3b-118">См. также</span><span class="sxs-lookup"><span data-stu-id="d1e3b-118">See also</span></span>

- [<span data-ttu-id="d1e3b-119">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="d1e3b-119">SPropProblemArray</span></span>](spropproblemarray.md)
- [<span data-ttu-id="d1e3b-120">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="d1e3b-120">SPropProblem</span></span>](spropproblem.md)
- [<span data-ttu-id="d1e3b-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="d1e3b-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

