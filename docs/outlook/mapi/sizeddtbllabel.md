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
ms.openlocfilehash: c2e275e373677e50510a0aa87f5060070a870a0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812314"
---
# <a name="sizeddtbllabel"></a><span data-ttu-id="a3336-103">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="a3336-103">SizedDtblLabel</span></span>

<span data-ttu-id="a3336-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a3336-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a3336-105">Создает именованный структуру, которая включает в себя структуры [DTBLLABEL](dtbllabel.md) для описания элемента управления label и связанные метки заданной длины.</span><span class="sxs-lookup"><span data-stu-id="a3336-105">Creates a named structure that includes a [DTBLLABEL](dtbllabel.md) structure for describing a label control and the associated label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a3336-106">Указанный в файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a3336-106">Specified in header file:</span></span>  <br/> |<span data-ttu-id="a3336-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a3336-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a3336-108">Связанные структуры</span><span class="sxs-lookup"><span data-stu-id="a3336-108">Related structure</span></span>  <br/> |<span data-ttu-id="a3336-109">**DTBLLABEL**</span><span class="sxs-lookup"><span data-stu-id="a3336-109">**DTBLLABEL**</span></span> <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a><span data-ttu-id="a3336-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3336-110">Parameters</span></span>

<span data-ttu-id="a3336-111">_n_</span><span class="sxs-lookup"><span data-stu-id="a3336-111">_n_</span></span>
  
> <span data-ttu-id="a3336-112">Длина метки.</span><span class="sxs-lookup"><span data-stu-id="a3336-112">Length of the label.</span></span> <span data-ttu-id="a3336-113">Этот компонент включает конечным символом NULL.</span><span class="sxs-lookup"><span data-stu-id="a3336-113">This includes the ending NULL character.</span></span> 
    
<span data-ttu-id="a3336-114">_u_</span><span class="sxs-lookup"><span data-stu-id="a3336-114">_u_</span></span>
  
> <span data-ttu-id="a3336-115">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="a3336-115">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a3336-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="a3336-116">Remarks</span></span>

<span data-ttu-id="a3336-117">Макрос **SizedDtblLabel** позволяет определить метки в таблице отображения при известные число символов в подписи.</span><span class="sxs-lookup"><span data-stu-id="a3336-117">The **SizedDtblLabel** macro lets you define a display table label when the number of characters in the label is known.</span></span> <span data-ttu-id="a3336-118">Новая структура создается с следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="a3336-118">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

<span data-ttu-id="a3336-119">Чтобы использовать указатель в итоговый структуру из макроса **SizedDtblLabel** как указатель на структуру **DTBLLABEL** , выполните следующие приведения:</span><span class="sxs-lookup"><span data-stu-id="a3336-119">To use a pointer to the resulting structure from the **SizedDtblLabel** macro as a **DTBLLABEL** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a><span data-ttu-id="a3336-120">См. также</span><span class="sxs-lookup"><span data-stu-id="a3336-120">See also</span></span>

- [<span data-ttu-id="a3336-121">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="a3336-121">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="a3336-122">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="a3336-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

