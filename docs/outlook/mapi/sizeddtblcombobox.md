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
# <a name="sizeddtblcombobox"></a><span data-ttu-id="97ffa-103">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="97ffa-103">SizedDtblComboBox</span></span>
 
<span data-ttu-id="97ffa-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97ffa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97ffa-105">Создает именованную структуру, которая включает структуру [DTBLCOMBOBOX](dtblcombobox.md) для описания управления коробкой комбо и максимального количества символов, которые можно вписать в связанное управление редактированием.</span><span class="sxs-lookup"><span data-stu-id="97ffa-105">Creates a named structure that includes a [DTBLCOMBOBOX](dtblcombobox.md) structure for describing a combo box control and the maximum number of characters that can be entered in the associated edit control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="97ffa-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="97ffa-106">Header file:</span></span>  <br/> |<span data-ttu-id="97ffa-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="97ffa-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="97ffa-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="97ffa-108">Related structure:</span></span>  <br/> |<span data-ttu-id="97ffa-109">**DTBLCOMBOBOX**</span><span class="sxs-lookup"><span data-stu-id="97ffa-109">**DTBLCOMBOBOX**</span></span> <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="97ffa-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="97ffa-110">Parameters</span></span>

<span data-ttu-id="97ffa-111">_n_</span><span class="sxs-lookup"><span data-stu-id="97ffa-111">_n_</span></span>
  
> <span data-ttu-id="97ffa-112">Количество символов, которые можно вписать в управление редактированием в комбо-окне.</span><span class="sxs-lookup"><span data-stu-id="97ffa-112">Number of characters that can be entered in the combo box's edit control.</span></span> 
    
<span data-ttu-id="97ffa-113">_u_</span><span class="sxs-lookup"><span data-stu-id="97ffa-113">_u_</span></span>
  
> <span data-ttu-id="97ffa-114">Имя новой структуры.</span><span class="sxs-lookup"><span data-stu-id="97ffa-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="97ffa-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="97ffa-115">Remarks</span></span>

<span data-ttu-id="97ffa-116">Макрос **SizedDtblComboBox позволяет** определить поле комбо, когда известна длина включенной строки символов.</span><span class="sxs-lookup"><span data-stu-id="97ffa-116">The **SizedDtblComboBox** macro lets you define a combo box when the length of the enabled character string is known.</span></span> <span data-ttu-id="97ffa-117">Новая структура создается со следующими участниками:</span><span class="sxs-lookup"><span data-stu-id="97ffa-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="97ffa-118">Чтобы использовать указатель на результатовую структуру **макроса SizedDtblComboBox** в качестве указателя структуры **DTBLCOMBOBOX,** выполните следующий бросок:</span><span class="sxs-lookup"><span data-stu-id="97ffa-118">To use a pointer to the resulting structure from the **SizedDtblComboBox** macro as a **DTBLCOMBOBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a><span data-ttu-id="97ffa-119">См. также</span><span class="sxs-lookup"><span data-stu-id="97ffa-119">See also</span></span>

- [<span data-ttu-id="97ffa-120">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="97ffa-120">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="97ffa-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="97ffa-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

