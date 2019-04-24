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
ms.openlocfilehash: f14b8d7a9a73997f797f9cfa26a2e574222e839e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282659"
---
# <a name="sizeddtblpage"></a><span data-ttu-id="52b69-103">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="52b69-103">SizedDtblPage</span></span>

<span data-ttu-id="52b69-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52b69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52b69-105">Создает именованную структуру, которая включает структуру [дтблпаже](dtblpage.md) для описания элемента управления страницы с вкладками, метку указанной длины и запись файла справки с указанной длиной.</span><span class="sxs-lookup"><span data-stu-id="52b69-105">Creates a named structure that includes a [DTBLPAGE](dtblpage.md) structure for describing a tabbed page control, a label of a specified length, and a Help file entry of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="52b69-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="52b69-106">Header file:</span></span>  <br/> |<span data-ttu-id="52b69-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="52b69-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="52b69-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="52b69-108">Related structure:</span></span>  <br/> |<span data-ttu-id="52b69-109">**DTBLPAGE**</span><span class="sxs-lookup"><span data-stu-id="52b69-109">**DTBLPAGE**</span></span> <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a><span data-ttu-id="52b69-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="52b69-110">Parameters</span></span>

<span data-ttu-id="52b69-111">_n_</span><span class="sxs-lookup"><span data-stu-id="52b69-111">_n_</span></span>
  
> <span data-ttu-id="52b69-112">Длина метки для вкладки страницы.</span><span class="sxs-lookup"><span data-stu-id="52b69-112">Length of the label for the page tab.</span></span>
    
<span data-ttu-id="52b69-113">_N1_</span><span class="sxs-lookup"><span data-stu-id="52b69-113">_n1_</span></span>
  
> <span data-ttu-id="52b69-114">Длина записи в файле Mapisvc. INF, определяющая файл справки, который будет использоваться с элементом управления со вкладками.</span><span class="sxs-lookup"><span data-stu-id="52b69-114">Length of the entry appearing in the Mapisvc.inf file identifying the Help file that will be used with the tabbed page control.</span></span>
    
<span data-ttu-id="52b69-115">_u_</span><span class="sxs-lookup"><span data-stu-id="52b69-115">_u_</span></span>
  
> <span data-ttu-id="52b69-116">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="52b69-116">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="52b69-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="52b69-117">Remarks</span></span>

<span data-ttu-id="52b69-118">Макрос **сизеддтблпаже** позволяет определить элемент управления со вкладками, если известно число символов в связанной метке и записи файла справки.</span><span class="sxs-lookup"><span data-stu-id="52b69-118">The **SizedDtblPage** macro lets you define a tabbed page control when the number of characters in the associated label and Help file entry is known.</span></span> <span data-ttu-id="52b69-119">Новая структура создается со следующими элементами:</span><span class="sxs-lookup"><span data-stu-id="52b69-119">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

<span data-ttu-id="52b69-120">Чтобы использовать указатель на полученную структуру из макроса **сизеддтблпаже** в качестве указателя структуры **дтблпаже** , выполните следующую операцию приведения:</span><span class="sxs-lookup"><span data-stu-id="52b69-120">To use a pointer to the resulting structure from the **SizedDtblPage** macro as a **DTBLPAGE** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a><span data-ttu-id="52b69-121">См. также</span><span class="sxs-lookup"><span data-stu-id="52b69-121">See also</span></span>

- [<span data-ttu-id="52b69-122">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="52b69-122">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="52b69-123">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="52b69-123">Macros Related to Structures</span></span>](macros-related-to-structures.md)

