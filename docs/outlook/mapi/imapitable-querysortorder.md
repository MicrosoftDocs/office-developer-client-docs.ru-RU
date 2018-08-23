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
ms.openlocfilehash: 48ca692779fb53cab386d8a18b5f0a50e11d531c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569437"
---
# <a name="imapitablequerysortorder"></a><span data-ttu-id="c7418-103">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="c7418-103">IMAPITable::QuerySortOrder</span></span>

  
  
<span data-ttu-id="c7418-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7418-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7418-105">Получает текущий порядок сортировки для таблицы.</span><span class="sxs-lookup"><span data-stu-id="c7418-105">Retrieves the current sort order for a table.</span></span>
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a><span data-ttu-id="c7418-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7418-106">Parameters</span></span>

 <span data-ttu-id="c7418-107">_lppSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="c7418-107">_lppSortCriteria_</span></span>
  
> <span data-ttu-id="c7418-108">[out] Указатель на указатель на структуру [SSortOrderSet](ssortorderset.md) , содержащую текущий порядок сортировки.</span><span class="sxs-lookup"><span data-stu-id="c7418-108">[out] Pointer to a pointer to the [SSortOrderSet](ssortorderset.md) structure holding the current sort order.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c7418-109">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="c7418-109">Return value</span></span>

<span data-ttu-id="c7418-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="c7418-110">S_OK</span></span> 
  
> <span data-ttu-id="c7418-111">Порядок сортировки успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="c7418-111">The current sort order was successfully returned.</span></span>
    
<span data-ttu-id="c7418-112">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="c7418-112">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="c7418-113">В, не позволяющей операции извлечения порядок сортировки запуск выполняется другой операции.</span><span class="sxs-lookup"><span data-stu-id="c7418-113">Another operation is in progress that prevents the sort order retrieval operation from starting.</span></span> <span data-ttu-id="c7418-114">В процессе выполнения операции должны выполнить либо должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="c7418-114">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c7418-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="c7418-115">Remarks</span></span>

<span data-ttu-id="c7418-116">Метод **IMAPITable::QuerySortOrder** получает текущий порядок сортировки для таблицы.</span><span class="sxs-lookup"><span data-stu-id="c7418-116">The **IMAPITable::QuerySortOrder** method retrieves the current sort order for a table.</span></span> <span data-ttu-id="c7418-117">Порядок сортировки, описаны в структуру [SSortOrderSet](ssortorderset.md) .</span><span class="sxs-lookup"><span data-stu-id="c7418-117">Sort orders are described with an [SSortOrderSet](ssortorderset.md) structure.</span></span> 
  
- <span data-ttu-id="c7418-118">Член **cSorts** структуры **SSortOrderSet** можно задать нулевое значение, если:</span><span class="sxs-lookup"><span data-stu-id="c7418-118">The **cSorts** member of the **SSortOrderSet** structure can be set to zero if:</span></span> 
    
- <span data-ttu-id="c7418-119">В таблице приведен без сортировки.</span><span class="sxs-lookup"><span data-stu-id="c7418-119">The table is unsorted.</span></span>
    
- <span data-ttu-id="c7418-120">Нет информации о порядок сортировки таблицы.</span><span class="sxs-lookup"><span data-stu-id="c7418-120">There is no information about how the table is sorted.</span></span>
    
- <span data-ttu-id="c7418-121">Структура **SSortOrderSet** не подходит для описания порядка сортировки.</span><span class="sxs-lookup"><span data-stu-id="c7418-121">The **SSortOrderSet** structure is not appropriate for describing the sort order.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="c7418-122">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="c7418-122">Notes to implementers</span></span>

<span data-ttu-id="c7418-123">Если вызывается метод [IMAPITable::SortTable](imapitable-sorttable.md) с структуру **SSortOrderSet** , содержащую ноль столбцов в ключ сортировки, удалите текущий порядок сортировки и применить порядок по умолчанию, если он существует.</span><span class="sxs-lookup"><span data-stu-id="c7418-123">If a call is made to your [IMAPITable::SortTable](imapitable-sorttable.md) method with an **SSortOrderSet** structure containing zero columns in the sort key, remove the current sort order and apply the default order, if there is one.</span></span> <span data-ttu-id="c7418-124">В последующие вызовы **QuerySortOrder**можно выбрать, нужно ли возвращать ноль или больше столбцов для ключа сортировки.</span><span class="sxs-lookup"><span data-stu-id="c7418-124">In subsequent calls to **QuerySortOrder**, you can choose whether to return zero or more columns for the sort key.</span></span> <span data-ttu-id="c7418-125">Можно вернуть больше столбцов, чем в наличии представления.</span><span class="sxs-lookup"><span data-stu-id="c7418-125">You can return more columns than are in the present view.</span></span>
  
<span data-ttu-id="c7418-126">Дополнительные сведения о сортировке см [категоризации](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="c7418-126">For more information about sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c7418-127">См. также</span><span class="sxs-lookup"><span data-stu-id="c7418-127">See also</span></span>



[<span data-ttu-id="c7418-128">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="c7418-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="c7418-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c7418-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c7418-130">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="c7418-130">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="c7418-131">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c7418-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

