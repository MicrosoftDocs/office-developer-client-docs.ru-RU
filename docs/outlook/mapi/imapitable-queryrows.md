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
ms.openlocfilehash: a6659f64f6e8d2e3dc61819b2263efe672cdd15c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809242"
---
# <a name="imapitablequeryrows"></a><span data-ttu-id="2d724-103">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="2d724-103">IMAPITable::QueryRows</span></span>

  
  
<span data-ttu-id="2d724-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2d724-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2d724-105">Возвращает один или несколько строк из таблицы, начиная с текущей позиции курсора.</span><span class="sxs-lookup"><span data-stu-id="2d724-105">Returns one or more rows from a table, beginning at the current cursor position.</span></span>
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a><span data-ttu-id="2d724-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2d724-106">Parameters</span></span>

 <span data-ttu-id="2d724-107">_lRowCount_</span><span class="sxs-lookup"><span data-stu-id="2d724-107">_lRowCount_</span></span>
  
> <span data-ttu-id="2d724-108">[in] Максимальное число возвращаемых строк.</span><span class="sxs-lookup"><span data-stu-id="2d724-108">[in] Maximum number of rows to be returned.</span></span>
    
 <span data-ttu-id="2d724-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2d724-109">_ulFlags_</span></span>
  
> <span data-ttu-id="2d724-110">[in] Битовая маска флаги, определяющие, каким образом возвращенных строк.</span><span class="sxs-lookup"><span data-stu-id="2d724-110">[in] Bitmask of flags that control how rows are returned.</span></span> <span data-ttu-id="2d724-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="2d724-111">The following flag can be set:</span></span>
    
<span data-ttu-id="2d724-112">TBL_NOADVANCE</span><span class="sxs-lookup"><span data-stu-id="2d724-112">TBL_NOADVANCE</span></span> 
  
> <span data-ttu-id="2d724-113">Предотвращает переход из-за извлечения строк курсора.</span><span class="sxs-lookup"><span data-stu-id="2d724-113">Prevents the cursor from advancing as a result of the row retrieval.</span></span> <span data-ttu-id="2d724-114">Если установлен флаг TBL_NOADVANCE, возвращаемые точек курсор в первую строку.</span><span class="sxs-lookup"><span data-stu-id="2d724-114">If the TBL_NOADVANCE flag is set, the cursor points to the first row returned.</span></span> <span data-ttu-id="2d724-115">Если флаг TBL_NOADVANCE не установлен, курсор указывает строка, следующая последней строки.</span><span class="sxs-lookup"><span data-stu-id="2d724-115">If the TBL_NOADVANCE flag is not set, the cursor points to the row following the last row returned.</span></span>
    
 <span data-ttu-id="2d724-116">_lppRows_</span><span class="sxs-lookup"><span data-stu-id="2d724-116">_lppRows_</span></span>
  
> <span data-ttu-id="2d724-117">[out] Указатель на указатель на структуру [SRowSet](srowset.md) руку строк таблицы.</span><span class="sxs-lookup"><span data-stu-id="2d724-117">[out] Pointer to a pointer to an [SRowSet](srowset.md) structure holding the table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2d724-118">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="2d724-118">Return value</span></span>

<span data-ttu-id="2d724-119">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="2d724-119">S_OK</span></span> 
  
> <span data-ttu-id="2d724-120">Строки были успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="2d724-120">The rows were successfully returned.</span></span>
    
<span data-ttu-id="2d724-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="2d724-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="2d724-122">В, не позволяющей операции извлечения строк из запуск выполняется другой операции.</span><span class="sxs-lookup"><span data-stu-id="2d724-122">Another operation is in progress that prevents the row retrieval operation from starting.</span></span> <span data-ttu-id="2d724-123">В процессе выполнения операции должны выполнить либо должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="2d724-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="2d724-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2d724-124">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="2d724-125">Параметр _IRowCount_ присваивается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="2d724-125">The  _IRowCount_ parameter is set to zero.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2d724-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="2d724-126">Remarks</span></span>

<span data-ttu-id="2d724-127">Метод **IMAPITable::QueryRows** получает один или несколько строк данных из таблицы.</span><span class="sxs-lookup"><span data-stu-id="2d724-127">The **IMAPITable::QueryRows** method gets one or more rows of data from a table.</span></span> <span data-ttu-id="2d724-128">Значение параметра _IRowCount_ влияет на начальную точку для извлечения.</span><span class="sxs-lookup"><span data-stu-id="2d724-128">The value of the  _IRowCount_ parameter affects the starting point for the retrieval.</span></span> <span data-ttu-id="2d724-129">При положительном _IRowCount_ строк считываются вперед, начиная с текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="2d724-129">If  _IRowCount_ is positive, rows are read in a forward direction, starting at the current position.</span></span> <span data-ttu-id="2d724-130">Если отрицательно _IRowCount_ **QueryRows** сбрасывает начальной точки при перемещении назад на указанное число строк.</span><span class="sxs-lookup"><span data-stu-id="2d724-130">If  _IRowCount_ is negative, **QueryRows** resets the starting point by moving backward the indicated number of rows.</span></span> <span data-ttu-id="2d724-131">После сброса курсор, строки считываются в очереди.</span><span class="sxs-lookup"><span data-stu-id="2d724-131">After the cursor is reset, rows are read in forward order.</span></span> 
  
<span data-ttu-id="2d724-132">Член **cRows** в структуре [SRowSet](srowset.md) указывает параметр _lppRows_ указывает число строк, возвращаемых.</span><span class="sxs-lookup"><span data-stu-id="2d724-132">The **cRows** member in the [SRowSet](srowset.md) structure pointed to by the  _lppRows_ parameter indicates the number of rows returned.</span></span> <span data-ttu-id="2d724-133">Если не возвращается ноль строки:</span><span class="sxs-lookup"><span data-stu-id="2d724-133">If zero rows are returned:</span></span> 
  
- <span data-ttu-id="2d724-134">Курсор уже была находится в начале таблицы и значение _IRowCount_ является отрицательным.</span><span class="sxs-lookup"><span data-stu-id="2d724-134">The cursor was already positioned at the beginning of the table and the value of  _IRowCount_ is negative.</span></span> <span data-ttu-id="2d724-135">- Или -</span><span class="sxs-lookup"><span data-stu-id="2d724-135">-Or-</span></span> 
    
- <span data-ttu-id="2d724-136">Курсор уже была находится в конце таблицы и значение _IRowCount_ является положительным.</span><span class="sxs-lookup"><span data-stu-id="2d724-136">The cursor was already positioned at the end of the table and the value of  _IRowCount_ is positive.</span></span> 
    
<span data-ttu-id="2d724-137">Число столбцов и их порядок аналогична для каждой строки.</span><span class="sxs-lookup"><span data-stu-id="2d724-137">The number of columns and their ordering is the same for each row.</span></span> <span data-ttu-id="2d724-138">Если свойство не существует для строки или Ошибка чтения свойство, структура **SPropValue** для свойства в строке содержит следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2d724-138">If a property does not exist for a row or there is an error reading a property, the **SPropValue** structure for the property in the row contains the following values:</span></span> 
  
- <span data-ttu-id="2d724-139">PT_ERROR тип свойства в элементе **ulPropTag** .</span><span class="sxs-lookup"><span data-stu-id="2d724-139">PT_ERROR for the property type in the **ulPropTag** member.</span></span> 
    
- <span data-ttu-id="2d724-140">MAPI_E_NOT_FOUND элемент **значения** .</span><span class="sxs-lookup"><span data-stu-id="2d724-140">MAPI_E_NOT_FOUND for the **Value** member.</span></span> 
    
<span data-ttu-id="2d724-141">Объем памяти, используемый для структур [SPropValue](spropvalue.md) в наборе строк, на который указывает параметр _lppRows_ необходимо выделить отдельно и освободить для каждой строки.</span><span class="sxs-lookup"><span data-stu-id="2d724-141">Memory used for the [SPropValue](spropvalue.md) structures in the row set pointed to by the  _lppRows_ parameter must be separately allocated and freed for each row.</span></span> <span data-ttu-id="2d724-142">Используйте [MAPIFreeBuffer](mapifreebuffer.md) для освобождения структур значение свойства и чтобы освободить место на строку параметры.</span><span class="sxs-lookup"><span data-stu-id="2d724-142">Use [MAPIFreeBuffer](mapifreebuffer.md) to free the property value structures and to free the row set.</span></span> <span data-ttu-id="2d724-143">При вызове **QueryRows** возвращает нуль, тем не менее, указывающее начала или окончания в таблице только структура **SRowSet** самого должен освободить.</span><span class="sxs-lookup"><span data-stu-id="2d724-143">When a call to **QueryRows** returns zero, however, indicating the beginning or end of the table, only the **SRowSet** structure itself needs to be freed.</span></span> <span data-ttu-id="2d724-144">Дополнительные сведения о том, как выделить и освободить память в структуре **SRowSet** можно [Памяти ADRLIST и SRowSet структур](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="2d724-144">For more information about how to allocate and free memory in an **SRowSet** structure, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
<span data-ttu-id="2d724-145">Строк, возвращаемых и порядок, в котором они возвращаются, зависят от того, является ли успешные вызовы были внесены [IMAPITable::Restrict](imapitable-restrict.md) и [IMAPITable::SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="2d724-145">The rows that are returned and the order in which they are returned depend on whether or not successful calls have been made to [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::SortTable](imapitable-sorttable.md).</span></span> <span data-ttu-id="2d724-146">**Ограничить** фильтр строк из представления, использование которых приводит **QueryRows** для возврата только строки, соответствующие критериям указанного в ограничении.</span><span class="sxs-lookup"><span data-stu-id="2d724-146">**Restrict** filters rows from the view, causing **QueryRows** to return only the rows that match the criteria specified in the restriction.</span></span> <span data-ttu-id="2d724-147">**SortTable** устанавливает стандартный или порядок сортировки по категориям влияния на последовательности строк, возвращенных **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="2d724-147">**SortTable** establishes a standard or categorized sort order, affecting the sequence of rows returned by **QueryRows**.</span></span> <span data-ttu-id="2d724-148">В порядке, указанном в структуре [SSortOrderSet](ssortorderset.md) , переданной в **SortTable**, возвращенных строк.</span><span class="sxs-lookup"><span data-stu-id="2d724-148">The returned rows are in the order specified in the [SSortOrderSet](ssortorderset.md) structure passed to **SortTable**.</span></span>
  
<span data-ttu-id="2d724-149">Для каждой строки, возвращаемой столбцов и порядок, в котором они возвращаются, зависят от того, является ли успешного вызова совершена [IMAPITable::SetColumns](imapitable-setcolumns.md).</span><span class="sxs-lookup"><span data-stu-id="2d724-149">The columns returned for each row and the order in which they are returned depend on whether or not a successful call has been made to [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> <span data-ttu-id="2d724-150">**Метода SetColumns** устанавливает набор столбцов Указание свойств, которые будут включены в столбцы в таблице и порядок, в котором они должны быть включены.</span><span class="sxs-lookup"><span data-stu-id="2d724-150">**SetColumns** establishes a column set, specifying the properties to be included in columns in the table and the order in which they should be included.</span></span> <span data-ttu-id="2d724-151">Если выполнен вызов **метода SetColumns** , определенного столбцов в каждой строке и порядок их столбцов соответствует столбца, указанного в вызове набора.</span><span class="sxs-lookup"><span data-stu-id="2d724-151">If a **SetColumns** call has been made, the particular columns in each row and the order of those columns match the column set specified in the call.</span></span> <span data-ttu-id="2d724-152">Если вызов **метода SetColumns** таблице возвращает его набор столбцов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2d724-152">If no **SetColumns** call has been made, the table returns its default column set.</span></span> 
  
<span data-ttu-id="2d724-153">Если ни один из них не выполнена, **QueryRows** возвращает все строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="2d724-153">If none of these calls has been made, **QueryRows** returns all of the rows in the table.</span></span> <span data-ttu-id="2d724-154">Каждая строка содержит столбец по умолчанию, задайте в порядке, по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2d724-154">Each row contains the default column set in default order.</span></span> 
  
<span data-ttu-id="2d724-155">При наборе столбцов установить в вызове [IMAPITable::SetColumns](imapitable-setcolumns.md) включает столбцы, задайте значение PR_NULL, [SPropValue](spropvalue.md) массив в наборе строк, возвращаемых в _lppRows_ будет содержать пустых ячеек.</span><span class="sxs-lookup"><span data-stu-id="2d724-155">When the column set established in a call to [IMAPITable::SetColumns](imapitable-setcolumns.md) includes columns set to PR_NULL, the [SPropValue](spropvalue.md) array within the row set returned in  _lppRows_ will contain empty slots.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2d724-156">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="2d724-156">Notes to implementers</span></span>

<span data-ttu-id="2d724-157">Можно разрешить вызывающего для запроса не поддерживается столбцов должны быть включены в набор столбцов.</span><span class="sxs-lookup"><span data-stu-id="2d724-157">You can allow a caller to request an unsupported column to be included in the column set.</span></span> <span data-ttu-id="2d724-158">При возникновении этой ошибки поместите PT_ERROR в свойство типа части свойство tag и MAPI_E_NOT_FOUND в значение свойства в столбце не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2d724-158">When this occurs, place PT_ERROR in the property type portion of the property tag and MAPI_E_NOT_FOUND in the property value for the unsupported column.</span></span> 
  
<span data-ttu-id="2d724-159">Считать число строк запроса, а не является обязательным требованием.</span><span class="sxs-lookup"><span data-stu-id="2d724-159">Treat the row count as a request rather than a requirement.</span></span> <span data-ttu-id="2d724-160">Вы можете вернуться в любом из строки, если нет ни одной строки в направлении запроса к номеру запрошено.</span><span class="sxs-lookup"><span data-stu-id="2d724-160">You can return anywhere from zero rows, if there are no rows in the direction of the query, to the number requested.</span></span> 
  
<span data-ttu-id="2d724-161">Возвращает только строки, пользователь увидит при запросе строк из него по категориям, позволяя вызывающему допустимый допущений о области данных и избежать дополнительных действий.</span><span class="sxs-lookup"><span data-stu-id="2d724-161">Return only the rows that the user will see when rows are requested from a categorized table view, allowing the caller to make valid assumptions about the scope of the data and avoid extra work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2d724-162">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="2d724-162">Notes to callers</span></span>

<span data-ttu-id="2d724-163">Как правило, появятся числом строк, как было задано с помощью параметра _lRowCount_ .</span><span class="sxs-lookup"><span data-stu-id="2d724-163">Usually you will end up with as many rows as you have specified in the  _lRowCount_ parameter.</span></span> <span data-ttu-id="2d724-164">Тем не менее ограничения памяти или реализации проблемы и по достижении операции начала или окончания таблицы преждевременно, **QueryRows** возвращает меньше строк, чем запрошено.</span><span class="sxs-lookup"><span data-stu-id="2d724-164">However, when memory or implementation limits are an issue or when the operation reaches the beginning or end of the table prematurely, **QueryRows** will return less rows than requested.</span></span> 
  
<span data-ttu-id="2d724-165">Если **QueryRows** возвращает MAPI_E_BUSY, вызовите метод [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) и повторите попытку вызова **QueryRows** после завершения асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="2d724-165">If **QueryRows** returns MAPI_E_BUSY, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method and retry the call to **QueryRows** when the asynchronous operation is complete.</span></span> 
  
<span data-ttu-id="2d724-166">При вызове **QueryRows**, обратите внимание, что время асинхронного уведомления может вызвать набор строк, что можно получить из **QueryRows** не будет точно представлять базовые данные.</span><span class="sxs-lookup"><span data-stu-id="2d724-166">When calling **QueryRows**, be aware that the timing of asynchronous notifications can potentially cause the row set that you get back from **QueryRows** not to accurately represent the underlying data.</span></span> <span data-ttu-id="2d724-167">Например задайте вызов **QueryRows** в таблице ниже содержимое папки что удаление сообщения, но до получения соответствующее уведомление приведет к удаленной строки должно быть возвращено в строке.</span><span class="sxs-lookup"><span data-stu-id="2d724-167">For example, a call to **QueryRows** to a folder's contents table following the deletion of a message but prior to the receipt of the corresponding notification will cause the deleted row to be returned in the row set.</span></span> <span data-ttu-id="2d724-168">Всегда ожидают уведомления поступать перед обновлением пользователя представление данных.</span><span class="sxs-lookup"><span data-stu-id="2d724-168">Always wait for a notification to arrive before updating the user's view of the data.</span></span> 
  
<span data-ttu-id="2d724-169">Дополнительные сведения о получении строк из таблицы можно [Извлечение данных из строк таблицы](retrieving-data-from-table-rows.md).</span><span class="sxs-lookup"><span data-stu-id="2d724-169">For more information about retrieving rows from tables, see [Retrieving Data from Table Rows](retrieving-data-from-table-rows.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2d724-170">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="2d724-170">MFCMAPI reference</span></span>

<span data-ttu-id="2d724-171">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="2d724-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2d724-172">**����**</span><span class="sxs-lookup"><span data-stu-id="2d724-172">**File**</span></span>|<span data-ttu-id="2d724-173">**�������**</span><span class="sxs-lookup"><span data-stu-id="2d724-173">**Function**</span></span>|<span data-ttu-id="2d724-174">**�����������**</span><span class="sxs-lookup"><span data-stu-id="2d724-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2d724-175">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="2d724-175">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="2d724-176">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="2d724-176">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="2d724-177">Mfcmapi (en) использует метод **IMAPITable::QueryRows** для извлечения строк таблицы для загрузки в представлении.</span><span class="sxs-lookup"><span data-stu-id="2d724-177">MFCMAPI uses the **IMAPITable::QueryRows** method to retrieve rows in the table to load into the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2d724-178">См. также</span><span class="sxs-lookup"><span data-stu-id="2d724-178">See also</span></span>



[<span data-ttu-id="2d724-179">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="2d724-179">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="2d724-180">FreeProws</span><span class="sxs-lookup"><span data-stu-id="2d724-180">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="2d724-181">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="2d724-181">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="2d724-182">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="2d724-182">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="2d724-183">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="2d724-183">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="2d724-184">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="2d724-184">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="2d724-185">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="2d724-185">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="2d724-186">SRow</span><span class="sxs-lookup"><span data-stu-id="2d724-186">SRow</span></span>](srow.md)
  
[<span data-ttu-id="2d724-187">SRowSet</span><span class="sxs-lookup"><span data-stu-id="2d724-187">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="2d724-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2d724-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="2d724-189">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="2d724-189">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

