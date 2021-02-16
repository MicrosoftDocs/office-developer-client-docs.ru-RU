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
# <a name="imapitablerestrict"></a><span data-ttu-id="cb133-103">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="cb133-103">IMAPITable::Restrict</span></span>

  
  
<span data-ttu-id="cb133-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb133-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb133-105">Применяет фильтр к таблице, уменьшая набор строк только теми строками, которые соответствуют указанным условиям.</span><span class="sxs-lookup"><span data-stu-id="cb133-105">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="cb133-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb133-106">Parameters</span></span>

 <span data-ttu-id="cb133-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="cb133-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="cb133-108">[in] Указатель на [структуру SRestriction,](srestriction.md) определяющей условия фильтра.</span><span class="sxs-lookup"><span data-stu-id="cb133-108">[in] Pointer to an [SRestriction](srestriction.md) structure defining the conditions of the filter.</span></span> <span data-ttu-id="cb133-109">Передача NULL в  _параметре lpRestriction_ удаляет текущий фильтр.</span><span class="sxs-lookup"><span data-stu-id="cb133-109">Passing NULL in the  _lpRestriction_ parameter removes the current filter.</span></span> 
    
 <span data-ttu-id="cb133-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cb133-110">_ulFlags_</span></span>
  
> <span data-ttu-id="cb133-111">[in] Битоваяmas флагов, которая управляет временем операции ограничения.</span><span class="sxs-lookup"><span data-stu-id="cb133-111">[in] Bitmask of flags that controls the timing of the restriction operation.</span></span> <span data-ttu-id="cb133-112">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="cb133-112">The following flags can be set:</span></span>
    
<span data-ttu-id="cb133-113">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="cb133-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="cb133-114">Запускает операцию асинхронно и возвращается до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="cb133-114">Starts the operation asynchronously and returns before the operation completes.</span></span>
    
<span data-ttu-id="cb133-115">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="cb133-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="cb133-116">Откладывает оценку фильтра, пока не потребуются данные в таблице.</span><span class="sxs-lookup"><span data-stu-id="cb133-116">Defers evaluation of the filter until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cb133-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb133-117">Return value</span></span>

<span data-ttu-id="cb133-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="cb133-118">S_OK</span></span> 
  
> <span data-ttu-id="cb133-119">Фильтр успешно применен.</span><span class="sxs-lookup"><span data-stu-id="cb133-119">The filter was successfully applied.</span></span>
    
<span data-ttu-id="cb133-120">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="cb133-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="cb133-121">В настоящее время идет другая операция, которая препятствует запуску операции ограничения.</span><span class="sxs-lookup"><span data-stu-id="cb133-121">Another operation is in progress that prevents the restriction operation from starting.</span></span> <span data-ttu-id="cb133-122">Либо операция должна быть разрешена для завершения, либо она должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="cb133-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="cb133-123">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="cb133-123">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="cb133-124">Таблица не может выполнить операцию, так как конкретный фильтр, на который указывает параметр  _lpRestriction,_ слишком сложный.</span><span class="sxs-lookup"><span data-stu-id="cb133-124">The table cannot perform the operation because the particular filter pointed to by the  _lpRestriction_ parameter is too complicated.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cb133-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="cb133-125">Remarks</span></span>

<span data-ttu-id="cb133-126">Метод **IMAPITable::Restrict** устанавливает ограничение (или фильтр) для таблицы.</span><span class="sxs-lookup"><span data-stu-id="cb133-126">The **IMAPITable::Restrict** method establishes a restriction, or filter, on a table.</span></span> <span data-ttu-id="cb133-127">Если существует предыдущее ограничение, оно удаляется и применяется новое.</span><span class="sxs-lookup"><span data-stu-id="cb133-127">If there is a previous restriction, it is discarded and the new one applied.</span></span> <span data-ttu-id="cb133-128">Применение ограничения не влияет на данные таблицы; Он просто изменяет представление, ограничив строки, которые можно получить, строками, содержащими данные, удовлетворяющие ограничению.</span><span class="sxs-lookup"><span data-stu-id="cb133-128">Applying a restriction has no affect on the underlying data of a table; it simply alters the view by limiting the rows that can be retrieved to rows containing data that satisfy the restriction.</span></span> 
  
<span data-ttu-id="cb133-129">Существует несколько различных типов ограничений, каждый из которых описывается с разной структурой.</span><span class="sxs-lookup"><span data-stu-id="cb133-129">There are several different types of restrictions, each described with a different structure.</span></span> <span data-ttu-id="cb133-130">Структура [SRestriction](srestriction.md) содержит два члена: значение, которое указывает тип ограничения и конкретную структуру, применимую к этому типу.</span><span class="sxs-lookup"><span data-stu-id="cb133-130">The [SRestriction](srestriction.md) structure contains two members: a value that indicates the type of restriction and the specific structure applicable for that type.</span></span> 
  
<span data-ttu-id="cb133-131">Уведомления о строках таблиц, скрытых вызовами **ограничения,** никогда не создаются.</span><span class="sxs-lookup"><span data-stu-id="cb133-131">Notifications for table rows that are hidden from view by calls to **Restrict** are never generated.</span></span> 
  
<span data-ttu-id="cb133-132">Ограничение свойства для многоценного свойства работает как ограничение для свойства с одним значением.</span><span class="sxs-lookup"><span data-stu-id="cb133-132">A property restriction on a multivalued property works like a restriction on a single-valued property.</span></span> <span data-ttu-id="cb133-133">Многоценное свойство, используемого в ограничении свойства, должно иметь MVI_FLAG флага.</span><span class="sxs-lookup"><span data-stu-id="cb133-133">A multivalued property to be used in a property restriction must have the MVI_FLAG flag set.</span></span> <span data-ttu-id="cb133-134">Если в нем нет этого флага, он будет рассматриваться как полностью упорядоченный набор.</span><span class="sxs-lookup"><span data-stu-id="cb133-134">If it doesn't have this flag set, it is treated as a totally ordered tuple.</span></span> <span data-ttu-id="cb133-135">Сравнение двух многоценных столбцов сравнивает элементы столбцов по порядку, сообщая о связи столбцов при первом ветви.</span><span class="sxs-lookup"><span data-stu-id="cb133-135">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality.</span></span> <span data-ttu-id="cb133-136">Равенства возвращается только в том случае, если сравниваемая столбца содержит одинаковые значения в том же порядке.</span><span class="sxs-lookup"><span data-stu-id="cb133-136">Equality is returned only if the columns compared contain the same values in the same order.</span></span> <span data-ttu-id="cb133-137">Если в одном столбце меньше значений, чем в другом, сообщается, что относительно другого имеется значение null.</span><span class="sxs-lookup"><span data-stu-id="cb133-137">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
<span data-ttu-id="cb133-138">Дополнительные сведения об ограничениях см. в [сведениях об ограничениях.](about-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="cb133-138">For more information about restrictions, see [About Restrictions](about-restrictions.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="cb133-139">Если вы создаете динамические запросы для поиска данных на сервере, используйте метод **FindRow** вместо использования метода **Restrict** и **метода QueryRows** вместе.</span><span class="sxs-lookup"><span data-stu-id="cb133-139">If you create dynamic queries to search for data on the server, use the **FindRow** method instead of using the **Restrict** method and the **QueryRows** method together.</span></span> <span data-ttu-id="cb133-140">Метод **Restrict** создает кэшное представление, которое используется для оценки всех сообщений, добавленных в базовую папку или измененных в нее.</span><span class="sxs-lookup"><span data-stu-id="cb133-140">The **Restrict** method creates a cached view that is used to evaluate all messages added to or modified in the base folder.</span></span> <span data-ttu-id="cb133-141">Если клиентские приложения используют метод **Restrict** для каждого динамического запроса, для каждого запроса создается кэш-представление.</span><span class="sxs-lookup"><span data-stu-id="cb133-141">If a client application uses the **Restrict** method for each dynamic query, a cached view will be created for each query.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="cb133-142">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="cb133-142">Notes to callers</span></span>

<span data-ttu-id="cb133-143">Чтобы отменить текущее ограничение без создания нового, передайте NULL в _lpRestriction._</span><span class="sxs-lookup"><span data-stu-id="cb133-143">To discard the current restriction without creating a new one, pass NULL in  _lpRestriction_.</span></span>
  
<span data-ttu-id="cb133-144">Если идет еще один асинхронный  вызов таблицы, из-за чего restrict возвращает MAPI_E_BUSY, можно вызвать [IMAPITable::Abort,](imapitable-abort.md) чтобы остановить вызов.</span><span class="sxs-lookup"><span data-stu-id="cb133-144">If another asynchronous table call is in progress, causing **Restrict** to return MAPI_E_BUSY, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the call.</span></span> 
  
 <span data-ttu-id="cb133-145">**Ограничение** работает синхронно, если не установлен один из флагов.</span><span class="sxs-lookup"><span data-stu-id="cb133-145">**Restrict** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="cb133-146">Если установлен флаг TBL_BATCH, **ограничение** откладывает оценку ограничения, если вы не запросили данные.</span><span class="sxs-lookup"><span data-stu-id="cb133-146">If you set the TBL_BATCH flag, **Restrict** postpones the evaluation of the restriction unless you request the data.</span></span> <span data-ttu-id="cb133-147">Если флаг TBL_ASYNC установлен, **ограничение** работает асинхронно, потенциально возвращаясь до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="cb133-147">If the TBL_ASYNC flag is set, **Restrict** operates asynchronously, potentially returning before the completion of the operation.</span></span>
  
<span data-ttu-id="cb133-148">Все закладки для таблицы удаляются при  вызове ограничения, а BOOKMARK_CURRENT текущее положение курсора устанавливается в начале таблицы.</span><span class="sxs-lookup"><span data-stu-id="cb133-148">All bookmarks for a table are discarded when a call to **Restrict** is made, and BOOKMARK_CURRENT, the current cursor position, is set to the beginning of the table.</span></span> 
  
<span data-ttu-id="cb133-149">Если попытаться наложить ограничение на свойство, которое не находится в наборе столбцов таблицы, результаты будут неопределенными.</span><span class="sxs-lookup"><span data-stu-id="cb133-149">If you attempt to impose a property restriction on a property that is not in the table's column set, the results are undefined.</span></span> <span data-ttu-id="cb133-150">Если вы не знаете, поддерживается ли свойство в таблице, совмещайте ограничение свойства с ограничением на существование.</span><span class="sxs-lookup"><span data-stu-id="cb133-150">Whenever you are unsure as to whether a property is supported in a table, combine the property restriction with an exists restriction.</span></span> <span data-ttu-id="cb133-151">Существует ограничение проверяет наличие свойства, прежде чем пытаться наложить ограничение свойства.</span><span class="sxs-lookup"><span data-stu-id="cb133-151">The exists restriction checks for the existence of the property before attempting to impose the property restriction.</span></span> 
  
<span data-ttu-id="cb133-152">Не ожидайте получения уведомления о таблице в строке, которая была отфильтрованной из таблицы из-за ограничения.</span><span class="sxs-lookup"><span data-stu-id="cb133-152">Do not expect to receive a table notification on a row that has been filtered from a table due to a restriction.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cb133-153">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="cb133-153">MFCMAPI reference</span></span>

<span data-ttu-id="cb133-154">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="cb133-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cb133-155">**Файл**</span><span class="sxs-lookup"><span data-stu-id="cb133-155">**File**</span></span>|<span data-ttu-id="cb133-156">**Функция**</span><span class="sxs-lookup"><span data-stu-id="cb133-156">**Function**</span></span>|<span data-ttu-id="cb133-157">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="cb133-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cb133-158">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="cb133-158">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="cb133-159">CContentsTableListCtrl::ApplyRestriction</span><span class="sxs-lookup"><span data-stu-id="cb133-159">CContentsTableListCtrl::ApplyRestriction</span></span>  <br/> |<span data-ttu-id="cb133-160">MFCMAPI использует метод **IMAPITable::Restrict,** чтобы установить ограничение для таблицы.</span><span class="sxs-lookup"><span data-stu-id="cb133-160">MFCMAPI uses the **IMAPITable::Restrict** method to set a restriction on a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cb133-161">См. также</span><span class="sxs-lookup"><span data-stu-id="cb133-161">See also</span></span>



[<span data-ttu-id="cb133-162">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="cb133-162">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="cb133-163">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="cb133-163">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="cb133-164">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="cb133-164">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="cb133-165">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="cb133-165">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="cb133-166">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="cb133-166">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="cb133-167">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cb133-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="cb133-168">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="cb133-168">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

