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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282707"
---
# <a name="sizeddtbllabel"></a><span data-ttu-id="9ff66-103">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="9ff66-103">SizedDtblLabel</span></span>

<span data-ttu-id="9ff66-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ff66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ff66-105">Создает именованную структуру, которая включает структуру [дтбллабел](dtbllabel.md) для описания элемента управления Label и связанную метку заданной длины.</span><span class="sxs-lookup"><span data-stu-id="9ff66-105">Creates a named structure that includes a [DTBLLABEL](dtbllabel.md) structure for describing a label control and the associated label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9ff66-106">Указано в файле заголовка:</span><span class="sxs-lookup"><span data-stu-id="9ff66-106">Specified in header file:</span></span>  <br/> |<span data-ttu-id="9ff66-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="9ff66-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9ff66-108">Связанная структура</span><span class="sxs-lookup"><span data-stu-id="9ff66-108">Related structure</span></span>  <br/> |<span data-ttu-id="9ff66-109">**DTBLLABEL**</span><span class="sxs-lookup"><span data-stu-id="9ff66-109">**DTBLLABEL**</span></span> <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a><span data-ttu-id="9ff66-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ff66-110">Parameters</span></span>

<span data-ttu-id="9ff66-111">_n_</span><span class="sxs-lookup"><span data-stu-id="9ff66-111">_n_</span></span>
  
> <span data-ttu-id="9ff66-112">Длина метки.</span><span class="sxs-lookup"><span data-stu-id="9ff66-112">Length of the label.</span></span> <span data-ttu-id="9ff66-113">Сюда входит конечный символ NULL.</span><span class="sxs-lookup"><span data-stu-id="9ff66-113">This includes the ending NULL character.</span></span> 
    
<span data-ttu-id="9ff66-114">_u_</span><span class="sxs-lookup"><span data-stu-id="9ff66-114">_u_</span></span>
  
> <span data-ttu-id="9ff66-115">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="9ff66-115">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9ff66-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="9ff66-116">Remarks</span></span>

<span data-ttu-id="9ff66-117">Макрос **сизеддтбллабел** позволяет определить метку отображаемой таблицы, когда число символов в метке известно.</span><span class="sxs-lookup"><span data-stu-id="9ff66-117">The **SizedDtblLabel** macro lets you define a display table label when the number of characters in the label is known.</span></span> <span data-ttu-id="9ff66-118">Новая структура создается со следующими элементами:</span><span class="sxs-lookup"><span data-stu-id="9ff66-118">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

<span data-ttu-id="9ff66-119">Чтобы использовать указатель на полученную структуру из макроса **сизеддтбллабел** в качестве указателя структуры **дтбллабел** , выполните следующую операцию приведения:</span><span class="sxs-lookup"><span data-stu-id="9ff66-119">To use a pointer to the resulting structure from the **SizedDtblLabel** macro as a **DTBLLABEL** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a><span data-ttu-id="9ff66-120">См. также</span><span class="sxs-lookup"><span data-stu-id="9ff66-120">See also</span></span>

- [<span data-ttu-id="9ff66-121">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="9ff66-121">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="9ff66-122">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="9ff66-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

