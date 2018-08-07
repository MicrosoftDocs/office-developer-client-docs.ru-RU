---
title: SizedSSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSSortOrderSet
api_type:
- COM
ms.assetid: f0b9c2f4-7011-414d-8e6c-ab22893ef132
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2eb92c3f1555407a77332bd6ec3b2b7202f0553f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812322"
---
# <a name="sizedssortorderset"></a><span data-ttu-id="a48b0-103">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="a48b0-103">SizedSSortOrderSet</span></span>

<span data-ttu-id="a48b0-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a48b0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a48b0-105">Создает структуру [SSortOrderSet](ssortorderset.md) именованные, содержащий указанное число порядок сортировки.</span><span class="sxs-lookup"><span data-stu-id="a48b0-105">Creates a named [SSortOrderSet](ssortorderset.md) structure that contains a specified number of sort orders.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a48b0-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a48b0-106">Header file:</span></span>  <br/> |<span data-ttu-id="a48b0-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a48b0-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a48b0-108">Связанные структуры:</span><span class="sxs-lookup"><span data-stu-id="a48b0-108">Related structure:</span></span>  <br/> |<span data-ttu-id="a48b0-109">**SSortOrderSet**</span><span class="sxs-lookup"><span data-stu-id="a48b0-109">**SSortOrderSet**</span></span> <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a><span data-ttu-id="a48b0-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a48b0-110">Parameters</span></span>

<span data-ttu-id="a48b0-111">__csort_</span><span class="sxs-lookup"><span data-stu-id="a48b0-111">__csort_</span></span>
  
> <span data-ttu-id="a48b0-112">Число порядок сортировки должны быть включены в новой структуры.</span><span class="sxs-lookup"><span data-stu-id="a48b0-112">Count of sort orders to be included in the new structure.</span></span>
    
<span data-ttu-id="a48b0-113">_имя_</span><span class="sxs-lookup"><span data-stu-id="a48b0-113">__name_</span></span>
  
> <span data-ttu-id="a48b0-114">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="a48b0-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a48b0-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="a48b0-115">Remarks</span></span>

<span data-ttu-id="a48b0-116">Используйте макрос **SizedSSortOrderSet** для создания набора с явные границы порядок сортировки.</span><span class="sxs-lookup"><span data-stu-id="a48b0-116">Use the **SizedSSortOrderSet** macro to create a sort order set with explicit bounds.</span></span> 
  
<span data-ttu-id="a48b0-117">Для применения новой структуры, результаты из макроса **SizedSSortOrderSet** как указатель на структуру **SSortOrderSet** , выполните следующие приведения.</span><span class="sxs-lookup"><span data-stu-id="a48b0-117">To use the new structure that results from the **SizedSSortOrderSet** macro as a pointer to an **SSortOrderSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a><span data-ttu-id="a48b0-118">См. также</span><span class="sxs-lookup"><span data-stu-id="a48b0-118">See also</span></span>

- [<span data-ttu-id="a48b0-119">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="a48b0-119">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="a48b0-120">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="a48b0-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

