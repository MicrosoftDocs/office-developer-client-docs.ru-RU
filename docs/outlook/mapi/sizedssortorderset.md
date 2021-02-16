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
# <a name="sizedssortorderset"></a><span data-ttu-id="b7141-103">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="b7141-103">SizedSSortOrderSet</span></span>

<span data-ttu-id="b7141-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7141-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7141-105">Создает именоваемую [структуру SSortOrderSet,](ssortorderset.md) которая содержит указанное число заказов на сортировку.</span><span class="sxs-lookup"><span data-stu-id="b7141-105">Creates a named [SSortOrderSet](ssortorderset.md) structure that contains a specified number of sort orders.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b7141-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b7141-106">Header file:</span></span>  <br/> |<span data-ttu-id="b7141-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b7141-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b7141-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="b7141-108">Related structure:</span></span>  <br/> |<span data-ttu-id="b7141-109">**SSortOrderSet**</span><span class="sxs-lookup"><span data-stu-id="b7141-109">**SSortOrderSet**</span></span> <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a><span data-ttu-id="b7141-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b7141-110">Parameters</span></span>

<span data-ttu-id="b7141-111">_ _csort_</span><span class="sxs-lookup"><span data-stu-id="b7141-111">_ _csort_</span></span>
  
> <span data-ttu-id="b7141-112">Количество заказов сортировки, которые необходимо включить в новую структуру.</span><span class="sxs-lookup"><span data-stu-id="b7141-112">Count of sort orders to be included in the new structure.</span></span>
    
<span data-ttu-id="b7141-113">_ _name_</span><span class="sxs-lookup"><span data-stu-id="b7141-113">_ _name_</span></span>
  
> <span data-ttu-id="b7141-114">Имя новой структуры.</span><span class="sxs-lookup"><span data-stu-id="b7141-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b7141-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="b7141-115">Remarks</span></span>

<span data-ttu-id="b7141-116">Используйте **макрос SizedSSortOrderSet,** чтобы создать порядок сортировки с явными границами.</span><span class="sxs-lookup"><span data-stu-id="b7141-116">Use the **SizedSSortOrderSet** macro to create a sort order set with explicit bounds.</span></span> 
  
<span data-ttu-id="b7141-117">Чтобы использовать новую структуру, которая является результатом выполнения **макроса SizedSSortOrderSet** в качестве указателя на структуру **SSortOrderSet,** выполните следующую пристановка:</span><span class="sxs-lookup"><span data-stu-id="b7141-117">To use the new structure that results from the **SizedSSortOrderSet** macro as a pointer to an **SSortOrderSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a><span data-ttu-id="b7141-118">См. также</span><span class="sxs-lookup"><span data-stu-id="b7141-118">See also</span></span>

- [<span data-ttu-id="b7141-119">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="b7141-119">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="b7141-120">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="b7141-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

