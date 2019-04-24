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
ms.openlocfilehash: b5b9c42d944ad9d3ce92e99d08d29964944c8028
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282805"
---
# <a name="sizeddtbledit"></a><span data-ttu-id="9ba5b-103">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="9ba5b-103">SizedDtblEdit</span></span>

<span data-ttu-id="9ba5b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ba5b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ba5b-105">Создает именованную структуру, включающую структуру [дтбледит](dtbledit.md) для описания элемента управления Editing и максимальное количество символов, которое можно ввести в элемент управления.</span><span class="sxs-lookup"><span data-stu-id="9ba5b-105">Creates a named structure that includes a [DTBLEDIT](dtbledit.md) structure for describing an edit control and the maximum number of characters that can be entered in the control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9ba5b-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9ba5b-106">Header file:</span></span>  <br/> |<span data-ttu-id="9ba5b-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="9ba5b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9ba5b-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="9ba5b-108">Related structure:</span></span>  <br/> |<span data-ttu-id="9ba5b-109">**DTBLEDIT**</span><span class="sxs-lookup"><span data-stu-id="9ba5b-109">**DTBLEDIT**</span></span> <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a><span data-ttu-id="9ba5b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ba5b-110">Parameters</span></span>

<span data-ttu-id="9ba5b-111">_n_</span><span class="sxs-lookup"><span data-stu-id="9ba5b-111">_n_</span></span>
  
> <span data-ttu-id="9ba5b-112">Максимальное количество символов, которое можно ввести в поле редактирования.</span><span class="sxs-lookup"><span data-stu-id="9ba5b-112">Maximum number of characters that can be entered in the edit control.</span></span>
    
<span data-ttu-id="9ba5b-113">_u_</span><span class="sxs-lookup"><span data-stu-id="9ba5b-113">_u_</span></span>
  
> <span data-ttu-id="9ba5b-114">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="9ba5b-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9ba5b-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="9ba5b-115">Remarks</span></span>

<span data-ttu-id="9ba5b-116">Макрос **сизеддтбледит** позволяет определить элемент управления редактированием, если известно количество включенных символов.</span><span class="sxs-lookup"><span data-stu-id="9ba5b-116">The **SizedDtblEdit** macro lets you define an edit control when the number of enabled characters is known.</span></span> <span data-ttu-id="9ba5b-117">Новая структура создается со следующими элементами:</span><span class="sxs-lookup"><span data-stu-id="9ba5b-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="9ba5b-118">Чтобы использовать указатель на полученную структуру из макроса **сизеддтбледит** в качестве указателя структуры **дтбледит** , выполните следующую операцию приведения:</span><span class="sxs-lookup"><span data-stu-id="9ba5b-118">To use a pointer to the resulting structure from the **SizedDtblEdit** macro as a **DTBLEDIT** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a><span data-ttu-id="9ba5b-119">См. также</span><span class="sxs-lookup"><span data-stu-id="9ba5b-119">See also</span></span>

- [<span data-ttu-id="9ba5b-120">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="9ba5b-120">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="9ba5b-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="9ba5b-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

