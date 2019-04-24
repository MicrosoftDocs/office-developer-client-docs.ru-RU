---
title: Имапитаблесорттабле
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328856"
---
# <a name="imapitablesorttable"></a><span data-ttu-id="6c783-103">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="6c783-103">IMAPITable::SortTable</span></span>

<span data-ttu-id="6c783-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c783-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c783-105">Метод **IMAPITable:: сорттабле** упорядочивает строки таблицы в зависимости от условий сортировки.</span><span class="sxs-lookup"><span data-stu-id="6c783-105">The **IMAPITable::SortTable** method orders the rows of the table, depending on sort criteria.</span></span> 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="6c783-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c783-106">Parameters</span></span>

<span data-ttu-id="6c783-107">_Лпсорткритериа_</span><span class="sxs-lookup"><span data-stu-id="6c783-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="6c783-108">возврата Указатель на структуру [ссортордерсет](ssortorderset.md) , которая содержит применяемые критерии сортировки.</span><span class="sxs-lookup"><span data-stu-id="6c783-108">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the sort criteria to apply.</span></span> <span data-ttu-id="6c783-109">Передача структуры **ссортордерсет** , содержащей нулевые столбцы, указывает на то, что таблица не должна быть отсортирована в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="6c783-109">Passing an **SSortOrderSet** structure that contains zero columns indicates that the table does not have to be sorted in any particular order.</span></span> 
    
<span data-ttu-id="6c783-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6c783-110">_ulFlags_</span></span>
  
> <span data-ttu-id="6c783-111">возврата Битовая маска флагов, которые управляют временем действия **IMAPITable:: сорттабле** .</span><span class="sxs-lookup"><span data-stu-id="6c783-111">[in] Bitmask of flags that controls the timing of the **IMAPITable::SortTable** operation.</span></span> <span data-ttu-id="6c783-112">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="6c783-112">The following flags can be set:</span></span> 
    
<span data-ttu-id="6c783-113">ТБЛ_АСИНК</span><span class="sxs-lookup"><span data-stu-id="6c783-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="6c783-114">Асинхронно запускает операцию и возвращает результат до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="6c783-114">Starts the operation asynchronously and returns before the operation is complete.</span></span>
    
<span data-ttu-id="6c783-115">ТБЛ_БАТЧ</span><span class="sxs-lookup"><span data-stu-id="6c783-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="6c783-116">ОтКладывает выполнение сортировки до тех пор, пока данные в таблице не будут обязательными.</span><span class="sxs-lookup"><span data-stu-id="6c783-116">Defers the completion of the sort until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6c783-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c783-117">Return value</span></span>

<span data-ttu-id="6c783-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="6c783-118">S_OK</span></span> 
  
> <span data-ttu-id="6c783-119">Операция сортировки выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="6c783-119">The sort operation was successful.</span></span>
    
<span data-ttu-id="6c783-120">МАПИ_Е_БУСИ</span><span class="sxs-lookup"><span data-stu-id="6c783-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="6c783-121">Выполняется другая операция, которая не позволяет начать операцию сортировки.</span><span class="sxs-lookup"><span data-stu-id="6c783-121">Another operation is in progress that prevents the sort operation from starting.</span></span> <span data-ttu-id="6c783-122">Выполнение выполняемой операции должно быть разрешено или остановлено.</span><span class="sxs-lookup"><span data-stu-id="6c783-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="6c783-123">МАПИ_Е_НО_СУППОРТ</span><span class="sxs-lookup"><span data-stu-id="6c783-123">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="6c783-124">Таблица не поддерживает тип запрошенной сортировки.</span><span class="sxs-lookup"><span data-stu-id="6c783-124">The table does not support the type of sorting requested.</span></span>
    
<span data-ttu-id="6c783-125">МАПИ_Е_ТУ_КОМПЛЕКС</span><span class="sxs-lookup"><span data-stu-id="6c783-125">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="6c783-126">Таблице не удается выполнить операцию, так как некоторые критерии сортировки, на которые указывает параметр _лпсорткритериа_ , слишком сложны.</span><span class="sxs-lookup"><span data-stu-id="6c783-126">The table cannot perform the operation because the particular sort criteria pointed to by the  _lpSortCriteria_ parameter is too complex.</span></span> <span data-ttu-id="6c783-127">**Сорттабле** может возвращать мапи_е_ту_комплекс в следующих условиях.</span><span class="sxs-lookup"><span data-stu-id="6c783-127">**SortTable** can return MAPI_E_TOO_COMPLEX under the following conditions.</span></span> 
    
   - <span data-ttu-id="6c783-128">Для столбца свойств, который не может сортировать реализация, запрашивается операция сортировки.</span><span class="sxs-lookup"><span data-stu-id="6c783-128">A sort operation is requested for a property column that the implementation cannot sort.</span></span>
    
   - <span data-ttu-id="6c783-129">Реализация не поддерживает порядок сортировки, запрошенный в элементе **улордер** структуры **ссортордерсет** .</span><span class="sxs-lookup"><span data-stu-id="6c783-129">The implementation does not support the sort order requested in the **ulOrder** member of the **SSortOrderSet** structure.</span></span> 
    
   - <span data-ttu-id="6c783-130">Число столбцов, которые необходимо отсортировать, как указано в элементе **ксортс** в **ссортордерсет**, больше, чем может обрабатывать реализация.</span><span class="sxs-lookup"><span data-stu-id="6c783-130">The number of columns to be sorted, as specified in the **cSorts** member in **SSortOrderSet**, is larger than the implementation can handle.</span></span>
    
   - <span data-ttu-id="6c783-131">Запрашивается операция сортировки, как указано в теге свойства в **ссортордерсет**, на основе свойства, которое не является доступным или активным, а реализация не поддерживает сортировку свойств, не включенных в набор доступных.</span><span class="sxs-lookup"><span data-stu-id="6c783-131">A sort operation is requested, as indicated by a property tag in **SSortOrderSet**, based on a property that is not in the available or active set and the implementation does not support sorting on properties not in the available set.</span></span>
    
   - <span data-ttu-id="6c783-132">Одно свойство указывается несколько раз в наборе порядка сортировки, как указано в нескольких экземплярах одного тега свойства, и реализация не может выполнять такую операцию сортировки.</span><span class="sxs-lookup"><span data-stu-id="6c783-132">One property is specified multiple times in a sort order set, as indicated by multiple instances of the same property tag, and the implementation cannot perform such a sort operation.</span></span>
    
   - <span data-ttu-id="6c783-133">Операция сортировки, основанная на столбцах с многозначными свойствами, запрашивается с помощью МВИ_ФЛАГ, а реализация не поддерживает сортировку в многозначных свойствах.</span><span class="sxs-lookup"><span data-stu-id="6c783-133">A sort operation based on multivalued property columns is requested using MVI_FLAG and the implementation does not support sorting on multivalued properties.</span></span> 
    
   - <span data-ttu-id="6c783-134">Тег свойства для свойства в **ссортордерсет** указывает свойство или тип, который не поддерживается в реализации.</span><span class="sxs-lookup"><span data-stu-id="6c783-134">A property tag for a property in **SSortOrderSet** specifies a property or type that the implementation does not support.</span></span> 
    
   - <span data-ttu-id="6c783-135">Операция сортировки, отличная от таблицы из свойства **пр_рендеринг_поситион** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)), задается только для таблицы вложений, которая поддерживает этот тип сортировки.</span><span class="sxs-lookup"><span data-stu-id="6c783-135">A sort operation other than one that proceeds through the table from the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property forward is specified only for an attachment table that supports this type of sorting.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6c783-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c783-136">Remarks</span></span>

<span data-ttu-id="6c783-137">Метод **IMAPITable:: сорттабле** упорядочивает строки в табличном представлении.</span><span class="sxs-lookup"><span data-stu-id="6c783-137">The **IMAPITable::SortTable** method orders the rows in a table view.</span></span> <span data-ttu-id="6c783-138">В то время как некоторые таблицы поддерживают как стандартную, так и сортировку по нескольким ключевым столбцам сортировки, другие таблицы в их поддержке более ограничены.</span><span class="sxs-lookup"><span data-stu-id="6c783-138">Whereas some tables support both standard and categorized sorting on various sort key columns, other tables are more limited in their support.</span></span> <span data-ttu-id="6c783-139">Как правило, поставщики адресных книг не поддерживают сортировку таблиц.</span><span class="sxs-lookup"><span data-stu-id="6c783-139">Address book providers ordinarily do not support table sorting.</span></span> <span data-ttu-id="6c783-140">Поставщики хранилищ сообщений обычно поддерживают сортировку в экстент, в котором они сохраняют порядок сортировки папок, которые отображаются при сортировке всей таблицы (таблицы без ограничений).</span><span class="sxs-lookup"><span data-stu-id="6c783-140">Message store providers usually support sorting to the extent that they keep the sort order of folders that results when a full table (a table without restrictions) is sorted.</span></span> 
  
<span data-ttu-id="6c783-141">Некоторые таблицы позволяют выполнять сортировку для любого столбца таблицы.</span><span class="sxs-lookup"><span data-stu-id="6c783-141">Some tables allow sorting to be done on any table column.</span></span> <span data-ttu-id="6c783-142">Другие таблицы не поддерживаются; вызов **сорттабле** не влияет на столбцы, не включенные в представление таблицы.</span><span class="sxs-lookup"><span data-stu-id="6c783-142">Other tables do not; columns not included in the table view are unaffected by a **SortTable** call.</span></span> <span data-ttu-id="6c783-143">Для некоторых таблиц требуется, чтобы ключи сортировки создавались только со столбцами в текущем наборе столбцов таблицы.</span><span class="sxs-lookup"><span data-stu-id="6c783-143">Some tables require that sort keys be built only with columns in the table's current column set.</span></span> 
  
<span data-ttu-id="6c783-144">Таблица может возвращать значение МАПИ_Е_НО_СУППОРТ или МАПИ_Е_ТУ_КОМПЛЕКС из **сорттабле** , когда она не может выполнить операцию сортировки.</span><span class="sxs-lookup"><span data-stu-id="6c783-144">A table can return either MAPI_E_NO_SUPPORT or MAPI_E_TOO_COMPLEX from **SortTable** when it cannot complete a sort operation.</span></span> <span data-ttu-id="6c783-145">Кроме того, поставщики хранилища не гарантируют соблюдение порядка сортировки, указанного для таблиц иерархии.</span><span class="sxs-lookup"><span data-stu-id="6c783-145">Moreover, store providers are not guaranteed to honor the sort order set specified for hierarchy tables.</span></span> 
  
<span data-ttu-id="6c783-146">Если в структуре [ссортордерсет](ssortorderset.md) есть нулевые столбцы, на которые указывает параметр _лпсорткритериа_ , то таблица возвращает текущий набор столбцов.</span><span class="sxs-lookup"><span data-stu-id="6c783-146">When there are zero columns in the [SSortOrderSet](ssortorderset.md) structure pointed to by the  _lpSortCriteria_ parameter, the table returns the current column set.</span></span> <span data-ttu-id="6c783-147">Текущий порядок сортировки можно получить, вызвав метод [IMAPITable:: куерисортордер](imapitable-querysortorder.md) в таблице.</span><span class="sxs-lookup"><span data-stu-id="6c783-147">The current sort order can be retrieved by calling the table's [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
<span data-ttu-id="6c783-148">Все закладки для таблицы становятся недействительными и должны быть удалены при выполнении вызова **сорттабле** и закладке букмарк_куррент, указывающей текущее положение курсора, должно быть равно началу таблицы.</span><span class="sxs-lookup"><span data-stu-id="6c783-148">All bookmarks for a table are invalidated and should be deleted when a call to **SortTable** is made, and the BOOKMARK_CURRENT bookmark that indicates the current cursor position, should be set to the beginning of the table.</span></span> 
  
<span data-ttu-id="6c783-149">При сортировке по столбцу, содержащему многозначное свойство без установленного флага МВИ_ФЛАГ, значения столбца рассматриваются как полностью упорядоченный кортеж.</span><span class="sxs-lookup"><span data-stu-id="6c783-149">If you are sorting on a column that contains a multivalued property without the MVI_FLAG flag set, the column's values are treated as a completely ordered tuple.</span></span> <span data-ttu-id="6c783-150">Сравнение двух многозначных столбцов сравнивает элементы столбцов по порядку с первого неравенства и возвращает равенство только в том случае, если сравниваемые столбцы содержат одни и те же значения в одном порядке.</span><span class="sxs-lookup"><span data-stu-id="6c783-150">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality, and returns equality only if the columns being compared contain the same values in the same order.</span></span> <span data-ttu-id="6c783-151">Если один столбец содержит меньше значений, чем другой, то полученное отношение имеет значение NULL для другого значения.</span><span class="sxs-lookup"><span data-stu-id="6c783-151">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="6c783-152">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="6c783-152">Notes to callers</span></span>

<span data-ttu-id="6c783-153">**Сорттабле** работает синхронно, если не установлен один из флагов.</span><span class="sxs-lookup"><span data-stu-id="6c783-153">**SortTable** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="6c783-154">Если вы установили флаг ТБЛ_БАТЧ, **сорттабле** откладывает операцию сортировки, пока не запросите данные.</span><span class="sxs-lookup"><span data-stu-id="6c783-154">If you set the TBL_BATCH flag, **SortTable** postpones the sort operation unless you request the data.</span></span> <span data-ttu-id="6c783-155">Если установлен флаг ТБЛ_АСИНК, **сорттабле** работает асинхронно, потенциально возвращать до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="6c783-155">If the TBL_ASYNC flag is set, **SortTable** operates asynchronously, potentially returning before the completion of the operation.</span></span> 
  
<span data-ttu-id="6c783-156">ВыЗовите метод [IMAPITable:: Abort](imapitable-abort.md) , чтобы остановить выполнение асинхронной операции, если сортировка должна быть выполнена немедленно.</span><span class="sxs-lookup"><span data-stu-id="6c783-156">Call the [IMAPITable::Abort](imapitable-abort.md) method to stop an asynchronous operation in progress if your sort must be done immediately.</span></span> <span data-ttu-id="6c783-157">Если **сорттабле** не удается продолжить, так как выполняется одна или несколько асинхронных операций над таблицей, возвращается мапи_е_буси.</span><span class="sxs-lookup"><span data-stu-id="6c783-157">If **SortTable** cannot continue because one or more asynchronous operations on the table are in progress, it returns MAPI_E_BUSY.</span></span> 
  
<span data-ttu-id="6c783-158">Для достижения лучшей производительности вызовите **метода SetColumns** , чтобы настроить набор столбцов таблицы и **ограничить** количество строк в таблице перед вызовом **сорттабле** для выполнения сортировки.</span><span class="sxs-lookup"><span data-stu-id="6c783-158">For best performance, call **SetColumns** to customize the table's column set and **Restrict** to limit the number of rows in the table before you call **SortTable** to perform the sort.</span></span> 
  
<span data-ttu-id="6c783-159">При сбое **сорттабле** порядок сортировки, который действовал до сбоя, по-прежнему действует.</span><span class="sxs-lookup"><span data-stu-id="6c783-159">Whenever **SortTable** fails, the sort order that was in effect before the failure is still in effect.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6c783-160">См. также</span><span class="sxs-lookup"><span data-stu-id="6c783-160">See also</span></span>

- [<span data-ttu-id="6c783-161">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="6c783-161">IMAPITable::Abort</span></span>](imapitable-abort.md)
- [<span data-ttu-id="6c783-162">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="6c783-162">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
- [<span data-ttu-id="6c783-163">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="6c783-163">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
- [<span data-ttu-id="6c783-164">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="6c783-164">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
- [<span data-ttu-id="6c783-165">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="6c783-165">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
- [<span data-ttu-id="6c783-166">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="6c783-166">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="6c783-167">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6c783-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

