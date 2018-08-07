---
title: IMAPITableRestrict
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Restrict
api_type:
- COM
ms.assetid: a5bfc190-b58f-44c3-893c-8727df14ee58
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3ab069728f872d82246e8925c5ad35c07f41f02e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809232"
---
# <a name="imapitablerestrict"></a><span data-ttu-id="7ea15-103">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="7ea15-103">IMAPITable::Restrict</span></span>

  
  
<span data-ttu-id="7ea15-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7ea15-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7ea15-105">Применение фильтра к таблице, уменьшение строки, задайте значение только строк, соответствующих определенным условиям.</span><span class="sxs-lookup"><span data-stu-id="7ea15-105">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7ea15-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ea15-106">Parameters</span></span>

 <span data-ttu-id="7ea15-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="7ea15-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="7ea15-108">[in] Указатель на структуру [SRestriction](srestriction.md) , определяющие условия фильтра.</span><span class="sxs-lookup"><span data-stu-id="7ea15-108">[in] Pointer to an [SRestriction](srestriction.md) structure defining the conditions of the filter.</span></span> <span data-ttu-id="7ea15-109">Указать значение NULL для параметра _lpRestriction_ удаляет текущий фильтр.</span><span class="sxs-lookup"><span data-stu-id="7ea15-109">Passing NULL in the  _lpRestriction_ parameter removes the current filter.</span></span> 
    
 <span data-ttu-id="7ea15-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7ea15-110">_ulFlags_</span></span>
  
> <span data-ttu-id="7ea15-111">[in] Битовая маска флаги, определяющее время операции ограничение.</span><span class="sxs-lookup"><span data-stu-id="7ea15-111">[in] Bitmask of flags that controls the timing of the restriction operation.</span></span> <span data-ttu-id="7ea15-112">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="7ea15-112">The following flags can be set:</span></span>
    
<span data-ttu-id="7ea15-113">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="7ea15-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="7ea15-114">Асинхронно запускает операцию и возвращает до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="7ea15-114">Starts the operation asynchronously and returns before the operation completes.</span></span>
    
<span data-ttu-id="7ea15-115">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="7ea15-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="7ea15-116">Вычисление фильтра которого откладывается, пока данные в таблице является обязательным.</span><span class="sxs-lookup"><span data-stu-id="7ea15-116">Defers evaluation of the filter until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7ea15-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7">Return value</span></span>

<span data-ttu-id="7ea15-118">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="7ea15-118">S_OK</span></span> 
  
> <span data-ttu-id="7ea15-119">Фильтр успешно применена.</span><span class="sxs-lookup"><span data-stu-id="7ea15-119">The filter was successfully applied.</span></span>
    
<span data-ttu-id="7ea15-120">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="7ea15-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="7ea15-121">В, не позволяющей операции ограничение запуск выполняется другой операции.</span><span class="sxs-lookup"><span data-stu-id="7ea15-121">Another operation is in progress that prevents the restriction operation from starting.</span></span> <span data-ttu-id="7ea15-122">В процессе выполнения операции должны выполнить либо должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="7ea15-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="7ea15-123">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="7ea15-123">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="7ea15-124">Таблицы не удается выполнить операцию, так как отдельного фильтра, на который указывает параметр _lpRestriction_ довольно просто.</span><span class="sxs-lookup"><span data-stu-id="7ea15-124">The table cannot perform the operation because the particular filter pointed to by the  _lpRestriction_ parameter is too complicated.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7ea15-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="7ea15-125">Remarks</span></span>

<span data-ttu-id="7ea15-126">Метод **IMAPITable::Restrict** устанавливает ограничения или фильтр, в таблице.</span><span class="sxs-lookup"><span data-stu-id="7ea15-126">The **IMAPITable::Restrict** method establishes a restriction, or filter, on a table.</span></span> <span data-ttu-id="7ea15-127">Если предыдущие ограничения, она удаляется и применяется новое.</span><span class="sxs-lookup"><span data-stu-id="7ea15-127">If there is a previous restriction, it is discarded and the new one applied.</span></span> <span data-ttu-id="7ea15-128">Применение ограничения не оказывает воздействия на базовых данных таблицы. он просто изменяет представление, ограничив число строк, которые могут быть получены для строки, содержащие данные, которые удовлетворяют ограничение.</span><span class="sxs-lookup"><span data-stu-id="7ea15-128">Applying a restriction has no affect on the underlying data of a table; it simply alters the view by limiting the rows that can be retrieved to rows containing data that satisfy the restriction.</span></span> 
  
<span data-ttu-id="7ea15-129">Существует несколько различных типов ограничений, каждый описывается с другой структурой.</span><span class="sxs-lookup"><span data-stu-id="7ea15-129">There are several different types of restrictions, each described with a different structure.</span></span> <span data-ttu-id="7ea15-130">Структура [SRestriction](srestriction.md) содержит два элемента: значение, которое указывает тип ограничения и определенную структуру для этого типа.</span><span class="sxs-lookup"><span data-stu-id="7ea15-130">The [SRestriction](srestriction.md) structure contains two members: a value that indicates the type of restriction and the specific structure applicable for that type.</span></span> 
  
<span data-ttu-id="7ea15-131">Уведомления для строки таблицы, которые являются скрытыми от режима отображения путем вызова **Restrict** никогда не создаются.</span><span class="sxs-lookup"><span data-stu-id="7ea15-131">Notifications for table rows that are hidden from view by calls to **Restrict** are never generated.</span></span> 
  
<span data-ttu-id="7ea15-132">Ограничение свойства на свойством работает как ограничение на одно значение свойства.</span><span class="sxs-lookup"><span data-stu-id="7ea15-132">A property restriction on a multivalued property works like a restriction on a single-valued property.</span></span> <span data-ttu-id="7ea15-133">Многозначные свойства для использования в ограничении свойства должен быть установлен флаг MVI_FLAG.</span><span class="sxs-lookup"><span data-stu-id="7ea15-133">A multivalued property to be used in a property restriction must have the MVI_FLAG flag set.</span></span> <span data-ttu-id="7ea15-134">Если он не установлен этот флаг, он обрабатывается как полностью упорядоченном кортеж.</span><span class="sxs-lookup"><span data-stu-id="7ea15-134">If it doesn't have this flag set, it is treated as a totally ordered tuple.</span></span> <span data-ttu-id="7ea15-135">Сравнение двух многозначных столбцов сравниваются элементы столбцов в порядке, отчетов отношения столбцов в первом неравенство.</span><span class="sxs-lookup"><span data-stu-id="7ea15-135">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality.</span></span> <span data-ttu-id="7ea15-136">Равенство возвращается только в том случае, если по сравнению столбцы содержат те же значения, в том же порядке.</span><span class="sxs-lookup"><span data-stu-id="7ea15-136">Equality is returned only if the columns compared contain the same values in the same order.</span></span> <span data-ttu-id="7ea15-137">Если один столбец значений меньше, чем другое, переданные отношения, является значение null на другое значение.</span><span class="sxs-lookup"><span data-stu-id="7ea15-137">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
<span data-ttu-id="7ea15-138">Дополнительные сведения об ограничениях обратитесь к разделу [О ограничения](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="7ea15-138">For more information about restrictions, see [About Restrictions](about-restrictions.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="7ea15-139">При создании динамических запросов для поиска данных на сервере, используйте метод **FindRow** вместо вместе с помощью метода **Restrict** и метод **QueryRows** .</span><span class="sxs-lookup"><span data-stu-id="7ea15-139">If you create dynamic queries to search for data on the server, use the **FindRow** method instead of using the **Restrict** method and the **QueryRows** method together.</span></span> <span data-ttu-id="7ea15-140">Метод **Restrict** создает кэшированные представления, которая используется для оценки все сообщения, добавлены или изменены в основной папке.</span><span class="sxs-lookup"><span data-stu-id="7ea15-140">The **Restrict** method creates a cached view that is used to evaluate all messages added to or modified in the base folder.</span></span> <span data-ttu-id="7ea15-141">Если клиентское приложение использует метод **Restrict** для каждого динамического запроса, кэшированные представления создается для каждого запроса.</span><span class="sxs-lookup"><span data-stu-id="7ea15-141">If a client application uses the **Restrict** method for each dynamic query, a cached view will be created for each query.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7ea15-142">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="7ea15-142">Notes to callers</span></span>

<span data-ttu-id="7ea15-143">Чтобы отменить текущее ограничение без создания новой, передайте _lpRestriction_NULL.</span><span class="sxs-lookup"><span data-stu-id="7ea15-143">To discard the current restriction without creating a new one, pass NULL in  _lpRestriction_.</span></span>
  
<span data-ttu-id="7ea15-144">Если выполняется другой вызов асинхронных таблице вызывает ошибку **ограничить** для возврата MAPI_E_BUSY, можно вызвать [IMAPITable::Abort](imapitable-abort.md) для остановки вызова.</span><span class="sxs-lookup"><span data-stu-id="7ea15-144">If another asynchronous table call is in progress, causing **Restrict** to return MAPI_E_BUSY, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the call.</span></span> 
  
 <span data-ttu-id="7ea15-145">**Ограничить** работает синхронно, если не выбрано флаги.</span><span class="sxs-lookup"><span data-stu-id="7ea15-145">**Restrict** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="7ea15-146">Если установлен флаг TBL_BATCH, **ограничить** откладывает оценки ограничение, если не запрашивать данные.</span><span class="sxs-lookup"><span data-stu-id="7ea15-146">If you set the TBL_BATCH flag, **Restrict** postpones the evaluation of the restriction unless you request the data.</span></span> <span data-ttu-id="7ea15-147">Если установлен флаг TBL_ASYNC, **ограничить**работает асинхронно, потенциально возврат до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="7ea15-147">If the TBL_ASYNC flag is set, **Restrict**operates asynchronously, potentially returning before the completion of the operation.</span></span>
  
<span data-ttu-id="7ea15-148">Все закладки для таблицы удаляются, когда выполняется вызов для **Restrict** и имеет значение BOOKMARK_CURRENT, текущей позиции курсора в начало таблицы.</span><span class="sxs-lookup"><span data-stu-id="7ea15-148">All bookmarks for a table are discarded when a call to **Restrict** is made, and BOOKMARK_CURRENT, the current cursor position, is set to the beginning of the table.</span></span> 
  
<span data-ttu-id="7ea15-149">При попытке наложить ограничение свойства для свойства, которое не входит в набор столбцов в таблице результатов не определено.</span><span class="sxs-lookup"><span data-stu-id="7ea15-149">If you attempt to impose a property restriction on a property that is not in the table's column set, the results are undefined.</span></span> <span data-ttu-id="7ea15-150">Каждый раз, когда вы не знаете поддерживается ли свойство в таблице, объединять ограничение свойства с существует ограничение.</span><span class="sxs-lookup"><span data-stu-id="7ea15-150">Whenever you are unsure as to whether a property is supported in a table, combine the property restriction with an exists restriction.</span></span> <span data-ttu-id="7ea15-151">Существует ограничение проверяется на наличие свойства перед попыткой наложить ограничение свойства.</span><span class="sxs-lookup"><span data-stu-id="7ea15-151">The exists restriction checks for the existence of the property before attempting to impose the property restriction.</span></span> 
  
<span data-ttu-id="7ea15-152">Не ожидается получение уведомлений в таблице на строку, в которой было отфильтровано из таблицы из-за ограничения.</span><span class="sxs-lookup"><span data-stu-id="7ea15-152">Do not expect to receive a table notification on a row that has been filtered from a table due to a restriction.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7ea15-153">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="7ea15-153">MFCMAPI reference</span></span>

<span data-ttu-id="7ea15-154">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="7ea15-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7ea15-155">**����**</span><span class="sxs-lookup"><span data-stu-id="7ea15-155">**File**</span></span>|<span data-ttu-id="7ea15-156">**�������**</span><span class="sxs-lookup"><span data-stu-id="7ea15-156">**Function**</span></span>|<span data-ttu-id="7ea15-157">**�����������**</span><span class="sxs-lookup"><span data-stu-id="7ea15-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7ea15-158">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="7ea15-158">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="7ea15-159">CContentsTableListCtrl::ApplyRestriction</span><span class="sxs-lookup"><span data-stu-id="7ea15-159">CContentsTableListCtrl::ApplyRestriction</span></span>  <br/> |<span data-ttu-id="7ea15-160">Mfcmapi (en) используется метод **IMAPITable::Restrict** для определения ограничения на таблицу.</span><span class="sxs-lookup"><span data-stu-id="7ea15-160">MFCMAPI uses the **IMAPITable::Restrict** method to set a restriction on a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7ea15-161">См. также</span><span class="sxs-lookup"><span data-stu-id="7ea15-161">See also</span></span>



[<span data-ttu-id="7ea15-162">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="7ea15-162">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="7ea15-163">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="7ea15-163">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="7ea15-164">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="7ea15-164">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="7ea15-165">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="7ea15-165">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="7ea15-166">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="7ea15-166">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="7ea15-167">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7ea15-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="7ea15-168">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="7ea15-168">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

