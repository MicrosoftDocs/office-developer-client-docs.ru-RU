---
title: SizedDtblButton
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblButton
api_type:
- COM
ms.assetid: ee73ced9-14d8-4a30-9b9f-d54ed9c3a454
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: dc4d3a7a827e728dfd6725ac269350067d4530cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590346"
---
# <a name="sizeddtblbutton"></a><span data-ttu-id="372b4-103">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="372b4-103">SizedDtblButton</span></span>

  
  
<span data-ttu-id="372b4-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="372b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="372b4-105">Создает именованный структуру, которая включает в себя структуры [DTBLBUTTON](dtblbutton.md) для описания кнопки и метки заданной длины.</span><span class="sxs-lookup"><span data-stu-id="372b4-105">Creates a named structure that includes a [DTBLBUTTON](dtblbutton.md) structure for describing a button and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="372b4-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="372b4-106">Header file:</span></span>  <br/> |<span data-ttu-id="372b4-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="372b4-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="372b4-108">Связанные структуры:</span><span class="sxs-lookup"><span data-stu-id="372b4-108">Related structure:</span></span>  <br/> |<span data-ttu-id="372b4-109">**DTBLBUTTON**</span><span class="sxs-lookup"><span data-stu-id="372b4-109">**DTBLBUTTON**</span></span> <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a><span data-ttu-id="372b4-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="372b4-110">Parameters</span></span>

 <span data-ttu-id="372b4-111">_n_</span><span class="sxs-lookup"><span data-stu-id="372b4-111">_n_</span></span>
  
> <span data-ttu-id="372b4-112">Длина метки должны быть включены в новой структуры.</span><span class="sxs-lookup"><span data-stu-id="372b4-112">Length of the label to be included in the new structure.</span></span>
    
 <span data-ttu-id="372b4-113">_u_</span><span class="sxs-lookup"><span data-stu-id="372b4-113">_u_</span></span>
  
> <span data-ttu-id="372b4-114">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="372b4-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="372b4-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="372b4-115">Remarks</span></span>

<span data-ttu-id="372b4-116">Новая структура создается с следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="372b4-116">The new structure is created with the following members:</span></span>
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a><span data-ttu-id="372b4-117">См. также</span><span class="sxs-lookup"><span data-stu-id="372b4-117">See also</span></span>



[<span data-ttu-id="372b4-118">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="372b4-118">DTBLBUTTON</span></span>](dtblbutton.md)


[<span data-ttu-id="372b4-119">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="372b4-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

