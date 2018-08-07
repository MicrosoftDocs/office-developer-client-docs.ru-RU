---
title: SSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSortOrderSet
api_type:
- COM
ms.assetid: e7f9be6a-92e7-44a8-93ee-b087713a31df
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1604c4a1a0d1bf4008595b0d150b4f7eb3d1c2ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812379"
---
# <a name="ssortorderset"></a><span data-ttu-id="e61e6-103">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="e61e6-103">SSortOrderSet</span></span>

  
  
<span data-ttu-id="e61e6-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e61e6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e61e6-105">Определяет коллекцию ключей сортировки для таблицы, используемый для сортировки стандартный или по категориям.</span><span class="sxs-lookup"><span data-stu-id="e61e6-105">Defines a collection of sort keys for a table that is used for standard or categorized sorting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e61e6-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e61e6-106">Header file:</span></span>  <br/> |<span data-ttu-id="e61e6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e61e6-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e61e6-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="e61e6-108">Related macros:</span></span>  <br/> |<span data-ttu-id="e61e6-109">[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md) [SizedSSortOrderSet](sizedssortorderset.md)</span><span class="sxs-lookup"><span data-stu-id="e61e6-109">[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md)</span></span> <br/> |
   
```cpp
typedef struct _SSortOrderSet
{
  ULONG cSorts;
  ULONG cCategories;
  ULONG cExpanded;
  SSortOrder aSort[MAPI_DIM];
} SSortOrderSet, FAR *LPSSortOrderSet;

```

## <a name="members"></a><span data-ttu-id="e61e6-110">Members</span><span class="sxs-lookup"><span data-stu-id="e61e6-110">Members</span></span>

 <span data-ttu-id="e61e6-111">**cSorts**</span><span class="sxs-lookup"><span data-stu-id="e61e6-111">**cSorts**</span></span>
  
> <span data-ttu-id="e61e6-112">Число [SSortOrder](ssortorder.md) структуры, которые включены в элемент **aSort** .</span><span class="sxs-lookup"><span data-stu-id="e61e6-112">Count of [SSortOrder](ssortorder.md) structures that are included in the **aSort** member.</span></span> 
    
 <span data-ttu-id="e61e6-113">**cCategories**</span><span class="sxs-lookup"><span data-stu-id="e61e6-113">**cCategories**</span></span>
  
> <span data-ttu-id="e61e6-114">Число столбцов, которые используются для категории столбцов.</span><span class="sxs-lookup"><span data-stu-id="e61e6-114">Count of columns that are designated as category columns.</span></span> <span data-ttu-id="e61e6-115">Возможны значения в диапазоне от нуля, это означает не по категориям или стандартный сортировки, на номер, указанный в параметре члена **cSorts** .</span><span class="sxs-lookup"><span data-stu-id="e61e6-115">Possible values range from zero, which indicates a non-categorized or standard sort, to the number indicated by the **cSorts** member.</span></span> 
    
 <span data-ttu-id="e61e6-116">**cExpanded**</span><span class="sxs-lookup"><span data-stu-id="e61e6-116">**cExpanded**</span></span>
  
> <span data-ttu-id="e61e6-117">Число категорий, которые запускаются в развернутом состоянии, где все строки, относящиеся к категории отображаются в табличном представлении.</span><span class="sxs-lookup"><span data-stu-id="e61e6-117">Count of categories that start in an expanded state, where all of the rows that apply to the category are visible in the table view.</span></span> <span data-ttu-id="e61e6-118">Диапазон допустимых значений от 0 до номер, указанный в параметре **cCategories**.</span><span class="sxs-lookup"><span data-stu-id="e61e6-118">Possible values range from 0 to the number indicated by **cCategories**.</span></span>
    
 <span data-ttu-id="e61e6-119">**aSort**</span><span class="sxs-lookup"><span data-stu-id="e61e6-119">**aSort**</span></span>
  
> <span data-ttu-id="e61e6-120">Массив структур **SSortOrder** каждого определения порядка сортировки.</span><span class="sxs-lookup"><span data-stu-id="e61e6-120">Array of **SSortOrder** structures, each defining a sort order.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e61e6-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="e61e6-121">Remarks</span></span>

<span data-ttu-id="e61e6-122">Структура **SSortOrderSet** используется для определения нескольких порядок сортировки для сортировки standard и по категориям.</span><span class="sxs-lookup"><span data-stu-id="e61e6-122">A **SSortOrderSet** structure is used for defining multiple sort orders for standard and categorized sorting.</span></span> 
  
<span data-ttu-id="e61e6-123">Структура каждого **SSortOrderSet** содержит по крайней мере один **SSortOrder** структуры, определяется направление сортировки и столбца, который будет использоваться в качестве ключа сортировки.</span><span class="sxs-lookup"><span data-stu-id="e61e6-123">Each **SSortOrderSet** structure contains at least one **SSortOrder** structure defining the direction of the sort and the column that will be used as the sort key.</span></span> <span data-ttu-id="e61e6-124">Для сортировки по категориям, этот столбец используется в качестве категории.</span><span class="sxs-lookup"><span data-stu-id="e61e6-124">For categorized sorting, this column is used as the category.</span></span> <span data-ttu-id="e61e6-125">Когда значение элемента **cSorts** превышает значение элемента **cCategories** , существует несколько ключей сортировки, чем категорий и категории создаются из столбцов, отображаемых в массиве **SSortOrder** первого.</span><span class="sxs-lookup"><span data-stu-id="e61e6-125">When the value of the **cSorts** member exceeds the value of the **cCategories** member, there are more sort keys than categories, and categories are created from the columns that appear first in the **SSortOrder** array.</span></span> 
  
<span data-ttu-id="e61e6-126">К примеру Если **cSorts** задано значение 3, **cCategories** задано значение 2, столбцы, описанные в член **ulPropTag** первых двух записей в массиве **SSortOrder** используются в качестве столбцов категории.</span><span class="sxs-lookup"><span data-stu-id="e61e6-126">For example, if **cSorts** is set to 3 and **cCategories** is set to 2, the columns described by the **ulPropTag** member of the first two entries in the **SSortOrder** array are used as the category columns.</span></span> <span data-ttu-id="e61e6-127">Первой записи выступает в качестве категории верхнего уровня группировки; второй запись как дополнительный группировки.</span><span class="sxs-lookup"><span data-stu-id="e61e6-127">The first entry serves as the top-level category grouping; the second entry as the secondary grouping.</span></span> <span data-ttu-id="e61e6-128">Все строки, соответствующие столбцы двух категорий сортируются с помощью ключа сортировки, определенных в третья запись.</span><span class="sxs-lookup"><span data-stu-id="e61e6-128">All of the rows that match the two category columns are sorted by using the sort key defined in the third entry.</span></span> 
  
<span data-ttu-id="e61e6-129">Элемент **cExpanded** указывает число категорий, которые в первую очередь расширяются.</span><span class="sxs-lookup"><span data-stu-id="e61e6-129">The **cExpanded** member specifies the number of categories that are at first expanded.</span></span> <span data-ttu-id="e61e6-130">При наличии нескольких категорий, реализации таблицы начинается с первого столбца в качестве категории и сохраняется в последовательности со столбцами последующих категории до превысил количество **cCategories** .</span><span class="sxs-lookup"><span data-stu-id="e61e6-130">When there are multiple categories, the table implementation starts with the first column to be designated as a category and continues in sequential order with the subsequent category columns until the number of **cCategories** has been exceeded.</span></span> <span data-ttu-id="e61e6-131">Если имеются дополнительные столбцы категории, чем расширенное столбцов, свернуты столбцы категории.</span><span class="sxs-lookup"><span data-stu-id="e61e6-131">If there are more category columns than there are expanded columns, the category columns are collapsed.</span></span> <span data-ttu-id="e61e6-132">Если **cExpanded** равно нулю, доступные пользователю таблицы для отображения только строку заголовков верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="e61e6-132">If **cExpanded** is equal to zero, only the top level heading row is available to the table user for display.</span></span> <span data-ttu-id="e61e6-133">Если нет конечные строки, **cExpanded** равно один меньше, чем число категорий, а затем все строки заголовка.</span><span class="sxs-lookup"><span data-stu-id="e61e6-133">If **cExpanded** is equal to one less than the number of categories, then all of the heading rows and none of the leaf rows are available.</span></span> <span data-ttu-id="e61e6-134">Если **cExpanded** равно числу категориями, таблицы полностью развернут.</span><span class="sxs-lookup"><span data-stu-id="e61e6-134">If **cExpanded** is equal to the number of categories, then the table is fully expanded.</span></span> 
  
<span data-ttu-id="e61e6-135">Дополнительные сведения о стандартных и по категориям сортировка см [категоризации](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="e61e6-135">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e61e6-136">См. также</span><span class="sxs-lookup"><span data-stu-id="e61e6-136">See also</span></span>



[<span data-ttu-id="e61e6-137">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="e61e6-137">SSortOrder</span></span>](ssortorder.md)
  
[<span data-ttu-id="e61e6-138">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="e61e6-138">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="e61e6-139">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="e61e6-139">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)


[<span data-ttu-id="e61e6-140">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="e61e6-140">MAPI Structures</span></span>](mapi-structures.md)

