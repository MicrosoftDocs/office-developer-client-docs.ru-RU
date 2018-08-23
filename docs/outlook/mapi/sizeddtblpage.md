---
title: SizedDtblPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblPage
api_type:
- COM
ms.assetid: 47b2a69d-e902-429f-8b31-166b51aeaf7f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ae3f84c6b219c7becb88737f0d6c9fcb9722ea34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584970"
---
# <a name="sizeddtblpage"></a><span data-ttu-id="58f46-103">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="58f46-103">SizedDtblPage</span></span>

<span data-ttu-id="58f46-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58f46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58f46-105">Создание именованного структуру, которая включает в себя структуры [DTBLPAGE](dtblpage.md) для описания элемента управления вкладки, метки заданной длины и запись в файле справки заданной длины.</span><span class="sxs-lookup"><span data-stu-id="58f46-105">Creates a named structure that includes a [DTBLPAGE](dtblpage.md) structure for describing a tabbed page control, a label of a specified length, and a Help file entry of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="58f46-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="58f46-106">Header file:</span></span>  <br/> |<span data-ttu-id="58f46-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="58f46-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="58f46-108">Связанные структуры:</span><span class="sxs-lookup"><span data-stu-id="58f46-108">Related structure:</span></span>  <br/> |<span data-ttu-id="58f46-109">**DTBLPAGE**</span><span class="sxs-lookup"><span data-stu-id="58f46-109">**DTBLPAGE**</span></span> <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a><span data-ttu-id="58f46-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="58f46-110">Parameters</span></span>

<span data-ttu-id="58f46-111">_n_</span><span class="sxs-lookup"><span data-stu-id="58f46-111">_n_</span></span>
  
> <span data-ttu-id="58f46-112">Длина метки для вкладку страница.</span><span class="sxs-lookup"><span data-stu-id="58f46-112">Length of the label for the page tab.</span></span>
    
<span data-ttu-id="58f46-113">_N1_</span><span class="sxs-lookup"><span data-stu-id="58f46-113">_n1_</span></span>
  
> <span data-ttu-id="58f46-114">Длина записи, изображения которых появляются в файла Mapisvc.inf, идентифицирующий файл справки, который будет использоваться с элементом управления страницы с вкладками.</span><span class="sxs-lookup"><span data-stu-id="58f46-114">Length of the entry appearing in the Mapisvc.inf file identifying the Help file that will be used with the tabbed page control.</span></span>
    
<span data-ttu-id="58f46-115">_u_</span><span class="sxs-lookup"><span data-stu-id="58f46-115">_u_</span></span>
  
> <span data-ttu-id="58f46-116">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="58f46-116">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="58f46-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="58f46-117">Remarks</span></span>

<span data-ttu-id="58f46-118">Макрос **SizedDtblPage** позволяет определить элемент управления вкладки при известно количество символов в связанные метки и запись файла справки.</span><span class="sxs-lookup"><span data-stu-id="58f46-118">The **SizedDtblPage** macro lets you define a tabbed page control when the number of characters in the associated label and Help file entry is known.</span></span> <span data-ttu-id="58f46-119">Новая структура создается с следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="58f46-119">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

<span data-ttu-id="58f46-120">Чтобы использовать указатель в итоговый структуру из макроса **SizedDtblPage** как указатель на структуру **DTBLPAGE** , выполните следующие приведения:</span><span class="sxs-lookup"><span data-stu-id="58f46-120">To use a pointer to the resulting structure from the **SizedDtblPage** macro as a **DTBLPAGE** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a><span data-ttu-id="58f46-121">См. также</span><span class="sxs-lookup"><span data-stu-id="58f46-121">See also</span></span>

- [<span data-ttu-id="58f46-122">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="58f46-122">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="58f46-123">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="58f46-123">Macros Related to Structures</span></span>](macros-related-to-structures.md)

