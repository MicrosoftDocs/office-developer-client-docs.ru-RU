---
title: SizedDtblGroupBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblGroupBox
api_type:
- COM
ms.assetid: 7ca01bf7-5185-41cc-907e-01f256345997
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0a9bda8831f4a38b62d71a54115c40bb3374d97d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419319"
---
# <a name="sizeddtblgroupbox"></a><span data-ttu-id="975e1-103">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="975e1-103">SizedDtblGroupBox</span></span>

<span data-ttu-id="975e1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="975e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="975e1-105">Создает именованную структуру, которая включает структуру [дтблграупбокс](dtblgroupbox.md) для описания элемента управления "Группа" и метку указанной длины.</span><span class="sxs-lookup"><span data-stu-id="975e1-105">Creates a named structure that includes a [DTBLGROUPBOX](dtblgroupbox.md) structure for describing a group box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="975e1-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="975e1-106">Header file:</span></span>  <br/> |<span data-ttu-id="975e1-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="975e1-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="975e1-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="975e1-108">Related structure:</span></span>  <br/> |<span data-ttu-id="975e1-109">**DTBLGROUPBOX**</span><span class="sxs-lookup"><span data-stu-id="975e1-109">**DTBLGROUPBOX**</span></span> <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="975e1-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="975e1-110">Parameters</span></span>

<span data-ttu-id="975e1-111">_n_</span><span class="sxs-lookup"><span data-stu-id="975e1-111">_n_</span></span>
  
> <span data-ttu-id="975e1-112">Длина метки поля группы.</span><span class="sxs-lookup"><span data-stu-id="975e1-112">Length of the group box's label.</span></span> 
    
<span data-ttu-id="975e1-113">_u_</span><span class="sxs-lookup"><span data-stu-id="975e1-113">_u_</span></span>
  
> <span data-ttu-id="975e1-114">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="975e1-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="975e1-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="975e1-115">Remarks</span></span>

<span data-ttu-id="975e1-116">Макрос **сизеддтблграупбокс** позволяет определить элемент управления поля группы, если длина метки известна.</span><span class="sxs-lookup"><span data-stu-id="975e1-116">The **SizedDtblGroupBox** macro lets you define a group box control when the length of the label is known.</span></span> <span data-ttu-id="975e1-117">Новая структура создается со следующими элементами:</span><span class="sxs-lookup"><span data-stu-id="975e1-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

<span data-ttu-id="975e1-118">Чтобы использовать указатель на полученную структуру из макроса **сизеддтблграупбокс** в качестве указателя структуры **дтблграупбокс** , выполните следующую операцию приведения:</span><span class="sxs-lookup"><span data-stu-id="975e1-118">To use a pointer to the resulting structure from the **SizedDtblGroupBox** macro as a **DTBLGROUPBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a><span data-ttu-id="975e1-119">См. также</span><span class="sxs-lookup"><span data-stu-id="975e1-119">See also</span></span>

- [<span data-ttu-id="975e1-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="975e1-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="975e1-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="975e1-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

