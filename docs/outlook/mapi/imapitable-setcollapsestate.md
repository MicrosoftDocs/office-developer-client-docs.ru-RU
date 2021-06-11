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
# <a name="imapitablesetcollapsestate"></a><span data-ttu-id="8ecd2-103">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="8ecd2-103">IMAPITable::SetCollapseState</span></span>

  
  
<span data-ttu-id="8ecd2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ecd2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ecd2-105">Восстановление текущего расширенного или свернутого состояния таблицы категорий с помощью данных, которые были сохранены при предварительном вызове метода [IMAPITable::GetCollapseState.](imapitable-getcollapsestate.md)</span><span class="sxs-lookup"><span data-stu-id="8ecd2-105">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) method.</span></span> 
  
```cpp
HRESULT SetCollapseState(
ULONG ulFlags,
ULONG cbCollapseState,
LPBYTE pbCollapseState,
BOOKMARK FAR * lpbkLocation
);
```

## <a name="parameters"></a><span data-ttu-id="8ecd2-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="8ecd2-106">Parameters</span></span>

 <span data-ttu-id="8ecd2-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8ecd2-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8ecd2-108">Зарезервировано; должно быть нулевой.</span><span class="sxs-lookup"><span data-stu-id="8ecd2-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="8ecd2-109">_cbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="8ecd2-109">_cbCollapseState_</span></span>
  
> <span data-ttu-id="8ecd2-110">[in] Количество bytes в структуре, на который указывает параметр _pbCollapseState._</span><span class="sxs-lookup"><span data-stu-id="8ecd2-110">[in] Count of bytes in the structure pointed to by the  _pbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="8ecd2-111">_pbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="8ecd2-111">_pbCollapseState_</span></span>
  
> <span data-ttu-id="8ecd2-112">[in] Указатель на структуры, содержащие данные, необходимые для восстановления представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="8ecd2-112">[in] Pointer to the structures containing the data needed to rebuild the table view.</span></span>
    
 <span data-ttu-id="8ecd2-113">_lpbkLocation_</span><span class="sxs-lookup"><span data-stu-id="8ecd2-113">_lpbkLocation_</span></span>
  
> <span data-ttu-id="8ecd2-114">[вышел] Указатель на закладки, определяющие строку в таблице, на которой должно быть восстановлено рухнувшего или расширенного состояния.</span><span class="sxs-lookup"><span data-stu-id="8ecd2-114">[out] Pointer to a bookmark identifying the row in the table at which the collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="8ecd2-115">Эта закладка и ключ экземпляра, переданные в  _параметре lpbInstanceKey_ в [вызове IMAPITable::GetCollapseState,](imapitable-getcollapsestate.md) определяют ту же строку.</span><span class="sxs-lookup"><span data-stu-id="8ecd2-115">This bookmark and the instance key passed in the  _lpbInstanceKey_ parameter in the call to [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) identify the same row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8ecd2-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ecd2-116">Return value</span></span>

<span data-ttu-id="8ecd2-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="8ecd2-117">S_OK</span></span> 
  
> <span data-ttu-id="8ecd2-118">Состояние классифицизированной таблицы было успешно восстановлено.</span><span class="sxs-lookup"><span data-stu-id="8ecd2-118">The state of the categorized table was successfully rebuilt.</span></span>
    
<span data-ttu-id="8ecd2-119">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="8ecd2-119">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="8ecd2-120">В настоящее время продолжается еще одна операция, которая не позволяет начать операцию.</span><span class="sxs-lookup"><span data-stu-id="8ecd2-120">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="8ecd2-121">Либо операция должна быть разрешена к завершению, либо она должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="8ecd2-121">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="8ecd2-122">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="8ecd2-122">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="8ecd2-123">В таблице не удалось завершить восстановление рухнувшего или расширенного представления.</span><span class="sxs-lookup"><span data-stu-id="8ecd2-123">The table could not finish rebuilding the collapsed or expanded view.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8ecd2-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="8ecd2-124">Remarks</span></span>

<span data-ttu-id="8ecd2-125">Метод **IMAPITable::SetCollapseState** reestablishes expanded or collapsed state of the table view.</span><span class="sxs-lookup"><span data-stu-id="8ecd2-125">The **IMAPITable::SetCollapseState** method reestablishes the expanded or collapsed state of the table view.</span></span> <span data-ttu-id="8ecd2-126">**SetCollapseState и** **GetCollapseState** работают вместе следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8ecd2-126">**SetCollapseState** and **GetCollapseState** work together as follows:</span></span> 
  
1. <span data-ttu-id="8ecd2-127">Когда состояние классифицируемых таблиц изменится, для сохранения всех данных, относящихся к государству до изменения, вызван [IMAPITable::GetCollapseState.](imapitable-getcollapsestate.md)</span><span class="sxs-lookup"><span data-stu-id="8ecd2-127">When the state of a categorized table is about to change, [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) is called to save all of the data pertaining to the state prior to the change.</span></span> 
    
2. <span data-ttu-id="8ecd2-128">Чтобы восстановить представление таблицы до сохраненного состояния, **называется SetCollapseState.**</span><span class="sxs-lookup"><span data-stu-id="8ecd2-128">To restore the view of the table to its saved state, **SetCollapseState** is called.</span></span> <span data-ttu-id="8ecd2-129">Данные, сохраненные **GetCollapseState,** передаются **в SetCollapseState.**</span><span class="sxs-lookup"><span data-stu-id="8ecd2-129">The data saved by **GetCollapseState** is passed to **SetCollapseState**.</span></span> <span data-ttu-id="8ecd2-130">**SetCollapseState** может использовать эти данные для восстановления состояния.</span><span class="sxs-lookup"><span data-stu-id="8ecd2-130">**SetCollapseState** is able to use that data to restore the state.</span></span> 
    
3. <span data-ttu-id="8ecd2-131">**SetCollapseState** возвращает в качестве параметра вывода закладки, которая определяет ту же строку, что и ключ экземпляра, переданный в качестве ввода **в GetCollapseState.**</span><span class="sxs-lookup"><span data-stu-id="8ecd2-131">**SetCollapseState** returns as an output parameter a bookmark that identifies the same row as the instance key passed as input to **GetCollapseState**.</span></span>
    
<span data-ttu-id="8ecd2-132">Дополнительные сведения о классификации таблиц см. в [рубрике Сортировка и классификация.](sorting-and-categorization.md)</span><span class="sxs-lookup"><span data-stu-id="8ecd2-132">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8ecd2-133">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="8ecd2-133">Notes to implementers</span></span>

<span data-ttu-id="8ecd2-134">Вы несете ответственность за проверку того, что порядок сортировки и ограничения точно такие же, как и во время вызова **GetCollapseState.**</span><span class="sxs-lookup"><span data-stu-id="8ecd2-134">You are responsible for verifying that the sort order and restrictions are exactly the same as they were at the time of the **GetCollapseState** call.</span></span> <span data-ttu-id="8ecd2-135">Если изменения были сделаны, **SetCollapseState** не следует называть, так как результаты могут быть непредсказуемыми.</span><span class="sxs-lookup"><span data-stu-id="8ecd2-135">If a change has been made, **SetCollapseState** should not be called because the results can be unpredictable.</span></span> <span data-ttu-id="8ecd2-136">Это может произойти, если, например, клиент вызывает **GetCollapseState,** а затем **SortTable,** чтобы изменить ключ сортировки перед вызовом **SetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="8ecd2-136">This can happen if, for example, a client calls **GetCollapseState** and then **SortTable** to change the sort key before calling **SetCollapseState**.</span></span> <span data-ttu-id="8ecd2-137">Чтобы быть безопасным, убедитесь, что сохраненные данные по-прежнему действительны перед началом восстановления.</span><span class="sxs-lookup"><span data-stu-id="8ecd2-137">To be safe, check that the saved data is still valid before proceeding with the restoration.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8ecd2-138">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="8ecd2-138">Notes to callers</span></span>

<span data-ttu-id="8ecd2-139">Чтобы вызвать **SetCollapseState,** необходимо предварительно вызвать **GetCollapseState.**</span><span class="sxs-lookup"><span data-stu-id="8ecd2-139">To call **SetCollapseState**, you must have previously called **GetCollapseState**.</span></span> <span data-ttu-id="8ecd2-140">Порядок сортировки, устанавливающий категории, должен быть одинаковым для обоих методов.</span><span class="sxs-lookup"><span data-stu-id="8ecd2-140">The sort order establishing the categories should be the same for both methods.</span></span> <span data-ttu-id="8ecd2-141">Если заказы сортировки отличаются, результаты операции **SetCollapseState** непредсказуемы.</span><span class="sxs-lookup"><span data-stu-id="8ecd2-141">If the sort orders differ, the results of the **SetCollapseState** operation are unpredictable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8ecd2-142">См. также</span><span class="sxs-lookup"><span data-stu-id="8ecd2-142">See also</span></span>



[<span data-ttu-id="8ecd2-143">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="8ecd2-143">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="8ecd2-144">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="8ecd2-144">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="8ecd2-145">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="8ecd2-145">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="8ecd2-146">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8ecd2-146">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

