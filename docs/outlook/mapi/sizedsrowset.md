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
ms.openlocfilehash: cb1e19a3f3703dc4943a5f6c322f1c8b429da5fa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410933"
---
# <a name="sizedsrowset"></a><span data-ttu-id="eaa65-103">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="eaa65-103">SizedSRowSet</span></span>

<span data-ttu-id="eaa65-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eaa65-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eaa65-105">Создает именоваемую [структуру SRowSet,](srowset.md) которая содержит указанное число строк.</span><span class="sxs-lookup"><span data-stu-id="eaa65-105">Creates a named [SRowSet](srowset.md) structure that contains a specified number of rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eaa65-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="eaa65-106">Header file:</span></span>  <br/> |<span data-ttu-id="eaa65-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eaa65-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="eaa65-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="eaa65-108">Related structure:</span></span>  <br/> |<span data-ttu-id="eaa65-109">**SRowSet**</span><span class="sxs-lookup"><span data-stu-id="eaa65-109">**SRowSet**</span></span> <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a><span data-ttu-id="eaa65-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="eaa65-110">Parameters</span></span>

<span data-ttu-id="eaa65-111">_ ___</span><span class="sxs-lookup"><span data-stu-id="eaa65-111">_ _crow_</span></span>
  
> <span data-ttu-id="eaa65-112">Количество строк, включаемой в новую структуру.</span><span class="sxs-lookup"><span data-stu-id="eaa65-112">Count of the number of rows to be included in the new structure.</span></span>
    
<span data-ttu-id="eaa65-113">_ _name_</span><span class="sxs-lookup"><span data-stu-id="eaa65-113">_ _name_</span></span>
  
> <span data-ttu-id="eaa65-114">Имя новой структуры.</span><span class="sxs-lookup"><span data-stu-id="eaa65-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eaa65-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="eaa65-115">Remarks</span></span>

<span data-ttu-id="eaa65-116">Чтобы использовать новую структуру, которая является результатом макроса **SizedSRowSet** в качестве указателя на структуру **SRowSet,** выполните следующую cast:</span><span class="sxs-lookup"><span data-stu-id="eaa65-116">To use the new structure that results from the **SizedSRowSet** macro as a pointer to an **SRowSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a><span data-ttu-id="eaa65-117">См. также</span><span class="sxs-lookup"><span data-stu-id="eaa65-117">See also</span></span>

- [<span data-ttu-id="eaa65-118">SRowSet</span><span class="sxs-lookup"><span data-stu-id="eaa65-118">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="eaa65-119">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="eaa65-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

