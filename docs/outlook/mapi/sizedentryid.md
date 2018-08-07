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
ms.openlocfilehash: 814cfeab61854469f460cc38f927b0e3723f6f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812303"
---
# <a name="sizedentryid"></a><span data-ttu-id="32fcd-103">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="32fcd-103">SizedENTRYID</span></span>

<span data-ttu-id="32fcd-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="32fcd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="32fcd-105">Создает структуру [ENTRYID](entryid.md) именованные, содержащего члены **ab** указанного размера.</span><span class="sxs-lookup"><span data-stu-id="32fcd-105">Creates a named [ENTRYID](entryid.md) structure that contains an **ab** member of a specified size.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="32fcd-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="32fcd-106">Header file:</span></span>  <br/> |<span data-ttu-id="32fcd-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="32fcd-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="32fcd-108">Связанные структуры:</span><span class="sxs-lookup"><span data-stu-id="32fcd-108">Related structure:</span></span>  <br/> |<span data-ttu-id="32fcd-109">**ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="32fcd-109">**ENTRYID**</span></span> <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a><span data-ttu-id="32fcd-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="32fcd-110">Parameters</span></span>

<span data-ttu-id="32fcd-111">__Сертификация_</span><span class="sxs-lookup"><span data-stu-id="32fcd-111">__cb_</span></span>
  
> <span data-ttu-id="32fcd-112">Число байт в член **ab** новой структуры.</span><span class="sxs-lookup"><span data-stu-id="32fcd-112">Count of bytes in the **ab** member of the new structure.</span></span> 
    
<span data-ttu-id="32fcd-113">_имя_</span><span class="sxs-lookup"><span data-stu-id="32fcd-113">__name_</span></span>
  
> <span data-ttu-id="32fcd-114">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="32fcd-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="32fcd-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="32fcd-115">Remarks</span></span>

<span data-ttu-id="32fcd-116">Макрос **SizedENTRYID** позволяет определить идентификатор записи после известные требования к длине массива.</span><span class="sxs-lookup"><span data-stu-id="32fcd-116">The **SizedENTRYID** macro lets you define an entry identifier after array length requirements are known.</span></span> <span data-ttu-id="32fcd-117">Используйте этот макрос для создания идентификатора запись с явные границы.</span><span class="sxs-lookup"><span data-stu-id="32fcd-117">Use this macro to create an entry identifier with explicit bounds.</span></span> 
  
<span data-ttu-id="32fcd-118">Для применения новой структуры, результаты из макроса **SizedENTRYID** как указатель на структуру **ENTRYID** , выполните следующие приведения.</span><span class="sxs-lookup"><span data-stu-id="32fcd-118">To use the new structure that results from the **SizedENTRYID** macro as a pointer to an **ENTRYID** structure, perform the following cast:</span></span> 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a><span data-ttu-id="32fcd-119">См. также</span><span class="sxs-lookup"><span data-stu-id="32fcd-119">See also</span></span>

- [<span data-ttu-id="32fcd-120">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="32fcd-120">ENTRYID</span></span>](entryid.md)
- [<span data-ttu-id="32fcd-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="32fcd-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

