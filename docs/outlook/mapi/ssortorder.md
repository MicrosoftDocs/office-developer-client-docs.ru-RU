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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 7cb511c7a021c4e65214acc7efa785be0e02ffc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812376"
---
# <a name="ssortorder"></a><span data-ttu-id="7275f-103">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="7275f-103">SSortOrder</span></span>
 
<span data-ttu-id="7275f-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7275f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7275f-105">Определяет порядок сортировки строк таблицы, в каких столбцов для использования в качестве ключа сортировки и направление сортировки.</span><span class="sxs-lookup"><span data-stu-id="7275f-105">Defines how to sort the rows of a table, what column to use as the sort key, and the direction of the sort.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7275f-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="7275f-106">Header file:</span></span>  <br/> |<span data-ttu-id="7275f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7275f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSortOrder
{
  ULONG ulPropTag;
  ULONG ulOrder;
} SSortOrder, FAR *LPSSortOrder;

```

## <a name="members"></a><span data-ttu-id="7275f-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="7275f-108">Members</span></span>

<span data-ttu-id="7275f-109">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="7275f-109">**ulPropTag**</span></span>
  
> <span data-ttu-id="7275f-110">Свойство tag идентифицирующий сортировки ключа или, для сортировки по категориям, в столбце категории.</span><span class="sxs-lookup"><span data-stu-id="7275f-110">Property tag identifying the sort key or, for a categorized sort, the category column.</span></span>
    
<span data-ttu-id="7275f-111">**ulOrder**</span><span class="sxs-lookup"><span data-stu-id="7275f-111">**ulOrder**</span></span>
  
> <span data-ttu-id="7275f-112">Порядок, в котором будет сортировать данные.</span><span class="sxs-lookup"><span data-stu-id="7275f-112">The order in which the data is to be sorted.</span></span> <span data-ttu-id="7275f-113">Возможны следующие возможные значения:</span><span class="sxs-lookup"><span data-stu-id="7275f-113">Possible values are as follow:</span></span>
    
  - <span data-ttu-id="7275f-114">TABLE_SORT_ASCEND: Таблицы будут сортироваться в восходящем порядке.</span><span class="sxs-lookup"><span data-stu-id="7275f-114">TABLE_SORT_ASCEND: The table should be sorted in ascending order.</span></span>
      
  - <span data-ttu-id="7275f-115">TABLE_SORT_COMBINE: Сортировку следует создать категории, который объединяет свойства, определенные как столбец сортировки в член **ulPropTag** со столбцом ключа сортировки, указанной в предыдущем структуры **SSortOrder** .</span><span class="sxs-lookup"><span data-stu-id="7275f-115">TABLE_SORT_COMBINE: The sort operation should create a category that combines the property identified as the sort key column in the **ulPropTag** member with the sort key column specified in the previous **SSortOrder** structure.</span></span> 
      
    <span data-ttu-id="7275f-116">TABLE_SORT_COMBINE может использоваться только в тех случаях, когда структура **SSortOrder** , используется как записи в структуре [SSortOrderSet](ssortorderset.md) для указания нескольких порядок сортировки для сортировки по категориям.</span><span class="sxs-lookup"><span data-stu-id="7275f-116">TABLE_SORT_COMBINE can only be used when the **SSortOrder** structure is being used as an entry in an [SSortOrderSet](ssortorderset.md) structure to specify multiple sort orders for a categorized sort.</span></span> <span data-ttu-id="7275f-117">TABLE_SORT_COMBINE не может использоваться в структуре первого **SSortOrder** в структуре **SSortOrderSet** .</span><span class="sxs-lookup"><span data-stu-id="7275f-117">TABLE_SORT_COMBINE cannot be used in the first **SSortOrder** structure in an **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="7275f-118">TABLE_SORT_DESCEND: Таблицы будут сортироваться по убыванию.</span><span class="sxs-lookup"><span data-stu-id="7275f-118">TABLE_SORT_DESCEND: The table should be sorted in descending order.</span></span>
      
  - <span data-ttu-id="7275f-119">TABLE_SORT_CATEG_MAX: Таблицы будут сортироваться на максимальное значение элемента **ulPropTag** строк данных в категории, указанный с предыдущей порядок сортировки в структуре **SSortOrderSet** .</span><span class="sxs-lookup"><span data-stu-id="7275f-119">TABLE_SORT_CATEG_MAX: The table should be sorted on the maximum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="7275f-120">TABLE_SORT_CATEG_MIN: Таблицы будут сортироваться на минимальное значение члена **ulPropTag** строк данных в категории, указанный с предыдущей порядок сортировки в структуре в **SSortOrderSet** .</span><span class="sxs-lookup"><span data-stu-id="7275f-120">TABLE_SORT_CATEG_MIN: The table should be sorted on the minimum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the in **SSortOrderSet** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7275f-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="7275f-121">Remarks</span></span>

<span data-ttu-id="7275f-122">Структура **SSortOrder** используется описывается, как выполнять стандартные сортировку или сортировку по категориям.</span><span class="sxs-lookup"><span data-stu-id="7275f-122">An **SSortOrder** structure is used to describe how to perform either a standard sort operation or a categorized sort operation.</span></span> <span data-ttu-id="7275f-123">**SSortOrder** структуры обычно объединяются в структуру **SSortOrderSet** для описания нескольких ключей сортировки и инструкции по панелям.</span><span class="sxs-lookup"><span data-stu-id="7275f-123">**SSortOrder** structures are typically combined into an **SSortOrderSet** structure to describe multiple sort keys and directions.</span></span> <span data-ttu-id="7275f-124">**SSortOrderSet** структуры используются следующие функции и методы интерфейса:</span><span class="sxs-lookup"><span data-stu-id="7275f-124">**SSortOrderSet** structures are used in the following functions and interface methods:</span></span> 
  
- [<span data-ttu-id="7275f-125">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="7275f-125">ITableData::HrGetView</span></span>](itabledata-hrgetview.md)
    
- [<span data-ttu-id="7275f-126">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="7275f-126">IMAPIFolder::SaveContentsSort</span></span>](imapifolder-savecontentssort.md)
    
- [<span data-ttu-id="7275f-127">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="7275f-127">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
    
- [<span data-ttu-id="7275f-128">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="7275f-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="7275f-129">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="7275f-129">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
- [<span data-ttu-id="7275f-130">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="7275f-130">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="7275f-131">Диапазон допустимых столбцов в таблице, можно использовать в качестве ключа сортировки зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="7275f-131">The range of allowed columns in a table that can be used as a sort key depends on the provider.</span></span> <span data-ttu-id="7275f-132">Столбцы, которые являются частью текущего набора столбца всегда можно использовать в качестве ключей сортировки.</span><span class="sxs-lookup"><span data-stu-id="7275f-132">Columns that are part of the current column set can always be used as sort keys.</span></span> <span data-ttu-id="7275f-133">Тем не менее каждый поставщик определяет ли ключи сортировки может быть определен с помощью доступные столбцы, не в текущем столбце заданные.</span><span class="sxs-lookup"><span data-stu-id="7275f-133">However, each provider determines whether sort keys can be defined by using available columns that are not in the current column set.</span></span> <span data-ttu-id="7275f-134">Необходимые столбцы — это столбец, который возвращается из [IMAPITable::QueryColumns](imapitable-querycolumns.md) при установке флага TBL_ALL_COLUMNS.</span><span class="sxs-lookup"><span data-stu-id="7275f-134">An available column is a column that is returned from [IMAPITable::QueryColumns](imapitable-querycolumns.md) when the TBL_ALL_COLUMNS flag is set.</span></span> 
  
<span data-ttu-id="7275f-135">Элемент **ulOrder** указывает направления порядке и сведения о категоризации, например по беседе ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), то есть естественного поток, который представляет собой ряд сообщения и ответы.</span><span class="sxs-lookup"><span data-stu-id="7275f-135">The **ulOrder** member indicates both directional order and categorization information, for example, by conversation ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), that is, conversational thread, which is a series of messages and replies.</span></span> <span data-ttu-id="7275f-136">Можно сортировать строки в по возрастанию или по убыванию последовательность все операции NULL, размещенный последнего.</span><span class="sxs-lookup"><span data-stu-id="7275f-136">Rows can be sorted in either an ascending or descending sequence with all NULL entries positioned last.</span></span> 
  
<span data-ttu-id="7275f-137">Значение TABLE_SORT_COMBINE указывает, что столбец, указанный в **ulPropTag** следует использовать в сочетании с предыдущего столбца категории для формирования составных категории.</span><span class="sxs-lookup"><span data-stu-id="7275f-137">The TABLE_SORT_COMBINE value indicates that the column specified in **ulPropTag** should be combined with the previous category column to form a composite category.</span></span> <span data-ttu-id="7275f-138">То есть вместо классификации на уникальные значения отдельных столбцов TABLE_SORT_COMBINE обеспечивает классификации на уникальные значения сочетание столбцов.</span><span class="sxs-lookup"><span data-stu-id="7275f-138">That is, instead of categorizing on unique values of individual columns, TABLE_SORT_COMBINE allows for categorization on unique values of a combination of columns.</span></span> <span data-ttu-id="7275f-139">Например, для одной категории можно задать для группы сообщений, полученных от конкретного отправителя на конкретной темы.</span><span class="sxs-lookup"><span data-stu-id="7275f-139">For example, a single category could be defined to group messages received from a particular sender on a particular subject.</span></span> <span data-ttu-id="7275f-140">Значение TABLE_SORT_COMBINE уменьшает количество отображаемых строк категории.</span><span class="sxs-lookup"><span data-stu-id="7275f-140">Setting the value to TABLE_SORT_COMBINE reduces the number of category rows that are displayed.</span></span> 
  
<span data-ttu-id="7275f-141">Сортировка на многозначные столбцы не поддерживается универсального реализациями таблицы.</span><span class="sxs-lookup"><span data-stu-id="7275f-141">Sorting on multi-valued columns is not universally supported by all table implementations.</span></span> <span data-ttu-id="7275f-142">Если поддерживается, применяются MV_FLAG, использование макрос MVI_PROP для тега свойства участника **ulPropTag** для идентификации ключа сортировки в виде многозначных столбцов.</span><span class="sxs-lookup"><span data-stu-id="7275f-142">If supported, apply the MV_FLAG using the MVI_PROP macro to the property tag in the **ulPropTag** member to identify the sort key as a multi-valued column.</span></span> <span data-ttu-id="7275f-143">Сортировка по столбцу с несколькими значениями основано на использование отдельных значений.</span><span class="sxs-lookup"><span data-stu-id="7275f-143">Sorting on a multi-valued column is based on using the individual values.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="7275f-144">Значения элементов **ulOrder** , TABLE_SORT_CATEG_MAX и TABLE_SORT_CATEG_MIN не может быть определен в файле загружаемых заголовка имеется в настоящее время, в противном случае ее можно добавить в код, используя следующие значения: >`#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span><span class="sxs-lookup"><span data-stu-id="7275f-144">The **ulOrder** member values TABLE_SORT_CATEG_MAX and TABLE_SORT_CATEG_MIN might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span></span>
  
<span data-ttu-id="7275f-145">Дополнительные сведения о стандартных и по категориям сортировка см [категоризации](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="7275f-145">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7275f-146">См. также</span><span class="sxs-lookup"><span data-stu-id="7275f-146">See also</span></span>

- [<span data-ttu-id="7275f-147">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="7275f-147">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="7275f-148">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="7275f-148">MAPI Structures</span></span>](mapi-structures.md)

