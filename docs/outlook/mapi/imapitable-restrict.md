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
ms.openlocfilehash: 6cca6bc12fa6f100885b7bf705d79fa24a2e2f91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414622"
---
# <a name="imapitablerestrict"></a><span data-ttu-id="dcd9a-103">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="dcd9a-103">IMAPITable::Restrict</span></span>

  
  
<span data-ttu-id="dcd9a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dcd9a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dcd9a-105">Применяет фильтр к таблице, уменьшая набор строк только к тем строкам, которые соответствуют указанным критериям.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-105">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="dcd9a-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="dcd9a-106">Parameters</span></span>

 <span data-ttu-id="dcd9a-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="dcd9a-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="dcd9a-108">[in] Указатель на [структуру SRestriction,](srestriction.md) определяющей условия фильтра.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-108">[in] Pointer to an [SRestriction](srestriction.md) structure defining the conditions of the filter.</span></span> <span data-ttu-id="dcd9a-109">Передача NULL в  _параметре lpRestriction_ удаляет текущий фильтр.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-109">Passing NULL in the  _lpRestriction_ parameter removes the current filter.</span></span> 
    
 <span data-ttu-id="dcd9a-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dcd9a-110">_ulFlags_</span></span>
  
> <span data-ttu-id="dcd9a-111">[in] Bitmask флагов, которые контролируют сроки операции ограничения.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-111">[in] Bitmask of flags that controls the timing of the restriction operation.</span></span> <span data-ttu-id="dcd9a-112">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="dcd9a-112">The following flags can be set:</span></span>
    
<span data-ttu-id="dcd9a-113">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="dcd9a-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="dcd9a-114">Запускает операцию асинхронно и возвращается до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-114">Starts the operation asynchronously and returns before the operation completes.</span></span>
    
<span data-ttu-id="dcd9a-115">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="dcd9a-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="dcd9a-116">Откладывает оценку фильтра до тех пор, пока не потребуются данные в таблице.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-116">Defers evaluation of the filter until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dcd9a-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dcd9a-117">Return value</span></span>

<span data-ttu-id="dcd9a-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="dcd9a-118">S_OK</span></span> 
  
> <span data-ttu-id="dcd9a-119">Фильтр был успешно применен.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-119">The filter was successfully applied.</span></span>
    
<span data-ttu-id="dcd9a-120">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="dcd9a-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="dcd9a-121">В настоящее время продолжается другая операция, которая не позволяет начать операцию ограничения.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-121">Another operation is in progress that prevents the restriction operation from starting.</span></span> <span data-ttu-id="dcd9a-122">Либо операция должна быть разрешена к завершению, либо она должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="dcd9a-123">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="dcd9a-123">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="dcd9a-124">Таблица не может выполнять операцию, так как определенный фильтр, на который указывает  _параметр lpRestriction,_ является слишком сложным.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-124">The table cannot perform the operation because the particular filter pointed to by the  _lpRestriction_ parameter is too complicated.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="dcd9a-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="dcd9a-125">Remarks</span></span>

<span data-ttu-id="dcd9a-126">Метод **IMAPITable::Restrict** устанавливает ограничение или фильтр на таблице.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-126">The **IMAPITable::Restrict** method establishes a restriction, or filter, on a table.</span></span> <span data-ttu-id="dcd9a-127">Если существует предыдущее ограничение, оно отбрасывается и применяется новое.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-127">If there is a previous restriction, it is discarded and the new one applied.</span></span> <span data-ttu-id="dcd9a-128">Применение ограничения не влияет на данные таблицы; он просто изменяет представление, ограничив строки, которые можно получить, строками, содержащими данные, удовлетворяющие ограничению.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-128">Applying a restriction has no affect on the underlying data of a table; it simply alters the view by limiting the rows that can be retrieved to rows containing data that satisfy the restriction.</span></span> 
  
<span data-ttu-id="dcd9a-129">Существует несколько различных типов ограничений, каждый из которых описывается с другой структурой.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-129">There are several different types of restrictions, each described with a different structure.</span></span> <span data-ttu-id="dcd9a-130">Структура [SRestriction](srestriction.md) содержит два члена: значение, которое указывает тип ограничения и конкретную структуру, применимую к этому типу.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-130">The [SRestriction](srestriction.md) structure contains two members: a value that indicates the type of restriction and the specific structure applicable for that type.</span></span> 
  
<span data-ttu-id="dcd9a-131">Уведомления для строк таблиц, которые скрыты от просмотра вызовами **для ограничения,** никогда не создаются.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-131">Notifications for table rows that are hidden from view by calls to **Restrict** are never generated.</span></span> 
  
<span data-ttu-id="dcd9a-132">Ограничение свойства для многоценного свойства работает как ограничение для одноценного свойства.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-132">A property restriction on a multivalued property works like a restriction on a single-valued property.</span></span> <span data-ttu-id="dcd9a-133">Многоценное свойство, используемого в ограничении свойств, должно иметь MVI_FLAG флага.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-133">A multivalued property to be used in a property restriction must have the MVI_FLAG flag set.</span></span> <span data-ttu-id="dcd9a-134">Если у него нет этого набора флага, он рассматривается как полностью упорядоченный пучок.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-134">If it doesn't have this flag set, it is treated as a totally ordered tuple.</span></span> <span data-ttu-id="dcd9a-135">Сравнение двух многоценных столбцов сравнивает элементы столбцов в порядке, сообщая о связи столбцов при первом неравенстве.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-135">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality.</span></span> <span data-ttu-id="dcd9a-136">Равенство возвращается только в том случае, если сравниваемые столбцы содержат те же значения в том же порядке.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-136">Equality is returned only if the columns compared contain the same values in the same order.</span></span> <span data-ttu-id="dcd9a-137">Если у одного столбца меньше значений, чем у другого, сообщаемая связь имеет значение null к другому значению.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-137">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
<span data-ttu-id="dcd9a-138">Дополнительные сведения об ограничениях см. в [дополнительных сведениях об ограничениях.](about-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="dcd9a-138">For more information about restrictions, see [About Restrictions](about-restrictions.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="dcd9a-139">Если вы создаете динамические запросы для поиска данных на сервере, используйте метод **FindRow** вместо использования метода Restrict и **метода QueryRows** вместе. </span><span class="sxs-lookup"><span data-stu-id="dcd9a-139">If you create dynamic queries to search for data on the server, use the **FindRow** method instead of using the **Restrict** method and the **QueryRows** method together.</span></span> <span data-ttu-id="dcd9a-140">Метод **Restrict** создает кэшировать представление, которое используется для оценки всех сообщений, добавленных или измененных в базовой папке.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-140">The **Restrict** method creates a cached view that is used to evaluate all messages added to or modified in the base folder.</span></span> <span data-ttu-id="dcd9a-141">Если клиентская заявка использует метод **Restrict** для каждого динамического запроса, для каждого запроса будет создано кэшистское представление.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-141">If a client application uses the **Restrict** method for each dynamic query, a cached view will be created for each query.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="dcd9a-142">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="dcd9a-142">Notes to callers</span></span>

<span data-ttu-id="dcd9a-143">Чтобы отменить текущее ограничение без создания нового, передайте NULL в  _lpRestriction_.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-143">To discard the current restriction without creating a new one, pass NULL in  _lpRestriction_.</span></span>
  
<span data-ttu-id="dcd9a-144">Если еще один асинхронный вызов  таблицы продолжается, что приводит к MAPI_E_BUSY, вы можете вызвать [IMAPITable::Abort,](imapitable-abort.md) чтобы остановить вызов.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-144">If another asynchronous table call is in progress, causing **Restrict** to return MAPI_E_BUSY, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the call.</span></span> 
  
 <span data-ttu-id="dcd9a-145">**Ограничение** работает синхронно, если только не задать один из флагов.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-145">**Restrict** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="dcd9a-146">Если вы установите флаг TBL_BATCH,  ограничить оценку ограничения, если не запрашивать данные.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-146">If you set the TBL_BATCH flag, **Restrict** postpones the evaluation of the restriction unless you request the data.</span></span> <span data-ttu-id="dcd9a-147">Если флаг TBL_ASYNC, **ограничение** работает асинхронно, потенциально возвращаясь до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-147">If the TBL_ASYNC flag is set, **Restrict** operates asynchronously, potentially returning before the completion of the operation.</span></span>
  
<span data-ttu-id="dcd9a-148">Все закладки для таблицы отбрасываются при вызове ограничения, и BOOKMARK_CURRENT текущее положение курсора устанавливается в начале таблицы. </span><span class="sxs-lookup"><span data-stu-id="dcd9a-148">All bookmarks for a table are discarded when a call to **Restrict** is made, and BOOKMARK_CURRENT, the current cursor position, is set to the beginning of the table.</span></span> 
  
<span data-ttu-id="dcd9a-149">При попытке наложить ограничение свойства на свойство, которое не находится в наборе столбцов таблицы, результаты будут неопределенными.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-149">If you attempt to impose a property restriction on a property that is not in the table's column set, the results are undefined.</span></span> <span data-ttu-id="dcd9a-150">Всякий раз, когда вы не уверены в том, поддерживается ли свойство в таблице, совмещайте ограничение свойств с ограничением на существование.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-150">Whenever you are unsure as to whether a property is supported in a table, combine the property restriction with an exists restriction.</span></span> <span data-ttu-id="dcd9a-151">Существует ограничение проверки на наличие свойства, прежде чем пытаться навязать ограничение свойства.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-151">The exists restriction checks for the existence of the property before attempting to impose the property restriction.</span></span> 
  
<span data-ttu-id="dcd9a-152">Не ожидайте получения уведомления таблицы в строке, которая была отфильтрованной из таблицы из-за ограничения.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-152">Do not expect to receive a table notification on a row that has been filtered from a table due to a restriction.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="dcd9a-153">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="dcd9a-153">MFCMAPI reference</span></span>

<span data-ttu-id="dcd9a-154">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="dcd9a-155">**Файл**</span><span class="sxs-lookup"><span data-stu-id="dcd9a-155">**File**</span></span>|<span data-ttu-id="dcd9a-156">**Функция**</span><span class="sxs-lookup"><span data-stu-id="dcd9a-156">**Function**</span></span>|<span data-ttu-id="dcd9a-157">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="dcd9a-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dcd9a-158">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="dcd9a-158">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="dcd9a-159">CContentsTableListCtrl::ApplyRestriction</span><span class="sxs-lookup"><span data-stu-id="dcd9a-159">CContentsTableListCtrl::ApplyRestriction</span></span>  <br/> |<span data-ttu-id="dcd9a-160">MFCMAPI использует **метод IMAPITable::Restrict,** чтобы установить ограничение на таблице.</span><span class="sxs-lookup"><span data-stu-id="dcd9a-160">MFCMAPI uses the **IMAPITable::Restrict** method to set a restriction on a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dcd9a-161">См. также</span><span class="sxs-lookup"><span data-stu-id="dcd9a-161">See also</span></span>



[<span data-ttu-id="dcd9a-162">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="dcd9a-162">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="dcd9a-163">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="dcd9a-163">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="dcd9a-164">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="dcd9a-164">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="dcd9a-165">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="dcd9a-165">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="dcd9a-166">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="dcd9a-166">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="dcd9a-167">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dcd9a-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="dcd9a-168">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="dcd9a-168">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

