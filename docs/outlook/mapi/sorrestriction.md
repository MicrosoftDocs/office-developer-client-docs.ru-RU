---
title: SOrRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SOrRestriction
api_type:
- COM
ms.assetid: 6fee29ce-9a34-4e0c-bb71-03120c3f1117
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9b4ca4628f356142eb5303c064e3916474810fda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345103"
---
# <a name="sorrestriction"></a><span data-ttu-id="08b0c-103">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="08b0c-103">SOrRestriction</span></span>

  
  
<span data-ttu-id="08b0c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08b0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08b0c-105">Описывает ограничение \*\*\*\* , используемое для применения логической операции **или** к ограничению.</span><span class="sxs-lookup"><span data-stu-id="08b0c-105">Describes an **OR** restriction which is used to apply a logical **OR** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08b0c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="08b0c-106">Header file:</span></span>  <br/> |<span data-ttu-id="08b0c-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="08b0c-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SOrRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SOrRestriction;

```

## <a name="members"></a><span data-ttu-id="08b0c-108">Members</span><span class="sxs-lookup"><span data-stu-id="08b0c-108">Members</span></span>

 <span data-ttu-id="08b0c-109">**Крес**</span><span class="sxs-lookup"><span data-stu-id="08b0c-109">**cRes**</span></span>
  
> <span data-ttu-id="08b0c-110">Количество структур в массиве, на которое указывает элемент **лпрес** .</span><span class="sxs-lookup"><span data-stu-id="08b0c-110">Count of structures in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="08b0c-111">**Лпрес**</span><span class="sxs-lookup"><span data-stu-id="08b0c-111">**lpRes**</span></span>
  
> <span data-ttu-id="08b0c-112">Указатель на структуру [срестриктион](srestriction.md) , описывающую ограничение, которое необходимо присоединить с помощью логической операции **or** .</span><span class="sxs-lookup"><span data-stu-id="08b0c-112">Pointer to the [SRestriction](srestriction.md) structure describing the restriction to be joined using the logical **OR** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="08b0c-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08b0c-113">Remarks</span></span>

<span data-ttu-id="08b0c-114">Более подробную информацию о структуре **соррестриктион** можно узнать в статье [ограничения](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="08b0c-114">For more information about the **SOrRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="08b0c-115">См. также</span><span class="sxs-lookup"><span data-stu-id="08b0c-115">See also</span></span>



[<span data-ttu-id="08b0c-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="08b0c-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="08b0c-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="08b0c-117">MAPI Structures</span></span>](mapi-structures.md)

