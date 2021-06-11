---
title: SSortOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSortOrder
api_type:
- COM
ms.assetid: fe181b9a-5903-4cc0-bcd5-2061b440b5b1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f9d38c90fa5795d34f78c61ce0faa5f76d8f740d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439725"
---
# <a name="ssortorder"></a><span data-ttu-id="aaf97-103">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="aaf97-103">SSortOrder</span></span>
 
<span data-ttu-id="aaf97-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aaf97-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aaf97-105">Определяет, как сортировать строки таблицы, какой столбец использовать в качестве ключа сортировки и направление сортировки.</span><span class="sxs-lookup"><span data-stu-id="aaf97-105">Defines how to sort the rows of a table, what column to use as the sort key, and the direction of the sort.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aaf97-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="aaf97-106">Header file:</span></span>  <br/> |<span data-ttu-id="aaf97-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aaf97-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSortOrder
{
  ULONG ulPropTag;
  ULONG ulOrder;
} SSortOrder, FAR *LPSSortOrder;

```

## <a name="members"></a><span data-ttu-id="aaf97-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="aaf97-108">Members</span></span>

<span data-ttu-id="aaf97-109">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="aaf97-109">**ulPropTag**</span></span>
  
> <span data-ttu-id="aaf97-110">Тег свойства, определяющий ключ сортировки или столбец категории.</span><span class="sxs-lookup"><span data-stu-id="aaf97-110">Property tag identifying the sort key or, for a categorized sort, the category column.</span></span>
    
<span data-ttu-id="aaf97-111">**ulOrder**</span><span class="sxs-lookup"><span data-stu-id="aaf97-111">**ulOrder**</span></span>
  
> <span data-ttu-id="aaf97-112">Порядок сортировки данных.</span><span class="sxs-lookup"><span data-stu-id="aaf97-112">The order in which the data is to be sorted.</span></span> <span data-ttu-id="aaf97-113">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="aaf97-113">Possible values are as follow:</span></span>
    
  - <span data-ttu-id="aaf97-114">TABLE_SORT_ASCEND. Таблица должна сортироваться в порядке восходящей.</span><span class="sxs-lookup"><span data-stu-id="aaf97-114">TABLE_SORT_ASCEND: The table should be sorted in ascending order.</span></span>
      
  - <span data-ttu-id="aaf97-115">TABLE_SORT_COMBINE. Операция сортировки должна создать категорию, которая объединяет свойство, указанное в качестве столбца ключа сортировки в члене **ulPropTag,** с столбцом ключа сортировки, указанным в предыдущей структуре **SSortOrder.**</span><span class="sxs-lookup"><span data-stu-id="aaf97-115">TABLE_SORT_COMBINE: The sort operation should create a category that combines the property identified as the sort key column in the **ulPropTag** member with the sort key column specified in the previous **SSortOrder** structure.</span></span> 
      
    <span data-ttu-id="aaf97-116">TABLE_SORT_COMBINE можно использовать только в том случае, если структура **SSortOrder** используется в качестве записи в [структуре SSortOrderSet](ssortorderset.md) для указания нескольких заказов сортировки для классифицировать сорт.</span><span class="sxs-lookup"><span data-stu-id="aaf97-116">TABLE_SORT_COMBINE can only be used when the **SSortOrder** structure is being used as an entry in an [SSortOrderSet](ssortorderset.md) structure to specify multiple sort orders for a categorized sort.</span></span> <span data-ttu-id="aaf97-117">TABLE_SORT_COMBINE не может использоваться в первой **структуре SSortOrder** в **структуре SSortOrderSet.**</span><span class="sxs-lookup"><span data-stu-id="aaf97-117">TABLE_SORT_COMBINE cannot be used in the first **SSortOrder** structure in an **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="aaf97-118">TABLE_SORT_DESCEND. Таблица должна сортироваться в порядке убывания.</span><span class="sxs-lookup"><span data-stu-id="aaf97-118">TABLE_SORT_DESCEND: The table should be sorted in descending order.</span></span>
      
  - <span data-ttu-id="aaf97-119">TABLE_SORT_CATEG_MAX. Таблица должна сортироваться по максимальному значению члена **ulPropTag** для строк данных в категориях, указанных в предыдущем порядке сортировки в структуре **SSortOrderSet.**</span><span class="sxs-lookup"><span data-stu-id="aaf97-119">TABLE_SORT_CATEG_MAX: The table should be sorted on the maximum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="aaf97-120">TABLE_SORT_CATEG_MIN. Таблица должна сортироваться на минимальном значении члена **ulPropTag** для строк данных в категориях, указанных в предыдущем порядке сортировки в структуре **SSortOrderSet.**</span><span class="sxs-lookup"><span data-stu-id="aaf97-120">TABLE_SORT_CATEG_MIN: The table should be sorted on the minimum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the in **SSortOrderSet** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="aaf97-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="aaf97-121">Remarks</span></span>

<span data-ttu-id="aaf97-122">Структура **SSortOrder используется** для описания выполнения стандартной операции сортировки или сортировки категории.</span><span class="sxs-lookup"><span data-stu-id="aaf97-122">An **SSortOrder** structure is used to describe how to perform either a standard sort operation or a categorized sort operation.</span></span> <span data-ttu-id="aaf97-123">**Структуры SSortOrder** обычно объединяются в **структуру SSortOrderSet** для описания нескольких ключей и направлений сортировки.</span><span class="sxs-lookup"><span data-stu-id="aaf97-123">**SSortOrder** structures are typically combined into an **SSortOrderSet** structure to describe multiple sort keys and directions.</span></span> <span data-ttu-id="aaf97-124">**Структуры SSortOrderSet** используются в следующих функциях и методах интерфейса:</span><span class="sxs-lookup"><span data-stu-id="aaf97-124">**SSortOrderSet** structures are used in the following functions and interface methods:</span></span> 
  
- [<span data-ttu-id="aaf97-125">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="aaf97-125">ITableData::HrGetView</span></span>](itabledata-hrgetview.md)
    
- [<span data-ttu-id="aaf97-126">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="aaf97-126">IMAPIFolder::SaveContentsSort</span></span>](imapifolder-savecontentssort.md)
    
- [<span data-ttu-id="aaf97-127">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="aaf97-127">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
    
- [<span data-ttu-id="aaf97-128">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="aaf97-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="aaf97-129">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="aaf97-129">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
- [<span data-ttu-id="aaf97-130">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="aaf97-130">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="aaf97-131">Диапазон разрешенных столбцов в таблице, которые можно использовать в качестве ключа сортировки, зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="aaf97-131">The range of allowed columns in a table that can be used as a sort key depends on the provider.</span></span> <span data-ttu-id="aaf97-132">Столбцы, которые являются частью текущего набора столбцов, всегда можно использовать в качестве ключей сортировки.</span><span class="sxs-lookup"><span data-stu-id="aaf97-132">Columns that are part of the current column set can always be used as sort keys.</span></span> <span data-ttu-id="aaf97-133">Однако каждый поставщик определяет, можно ли определить ключи сортировки с помощью доступных столбцов, которые не находятся в текущем наборе столбцов.</span><span class="sxs-lookup"><span data-stu-id="aaf97-133">However, each provider determines whether sort keys can be defined by using available columns that are not in the current column set.</span></span> <span data-ttu-id="aaf97-134">Доступный столбец — это столбец, возвращаемый из [IMAPITable::QueryColumns](imapitable-querycolumns.md) при TBL_ALL_COLUMNS флага.</span><span class="sxs-lookup"><span data-stu-id="aaf97-134">An available column is a column that is returned from [IMAPITable::QueryColumns](imapitable-querycolumns.md) when the TBL_ALL_COLUMNS flag is set.</span></span> 
  
<span data-ttu-id="aaf97-135">Член **ulOrder** указывает как сведения о направлении порядка, так и о категоризации, например, по разговору [(PidTagConversationTopic),](pidtagconversationtopic-canonical-property.md)то есть разговорной теме, которая является серией сообщений и ответов.</span><span class="sxs-lookup"><span data-stu-id="aaf97-135">The **ulOrder** member indicates both directional order and categorization information, for example, by conversation ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), that is, conversational thread, which is a series of messages and replies.</span></span> <span data-ttu-id="aaf97-136">Строки можно сортировать в последовательности восходящих или убывающих строк со всеми записями NULL, позиционными последними.</span><span class="sxs-lookup"><span data-stu-id="aaf97-136">Rows can be sorted in either an ascending or descending sequence with all NULL entries positioned last.</span></span> 
  
<span data-ttu-id="aaf97-137">Значение TABLE_SORT_COMBINE указывает, что столбец, указанный в **ulPropTag,** должен сочетаться с предыдущим столбцом категории для формирования сводной категории.</span><span class="sxs-lookup"><span data-stu-id="aaf97-137">The TABLE_SORT_COMBINE value indicates that the column specified in **ulPropTag** should be combined with the previous category column to form a composite category.</span></span> <span data-ttu-id="aaf97-138">То есть вместо классификации уникальных значений отдельных столбцов TABLE_SORT_COMBINE позволяет классифицовать уникальные значения сочетания столбцов.</span><span class="sxs-lookup"><span data-stu-id="aaf97-138">That is, instead of categorizing on unique values of individual columns, TABLE_SORT_COMBINE allows for categorization on unique values of a combination of columns.</span></span> <span data-ttu-id="aaf97-139">Например, можно определить одну категорию для групповых сообщений, полученных от конкретного отправитель по определенному вопросу.</span><span class="sxs-lookup"><span data-stu-id="aaf97-139">For example, a single category could be defined to group messages received from a particular sender on a particular subject.</span></span> <span data-ttu-id="aaf97-140">Настройка значения TABLE_SORT_COMBINE уменьшает количество отображаемого числа строк категории.</span><span class="sxs-lookup"><span data-stu-id="aaf97-140">Setting the value to TABLE_SORT_COMBINE reduces the number of category rows that are displayed.</span></span> 
  
<span data-ttu-id="aaf97-141">Сортировка на столбцах с несколькими значениями не поддерживается всеми реализации таблиц.</span><span class="sxs-lookup"><span data-stu-id="aaf97-141">Sorting on multi-valued columns is not universally supported by all table implementations.</span></span> <span data-ttu-id="aaf97-142">Если поддерживается, MV_FLAG с помощью макроса MVI_PROP к тегу свойств в члене **ulPropTag,** чтобы определить ключ сортировки как столбец с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="aaf97-142">If supported, apply the MV_FLAG using the MVI_PROP macro to the property tag in the **ulPropTag** member to identify the sort key as a multi-valued column.</span></span> <span data-ttu-id="aaf97-143">Сортировка в столбце с несколькими значениями основана на использовании отдельных значений.</span><span class="sxs-lookup"><span data-stu-id="aaf97-143">Sorting on a multi-valued column is based on using the individual values.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="aaf97-144">Значения **члена ulOrder** TABLE_SORT_CATEG_MAX и TABLE_SORT_CATEG_MIN могут быть не определены в загружаемом файле заголовки, который у вас сейчас есть, и в этом случае его можно добавить в код с помощью следующих значений: >  `#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span><span class="sxs-lookup"><span data-stu-id="aaf97-144">The **ulOrder** member values TABLE_SORT_CATEG_MAX and TABLE_SORT_CATEG_MIN might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span></span>
  
<span data-ttu-id="aaf97-145">Дополнительные сведения о стандартной и категоризации сортировки см. в [рубрике Сортировка и классификация.](sorting-and-categorization.md)</span><span class="sxs-lookup"><span data-stu-id="aaf97-145">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aaf97-146">См. также</span><span class="sxs-lookup"><span data-stu-id="aaf97-146">See also</span></span>

- [<span data-ttu-id="aaf97-147">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="aaf97-147">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="aaf97-148">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="aaf97-148">MAPI Structures</span></span>](mapi-structures.md)

