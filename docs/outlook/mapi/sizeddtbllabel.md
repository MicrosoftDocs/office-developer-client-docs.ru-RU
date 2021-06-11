---
title: SizedDtblLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblLabel
api_type:
- COM
ms.assetid: c7cb8cf9-7abd-4ee3-b88c-d61695f4ed31
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1ae675d1d4adf841e18bbfc8990913136afe8b4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408616"
---
# <a name="sizeddtbllabel"></a><span data-ttu-id="3bc40-103">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="3bc40-103">SizedDtblLabel</span></span>

<span data-ttu-id="3bc40-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3bc40-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3bc40-105">Создает именоваемую структуру, которая включает структуру [DTBLLABEL](dtbllabel.md) для описания управления меткой и связанной метки указанной длины.</span><span class="sxs-lookup"><span data-stu-id="3bc40-105">Creates a named structure that includes a [DTBLLABEL](dtbllabel.md) structure for describing a label control and the associated label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3bc40-106">Указанный в файле загона:</span><span class="sxs-lookup"><span data-stu-id="3bc40-106">Specified in header file:</span></span>  <br/> |<span data-ttu-id="3bc40-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3bc40-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3bc40-108">Связанная структура</span><span class="sxs-lookup"><span data-stu-id="3bc40-108">Related structure</span></span>  <br/> |<span data-ttu-id="3bc40-109">**DTBLLABEL**</span><span class="sxs-lookup"><span data-stu-id="3bc40-109">**DTBLLABEL**</span></span> <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a><span data-ttu-id="3bc40-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="3bc40-110">Parameters</span></span>

<span data-ttu-id="3bc40-111">_n_</span><span class="sxs-lookup"><span data-stu-id="3bc40-111">_n_</span></span>
  
> <span data-ttu-id="3bc40-112">Длина метки.</span><span class="sxs-lookup"><span data-stu-id="3bc40-112">Length of the label.</span></span> <span data-ttu-id="3bc40-113">Это включает в себя завершающий символ NULL.</span><span class="sxs-lookup"><span data-stu-id="3bc40-113">This includes the ending NULL character.</span></span> 
    
<span data-ttu-id="3bc40-114">_u_</span><span class="sxs-lookup"><span data-stu-id="3bc40-114">_u_</span></span>
  
> <span data-ttu-id="3bc40-115">Имя новой структуры.</span><span class="sxs-lookup"><span data-stu-id="3bc40-115">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3bc40-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="3bc40-116">Remarks</span></span>

<span data-ttu-id="3bc40-117">Макрос **SizedDtblLabel** позволяет определить метку таблицы отображения, когда известно количество символов в мете.</span><span class="sxs-lookup"><span data-stu-id="3bc40-117">The **SizedDtblLabel** macro lets you define a display table label when the number of characters in the label is known.</span></span> <span data-ttu-id="3bc40-118">Новая структура создается со следующими участниками:</span><span class="sxs-lookup"><span data-stu-id="3bc40-118">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

<span data-ttu-id="3bc40-119">Чтобы использовать указатель на результатовую структуру макроса **SizedDtblLabel** в качестве указателя **структуры DTBLLABEL,** выполните следующий бросок:</span><span class="sxs-lookup"><span data-stu-id="3bc40-119">To use a pointer to the resulting structure from the **SizedDtblLabel** macro as a **DTBLLABEL** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a><span data-ttu-id="3bc40-120">См. также</span><span class="sxs-lookup"><span data-stu-id="3bc40-120">See also</span></span>

- [<span data-ttu-id="3bc40-121">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="3bc40-121">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="3bc40-122">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="3bc40-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

