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
ms.openlocfilehash: 635a4a872b83a2996b1a0198975a0ecd2cd906eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809580"
---
# <a name="isequalmapiuid"></a><span data-ttu-id="4eef7-103">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="4eef7-103">IsEqualMAPIUID</span></span>

  
  
<span data-ttu-id="4eef7-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4eef7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4eef7-105">Проверяет две структуры [MAPIUID](mapiuid.md) определяет, содержат ли они тот же идентификатор.</span><span class="sxs-lookup"><span data-stu-id="4eef7-105">Tests two [MAPIUID](mapiuid.md) structures to determine whether they contain the same identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4eef7-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="4eef7-106">Header file:</span></span>  <br/> |<span data-ttu-id="4eef7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4eef7-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4eef7-108">Связанные структуры:</span><span class="sxs-lookup"><span data-stu-id="4eef7-108">Related structure:</span></span>  <br/> |<span data-ttu-id="4eef7-109">**MAPIUID**</span><span class="sxs-lookup"><span data-stu-id="4eef7-109">**MAPIUID**</span></span> <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a><span data-ttu-id="4eef7-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="4eef7-110">Parameters</span></span>

 <span data-ttu-id="4eef7-111">_lpuid1_</span><span class="sxs-lookup"><span data-stu-id="4eef7-111">_lpuid1_</span></span>
  
> <span data-ttu-id="4eef7-112">Указатель на структуру первого **MAPIUID** , который необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="4eef7-112">Pointer to the first **MAPIUID** structure to be tested.</span></span> 
    
 <span data-ttu-id="4eef7-113">_lpuid2_</span><span class="sxs-lookup"><span data-stu-id="4eef7-113">_lpuid2_</span></span>
  
> <span data-ttu-id="4eef7-114">Указатель на структуру второй **MAPIUID** , который необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="4eef7-114">Pointer to the second **MAPIUID** structure to be tested.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4eef7-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="4eef7-115">Remarks</span></span>

<span data-ttu-id="4eef7-116">Макрос **IsEqualMAPIUID** возвращает значение TRUE, если две структуры **MAPIUID** содержат тот же идентификатор и значение FALSE, если это не так.</span><span class="sxs-lookup"><span data-stu-id="4eef7-116">The **IsEqualMAPIUID** macro returns TRUE if the two **MAPIUID** structures contain the same identifier and FALSE if they do not.</span></span> 
  
<span data-ttu-id="4eef7-117">Макрос **IsEqualMAPIUID** необходимо включить файл заголовка Memory.h.</span><span class="sxs-lookup"><span data-stu-id="4eef7-117">The **IsEqualMAPIUID** macro requires that the header file Memory.h be included.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4eef7-118">См. также</span><span class="sxs-lookup"><span data-stu-id="4eef7-118">See also</span></span>



[<span data-ttu-id="4eef7-119">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="4eef7-119">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="4eef7-120">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="4eef7-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

