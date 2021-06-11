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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420810"
---
# <a name="sizeddtblcheckbox"></a><span data-ttu-id="16e47-103">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="16e47-103">SizedDtblCheckBox</span></span>
 
<span data-ttu-id="16e47-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16e47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16e47-105">Создает именованную структуру, которая включает структуру [DTBLCHECKBOX](dtblcheckbox.md) для описания управления контрольным окном и метки определенной длины.</span><span class="sxs-lookup"><span data-stu-id="16e47-105">Creates a named structure that includes a [DTBLCHECKBOX](dtblcheckbox.md) structure for describing a check box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="16e47-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="16e47-106">Header file:</span></span>  <br/> |<span data-ttu-id="16e47-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="16e47-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="16e47-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="16e47-108">Related structure:</span></span>  <br/> |<span data-ttu-id="16e47-109">**DTBLCHECKBOX**</span><span class="sxs-lookup"><span data-stu-id="16e47-109">**DTBLCHECKBOX**</span></span> <br/> |
   
```cpp
SizedDtblCheckBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="16e47-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="16e47-110">Parameters</span></span>

<span data-ttu-id="16e47-111">_n_</span><span class="sxs-lookup"><span data-stu-id="16e47-111">_n_</span></span>
  
> <span data-ttu-id="16e47-112">Длина метки, которая будет включена в новую структуру.</span><span class="sxs-lookup"><span data-stu-id="16e47-112">Length of the label to be included in the new structure.</span></span>
    
<span data-ttu-id="16e47-113">_u_</span><span class="sxs-lookup"><span data-stu-id="16e47-113">_u_</span></span>
  
> <span data-ttu-id="16e47-114">Имя новой структуры.</span><span class="sxs-lookup"><span data-stu-id="16e47-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="16e47-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="16e47-115">Remarks</span></span>

<span data-ttu-id="16e47-116">Макрос **SizedDtblCheckBox** позволяет определить контрольный ящик, если известно число символов метки.</span><span class="sxs-lookup"><span data-stu-id="16e47-116">The **SizedDtblCheckBox** macro lets you define a check box when the number of label characters is known.</span></span> <span data-ttu-id="16e47-117">Новая структура создается со следующими участниками:</span><span class="sxs-lookup"><span data-stu-id="16e47-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

<span data-ttu-id="16e47-118">Чтобы использовать указатель на следующую структуру из **макроса SizedDtblCheckBox** в качестве указателя **структуры DTBLCHECKBOX,** выполните следующий бросок:</span><span class="sxs-lookup"><span data-stu-id="16e47-118">To use a pointer to the resulting structure from the **SizedDtblCheckBox** macro as a **DTBLCHECKBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a><span data-ttu-id="16e47-119">См. также</span><span class="sxs-lookup"><span data-stu-id="16e47-119">See also</span></span>

- [<span data-ttu-id="16e47-120">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="16e47-120">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="16e47-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="16e47-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

