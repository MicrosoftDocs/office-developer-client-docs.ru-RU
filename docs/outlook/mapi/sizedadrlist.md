---
title: SizedADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedADRLIST
api_type:
- COM
ms.assetid: 5c64d74a-83a7-4122-b1d1-fcca0f4a6cdb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c35a1eb54b29c04bc8eed453272b59aae0ea737e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423463"
---
# <a name="sizedadrlist"></a><span data-ttu-id="06c09-103">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="06c09-103">SizedADRLIST</span></span>

<span data-ttu-id="06c09-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06c09-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06c09-105">Определяет структуру [ADRLIST](adrlist.md) с указанным именем, которое содержит указанное число структур [ADRENTRY.](adrentry.md)</span><span class="sxs-lookup"><span data-stu-id="06c09-105">Defines an [ADRLIST](adrlist.md) structure with the specified name that contains a specified number of [ADRENTRY](adrentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="06c09-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="06c09-106">Header file:</span></span>  <br/> |<span data-ttu-id="06c09-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="06c09-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="06c09-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="06c09-108">Related structure:</span></span>  <br/> |<span data-ttu-id="06c09-109">**ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="06c09-109">**ADRLIST**</span></span> <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a><span data-ttu-id="06c09-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="06c09-110">Parameters</span></span>

<span data-ttu-id="06c09-111">_ _centries_</span><span class="sxs-lookup"><span data-stu-id="06c09-111">_ _centries_</span></span>
  
> <span data-ttu-id="06c09-112">Количество структур **ADRENTRY,** которые необходимо включить в новую структуру **ADRLIST.**</span><span class="sxs-lookup"><span data-stu-id="06c09-112">Count of **ADRENTRY** structures to be included in the new **ADRLIST** structure.</span></span> 
    
<span data-ttu-id="06c09-113">_ _name_</span><span class="sxs-lookup"><span data-stu-id="06c09-113">_ _name_</span></span>
  
> <span data-ttu-id="06c09-114">Имя новой структуры **ADRLIST.**</span><span class="sxs-lookup"><span data-stu-id="06c09-114">Name for the new **ADRLIST** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="06c09-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="06c09-115">Remarks</span></span>

<span data-ttu-id="06c09-116">Макрос **SizedADRLIST** позволяет определить список получателей, который имеет явные границы, когда известны требования к длине массива.</span><span class="sxs-lookup"><span data-stu-id="06c09-116">The **SizedADRLIST** macro lets you define a recipient list that has explicit bounds when array length requirements are known.</span></span> <span data-ttu-id="06c09-117">В следующем коде показано, как привести результат макроса **SizedADRLIST** к указателю структуры **ADRLIST:**</span><span class="sxs-lookup"><span data-stu-id="06c09-117">The following code shows how to cast the result of the **SizedADRLIST** macro to an **ADRLIST** structure pointer:</span></span> 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a><span data-ttu-id="06c09-118">См. также</span><span class="sxs-lookup"><span data-stu-id="06c09-118">See also</span></span>

- [<span data-ttu-id="06c09-119">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="06c09-119">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="06c09-120">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="06c09-120">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="06c09-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="06c09-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

