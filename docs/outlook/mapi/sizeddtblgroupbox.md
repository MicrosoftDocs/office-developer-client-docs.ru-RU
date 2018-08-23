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
ms.openlocfilehash: 882638d5359154a56fa4438e7a62f213159f916d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581218"
---
# <a name="sizeddtblgroupbox"></a><span data-ttu-id="15962-103">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="15962-103">SizedDtblGroupBox</span></span>

<span data-ttu-id="15962-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15962-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15962-105">Создает именованный структуру, которая включает в себя структуру [DTBLGROUPBOX](dtblgroupbox.md) , содержащие элемент управления поля группы и метка заданной длины.</span><span class="sxs-lookup"><span data-stu-id="15962-105">Creates a named structure that includes a [DTBLGROUPBOX](dtblgroupbox.md) structure for describing a group box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="15962-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="15962-106">Header file:</span></span>  <br/> |<span data-ttu-id="15962-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="15962-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="15962-108">Связанные структуры:</span><span class="sxs-lookup"><span data-stu-id="15962-108">Related structure:</span></span>  <br/> |<span data-ttu-id="15962-109">**DTBLGROUPBOX**</span><span class="sxs-lookup"><span data-stu-id="15962-109">**DTBLGROUPBOX**</span></span> <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="15962-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="15962-110">Parameters</span></span>

<span data-ttu-id="15962-111">_n_</span><span class="sxs-lookup"><span data-stu-id="15962-111">_n_</span></span>
  
> <span data-ttu-id="15962-112">Длина подписи для поля группы.</span><span class="sxs-lookup"><span data-stu-id="15962-112">Length of the group box's label.</span></span> 
    
<span data-ttu-id="15962-113">_u_</span><span class="sxs-lookup"><span data-stu-id="15962-113">_u_</span></span>
  
> <span data-ttu-id="15962-114">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="15962-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="15962-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="15962-115">Remarks</span></span>

<span data-ttu-id="15962-116">Макрос **SizedDtblGroupBox** позволяет определить элемент управления поля группы при известные длина метки.</span><span class="sxs-lookup"><span data-stu-id="15962-116">The **SizedDtblGroupBox** macro lets you define a group box control when the length of the label is known.</span></span> <span data-ttu-id="15962-117">Новая структура создается с следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="15962-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

<span data-ttu-id="15962-118">Чтобы использовать указатель в итоговый структуру из макроса **SizedDtblGroupBox** как указатель на структуру **DTBLGROUPBOX** , выполните следующие приведения:</span><span class="sxs-lookup"><span data-stu-id="15962-118">To use a pointer to the resulting structure from the **SizedDtblGroupBox** macro as a **DTBLGROUPBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a><span data-ttu-id="15962-119">См. также</span><span class="sxs-lookup"><span data-stu-id="15962-119">See also</span></span>

- [<span data-ttu-id="15962-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="15962-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="15962-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="15962-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

