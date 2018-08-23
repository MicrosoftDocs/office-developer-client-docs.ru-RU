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
ms.openlocfilehash: 990fe49d39a73c5bf80b9fdda96d2e5997869edf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595421"
---
# <a name="ssizerestriction"></a><span data-ttu-id="53c60-103">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="53c60-103">SSizeRestriction</span></span>

  
  
<span data-ttu-id="53c60-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53c60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53c60-105">Описываются ограничения размера, который используется для тестирования размера значение свойства.</span><span class="sxs-lookup"><span data-stu-id="53c60-105">Describes a size restriction which is used to test the size of a property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="53c60-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="53c60-106">Header file:</span></span>  <br/> |<span data-ttu-id="53c60-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="53c60-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSizeRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  ULONG cb;
} SSizeRestriction;

```

## <a name="members"></a><span data-ttu-id="53c60-108">Members</span><span class="sxs-lookup"><span data-stu-id="53c60-108">Members</span></span>

 <span data-ttu-id="53c60-109">**RelOp**</span><span class="sxs-lookup"><span data-stu-id="53c60-109">**relop**</span></span>
  
> <span data-ttu-id="53c60-110">Оператор, который используется для сравнения размера.</span><span class="sxs-lookup"><span data-stu-id="53c60-110">Relational operator that is used in the size comparison.</span></span> <span data-ttu-id="53c60-111">Ниже приведены возможные значения:</span><span class="sxs-lookup"><span data-stu-id="53c60-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="53c60-112">RELOP_GE</span><span class="sxs-lookup"><span data-stu-id="53c60-112">RELOP_GE</span></span> 
  
> <span data-ttu-id="53c60-113">Сравнение выполняется на основе больше или равно первого значения.</span><span class="sxs-lookup"><span data-stu-id="53c60-113">The comparison is made based on a greater or equal first value.</span></span>
    
<span data-ttu-id="53c60-114">RELOP_GT</span><span class="sxs-lookup"><span data-stu-id="53c60-114">RELOP_GT</span></span> 
  
> <span data-ttu-id="53c60-115">Сравнение выполняется на основе больше первого значения.</span><span class="sxs-lookup"><span data-stu-id="53c60-115">The comparison is made based on a greater first value.</span></span>
    
<span data-ttu-id="53c60-116">RELOP_LE</span><span class="sxs-lookup"><span data-stu-id="53c60-116">RELOP_LE</span></span> 
  
> <span data-ttu-id="53c60-117">Сравнение выполняется на основе меньше или равно первого значения.</span><span class="sxs-lookup"><span data-stu-id="53c60-117">The comparison is made based on a lesser or equal first value.</span></span>
    
<span data-ttu-id="53c60-118">RELOP_LT</span><span class="sxs-lookup"><span data-stu-id="53c60-118">RELOP_LT</span></span> 
  
> <span data-ttu-id="53c60-119">Сравнение выполняется на основе меньшим первое значение.</span><span class="sxs-lookup"><span data-stu-id="53c60-119">The comparison is made based on a lesser first value.</span></span>
    
<span data-ttu-id="53c60-120">RELOP_NE</span><span class="sxs-lookup"><span data-stu-id="53c60-120">RELOP_NE</span></span> 
  
> <span data-ttu-id="53c60-121">Сравнение выполняется на основе разные значения.</span><span class="sxs-lookup"><span data-stu-id="53c60-121">The comparison is made based on unequal values.</span></span>
    
<span data-ttu-id="53c60-122">RELOP_RE</span><span class="sxs-lookup"><span data-stu-id="53c60-122">RELOP_RE</span></span> 
  
> <span data-ttu-id="53c60-123">Сравнение выполняется на основе как значения (регулярное выражение).</span><span class="sxs-lookup"><span data-stu-id="53c60-123">The comparison is made based on LIKE (regular expression) values.</span></span>
    
<span data-ttu-id="53c60-124">RELOP_EQ</span><span class="sxs-lookup"><span data-stu-id="53c60-124">RELOP_EQ</span></span> 
  
> <span data-ttu-id="53c60-125">Сравнение выполняется на основе одинаковые значения.</span><span class="sxs-lookup"><span data-stu-id="53c60-125">The comparison is made based on equal values.</span></span>
    
 <span data-ttu-id="53c60-126">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="53c60-126">**ulPropTag**</span></span>
  
> <span data-ttu-id="53c60-127">Свойство tag идентификации свойства для тестирования.</span><span class="sxs-lookup"><span data-stu-id="53c60-127">Property tag identifying the property to test.</span></span>
    
 <span data-ttu-id="53c60-128">**cb**</span><span class="sxs-lookup"><span data-stu-id="53c60-128">**cb**</span></span>
  
> <span data-ttu-id="53c60-129">Число байт в значение свойства.</span><span class="sxs-lookup"><span data-stu-id="53c60-129">Count of bytes in the property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="53c60-130">Замечания</span><span class="sxs-lookup"><span data-stu-id="53c60-130">Remarks</span></span>

<span data-ttu-id="53c60-131">Общие сведения о работе ограничения обратитесь к разделу [О ограничения](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="53c60-131">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="53c60-132">См. также</span><span class="sxs-lookup"><span data-stu-id="53c60-132">See also</span></span>



[<span data-ttu-id="53c60-133">SRestriction</span><span class="sxs-lookup"><span data-stu-id="53c60-133">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="53c60-134">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="53c60-134">MAPI Structures</span></span>](mapi-structures.md)

