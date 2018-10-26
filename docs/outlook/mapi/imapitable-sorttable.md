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
ms.openlocfilehash: efeff92f1a21d076c1ee58b82ad3ab25797df014
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592306"
---
# <a name="imapitablesorttable"></a><span data-ttu-id="92d45-103">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="92d45-103">IMAPITable::SortTable</span></span>

<span data-ttu-id="92d45-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92d45-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92d45-105">Метод **IMAPITable::SortTable** заказов строки в таблице, в зависимости от сортировки критериев.</span><span class="sxs-lookup"><span data-stu-id="92d45-105">The **IMAPITable::SortTable** method orders the rows of the table, depending on sort criteria.</span></span> 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="92d45-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="92d45-106">Parameters</span></span>

<span data-ttu-id="92d45-107">_lpSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="92d45-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="92d45-108">[in] Указатель на структуру [SSortOrderSet](ssortorderset.md) , содержащий условия сортировки для применения.</span><span class="sxs-lookup"><span data-stu-id="92d45-108">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the sort criteria to apply.</span></span> <span data-ttu-id="92d45-109">Передача структуру **SSortOrderSet** , которая содержит ноль столбцы указывает, что таблица имеет сортировки в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="92d45-109">Passing an **SSortOrderSet** structure that contains zero columns indicates that the table does not have to be sorted in any particular order.</span></span> 
    
<span data-ttu-id="92d45-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="92d45-110">_ulFlags_</span></span>
  
> <span data-ttu-id="92d45-111">[in] Битовая маска флаги, определяющее время операции **IMAPITable::SortTable** .</span><span class="sxs-lookup"><span data-stu-id="92d45-111">[in] Bitmask of flags that controls the timing of the **IMAPITable::SortTable** operation.</span></span> <span data-ttu-id="92d45-112">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="92d45-112">The following flags can be set:</span></span> 
    
<span data-ttu-id="92d45-113">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="92d45-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="92d45-114">Асинхронно запускает операцию и возвращает до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="92d45-114">Starts the operation asynchronously and returns before the operation is complete.</span></span>
    
<span data-ttu-id="92d45-115">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="92d45-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="92d45-116">Определяет завершения сортировки, пока данные в таблице является обязательным.</span><span class="sxs-lookup"><span data-stu-id="92d45-116">Defers the completion of the sort until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="92d45-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92d45-117">Return value</span></span>

<span data-ttu-id="92d45-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="92d45-118">S_OK</span></span> 
  
> <span data-ttu-id="92d45-119">Сортировка операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="92d45-119">The sort operation was successful.</span></span>
    
<span data-ttu-id="92d45-120">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="92d45-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="92d45-121">В, не позволяющей сортировку запуск выполняется другой операции.</span><span class="sxs-lookup"><span data-stu-id="92d45-121">Another operation is in progress that prevents the sort operation from starting.</span></span> <span data-ttu-id="92d45-122">В процессе выполнения операции должны выполнить либо должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="92d45-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="92d45-123">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="92d45-123">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="92d45-124">Таблица не поддерживает тип сортировки в запросе.</span><span class="sxs-lookup"><span data-stu-id="92d45-124">The table does not support the type of sorting requested.</span></span>
    
<span data-ttu-id="92d45-125">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="92d45-125">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="92d45-126">Таблицы не удается выполнить операцию, так как определенного сортировки, на который указывает параметр _lpSortCriteria_ слишком сложный.</span><span class="sxs-lookup"><span data-stu-id="92d45-126">The table cannot perform the operation because the particular sort criteria pointed to by the  _lpSortCriteria_ parameter is too complex.</span></span> <span data-ttu-id="92d45-127">**SortTable** может вернуть MAPI_E_TOO_COMPLEX при следующих условиях.</span><span class="sxs-lookup"><span data-stu-id="92d45-127">**SortTable** can return MAPI_E_TOO_COMPLEX under the following conditions.</span></span> 
    
   - <span data-ttu-id="92d45-128">Операция сортировки запрашивается для столбца свойства сортировать реализации нельзя.</span><span class="sxs-lookup"><span data-stu-id="92d45-128">A sort operation is requested for a property column that the implementation cannot sort.</span></span>
    
   - <span data-ttu-id="92d45-129">Реализация не поддерживает порядок сортировки, запрашиваемый в член **ulOrder** структуры **SSortOrderSet** .</span><span class="sxs-lookup"><span data-stu-id="92d45-129">The implementation does not support the sort order requested in the **ulOrder** member of the **SSortOrderSet** structure.</span></span> 
    
   - <span data-ttu-id="92d45-130">Число столбцов для сортировки, как указано в член **cSorts** в **SSortOrderSet**, больше, чем реализация может обрабатывать.</span><span class="sxs-lookup"><span data-stu-id="92d45-130">The number of columns to be sorted, as specified in the **cSorts** member in **SSortOrderSet**, is larger than the implementation can handle.</span></span>
    
   - <span data-ttu-id="92d45-131">Запрашивается операция сортировки, как указано в тег свойства в **SSortOrderSet**, на основе свойства, которое не входит в набор доступных и активных и реализация не поддерживает сортировку на набор свойств.</span><span class="sxs-lookup"><span data-stu-id="92d45-131">A sort operation is requested, as indicated by a property tag in **SSortOrderSet**, based on a property that is not in the available or active set and the implementation does not support sorting on properties not in the available set.</span></span>
    
   - <span data-ttu-id="92d45-132">Одно свойство задано несколько раз в наборе порядок сортировки, как указано в несколько экземпляров одной тега свойства и реализация не могут выполнять операции сортировки.</span><span class="sxs-lookup"><span data-stu-id="92d45-132">One property is specified multiple times in a sort order set, as indicated by multiple instances of the same property tag, and the implementation cannot perform such a sort operation.</span></span>
    
   - <span data-ttu-id="92d45-133">Запрашивается операция сортировки, основанные на столбцах многозначных свойств при помощи MVI_FLAG и реализация не поддерживает сортировку на многозначные свойства.</span><span class="sxs-lookup"><span data-stu-id="92d45-133">A sort operation based on multivalued property columns is requested using MVI_FLAG and the implementation does not support sorting on multivalued properties.</span></span> 
    
   - <span data-ttu-id="92d45-134">Тег свойства для свойства в **SSortOrderSet** задает свойство или тип, который не поддерживает реализацию.</span><span class="sxs-lookup"><span data-stu-id="92d45-134">A property tag for a property in **SSortOrderSet** specifies a property or type that the implementation does not support.</span></span> 
    
   - <span data-ttu-id="92d45-135">Операция сортировки, кроме одного, которое проходит таблицы из свойства **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) переадресовывать указан только для таблицы вложений, поддерживающего этот тип сортировки.</span><span class="sxs-lookup"><span data-stu-id="92d45-135">A sort operation other than one that proceeds through the table from the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property forward is specified only for an attachment table that supports this type of sorting.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="92d45-136">Замечания</span><span class="sxs-lookup"><span data-stu-id="92d45-136">Remarks</span></span>

<span data-ttu-id="92d45-137">Метод **IMAPITable::SortTable** заказов строки в представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="92d45-137">The **IMAPITable::SortTable** method orders the rows in a table view.</span></span> <span data-ttu-id="92d45-138">В то время как некоторые таблицы поддерживает стандартные и по категориям сортировка на различные столбцы, другими таблицами более ограничены в их поддержка.</span><span class="sxs-lookup"><span data-stu-id="92d45-138">Whereas some tables support both standard and categorized sorting on various sort key columns, other tables are more limited in their support.</span></span> <span data-ttu-id="92d45-139">Поставщиками адресных книг обычно не поддерживают Сортировка в таблице.</span><span class="sxs-lookup"><span data-stu-id="92d45-139">Address book providers ordinarily do not support table sorting.</span></span> <span data-ttu-id="92d45-140">Поставщики хранилища сообщений обычно поддерживает сортировку при условии, что они сохранить порядок сортировки папок, полученные при сортировке полной таблицы (таблицы без ограничений).</span><span class="sxs-lookup"><span data-stu-id="92d45-140">Message store providers usually support sorting to the extent that they keep the sort order of folders that results when a full table (a table without restrictions) is sorted.</span></span> 
  
<span data-ttu-id="92d45-141">Некоторые таблицы разрешить сортировку необходимо выполнить для любого столбца в таблице.</span><span class="sxs-lookup"><span data-stu-id="92d45-141">Some tables allow sorting to be done on any table column.</span></span> <span data-ttu-id="92d45-142">Нет других таблиц; столбцы, не включенные в табличном представлении не влияет на вызов **SortTable** .</span><span class="sxs-lookup"><span data-stu-id="92d45-142">Other tables do not; columns not included in the table view are unaffected by a **SortTable** call.</span></span> <span data-ttu-id="92d45-143">Для некоторых таблиц требуется создать ключи сортировки только со столбцами в текущий набор столбцов таблицы.</span><span class="sxs-lookup"><span data-stu-id="92d45-143">Some tables require that sort keys be built only with columns in the table's current column set.</span></span> 
  
<span data-ttu-id="92d45-144">Таблица может вернуть MAPI_E_NO_SUPPORT или MAPI_E_TOO_COMPLEX из **SortTable** , когда она не может выполнить операцию сортировки.</span><span class="sxs-lookup"><span data-stu-id="92d45-144">A table can return either MAPI_E_NO_SUPPORT or MAPI_E_TOO_COMPLEX from **SortTable** when it cannot complete a sort operation.</span></span> <span data-ttu-id="92d45-145">Кроме того поставщики хранилища не обязательно соблюдать порядок сортировки, указанный для таблиц иерархии набор.</span><span class="sxs-lookup"><span data-stu-id="92d45-145">Moreover, store providers are not guaranteed to honor the sort order set specified for hierarchy tables.</span></span> 
  
<span data-ttu-id="92d45-146">При наличии ноль столбцов в структуре [SSortOrderSet](ssortorderset.md) указывает параметр _lpSortCriteria_ , таблице возвращает текущий набор столбцов.</span><span class="sxs-lookup"><span data-stu-id="92d45-146">When there are zero columns in the [SSortOrderSet](ssortorderset.md) structure pointed to by the  _lpSortCriteria_ parameter, the table returns the current column set.</span></span> <span data-ttu-id="92d45-147">Порядок сортировки можно извлечь путем вызова метода [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) таблицы.</span><span class="sxs-lookup"><span data-stu-id="92d45-147">The current sort order can be retrieved by calling the table's [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
<span data-ttu-id="92d45-148">Все закладки для таблицы становятся недействительными и должны быть удалены, когда выполняется вызов для **SortTable** и необходимо задать закладку BOOKMARK_CURRENT, которое указывает текущую позицию курсора в начало таблицы.</span><span class="sxs-lookup"><span data-stu-id="92d45-148">All bookmarks for a table are invalidated and should be deleted when a call to **SortTable** is made, and the BOOKMARK_CURRENT bookmark that indicates the current cursor position, should be set to the beginning of the table.</span></span> 
  
<span data-ttu-id="92d45-149">Если сортируется на столбец, который содержит свойством без установленного флага MVI_FLAG значения в столбцах обрабатывается как полностью упорядоченном кортеж.</span><span class="sxs-lookup"><span data-stu-id="92d45-149">If you are sorting on a column that contains a multivalued property without the MVI_FLAG flag set, the column's values are treated as a completely ordered tuple.</span></span> <span data-ttu-id="92d45-150">Сравнение двух многозначных столбцов сравнивает элементы столбцов в порядке, отчетов отношения столбцов в первом неравенство и возвращает равенства только в том случае, если сравниваемые столбцы содержат те же значения, в том же порядке.</span><span class="sxs-lookup"><span data-stu-id="92d45-150">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality, and returns equality only if the columns being compared contain the same values in the same order.</span></span> <span data-ttu-id="92d45-151">Если один столбец значений меньше, чем другое, переданные отношения, является значение null на другое значение.</span><span class="sxs-lookup"><span data-stu-id="92d45-151">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="92d45-152">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="92d45-152">Notes to callers</span></span>

<span data-ttu-id="92d45-153">**SortTable** работает синхронно, если не выбрано флаги.</span><span class="sxs-lookup"><span data-stu-id="92d45-153">**SortTable** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="92d45-154">Если установлен флаг TBL_BATCH **SortTable** откладывает сортировку, если не запрашивать данные.</span><span class="sxs-lookup"><span data-stu-id="92d45-154">If you set the TBL_BATCH flag, **SortTable** postpones the sort operation unless you request the data.</span></span> <span data-ttu-id="92d45-155">Если установлен флаг TBL_ASYNC, **SortTable** работает асинхронно, потенциально возврат до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="92d45-155">If the TBL_ASYNC flag is set, **SortTable** operates asynchronously, potentially returning before the completion of the operation.</span></span> 
  
<span data-ttu-id="92d45-156">Вызовите метод [IMAPITable::Abort](imapitable-abort.md) для остановки асинхронной операции в процессе выполнения, если порядка сортировки необходимо выполнить немедленно.</span><span class="sxs-lookup"><span data-stu-id="92d45-156">Call the [IMAPITable::Abort](imapitable-abort.md) method to stop an asynchronous operation in progress if your sort must be done immediately.</span></span> <span data-ttu-id="92d45-157">Если **SortTable** не может продолжать работу, так как один или несколько асинхронной операции для таблицы находятся в процессе выполнения, возвращает MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="92d45-157">If **SortTable** cannot continue because one or more asynchronous operations on the table are in progress, it returns MAPI_E_BUSY.</span></span> 
  
<span data-ttu-id="92d45-158">Для достижения наилучшей производительности вызова **метода SetColumns** для настройки набора столбцов таблицы и **ограничить** для ограничения количество строк в таблице, прежде чем вызывать **SortTable** для выполнения сортировки.</span><span class="sxs-lookup"><span data-stu-id="92d45-158">For best performance, call **SetColumns** to customize the table's column set and **Restrict** to limit the number of rows in the table before you call **SortTable** to perform the sort.</span></span> 
  
<span data-ttu-id="92d45-159">Каждый раз, когда происходит сбой **SortTable** , порядок сортировки, который был фактически до сбоя — это по-прежнему в силу.</span><span class="sxs-lookup"><span data-stu-id="92d45-159">Whenever **SortTable** fails, the sort order that was in effect before the failure is still in effect.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="92d45-160">См. также</span><span class="sxs-lookup"><span data-stu-id="92d45-160">See also</span></span>

- [<span data-ttu-id="92d45-161">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="92d45-161">IMAPITable::Abort</span></span>](imapitable-abort.md)
- [<span data-ttu-id="92d45-162">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="92d45-162">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
- [<span data-ttu-id="92d45-163">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="92d45-163">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
- [<span data-ttu-id="92d45-164">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="92d45-164">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
- [<span data-ttu-id="92d45-165">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="92d45-165">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
- [<span data-ttu-id="92d45-166">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="92d45-166">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="92d45-167">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="92d45-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

