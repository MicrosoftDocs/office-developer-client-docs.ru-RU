---
title: SizedDtblComboBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblComboBox
api_type:
- COM
ms.assetid: 1e5ea9f2-1029-4584-845a-890d3e956036
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 39854c320078d2e2ca2365244f094e28962380d0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593657"
---
# <a name="sizeddtblcombobox"></a><span data-ttu-id="911c4-103">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="911c4-103">SizedDtblComboBox</span></span>
 
<span data-ttu-id="911c4-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="911c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="911c4-105">Создает именованные структуру, которая включает в себя структуры [DTBLCOMBOBOX](dtblcombobox.md) для описания поле со списком и максимальное число символов, которые можно ввести в окне связанный редактирования.</span><span class="sxs-lookup"><span data-stu-id="911c4-105">Creates a named structure that includes a [DTBLCOMBOBOX](dtblcombobox.md) structure for describing a combo box control and the maximum number of characters that can be entered in the associated edit control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="911c4-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="911c4-106">Header file:</span></span>  <br/> |<span data-ttu-id="911c4-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="911c4-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="911c4-108">Связанные структуры:</span><span class="sxs-lookup"><span data-stu-id="911c4-108">Related structure:</span></span>  <br/> |<span data-ttu-id="911c4-109">**DTBLCOMBOBOX**</span><span class="sxs-lookup"><span data-stu-id="911c4-109">**DTBLCOMBOBOX**</span></span> <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="911c4-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="911c4-110">Parameters</span></span>

<span data-ttu-id="911c4-111">_n_</span><span class="sxs-lookup"><span data-stu-id="911c4-111">_n_</span></span>
  
> <span data-ttu-id="911c4-112">Число знаков, которое можно ввести в поле со списком редактирование элемента управления.</span><span class="sxs-lookup"><span data-stu-id="911c4-112">Number of characters that can be entered in the combo box's edit control.</span></span> 
    
<span data-ttu-id="911c4-113">_u_</span><span class="sxs-lookup"><span data-stu-id="911c4-113">_u_</span></span>
  
> <span data-ttu-id="911c4-114">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="911c4-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="911c4-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="911c4-115">Remarks</span></span>

<span data-ttu-id="911c4-116">Макрос **SizedDtblComboBox** позволяет определить поле со списком при известные длина строки включено символов.</span><span class="sxs-lookup"><span data-stu-id="911c4-116">The **SizedDtblComboBox** macro lets you define a combo box when the length of the enabled character string is known.</span></span> <span data-ttu-id="911c4-117">Новая структура создается с следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="911c4-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="911c4-118">Чтобы использовать указатель в итоговый структуру из макроса **SizedDtblComboBox** как указатель на структуру **DTBLCOMBOBOX** , выполните следующие приведения:</span><span class="sxs-lookup"><span data-stu-id="911c4-118">To use a pointer to the resulting structure from the **SizedDtblComboBox** macro as a **DTBLCOMBOBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a><span data-ttu-id="911c4-119">См. также</span><span class="sxs-lookup"><span data-stu-id="911c4-119">See also</span></span>

- [<span data-ttu-id="911c4-120">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="911c4-120">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="911c4-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="911c4-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

