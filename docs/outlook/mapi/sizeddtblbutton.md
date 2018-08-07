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
ms.openlocfilehash: 3de56b12fa7d34004fddbfe3633b8b8307c0ffc1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812290"
---
# <a name="sizeddtblbutton"></a><span data-ttu-id="874b1-103">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="874b1-103">SizedDtblButton</span></span>

  
  
<span data-ttu-id="874b1-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="874b1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="874b1-105">Создает именованный структуру, которая включает в себя структуры [DTBLBUTTON](dtblbutton.md) для описания кнопки и метки заданной длины.</span><span class="sxs-lookup"><span data-stu-id="874b1-105">Creates a named structure that includes a [DTBLBUTTON](dtblbutton.md) structure for describing a button and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="874b1-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="874b1-106">Header file:</span></span>  <br/> |<span data-ttu-id="874b1-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="874b1-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="874b1-108">Связанные структуры:</span><span class="sxs-lookup"><span data-stu-id="874b1-108">Related structure:</span></span>  <br/> |<span data-ttu-id="874b1-109">**DTBLBUTTON**</span><span class="sxs-lookup"><span data-stu-id="874b1-109">**DTBLBUTTON**</span></span> <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a><span data-ttu-id="874b1-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="874b1-110">Parameters</span></span>

 <span data-ttu-id="874b1-111">_n_</span><span class="sxs-lookup"><span data-stu-id="874b1-111">_n_</span></span>
  
> <span data-ttu-id="874b1-112">Длина метки должны быть включены в новой структуры.</span><span class="sxs-lookup"><span data-stu-id="874b1-112">Length of the label to be included in the new structure.</span></span>
    
 <span data-ttu-id="874b1-113">_u_</span><span class="sxs-lookup"><span data-stu-id="874b1-113">_u_</span></span>
  
> <span data-ttu-id="874b1-114">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="874b1-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="874b1-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="874b1-115">Remarks</span></span>

<span data-ttu-id="874b1-116">Новая структура создается с следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="874b1-116">The new structure is created with the following members:</span></span>
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a><span data-ttu-id="874b1-117">См. также</span><span class="sxs-lookup"><span data-stu-id="874b1-117">See also</span></span>



[<span data-ttu-id="874b1-118">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="874b1-118">DTBLBUTTON</span></span>](dtblbutton.md)


[<span data-ttu-id="874b1-119">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="874b1-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

