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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344550"
---
# <a name="ssortorder"></a><span data-ttu-id="a0e37-103">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="a0e37-103">SSortOrder</span></span>
 
<span data-ttu-id="a0e37-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0e37-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0e37-105">Определяет порядок сортировки строк таблицы, столбец, который будет использоваться в качестве ключа сортировки, а также направление сортировки.</span><span class="sxs-lookup"><span data-stu-id="a0e37-105">Defines how to sort the rows of a table, what column to use as the sort key, and the direction of the sort.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0e37-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a0e37-106">Header file:</span></span>  <br/> |<span data-ttu-id="a0e37-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="a0e37-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSortOrder
{
  ULONG ulPropTag;
  ULONG ulOrder;
} SSortOrder, FAR *LPSSortOrder;

```

## <a name="members"></a><span data-ttu-id="a0e37-108">Members</span><span class="sxs-lookup"><span data-stu-id="a0e37-108">Members</span></span>

<span data-ttu-id="a0e37-109">**Улпроптаг**</span><span class="sxs-lookup"><span data-stu-id="a0e37-109">**ulPropTag**</span></span>
  
> <span data-ttu-id="a0e37-110">Тег свойства, определяющий ключ сортировки или, для столбца категорий, для сортировки по категориям.</span><span class="sxs-lookup"><span data-stu-id="a0e37-110">Property tag identifying the sort key or, for a categorized sort, the category column.</span></span>
    
<span data-ttu-id="a0e37-111">**Улордер**</span><span class="sxs-lookup"><span data-stu-id="a0e37-111">**ulOrder**</span></span>
  
> <span data-ttu-id="a0e37-112">Порядок сортировки данных.</span><span class="sxs-lookup"><span data-stu-id="a0e37-112">The order in which the data is to be sorted.</span></span> <span data-ttu-id="a0e37-113">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="a0e37-113">Possible values are as follow:</span></span>
    
  - <span data-ttu-id="a0e37-114">ТАБЛЕ_СОРТ_АСЦЕНД: таблица должна быть отсортирована в возрастающем порядке.</span><span class="sxs-lookup"><span data-stu-id="a0e37-114">TABLE_SORT_ASCEND: The table should be sorted in ascending order.</span></span>
      
  - <span data-ttu-id="a0e37-115">ТАБЛЕ_СОРТ_КОМБИНЕ: операция Sort должна создать категорию, объединяющую свойство, определенное как столбец ключа сортировки в элементе **улпроптаг** , с ключевым столбцом сортировки, указанным в предыдущей структуре **ссортордер** .</span><span class="sxs-lookup"><span data-stu-id="a0e37-115">TABLE_SORT_COMBINE: The sort operation should create a category that combines the property identified as the sort key column in the **ulPropTag** member with the sort key column specified in the previous **SSortOrder** structure.</span></span> 
      
    <span data-ttu-id="a0e37-116">ТАБЛЕ_СОРТ_КОМБИНЕ можно использовать только в том случае, если структура **ссортордер** используется в качестве записи в структуре [ссортордерсет](ssortorderset.md) , чтобы указать несколько порядков сортировки для сортировки по категориям.</span><span class="sxs-lookup"><span data-stu-id="a0e37-116">TABLE_SORT_COMBINE can only be used when the **SSortOrder** structure is being used as an entry in an [SSortOrderSet](ssortorderset.md) structure to specify multiple sort orders for a categorized sort.</span></span> <span data-ttu-id="a0e37-117">ТАБЛЕ_СОРТ_КОМБИНЕ не может использоваться в первой структуре **ссортордер** в структуре **ссортордерсет** .</span><span class="sxs-lookup"><span data-stu-id="a0e37-117">TABLE_SORT_COMBINE cannot be used in the first **SSortOrder** structure in an **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="a0e37-118">ТАБЛЕ_СОРТ_ДЕСЦЕНД: таблица должна быть отсортирована в убывающем порядке.</span><span class="sxs-lookup"><span data-stu-id="a0e37-118">TABLE_SORT_DESCEND: The table should be sorted in descending order.</span></span>
      
  - <span data-ttu-id="a0e37-119">ТАБЛЕ_СОРТ_КАТЕГ_МАКС: таблица должна быть отсортирована по максимальному значению элемента **улпроптаг** для строк данных в категориях, указанных в предыдущем порядке сортировки в структуре **ссортордерсет** .</span><span class="sxs-lookup"><span data-stu-id="a0e37-119">TABLE_SORT_CATEG_MAX: The table should be sorted on the maximum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="a0e37-120">ТАБЛЕ_СОРТ_КАТЕГ_МИН: таблица должна быть отсортирована по минимальному значению элемента **улпроптаг** для строк данных в категориях, указанных в предыдущем порядке сортировки в структуре in **ссортордерсет** .</span><span class="sxs-lookup"><span data-stu-id="a0e37-120">TABLE_SORT_CATEG_MIN: The table should be sorted on the minimum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the in **SSortOrderSet** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a0e37-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0e37-121">Remarks</span></span>

<span data-ttu-id="a0e37-122">Структура **ссортордер** используется для описания способов выполнения стандартной или операции сортировки по категориям.</span><span class="sxs-lookup"><span data-stu-id="a0e37-122">An **SSortOrder** structure is used to describe how to perform either a standard sort operation or a categorized sort operation.</span></span> <span data-ttu-id="a0e37-123">Структуры **ссортордер** обычно объединяются в структуру **ссортордерсет** , чтобы описать несколько ключей сортировки и инструкций.</span><span class="sxs-lookup"><span data-stu-id="a0e37-123">**SSortOrder** structures are typically combined into an **SSortOrderSet** structure to describe multiple sort keys and directions.</span></span> <span data-ttu-id="a0e37-124">Структуры **ссортордерсет** используются в следующих функциях и методах интерфейса:</span><span class="sxs-lookup"><span data-stu-id="a0e37-124">**SSortOrderSet** structures are used in the following functions and interface methods:</span></span> 
  
- [<span data-ttu-id="a0e37-125">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="a0e37-125">ITableData::HrGetView</span></span>](itabledata-hrgetview.md)
    
- [<span data-ttu-id="a0e37-126">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="a0e37-126">IMAPIFolder::SaveContentsSort</span></span>](imapifolder-savecontentssort.md)
    
- [<span data-ttu-id="a0e37-127">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="a0e37-127">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
    
- [<span data-ttu-id="a0e37-128">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="a0e37-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="a0e37-129">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="a0e37-129">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
- [<span data-ttu-id="a0e37-130">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="a0e37-130">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="a0e37-131">Диапазон разрешенных столбцов таблицы, который можно использовать в качестве ключа сортировки, зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="a0e37-131">The range of allowed columns in a table that can be used as a sort key depends on the provider.</span></span> <span data-ttu-id="a0e37-132">Столбцы, которые входят в текущий набор столбцов, всегда могут использоваться в качестве ключей сортировки.</span><span class="sxs-lookup"><span data-stu-id="a0e37-132">Columns that are part of the current column set can always be used as sort keys.</span></span> <span data-ttu-id="a0e37-133">Однако каждый поставщик определяет, могут ли клавиши сортировки определяться с помощью доступных столбцов, которые не входят в текущий набор столбцов.</span><span class="sxs-lookup"><span data-stu-id="a0e37-133">However, each provider determines whether sort keys can be defined by using available columns that are not in the current column set.</span></span> <span data-ttu-id="a0e37-134">Доступный столбец — это столбец, который возвращается из [IMAPITable:: куериколумнс](imapitable-querycolumns.md) , если установлен флаг тбл_алл_колумнс.</span><span class="sxs-lookup"><span data-stu-id="a0e37-134">An available column is a column that is returned from [IMAPITable::QueryColumns](imapitable-querycolumns.md) when the TBL_ALL_COLUMNS flag is set.</span></span> 
  
<span data-ttu-id="a0e37-135">Элемент **улордер** указывает как направленный порядок, так и сведения о классификации, например, по беседе ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), то есть поток бесед, представляющий собой серию сообщений и ответов.</span><span class="sxs-lookup"><span data-stu-id="a0e37-135">The **ulOrder** member indicates both directional order and categorization information, for example, by conversation ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), that is, conversational thread, which is a series of messages and replies.</span></span> <span data-ttu-id="a0e37-136">Строки можно сортировать как в порядке возрастания, так и в порядке убывания со всеми записями NULL, расположенными в последний раз.</span><span class="sxs-lookup"><span data-stu-id="a0e37-136">Rows can be sorted in either an ascending or descending sequence with all NULL entries positioned last.</span></span> 
  
<span data-ttu-id="a0e37-137">Значение ТАБЛЕ_СОРТ_КОМБИНЕ указывает на то, что столбец, указанный в **улпроптаг** , следует объединить с предыдущим столбцом Category, чтобы сформировать составную категорию.</span><span class="sxs-lookup"><span data-stu-id="a0e37-137">The TABLE_SORT_COMBINE value indicates that the column specified in **ulPropTag** should be combined with the previous category column to form a composite category.</span></span> <span data-ttu-id="a0e37-138">То есть вместо категоризации по уникальным значениям отдельных столбцов ТАБЛЕ_СОРТ_КОМБИНЕ позволяет выполнять категоризацию по уникальным значениям комбинации столбцов.</span><span class="sxs-lookup"><span data-stu-id="a0e37-138">That is, instead of categorizing on unique values of individual columns, TABLE_SORT_COMBINE allows for categorization on unique values of a combination of columns.</span></span> <span data-ttu-id="a0e37-139">Например, можно определить одну категорию, чтобы сгруппировать сообщения, полученные от конкретного отправителя для определенной темы.</span><span class="sxs-lookup"><span data-stu-id="a0e37-139">For example, a single category could be defined to group messages received from a particular sender on a particular subject.</span></span> <span data-ttu-id="a0e37-140">Если задать для параметра значение ТАБЛЕ_СОРТ_КОМБИНЕ, будет уменьшено количество отображаемых строк категорий.</span><span class="sxs-lookup"><span data-stu-id="a0e37-140">Setting the value to TABLE_SORT_COMBINE reduces the number of category rows that are displayed.</span></span> 
  
<span data-ttu-id="a0e37-141">Сортировка по многозначным столбцам не поддерживается всеми реализациями таблиц.</span><span class="sxs-lookup"><span data-stu-id="a0e37-141">Sorting on multi-valued columns is not universally supported by all table implementations.</span></span> <span data-ttu-id="a0e37-142">Если это поддерживается, примените МВ_ФЛАГ с помощью макроса МВИ_ПРОП к тегу свойства в элементе **улпроптаг** , чтобы идентифицировать ключ сортировки как многозначный столбец.</span><span class="sxs-lookup"><span data-stu-id="a0e37-142">If supported, apply the MV_FLAG using the MVI_PROP macro to the property tag in the **ulPropTag** member to identify the sort key as a multi-valued column.</span></span> <span data-ttu-id="a0e37-143">Сортировка по многозначному столбцу основана на использовании отдельных значений.</span><span class="sxs-lookup"><span data-stu-id="a0e37-143">Sorting on a multi-valued column is based on using the individual values.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="a0e37-144">Значения членов **УЛОРДЕР** ТАБЛЕ_СОРТ_КАТЕГ_МАКС и табле_сорт_катег_мин могут не определяться в файле заголовков, доступных для загрузки, в этом случае можно добавить его в код, используя следующие значения: _гт_`#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span><span class="sxs-lookup"><span data-stu-id="a0e37-144">The **ulOrder** member values TABLE_SORT_CATEG_MAX and TABLE_SORT_CATEG_MIN might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span></span>
  
<span data-ttu-id="a0e37-145">Дополнительные сведения о стандартной и упорядоченной сортировке приведены в разделе [Сортировка и категоризация](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="a0e37-145">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a0e37-146">См. также</span><span class="sxs-lookup"><span data-stu-id="a0e37-146">See also</span></span>

- [<span data-ttu-id="a0e37-147">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="a0e37-147">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="a0e37-148">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="a0e37-148">MAPI Structures</span></span>](mapi-structures.md)

