---
title: имапитаблесетколлапсестате
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
# <a name="imapitablesetcollapsestate"></a><span data-ttu-id="ab1bd-103">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="ab1bd-103">IMAPITable::SetCollapseState</span></span>

  
  
<span data-ttu-id="ab1bd-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab1bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab1bd-105">Перестраивает текущее развернутое или свернутое состояние таблицы с классификацией с использованием данных, сохраненных при предыдущем вызове метода [IMAPITable:: жетколлапсестате](imapitable-getcollapsestate.md) .</span><span class="sxs-lookup"><span data-stu-id="ab1bd-105">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) method.</span></span> 
  
```cpp
HRESULT SetCollapseState(
ULONG ulFlags,
ULONG cbCollapseState,
LPBYTE pbCollapseState,
BOOKMARK FAR * lpbkLocation
);
```

## <a name="parameters"></a><span data-ttu-id="ab1bd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ab1bd-106">Parameters</span></span>

 <span data-ttu-id="ab1bd-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ab1bd-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ab1bd-108">Резервирования должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="ab1bd-109">_кбколлапсестате_</span><span class="sxs-lookup"><span data-stu-id="ab1bd-109">_cbCollapseState_</span></span>
  
> <span data-ttu-id="ab1bd-110">возврата Количество байтов в структуре, на которую указывает параметр _пбколлапсестате_ .</span><span class="sxs-lookup"><span data-stu-id="ab1bd-110">[in] Count of bytes in the structure pointed to by the  _pbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="ab1bd-111">_пбколлапсестате_</span><span class="sxs-lookup"><span data-stu-id="ab1bd-111">_pbCollapseState_</span></span>
  
> <span data-ttu-id="ab1bd-112">возврата Указатель на структуры, содержащие данные, необходимые для перестроения представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-112">[in] Pointer to the structures containing the data needed to rebuild the table view.</span></span>
    
 <span data-ttu-id="ab1bd-113">_лпбклокатион_</span><span class="sxs-lookup"><span data-stu-id="ab1bd-113">_lpbkLocation_</span></span>
  
> <span data-ttu-id="ab1bd-114">вышли Указатель на закладку, указывающую строку в таблице, в которой должно быть перестроено свернутое или развернутое состояние.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-114">[out] Pointer to a bookmark identifying the row in the table at which the collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="ab1bd-115">Эта закладка и ключ экземпляра передаются в параметре _лпбинстанцекэй_ в вызове [IMAPITable:: жетколлапсестате](imapitable-getcollapsestate.md) Идентифицируйте ту же строку.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-115">This bookmark and the instance key passed in the  _lpbInstanceKey_ parameter in the call to [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) identify the same row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ab1bd-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ab1bd-116">Return value</span></span>

<span data-ttu-id="ab1bd-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="ab1bd-117">S_OK</span></span> 
  
> <span data-ttu-id="ab1bd-118">Состояние таблицы, классифицированной по категориям, успешно перестроено.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-118">The state of the categorized table was successfully rebuilt.</span></span>
    
<span data-ttu-id="ab1bd-119">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="ab1bd-119">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="ab1bd-120">Выполняется другая операция, которая не позволяет запустить операцию.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-120">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="ab1bd-121">Выполнение выполняемой операции должно быть разрешено или остановлено.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-121">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="ab1bd-122">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="ab1bd-122">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="ab1bd-123">Таблице не удалось завершить перестроение свернутого или расширенного представления.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-123">The table could not finish rebuilding the collapsed or expanded view.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ab1bd-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="ab1bd-124">Remarks</span></span>

<span data-ttu-id="ab1bd-125">Метод **IMAPITable:: сетколлапсестате** переустанавливает развернутое или свернутое состояние представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-125">The **IMAPITable::SetCollapseState** method reestablishes the expanded or collapsed state of the table view.</span></span> <span data-ttu-id="ab1bd-126">**Сетколлапсестате** и **жетколлапсестате** работают вместе следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ab1bd-126">**SetCollapseState** and **GetCollapseState** work together as follows:</span></span> 
  
1. <span data-ttu-id="ab1bd-127">Когда состояние таблицы, классифицированной по категориям, будет изменено, вызов [IMAPITable:: жетколлапсестате](imapitable-getcollapsestate.md) вызывается для сохранения всех данных, относящихся к состоянию до изменения.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-127">When the state of a categorized table is about to change, [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) is called to save all of the data pertaining to the state prior to the change.</span></span> 
    
2. <span data-ttu-id="ab1bd-128">Чтобы восстановить сохраненное состояние таблицы, вызывается метод **сетколлапсестате** .</span><span class="sxs-lookup"><span data-stu-id="ab1bd-128">To restore the view of the table to its saved state, **SetCollapseState** is called.</span></span> <span data-ttu-id="ab1bd-129">Данные, сохраненные в **жетколлапсестате** , передаются в **сетколлапсестате**.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-129">The data saved by **GetCollapseState** is passed to **SetCollapseState**.</span></span> <span data-ttu-id="ab1bd-130">**Сетколлапсестате** может использовать эти данные для восстановления состояния.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-130">**SetCollapseState** is able to use that data to restore the state.</span></span> 
    
3. <span data-ttu-id="ab1bd-131">**Сетколлапсестате** возвращает в качестве выходного параметра закладку, которая определяет ту же строку, что и ключ экземпляра, переданный в качестве входных данных для **жетколлапсестате**.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-131">**SetCollapseState** returns as an output parameter a bookmark that identifies the same row as the instance key passed as input to **GetCollapseState**.</span></span>
    
<span data-ttu-id="ab1bd-132">Для получения дополнительных сведений об классифицированных таблицах, ознакомьтесь со статьей [Сортировка и категоризация](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="ab1bd-132">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ab1bd-133">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="ab1bd-133">Notes to implementers</span></span>

<span data-ttu-id="ab1bd-134">Вы несете ответственность за проверку того, что порядок сортировки и ограничения точно совпадают со временем вызова **жетколлапсестате** .</span><span class="sxs-lookup"><span data-stu-id="ab1bd-134">You are responsible for verifying that the sort order and restrictions are exactly the same as they were at the time of the **GetCollapseState** call.</span></span> <span data-ttu-id="ab1bd-135">Если было сделано изменение, **сетколлапсестате** не должно вызываться, так как результаты могут быть непредсказуемыми.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-135">If a change has been made, **SetCollapseState** should not be called because the results can be unpredictable.</span></span> <span data-ttu-id="ab1bd-136">Это может произойти, если, например, клиент вызывает **жетколлапсестате** , а затем **сорттабле** для изменения ключа сортировки перед вызовом **сетколлапсестате**.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-136">This can happen if, for example, a client calls **GetCollapseState** and then **SortTable** to change the sort key before calling **SetCollapseState**.</span></span> <span data-ttu-id="ab1bd-137">Чтобы обеспечить безопасность, убедитесь, что сохраненные данные все еще действительны, прежде чем продолжить восстановление.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-137">To be safe, check that the saved data is still valid before proceeding with the restoration.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ab1bd-138">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="ab1bd-138">Notes to callers</span></span>

<span data-ttu-id="ab1bd-139">Для вызова **сетколлапсестате**необходимо ранее вызвать **жетколлапсестате**.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-139">To call **SetCollapseState**, you must have previously called **GetCollapseState**.</span></span> <span data-ttu-id="ab1bd-140">Порядок сортировки, устанавливающий категории, должен быть одинаковым для обоих методов.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-140">The sort order establishing the categories should be the same for both methods.</span></span> <span data-ttu-id="ab1bd-141">Если порядок сортировки отличается, результаты операции **сетколлапсестате** непредсказуемы.</span><span class="sxs-lookup"><span data-stu-id="ab1bd-141">If the sort orders differ, the results of the **SetCollapseState** operation are unpredictable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ab1bd-142">См. также</span><span class="sxs-lookup"><span data-stu-id="ab1bd-142">See also</span></span>



[<span data-ttu-id="ab1bd-143">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="ab1bd-143">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="ab1bd-144">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="ab1bd-144">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="ab1bd-145">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="ab1bd-145">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="ab1bd-146">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ab1bd-146">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

