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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407447"
---
# <a name="sizeddtblpage"></a><span data-ttu-id="f2b05-103">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="f2b05-103">SizedDtblPage</span></span>

<span data-ttu-id="f2b05-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2b05-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2b05-105">Создает именованную структуру, которая включает структуру [DTBLPAGE](dtblpage.md) для описания управления страницей вкладки, метки определенной длины и записи файла справки указанной длины.</span><span class="sxs-lookup"><span data-stu-id="f2b05-105">Creates a named structure that includes a [DTBLPAGE](dtblpage.md) structure for describing a tabbed page control, a label of a specified length, and a Help file entry of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f2b05-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f2b05-106">Header file:</span></span>  <br/> |<span data-ttu-id="f2b05-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f2b05-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f2b05-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="f2b05-108">Related structure:</span></span>  <br/> |<span data-ttu-id="f2b05-109">**DTBLPAGE**</span><span class="sxs-lookup"><span data-stu-id="f2b05-109">**DTBLPAGE**</span></span> <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a><span data-ttu-id="f2b05-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="f2b05-110">Parameters</span></span>

<span data-ttu-id="f2b05-111">_n_</span><span class="sxs-lookup"><span data-stu-id="f2b05-111">_n_</span></span>
  
> <span data-ttu-id="f2b05-112">Длина метки для вкладки страницы.</span><span class="sxs-lookup"><span data-stu-id="f2b05-112">Length of the label for the page tab.</span></span>
    
<span data-ttu-id="f2b05-113">_n1_</span><span class="sxs-lookup"><span data-stu-id="f2b05-113">_n1_</span></span>
  
> <span data-ttu-id="f2b05-114">Длина записи, которая появится в файле Mapisvc.inf, определяя файл справки, который будет использоваться с помощью управления страницей вкладки.</span><span class="sxs-lookup"><span data-stu-id="f2b05-114">Length of the entry appearing in the Mapisvc.inf file identifying the Help file that will be used with the tabbed page control.</span></span>
    
<span data-ttu-id="f2b05-115">_u_</span><span class="sxs-lookup"><span data-stu-id="f2b05-115">_u_</span></span>
  
> <span data-ttu-id="f2b05-116">Имя новой структуры.</span><span class="sxs-lookup"><span data-stu-id="f2b05-116">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f2b05-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="f2b05-117">Remarks</span></span>

<span data-ttu-id="f2b05-118">Макрос **SizedDtblPage** позволяет определить управление страницей вкладок, когда известно количество символов в связанной метке и записи файла справки.</span><span class="sxs-lookup"><span data-stu-id="f2b05-118">The **SizedDtblPage** macro lets you define a tabbed page control when the number of characters in the associated label and Help file entry is known.</span></span> <span data-ttu-id="f2b05-119">Новая структура создается со следующими участниками:</span><span class="sxs-lookup"><span data-stu-id="f2b05-119">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

<span data-ttu-id="f2b05-120">Чтобы использовать указатель на результатовую структуру макроса **SizedDtblPage** в качестве указателя **структуры DTBLPAGE,** выполните следующий бросок:</span><span class="sxs-lookup"><span data-stu-id="f2b05-120">To use a pointer to the resulting structure from the **SizedDtblPage** macro as a **DTBLPAGE** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a><span data-ttu-id="f2b05-121">См. также</span><span class="sxs-lookup"><span data-stu-id="f2b05-121">See also</span></span>

- [<span data-ttu-id="f2b05-122">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="f2b05-122">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="f2b05-123">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="f2b05-123">Macros Related to Structures</span></span>](macros-related-to-structures.md)

