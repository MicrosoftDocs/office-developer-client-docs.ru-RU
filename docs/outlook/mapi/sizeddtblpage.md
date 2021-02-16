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
# <a name="sizeddtblpage"></a><span data-ttu-id="de051-103">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="de051-103">SizedDtblPage</span></span>

<span data-ttu-id="de051-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de051-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de051-105">Создает именованную структуру, включаемую в себя структуру [DTBLPAGE](dtblpage.md) для описания вкладки, метки указанной длины и записи файла справки указанной длины.</span><span class="sxs-lookup"><span data-stu-id="de051-105">Creates a named structure that includes a [DTBLPAGE](dtblpage.md) structure for describing a tabbed page control, a label of a specified length, and a Help file entry of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="de051-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="de051-106">Header file:</span></span>  <br/> |<span data-ttu-id="de051-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="de051-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="de051-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="de051-108">Related structure:</span></span>  <br/> |<span data-ttu-id="de051-109">**DTBLPAGE**</span><span class="sxs-lookup"><span data-stu-id="de051-109">**DTBLPAGE**</span></span> <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a><span data-ttu-id="de051-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="de051-110">Parameters</span></span>

<span data-ttu-id="de051-111">_n_</span><span class="sxs-lookup"><span data-stu-id="de051-111">_n_</span></span>
  
> <span data-ttu-id="de051-112">Длина метки для вкладки страницы.</span><span class="sxs-lookup"><span data-stu-id="de051-112">Length of the label for the page tab.</span></span>
    
<span data-ttu-id="de051-113">_n1_</span><span class="sxs-lookup"><span data-stu-id="de051-113">_n1_</span></span>
  
> <span data-ttu-id="de051-114">Длина записи, которая будет отображаться в файле Mapisvc.inf, определяя файл справки, который будет использоваться с вкладками на странице.</span><span class="sxs-lookup"><span data-stu-id="de051-114">Length of the entry appearing in the Mapisvc.inf file identifying the Help file that will be used with the tabbed page control.</span></span>
    
<span data-ttu-id="de051-115">_u_</span><span class="sxs-lookup"><span data-stu-id="de051-115">_u_</span></span>
  
> <span data-ttu-id="de051-116">Имя новой структуры.</span><span class="sxs-lookup"><span data-stu-id="de051-116">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="de051-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="de051-117">Remarks</span></span>

<span data-ttu-id="de051-118">Макрос **SizedDtblPage** позволяет определить табуляцию страницы, если известно количество символов в связанной метке и записи файла справки.</span><span class="sxs-lookup"><span data-stu-id="de051-118">The **SizedDtblPage** macro lets you define a tabbed page control when the number of characters in the associated label and Help file entry is known.</span></span> <span data-ttu-id="de051-119">Новая структура создается с помощью следующих членов:</span><span class="sxs-lookup"><span data-stu-id="de051-119">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

<span data-ttu-id="de051-120">Чтобы использовать указатель на итоговую структуру из макроса **SizedDtblPage** в качестве указателя структуры **DTBLPAGE,** выполните следующую привязку:</span><span class="sxs-lookup"><span data-stu-id="de051-120">To use a pointer to the resulting structure from the **SizedDtblPage** macro as a **DTBLPAGE** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a><span data-ttu-id="de051-121">См. также</span><span class="sxs-lookup"><span data-stu-id="de051-121">See also</span></span>

- [<span data-ttu-id="de051-122">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="de051-122">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="de051-123">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="de051-123">Macros Related to Structures</span></span>](macros-related-to-structures.md)

