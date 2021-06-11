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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429350"
---
# <a name="sizedsproptagarray"></a><span data-ttu-id="4e620-103">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="4e620-103">SizedSPropTagArray</span></span>

<span data-ttu-id="4e620-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e620-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e620-105">Создает структуру [SPropTagArray](sproptagarray.md) с указанным числом тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="4e620-105">Creates a named [SPropTagArray](sproptagarray.md) structure that includes a specified number of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4e620-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="4e620-106">Header file:</span></span>  <br/> |<span data-ttu-id="4e620-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4e620-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4e620-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="4e620-108">Related structure:</span></span>  <br/> |<span data-ttu-id="4e620-109">**SPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="4e620-109">**SPropTagArray**</span></span> <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a><span data-ttu-id="4e620-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="4e620-110">Parameters</span></span>

<span data-ttu-id="4e620-111">_ _ctag_</span><span class="sxs-lookup"><span data-stu-id="4e620-111">_ _ctag_</span></span>
  
> <span data-ttu-id="4e620-112">Количество тегов свойств, которые будут включены в новую структуру.</span><span class="sxs-lookup"><span data-stu-id="4e620-112">Count of property tags to be included in the new structure.</span></span>
    
<span data-ttu-id="4e620-113">_ _имя_</span><span class="sxs-lookup"><span data-stu-id="4e620-113">_ _name_</span></span>
  
> <span data-ttu-id="4e620-114">Имя новой структуры.</span><span class="sxs-lookup"><span data-stu-id="4e620-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4e620-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="4e620-115">Remarks</span></span>

<span data-ttu-id="4e620-116">Используйте **макрос SizedSPropTagArray** для создания массива тегов свойств с явными границами.</span><span class="sxs-lookup"><span data-stu-id="4e620-116">Use the **SizedSPropTagArray** macro to create a property tag array with explicit bounds.</span></span> 
  
<span data-ttu-id="4e620-117">Чтобы использовать новую структуру, которая является результатом макроса **SizedSPropTagArray** в качестве указателя на **структуру SPropTagArray,** выполните следующие броски:</span><span class="sxs-lookup"><span data-stu-id="4e620-117">To use the new structure that results from the **SizedSPropTagArray** macro as a pointer to an **SPropTagArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a><span data-ttu-id="4e620-118">См. также</span><span class="sxs-lookup"><span data-stu-id="4e620-118">See also</span></span>

- [<span data-ttu-id="4e620-119">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="4e620-119">SPropTagArray</span></span>](sproptagarray.md)
- [<span data-ttu-id="4e620-120">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="4e620-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

