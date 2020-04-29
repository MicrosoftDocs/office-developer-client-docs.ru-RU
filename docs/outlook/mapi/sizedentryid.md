---
title: SizedENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedENTRYID
api_type:
- COM
ms.assetid: 491170af-db35-4d7e-a912-44ffe8c7506b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 88cf91330dea82dda490b81cc8de6fea0504baf7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405711"
---
# <a name="sizedentryid"></a><span data-ttu-id="51199-103">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="51199-103">SizedENTRYID</span></span>

<span data-ttu-id="51199-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51199-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51199-105">Создает именованную структуру [EntryID](entryid.md) , содержащую элемент **AB** указанного размера.</span><span class="sxs-lookup"><span data-stu-id="51199-105">Creates a named [ENTRYID](entryid.md) structure that contains an **ab** member of a specified size.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="51199-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="51199-106">Header file:</span></span>  <br/> |<span data-ttu-id="51199-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="51199-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="51199-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="51199-108">Related structure:</span></span>  <br/> |<span data-ttu-id="51199-109">**ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="51199-109">**ENTRYID**</span></span> <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a><span data-ttu-id="51199-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="51199-110">Parameters</span></span>

<span data-ttu-id="51199-111">__CB_</span><span class="sxs-lookup"><span data-stu-id="51199-111">__cb_</span></span>
  
> <span data-ttu-id="51199-112">Количество байтов в элементе **AB** новой структуры.</span><span class="sxs-lookup"><span data-stu-id="51199-112">Count of bytes in the **ab** member of the new structure.</span></span> 
    
<span data-ttu-id="51199-113">__имя_</span><span class="sxs-lookup"><span data-stu-id="51199-113">__name_</span></span>
  
> <span data-ttu-id="51199-114">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="51199-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="51199-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="51199-115">Remarks</span></span>

<span data-ttu-id="51199-116">Макрос **сизедентрид** позволяет определить идентификатор записи после того, как будут известны требования к длине массива.</span><span class="sxs-lookup"><span data-stu-id="51199-116">The **SizedENTRYID** macro lets you define an entry identifier after array length requirements are known.</span></span> <span data-ttu-id="51199-117">Используйте этот макрос для создания идентификатора записи с явно заданными границами.</span><span class="sxs-lookup"><span data-stu-id="51199-117">Use this macro to create an entry identifier with explicit bounds.</span></span> 
  
<span data-ttu-id="51199-118">Чтобы использовать новую структуру, полученную из макроса **сизедентрид** в качестве указателя на структуру **EntryID** , выполните приведенные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="51199-118">To use the new structure that results from the **SizedENTRYID** macro as a pointer to an **ENTRYID** structure, perform the following cast:</span></span> 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a><span data-ttu-id="51199-119">См. также</span><span class="sxs-lookup"><span data-stu-id="51199-119">See also</span></span>

- [<span data-ttu-id="51199-120">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="51199-120">ENTRYID</span></span>](entryid.md)
- [<span data-ttu-id="51199-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="51199-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

