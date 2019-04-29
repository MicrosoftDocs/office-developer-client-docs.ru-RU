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
ms.openlocfilehash: 8861c8f86eaab6defb270b673e0ee200446aedb3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416267"
---
# <a name="sizeddtblcombobox"></a><span data-ttu-id="12dd3-103">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="12dd3-103">SizedDtblComboBox</span></span>
 
<span data-ttu-id="12dd3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12dd3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12dd3-105">Создает именованную структуру, включающую структуру [дтблкомбобокс](dtblcombobox.md) для описания элемента управления "поле со списком" и максимальное количество символов, которое можно ввести в связанный элемент управления редактирования.</span><span class="sxs-lookup"><span data-stu-id="12dd3-105">Creates a named structure that includes a [DTBLCOMBOBOX](dtblcombobox.md) structure for describing a combo box control and the maximum number of characters that can be entered in the associated edit control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="12dd3-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="12dd3-106">Header file:</span></span>  <br/> |<span data-ttu-id="12dd3-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="12dd3-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="12dd3-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="12dd3-108">Related structure:</span></span>  <br/> |<span data-ttu-id="12dd3-109">**DTBLCOMBOBOX**</span><span class="sxs-lookup"><span data-stu-id="12dd3-109">**DTBLCOMBOBOX**</span></span> <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="12dd3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="12dd3-110">Parameters</span></span>

<span data-ttu-id="12dd3-111">_n_</span><span class="sxs-lookup"><span data-stu-id="12dd3-111">_n_</span></span>
  
> <span data-ttu-id="12dd3-112">Число символов, которое можно ввести в поле ввода поля со списком.</span><span class="sxs-lookup"><span data-stu-id="12dd3-112">Number of characters that can be entered in the combo box's edit control.</span></span> 
    
<span data-ttu-id="12dd3-113">_u_</span><span class="sxs-lookup"><span data-stu-id="12dd3-113">_u_</span></span>
  
> <span data-ttu-id="12dd3-114">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="12dd3-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="12dd3-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="12dd3-115">Remarks</span></span>

<span data-ttu-id="12dd3-116">С помощью макроса **сизеддтблкомбобокс** можно определить поле со списком, если известна длина строки разрешенных символов.</span><span class="sxs-lookup"><span data-stu-id="12dd3-116">The **SizedDtblComboBox** macro lets you define a combo box when the length of the enabled character string is known.</span></span> <span data-ttu-id="12dd3-117">Новая структура создается со следующими элементами:</span><span class="sxs-lookup"><span data-stu-id="12dd3-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="12dd3-118">Чтобы использовать указатель на полученную структуру из макроса **сизеддтблкомбобокс** в качестве указателя структуры **дтблкомбобокс** , выполните следующую операцию приведения:</span><span class="sxs-lookup"><span data-stu-id="12dd3-118">To use a pointer to the resulting structure from the **SizedDtblComboBox** macro as a **DTBLCOMBOBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a><span data-ttu-id="12dd3-119">См. также</span><span class="sxs-lookup"><span data-stu-id="12dd3-119">See also</span></span>

- [<span data-ttu-id="12dd3-120">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="12dd3-120">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="12dd3-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="12dd3-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

