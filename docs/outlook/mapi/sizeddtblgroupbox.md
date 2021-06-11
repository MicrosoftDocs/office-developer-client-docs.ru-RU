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
# <a name="sizeddtblgroupbox"></a><span data-ttu-id="1a1fd-103">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="1a1fd-103">SizedDtblGroupBox</span></span>

<span data-ttu-id="1a1fd-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a1fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a1fd-105">Создает именованную структуру, которая включает структуру [DTBLGROUPBOX](dtblgroupbox.md) для описания управления групповым полем и метки определенной длины.</span><span class="sxs-lookup"><span data-stu-id="1a1fd-105">Creates a named structure that includes a [DTBLGROUPBOX](dtblgroupbox.md) structure for describing a group box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1a1fd-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="1a1fd-106">Header file:</span></span>  <br/> |<span data-ttu-id="1a1fd-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1a1fd-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="1a1fd-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="1a1fd-108">Related structure:</span></span>  <br/> |<span data-ttu-id="1a1fd-109">**DTBLGROUPBOX**</span><span class="sxs-lookup"><span data-stu-id="1a1fd-109">**DTBLGROUPBOX**</span></span> <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="1a1fd-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="1a1fd-110">Parameters</span></span>

<span data-ttu-id="1a1fd-111">_n_</span><span class="sxs-lookup"><span data-stu-id="1a1fd-111">_n_</span></span>
  
> <span data-ttu-id="1a1fd-112">Длина метки группового окна.</span><span class="sxs-lookup"><span data-stu-id="1a1fd-112">Length of the group box's label.</span></span> 
    
<span data-ttu-id="1a1fd-113">_u_</span><span class="sxs-lookup"><span data-stu-id="1a1fd-113">_u_</span></span>
  
> <span data-ttu-id="1a1fd-114">Имя новой структуры.</span><span class="sxs-lookup"><span data-stu-id="1a1fd-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1a1fd-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="1a1fd-115">Remarks</span></span>

<span data-ttu-id="1a1fd-116">Макрос **SizedDtblGroupBox позволяет** определить управление групповым полем, если известна длина метки.</span><span class="sxs-lookup"><span data-stu-id="1a1fd-116">The **SizedDtblGroupBox** macro lets you define a group box control when the length of the label is known.</span></span> <span data-ttu-id="1a1fd-117">Новая структура создается со следующими участниками:</span><span class="sxs-lookup"><span data-stu-id="1a1fd-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

<span data-ttu-id="1a1fd-118">Чтобы использовать указатель на результатовую структуру макроса **SizedDtblGroupBox** в качестве указателя **структуры DTBLGROUPBOX,** выполните следующий бросок:</span><span class="sxs-lookup"><span data-stu-id="1a1fd-118">To use a pointer to the resulting structure from the **SizedDtblGroupBox** macro as a **DTBLGROUPBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a><span data-ttu-id="1a1fd-119">См. также</span><span class="sxs-lookup"><span data-stu-id="1a1fd-119">See also</span></span>

- [<span data-ttu-id="1a1fd-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="1a1fd-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="1a1fd-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="1a1fd-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

