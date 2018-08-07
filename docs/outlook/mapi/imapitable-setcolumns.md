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
ms.openlocfilehash: 9eeab1e1186aeb5a9b458facd59bd4cc155e8014
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809224"
---
# <a name="imapitablesetcolumns"></a><span data-ttu-id="1cdb7-103">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="1cdb7-103">IMAPITable::SetColumns</span></span>

  
  
<span data-ttu-id="1cdb7-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1cdb7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1cdb7-105">Определяет конкретного свойства и порядок свойств в виде столбцов в таблице.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-105">Defines the particular properties and order of properties to appear as columns in the table.</span></span>
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1cdb7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1cdb7-106">Parameters</span></span>

 <span data-ttu-id="1cdb7-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="1cdb7-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="1cdb7-108">[in] Указатель на массив тегов свойств, идентифицирующий свойства в качестве столбцов в таблице.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-108">[in] Pointer to an array of property tags identifying properties to be included as columns in the table.</span></span> <span data-ttu-id="1cdb7-109">Тип свойства часть каждого тега может быть присвоено недопустимого типа или **PR_NULL** зарезервировать место для последующего добавления.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-109">The property type portion of each tag can be set to a valid type or to **PR_NULL** to reserve space for subsequent additions.</span></span> <span data-ttu-id="1cdb7-110">Параметр _lpPropTagArray_ не может иметь значение NULL. Каждый таблица должна иметь по крайней мере один столбец.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-110">The  _lpPropTagArray_ parameter cannot be set to NULL; every table must have at least one column.</span></span> 
    
 <span data-ttu-id="1cdb7-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1cdb7-111">_ulFlags_</span></span>
  
> <span data-ttu-id="1cdb7-112">[in] Битовая маска флаги, который управляет return асинхронный вызов **метода SetColumns**, например, при использовании **метода SetColumns** в уведомлении.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-112">[in] Bitmask of flags that controls the return of an asynchronous call to **SetColumns**, for example when **SetColumns** is used in notification.</span></span> <span data-ttu-id="1cdb7-113">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="1cdb7-113">The following flags can be set:</span></span> 
    
<span data-ttu-id="1cdb7-114">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="1cdb7-114">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="1cdb7-115">Запросы, которые операции задания столбца быть выполнена асинхронно вызывает ошибку **метода SetColumns** потенциально возвращает перед полностью завершения операции.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-115">Requests that the column setting operation be performed asynchronously causing **SetColumns** to potentially return before the operation has fully completed.</span></span> 
    
<span data-ttu-id="1cdb7-116">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="1cdb7-116">TBL_BATCH</span></span> 
  
> <span data-ttu-id="1cdb7-117">Позволяет таблице отложить операцию параметр столбца, пока данные не требуется.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-117">Permits the table to postpone the column setting operation until the data is actually required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1cdb7-118">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="1cdb7-118">Return value</span></span>

<span data-ttu-id="1cdb7-119">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="1cdb7-119">S_OK</span></span> 
  
> <span data-ttu-id="1cdb7-120">Столбец параметр операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-120">The column setting operation was successful.</span></span>
    
<span data-ttu-id="1cdb7-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="1cdb7-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="1cdb7-122">В, не позволяющей столбца, установка операция запуск выполняется другой операции.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-122">Another operation is in progress that prevents the column setting operation from starting.</span></span> <span data-ttu-id="1cdb7-123">В процессе выполнения операции должны выполнить либо должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1cdb7-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="1cdb7-124">Remarks</span></span>

<span data-ttu-id="1cdb7-125">Набор столбцов таблицы — набор свойств, которые будут включены в столбцы для строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-125">The column set of a table is the group of properties that make up the columns for the rows in the table.</span></span> <span data-ttu-id="1cdb7-126">Существует столбец по умолчанию для каждого типа в таблице.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-126">There is a default column set for each type of table.</span></span> <span data-ttu-id="1cdb7-127">Набор столбцов по умолчанию, состоящих из свойства, которые разработчик таблицы автоматически включает в себя.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-127">The default column set is made up of the properties that the table implementer automatically includes.</span></span> <span data-ttu-id="1cdb7-128">Таблица пользователей можно изменить это значение по умолчанию, задайте путем вызова метода **IMAPITable::SetColumns** .</span><span class="sxs-lookup"><span data-stu-id="1cdb7-128">Table users can alter this default set by calling the **IMAPITable::SetColumns** method.</span></span> <span data-ttu-id="1cdb7-129">Они могут запросить, что остальные столбцы добавляется к набору Если разработчик в таблице поддерживает их удаления столбцов или изменить порядок столбцов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-129">They can request that other columns be added to the default set if the table implementer supports them that columns be removed, or that the order of columns be changed.</span></span> <span data-ttu-id="1cdb7-130">**Метода SetColumns** указывает столбцы, возвращаемые с каждой строки и порядок этих столбцов в строке.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-130">**SetColumns** specifies the columns that are returned with each row and the order of these columns within the row.</span></span> 
  
<span data-ttu-id="1cdb7-131">Успешное выполнение **метода SetColumns** происходит только после последующих вызовов для извлечения данных из таблицы.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-131">The success of the **SetColumns** operation is apparent only after a subsequent call has been made to retrieve the data of the table.</span></span> <span data-ttu-id="1cdb7-132">Затем это сообщает об ошибках.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-132">It is then that any errors are reported.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1cdb7-133">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="1cdb7-133">Notes to implementers</span></span>

<span data-ttu-id="1cdb7-134">Некоторые поставщики разрешить вызов **метода SetColumns** заказ только столбцов таблицы, которые входят в состав доступные столбцы для представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-134">Some providers allow a **SetColumns** call to order only table columns that are part of the available columns for a table view.</span></span> <span data-ttu-id="1cdb7-135">Прочие разрешить вызов **метода SetColumns** заказ всех столбцов таблицы, включая те, содержащий свойства не в наборе исходного столбца.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-135">Other providers allow a **SetColumns** call to order all table columns, including those containing properties not in the original column set.</span></span> 
  
<span data-ttu-id="1cdb7-136">Если TBL_BATCH для асинхронной операции, поставщики должен возвращать типа свойства PT_ERROR и свойство значение NULL для столбцов, которые не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-136">When TBL_BATCH is set for asynchronous operations, providers should return a property type of PT_ERROR and a property value of NULL for columns that are not supported.</span></span>
  
<span data-ttu-id="1cdb7-137">Необходимо ответить на TBL_ASYNC флаг разрешения на запрос, что быть асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-137">You do not need to respond to the TBL_ASYNC flag requesting that the operation be asynchronous.</span></span> <span data-ttu-id="1cdb7-138">Если вы не поддерживают определение набора асинхронных столбца, синхронно выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-138">If you do not support asynchronous column set definition, perform the operation synchronously.</span></span> <span data-ttu-id="1cdb7-139">Если может поддерживать флаг TBL_ASYNC и другой асинхронной операции выполняется по-прежнему в, возвращаемого MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-139">If you can support the TBL_ASYNC flag and another asynchronous operation is still in progress, return MAPI_E_BUSY.</span></span> <span data-ttu-id="1cdb7-140">В противном случае возвращает значение S_OK независимо от того, ли все свойства, включенные в массиве свойство tag поддерживать.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-140">Otherwise, return S_OK regardless of whether or not you support all of the properties included in the property tag array.</span></span> <span data-ttu-id="1cdb7-141">Ошибки, связанные с неподдерживаемые свойства должны возвращаться из **IMAPITable** методы для получения данных, таких как **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-141">Errors resulting from unsupported properties should be returned from **IMAPITable** methods that retrieve data, such as **QueryRows**.</span></span> 
  
<span data-ttu-id="1cdb7-142">Не создавать уведомления для строки таблицы, которые являются скрытыми от режима отображения путем вызова **Restrict**.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-142">Do not generate notifications for table rows that are hidden from view by calls to **Restrict**.</span></span> 
  
<span data-ttu-id="1cdb7-143">После отправки уведомлений в таблице, порядок свойств в элемент **строки** [TABLE_NOTIFICATION](table_notification.md) структуры и порядок указанного с самыми последними вызова **метода SetColumns** должны быть одинаковыми по состоянию на время, запрашивать уведомление отправлено.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-143">When sending table notifications, the order of the properties in the **row** member of the [TABLE_NOTIFICATION](table_notification.md) structure and the order specified by the most recent **SetColumns** call must be the same as of the time that the notification request was sent.</span></span> 
  
<span data-ttu-id="1cdb7-144">Другой флаг, TBL_BATCH, позволяет вызывающих объектов указать, что разработчик в таблице можно отложить оценка результаты операции на более поздний срок.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-144">Another flag, TBL_BATCH, allows callers to specify that the table implementer can defer evaluating the results of the operation until a later time.</span></span> <span data-ttu-id="1cdb7-145">По возможности абонентов следует задать этот флаг, поскольку пакетной операции повышает производительность.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-145">Whenever possible, callers should set this flag because batched operation improves performance.</span></span>
  
<span data-ttu-id="1cdb7-146">Часто удобно для абонентов на бронирование некоторые столбцы в наборе строк извлеченных для значения, добавляемые позже.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-146">It is often convenient for callers to reserve some columns in the retrieved row set for values to be added later.</span></span> <span data-ttu-id="1cdb7-147">Вызывающие этого путем добавления **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) в нужное положение в массиве тега свойства, передаваемые **метода SetColumns**; Таблица будет затем обратно прохода **PR_NULL** в этих положениях все строки извлекается с **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-147">Callers do this by placing **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) at the desired positions in the property tag array passed to **SetColumns**; the table will then pass back **PR_NULL** at those positions in all rows retrieved with **QueryRows**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="1cdb7-148">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="1cdb7-148">Notes to callers</span></span>

<span data-ttu-id="1cdb7-149">При создании массива тега свойства для параметра _lpPropTagArray_ заказа теги в порядке столбцов, отображаемых в представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-149">When building the property tag array for the  _lpPropTagArray_ parameter, order the tags in the order that you want the columns to appear in the table view.</span></span> 
  
<span data-ttu-id="1cdb7-150">Можно указать многозначные свойства, которые будут включены в набор, применив флаг многозначных экземпляра или константа MVI_FLAG тега свойства столбцов.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-150">You can specify multivalued properties to be included in the column set by applying the multivalued instance flag, or MVI_FLAG constant, to the property tag.</span></span> <span data-ttu-id="1cdb7-151">Установите этот флаг, передав свойство тег для версии одним значением свойства как параметр макрос MVI_PROP следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1cdb7-151">Set this flag by passing the property tag for the single-valued version of the property as a parameter to the MVI_PROP macro as follows:</span></span>
  
```
MVI_PROP(ulPropTag)

```

<span data-ttu-id="1cdb7-152">Макрос MVI_PROP устанавливающей MVI_FLAG для свойства отсутствию тега в многозначных тег.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-152">The MVI_PROP macro will set MVI_FLAG for the property, turning the tag into a multivalued tag.</span></span> <span data-ttu-id="1cdb7-153">Если по ошибке попытка вызвать MVI_PROP для свойства с одним значением, MAPI пропуск вызов и оставьте без изменений тега свойства.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-153">If you erroneously try to call MVI_PROP on a single-valued property, MAPI will ignore the call and leave the property tag unchanged.</span></span> 
  
<span data-ttu-id="1cdb7-154">Может включать свойство теги для **PR_NULL** в массиве свойство tag резервирует место в наборе столбцов.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-154">You can include property tags set to **PR_NULL** in the property tag array to reserve space in the column set.</span></span> <span data-ttu-id="1cdb7-155">Резервирование места позволяет добавить в набор без необходимости выделить новый массив тега свойства столбцов.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-155">Reserving space allows you to add to a column set without having to allocate a new property tag array.</span></span> 
  
<span data-ttu-id="1cdb7-156">При вызове **метода SetColumns** являются причиной изменения порядку столбцов таблицы и одной или нескольких из этих столбцов представления многозначные свойства, существует возможность количество строк в таблице, чтобы увеличить.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-156">When your call to **SetColumns** causes a change to the order of a table's columns and one or more of these columns represent a multivalued property, it is possible for the number of rows in the table to increase.</span></span> <span data-ttu-id="1cdb7-157">В этом случае все закладки для таблицы удаляются.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-157">If this occurs, all of the bookmarks for the table are discarded.</span></span> <span data-ttu-id="1cdb7-158">Дополнительные сведения о том, как многозначные столбцы влияет на таблицы, работу [с несколькими значениями столбцов](working-with-multivalued-columns.md).</span><span class="sxs-lookup"><span data-stu-id="1cdb7-158">For more information about how multivalued columns affect tables, see [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
<span data-ttu-id="1cdb7-159">Настройка столбцов по умолчанию является синхронный режим.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-159">Setting columns is by default a synchronous operation.</span></span> <span data-ttu-id="1cdb7-160">Тем не менее можно разрешить таблице откладывать операции до тех пор данные, необходимые путем установки флага TBL_BATCH.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-160">However, you can allow the table to postpone the operation until such time as the data is needed by setting the TBL_BATCH flag.</span></span> <span data-ttu-id="1cdb7-161">Установка этого флага может повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-161">Setting this flag can improve performance.</span></span> <span data-ttu-id="1cdb7-162">Другой флаг TBL_ASYNC, выполняет операцию асинхронной, позволяя **метода SetColumns** для возврата до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-162">Another flag, TBL_ASYNC, makes the operation asynchronous, allowing **SetColumns** to return before the operation is complete.</span></span> <span data-ttu-id="1cdb7-163">Чтобы определить, когда происходит завершение работы, вызовите [IMAPITable::GetStatus](imapitable-getstatus.md).</span><span class="sxs-lookup"><span data-stu-id="1cdb7-163">To determine when completion occurs, call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span>
  
<span data-ttu-id="1cdb7-164">Если вызов **метода SetColumns** возвращает MAPI_E_BUSY, указывающего на то, что операция другой препятствует операции запуска, можно вызвать [IMAPITable::Abort](imapitable-abort.md) , чтобы отменить эту операцию в процессе выполнения.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-164">If a call to **SetColumns** returns MAPI_E_BUSY, indicating that another operation is preventing your operation from starting, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the operation in progress.</span></span> 
  
<span data-ttu-id="1cdb7-165">Можно также вызвать [HrAddColumnsEx](hraddcolumnsex.md) , чтобы изменить набор столбцов.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-165">You can also call [HrAddColumnsEx](hraddcolumnsex.md) to change a column set.</span></span> <span data-ttu-id="1cdb7-166">Различие между **HrAddColumnsEx** и **IMAPITable::SetColumns** является **HrAddColumnsEx** менее гибкие; его можно только добавить столбцы.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-166">The difference between **HrAddColumnsEx** and **IMAPITable::SetColumns** is that **HrAddColumnsEx** is less flexible; it can only add columns.</span></span> <span data-ttu-id="1cdb7-167">Дополнительные столбцы помещаются в начале набор столбцов; все существующие столбцы отображаются следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-167">The additional columns are placed at the beginning of the column set; all existing columns appear following these columns.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1cdb7-168">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="1cdb7-168">MFCMAPI reference</span></span>

<span data-ttu-id="1cdb7-169">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1cdb7-170">**����**</span><span class="sxs-lookup"><span data-stu-id="1cdb7-170">**File**</span></span>|<span data-ttu-id="1cdb7-171">**�������**</span><span class="sxs-lookup"><span data-stu-id="1cdb7-171">**Function**</span></span>|<span data-ttu-id="1cdb7-172">**�����������**</span><span class="sxs-lookup"><span data-stu-id="1cdb7-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1cdb7-173">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="1cdb7-173">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="1cdb7-174">CContentsTableListCtrl::DoSetColumns</span><span class="sxs-lookup"><span data-stu-id="1cdb7-174">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="1cdb7-175">Mfcmapi (en) используется метод **IMAPITable::SetColumns** для определения нужные столбцы для таблицы.</span><span class="sxs-lookup"><span data-stu-id="1cdb7-175">MFCMAPI uses the **IMAPITable::SetColumns** method to set the desired columns for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1cdb7-176">См. также</span><span class="sxs-lookup"><span data-stu-id="1cdb7-176">See also</span></span>



[<span data-ttu-id="1cdb7-177">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="1cdb7-177">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="1cdb7-178">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="1cdb7-178">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="1cdb7-179">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="1cdb7-179">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="1cdb7-180">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="1cdb7-180">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="1cdb7-181">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="1cdb7-181">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="1cdb7-182">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="1cdb7-182">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="1cdb7-183">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="1cdb7-183">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="1cdb7-184">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="1cdb7-184">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="1cdb7-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="1cdb7-185">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="1cdb7-186">SRowSet</span><span class="sxs-lookup"><span data-stu-id="1cdb7-186">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="1cdb7-187">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1cdb7-187">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="1cdb7-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1cdb7-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="1cdb7-189">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="1cdb7-189">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

