---
title: SNotRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SNotRestriction
api_type:
- COM
ms.assetid: e86ca032-d973-4b79-976e-5240ab38a0da
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 174da93e7682246565b12c4fc4ffa6d1a9de065c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575065"
---
# <a name="snotrestriction"></a><span data-ttu-id="5da18-103">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="5da18-103">SNotRestriction</span></span>

  
  
<span data-ttu-id="5da18-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5da18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5da18-105">Описываются ограничения **не** , который используется для применения к ограничению логическая операция **не** .</span><span class="sxs-lookup"><span data-stu-id="5da18-105">Describes a **NOT** restriction, which is used to apply a logical **NOT** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5da18-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5da18-106">Header file:</span></span>  <br/> |<span data-ttu-id="5da18-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5da18-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SNotRestriction
{
  ULONG ulReserved;
  LPSRestriction lpRes;
} SNotRestriction;

```

## <a name="members"></a><span data-ttu-id="5da18-108">Members</span><span class="sxs-lookup"><span data-stu-id="5da18-108">Members</span></span>

 <span data-ttu-id="5da18-109">**ulReserved**</span><span class="sxs-lookup"><span data-stu-id="5da18-109">**ulReserved**</span></span>
  
> <span data-ttu-id="5da18-110">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="5da18-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="5da18-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="5da18-111">**lpRes**</span></span>
  
> <span data-ttu-id="5da18-112">Указатель на структуру [SRestriction](srestriction.md) , описывающая ограничения, чтобы быть присоединен к логический оператор, который **не** .</span><span class="sxs-lookup"><span data-stu-id="5da18-112">Pointer to a [SRestriction](srestriction.md) structure describing the restriction to be joined to the logical **NOT** operator.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5da18-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="5da18-113">Remarks</span></span>

<span data-ttu-id="5da18-114">Дополнительные сведения о структуре **SNotRestriction** [О ограничения](about-restrictions.md)см.</span><span class="sxs-lookup"><span data-stu-id="5da18-114">For more information about the **SNotRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5da18-115">См. также</span><span class="sxs-lookup"><span data-stu-id="5da18-115">See also</span></span>



[<span data-ttu-id="5da18-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="5da18-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="5da18-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="5da18-117">MAPI Structures</span></span>](mapi-structures.md)

