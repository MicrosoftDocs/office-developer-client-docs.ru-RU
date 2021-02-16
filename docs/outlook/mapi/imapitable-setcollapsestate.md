---
title: IMAPITableSetCollapseState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SetCollapseState
api_type:
- COM
ms.assetid: 31325e8f-1cf9-49b2-8118-953996b0037f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7351457dc5b72cfc4a7ef9f91e9d33a80ca98c39
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414069"
---
# <a name="imapitablesetcollapsestate"></a><span data-ttu-id="a51d1-103">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="a51d1-103">IMAPITable::SetCollapseState</span></span>

  
  
<span data-ttu-id="a51d1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a51d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a51d1-105">Перестраивать текущее расширенное или свернутое состояние классизированной таблицы с помощью данных, сохраненных при предыдущем вызове метода [IMAPITable::GetCollapseState.](imapitable-getcollapsestate.md)</span><span class="sxs-lookup"><span data-stu-id="a51d1-105">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) method.</span></span> 
  
```cpp
HRESULT SetCollapseState(
ULONG ulFlags,
ULONG cbCollapseState,
LPBYTE pbCollapseState,
BOOKMARK FAR * lpbkLocation
);
```

## <a name="parameters"></a><span data-ttu-id="a51d1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a51d1-106">Parameters</span></span>

 <span data-ttu-id="a51d1-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a51d1-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a51d1-108">Зарезервировано; должно быть нулем.</span><span class="sxs-lookup"><span data-stu-id="a51d1-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="a51d1-109">_cbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="a51d1-109">_cbCollapseState_</span></span>
  
> <span data-ttu-id="a51d1-110">[in] Количествобайтов в структуре, на которые указывает параметр _pbCollapseState._</span><span class="sxs-lookup"><span data-stu-id="a51d1-110">[in] Count of bytes in the structure pointed to by the  _pbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="a51d1-111">_pbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="a51d1-111">_pbCollapseState_</span></span>
  
> <span data-ttu-id="a51d1-112">[in] Указатель на структуры, содержащие данные, необходимые для перестроения представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="a51d1-112">[in] Pointer to the structures containing the data needed to rebuild the table view.</span></span>
    
 <span data-ttu-id="a51d1-113">_lpbkLocation_</span><span class="sxs-lookup"><span data-stu-id="a51d1-113">_lpbkLocation_</span></span>
  
> <span data-ttu-id="a51d1-114">[out] Указатель на закладку, определяя строку в таблице, в которой необходимо перестроить свернутые или расширенные состояния.</span><span class="sxs-lookup"><span data-stu-id="a51d1-114">[out] Pointer to a bookmark identifying the row in the table at which the collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="a51d1-115">Эта закладка и ключ экземпляра, переданные в  _параметре lpbInstanceKey_ при вызове [IMAPITable::GetCollapseState,](imapitable-getcollapsestate.md) определяют ту же строку.</span><span class="sxs-lookup"><span data-stu-id="a51d1-115">This bookmark and the instance key passed in the  _lpbInstanceKey_ parameter in the call to [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) identify the same row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a51d1-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a51d1-116">Return value</span></span>

<span data-ttu-id="a51d1-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="a51d1-117">S_OK</span></span> 
  
> <span data-ttu-id="a51d1-118">Состояние классизированной таблицы было успешно перестроено.</span><span class="sxs-lookup"><span data-stu-id="a51d1-118">The state of the categorized table was successfully rebuilt.</span></span>
    
<span data-ttu-id="a51d1-119">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="a51d1-119">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="a51d1-120">В настоящее время идет другая операция, которая препятствует запуску операции.</span><span class="sxs-lookup"><span data-stu-id="a51d1-120">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="a51d1-121">Либо операция должна быть завершена, либо она должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="a51d1-121">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="a51d1-122">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="a51d1-122">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="a51d1-123">Не удалось завершить перестройку свернутой или расширенной представления.</span><span class="sxs-lookup"><span data-stu-id="a51d1-123">The table could not finish rebuilding the collapsed or expanded view.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a51d1-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="a51d1-124">Remarks</span></span>

<span data-ttu-id="a51d1-125">Метод **IMAPITable::SetCollapseState** повторно восстановить состояние расширенного или свернутого представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="a51d1-125">The **IMAPITable::SetCollapseState** method reestablishes the expanded or collapsed state of the table view.</span></span> <span data-ttu-id="a51d1-126">**SetCollapseState** и **GetCollapseState** работают вместе следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a51d1-126">**SetCollapseState** and **GetCollapseState** work together as follows:</span></span> 
  
1. <span data-ttu-id="a51d1-127">Когда состояние классизированной таблицы вот-вот изменится, будет вызванО сообщение [IMAPITable::GetCollapseState,](imapitable-getcollapsestate.md) чтобы сохранить все данные, относящиеся к этому состоянии, до изменения.</span><span class="sxs-lookup"><span data-stu-id="a51d1-127">When the state of a categorized table is about to change, [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) is called to save all of the data pertaining to the state prior to the change.</span></span> 
    
2. <span data-ttu-id="a51d1-128">Чтобы восстановить представление таблицы до сохраненного состояния, **вызвано setCollapseState.**</span><span class="sxs-lookup"><span data-stu-id="a51d1-128">To restore the view of the table to its saved state, **SetCollapseState** is called.</span></span> <span data-ttu-id="a51d1-129">Данные, сохраненные с помощью **GetCollapseState,** передаются **в setCollapseState.**</span><span class="sxs-lookup"><span data-stu-id="a51d1-129">The data saved by **GetCollapseState** is passed to **SetCollapseState**.</span></span> <span data-ttu-id="a51d1-130">**SetCollapseState** может использовать эти данные для восстановления состояния.</span><span class="sxs-lookup"><span data-stu-id="a51d1-130">**SetCollapseState** is able to use that data to restore the state.</span></span> 
    
3. <span data-ttu-id="a51d1-131">**SetCollapseState** возвращает в качестве выходного параметра закладку, которая определяет ту же строку, что и ключ экземпляра, переданный в качестве входных данных **для GetCollapseState.**</span><span class="sxs-lookup"><span data-stu-id="a51d1-131">**SetCollapseState** returns as an output parameter a bookmark that identifies the same row as the instance key passed as input to **GetCollapseState**.</span></span>
    
<span data-ttu-id="a51d1-132">Дополнительные сведения о категориях таблиц см. в таблице [сортировки и категоризации.](sorting-and-categorization.md)</span><span class="sxs-lookup"><span data-stu-id="a51d1-132">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a51d1-133">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="a51d1-133">Notes to implementers</span></span>

<span data-ttu-id="a51d1-134">Вы несете ответственность за проверку того, что порядок сортировки и ограничения точно такие же, как они были во время вызова **GetCollapseState.**</span><span class="sxs-lookup"><span data-stu-id="a51d1-134">You are responsible for verifying that the sort order and restrictions are exactly the same as they were at the time of the **GetCollapseState** call.</span></span> <span data-ttu-id="a51d1-135">Если было внося изменение, не следует использовать **SetCollapseState,** так как результаты могут быть непредсказуемыми.</span><span class="sxs-lookup"><span data-stu-id="a51d1-135">If a change has been made, **SetCollapseState** should not be called because the results can be unpredictable.</span></span> <span data-ttu-id="a51d1-136">Это может произойти, если, например, клиент вызывает **GetCollapseState,** а затем **SortTable** для изменения ключа сортировки перед вызовом **SetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="a51d1-136">This can happen if, for example, a client calls **GetCollapseState** and then **SortTable** to change the sort key before calling **SetCollapseState**.</span></span> <span data-ttu-id="a51d1-137">Чтобы быть безопасным, убедитесь, что сохраненные данные остаются действительными, прежде чем при восстановлении.</span><span class="sxs-lookup"><span data-stu-id="a51d1-137">To be safe, check that the saved data is still valid before proceeding with the restoration.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a51d1-138">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="a51d1-138">Notes to callers</span></span>

<span data-ttu-id="a51d1-139">Чтобы вызвать **SetCollapseState,** необходимо ранее вызвать **GetCollapseState.**</span><span class="sxs-lookup"><span data-stu-id="a51d1-139">To call **SetCollapseState**, you must have previously called **GetCollapseState**.</span></span> <span data-ttu-id="a51d1-140">Порядок сортировки, устанавливающий категории, должен быть одинаковым для обоих методов.</span><span class="sxs-lookup"><span data-stu-id="a51d1-140">The sort order establishing the categories should be the same for both methods.</span></span> <span data-ttu-id="a51d1-141">Если заказы сортировки отличаются, результаты операции **SetCollapseState** непредсказуемы.</span><span class="sxs-lookup"><span data-stu-id="a51d1-141">If the sort orders differ, the results of the **SetCollapseState** operation are unpredictable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a51d1-142">См. также</span><span class="sxs-lookup"><span data-stu-id="a51d1-142">See also</span></span>



[<span data-ttu-id="a51d1-143">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="a51d1-143">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="a51d1-144">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="a51d1-144">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="a51d1-145">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="a51d1-145">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="a51d1-146">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a51d1-146">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

