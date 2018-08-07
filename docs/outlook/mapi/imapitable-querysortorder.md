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
ms.openlocfilehash: b5eb671be022a6c3aa22e66f68386691fe23b275
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809219"
---
# <a name="imapitablequerysortorder"></a><span data-ttu-id="d154b-103">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="d154b-103">IMAPITable::QuerySortOrder</span></span>

  
  
<span data-ttu-id="d154b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d154b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d154b-105">Получает текущий порядок сортировки для таблицы.</span><span class="sxs-lookup"><span data-stu-id="d154b-105">Retrieves the current sort order for a table.</span></span>
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a><span data-ttu-id="d154b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d154b-106">Parameters</span></span>

 <span data-ttu-id="d154b-107">_lppSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="d154b-107">_lppSortCriteria_</span></span>
  
> <span data-ttu-id="d154b-108">[out] Указатель на указатель на структуру [SSortOrderSet](ssortorderset.md) , содержащую текущий порядок сортировки.</span><span class="sxs-lookup"><span data-stu-id="d154b-108">[out] Pointer to a pointer to the [SSortOrderSet](ssortorderset.md) structure holding the current sort order.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d154b-109">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="d154b-109">Return value</span></span>

<span data-ttu-id="d154b-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="d154b-110">S_OK</span></span> 
  
> <span data-ttu-id="d154b-111">Порядок сортировки успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="d154b-111">The current sort order was successfully returned.</span></span>
    
<span data-ttu-id="d154b-112">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="d154b-112">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="d154b-113">В, не позволяющей операции извлечения порядок сортировки запуск выполняется другой операции.</span><span class="sxs-lookup"><span data-stu-id="d154b-113">Another operation is in progress that prevents the sort order retrieval operation from starting.</span></span> <span data-ttu-id="d154b-114">В процессе выполнения операции должны выполнить либо должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="d154b-114">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d154b-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="d154b-115">Remarks</span></span>

<span data-ttu-id="d154b-116">Метод **IMAPITable::QuerySortOrder** получает текущий порядок сортировки для таблицы.</span><span class="sxs-lookup"><span data-stu-id="d154b-116">The **IMAPITable::QuerySortOrder** method retrieves the current sort order for a table.</span></span> <span data-ttu-id="d154b-117">Порядок сортировки, описаны в структуру [SSortOrderSet](ssortorderset.md) .</span><span class="sxs-lookup"><span data-stu-id="d154b-117">Sort orders are described with an [SSortOrderSet](ssortorderset.md) structure.</span></span> 
  
- <span data-ttu-id="d154b-118">Член **cSorts** структуры **SSortOrderSet** можно задать нулевое значение, если:</span><span class="sxs-lookup"><span data-stu-id="d154b-118">The **cSorts** member of the **SSortOrderSet** structure can be set to zero if:</span></span> 
    
- <span data-ttu-id="d154b-119">В таблице приведен без сортировки.</span><span class="sxs-lookup"><span data-stu-id="d154b-119">The table is unsorted.</span></span>
    
- <span data-ttu-id="d154b-120">Нет информации о порядок сортировки таблицы.</span><span class="sxs-lookup"><span data-stu-id="d154b-120">There is no information about how the table is sorted.</span></span>
    
- <span data-ttu-id="d154b-121">Структура **SSortOrderSet** не подходит для описания порядка сортировки.</span><span class="sxs-lookup"><span data-stu-id="d154b-121">The **SSortOrderSet** structure is not appropriate for describing the sort order.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="d154b-122">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="d154b-122">Notes to implementers</span></span>

<span data-ttu-id="d154b-123">Если вызывается метод [IMAPITable::SortTable](imapitable-sorttable.md) с структуру **SSortOrderSet** , содержащую ноль столбцов в ключ сортировки, удалите текущий порядок сортировки и применить порядок по умолчанию, если он существует.</span><span class="sxs-lookup"><span data-stu-id="d154b-123">If a call is made to your [IMAPITable::SortTable](imapitable-sorttable.md) method with an **SSortOrderSet** structure containing zero columns in the sort key, remove the current sort order and apply the default order, if there is one.</span></span> <span data-ttu-id="d154b-124">В последующие вызовы **QuerySortOrder**можно выбрать, нужно ли возвращать ноль или больше столбцов для ключа сортировки.</span><span class="sxs-lookup"><span data-stu-id="d154b-124">In subsequent calls to **QuerySortOrder**, you can choose whether to return zero or more columns for the sort key.</span></span> <span data-ttu-id="d154b-125">Можно вернуть больше столбцов, чем в наличии представления.</span><span class="sxs-lookup"><span data-stu-id="d154b-125">You can return more columns than are in the present view.</span></span>
  
<span data-ttu-id="d154b-126">Дополнительные сведения о сортировке см [категоризации](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="d154b-126">For more information about sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d154b-127">См. также</span><span class="sxs-lookup"><span data-stu-id="d154b-127">See also</span></span>



[<span data-ttu-id="d154b-128">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="d154b-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="d154b-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="d154b-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="d154b-130">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="d154b-130">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="d154b-131">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d154b-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

