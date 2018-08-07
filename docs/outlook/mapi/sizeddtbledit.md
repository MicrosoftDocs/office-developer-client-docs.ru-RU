---
title: SizedDtblEdit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblEdit
api_type:
- COM
ms.assetid: a658d027-03a2-4cde-bf99-563e8521cb31
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4ea77023bdc9442325f4af46d23c107e7172ceaf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812297"
---
# <a name="sizeddtbledit"></a><span data-ttu-id="ba92b-103">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="ba92b-103">SizedDtblEdit</span></span>

<span data-ttu-id="ba92b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ba92b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ba92b-105">Создает именованный структуру, которая включает в себя структуры [DTBLEDIT](dtbledit.md) для описания элемента управления и максимальное число символов, которые могут быть введены в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="ba92b-105">Creates a named structure that includes a [DTBLEDIT](dtbledit.md) structure for describing an edit control and the maximum number of characters that can be entered in the control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ba92b-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ba92b-106">Header file:</span></span>  <br/> |<span data-ttu-id="ba92b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ba92b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ba92b-108">Связанные структуры:</span><span class="sxs-lookup"><span data-stu-id="ba92b-108">Related structure:</span></span>  <br/> |<span data-ttu-id="ba92b-109">**DTBLEDIT**</span><span class="sxs-lookup"><span data-stu-id="ba92b-109">**DTBLEDIT**</span></span> <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a><span data-ttu-id="ba92b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba92b-110">Parameters</span></span>

<span data-ttu-id="ba92b-111">_n_</span><span class="sxs-lookup"><span data-stu-id="ba92b-111">_n_</span></span>
  
> <span data-ttu-id="ba92b-112">Максимальное число символов, которые можно ввести в элемент управления для редактирования.</span><span class="sxs-lookup"><span data-stu-id="ba92b-112">Maximum number of characters that can be entered in the edit control.</span></span>
    
<span data-ttu-id="ba92b-113">_u_</span><span class="sxs-lookup"><span data-stu-id="ba92b-113">_u_</span></span>
  
> <span data-ttu-id="ba92b-114">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="ba92b-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ba92b-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="ba92b-115">Remarks</span></span>

<span data-ttu-id="ba92b-116">Макрос **SizedDtblEdit** позволяет определить элемента управления, если известен число включенных символов.</span><span class="sxs-lookup"><span data-stu-id="ba92b-116">The **SizedDtblEdit** macro lets you define an edit control when the number of enabled characters is known.</span></span> <span data-ttu-id="ba92b-117">Новая структура создается с следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="ba92b-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="ba92b-118">Чтобы использовать указатель в итоговый структуру из макроса **SizedDtblEdit** как указатель на структуру **DTBLEDIT** , выполните следующие приведения:</span><span class="sxs-lookup"><span data-stu-id="ba92b-118">To use a pointer to the resulting structure from the **SizedDtblEdit** macro as a **DTBLEDIT** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a><span data-ttu-id="ba92b-119">См. также</span><span class="sxs-lookup"><span data-stu-id="ba92b-119">See also</span></span>

- [<span data-ttu-id="ba92b-120">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="ba92b-120">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="ba92b-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="ba92b-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

