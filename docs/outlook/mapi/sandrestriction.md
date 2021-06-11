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
# <a name="sandrestriction"></a><span data-ttu-id="7efc2-103">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="7efc2-103">SAndRestriction</span></span>

  
  
<span data-ttu-id="7efc2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7efc2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7efc2-105">Описывает ограничение **AND,** которое используется для вступив в группу ограничений с помощью логической **и операции.**</span><span class="sxs-lookup"><span data-stu-id="7efc2-105">Describes an **AND** restriction, which is used to join a group of restrictions using a logical **AND** operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7efc2-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="7efc2-106">Header file:</span></span>  <br/> |<span data-ttu-id="7efc2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7efc2-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a><span data-ttu-id="7efc2-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="7efc2-108">Members</span></span>

 <span data-ttu-id="7efc2-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="7efc2-109">**cRes**</span></span>
  
> <span data-ttu-id="7efc2-110">Количество ограничений поиска в массиве, на который указывает член **lpRes.**</span><span class="sxs-lookup"><span data-stu-id="7efc2-110">Count of search restrictions in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="7efc2-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="7efc2-111">**lpRes**</span></span>
  
> <span data-ttu-id="7efc2-112">Указатель на массив [структур SRestriction,](srestriction.md) которые будут объединены с логической и **операцией.**</span><span class="sxs-lookup"><span data-stu-id="7efc2-112">Pointer to an array of [SRestriction](srestriction.md) structures that will be combined with a logical **AND** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7efc2-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="7efc2-113">Remarks</span></span>

<span data-ttu-id="7efc2-114">Результат **SAndRestriction** true, если все его ограничения для детей оцениваются как TRUE.</span><span class="sxs-lookup"><span data-stu-id="7efc2-114">The result of the **SAndRestriction** is TRUE if all its child restrictions evaluate to TRUE.</span></span> <span data-ttu-id="7efc2-115">Это FALSE, если любое ограничение для детей оценивается как FALSE.</span><span class="sxs-lookup"><span data-stu-id="7efc2-115">It is FALSE if any child restriction evaluates to FALSE.</span></span> 
  
<span data-ttu-id="7efc2-116">Описание типов ограничений, их сборки и пример кода см. в описании [ограничений.](about-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="7efc2-116">For a description of types of restrictions, how to build them, and sample code, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7efc2-117">См. также</span><span class="sxs-lookup"><span data-stu-id="7efc2-117">See also</span></span>



[<span data-ttu-id="7efc2-118">SRestriction</span><span class="sxs-lookup"><span data-stu-id="7efc2-118">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="7efc2-119">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="7efc2-119">MAPI Structures</span></span>](mapi-structures.md)

