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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428608"
---
# <a name="sizedssortorderset"></a><span data-ttu-id="65305-103">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="65305-103">SizedSSortOrderSet</span></span>

<span data-ttu-id="65305-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65305-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65305-105">Создает именоваемую [структуру SSortOrderSet,](ssortorderset.md) которая содержит определенное количество заказов сортировки.</span><span class="sxs-lookup"><span data-stu-id="65305-105">Creates a named [SSortOrderSet](ssortorderset.md) structure that contains a specified number of sort orders.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="65305-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="65305-106">Header file:</span></span>  <br/> |<span data-ttu-id="65305-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="65305-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="65305-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="65305-108">Related structure:</span></span>  <br/> |<span data-ttu-id="65305-109">**SSortOrderSet**</span><span class="sxs-lookup"><span data-stu-id="65305-109">**SSortOrderSet**</span></span> <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a><span data-ttu-id="65305-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="65305-110">Parameters</span></span>

<span data-ttu-id="65305-111">_ _csort_</span><span class="sxs-lookup"><span data-stu-id="65305-111">_ _csort_</span></span>
  
> <span data-ttu-id="65305-112">Количество заказов сортировки, которые будут включены в новую структуру.</span><span class="sxs-lookup"><span data-stu-id="65305-112">Count of sort orders to be included in the new structure.</span></span>
    
<span data-ttu-id="65305-113">_ _имя_</span><span class="sxs-lookup"><span data-stu-id="65305-113">_ _name_</span></span>
  
> <span data-ttu-id="65305-114">Имя новой структуры.</span><span class="sxs-lookup"><span data-stu-id="65305-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="65305-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="65305-115">Remarks</span></span>

<span data-ttu-id="65305-116">Используйте **макрос SizedSSortOrderSet** для создания набора сортировки с явными границами.</span><span class="sxs-lookup"><span data-stu-id="65305-116">Use the **SizedSSortOrderSet** macro to create a sort order set with explicit bounds.</span></span> 
  
<span data-ttu-id="65305-117">Чтобы использовать новую структуру, которая является результатом **макроса SizedSSortOrderSet** в качестве указателя на **структуру SSortOrderSet,** выполните следующие броски:</span><span class="sxs-lookup"><span data-stu-id="65305-117">To use the new structure that results from the **SizedSSortOrderSet** macro as a pointer to an **SSortOrderSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a><span data-ttu-id="65305-118">См. также</span><span class="sxs-lookup"><span data-stu-id="65305-118">See also</span></span>

- [<span data-ttu-id="65305-119">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="65305-119">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="65305-120">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="65305-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

