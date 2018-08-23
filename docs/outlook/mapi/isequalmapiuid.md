---
title: IsEqualMAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IsEqualMAPIUID
api_type:
- COM
ms.assetid: 85d71b73-0630-4c5d-b0e3-b48d27a300d0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0c72164cac8a37d0372ac93f4ed6d3face966ddb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566665"
---
# <a name="isequalmapiuid"></a><span data-ttu-id="58e64-103">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="58e64-103">IsEqualMAPIUID</span></span>

  
  
<span data-ttu-id="58e64-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58e64-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58e64-105">Проверяет две структуры [MAPIUID](mapiuid.md) определяет, содержат ли они тот же идентификатор.</span><span class="sxs-lookup"><span data-stu-id="58e64-105">Tests two [MAPIUID](mapiuid.md) structures to determine whether they contain the same identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="58e64-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="58e64-106">Header file:</span></span>  <br/> |<span data-ttu-id="58e64-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="58e64-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="58e64-108">Связанные структуры:</span><span class="sxs-lookup"><span data-stu-id="58e64-108">Related structure:</span></span>  <br/> |<span data-ttu-id="58e64-109">**MAPIUID**</span><span class="sxs-lookup"><span data-stu-id="58e64-109">**MAPIUID**</span></span> <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a><span data-ttu-id="58e64-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="58e64-110">Parameters</span></span>

 <span data-ttu-id="58e64-111">_lpuid1_</span><span class="sxs-lookup"><span data-stu-id="58e64-111">_lpuid1_</span></span>
  
> <span data-ttu-id="58e64-112">Указатель на структуру первого **MAPIUID** , который необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="58e64-112">Pointer to the first **MAPIUID** structure to be tested.</span></span> 
    
 <span data-ttu-id="58e64-113">_lpuid2_</span><span class="sxs-lookup"><span data-stu-id="58e64-113">_lpuid2_</span></span>
  
> <span data-ttu-id="58e64-114">Указатель на структуру второй **MAPIUID** , который необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="58e64-114">Pointer to the second **MAPIUID** structure to be tested.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="58e64-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="58e64-115">Remarks</span></span>

<span data-ttu-id="58e64-116">Макрос **IsEqualMAPIUID** возвращает значение TRUE, если две структуры **MAPIUID** содержат тот же идентификатор и значение FALSE, если это не так.</span><span class="sxs-lookup"><span data-stu-id="58e64-116">The **IsEqualMAPIUID** macro returns TRUE if the two **MAPIUID** structures contain the same identifier and FALSE if they do not.</span></span> 
  
<span data-ttu-id="58e64-117">Макрос **IsEqualMAPIUID** необходимо включить файл заголовка Memory.h.</span><span class="sxs-lookup"><span data-stu-id="58e64-117">The **IsEqualMAPIUID** macro requires that the header file Memory.h be included.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="58e64-118">См. также</span><span class="sxs-lookup"><span data-stu-id="58e64-118">See also</span></span>



[<span data-ttu-id="58e64-119">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="58e64-119">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="58e64-120">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="58e64-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

