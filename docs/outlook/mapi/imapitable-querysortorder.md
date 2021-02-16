---
title: IMAPITableQuerySortOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QuerySortOrder
api_type:
- COM
ms.assetid: 7b4ca523-0703-417c-8586-c4324c200020
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 61991972fdf8674a9ffd2b790e26c7fa669df357
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407552"
---
# <a name="imapitablequerysortorder"></a><span data-ttu-id="0614b-103">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="0614b-103">IMAPITable::QuerySortOrder</span></span>

  
  
<span data-ttu-id="0614b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0614b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0614b-105">Извлекает текущий порядок сортировки для таблицы.</span><span class="sxs-lookup"><span data-stu-id="0614b-105">Retrieves the current sort order for a table.</span></span>
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a><span data-ttu-id="0614b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0614b-106">Parameters</span></span>

 <span data-ttu-id="0614b-107">_lppSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="0614b-107">_lppSortCriteria_</span></span>
  
> <span data-ttu-id="0614b-108">[out] Указатель на указатель на структуру [SSortOrderSet, удерживая](ssortorderset.md) текущий порядок сортировки.</span><span class="sxs-lookup"><span data-stu-id="0614b-108">[out] Pointer to a pointer to the [SSortOrderSet](ssortorderset.md) structure holding the current sort order.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0614b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0614b-109">Return value</span></span>

<span data-ttu-id="0614b-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="0614b-110">S_OK</span></span> 
  
> <span data-ttu-id="0614b-111">Текущий порядок сортировки был успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="0614b-111">The current sort order was successfully returned.</span></span>
    
<span data-ttu-id="0614b-112">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="0614b-112">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="0614b-113">В настоящее время идет другая операция, которая препятствует запуску операции и получения порядка сортировки.</span><span class="sxs-lookup"><span data-stu-id="0614b-113">Another operation is in progress that prevents the sort order retrieval operation from starting.</span></span> <span data-ttu-id="0614b-114">Либо операция должна быть завершена, либо она должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="0614b-114">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0614b-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="0614b-115">Remarks</span></span>

<span data-ttu-id="0614b-116">Метод **IMAPITable::QuerySortOrder** извлекает текущий порядок сортировки для таблицы.</span><span class="sxs-lookup"><span data-stu-id="0614b-116">The **IMAPITable::QuerySortOrder** method retrieves the current sort order for a table.</span></span> <span data-ttu-id="0614b-117">Заказы сортировки описываются в структуре [SSortOrderSet.](ssortorderset.md)</span><span class="sxs-lookup"><span data-stu-id="0614b-117">Sort orders are described with an [SSortOrderSet](ssortorderset.md) structure.</span></span> 
  
- <span data-ttu-id="0614b-118">Для **члена cSorts** структуры **SSortOrderSet** можно установить нулевое значение, если:</span><span class="sxs-lookup"><span data-stu-id="0614b-118">The **cSorts** member of the **SSortOrderSet** structure can be set to zero if:</span></span> 
    
- <span data-ttu-id="0614b-119">Таблица не отсортна.</span><span class="sxs-lookup"><span data-stu-id="0614b-119">The table is unsorted.</span></span>
    
- <span data-ttu-id="0614b-120">Сведения о сортировке таблицы не имеются.</span><span class="sxs-lookup"><span data-stu-id="0614b-120">There is no information about how the table is sorted.</span></span>
    
- <span data-ttu-id="0614b-121">Структура **SSortOrderSet** не подходит для описания порядка сортировки.</span><span class="sxs-lookup"><span data-stu-id="0614b-121">The **SSortOrderSet** structure is not appropriate for describing the sort order.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="0614b-122">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="0614b-122">Notes to implementers</span></span>

<span data-ttu-id="0614b-123">При вызове метода [IMAPITable::SortTable](imapitable-sorttable.md) со структурой **SSortOrderSet,** содержащей ноль столбцов в ключе сортировки, удалите текущий порядок сортировки и примените порядок по умолчанию, если он существует.</span><span class="sxs-lookup"><span data-stu-id="0614b-123">If a call is made to your [IMAPITable::SortTable](imapitable-sorttable.md) method with an **SSortOrderSet** structure containing zero columns in the sort key, remove the current sort order and apply the default order, if there is one.</span></span> <span data-ttu-id="0614b-124">В последующих вызовах **QuerySortOrder** можно выбрать, возвращать ли ноль или больше столбцов для ключа сортировки.</span><span class="sxs-lookup"><span data-stu-id="0614b-124">In subsequent calls to **QuerySortOrder**, you can choose whether to return zero or more columns for the sort key.</span></span> <span data-ttu-id="0614b-125">Вы можете вернуть больше столбцов, чем в настоящем представлении.</span><span class="sxs-lookup"><span data-stu-id="0614b-125">You can return more columns than are in the present view.</span></span>
  
<span data-ttu-id="0614b-126">Дополнительные сведения о сортировке см. в [теме "Сортировка и классификация".](sorting-and-categorization.md)</span><span class="sxs-lookup"><span data-stu-id="0614b-126">For more information about sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0614b-127">См. также</span><span class="sxs-lookup"><span data-stu-id="0614b-127">See also</span></span>



[<span data-ttu-id="0614b-128">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="0614b-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="0614b-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="0614b-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="0614b-130">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="0614b-130">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="0614b-131">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0614b-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

