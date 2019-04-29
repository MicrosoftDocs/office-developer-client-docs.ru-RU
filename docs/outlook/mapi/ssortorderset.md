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
# <a name="ssortorderset"></a><span data-ttu-id="5f7e8-103">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="5f7e8-103">SSortOrderSet</span></span>

  
  
<span data-ttu-id="5f7e8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f7e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f7e8-105">Определяет коллекцию ключей сортировки для таблицы, используемой для сортировки по стандарту или по категориям.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-105">Defines a collection of sort keys for a table that is used for standard or categorized sorting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5f7e8-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5f7e8-106">Header file:</span></span>  <br/> |<span data-ttu-id="5f7e8-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="5f7e8-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5f7e8-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="5f7e8-108">Related macros:</span></span>  <br/> |<span data-ttu-id="5f7e8-109">[Кбневссортордерсет](cbnewssortorderset.md), [кбссортордерсет](cbssortorderset.md), [сизедссортордерсет](sizedssortorderset.md)</span><span class="sxs-lookup"><span data-stu-id="5f7e8-109">[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md)</span></span> <br/> |
   
```cpp
typedef struct _SSortOrderSet
{
  ULONG cSorts;
  ULONG cCategories;
  ULONG cExpanded;
  SSortOrder aSort[MAPI_DIM];
} SSortOrderSet, FAR *LPSSortOrderSet;

```

## <a name="members"></a><span data-ttu-id="5f7e8-110">Members</span><span class="sxs-lookup"><span data-stu-id="5f7e8-110">Members</span></span>

 <span data-ttu-id="5f7e8-111">**Ксортс**</span><span class="sxs-lookup"><span data-stu-id="5f7e8-111">**cSorts**</span></span>
  
> <span data-ttu-id="5f7e8-112">Количество структур [ссортордер](ssortorder.md) , включенных в элемент **асорт** .</span><span class="sxs-lookup"><span data-stu-id="5f7e8-112">Count of [SSortOrder](ssortorder.md) structures that are included in the **aSort** member.</span></span> 
    
 <span data-ttu-id="5f7e8-113">**Ккатегориес**</span><span class="sxs-lookup"><span data-stu-id="5f7e8-113">**cCategories**</span></span>
  
> <span data-ttu-id="5f7e8-114">Количество столбцов, назначенных столбцами категорий.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-114">Count of columns that are designated as category columns.</span></span> <span data-ttu-id="5f7e8-115">Диапазон допустимых значений — от нуля, что означает неклассифицированную или стандартную сортировку, с номером, указанным элементом **ксортс** .</span><span class="sxs-lookup"><span data-stu-id="5f7e8-115">Possible values range from zero, which indicates a non-categorized or standard sort, to the number indicated by the **cSorts** member.</span></span> 
    
 <span data-ttu-id="5f7e8-116">**Цекспандед**</span><span class="sxs-lookup"><span data-stu-id="5f7e8-116">**cExpanded**</span></span>
  
> <span data-ttu-id="5f7e8-117">Количество категорий, которые начинаются в развернутом состоянии, и все строки, которые применяются к этой категории, отображаются в табличном представлении.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-117">Count of categories that start in an expanded state, where all of the rows that apply to the category are visible in the table view.</span></span> <span data-ttu-id="5f7e8-118">Возможные значения находятся в диапазоне от 0 до числа, указанного в **ккатегориес**.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-118">Possible values range from 0 to the number indicated by **cCategories**.</span></span>
    
 <span data-ttu-id="5f7e8-119">**асорт**</span><span class="sxs-lookup"><span data-stu-id="5f7e8-119">**aSort**</span></span>
  
> <span data-ttu-id="5f7e8-120">Массив структур **ссортордер** , каждый из которых определяет порядок сортировки.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-120">Array of **SSortOrder** structures, each defining a sort order.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5f7e8-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="5f7e8-121">Remarks</span></span>

<span data-ttu-id="5f7e8-122">Структура **ссортордерсет** используется для определения нескольких порядков сортировки для стандартной и упорядоченной сортировки.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-122">A **SSortOrderSet** structure is used for defining multiple sort orders for standard and categorized sorting.</span></span> 
  
<span data-ttu-id="5f7e8-123">Каждая структура **ссортордерсет** содержит по крайней мере одну структуру **ссортордер** , определяющую направление сортировки и столбец, который будет использоваться в качестве ключа сортировки.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-123">Each **SSortOrderSet** structure contains at least one **SSortOrder** structure defining the direction of the sort and the column that will be used as the sort key.</span></span> <span data-ttu-id="5f7e8-124">Для сортировки по категориям этот столбец используется в качестве категории.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-124">For categorized sorting, this column is used as the category.</span></span> <span data-ttu-id="5f7e8-125">Когда значение члена **ксортс** превышает значение члена **ккатегориес** , по сравнению со категориями создаются дополнительные ключи сортировки, а категории — из столбцов, которые отображаются первыми в массиве **ссортордер** .</span><span class="sxs-lookup"><span data-stu-id="5f7e8-125">When the value of the **cSorts** member exceeds the value of the **cCategories** member, there are more sort keys than categories, and categories are created from the columns that appear first in the **SSortOrder** array.</span></span> 
  
<span data-ttu-id="5f7e8-126">Например, если для **ксортс** задано значение 3, а для **ккатегориес** задано значение 2, в качестве столбцов категории используются столбцы, описываемые элементом **улпроптаг** первых двух записей в массиве **ссортордер** .</span><span class="sxs-lookup"><span data-stu-id="5f7e8-126">For example, if **cSorts** is set to 3 and **cCategories** is set to 2, the columns described by the **ulPropTag** member of the first two entries in the **SSortOrder** array are used as the category columns.</span></span> <span data-ttu-id="5f7e8-127">Первая запись выступает в качестве группирования категорий верхнего уровня; Вторая запись в качестве дополнительной группировки.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-127">The first entry serves as the top-level category grouping; the second entry as the secondary grouping.</span></span> <span data-ttu-id="5f7e8-128">Все строки, которые совпадают с двумя столбцами категорий, сортируются по ключу сортировки, определенному в третьей записи.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-128">All of the rows that match the two category columns are sorted by using the sort key defined in the third entry.</span></span> 
  
<span data-ttu-id="5f7e8-129">Член **цекспандед** указывает количество первых развернутых категорий.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-129">The **cExpanded** member specifies the number of categories that are at first expanded.</span></span> <span data-ttu-id="5f7e8-130">При наличии нескольких категорий реализация таблицы начинается с первого столбца, который назначается в качестве категории, и продолжается в последовательном порядке с последующими столбцами категорий до тех пор, пока не будет превышено число **ккатегориес** .</span><span class="sxs-lookup"><span data-stu-id="5f7e8-130">When there are multiple categories, the table implementation starts with the first column to be designated as a category and continues in sequential order with the subsequent category columns until the number of **cCategories** has been exceeded.</span></span> <span data-ttu-id="5f7e8-131">Если столбцов категорий больше, чем в развернутых столбцах, столбцы категорий свернуты.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-131">If there are more category columns than there are expanded columns, the category columns are collapsed.</span></span> <span data-ttu-id="5f7e8-132">Если **цекспандед** имеет значение 0, только строка заголовка верхнего уровня доступна пользователю таблицы для отображения.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-132">If **cExpanded** is equal to zero, only the top level heading row is available to the table user for display.</span></span> <span data-ttu-id="5f7e8-133">Если **цекспандед** равен единице, меньшему числу категорий, то все строки заголовков и конечные строки недоступны.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-133">If **cExpanded** is equal to one less than the number of categories, then all of the heading rows and none of the leaf rows are available.</span></span> <span data-ttu-id="5f7e8-134">Если **цекспандед** равно числу категорий, таблица полностью разворачивается.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-134">If **cExpanded** is equal to the number of categories, then the table is fully expanded.</span></span> 
  
<span data-ttu-id="5f7e8-135">Дополнительные сведения о стандартной и упорядоченной сортировке приведены в разделе [Сортировка и категоризация](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="5f7e8-135">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5f7e8-136">См. также</span><span class="sxs-lookup"><span data-stu-id="5f7e8-136">See also</span></span>



[<span data-ttu-id="5f7e8-137">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="5f7e8-137">SSortOrder</span></span>](ssortorder.md)
  
[<span data-ttu-id="5f7e8-138">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="5f7e8-138">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="5f7e8-139">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="5f7e8-139">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)


[<span data-ttu-id="5f7e8-140">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="5f7e8-140">MAPI Structures</span></span>](mapi-structures.md)

