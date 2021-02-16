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
ms.openlocfilehash: da35c9c72f4cf3f076715a7a35a3e3514c672ceb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438885"
---
# <a name="sandrestriction"></a><span data-ttu-id="edb3e-103">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="edb3e-103">SAndRestriction</span></span>

  
  
<span data-ttu-id="edb3e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="edb3e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="edb3e-105">Описывает ограничение **AND,** которое используется для присоединить группу ограничений с помощью логической **операции AND.**</span><span class="sxs-lookup"><span data-stu-id="edb3e-105">Describes an **AND** restriction, which is used to join a group of restrictions using a logical **AND** operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="edb3e-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="edb3e-106">Header file:</span></span>  <br/> |<span data-ttu-id="edb3e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="edb3e-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a><span data-ttu-id="edb3e-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="edb3e-108">Members</span></span>

 <span data-ttu-id="edb3e-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="edb3e-109">**cRes**</span></span>
  
> <span data-ttu-id="edb3e-110">Количество ограничений поиска в массиве, на который указывает **член lpRes.**</span><span class="sxs-lookup"><span data-stu-id="edb3e-110">Count of search restrictions in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="edb3e-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="edb3e-111">**lpRes**</span></span>
  
> <span data-ttu-id="edb3e-112">Указатель на массив структур [SRestriction,](srestriction.md) которые будут объединены с логической операцией **AND.**</span><span class="sxs-lookup"><span data-stu-id="edb3e-112">Pointer to an array of [SRestriction](srestriction.md) structures that will be combined with a logical **AND** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="edb3e-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="edb3e-113">Remarks</span></span>

<span data-ttu-id="edb3e-114">Результат **SAndRestriction имеет** true, если все его ограничения для всех его child-ограничений оцениваются как TRUE.</span><span class="sxs-lookup"><span data-stu-id="edb3e-114">The result of the **SAndRestriction** is TRUE if all its child restrictions evaluate to TRUE.</span></span> <span data-ttu-id="edb3e-115">Если для какого-либо из ограничений имеется уровень FALSE, то имеется false.</span><span class="sxs-lookup"><span data-stu-id="edb3e-115">It is FALSE if any child restriction evaluates to FALSE.</span></span> 
  
<span data-ttu-id="edb3e-116">Описание типов ограничений, их сборки и пример кода см. в [описании ограничений.](about-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="edb3e-116">For a description of types of restrictions, how to build them, and sample code, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="edb3e-117">См. также</span><span class="sxs-lookup"><span data-stu-id="edb3e-117">See also</span></span>



[<span data-ttu-id="edb3e-118">SRestriction</span><span class="sxs-lookup"><span data-stu-id="edb3e-118">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="edb3e-119">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="edb3e-119">MAPI Structures</span></span>](mapi-structures.md)

