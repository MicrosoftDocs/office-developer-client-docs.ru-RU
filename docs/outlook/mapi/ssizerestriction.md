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
ms.openlocfilehash: 24ceb7b5358447de3a240756227b86224d2c354c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344480"
---
# <a name="ssizerestriction"></a><span data-ttu-id="ddc45-103">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="ddc45-103">SSizeRestriction</span></span>

  
  
<span data-ttu-id="ddc45-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ddc45-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ddc45-105">Описывает ограничение размера, используемое для проверки размера значения свойства.</span><span class="sxs-lookup"><span data-stu-id="ddc45-105">Describes a size restriction which is used to test the size of a property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ddc45-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ddc45-106">Header file:</span></span>  <br/> |<span data-ttu-id="ddc45-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="ddc45-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSizeRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  ULONG cb;
} SSizeRestriction;

```

## <a name="members"></a><span data-ttu-id="ddc45-108">Members</span><span class="sxs-lookup"><span data-stu-id="ddc45-108">Members</span></span>

 <span data-ttu-id="ddc45-109">**релоп**</span><span class="sxs-lookup"><span data-stu-id="ddc45-109">**relop**</span></span>
  
> <span data-ttu-id="ddc45-110">Оператор отношения, используемый в сравнении размера.</span><span class="sxs-lookup"><span data-stu-id="ddc45-110">Relational operator that is used in the size comparison.</span></span> <span data-ttu-id="ddc45-111">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ddc45-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="ddc45-112">РЕЛОП_ЖЕ</span><span class="sxs-lookup"><span data-stu-id="ddc45-112">RELOP_GE</span></span> 
  
> <span data-ttu-id="ddc45-113">Сравнение выполняется на основе значения, равного большему или равному первому значению.</span><span class="sxs-lookup"><span data-stu-id="ddc45-113">The comparison is made based on a greater or equal first value.</span></span>
    
<span data-ttu-id="ddc45-114">РЕЛОП_ГТ</span><span class="sxs-lookup"><span data-stu-id="ddc45-114">RELOP_GT</span></span> 
  
> <span data-ttu-id="ddc45-115">Сравнение выполняется на основе большего первого значения.</span><span class="sxs-lookup"><span data-stu-id="ddc45-115">The comparison is made based on a greater first value.</span></span>
    
<span data-ttu-id="ddc45-116">РЕЛОП_ЛЕ</span><span class="sxs-lookup"><span data-stu-id="ddc45-116">RELOP_LE</span></span> 
  
> <span data-ttu-id="ddc45-117">Сравнение выполняется на основе меньшего или равного первого значения.</span><span class="sxs-lookup"><span data-stu-id="ddc45-117">The comparison is made based on a lesser or equal first value.</span></span>
    
<span data-ttu-id="ddc45-118">РЕЛОП_ЛТ</span><span class="sxs-lookup"><span data-stu-id="ddc45-118">RELOP_LT</span></span> 
  
> <span data-ttu-id="ddc45-119">Сравнение выполняется на основе меньшего первого значения.</span><span class="sxs-lookup"><span data-stu-id="ddc45-119">The comparison is made based on a lesser first value.</span></span>
    
<span data-ttu-id="ddc45-120">РЕЛОП_НЕ</span><span class="sxs-lookup"><span data-stu-id="ddc45-120">RELOP_NE</span></span> 
  
> <span data-ttu-id="ddc45-121">Сравнение выполняется на основе неодинаковых значений.</span><span class="sxs-lookup"><span data-stu-id="ddc45-121">The comparison is made based on unequal values.</span></span>
    
<span data-ttu-id="ddc45-122">РЕЛОП_РЕ</span><span class="sxs-lookup"><span data-stu-id="ddc45-122">RELOP_RE</span></span> 
  
> <span data-ttu-id="ddc45-123">Сравнение выполняется на основе значений LIKE (регулярное выражение).</span><span class="sxs-lookup"><span data-stu-id="ddc45-123">The comparison is made based on LIKE (regular expression) values.</span></span>
    
<span data-ttu-id="ddc45-124">РЕЛОП_ЕК</span><span class="sxs-lookup"><span data-stu-id="ddc45-124">RELOP_EQ</span></span> 
  
> <span data-ttu-id="ddc45-125">Сравнение выполняется на основе равных значений.</span><span class="sxs-lookup"><span data-stu-id="ddc45-125">The comparison is made based on equal values.</span></span>
    
 <span data-ttu-id="ddc45-126">**Улпроптаг**</span><span class="sxs-lookup"><span data-stu-id="ddc45-126">**ulPropTag**</span></span>
  
> <span data-ttu-id="ddc45-127">Тег свойства, определяющий свойство для проверки.</span><span class="sxs-lookup"><span data-stu-id="ddc45-127">Property tag identifying the property to test.</span></span>
    
 <span data-ttu-id="ddc45-128">**cb**</span><span class="sxs-lookup"><span data-stu-id="ddc45-128">**cb**</span></span>
  
> <span data-ttu-id="ddc45-129">Количество байтов в значении свойства.</span><span class="sxs-lookup"><span data-stu-id="ddc45-129">Count of bytes in the property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ddc45-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ddc45-130">Remarks</span></span>

<span data-ttu-id="ddc45-131">Общие сведения о том, как действуют ограничения, можно узнать в статье [ограничения](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="ddc45-131">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ddc45-132">См. также</span><span class="sxs-lookup"><span data-stu-id="ddc45-132">See also</span></span>



[<span data-ttu-id="ddc45-133">SRestriction</span><span class="sxs-lookup"><span data-stu-id="ddc45-133">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="ddc45-134">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="ddc45-134">MAPI Structures</span></span>](mapi-structures.md)

