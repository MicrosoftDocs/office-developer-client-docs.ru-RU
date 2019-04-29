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
# <a name="sandrestriction"></a><span data-ttu-id="29481-103">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="29481-103">SAndRestriction</span></span>

  
  
<span data-ttu-id="29481-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29481-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29481-105">Описывает ограничения **и** ограничения, которые используются для присоединения к группе ограничений с помощью логической операции **и** .</span><span class="sxs-lookup"><span data-stu-id="29481-105">Describes an **AND** restriction, which is used to join a group of restrictions using a logical **AND** operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="29481-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="29481-106">Header file:</span></span>  <br/> |<span data-ttu-id="29481-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="29481-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a><span data-ttu-id="29481-108">Members</span><span class="sxs-lookup"><span data-stu-id="29481-108">Members</span></span>

 <span data-ttu-id="29481-109">**Крес**</span><span class="sxs-lookup"><span data-stu-id="29481-109">**cRes**</span></span>
  
> <span data-ttu-id="29481-110">Число ограничений поиска в массиве, на который указывает элемент **лпрес** .</span><span class="sxs-lookup"><span data-stu-id="29481-110">Count of search restrictions in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="29481-111">**Лпрес**</span><span class="sxs-lookup"><span data-stu-id="29481-111">**lpRes**</span></span>
  
> <span data-ttu-id="29481-112">Указатель на массив структур [срестриктион](srestriction.md) , которые будут объединены с логической операцией **and** .</span><span class="sxs-lookup"><span data-stu-id="29481-112">Pointer to an array of [SRestriction](srestriction.md) structures that will be combined with a logical **AND** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="29481-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="29481-113">Remarks</span></span>

<span data-ttu-id="29481-114">Результат **сандрестриктион** имеет значение true, если все его дочерние ограничения оцениваются как true.</span><span class="sxs-lookup"><span data-stu-id="29481-114">The result of the **SAndRestriction** is TRUE if all its child restrictions evaluate to TRUE.</span></span> <span data-ttu-id="29481-115">Имеет значение FALSE, если любое дочернее ограничение имеет значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="29481-115">It is FALSE if any child restriction evaluates to FALSE.</span></span> 
  
<span data-ttu-id="29481-116">Описание типов ограничений, их построения и пример кода приведено в разделе [ограничения](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="29481-116">For a description of types of restrictions, how to build them, and sample code, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="29481-117">См. также</span><span class="sxs-lookup"><span data-stu-id="29481-117">See also</span></span>



[<span data-ttu-id="29481-118">SRestriction</span><span class="sxs-lookup"><span data-stu-id="29481-118">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="29481-119">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="29481-119">MAPI Structures</span></span>](mapi-structures.md)

