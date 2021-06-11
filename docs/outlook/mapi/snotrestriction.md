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
ms.openlocfilehash: 07a1a0a1953d136da534fbdc6339d326c877bebf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426655"
---
# <a name="snotrestriction"></a><span data-ttu-id="f78cb-103">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="f78cb-103">SNotRestriction</span></span>

  
  
<span data-ttu-id="f78cb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f78cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f78cb-105">Описывает ограничение **NOT,** которое используется для применения логической **операции NOT** к ограничению.</span><span class="sxs-lookup"><span data-stu-id="f78cb-105">Describes a **NOT** restriction, which is used to apply a logical **NOT** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f78cb-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f78cb-106">Header file:</span></span>  <br/> |<span data-ttu-id="f78cb-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f78cb-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SNotRestriction
{
  ULONG ulReserved;
  LPSRestriction lpRes;
} SNotRestriction;

```

## <a name="members"></a><span data-ttu-id="f78cb-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="f78cb-108">Members</span></span>

 <span data-ttu-id="f78cb-109">**ulReserved**</span><span class="sxs-lookup"><span data-stu-id="f78cb-109">**ulReserved**</span></span>
  
> <span data-ttu-id="f78cb-110">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="f78cb-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="f78cb-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="f78cb-111">**lpRes**</span></span>
  
> <span data-ttu-id="f78cb-112">Указатель на [структуру SRestriction,](srestriction.md) описывающий ограничение, присоединяемую к логическому **оператору NOT.**</span><span class="sxs-lookup"><span data-stu-id="f78cb-112">Pointer to a [SRestriction](srestriction.md) structure describing the restriction to be joined to the logical **NOT** operator.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f78cb-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="f78cb-113">Remarks</span></span>

<span data-ttu-id="f78cb-114">Дополнительные сведения о структуре **SNotRestriction** см. в дополнительных [сведениях об ограничениях.](about-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="f78cb-114">For more information about the **SNotRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f78cb-115">См. также</span><span class="sxs-lookup"><span data-stu-id="f78cb-115">See also</span></span>



[<span data-ttu-id="f78cb-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="f78cb-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="f78cb-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="f78cb-117">MAPI Structures</span></span>](mapi-structures.md)

