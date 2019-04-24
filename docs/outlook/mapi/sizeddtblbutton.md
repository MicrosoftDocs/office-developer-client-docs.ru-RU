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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282763"
---
# <a name="sizeddtblbutton"></a><span data-ttu-id="66c91-103">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="66c91-103">SizedDtblButton</span></span>

  
  
<span data-ttu-id="66c91-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66c91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66c91-105">Создает именованную структуру, включающую структуру [дтблбуттон](dtblbutton.md) для описания кнопки и метки заданной длины.</span><span class="sxs-lookup"><span data-stu-id="66c91-105">Creates a named structure that includes a [DTBLBUTTON](dtblbutton.md) structure for describing a button and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="66c91-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="66c91-106">Header file:</span></span>  <br/> |<span data-ttu-id="66c91-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="66c91-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="66c91-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="66c91-108">Related structure:</span></span>  <br/> |<span data-ttu-id="66c91-109">**DTBLBUTTON**</span><span class="sxs-lookup"><span data-stu-id="66c91-109">**DTBLBUTTON**</span></span> <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a><span data-ttu-id="66c91-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="66c91-110">Parameters</span></span>

 <span data-ttu-id="66c91-111">_n_</span><span class="sxs-lookup"><span data-stu-id="66c91-111">_n_</span></span>
  
> <span data-ttu-id="66c91-112">Длина метки, которая должна быть включена в новую структуру.</span><span class="sxs-lookup"><span data-stu-id="66c91-112">Length of the label to be included in the new structure.</span></span>
    
 <span data-ttu-id="66c91-113">_u_</span><span class="sxs-lookup"><span data-stu-id="66c91-113">_u_</span></span>
  
> <span data-ttu-id="66c91-114">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="66c91-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="66c91-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="66c91-115">Remarks</span></span>

<span data-ttu-id="66c91-116">Новая структура создается со следующими элементами:</span><span class="sxs-lookup"><span data-stu-id="66c91-116">The new structure is created with the following members:</span></span>
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a><span data-ttu-id="66c91-117">См. также</span><span class="sxs-lookup"><span data-stu-id="66c91-117">See also</span></span>



[<span data-ttu-id="66c91-118">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="66c91-118">DTBLBUTTON</span></span>](dtblbutton.md)


[<span data-ttu-id="66c91-119">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="66c91-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

