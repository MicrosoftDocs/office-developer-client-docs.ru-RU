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
ms.openlocfilehash: 62b5a42a540a4fb96761c45cd51c510f12225e9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812278"
---
# <a name="sexistrestriction"></a><span data-ttu-id="28f87-103">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="28f87-103">SExistRestriction</span></span>

  
  
<span data-ttu-id="28f87-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="28f87-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="28f87-105">Описание ограничений exist, который используется для проверки, является ли определенное свойство существует в виде столбцов в таблице.</span><span class="sxs-lookup"><span data-stu-id="28f87-105">Describes an exist restriction which is used to test whether a particular property exists as a column in the table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="28f87-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="28f87-106">Header file:</span></span>  <br/> |<span data-ttu-id="28f87-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="28f87-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SExistRestriction
{
  ULONG ulReserved1;
  ULONG ulPropTag;
  ULONG ulReserved2;
} SExistRestriction;

```

## <a name="members"></a><span data-ttu-id="28f87-108">Members</span><span class="sxs-lookup"><span data-stu-id="28f87-108">Members</span></span>

 <span data-ttu-id="28f87-109">**ulReserved1**</span><span class="sxs-lookup"><span data-stu-id="28f87-109">**ulReserved1**</span></span>
  
> <span data-ttu-id="28f87-110">Зарезервировано; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="28f87-110">Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="28f87-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="28f87-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="28f87-112">Свойство tag определение столбца проверяется на наличие в каждой строке.</span><span class="sxs-lookup"><span data-stu-id="28f87-112">Property tag identifying the column to be tested for existence in each row.</span></span>
    
 <span data-ttu-id="28f87-113">**ulReserved2**</span><span class="sxs-lookup"><span data-stu-id="28f87-113">**ulReserved2**</span></span>
  
> <span data-ttu-id="28f87-114">Зарезервировано; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="28f87-114">Reserved; must be zero.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="28f87-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="28f87-115">Remarks</span></span>

<span data-ttu-id="28f87-116">Ограничение exist используется для обеспечения достоверные результаты для других типов ограничений, в которых используются свойства, такие как свойства и содержимое ограничения.</span><span class="sxs-lookup"><span data-stu-id="28f87-116">The exist restriction is used to guarantee meaningful results for other types of restrictions that involve properties, such as property and content restrictions.</span></span> <span data-ttu-id="28f87-117">Если свойство не существует ограничение, которое включает в себя свойства передается [IMAPITable::Restrict](imapitable-restrict.md) или [IMAPITable::FindRow](imapitable-findrow.md) , результаты ограничение не определено.</span><span class="sxs-lookup"><span data-stu-id="28f87-117">When a restriction that involves a property is passed to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) and the property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="28f87-118">Путем создания **и** ограничение, которое присоединяется ограничение свойства ограничению exist Звонящий может гарантировать точных результатов.</span><span class="sxs-lookup"><span data-stu-id="28f87-118">By creating an **AND** restriction that joins the property restriction with an exist restriction, a caller can be guaranteed accurate results.</span></span> 
  
<span data-ttu-id="28f87-119">Существуют ограничения не может использоваться со свойствами дочерний объект, имеющие тип PT_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="28f87-119">Exist restrictions cannot be used with sub-object properties that have type PT_OBJECT.</span></span> 
  
<span data-ttu-id="28f87-120">Дополнительные сведения о структуре **SExistRestriction** [О ограничения](about-restrictions.md)см.</span><span class="sxs-lookup"><span data-stu-id="28f87-120">For more information about the **SExistRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="28f87-121">См. также</span><span class="sxs-lookup"><span data-stu-id="28f87-121">See also</span></span>



[<span data-ttu-id="28f87-122">SRestriction</span><span class="sxs-lookup"><span data-stu-id="28f87-122">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="28f87-123">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="28f87-123">MAPI Structures</span></span>](mapi-structures.md)

