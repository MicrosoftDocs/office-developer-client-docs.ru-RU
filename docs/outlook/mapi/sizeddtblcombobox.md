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
ms.openlocfilehash: fea2b496a34d7aa7f9469158fae14daf6a770608
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812309"
---
# <a name="sizeddtblcombobox"></a><span data-ttu-id="66e15-103">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="66e15-103">SizedDtblComboBox</span></span>
 
<span data-ttu-id="66e15-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="66e15-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="66e15-105">Создает именованные структуру, которая включает в себя структуры [DTBLCOMBOBOX](dtblcombobox.md) для описания поле со списком и максимальное число символов, которые можно ввести в окне связанный редактирования.</span><span class="sxs-lookup"><span data-stu-id="66e15-105">Creates a named structure that includes a [DTBLCOMBOBOX](dtblcombobox.md) structure for describing a combo box control and the maximum number of characters that can be entered in the associated edit control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="66e15-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="66e15-106">Header file:</span></span>  <br/> |<span data-ttu-id="66e15-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="66e15-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="66e15-108">Связанные структуры:</span><span class="sxs-lookup"><span data-stu-id="66e15-108">Related structure:</span></span>  <br/> |<span data-ttu-id="66e15-109">**DTBLCOMBOBOX**</span><span class="sxs-lookup"><span data-stu-id="66e15-109">**DTBLCOMBOBOX**</span></span> <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="66e15-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="66e15-110">Parameters</span></span>

<span data-ttu-id="66e15-111">_n_</span><span class="sxs-lookup"><span data-stu-id="66e15-111">_n_</span></span>
  
> <span data-ttu-id="66e15-112">Число знаков, которое можно ввести в поле со списком редактирование элемента управления.</span><span class="sxs-lookup"><span data-stu-id="66e15-112">Number of characters that can be entered in the combo box's edit control.</span></span> 
    
<span data-ttu-id="66e15-113">_u_</span><span class="sxs-lookup"><span data-stu-id="66e15-113">_u_</span></span>
  
> <span data-ttu-id="66e15-114">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="66e15-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="66e15-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="66e15-115">Remarks</span></span>

<span data-ttu-id="66e15-116">Макрос **SizedDtblComboBox** позволяет определить поле со списком при известные длина строки включено символов.</span><span class="sxs-lookup"><span data-stu-id="66e15-116">The **SizedDtblComboBox** macro lets you define a combo box when the length of the enabled character string is known.</span></span> <span data-ttu-id="66e15-117">Новая структура создается с следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="66e15-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="66e15-118">Чтобы использовать указатель в итоговый структуру из макроса **SizedDtblComboBox** как указатель на структуру **DTBLCOMBOBOX** , выполните следующие приведения:</span><span class="sxs-lookup"><span data-stu-id="66e15-118">To use a pointer to the resulting structure from the **SizedDtblComboBox** macro as a **DTBLCOMBOBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a><span data-ttu-id="66e15-119">См. также</span><span class="sxs-lookup"><span data-stu-id="66e15-119">See also</span></span>

- [<span data-ttu-id="66e15-120">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="66e15-120">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="66e15-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="66e15-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

