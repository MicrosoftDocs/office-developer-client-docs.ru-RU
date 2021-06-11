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
ms.openlocfilehash: a7d62d29638ae234667eb33a8103fb3a716afc32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421916"
---
# <a name="sizeddtblbutton"></a><span data-ttu-id="835f2-103">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="835f2-103">SizedDtblButton</span></span>

  
  
<span data-ttu-id="835f2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="835f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="835f2-105">Создает именованную структуру, которая включает [структуру DTBLBUTTON](dtblbutton.md) для описания кнопки и метки определенной длины.</span><span class="sxs-lookup"><span data-stu-id="835f2-105">Creates a named structure that includes a [DTBLBUTTON](dtblbutton.md) structure for describing a button and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="835f2-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="835f2-106">Header file:</span></span>  <br/> |<span data-ttu-id="835f2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="835f2-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="835f2-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="835f2-108">Related structure:</span></span>  <br/> |<span data-ttu-id="835f2-109">**DTBLBUTTON**</span><span class="sxs-lookup"><span data-stu-id="835f2-109">**DTBLBUTTON**</span></span> <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a><span data-ttu-id="835f2-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="835f2-110">Parameters</span></span>

 <span data-ttu-id="835f2-111">_n_</span><span class="sxs-lookup"><span data-stu-id="835f2-111">_n_</span></span>
  
> <span data-ttu-id="835f2-112">Длина метки, которая будет включена в новую структуру.</span><span class="sxs-lookup"><span data-stu-id="835f2-112">Length of the label to be included in the new structure.</span></span>
    
 <span data-ttu-id="835f2-113">_u_</span><span class="sxs-lookup"><span data-stu-id="835f2-113">_u_</span></span>
  
> <span data-ttu-id="835f2-114">Имя новой структуры.</span><span class="sxs-lookup"><span data-stu-id="835f2-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="835f2-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="835f2-115">Remarks</span></span>

<span data-ttu-id="835f2-116">Новая структура создается со следующими участниками:</span><span class="sxs-lookup"><span data-stu-id="835f2-116">The new structure is created with the following members:</span></span>
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a><span data-ttu-id="835f2-117">См. также</span><span class="sxs-lookup"><span data-stu-id="835f2-117">See also</span></span>



[<span data-ttu-id="835f2-118">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="835f2-118">DTBLBUTTON</span></span>](dtblbutton.md)


[<span data-ttu-id="835f2-119">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="835f2-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

