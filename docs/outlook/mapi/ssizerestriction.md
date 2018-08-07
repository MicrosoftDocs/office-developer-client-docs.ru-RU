---
title: SSizeRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSizeRestriction
api_type:
- COM
ms.assetid: 4e7340d1-3cb9-4276-b83f-1c8f94acb909
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 134eb844ef7b72d396c300b27a87a3a7ae320cf1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812389"
---
# <a name="ssizerestriction"></a><span data-ttu-id="476e6-103">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="476e6-103">SSizeRestriction</span></span>

  
  
<span data-ttu-id="476e6-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="476e6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="476e6-105">Описываются ограничения размера, который используется для тестирования размера значение свойства.</span><span class="sxs-lookup"><span data-stu-id="476e6-105">Describes a size restriction which is used to test the size of a property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="476e6-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="476e6-106">Header file:</span></span>  <br/> |<span data-ttu-id="476e6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="476e6-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSizeRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  ULONG cb;
} SSizeRestriction;

```

## <a name="members"></a><span data-ttu-id="476e6-108">Members</span><span class="sxs-lookup"><span data-stu-id="476e6-108">Members</span></span>

 <span data-ttu-id="476e6-109">**RelOp**</span><span class="sxs-lookup"><span data-stu-id="476e6-109">**relop**</span></span>
  
> <span data-ttu-id="476e6-110">Оператор, который используется для сравнения размера.</span><span class="sxs-lookup"><span data-stu-id="476e6-110">Relational operator that is used in the size comparison.</span></span> <span data-ttu-id="476e6-111">Ниже приведены возможные значения:</span><span class="sxs-lookup"><span data-stu-id="476e6-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="476e6-112">RELOP_GE</span><span class="sxs-lookup"><span data-stu-id="476e6-112">RELOP_GE</span></span> 
  
> <span data-ttu-id="476e6-113">Сравнение выполняется на основе больше или равно первого значения.</span><span class="sxs-lookup"><span data-stu-id="476e6-113">The comparison is made based on a greater or equal first value.</span></span>
    
<span data-ttu-id="476e6-114">RELOP_GT</span><span class="sxs-lookup"><span data-stu-id="476e6-114">RELOP_GT</span></span> 
  
> <span data-ttu-id="476e6-115">Сравнение выполняется на основе больше первого значения.</span><span class="sxs-lookup"><span data-stu-id="476e6-115">The comparison is made based on a greater first value.</span></span>
    
<span data-ttu-id="476e6-116">RELOP_LE</span><span class="sxs-lookup"><span data-stu-id="476e6-116">RELOP_LE</span></span> 
  
> <span data-ttu-id="476e6-117">Сравнение выполняется на основе меньше или равно первого значения.</span><span class="sxs-lookup"><span data-stu-id="476e6-117">The comparison is made based on a lesser or equal first value.</span></span>
    
<span data-ttu-id="476e6-118">RELOP_LT</span><span class="sxs-lookup"><span data-stu-id="476e6-118">RELOP_LT</span></span> 
  
> <span data-ttu-id="476e6-119">Сравнение выполняется на основе меньшим первое значение.</span><span class="sxs-lookup"><span data-stu-id="476e6-119">The comparison is made based on a lesser first value.</span></span>
    
<span data-ttu-id="476e6-120">RELOP_NE</span><span class="sxs-lookup"><span data-stu-id="476e6-120">RELOP_NE</span></span> 
  
> <span data-ttu-id="476e6-121">Сравнение выполняется на основе разные значения.</span><span class="sxs-lookup"><span data-stu-id="476e6-121">The comparison is made based on unequal values.</span></span>
    
<span data-ttu-id="476e6-122">RELOP_RE</span><span class="sxs-lookup"><span data-stu-id="476e6-122">RELOP_RE</span></span> 
  
> <span data-ttu-id="476e6-123">Сравнение выполняется на основе как значения (регулярное выражение).</span><span class="sxs-lookup"><span data-stu-id="476e6-123">The comparison is made based on LIKE (regular expression) values.</span></span>
    
<span data-ttu-id="476e6-124">RELOP_EQ</span><span class="sxs-lookup"><span data-stu-id="476e6-124">RELOP_EQ</span></span> 
  
> <span data-ttu-id="476e6-125">Сравнение выполняется на основе одинаковые значения.</span><span class="sxs-lookup"><span data-stu-id="476e6-125">The comparison is made based on equal values.</span></span>
    
 <span data-ttu-id="476e6-126">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="476e6-126">**ulPropTag**</span></span>
  
> <span data-ttu-id="476e6-127">Свойство tag идентификации свойства для тестирования.</span><span class="sxs-lookup"><span data-stu-id="476e6-127">Property tag identifying the property to test.</span></span>
    
 <span data-ttu-id="476e6-128">**cb**</span><span class="sxs-lookup"><span data-stu-id="476e6-128">**cb**</span></span>
  
> <span data-ttu-id="476e6-129">Число байт в значение свойства.</span><span class="sxs-lookup"><span data-stu-id="476e6-129">Count of bytes in the property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="476e6-130">Замечания</span><span class="sxs-lookup"><span data-stu-id="476e6-130">Remarks</span></span>

<span data-ttu-id="476e6-131">Общие сведения о работе ограничения обратитесь к разделу [О ограничения](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="476e6-131">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="476e6-132">См. также</span><span class="sxs-lookup"><span data-stu-id="476e6-132">See also</span></span>



[<span data-ttu-id="476e6-133">SRestriction</span><span class="sxs-lookup"><span data-stu-id="476e6-133">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="476e6-134">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="476e6-134">MAPI Structures</span></span>](mapi-structures.md)

