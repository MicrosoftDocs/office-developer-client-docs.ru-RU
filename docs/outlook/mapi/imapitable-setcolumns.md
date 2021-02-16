---
title: IMAPITableSetColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SetColumns
api_type:
- COM
ms.assetid: 9a39cf8d-df0f-493c-b272-f15c65b3f15e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 897330feb216dbc3ab143378977c77141cf488f0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416351"
---
# <a name="imapitablesetcolumns"></a><span data-ttu-id="05b48-103">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="05b48-103">IMAPITable::SetColumns</span></span>

  
  
<span data-ttu-id="05b48-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05b48-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05b48-105">Определяет конкретные свойства и порядок их появления в качестве столбцов в таблице.</span><span class="sxs-lookup"><span data-stu-id="05b48-105">Defines the particular properties and order of properties to appear as columns in the table.</span></span>
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="05b48-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="05b48-106">Parameters</span></span>

 <span data-ttu-id="05b48-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="05b48-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="05b48-108">[in] Указатель на массив тегов свойств, определяющих свойства, которые необходимо включить в качестве столбцов в таблице.</span><span class="sxs-lookup"><span data-stu-id="05b48-108">[in] Pointer to an array of property tags identifying properties to be included as columns in the table.</span></span> <span data-ttu-id="05b48-109">Для части типа свойства каждого тега можно установить  допустимый тип или PR_NULL зарезервировать место для последующих дополнений.</span><span class="sxs-lookup"><span data-stu-id="05b48-109">The property type portion of each tag can be set to a valid type or to **PR_NULL** to reserve space for subsequent additions.</span></span> <span data-ttu-id="05b48-110">Для  _параметра lpPropTagArray_ нельзя установить NULL; каждая таблица должна иметь по крайней мере один столбец.</span><span class="sxs-lookup"><span data-stu-id="05b48-110">The  _lpPropTagArray_ parameter cannot be set to NULL; every table must have at least one column.</span></span> 
    
 <span data-ttu-id="05b48-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="05b48-111">_ulFlags_</span></span>
  
> <span data-ttu-id="05b48-112">[in] Битоваяmas флагов, которая управляет возвратом асинхронного вызова **SetColumns,** например, если **SetColumns** используется в уведомлении.</span><span class="sxs-lookup"><span data-stu-id="05b48-112">[in] Bitmask of flags that controls the return of an asynchronous call to **SetColumns**, for example when **SetColumns** is used in notification.</span></span> <span data-ttu-id="05b48-113">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="05b48-113">The following flags can be set:</span></span> 
    
<span data-ttu-id="05b48-114">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="05b48-114">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="05b48-115">Запрашивает выполнение операции настройки столбца асинхронно, из-за чего **SetColumns** потенциально возвращается до полного завершения операции.</span><span class="sxs-lookup"><span data-stu-id="05b48-115">Requests that the column setting operation be performed asynchronously causing **SetColumns** to potentially return before the operation has fully completed.</span></span> 
    
<span data-ttu-id="05b48-116">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="05b48-116">TBL_BATCH</span></span> 
  
> <span data-ttu-id="05b48-117">Позволяет таблице отложить операцию настройки столбца до тех пор, пока данные не потребуются.</span><span class="sxs-lookup"><span data-stu-id="05b48-117">Permits the table to postpone the column setting operation until the data is actually required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="05b48-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="05b48-118">Return value</span></span>

<span data-ttu-id="05b48-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="05b48-119">S_OK</span></span> 
  
> <span data-ttu-id="05b48-120">Операция настройки столбца прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="05b48-120">The column setting operation was successful.</span></span>
    
<span data-ttu-id="05b48-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="05b48-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="05b48-122">В настоящее время идет другая операция, которая препятствует запуску операции настройки столбца.</span><span class="sxs-lookup"><span data-stu-id="05b48-122">Another operation is in progress that prevents the column setting operation from starting.</span></span> <span data-ttu-id="05b48-123">Либо операция должна быть разрешена для завершения, либо она должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="05b48-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="05b48-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="05b48-124">Remarks</span></span>

<span data-ttu-id="05b48-125">Набор столбцов таблицы — это группа свойств, которые составляют столбцы для строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="05b48-125">The column set of a table is the group of properties that make up the columns for the rows in the table.</span></span> <span data-ttu-id="05b48-126">Существует набор столбцов по умолчанию для каждого типа таблицы.</span><span class="sxs-lookup"><span data-stu-id="05b48-126">There is a default column set for each type of table.</span></span> <span data-ttu-id="05b48-127">Набор столбцов по умолчанию состоит из свойств, которые автоматически включает в себя реализутель таблицы.</span><span class="sxs-lookup"><span data-stu-id="05b48-127">The default column set is made up of the properties that the table implementer automatically includes.</span></span> <span data-ttu-id="05b48-128">Пользователи таблицы могут изменить этот набор по умолчанию, вызывая метод **IMAPITable::SetColumns.**</span><span class="sxs-lookup"><span data-stu-id="05b48-128">Table users can alter this default set by calling the **IMAPITable::SetColumns** method.</span></span> <span data-ttu-id="05b48-129">Они могут запросить, чтобы другие столбцы были добавлены в набор по умолчанию, если реализутель таблицы поддерживает их удаление столбцов или чтобы изменить порядок столбцов.</span><span class="sxs-lookup"><span data-stu-id="05b48-129">They can request that other columns be added to the default set if the table implementer supports them that columns be removed, or that the order of columns be changed.</span></span> <span data-ttu-id="05b48-130">**SetColumns** указывает столбцы, которые возвращаются с каждой строкой, и порядок этих столбцов в строке.</span><span class="sxs-lookup"><span data-stu-id="05b48-130">**SetColumns** specifies the columns that are returned with each row and the order of these columns within the row.</span></span> 
  
<span data-ttu-id="05b48-131">Успешность операции **SetColumns** становится очевидной только после последующего вызова для получения данных таблицы.</span><span class="sxs-lookup"><span data-stu-id="05b48-131">The success of the **SetColumns** operation is apparent only after a subsequent call has been made to retrieve the data of the table.</span></span> <span data-ttu-id="05b48-132">После этого сообщается о любых ошибках.</span><span class="sxs-lookup"><span data-stu-id="05b48-132">It is then that any errors are reported.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="05b48-133">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="05b48-133">Notes to implementers</span></span>

<span data-ttu-id="05b48-134">Некоторые поставщики позволяют вызвать **SetColumns,** чтобы указать только столбцы таблицы, которые являются частью доступных столбцов для представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="05b48-134">Some providers allow a **SetColumns** call to order only table columns that are part of the available columns for a table view.</span></span> <span data-ttu-id="05b48-135">Другие поставщики позволяют **вызову SetColumns** указать все столбцы таблицы, включая те, которые содержат свойства, не в исходном наборе столбцов.</span><span class="sxs-lookup"><span data-stu-id="05b48-135">Other providers allow a **SetColumns** call to order all table columns, including those containing properties not in the original column set.</span></span> 
  
<span data-ttu-id="05b48-136">Если TBL_BATCH для асинхронных операций, поставщики должны возвращать тип свойства PT_ERROR и значение NULL для столбцов, которые не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="05b48-136">When TBL_BATCH is set for asynchronous operations, providers should return a property type of PT_ERROR and a property value of NULL for columns that are not supported.</span></span>
  
<span data-ttu-id="05b48-137">Вам не нужно отвечать на флаг TBL_ASYNC запроса на асинхронную операцию.</span><span class="sxs-lookup"><span data-stu-id="05b48-137">You do not need to respond to the TBL_ASYNC flag requesting that the operation be asynchronous.</span></span> <span data-ttu-id="05b48-138">Если определение набора асинхронных столбцов не поддерживается, выполните операцию синхронно.</span><span class="sxs-lookup"><span data-stu-id="05b48-138">If you do not support asynchronous column set definition, perform the operation synchronously.</span></span> <span data-ttu-id="05b48-139">Если вы можете поддерживать флаг TBL_ASYNC и еще одна асинхронная операция все еще находится в процессе выполнения, MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="05b48-139">If you can support the TBL_ASYNC flag and another asynchronous operation is still in progress, return MAPI_E_BUSY.</span></span> <span data-ttu-id="05b48-140">В противном случае S_OK независимо от того, поддерживаете ли вы все свойства, включенные в массив тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="05b48-140">Otherwise, return S_OK regardless of whether or not you support all of the properties included in the property tag array.</span></span> <span data-ttu-id="05b48-141">Ошибки, полученные из неподтверченных свойств, следует возвращать из методов **IMAPITable,** которые извлекает данные, например **QueryRows.**</span><span class="sxs-lookup"><span data-stu-id="05b48-141">Errors resulting from unsupported properties should be returned from **IMAPITable** methods that retrieve data, such as **QueryRows**.</span></span> 
  
<span data-ttu-id="05b48-142">Не создавать уведомления для строк таблиц, скрытых из представления вызовами **ограничения.**</span><span class="sxs-lookup"><span data-stu-id="05b48-142">Do not generate notifications for table rows that are hidden from view by calls to **Restrict**.</span></span> 
  
<span data-ttu-id="05b48-143">При отправке уведомлений о таблице порядок свойств в члене строки структуры [TABLE_NOTIFICATION](table_notification.md) и порядок, указанный самым последним вызовом **SetColumns,** должны быть одинаковыми на момент отправки запроса уведомления. </span><span class="sxs-lookup"><span data-stu-id="05b48-143">When sending table notifications, the order of the properties in the **row** member of the [TABLE_NOTIFICATION](table_notification.md) structure and the order specified by the most recent **SetColumns** call must be the same as of the time that the notification request was sent.</span></span> 
  
<span data-ttu-id="05b48-144">Другой флаг, TBL_BATCH, позволяет звонятелям указать, что реализующий таблицу может отложить оценку результатов операции до более позднего времени.</span><span class="sxs-lookup"><span data-stu-id="05b48-144">Another flag, TBL_BATCH, allows callers to specify that the table implementer can defer evaluating the results of the operation until a later time.</span></span> <span data-ttu-id="05b48-145">По возможности вызывателям следует установить этот флаг, так как пакетная операция повышает производительность.</span><span class="sxs-lookup"><span data-stu-id="05b48-145">Whenever possible, callers should set this flag because batched operation improves performance.</span></span>
  
<span data-ttu-id="05b48-146">Часто звонятелям удобно резервировать некоторые столбцы в наборе полученных строк для значений, которые будут добавлены позже.</span><span class="sxs-lookup"><span data-stu-id="05b48-146">It is often convenient for callers to reserve some columns in the retrieved row set for values to be added later.</span></span> <span data-ttu-id="05b48-147">Для этого вызыватели **размещают PR_NULL** ([PidTagNull)](pidtagnull-canonical-property.md)в нужных позициях в массиве тегов свойств, переданном **в SetColumns;** затем таблица возвращает данные **PR_NULL** на этих позициях во всех строках, полученных с **помощью QueryRows.**</span><span class="sxs-lookup"><span data-stu-id="05b48-147">Callers do this by placing **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) at the desired positions in the property tag array passed to **SetColumns**; the table will then pass back **PR_NULL** at those positions in all rows retrieved with **QueryRows**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="05b48-148">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="05b48-148">Notes to callers</span></span>

<span data-ttu-id="05b48-149">При создании массива тегов свойств для параметра  _lpPropTagArray_ упорядочение тегов в том порядке, в который должны отображаться столбцы в представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="05b48-149">When building the property tag array for the  _lpPropTagArray_ parameter, order the tags in the order that you want the columns to appear in the table view.</span></span> 
  
<span data-ttu-id="05b48-150">Вы можете указать многоценные свойства, которые необходимо включить в набор столбцов, применив к тегу свойства многоценный флаг экземпляра MVI_FLAG константу.</span><span class="sxs-lookup"><span data-stu-id="05b48-150">You can specify multivalued properties to be included in the column set by applying the multivalued instance flag, or MVI_FLAG constant, to the property tag.</span></span> <span data-ttu-id="05b48-151">Установите этот флаг, передав тег свойства для одно значение версии свойства в качестве параметра в макрос MVI_PROP следующим образом:</span><span class="sxs-lookup"><span data-stu-id="05b48-151">Set this flag by passing the property tag for the single-valued version of the property as a parameter to the MVI_PROP macro as follows:</span></span>
  
```
MVI_PROP(ulPropTag)

```

<span data-ttu-id="05b48-152">Макрос MVI_PROP будет MVI_FLAG для свойства, превращая тег в многоценный тег.</span><span class="sxs-lookup"><span data-stu-id="05b48-152">The MVI_PROP macro will set MVI_FLAG for the property, turning the tag into a multivalued tag.</span></span> <span data-ttu-id="05b48-153">Если вы ошибочно попытались вызвать MVI_PROP свойство с одним значением, MAPI игнорирует вызов и оставляет тег свойства без изменений.</span><span class="sxs-lookup"><span data-stu-id="05b48-153">If you erroneously try to call MVI_PROP on a single-valued property, MAPI will ignore the call and leave the property tag unchanged.</span></span> 
  
<span data-ttu-id="05b48-154">Вы можете включить теги свойств, **PR_NULL** в массив тегов свойств, чтобы зарезервировать место в наборе столбцов.</span><span class="sxs-lookup"><span data-stu-id="05b48-154">You can include property tags set to **PR_NULL** in the property tag array to reserve space in the column set.</span></span> <span data-ttu-id="05b48-155">Пространство для хранения позволяет добавлять набор столбцов, не выделяя новый массив тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="05b48-155">Reserving space allows you to add to a column set without having to allocate a new property tag array.</span></span> 
  
<span data-ttu-id="05b48-156">Если вызов **SetColumns** приводит к изменению порядка столбцов таблицы, а один или несколько из этих столбцов представляют многоценное свойство, число строк в таблице может увеличиться.</span><span class="sxs-lookup"><span data-stu-id="05b48-156">When your call to **SetColumns** causes a change to the order of a table's columns and one or more of these columns represent a multivalued property, it is possible for the number of rows in the table to increase.</span></span> <span data-ttu-id="05b48-157">В этом случае все закладки для таблицы удаляются.</span><span class="sxs-lookup"><span data-stu-id="05b48-157">If this occurs, all of the bookmarks for the table are discarded.</span></span> <span data-ttu-id="05b48-158">Дополнительные сведения о том, как многоценные столбцы влияют на таблицы, см. в статье "Работа с [многоценными столбцами".](working-with-multivalued-columns.md)</span><span class="sxs-lookup"><span data-stu-id="05b48-158">For more information about how multivalued columns affect tables, see [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
<span data-ttu-id="05b48-159">Установка столбцов по умолчанию является синхронной операцией.</span><span class="sxs-lookup"><span data-stu-id="05b48-159">Setting columns is by default a synchronous operation.</span></span> <span data-ttu-id="05b48-160">Однако можно разрешить таблице откладывать операцию до тех пор, пока не будут необходимы данные, установив TBL_BATCH флага.</span><span class="sxs-lookup"><span data-stu-id="05b48-160">However, you can allow the table to postpone the operation until such time as the data is needed by setting the TBL_BATCH flag.</span></span> <span data-ttu-id="05b48-161">Установка этого флага может повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="05b48-161">Setting this flag can improve performance.</span></span> <span data-ttu-id="05b48-162">Другой флаг, TBL_ASYNC, делает операцию асинхронной, позволяя **SetColumns** возвращаться до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="05b48-162">Another flag, TBL_ASYNC, makes the operation asynchronous, allowing **SetColumns** to return before the operation is complete.</span></span> <span data-ttu-id="05b48-163">Чтобы определить время завершения, вызовите [IMAPITable::GetStatus.](imapitable-getstatus.md)</span><span class="sxs-lookup"><span data-stu-id="05b48-163">To determine when completion occurs, call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span>
  
<span data-ttu-id="05b48-164">Если вызов **SetColumns** возвращает MAPI_E_BUSY, что другая операция препятствует запуску операции, можно вызвать [IMAPITable::Abort,](imapitable-abort.md) чтобы остановить операцию.</span><span class="sxs-lookup"><span data-stu-id="05b48-164">If a call to **SetColumns** returns MAPI_E_BUSY, indicating that another operation is preventing your operation from starting, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the operation in progress.</span></span> 
  
<span data-ttu-id="05b48-165">Вы также можете вызвать [HrAddColumnsEx,](hraddcolumnsex.md) чтобы изменить набор столбцов.</span><span class="sxs-lookup"><span data-stu-id="05b48-165">You can also call [HrAddColumnsEx](hraddcolumnsex.md) to change a column set.</span></span> <span data-ttu-id="05b48-166">Разница между **HrAddColumnsEx** и **IMAPITable::SetColumns** заключается в том, что **HrAddColumnsEx** менее гибкая; он может добавлять только столбцы.</span><span class="sxs-lookup"><span data-stu-id="05b48-166">The difference between **HrAddColumnsEx** and **IMAPITable::SetColumns** is that **HrAddColumnsEx** is less flexible; it can only add columns.</span></span> <span data-ttu-id="05b48-167">Дополнительные столбцы размещаются в начале набора столбцов; Все существующие столбцы отображаются после этих столбцов.</span><span class="sxs-lookup"><span data-stu-id="05b48-167">The additional columns are placed at the beginning of the column set; all existing columns appear following these columns.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="05b48-168">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="05b48-168">MFCMAPI reference</span></span>

<span data-ttu-id="05b48-169">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="05b48-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="05b48-170">**Файл**</span><span class="sxs-lookup"><span data-stu-id="05b48-170">**File**</span></span>|<span data-ttu-id="05b48-171">**Функция**</span><span class="sxs-lookup"><span data-stu-id="05b48-171">**Function**</span></span>|<span data-ttu-id="05b48-172">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="05b48-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="05b48-173">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="05b48-173">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="05b48-174">CContentsTableListCtrl::D oSetColumns</span><span class="sxs-lookup"><span data-stu-id="05b48-174">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="05b48-175">MFCMAPI использует метод **IMAPITable::SetColumns,** чтобы установить нужные столбцы для таблицы.</span><span class="sxs-lookup"><span data-stu-id="05b48-175">MFCMAPI uses the **IMAPITable::SetColumns** method to set the desired columns for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="05b48-176">См. также</span><span class="sxs-lookup"><span data-stu-id="05b48-176">See also</span></span>



[<span data-ttu-id="05b48-177">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="05b48-177">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="05b48-178">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="05b48-178">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="05b48-179">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="05b48-179">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="05b48-180">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="05b48-180">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="05b48-181">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="05b48-181">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="05b48-182">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="05b48-182">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="05b48-183">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="05b48-183">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="05b48-184">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="05b48-184">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="05b48-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="05b48-185">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="05b48-186">SRowSet</span><span class="sxs-lookup"><span data-stu-id="05b48-186">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="05b48-187">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="05b48-187">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="05b48-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="05b48-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="05b48-189">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="05b48-189">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

