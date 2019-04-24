---
title: CbNewMTSID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CbNewMTSID
api_type:
- COM
ms.assetid: fd5ef226-39e6-4604-a751-2f6cc49c4895
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8ffff7958ab405e488ac2ce45bae43b78da7b0f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331600"
---
# <a name="cbnewmtsid"></a><span data-ttu-id="b170c-103">CbNewMTSID</span><span class="sxs-lookup"><span data-stu-id="b170c-103">CbNewMTSID</span></span>

  
  
<span data-ttu-id="b170c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b170c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b170c-105">Вычисляет количество байтов, которое следует выделить для новой структуры [мтсид](mtsid.md) с идентификатором агента передачи сообщений указанного размера.</span><span class="sxs-lookup"><span data-stu-id="b170c-105">Computes the number of bytes that should be allocated for a new [MTSID](mtsid.md) structure with a message transfer agent identifier of a specified size.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b170c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b170c-106">Header file:</span></span>  <br/> |<span data-ttu-id="b170c-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="b170c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b170c-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="b170c-108">Related structure:</span></span>  <br/> |<span data-ttu-id="b170c-109">**MTSID**</span><span class="sxs-lookup"><span data-stu-id="b170c-109">**MTSID**</span></span> <br/> |
   
```cpp
CbNewMTSID (_cb)
```

## <a name="parameters"></a><span data-ttu-id="b170c-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b170c-110">Parameters</span></span>

 <span data-ttu-id="b170c-111">__CB_</span><span class="sxs-lookup"><span data-stu-id="b170c-111">__cb_</span></span>
  
> <span data-ttu-id="b170c-112">Число байтов для идентификатора агента передачи сообщений, включаемого в новую структуру **мтсид** .</span><span class="sxs-lookup"><span data-stu-id="b170c-112">Count of bytes for the message transfer agent identifier to be included in the new **MTSID** structure.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="b170c-113">См. также</span><span class="sxs-lookup"><span data-stu-id="b170c-113">See also</span></span>



[<span data-ttu-id="b170c-114">MTSID</span><span class="sxs-lookup"><span data-stu-id="b170c-114">MTSID</span></span>](mtsid.md)


[<span data-ttu-id="b170c-115">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="b170c-115">Macros Related to Structures</span></span>](macros-related-to-structures.md)

