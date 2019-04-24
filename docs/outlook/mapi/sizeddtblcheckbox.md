---
title: SizedDtblCheckBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblCheckBox
api_type:
- COM
ms.assetid: 9d04a124-54d4-43ac-967f-ea8e7a09b1d0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6d23d56a27095497aedc64d7bbf5ffda266d0c97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282756"
---
# <a name="sizeddtblcheckbox"></a><span data-ttu-id="3a3b6-103">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="3a3b6-103">SizedDtblCheckBox</span></span>
 
<span data-ttu-id="3a3b6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a3b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a3b6-105">Создает именованную структуру, которая включает структуру [дтблчеккбокс](dtblcheckbox.md) для описания элемента управления "флажок" и метку указанной длины.</span><span class="sxs-lookup"><span data-stu-id="3a3b6-105">Creates a named structure that includes a [DTBLCHECKBOX](dtblcheckbox.md) structure for describing a check box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3a3b6-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3a3b6-106">Header file:</span></span>  <br/> |<span data-ttu-id="3a3b6-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="3a3b6-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3a3b6-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="3a3b6-108">Related structure:</span></span>  <br/> |<span data-ttu-id="3a3b6-109">**DTBLCHECKBOX**</span><span class="sxs-lookup"><span data-stu-id="3a3b6-109">**DTBLCHECKBOX**</span></span> <br/> |
   
```cpp
SizedDtblCheckBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="3a3b6-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a3b6-110">Parameters</span></span>

<span data-ttu-id="3a3b6-111">_n_</span><span class="sxs-lookup"><span data-stu-id="3a3b6-111">_n_</span></span>
  
> <span data-ttu-id="3a3b6-112">Длина метки, которая должна быть включена в новую структуру.</span><span class="sxs-lookup"><span data-stu-id="3a3b6-112">Length of the label to be included in the new structure.</span></span>
    
<span data-ttu-id="3a3b6-113">_u_</span><span class="sxs-lookup"><span data-stu-id="3a3b6-113">_u_</span></span>
  
> <span data-ttu-id="3a3b6-114">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="3a3b6-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3a3b6-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="3a3b6-115">Remarks</span></span>

<span data-ttu-id="3a3b6-116">Макрос **сизеддтблчеккбокс** позволяет установить флажок, если число символов в метке известно.</span><span class="sxs-lookup"><span data-stu-id="3a3b6-116">The **SizedDtblCheckBox** macro lets you define a check box when the number of label characters is known.</span></span> <span data-ttu-id="3a3b6-117">Новая структура создается со следующими элементами:</span><span class="sxs-lookup"><span data-stu-id="3a3b6-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

<span data-ttu-id="3a3b6-118">Чтобы использовать указатель на полученную структуру из макроса **сизеддтблчеккбокс** в качестве указателя структуры **дтблчеккбокс** , выполните следующую операцию приведения:</span><span class="sxs-lookup"><span data-stu-id="3a3b6-118">To use a pointer to the resulting structure from the **SizedDtblCheckBox** macro as a **DTBLCHECKBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a><span data-ttu-id="3a3b6-119">См. также</span><span class="sxs-lookup"><span data-stu-id="3a3b6-119">See also</span></span>

- [<span data-ttu-id="3a3b6-120">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="3a3b6-120">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="3a3b6-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="3a3b6-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

