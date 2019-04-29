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
# <a name="snotrestriction"></a><span data-ttu-id="82a17-103">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="82a17-103">SNotRestriction</span></span>

  
  
<span data-ttu-id="82a17-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82a17-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82a17-105">Описывает ограничение \*\*\*\* , которое используется для применения логической операции **Not** к ограничению.</span><span class="sxs-lookup"><span data-stu-id="82a17-105">Describes a **NOT** restriction, which is used to apply a logical **NOT** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="82a17-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="82a17-106">Header file:</span></span>  <br/> |<span data-ttu-id="82a17-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="82a17-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SNotRestriction
{
  ULONG ulReserved;
  LPSRestriction lpRes;
} SNotRestriction;

```

## <a name="members"></a><span data-ttu-id="82a17-108">Members</span><span class="sxs-lookup"><span data-stu-id="82a17-108">Members</span></span>

 <span data-ttu-id="82a17-109">**Улресервед**</span><span class="sxs-lookup"><span data-stu-id="82a17-109">**ulReserved**</span></span>
  
> <span data-ttu-id="82a17-110">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="82a17-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="82a17-111">**Лпрес**</span><span class="sxs-lookup"><span data-stu-id="82a17-111">**lpRes**</span></span>
  
> <span data-ttu-id="82a17-112">Указатель на структуру [срестриктион](srestriction.md) , описывающую ограничение, которое необходимо присоединить к логическому оператору **Not** .</span><span class="sxs-lookup"><span data-stu-id="82a17-112">Pointer to a [SRestriction](srestriction.md) structure describing the restriction to be joined to the logical **NOT** operator.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="82a17-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="82a17-113">Remarks</span></span>

<span data-ttu-id="82a17-114">Более подробную информацию о структуре **снотрестриктион** можно узнать в статье [ограничения](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="82a17-114">For more information about the **SNotRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="82a17-115">См. также</span><span class="sxs-lookup"><span data-stu-id="82a17-115">See also</span></span>



[<span data-ttu-id="82a17-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="82a17-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="82a17-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="82a17-117">MAPI Structures</span></span>](mapi-structures.md)

