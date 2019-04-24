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
ms.openlocfilehash: 60a335f85eea8778580e0bd74693a5c28591103c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282630"
---
# <a name="sizedssortorderset"></a><span data-ttu-id="269d9-103">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="269d9-103">SizedSSortOrderSet</span></span>

<span data-ttu-id="269d9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="269d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="269d9-105">Создает именованную структуру [ссортордерсет](ssortorderset.md) , содержащую указанное число порядков сортировки.</span><span class="sxs-lookup"><span data-stu-id="269d9-105">Creates a named [SSortOrderSet](ssortorderset.md) structure that contains a specified number of sort orders.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="269d9-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="269d9-106">Header file:</span></span>  <br/> |<span data-ttu-id="269d9-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="269d9-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="269d9-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="269d9-108">Related structure:</span></span>  <br/> |<span data-ttu-id="269d9-109">**SSortOrderSet**</span><span class="sxs-lookup"><span data-stu-id="269d9-109">**SSortOrderSet**</span></span> <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a><span data-ttu-id="269d9-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="269d9-110">Parameters</span></span>

<span data-ttu-id="269d9-111">__ксорт_</span><span class="sxs-lookup"><span data-stu-id="269d9-111">__csort_</span></span>
  
> <span data-ttu-id="269d9-112">Количество порядков сортировки, включаемых в новую структуру.</span><span class="sxs-lookup"><span data-stu-id="269d9-112">Count of sort orders to be included in the new structure.</span></span>
    
<span data-ttu-id="269d9-113">__имя_</span><span class="sxs-lookup"><span data-stu-id="269d9-113">__name_</span></span>
  
> <span data-ttu-id="269d9-114">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="269d9-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="269d9-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="269d9-115">Remarks</span></span>

<span data-ttu-id="269d9-116">Используйте макрос **сизедссортордерсет** для создания набора порядка сортировки с явными границами.</span><span class="sxs-lookup"><span data-stu-id="269d9-116">Use the **SizedSSortOrderSet** macro to create a sort order set with explicit bounds.</span></span> 
  
<span data-ttu-id="269d9-117">Чтобы использовать новую структуру, полученную из макроса **сизедссортордерсет** в качестве указателя на структуру **ссортордерсет** , выполните приведенные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="269d9-117">To use the new structure that results from the **SizedSSortOrderSet** macro as a pointer to an **SSortOrderSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a><span data-ttu-id="269d9-118">См. также</span><span class="sxs-lookup"><span data-stu-id="269d9-118">See also</span></span>

- [<span data-ttu-id="269d9-119">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="269d9-119">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="269d9-120">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="269d9-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

