---
title: SizedSPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropTagArray
api_type:
- COM
ms.assetid: 1d2dc6e9-735d-4b5b-af6f-adf6a32a666d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7505c5dbcfc98a8b868424ae51cbe9c47b1d4338
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812307"
---
# <a name="sizedsproptagarray"></a><span data-ttu-id="987c7-103">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="987c7-103">SizedSPropTagArray</span></span>

<span data-ttu-id="987c7-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="987c7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="987c7-105">Создает структуру [SPropTagArray](sproptagarray.md) именованные, содержащий указанное число тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="987c7-105">Creates a named [SPropTagArray](sproptagarray.md) structure that includes a specified number of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="987c7-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="987c7-106">Header file:</span></span>  <br/> |<span data-ttu-id="987c7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="987c7-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="987c7-108">Связанные структуры:</span><span class="sxs-lookup"><span data-stu-id="987c7-108">Related structure:</span></span>  <br/> |<span data-ttu-id="987c7-109">**SPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="987c7-109">**SPropTagArray**</span></span> <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a><span data-ttu-id="987c7-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="987c7-110">Parameters</span></span>

<span data-ttu-id="987c7-111">__ctag_</span><span class="sxs-lookup"><span data-stu-id="987c7-111">__ctag_</span></span>
  
> <span data-ttu-id="987c7-112">Число теги свойства должны быть включены в новой структуры.</span><span class="sxs-lookup"><span data-stu-id="987c7-112">Count of property tags to be included in the new structure.</span></span>
    
<span data-ttu-id="987c7-113">_имя_</span><span class="sxs-lookup"><span data-stu-id="987c7-113">__name_</span></span>
  
> <span data-ttu-id="987c7-114">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="987c7-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="987c7-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="987c7-115">Remarks</span></span>

<span data-ttu-id="987c7-116">Используйте макрос **SizedSPropTagArray** для создания массива тега свойства с помощью явных границы.</span><span class="sxs-lookup"><span data-stu-id="987c7-116">Use the **SizedSPropTagArray** macro to create a property tag array with explicit bounds.</span></span> 
  
<span data-ttu-id="987c7-117">Для применения новой структуры, результаты из макроса **SizedSPropTagArray** как указатель на структуру **SPropTagArray** , выполните следующие приведения.</span><span class="sxs-lookup"><span data-stu-id="987c7-117">To use the new structure that results from the **SizedSPropTagArray** macro as a pointer to an **SPropTagArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a><span data-ttu-id="987c7-118">См. также</span><span class="sxs-lookup"><span data-stu-id="987c7-118">See also</span></span>

- [<span data-ttu-id="987c7-119">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="987c7-119">SPropTagArray</span></span>](sproptagarray.md)
- [<span data-ttu-id="987c7-120">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="987c7-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

