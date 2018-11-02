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
ms.openlocfilehash: 51c239897e5e225a0765f78404526e2836371f30
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567904"
---
# <a name="imapitablesetcollapsestate"></a><span data-ttu-id="a1056-103">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="a1056-103">IMAPITable::SetCollapseState</span></span>

  
  
<span data-ttu-id="a1056-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1056-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1056-105">Заново создает текущее развернутое или свернутое состояние форматирование таблицы с использованием данных, сохраненный во время предыдущего вызова метода [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) .</span><span class="sxs-lookup"><span data-stu-id="a1056-105">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) method.</span></span> 
  
```cpp
HRESULT SetCollapseState(
ULONG ulFlags,
ULONG cbCollapseState,
LPBYTE pbCollapseState,
BOOKMARK FAR * lpbkLocation
);
```

## <a name="parameters"></a><span data-ttu-id="a1056-106">���������</span><span class="sxs-lookup"><span data-stu-id="a1056-106">Parameters</span></span>

 <span data-ttu-id="a1056-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a1056-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a1056-108">Зарезервировано; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="a1056-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="a1056-109">_cbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="a1056-109">_cbCollapseState_</span></span>
  
> <span data-ttu-id="a1056-110">[in] Число байт в структуре, на который указывает параметр _pbCollapseState_ .</span><span class="sxs-lookup"><span data-stu-id="a1056-110">[in] Count of bytes in the structure pointed to by the  _pbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="a1056-111">_pbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="a1056-111">_pbCollapseState_</span></span>
  
> <span data-ttu-id="a1056-112">[in] Указатель на структуры, содержащие данные, необходимые для перестроения в табличном представлении.</span><span class="sxs-lookup"><span data-stu-id="a1056-112">[in] Pointer to the structures containing the data needed to rebuild the table view.</span></span>
    
 <span data-ttu-id="a1056-113">_lpbkLocation_</span><span class="sxs-lookup"><span data-stu-id="a1056-113">_lpbkLocation_</span></span>
  
> <span data-ttu-id="a1056-114">[out] Указатель на закладку, идентифицирующий строку в таблице, необходимо перестроить свернутого или развернутого состояния.</span><span class="sxs-lookup"><span data-stu-id="a1056-114">[out] Pointer to a bookmark identifying the row in the table at which the collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="a1056-115">В этом закладку и ключа экземпляра, переданной в параметре _lpbInstanceKey_ в вызове [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) определите той же строке.</span><span class="sxs-lookup"><span data-stu-id="a1056-115">This bookmark and the instance key passed in the  _lpbInstanceKey_ parameter in the call to [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) identify the same row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a1056-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a1056-116">Return value</span></span>

<span data-ttu-id="a1056-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="a1056-117">S_OK</span></span> 
  
> <span data-ttu-id="a1056-118">Состояние по категориям таблицы успешно восстановлены.</span><span class="sxs-lookup"><span data-stu-id="a1056-118">The state of the categorized table was successfully rebuilt.</span></span>
    
<span data-ttu-id="a1056-119">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="a1056-119">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="a1056-120">В, не позволяющей операция запуск выполняется другой операции.</span><span class="sxs-lookup"><span data-stu-id="a1056-120">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="a1056-121">В процессе выполнения операции должны выполнить либо должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="a1056-121">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="a1056-122">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="a1056-122">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="a1056-123">Таблица не может завершить перестроение свернутого или развернутого представления.</span><span class="sxs-lookup"><span data-stu-id="a1056-123">The table could not finish rebuilding the collapsed or expanded view.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a1056-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="a1056-124">Remarks</span></span>

<span data-ttu-id="a1056-125">Метод **IMAPITable::SetCollapseState** восстанавливает развернутое или свернутое состояние в табличном представлении.</span><span class="sxs-lookup"><span data-stu-id="a1056-125">The **IMAPITable::SetCollapseState** method reestablishes the expanded or collapsed state of the table view.</span></span> <span data-ttu-id="a1056-126">**SetCollapseState** и **GetCollapseState** работают вместе следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a1056-126">**SetCollapseState** and **GetCollapseState** work together as follows:</span></span> 
  
1. <span data-ttu-id="a1056-127">Считается изменение состояния форматирование таблицы, чтобы сохранить все данные, относящиеся к состоянию до изменения называется [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) .</span><span class="sxs-lookup"><span data-stu-id="a1056-127">When the state of a categorized table is about to change, [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) is called to save all of the data pertaining to the state prior to the change.</span></span> 
    
2. <span data-ttu-id="a1056-128">Чтобы восстановить представление таблицы в состояние сохраненного, называется **SetCollapseState** .</span><span class="sxs-lookup"><span data-stu-id="a1056-128">To restore the view of the table to its saved state, **SetCollapseState** is called.</span></span> <span data-ttu-id="a1056-129">Данные сохраняются **GetCollapseState** передается в **SetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="a1056-129">The data saved by **GetCollapseState** is passed to **SetCollapseState**.</span></span> <span data-ttu-id="a1056-130">**SetCollapseState** могут использовать эти данные для восстановления состояния.</span><span class="sxs-lookup"><span data-stu-id="a1056-130">**SetCollapseState** is able to use that data to restore the state.</span></span> 
    
3. <span data-ttu-id="a1056-131">**SetCollapseState** возвращает в качестве выходного параметра закладка, идентифицирующее той же строке ключ экземпляра, переданной в качестве входных данных для **GetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="a1056-131">**SetCollapseState** returns as an output parameter a bookmark that identifies the same row as the instance key passed as input to **GetCollapseState**.</span></span>
    
<span data-ttu-id="a1056-132">Дополнительные сведения о таблицах по категориям можно [Сортировка и классификации](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="a1056-132">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a1056-133">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="a1056-133">Notes to implementers</span></span>

<span data-ttu-id="a1056-134">Вы несете ответственность за проверка, что порядок сортировки и ограничения полностью совпадают, как во время вызова **GetCollapseState** .</span><span class="sxs-lookup"><span data-stu-id="a1056-134">You are responsible for verifying that the sort order and restrictions are exactly the same as they were at the time of the **GetCollapseState** call.</span></span> <span data-ttu-id="a1056-135">Если был изменен, **SetCollapseState** его не следует вызывать поскольку результатов может быть непредсказуемым.</span><span class="sxs-lookup"><span data-stu-id="a1056-135">If a change has been made, **SetCollapseState** should not be called because the results can be unpredictable.</span></span> <span data-ttu-id="a1056-136">Это может произойти, если, например, клиент вызывает **GetCollapseState** , а затем **SortTable** , чтобы изменить ключ сортировки до вызова метода **SetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="a1056-136">This can happen if, for example, a client calls **GetCollapseState** and then **SortTable** to change the sort key before calling **SetCollapseState**.</span></span> <span data-ttu-id="a1056-137">В целях безопасности проверки, что сохраненные данные по-прежнему перед тем как продолжить восстановление.</span><span class="sxs-lookup"><span data-stu-id="a1056-137">To be safe, check that the saved data is still valid before proceeding with the restoration.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a1056-138">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="a1056-138">Notes to callers</span></span>

<span data-ttu-id="a1056-139">Чтобы позвонить **SetCollapseState**, необходимо ранее вызова **GetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="a1056-139">To call **SetCollapseState**, you must have previously called **GetCollapseState**.</span></span> <span data-ttu-id="a1056-140">Порядок сортировки, определение категории должно совпадать для обоих методов.</span><span class="sxs-lookup"><span data-stu-id="a1056-140">The sort order establishing the categories should be the same for both methods.</span></span> <span data-ttu-id="a1056-141">Если порядок сортировки не совпадают, результаты операции **SetCollapseState** непредсказуемы.</span><span class="sxs-lookup"><span data-stu-id="a1056-141">If the sort orders differ, the results of the **SetCollapseState** operation are unpredictable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a1056-142">См. также</span><span class="sxs-lookup"><span data-stu-id="a1056-142">See also</span></span>



[<span data-ttu-id="a1056-143">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="a1056-143">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="a1056-144">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="a1056-144">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="a1056-145">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="a1056-145">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="a1056-146">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a1056-146">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

