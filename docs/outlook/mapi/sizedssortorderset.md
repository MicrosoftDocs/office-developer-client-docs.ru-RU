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
ms.openlocfilehash: 7622baaebf6918cf84c48e53291cf5ec2c0b1a4a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572566"
---
# <a name="sizedssortorderset"></a><span data-ttu-id="1a950-103">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="1a950-103">SizedSSortOrderSet</span></span>

<span data-ttu-id="1a950-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a950-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a950-105">Создает структуру [SSortOrderSet](ssortorderset.md) именованные, содержащий указанное число порядок сортировки.</span><span class="sxs-lookup"><span data-stu-id="1a950-105">Creates a named [SSortOrderSet](ssortorderset.md) structure that contains a specified number of sort orders.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1a950-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="1a950-106">Header file:</span></span>  <br/> |<span data-ttu-id="1a950-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1a950-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="1a950-108">Связанные структуры:</span><span class="sxs-lookup"><span data-stu-id="1a950-108">Related structure:</span></span>  <br/> |<span data-ttu-id="1a950-109">**SSortOrderSet**</span><span class="sxs-lookup"><span data-stu-id="1a950-109">**SSortOrderSet**</span></span> <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a><span data-ttu-id="1a950-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a950-110">Parameters</span></span>

<span data-ttu-id="1a950-111">__csort_</span><span class="sxs-lookup"><span data-stu-id="1a950-111">__csort_</span></span>
  
> <span data-ttu-id="1a950-112">Число порядок сортировки должны быть включены в новой структуры.</span><span class="sxs-lookup"><span data-stu-id="1a950-112">Count of sort orders to be included in the new structure.</span></span>
    
<span data-ttu-id="1a950-113">_имя_</span><span class="sxs-lookup"><span data-stu-id="1a950-113">__name_</span></span>
  
> <span data-ttu-id="1a950-114">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="1a950-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1a950-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="1a950-115">Remarks</span></span>

<span data-ttu-id="1a950-116">Используйте макрос **SizedSSortOrderSet** для создания набора с явные границы порядок сортировки.</span><span class="sxs-lookup"><span data-stu-id="1a950-116">Use the **SizedSSortOrderSet** macro to create a sort order set with explicit bounds.</span></span> 
  
<span data-ttu-id="1a950-117">Для применения новой структуры, результаты из макроса **SizedSSortOrderSet** как указатель на структуру **SSortOrderSet** , выполните следующие приведения.</span><span class="sxs-lookup"><span data-stu-id="1a950-117">To use the new structure that results from the **SizedSSortOrderSet** macro as a pointer to an **SSortOrderSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a><span data-ttu-id="1a950-118">См. также</span><span class="sxs-lookup"><span data-stu-id="1a950-118">See also</span></span>

- [<span data-ttu-id="1a950-119">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="1a950-119">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="1a950-120">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="1a950-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

