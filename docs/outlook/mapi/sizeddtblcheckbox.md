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
ms.openlocfilehash: 6120439ea0d98ed6b64fe1542a4372265574723a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567533"
---
# <a name="sizeddtblcheckbox"></a><span data-ttu-id="235e6-103">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="235e6-103">SizedDtblCheckBox</span></span>
 
<span data-ttu-id="235e6-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="235e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="235e6-105">Создает именованный структуру, которая включает в себя структуры [DTBLCHECKBOX](dtblcheckbox.md) для описания элемента управления "флажок" и метки заданной длины.</span><span class="sxs-lookup"><span data-stu-id="235e6-105">Creates a named structure that includes a [DTBLCHECKBOX](dtblcheckbox.md) structure for describing a check box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="235e6-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="235e6-106">Header file:</span></span>  <br/> |<span data-ttu-id="235e6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="235e6-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="235e6-108">Связанные структуры:</span><span class="sxs-lookup"><span data-stu-id="235e6-108">Related structure:</span></span>  <br/> |<span data-ttu-id="235e6-109">**DTBLCHECKBOX**</span><span class="sxs-lookup"><span data-stu-id="235e6-109">**DTBLCHECKBOX**</span></span> <br/> |
   
```cpp
SizedDtblCheckBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="235e6-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="235e6-110">Parameters</span></span>

<span data-ttu-id="235e6-111">_n_</span><span class="sxs-lookup"><span data-stu-id="235e6-111">_n_</span></span>
  
> <span data-ttu-id="235e6-112">Длина метки должны быть включены в новой структуры.</span><span class="sxs-lookup"><span data-stu-id="235e6-112">Length of the label to be included in the new structure.</span></span>
    
<span data-ttu-id="235e6-113">_u_</span><span class="sxs-lookup"><span data-stu-id="235e6-113">_u_</span></span>
  
> <span data-ttu-id="235e6-114">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="235e6-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="235e6-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="235e6-115">Remarks</span></span>

<span data-ttu-id="235e6-116">Макрос **SizedDtblCheckBox** позволяет определить флажок при известные число знаков метки.</span><span class="sxs-lookup"><span data-stu-id="235e6-116">The **SizedDtblCheckBox** macro lets you define a check box when the number of label characters is known.</span></span> <span data-ttu-id="235e6-117">Новая структура создается с следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="235e6-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

<span data-ttu-id="235e6-118">Чтобы использовать указатель в итоговый структуру из макроса **SizedDtblCheckBox** как указатель на структуру **DTBLCHECKBOX** , выполните следующие приведения:</span><span class="sxs-lookup"><span data-stu-id="235e6-118">To use a pointer to the resulting structure from the **SizedDtblCheckBox** macro as a **DTBLCHECKBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a><span data-ttu-id="235e6-119">См. также</span><span class="sxs-lookup"><span data-stu-id="235e6-119">See also</span></span>

- [<span data-ttu-id="235e6-120">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="235e6-120">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="235e6-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="235e6-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

