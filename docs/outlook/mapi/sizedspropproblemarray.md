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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282693"
---
# <a name="sizedspropproblemarray"></a><span data-ttu-id="9748b-103">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="9748b-103">SizedSPropProblemArray</span></span>

<span data-ttu-id="9748b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9748b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9748b-105">Создает именованную структуру [спроппроблемаррай](spropproblemarray.md) , содержащую указанное число структур [спроппроблем](spropproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="9748b-105">Creates a named [SPropProblemArray](spropproblemarray.md) structure that contains a specified number of [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9748b-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9748b-106">Header file:</span></span>  <br/> |<span data-ttu-id="9748b-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="9748b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9748b-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="9748b-108">Related structure:</span></span>  <br/> |<span data-ttu-id="9748b-109">**SPropProblemArray**</span><span class="sxs-lookup"><span data-stu-id="9748b-109">**SPropProblemArray**</span></span> <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a><span data-ttu-id="9748b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="9748b-110">Parameters</span></span>

<span data-ttu-id="9748b-111">__кпроб_</span><span class="sxs-lookup"><span data-stu-id="9748b-111">__cprob_</span></span>
  
> <span data-ttu-id="9748b-112">Количество структур **спроппроблем** , включаемых в новую структуру.</span><span class="sxs-lookup"><span data-stu-id="9748b-112">Count of **SPropProblem** structures to be included in the new structure.</span></span> 
    
<span data-ttu-id="9748b-113">__имя_</span><span class="sxs-lookup"><span data-stu-id="9748b-113">__name_</span></span>
  
> <span data-ttu-id="9748b-114">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="9748b-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9748b-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="9748b-115">Remarks</span></span>

<span data-ttu-id="9748b-116">С помощью макроса **сизедспроппроблемаррай** создайте массив проблем свойств с явными границами.</span><span class="sxs-lookup"><span data-stu-id="9748b-116">Use the **SizedSPropProblemArray** macro to create a property problem array with explicit bounds.</span></span> <span data-ttu-id="9748b-117">Чтобы использовать новую структуру, полученную из макроса **сизедспроппроблемаррай** в качестве указателя на структуру **спроппроблемаррай** , выполните приведенные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="9748b-117">To use the new structure that results from the **SizedSPropProblemArray** macro as a pointer to an **SPropProblemArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a><span data-ttu-id="9748b-118">См. также</span><span class="sxs-lookup"><span data-stu-id="9748b-118">See also</span></span>

- [<span data-ttu-id="9748b-119">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="9748b-119">SPropProblemArray</span></span>](spropproblemarray.md)
- [<span data-ttu-id="9748b-120">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="9748b-120">SPropProblem</span></span>](spropproblem.md)
- [<span data-ttu-id="9748b-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="9748b-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

