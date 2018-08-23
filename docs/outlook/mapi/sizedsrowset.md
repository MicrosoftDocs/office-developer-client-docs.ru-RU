---
title: SizedSRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSRowSet
api_type:
- COM
ms.assetid: 419e2c6d-ac3b-46c6-9a12-33f51f6d7f12
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b8c70c8b13025f196fdebb2956939bec840a96f5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583941"
---
# <a name="sizedsrowset"></a><span data-ttu-id="5c121-103">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="5c121-103">SizedSRowSet</span></span>

<span data-ttu-id="5c121-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c121-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c121-105">Создает структуру [SRowSet](srowset.md) именованные, содержащий указанное число строк.</span><span class="sxs-lookup"><span data-stu-id="5c121-105">Creates a named [SRowSet](srowset.md) structure that contains a specified number of rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c121-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5c121-106">Header file:</span></span>  <br/> |<span data-ttu-id="5c121-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5c121-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5c121-108">Связанные структуры:</span><span class="sxs-lookup"><span data-stu-id="5c121-108">Related structure:</span></span>  <br/> |<span data-ttu-id="5c121-109">**SRowSet**</span><span class="sxs-lookup"><span data-stu-id="5c121-109">**SRowSet**</span></span> <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a><span data-ttu-id="5c121-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c121-110">Parameters</span></span>

<span data-ttu-id="5c121-111">__crow_</span><span class="sxs-lookup"><span data-stu-id="5c121-111">__crow_</span></span>
  
> <span data-ttu-id="5c121-112">Количество строк должны быть включены в новой структуры.</span><span class="sxs-lookup"><span data-stu-id="5c121-112">Count of the number of rows to be included in the new structure.</span></span>
    
<span data-ttu-id="5c121-113">_имя_</span><span class="sxs-lookup"><span data-stu-id="5c121-113">__name_</span></span>
  
> <span data-ttu-id="5c121-114">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="5c121-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5c121-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="5c121-115">Remarks</span></span>

<span data-ttu-id="5c121-116">Для применения новой структуры, результаты из макроса **SizedSRowSet** как указатель на структуру **SRowSet** , выполните следующие приведения.</span><span class="sxs-lookup"><span data-stu-id="5c121-116">To use the new structure that results from the **SizedSRowSet** macro as a pointer to an **SRowSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a><span data-ttu-id="5c121-117">См. также</span><span class="sxs-lookup"><span data-stu-id="5c121-117">See also</span></span>

- [<span data-ttu-id="5c121-118">SRowSet</span><span class="sxs-lookup"><span data-stu-id="5c121-118">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="5c121-119">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="5c121-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

