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
ms.openlocfilehash: f873ad5234460f9f1781c7427b60d285f7486196
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282700"
---
# <a name="sizedsproptagarray"></a><span data-ttu-id="16ffb-103">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="16ffb-103">SizedSPropTagArray</span></span>

<span data-ttu-id="16ffb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16ffb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16ffb-105">Создает именованную структуру [спроптагаррай](sproptagarray.md) , которая включает указанное количество тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="16ffb-105">Creates a named [SPropTagArray](sproptagarray.md) structure that includes a specified number of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="16ffb-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="16ffb-106">Header file:</span></span>  <br/> |<span data-ttu-id="16ffb-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="16ffb-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="16ffb-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="16ffb-108">Related structure:</span></span>  <br/> |<span data-ttu-id="16ffb-109">**SPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="16ffb-109">**SPropTagArray**</span></span> <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a><span data-ttu-id="16ffb-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="16ffb-110">Parameters</span></span>

<span data-ttu-id="16ffb-111">__ctag_</span><span class="sxs-lookup"><span data-stu-id="16ffb-111">__ctag_</span></span>
  
> <span data-ttu-id="16ffb-112">Количество тегов свойств, включаемых в новую структуру.</span><span class="sxs-lookup"><span data-stu-id="16ffb-112">Count of property tags to be included in the new structure.</span></span>
    
<span data-ttu-id="16ffb-113">__имя_</span><span class="sxs-lookup"><span data-stu-id="16ffb-113">__name_</span></span>
  
> <span data-ttu-id="16ffb-114">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="16ffb-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="16ffb-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="16ffb-115">Remarks</span></span>

<span data-ttu-id="16ffb-116">С помощью макроса **сизедспроптагаррай** создайте массив тегов свойств с явными границами.</span><span class="sxs-lookup"><span data-stu-id="16ffb-116">Use the **SizedSPropTagArray** macro to create a property tag array with explicit bounds.</span></span> 
  
<span data-ttu-id="16ffb-117">Чтобы использовать новую структуру, полученную из макроса **сизедспроптагаррай** в качестве указателя на структуру **спроптагаррай** , выполните приведенные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="16ffb-117">To use the new structure that results from the **SizedSPropTagArray** macro as a pointer to an **SPropTagArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a><span data-ttu-id="16ffb-118">См. также</span><span class="sxs-lookup"><span data-stu-id="16ffb-118">See also</span></span>

- [<span data-ttu-id="16ffb-119">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="16ffb-119">SPropTagArray</span></span>](sproptagarray.md)
- [<span data-ttu-id="16ffb-120">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="16ffb-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

