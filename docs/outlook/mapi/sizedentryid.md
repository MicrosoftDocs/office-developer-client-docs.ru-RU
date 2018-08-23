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
ms.openlocfilehash: d797acdbf2abfb88151d69d0c93e743f07afc5c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563872"
---
# <a name="sizedentryid"></a><span data-ttu-id="f9b05-103">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="f9b05-103">SizedENTRYID</span></span>

<span data-ttu-id="f9b05-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9b05-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9b05-105">Создает структуру [ENTRYID](entryid.md) именованные, содержащего члены **ab** указанного размера.</span><span class="sxs-lookup"><span data-stu-id="f9b05-105">Creates a named [ENTRYID](entryid.md) structure that contains an **ab** member of a specified size.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f9b05-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f9b05-106">Header file:</span></span>  <br/> |<span data-ttu-id="f9b05-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f9b05-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f9b05-108">Связанные структуры:</span><span class="sxs-lookup"><span data-stu-id="f9b05-108">Related structure:</span></span>  <br/> |<span data-ttu-id="f9b05-109">**ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="f9b05-109">**ENTRYID**</span></span> <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a><span data-ttu-id="f9b05-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f9b05-110">Parameters</span></span>

<span data-ttu-id="f9b05-111">__Сертификация_</span><span class="sxs-lookup"><span data-stu-id="f9b05-111">__cb_</span></span>
  
> <span data-ttu-id="f9b05-112">Число байт в член **ab** новой структуры.</span><span class="sxs-lookup"><span data-stu-id="f9b05-112">Count of bytes in the **ab** member of the new structure.</span></span> 
    
<span data-ttu-id="f9b05-113">_имя_</span><span class="sxs-lookup"><span data-stu-id="f9b05-113">__name_</span></span>
  
> <span data-ttu-id="f9b05-114">Имя для новой структуры.</span><span class="sxs-lookup"><span data-stu-id="f9b05-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f9b05-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="f9b05-115">Remarks</span></span>

<span data-ttu-id="f9b05-116">Макрос **SizedENTRYID** позволяет определить идентификатор записи после известные требования к длине массива.</span><span class="sxs-lookup"><span data-stu-id="f9b05-116">The **SizedENTRYID** macro lets you define an entry identifier after array length requirements are known.</span></span> <span data-ttu-id="f9b05-117">Используйте этот макрос для создания идентификатора запись с явные границы.</span><span class="sxs-lookup"><span data-stu-id="f9b05-117">Use this macro to create an entry identifier with explicit bounds.</span></span> 
  
<span data-ttu-id="f9b05-118">Для применения новой структуры, результаты из макроса **SizedENTRYID** как указатель на структуру **ENTRYID** , выполните следующие приведения.</span><span class="sxs-lookup"><span data-stu-id="f9b05-118">To use the new structure that results from the **SizedENTRYID** macro as a pointer to an **ENTRYID** structure, perform the following cast:</span></span> 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a><span data-ttu-id="f9b05-119">См. также</span><span class="sxs-lookup"><span data-stu-id="f9b05-119">See also</span></span>

- [<span data-ttu-id="f9b05-120">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f9b05-120">ENTRYID</span></span>](entryid.md)
- [<span data-ttu-id="f9b05-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="f9b05-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

