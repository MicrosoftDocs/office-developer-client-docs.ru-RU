---
title: SAndRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAndRestriction
api_type:
- COM
ms.assetid: 1b7dfe87-f87f-43e3-8332-a0d9c3f70d16
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1437130caecd57344fc171d234c5391ea92e1d4b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812189"
---
# <a name="sandrestriction"></a><span data-ttu-id="49750-103">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="49750-103">SAndRestriction</span></span>

  
  
<span data-ttu-id="49750-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="49750-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="49750-105">Описываются ограничения **и** используется для объединения группы с помощью логическую операцию **и** .</span><span class="sxs-lookup"><span data-stu-id="49750-105">Describes an **AND** restriction, which is used to join a group of restrictions using a logical **AND** operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="49750-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="49750-106">Header file:</span></span>  <br/> |<span data-ttu-id="49750-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="49750-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a><span data-ttu-id="49750-108">Members</span><span class="sxs-lookup"><span data-stu-id="49750-108">Members</span></span>

 <span data-ttu-id="49750-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="49750-109">**cRes**</span></span>
  
> <span data-ttu-id="49750-110">Число ограничения поиска в массиве, на который указывает член **lpRes** .</span><span class="sxs-lookup"><span data-stu-id="49750-110">Count of search restrictions in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="49750-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="49750-111">**lpRes**</span></span>
  
> <span data-ttu-id="49750-112">Указатель на массив структур [SRestriction](srestriction.md) , которые будут использоваться в сочетании с логическую операцию **и** .</span><span class="sxs-lookup"><span data-stu-id="49750-112">Pointer to an array of [SRestriction](srestriction.md) structures that will be combined with a logical **AND** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="49750-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="49750-113">Remarks</span></span>

<span data-ttu-id="49750-114">В результате **SAndRestriction** имеет значение TRUE, если все его дочерние ограничения принимают значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="49750-114">The result of the **SAndRestriction** is TRUE if all its child restrictions evaluate to TRUE.</span></span> <span data-ttu-id="49750-115">Это значение FALSE, если любое ограничение дочерних имеет значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="49750-115">It is FALSE if any child restriction evaluates to FALSE.</span></span> 
  
<span data-ttu-id="49750-116">Описание ограничений как их, построения и пример кода, обратитесь к разделу [О ограничения](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="49750-116">For a description of types of restrictions, how to build them, and sample code, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="49750-117">См. также</span><span class="sxs-lookup"><span data-stu-id="49750-117">See also</span></span>



[<span data-ttu-id="49750-118">SRestriction</span><span class="sxs-lookup"><span data-stu-id="49750-118">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="49750-119">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="49750-119">MAPI Structures</span></span>](mapi-structures.md)

