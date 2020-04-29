---
title: SExistRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SExistRestriction
api_type:
- COM
ms.assetid: 48d5ab42-ee70-4f6e-9184-18d22b08ea1b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6e3cdcf3579b26776d9e278bb339758d4f56d890
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418941"
---
# <a name="sexistrestriction"></a><span data-ttu-id="a2895-103">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="a2895-103">SExistRestriction</span></span>

  
  
<span data-ttu-id="a2895-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2895-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2895-105">Описывает ограничение EXISTS, используемое для проверки существования определенного свойства в виде столбца в таблице.</span><span class="sxs-lookup"><span data-stu-id="a2895-105">Describes an exist restriction which is used to test whether a particular property exists as a column in the table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a2895-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a2895-106">Header file:</span></span>  <br/> |<span data-ttu-id="a2895-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="a2895-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SExistRestriction
{
  ULONG ulReserved1;
  ULONG ulPropTag;
  ULONG ulReserved2;
} SExistRestriction;

```

## <a name="members"></a><span data-ttu-id="a2895-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="a2895-108">Members</span></span>

 <span data-ttu-id="a2895-109">**ulReserved1**</span><span class="sxs-lookup"><span data-stu-id="a2895-109">**ulReserved1**</span></span>
  
> <span data-ttu-id="a2895-110">Резервирования должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="a2895-110">Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="a2895-111">**улпроптаг**</span><span class="sxs-lookup"><span data-stu-id="a2895-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="a2895-112">Тег свойства, определяющий столбец, который необходимо проверить на существование в каждой строке.</span><span class="sxs-lookup"><span data-stu-id="a2895-112">Property tag identifying the column to be tested for existence in each row.</span></span>
    
 <span data-ttu-id="a2895-113">**ulReserved2**</span><span class="sxs-lookup"><span data-stu-id="a2895-113">**ulReserved2**</span></span>
  
> <span data-ttu-id="a2895-114">Резервирования должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="a2895-114">Reserved; must be zero.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a2895-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="a2895-115">Remarks</span></span>

<span data-ttu-id="a2895-116">Ограничение EXISTS используется для обеспечения осмысленных результатов для других типов ограничений, включающих в себя свойства, такие как ограничения свойств и контента.</span><span class="sxs-lookup"><span data-stu-id="a2895-116">The exist restriction is used to guarantee meaningful results for other types of restrictions that involve properties, such as property and content restrictions.</span></span> <span data-ttu-id="a2895-117">Если ограничение, включающее свойство, передается в [IMAPITable:: restrict](imapitable-restrict.md) или [IMAPITable:: FindRow](imapitable-findrow.md) , а свойство не существует, результаты ограничения не определены.</span><span class="sxs-lookup"><span data-stu-id="a2895-117">When a restriction that involves a property is passed to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) and the property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="a2895-118">Создавая **ограничение,** которое присоединяется к ограничению свойств с ограничением EXISTS, вызывающий абонент может гарантировать точный результат.</span><span class="sxs-lookup"><span data-stu-id="a2895-118">By creating an **AND** restriction that joins the property restriction with an exist restriction, a caller can be guaranteed accurate results.</span></span> 
  
<span data-ttu-id="a2895-119">Ограничения EXISTS не могут использоваться с свойствами вложенных объектов, имеющими тип PT_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="a2895-119">Exist restrictions cannot be used with sub-object properties that have type PT_OBJECT.</span></span> 
  
<span data-ttu-id="a2895-120">Более подробную информацию о структуре **сексистрестриктион** можно узнать в статье [ограничения](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="a2895-120">For more information about the **SExistRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a2895-121">См. также</span><span class="sxs-lookup"><span data-stu-id="a2895-121">See also</span></span>



[<span data-ttu-id="a2895-122">SRestriction</span><span class="sxs-lookup"><span data-stu-id="a2895-122">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="a2895-123">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="a2895-123">MAPI Structures</span></span>](mapi-structures.md)

