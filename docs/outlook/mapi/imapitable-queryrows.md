---
title: IMAPITableQueryRows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryRows
api_type:
- COM
ms.assetid: f26384f1-467e-4343-92b3-0425da9d2123
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 26d6ffe66a5e7749c9d8c4e5210e9f72de808932
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416295"
---
# <a name="imapitablequeryrows"></a><span data-ttu-id="fa7bd-103">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="fa7bd-103">IMAPITable::QueryRows</span></span>

  
  
<span data-ttu-id="fa7bd-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa7bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa7bd-105">Возвращает одну или несколько строк из таблицы, начиная с текущего положения курсора.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-105">Returns one or more rows from a table, beginning at the current cursor position.</span></span>
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a><span data-ttu-id="fa7bd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa7bd-106">Parameters</span></span>

 <span data-ttu-id="fa7bd-107">_lRowCount_</span><span class="sxs-lookup"><span data-stu-id="fa7bd-107">_lRowCount_</span></span>
  
> <span data-ttu-id="fa7bd-108">[in] Максимальное число возвращаемых строк.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-108">[in] Maximum number of rows to be returned.</span></span>
    
 <span data-ttu-id="fa7bd-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fa7bd-109">_ulFlags_</span></span>
  
> <span data-ttu-id="fa7bd-110">[in] Битоваяmas флагов, которые контролируют, как возвращаются строки.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-110">[in] Bitmask of flags that control how rows are returned.</span></span> <span data-ttu-id="fa7bd-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="fa7bd-111">The following flag can be set:</span></span>
    
<span data-ttu-id="fa7bd-112">TBL_NOADVANCE</span><span class="sxs-lookup"><span data-stu-id="fa7bd-112">TBL_NOADVANCE</span></span> 
  
> <span data-ttu-id="fa7bd-113">Предотвращает наступание курсора в результате искомой строки.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-113">Prevents the cursor from advancing as a result of the row retrieval.</span></span> <span data-ttu-id="fa7bd-114">Если установлен TBL_NOADVANCE, курсор указывает на первую возвращенную строку.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-114">If the TBL_NOADVANCE flag is set, the cursor points to the first row returned.</span></span> <span data-ttu-id="fa7bd-115">Если флаг TBL_NOADVANCE не установлен, курсор указывает на строку после последней возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-115">If the TBL_NOADVANCE flag is not set, the cursor points to the row following the last row returned.</span></span>
    
 <span data-ttu-id="fa7bd-116">_lppRows_</span><span class="sxs-lookup"><span data-stu-id="fa7bd-116">_lppRows_</span></span>
  
> <span data-ttu-id="fa7bd-117">[out] Указатель на указатель на структуру [SRowSet,](srowset.md) удерживая строки таблицы.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-117">[out] Pointer to a pointer to an [SRowSet](srowset.md) structure holding the table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fa7bd-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa7bd-118">Return value</span></span>

<span data-ttu-id="fa7bd-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="fa7bd-119">S_OK</span></span> 
  
> <span data-ttu-id="fa7bd-120">Строки были успешно возвращены.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-120">The rows were successfully returned.</span></span>
    
<span data-ttu-id="fa7bd-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="fa7bd-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="fa7bd-122">В настоящее время идет другая операция, которая не позволяет начать операцию ирисовки строк.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-122">Another operation is in progress that prevents the row retrieval operation from starting.</span></span> <span data-ttu-id="fa7bd-123">Либо операция должна быть разрешена для завершения, либо она должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="fa7bd-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fa7bd-124">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="fa7bd-125">Для  _параметра IRowCount_ задан ноль.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-125">The  _IRowCount_ parameter is set to zero.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fa7bd-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="fa7bd-126">Remarks</span></span>

<span data-ttu-id="fa7bd-127">Метод **IMAPITable::QueryRows** получает одну или несколько строк данных из таблицы.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-127">The **IMAPITable::QueryRows** method gets one or more rows of data from a table.</span></span> <span data-ttu-id="fa7bd-128">Значение параметра  _IRowCount_ влияет на отправную точку ищего.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-128">The value of the  _IRowCount_ parameter affects the starting point for the retrieval.</span></span> <span data-ttu-id="fa7bd-129">Если  _IRowCount_ положительное, строки считыются в направлении вперед, начиная с текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-129">If  _IRowCount_ is positive, rows are read in a forward direction, starting at the current position.</span></span> <span data-ttu-id="fa7bd-130">Если  _IRowCount_ отрицательное, **QueryRows** сбрасывает началую точку, перемещая назад задаваемого числа строк.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-130">If  _IRowCount_ is negative, **QueryRows** resets the starting point by moving backward the indicated number of rows.</span></span> <span data-ttu-id="fa7bd-131">После сброса курсора строки считыются в порядке переадселки.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-131">After the cursor is reset, rows are read in forward order.</span></span> 
  
<span data-ttu-id="fa7bd-132">Член **cRows** в структуре [SRowSet,](srowset.md) на который указывает параметр  _lppRows,_ указывает количество возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-132">The **cRows** member in the [SRowSet](srowset.md) structure pointed to by the  _lppRows_ parameter indicates the number of rows returned.</span></span> <span data-ttu-id="fa7bd-133">Если возвращается ноль строк:</span><span class="sxs-lookup"><span data-stu-id="fa7bd-133">If zero rows are returned:</span></span> 
  
- <span data-ttu-id="fa7bd-134">Курсор уже был в начале таблицы, а значение  _IRowCount_ отрицательное.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-134">The cursor was already positioned at the beginning of the table and the value of  _IRowCount_ is negative.</span></span> <span data-ttu-id="fa7bd-135">-Or-</span><span class="sxs-lookup"><span data-stu-id="fa7bd-135">-Or-</span></span> 
    
- <span data-ttu-id="fa7bd-136">Курсор уже находится в конце таблицы, а  _значение IRowCount_ положительное.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-136">The cursor was already positioned at the end of the table and the value of  _IRowCount_ is positive.</span></span> 
    
<span data-ttu-id="fa7bd-137">Количество столбцов и их порядок одинаковы для каждой строки.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-137">The number of columns and their ordering is the same for each row.</span></span> <span data-ttu-id="fa7bd-138">Если свойство не существует для строки или при чтении свойства произошла ошибка, **структура SPropValue** для свойства в строке содержит следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fa7bd-138">If a property does not exist for a row or there is an error reading a property, the **SPropValue** structure for the property in the row contains the following values:</span></span> 
  
- <span data-ttu-id="fa7bd-139">PT_ERROR для типа свойства в члене **ulPropTag.**</span><span class="sxs-lookup"><span data-stu-id="fa7bd-139">PT_ERROR for the property type in the **ulPropTag** member.</span></span> 
    
- <span data-ttu-id="fa7bd-140">MAPI_E_NOT_FOUND для члена **Value.**</span><span class="sxs-lookup"><span data-stu-id="fa7bd-140">MAPI_E_NOT_FOUND for the **Value** member.</span></span> 
    
<span data-ttu-id="fa7bd-141">Память, используемая для структур [SPropValue](spropvalue.md) в наборе строк, на которые указывает параметр  _lppRows,_ должна быть выделена отдельно и освобождена для каждой строки.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-141">Memory used for the [SPropValue](spropvalue.md) structures in the row set pointed to by the  _lppRows_ parameter must be separately allocated and freed for each row.</span></span> <span data-ttu-id="fa7bd-142">Используйте [MAPIFreeBuffer,](mapifreebuffer.md) чтобы освободить структуры значений свойств и освободить набор строк.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-142">Use [MAPIFreeBuffer](mapifreebuffer.md) to free the property value structures and to free the row set.</span></span> <span data-ttu-id="fa7bd-143">Однако когда вызов **QueryRows** возвращает ноль, указывающий начало или конец таблицы, необходимо освободить только сам **набор SRowSet.**</span><span class="sxs-lookup"><span data-stu-id="fa7bd-143">When a call to **QueryRows** returns zero, however, indicating the beginning or end of the table, only the **SRowSet** structure itself needs to be freed.</span></span> <span data-ttu-id="fa7bd-144">Дополнительные сведения о выделении и выделении памяти в структуре **SRowSet** см. в под управлением памятью [для ADRLIST и структур SRowSet.](managing-memory-for-adrlist-and-srowset-structures.md)</span><span class="sxs-lookup"><span data-stu-id="fa7bd-144">For more information about how to allocate and free memory in an **SRowSet** structure, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
<span data-ttu-id="fa7bd-145">Возвращаемые строки и порядок их возврата зависят от того, были ли выполнены успешные вызовы [IMAPITable::Restrict](imapitable-restrict.md) и [IMAPITable::SortTable.](imapitable-sorttable.md)</span><span class="sxs-lookup"><span data-stu-id="fa7bd-145">The rows that are returned and the order in which they are returned depend on whether or not successful calls have been made to [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::SortTable](imapitable-sorttable.md).</span></span> <span data-ttu-id="fa7bd-146">**Ограничение** строк фильтров из представления, в результате чего **QueryRows** возвращает только строки, которые соответствуют критериям, указанным в ограничении.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-146">**Restrict** filters rows from the view, causing **QueryRows** to return only the rows that match the criteria specified in the restriction.</span></span> <span data-ttu-id="fa7bd-147">**SortTable** устанавливает стандартный или упорядоченный порядок сортировки, влияющий на последовательность строк, возвращаемых **QueryRows.**</span><span class="sxs-lookup"><span data-stu-id="fa7bd-147">**SortTable** establishes a standard or categorized sort order, affecting the sequence of rows returned by **QueryRows**.</span></span> <span data-ttu-id="fa7bd-148">Возвращаемые строки находятся в порядке, указанном в структуре [SSortOrderSet,](ssortorderset.md) переданном **в SortTable.**</span><span class="sxs-lookup"><span data-stu-id="fa7bd-148">The returned rows are in the order specified in the [SSortOrderSet](ssortorderset.md) structure passed to **SortTable**.</span></span>
  
<span data-ttu-id="fa7bd-149">Столбцы, возвращаемые для каждой строки, и порядок их возврата зависят от того, был ли выполнен успешный вызов [IMAPITable::SetColumns.](imapitable-setcolumns.md)</span><span class="sxs-lookup"><span data-stu-id="fa7bd-149">The columns returned for each row and the order in which they are returned depend on whether or not a successful call has been made to [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> <span data-ttu-id="fa7bd-150">**SetColumns** устанавливает набор столбцов, определяя свойства, которые необходимо включить в столбцы таблицы, и порядок, в котором они должны быть включены.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-150">**SetColumns** establishes a column set, specifying the properties to be included in columns in the table and the order in which they should be included.</span></span> <span data-ttu-id="fa7bd-151">Если был выполнен вызов **SetColumns,** определенные столбцы в каждой строке и порядок этих столбцов соответствуют набору столбцов, указанному в вызове.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-151">If a **SetColumns** call has been made, the particular columns in each row and the order of those columns match the column set specified in the call.</span></span> <span data-ttu-id="fa7bd-152">Если вызов **SetColumns** не выполнен, таблица возвращает набор столбцов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-152">If no **SetColumns** call has been made, the table returns its default column set.</span></span> 
  
<span data-ttu-id="fa7bd-153">Если ни один из этих вызовов не был выполнен, **QueryRows** возвращает все строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-153">If none of these calls has been made, **QueryRows** returns all of the rows in the table.</span></span> <span data-ttu-id="fa7bd-154">Каждая строка содержит набор столбцов по умолчанию в порядке по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-154">Each row contains the default column set in default order.</span></span> 
  
<span data-ttu-id="fa7bd-155">Когда набор столбцов, установленный в вызове [IMAPITable::SetColumns,](imapitable-setcolumns.md) включает столбцы, задаваемые как PR_NULL, массив [SPropValue в](spropvalue.md) наборе строк, возвращаемом  _в lppRows,_ будет содержать пустые слоты.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-155">When the column set established in a call to [IMAPITable::SetColumns](imapitable-setcolumns.md) includes columns set to PR_NULL, the [SPropValue](spropvalue.md) array within the row set returned in  _lppRows_ will contain empty slots.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="fa7bd-156">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="fa7bd-156">Notes to implementers</span></span>

<span data-ttu-id="fa7bd-157">Вы можете разрешить звонячему запрашивать неподдермеченный столбец, который должен быть включен в набор столбцов.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-157">You can allow a caller to request an unsupported column to be included in the column set.</span></span> <span data-ttu-id="fa7bd-158">В этом случае поместите PT_ERROR в часть типа свойства тега свойства, а MAPI_E_NOT_FOUND в значение свойства для неподтверганного столбца.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-158">When this occurs, place PT_ERROR in the property type portion of the property tag and MAPI_E_NOT_FOUND in the property value for the unsupported column.</span></span> 
  
<span data-ttu-id="fa7bd-159">Обрабатывайте количество строк как запрос, а не как требование.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-159">Treat the row count as a request rather than a requirement.</span></span> <span data-ttu-id="fa7bd-160">Вы можете вернуться в любом месте от нуля строк, если в направлении запроса нет строк, до запрашиваемого числа.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-160">You can return anywhere from zero rows, if there are no rows in the direction of the query, to the number requested.</span></span> 
  
<span data-ttu-id="fa7bd-161">Возвращает только строки, которые будут видеться пользователем при запросе строк из представления таблицы с классификацией, позволяя вызываемой стороне делать допустимые предположения об области данных и избегать дополнительной работы.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-161">Return only the rows that the user will see when rows are requested from a categorized table view, allowing the caller to make valid assumptions about the scope of the data and avoid extra work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="fa7bd-162">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="fa7bd-162">Notes to callers</span></span>

<span data-ttu-id="fa7bd-163">Обычно у вас будет столько строк, сколько указано в параметре _lRowCount._</span><span class="sxs-lookup"><span data-stu-id="fa7bd-163">Usually you will end up with as many rows as you have specified in the  _lRowCount_ parameter.</span></span> <span data-ttu-id="fa7bd-164">Однако если в памяти или реализации не существует проблем или операция достигает начала или окончания таблицы раньше времени, **QueryRows** возвращает меньше строк, чем запрашивается.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-164">However, when memory or implementation limits are an issue or when the operation reaches the beginning or end of the table prematurely, **QueryRows** will return less rows than requested.</span></span> 
  
<span data-ttu-id="fa7bd-165">Если **QueryRows** возвращает MAPI_E_BUSY, вызовите метод [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) и повторно выполните вызов **QueryRows** после завершения асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-165">If **QueryRows** returns MAPI_E_BUSY, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method and retry the call to **QueryRows** when the asynchronous operation is complete.</span></span> 
  
<span data-ttu-id="fa7bd-166">При **вызове QueryRows** следует помнить, что синхронизация асинхронных уведомлений может привести к тому, что набор строк, возвращаемой из **QueryRows,** не будет точно представлять данные, которые следует использовать.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-166">When calling **QueryRows**, be aware that the timing of asynchronous notifications can potentially cause the row set that you get back from **QueryRows** not to accurately represent the underlying data.</span></span> <span data-ttu-id="fa7bd-167">Например, вызов **QueryRows** в таблицу содержимого папки после удаления сообщения, но до получения соответствующего уведомления приведет к возвращению удаленной строки в наборе строк.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-167">For example, a call to **QueryRows** to a folder's contents table following the deletion of a message but prior to the receipt of the corresponding notification will cause the deleted row to be returned in the row set.</span></span> <span data-ttu-id="fa7bd-168">Всегда дождись поступления уведомления перед обновлением представления данных пользователем.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-168">Always wait for a notification to arrive before updating the user's view of the data.</span></span> 
  
<span data-ttu-id="fa7bd-169">Дополнительные сведения о том, как получить строки из таблиц, см. в этой [теме.](retrieving-data-from-table-rows.md)</span><span class="sxs-lookup"><span data-stu-id="fa7bd-169">For more information about retrieving rows from tables, see [Retrieving Data from Table Rows](retrieving-data-from-table-rows.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fa7bd-170">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="fa7bd-170">MFCMAPI reference</span></span>

<span data-ttu-id="fa7bd-171">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fa7bd-172">**Файл**</span><span class="sxs-lookup"><span data-stu-id="fa7bd-172">**File**</span></span>|<span data-ttu-id="fa7bd-173">**Функция**</span><span class="sxs-lookup"><span data-stu-id="fa7bd-173">**Function**</span></span>|<span data-ttu-id="fa7bd-174">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="fa7bd-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fa7bd-175">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="fa7bd-175">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="fa7bd-176">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="fa7bd-176">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="fa7bd-177">MFCMAPI использует метод **IMAPITable::QueryRows** для получения строк в таблице для загрузки в представление.</span><span class="sxs-lookup"><span data-stu-id="fa7bd-177">MFCMAPI uses the **IMAPITable::QueryRows** method to retrieve rows in the table to load into the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fa7bd-178">См. также</span><span class="sxs-lookup"><span data-stu-id="fa7bd-178">See also</span></span>



[<span data-ttu-id="fa7bd-179">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="fa7bd-179">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="fa7bd-180">FreeProws</span><span class="sxs-lookup"><span data-stu-id="fa7bd-180">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="fa7bd-181">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="fa7bd-181">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="fa7bd-182">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="fa7bd-182">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="fa7bd-183">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="fa7bd-183">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="fa7bd-184">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="fa7bd-184">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="fa7bd-185">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="fa7bd-185">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="fa7bd-186">SRow</span><span class="sxs-lookup"><span data-stu-id="fa7bd-186">SRow</span></span>](srow.md)
  
[<span data-ttu-id="fa7bd-187">SRowSet</span><span class="sxs-lookup"><span data-stu-id="fa7bd-187">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="fa7bd-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fa7bd-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="fa7bd-189">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="fa7bd-189">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

