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
ms.openlocfilehash: db19c3908c419b98b8deb71e2a86d0aa6eebe240
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438101"
---
# <a name="ssortorderset"></a><span data-ttu-id="986f9-103">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="986f9-103">SSortOrderSet</span></span>

  
  
<span data-ttu-id="986f9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="986f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="986f9-105">Определяет коллекцию ключей сортировки для таблицы, используемой для стандартной или классификации сортировки.</span><span class="sxs-lookup"><span data-stu-id="986f9-105">Defines a collection of sort keys for a table that is used for standard or categorized sorting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="986f9-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="986f9-106">Header file:</span></span>  <br/> |<span data-ttu-id="986f9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="986f9-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="986f9-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="986f9-108">Related macros:</span></span>  <br/> |<span data-ttu-id="986f9-109">[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md)</span><span class="sxs-lookup"><span data-stu-id="986f9-109">[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md)</span></span> <br/> |
   
```cpp
typedef struct _SSortOrderSet
{
  ULONG cSorts;
  ULONG cCategories;
  ULONG cExpanded;
  SSortOrder aSort[MAPI_DIM];
} SSortOrderSet, FAR *LPSSortOrderSet;

```

## <a name="members"></a><span data-ttu-id="986f9-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="986f9-110">Members</span></span>

 <span data-ttu-id="986f9-111">**cSorts**</span><span class="sxs-lookup"><span data-stu-id="986f9-111">**cSorts**</span></span>
  
> <span data-ttu-id="986f9-112">Количество структур [SSortOrder,](ssortorder.md) включенных в **член aSort.**</span><span class="sxs-lookup"><span data-stu-id="986f9-112">Count of [SSortOrder](ssortorder.md) structures that are included in the **aSort** member.</span></span> 
    
 <span data-ttu-id="986f9-113">**cCategories**</span><span class="sxs-lookup"><span data-stu-id="986f9-113">**cCategories**</span></span>
  
> <span data-ttu-id="986f9-114">Количество столбцов, обозначенных в качестве столбцов категорий.</span><span class="sxs-lookup"><span data-stu-id="986f9-114">Count of columns that are designated as category columns.</span></span> <span data-ttu-id="986f9-115">Диапазон возможных значений: от 0, что указывает на не категории или стандартную сортировку, до числа, задаваемого членом **cSorts.**</span><span class="sxs-lookup"><span data-stu-id="986f9-115">Possible values range from zero, which indicates a non-categorized or standard sort, to the number indicated by the **cSorts** member.</span></span> 
    
 <span data-ttu-id="986f9-116">**cExpanded**</span><span class="sxs-lookup"><span data-stu-id="986f9-116">**cExpanded**</span></span>
  
> <span data-ttu-id="986f9-117">Количество категорий, которые начинаются в расширенном состоянии, где все строки, применимые к категории, видны в представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="986f9-117">Count of categories that start in an expanded state, where all of the rows that apply to the category are visible in the table view.</span></span> <span data-ttu-id="986f9-118">Диапазон возможных значений : от 0 до числа, на который указывают **cCategories.**</span><span class="sxs-lookup"><span data-stu-id="986f9-118">Possible values range from 0 to the number indicated by **cCategories**.</span></span>
    
 <span data-ttu-id="986f9-119">**aSort**</span><span class="sxs-lookup"><span data-stu-id="986f9-119">**aSort**</span></span>
  
> <span data-ttu-id="986f9-120">Массив структур **SSortOrder,** каждый из которых определяет порядок сортировки.</span><span class="sxs-lookup"><span data-stu-id="986f9-120">Array of **SSortOrder** structures, each defining a sort order.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="986f9-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="986f9-121">Remarks</span></span>

<span data-ttu-id="986f9-122">Структура **SSortOrderSet** используется для определения нескольких заказов сортировки для стандартной и классификационной сортировки.</span><span class="sxs-lookup"><span data-stu-id="986f9-122">A **SSortOrderSet** structure is used for defining multiple sort orders for standard and categorized sorting.</span></span> 
  
<span data-ttu-id="986f9-123">Каждая **структура SSortOrderSet** содержит по крайней мере одну **структуру SSortOrder,** определяющие направление сортировки, и столбец, который будет использоваться в качестве ключа сортировки.</span><span class="sxs-lookup"><span data-stu-id="986f9-123">Each **SSortOrderSet** structure contains at least one **SSortOrder** structure defining the direction of the sort and the column that will be used as the sort key.</span></span> <span data-ttu-id="986f9-124">Для сортировки по категориям этот столбец используется в качестве категории.</span><span class="sxs-lookup"><span data-stu-id="986f9-124">For categorized sorting, this column is used as the category.</span></span> <span data-ttu-id="986f9-125">Если значение члена **cSorts** превышает значение члена **cCategories,** ключей сортировки больше, чем категорий, и категории создаются из столбцов, которые отображаются первыми в массиве **SSortOrder.**</span><span class="sxs-lookup"><span data-stu-id="986f9-125">When the value of the **cSorts** member exceeds the value of the **cCategories** member, there are more sort keys than categories, and categories are created from the columns that appear first in the **SSortOrder** array.</span></span> 
  
<span data-ttu-id="986f9-126">Например, если **cSorts** имеет 3, а **cCategories** — 2, столбцы, описанные членом **ulPropTag** первых двух записей в **массиве SSortOrder,** используются в качестве столбцов категории.</span><span class="sxs-lookup"><span data-stu-id="986f9-126">For example, if **cSorts** is set to 3 and **cCategories** is set to 2, the columns described by the **ulPropTag** member of the first two entries in the **SSortOrder** array are used as the category columns.</span></span> <span data-ttu-id="986f9-127">Первая запись служит в качестве группировки категорий верхнего уровня; вторая запись в качестве вторичной группировки.</span><span class="sxs-lookup"><span data-stu-id="986f9-127">The first entry serves as the top-level category grouping; the second entry as the secondary grouping.</span></span> <span data-ttu-id="986f9-128">Все строки, которые соответствуют двум столбцам категории, сортироваться с помощью ключа сортировки, определенного в третьей записи.</span><span class="sxs-lookup"><span data-stu-id="986f9-128">All of the rows that match the two category columns are sorted by using the sort key defined in the third entry.</span></span> 
  
<span data-ttu-id="986f9-129">Член **cExpanded** указывает количество категорий, которые были сначала расширены.</span><span class="sxs-lookup"><span data-stu-id="986f9-129">The **cExpanded** member specifies the number of categories that are at first expanded.</span></span> <span data-ttu-id="986f9-130">Если имеется несколько категорий, реализация таблицы начинается с первого столбца, который назначается в качестве категории, и продолжается в последовательном порядке с последующими столбцы категорий до тех пор, пока количество **cCategories** не будет превышено.</span><span class="sxs-lookup"><span data-stu-id="986f9-130">When there are multiple categories, the table implementation starts with the first column to be designated as a category and continues in sequential order with the subsequent category columns until the number of **cCategories** has been exceeded.</span></span> <span data-ttu-id="986f9-131">Если столбцов категорий больше, чем расширенных, столбцы категории свернуты.</span><span class="sxs-lookup"><span data-stu-id="986f9-131">If there are more category columns than there are expanded columns, the category columns are collapsed.</span></span> <span data-ttu-id="986f9-132">Если **cExpanded** равно нулю, пользователю таблицы доступна только строка заголовка верхнего уровня для отображения.</span><span class="sxs-lookup"><span data-stu-id="986f9-132">If **cExpanded** is equal to zero, only the top level heading row is available to the table user for display.</span></span> <span data-ttu-id="986f9-133">Если **cExpanded** на один меньше числа категорий, то все строки заголовков и ни одна из листовых строк не будут доступны.</span><span class="sxs-lookup"><span data-stu-id="986f9-133">If **cExpanded** is equal to one less than the number of categories, then all of the heading rows and none of the leaf rows are available.</span></span> <span data-ttu-id="986f9-134">Если **cExpanded** равно числу категорий, таблица будет полностью расширена.</span><span class="sxs-lookup"><span data-stu-id="986f9-134">If **cExpanded** is equal to the number of categories, then the table is fully expanded.</span></span> 
  
<span data-ttu-id="986f9-135">Дополнительные сведения о стандартной и категоризации сортировки см. в этой [теме.](sorting-and-categorization.md)</span><span class="sxs-lookup"><span data-stu-id="986f9-135">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="986f9-136">См. также</span><span class="sxs-lookup"><span data-stu-id="986f9-136">See also</span></span>



[<span data-ttu-id="986f9-137">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="986f9-137">SSortOrder</span></span>](ssortorder.md)
  
[<span data-ttu-id="986f9-138">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="986f9-138">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="986f9-139">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="986f9-139">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)


[<span data-ttu-id="986f9-140">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="986f9-140">MAPI Structures</span></span>](mapi-structures.md)

