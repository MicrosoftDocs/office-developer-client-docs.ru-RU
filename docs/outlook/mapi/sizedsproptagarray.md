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
ms.openlocfilehash: 363a85e1c6f111936b16e471eda6b9f962f8b65d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573623"
---
# <a name="sizedsproptagarray"></a><span data-ttu-id="a5222-103">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="a5222-103">SizedSPropTagArray</span></span>

<span data-ttu-id="a5222-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5222-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5222-105">Создает структуру [SPropTagArray](sproptagarray.md) именованные, содержащий указанное число тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="a5222-105">Creates a named [SPropTagArray](sproptagarray.md) structure that includes a specified number of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a5222-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a5222-106">Header file:</span></span>  <br/> |<span data-ttu-id="a5222-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a5222-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a5222-108">Связанные структуры:</span><span class="sxs-lookup"><span data-stu-id="a5222-108">Related structure:</span></span>  <br/> |<span data-ttu-id="a5222-109">**SPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="a5222-109">**SPropTagArray**</span></span> <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a><span data-ttu-id="a5222-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5222-110">Parameters</span></span>

<span data-ttu-id="a5222-111">__ctag_</span><span class="sxs-lookup"><span data-stu-id="a5222-111">__ctag_</span></span>
  
> <span data-ttu-id="a5222-112">Число теги свойства должны быть включены в новой структуры.</span><span class="sxs-lookup"><span data-stu-id="a5222-112">Count of property tags to be included in the new structure.</span></span>
    
<span data-ttu-id="a5222-113">_имя_</span><span class="sxs-lookup"><span data-stu-id="a5222-113">__name_</span></span>
  
> <span data-ttu-id="a5222-114">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="a5222-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a5222-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="a5222-115">Remarks</span></span>

<span data-ttu-id="a5222-116">Используйте макрос **SizedSPropTagArray** для создания массива тега свойства с помощью явных границы.</span><span class="sxs-lookup"><span data-stu-id="a5222-116">Use the **SizedSPropTagArray** macro to create a property tag array with explicit bounds.</span></span> 
  
<span data-ttu-id="a5222-117">Для применения новой структуры, результаты из макроса **SizedSPropTagArray** как указатель на структуру **SPropTagArray** , выполните следующие приведения.</span><span class="sxs-lookup"><span data-stu-id="a5222-117">To use the new structure that results from the **SizedSPropTagArray** macro as a pointer to an **SPropTagArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a><span data-ttu-id="a5222-118">См. также</span><span class="sxs-lookup"><span data-stu-id="a5222-118">See also</span></span>

- [<span data-ttu-id="a5222-119">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="a5222-119">SPropTagArray</span></span>](sproptagarray.md)
- [<span data-ttu-id="a5222-120">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="a5222-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

