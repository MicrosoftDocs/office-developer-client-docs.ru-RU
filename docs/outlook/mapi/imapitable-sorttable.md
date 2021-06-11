---
title: IMAPITableSortTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SortTable
api_type:
- COM
ms.assetid: ff5f78ac-06cf-46fb-93da-5f4a3a5d1b22
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f16ba9164d55fdb7bd688d4068f99dc4407e5413
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432368"
---
# <a name="imapitablesorttable"></a><span data-ttu-id="78717-103">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="78717-103">IMAPITable::SortTable</span></span>

<span data-ttu-id="78717-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78717-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78717-105">Метод **IMAPITable::SortTable** заказывает строки таблицы в зависимости от критериев сортировки.</span><span class="sxs-lookup"><span data-stu-id="78717-105">The **IMAPITable::SortTable** method orders the rows of the table, depending on sort criteria.</span></span> 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="78717-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="78717-106">Parameters</span></span>

<span data-ttu-id="78717-107">_lpSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="78717-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="78717-108">[in] Указатель на [структуру SSortOrderSet,](ssortorderset.md) которая содержит критерии сортировки для применения.</span><span class="sxs-lookup"><span data-stu-id="78717-108">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the sort criteria to apply.</span></span> <span data-ttu-id="78717-109">Передача **структуры SSortOrderSet** с нулем столбцов указывает на то, что таблицу не нужно сортировать в любом конкретном порядке.</span><span class="sxs-lookup"><span data-stu-id="78717-109">Passing an **SSortOrderSet** structure that contains zero columns indicates that the table does not have to be sorted in any particular order.</span></span> 
    
<span data-ttu-id="78717-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="78717-110">_ulFlags_</span></span>
  
> <span data-ttu-id="78717-111">[in] Bitmask флагов, которые контролируют время **операции IMAPITable::SortTable.**</span><span class="sxs-lookup"><span data-stu-id="78717-111">[in] Bitmask of flags that controls the timing of the **IMAPITable::SortTable** operation.</span></span> <span data-ttu-id="78717-112">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="78717-112">The following flags can be set:</span></span> 
    
<span data-ttu-id="78717-113">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="78717-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="78717-114">Запускает операцию асинхронно и возвращается до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="78717-114">Starts the operation asynchronously and returns before the operation is complete.</span></span>
    
<span data-ttu-id="78717-115">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="78717-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="78717-116">Откладывает завершение сортировки до тех пор, пока не потребуются данные в таблице.</span><span class="sxs-lookup"><span data-stu-id="78717-116">Defers the completion of the sort until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="78717-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78717-117">Return value</span></span>

<span data-ttu-id="78717-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="78717-118">S_OK</span></span> 
  
> <span data-ttu-id="78717-119">Операция сортировки прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="78717-119">The sort operation was successful.</span></span>
    
<span data-ttu-id="78717-120">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="78717-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="78717-121">В настоящее время продолжается другая операция, которая не позволяет начать операцию сортировки.</span><span class="sxs-lookup"><span data-stu-id="78717-121">Another operation is in progress that prevents the sort operation from starting.</span></span> <span data-ttu-id="78717-122">Либо операция должна быть разрешена к завершению, либо она должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="78717-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="78717-123">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="78717-123">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="78717-124">В таблице не поддерживается тип запрашиваемой сортировки.</span><span class="sxs-lookup"><span data-stu-id="78717-124">The table does not support the type of sorting requested.</span></span>
    
<span data-ttu-id="78717-125">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="78717-125">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="78717-126">Таблица не может выполнять операцию, так как определенные критерии сортировки, на которые указывает параметр  _lpSortCriteria,_ слишком сложны.</span><span class="sxs-lookup"><span data-stu-id="78717-126">The table cannot perform the operation because the particular sort criteria pointed to by the  _lpSortCriteria_ parameter is too complex.</span></span> <span data-ttu-id="78717-127">**SortTable** может MAPI_E_TOO_COMPLEX в следующих условиях.</span><span class="sxs-lookup"><span data-stu-id="78717-127">**SortTable** can return MAPI_E_TOO_COMPLEX under the following conditions.</span></span> 
    
   - <span data-ttu-id="78717-128">Для столбца свойств, который не может сортироваться, запрашивается операция сортировки.</span><span class="sxs-lookup"><span data-stu-id="78717-128">A sort operation is requested for a property column that the implementation cannot sort.</span></span>
    
   - <span data-ttu-id="78717-129">Реализация не поддерживает заказ сортировки, запрашиваемого в **члене ulOrder** структуры **SSortOrderSet.**</span><span class="sxs-lookup"><span data-stu-id="78717-129">The implementation does not support the sort order requested in the **ulOrder** member of the **SSortOrderSet** structure.</span></span> 
    
   - <span data-ttu-id="78717-130">Количество столбцов для сортировки, как указано в члене **cSorts** в **SSortOrderSet,** больше, чем может обрабатывать реализация.</span><span class="sxs-lookup"><span data-stu-id="78717-130">The number of columns to be sorted, as specified in the **cSorts** member in **SSortOrderSet**, is larger than the implementation can handle.</span></span>
    
   - <span data-ttu-id="78717-131">Запрашивается операция сортировки, как указывает тег свойства **в SSortOrderSet,** на основе свойства, которое не находится в доступном или активном наборе, и реализация не поддерживает сортировку свойств, не имеющихся в доступном наборе.</span><span class="sxs-lookup"><span data-stu-id="78717-131">A sort operation is requested, as indicated by a property tag in **SSortOrderSet**, based on a property that is not in the available or active set and the implementation does not support sorting on properties not in the available set.</span></span>
    
   - <span data-ttu-id="78717-132">Одно свойство указывается несколько раз в наборе порядка сортировки, как указывается несколькими экземплярами одного и того же тега свойств, и реализация не может выполнять такую операцию сортировки.</span><span class="sxs-lookup"><span data-stu-id="78717-132">One property is specified multiple times in a sort order set, as indicated by multiple instances of the same property tag, and the implementation cannot perform such a sort operation.</span></span>
    
   - <span data-ttu-id="78717-133">Операция сортировки, основанная на столбцах многоценных свойств, запрашивается с помощью MVI_FLAG и реализация не поддерживает сортировку по многоценным свойствам.</span><span class="sxs-lookup"><span data-stu-id="78717-133">A sort operation based on multivalued property columns is requested using MVI_FLAG and the implementation does not support sorting on multivalued properties.</span></span> 
    
   - <span data-ttu-id="78717-134">Тег свойства свойства в **SSortOrderSet** указывает свойство или тип, который не поддерживается реализацией.</span><span class="sxs-lookup"><span data-stu-id="78717-134">A property tag for a property in **SSortOrderSet** specifies a property or type that the implementation does not support.</span></span> 
    
   - <span data-ttu-id="78717-135">Операция сортировки, которая проходит через таблицу  из свойства[PR_RENDERING_POSITION (PidTagRenderingPosition),](pidtagrenderingposition-canonical-property.md)указывается только для таблицы вложений, которая поддерживает этот тип сортировки.</span><span class="sxs-lookup"><span data-stu-id="78717-135">A sort operation other than one that proceeds through the table from the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property forward is specified only for an attachment table that supports this type of sorting.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="78717-136">Примечания</span><span class="sxs-lookup"><span data-stu-id="78717-136">Remarks</span></span>

<span data-ttu-id="78717-137">Метод **IMAPITable::SortTable** заказывает строки в представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="78717-137">The **IMAPITable::SortTable** method orders the rows in a table view.</span></span> <span data-ttu-id="78717-138">В то время как некоторые таблицы поддерживают стандартную и категоризированную сортировку в различных столбцах ключей сортировки, другие таблицы более ограничены в их поддержке.</span><span class="sxs-lookup"><span data-stu-id="78717-138">Whereas some tables support both standard and categorized sorting on various sort key columns, other tables are more limited in their support.</span></span> <span data-ttu-id="78717-139">Поставщики адресных книг обычно не поддерживают сортировку таблиц.</span><span class="sxs-lookup"><span data-stu-id="78717-139">Address book providers ordinarily do not support table sorting.</span></span> <span data-ttu-id="78717-140">Поставщики магазинов сообщений обычно поддерживают сортировку до такой степени, что они сохраняют порядок сортировки папок, который приводит к сортировке полной таблицы (таблицы без ограничений).</span><span class="sxs-lookup"><span data-stu-id="78717-140">Message store providers usually support sorting to the extent that they keep the sort order of folders that results when a full table (a table without restrictions) is sorted.</span></span> 
  
<span data-ttu-id="78717-141">Некоторые таблицы позволяют сортировать в любом столбце таблицы.</span><span class="sxs-lookup"><span data-stu-id="78717-141">Some tables allow sorting to be done on any table column.</span></span> <span data-ttu-id="78717-142">Другие таблицы не являются; столбцы, не включенные в представление таблицы, не влияет на вызов **SortTable.**</span><span class="sxs-lookup"><span data-stu-id="78717-142">Other tables do not; columns not included in the table view are unaffected by a **SortTable** call.</span></span> <span data-ttu-id="78717-143">Некоторые таблицы требуют, чтобы ключи сортировки были построены только с помощью столбцов в текущем наборе столбцов таблицы.</span><span class="sxs-lookup"><span data-stu-id="78717-143">Some tables require that sort keys be built only with columns in the table's current column set.</span></span> 
  
<span data-ttu-id="78717-144">Таблица может возвращаться MAPI_E_NO_SUPPORT или MAPI_E_TOO_COMPLEX **из SortTable,** если она не может выполнить операцию сортировки.</span><span class="sxs-lookup"><span data-stu-id="78717-144">A table can return either MAPI_E_NO_SUPPORT or MAPI_E_TOO_COMPLEX from **SortTable** when it cannot complete a sort operation.</span></span> <span data-ttu-id="78717-145">Кроме того, поставщики магазинов не гарантируют честь набора сортировки, заданного для таблиц иерархии.</span><span class="sxs-lookup"><span data-stu-id="78717-145">Moreover, store providers are not guaranteed to honor the sort order set specified for hierarchy tables.</span></span> 
  
<span data-ttu-id="78717-146">Если в структуре [SSortOrderSet](ssortorderset.md) имеются нулевые столбцы, на которые указывает параметр  _lpSortCriteria,_ в таблице возвращается текущий набор столбцов.</span><span class="sxs-lookup"><span data-stu-id="78717-146">When there are zero columns in the [SSortOrderSet](ssortorderset.md) structure pointed to by the  _lpSortCriteria_ parameter, the table returns the current column set.</span></span> <span data-ttu-id="78717-147">Текущий порядок сортировки можно получить, позвонив по методу [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md)</span><span class="sxs-lookup"><span data-stu-id="78717-147">The current sort order can be retrieved by calling the table's [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
<span data-ttu-id="78717-148">Все закладки для таблицы недействительны и должны быть удалены при вызове в **SortTable,** а закладки BOOKMARK_CURRENT, которая указывает текущее положение курсора, следует установить в начале таблицы.</span><span class="sxs-lookup"><span data-stu-id="78717-148">All bookmarks for a table are invalidated and should be deleted when a call to **SortTable** is made, and the BOOKMARK_CURRENT bookmark that indicates the current cursor position, should be set to the beginning of the table.</span></span> 
  
<span data-ttu-id="78717-149">Если вы сортировать столбец, содержащий многоценное свойство без MVI_FLAG флага, значения столбца рассматриваются как полностью упорядоченный пучок.</span><span class="sxs-lookup"><span data-stu-id="78717-149">If you are sorting on a column that contains a multivalued property without the MVI_FLAG flag set, the column's values are treated as a completely ordered tuple.</span></span> <span data-ttu-id="78717-150">Сравнение двух многооценных столбцов сравнивает элементы столбцов в порядке, сообщая о связи столбцов при первом неравенстве, и возвращает равенство только в том случае, если сравниваемые столбцы содержат одинаковые значения в том же порядке.</span><span class="sxs-lookup"><span data-stu-id="78717-150">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality, and returns equality only if the columns being compared contain the same values in the same order.</span></span> <span data-ttu-id="78717-151">Если у одного столбца меньше значений, чем у другого, сообщаемая связь имеет значение null к другому значению.</span><span class="sxs-lookup"><span data-stu-id="78717-151">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="78717-152">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="78717-152">Notes to callers</span></span>

<span data-ttu-id="78717-153">**SortTable** работает синхронно, если не установить один из флагов.</span><span class="sxs-lookup"><span data-stu-id="78717-153">**SortTable** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="78717-154">Если вы установите флаг TBL_BATCH, **SortTable** откладывает операцию сортировки, если не запрашивать данные.</span><span class="sxs-lookup"><span data-stu-id="78717-154">If you set the TBL_BATCH flag, **SortTable** postpones the sort operation unless you request the data.</span></span> <span data-ttu-id="78717-155">Если флаг TBL_ASYNC установлен, **SortTable** работает асинхронно, потенциально возвращаясь до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="78717-155">If the TBL_ASYNC flag is set, **SortTable** operates asynchronously, potentially returning before the completion of the operation.</span></span> 
  
<span data-ttu-id="78717-156">Вызов метода [IMAPITable::Abort,](imapitable-abort.md) чтобы остановить асинхронную операцию, если необходимо немедленно сделать сортировку.</span><span class="sxs-lookup"><span data-stu-id="78717-156">Call the [IMAPITable::Abort](imapitable-abort.md) method to stop an asynchronous operation in progress if your sort must be done immediately.</span></span> <span data-ttu-id="78717-157">Если **sortTable** не может продолжиться, так как одна или несколько асинхронных операций на таблице находятся в процессе выполнения, он возвращает MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="78717-157">If **SortTable** cannot continue because one or more asynchronous operations on the table are in progress, it returns MAPI_E_BUSY.</span></span> 
  
<span data-ttu-id="78717-158">Для лучшей производительности вызываем **SetColumns** для  настройки набора столбцов таблицы и ограничим ограничение количества строк в таблице перед вызовом **SortTable** для выполнения сортировки.</span><span class="sxs-lookup"><span data-stu-id="78717-158">For best performance, call **SetColumns** to customize the table's column set and **Restrict** to limit the number of rows in the table before you call **SortTable** to perform the sort.</span></span> 
  
<span data-ttu-id="78717-159">При **сбое SortTable** порядок сортировки, который был в силе до сбоя, по-прежнему действует.</span><span class="sxs-lookup"><span data-stu-id="78717-159">Whenever **SortTable** fails, the sort order that was in effect before the failure is still in effect.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="78717-160">См. также</span><span class="sxs-lookup"><span data-stu-id="78717-160">See also</span></span>

- [<span data-ttu-id="78717-161">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="78717-161">IMAPITable::Abort</span></span>](imapitable-abort.md)
- [<span data-ttu-id="78717-162">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="78717-162">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
- [<span data-ttu-id="78717-163">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="78717-163">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
- [<span data-ttu-id="78717-164">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="78717-164">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
- [<span data-ttu-id="78717-165">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="78717-165">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
- [<span data-ttu-id="78717-166">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="78717-166">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="78717-167">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="78717-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

