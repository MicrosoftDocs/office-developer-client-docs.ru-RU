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
# <a name="sizedspropproblemarray"></a><span data-ttu-id="0e892-103">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="0e892-103">SizedSPropProblemArray</span></span>

<span data-ttu-id="0e892-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e892-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e892-105">Создает именованную структуру [спроппроблемаррай](spropproblemarray.md) , содержащую указанное число структур [спроппроблем](spropproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="0e892-105">Creates a named [SPropProblemArray](spropproblemarray.md) structure that contains a specified number of [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0e892-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="0e892-106">Header file:</span></span>  <br/> |<span data-ttu-id="0e892-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="0e892-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0e892-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="0e892-108">Related structure:</span></span>  <br/> |<span data-ttu-id="0e892-109">**SPropProblemArray**</span><span class="sxs-lookup"><span data-stu-id="0e892-109">**SPropProblemArray**</span></span> <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a><span data-ttu-id="0e892-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e892-110">Parameters</span></span>

<span data-ttu-id="0e892-111">__кпроб_</span><span class="sxs-lookup"><span data-stu-id="0e892-111">__cprob_</span></span>
  
> <span data-ttu-id="0e892-112">Количество структур **спроппроблем** , включаемых в новую структуру.</span><span class="sxs-lookup"><span data-stu-id="0e892-112">Count of **SPropProblem** structures to be included in the new structure.</span></span> 
    
<span data-ttu-id="0e892-113">__имя_</span><span class="sxs-lookup"><span data-stu-id="0e892-113">__name_</span></span>
  
> <span data-ttu-id="0e892-114">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="0e892-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0e892-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="0e892-115">Remarks</span></span>

<span data-ttu-id="0e892-116">С помощью макроса **сизедспроппроблемаррай** создайте массив проблем свойств с явными границами.</span><span class="sxs-lookup"><span data-stu-id="0e892-116">Use the **SizedSPropProblemArray** macro to create a property problem array with explicit bounds.</span></span> <span data-ttu-id="0e892-117">Чтобы использовать новую структуру, полученную из макроса **сизедспроппроблемаррай** в качестве указателя на структуру **спроппроблемаррай** , выполните приведенные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="0e892-117">To use the new structure that results from the **SizedSPropProblemArray** macro as a pointer to an **SPropProblemArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a><span data-ttu-id="0e892-118">См. также</span><span class="sxs-lookup"><span data-stu-id="0e892-118">See also</span></span>

- [<span data-ttu-id="0e892-119">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="0e892-119">SPropProblemArray</span></span>](spropproblemarray.md)
- [<span data-ttu-id="0e892-120">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="0e892-120">SPropProblem</span></span>](spropproblem.md)
- [<span data-ttu-id="0e892-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="0e892-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

