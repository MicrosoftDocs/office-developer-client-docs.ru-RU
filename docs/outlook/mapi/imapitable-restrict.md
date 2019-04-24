---
title: Имапитаблерестрикт
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328849"
---
# <a name="imapitablerestrict"></a><span data-ttu-id="76612-103">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="76612-103">IMAPITable::Restrict</span></span>

  
  
<span data-ttu-id="76612-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76612-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76612-105">ПриМеняет фильтр к таблице, уменьшая набор строк только на те строки, которые соответствуют заданному условию.</span><span class="sxs-lookup"><span data-stu-id="76612-105">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="76612-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="76612-106">Parameters</span></span>

 <span data-ttu-id="76612-107">_Лпрестриктион_</span><span class="sxs-lookup"><span data-stu-id="76612-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="76612-108">возврата Указатель на структуру [срестриктион](srestriction.md) , определяющую условия фильтра.</span><span class="sxs-lookup"><span data-stu-id="76612-108">[in] Pointer to an [SRestriction](srestriction.md) structure defining the conditions of the filter.</span></span> <span data-ttu-id="76612-109">При передаче значения NULL в параметре _лпрестриктион_ удаляется текущий фильтр.</span><span class="sxs-lookup"><span data-stu-id="76612-109">Passing NULL in the  _lpRestriction_ parameter removes the current filter.</span></span> 
    
 <span data-ttu-id="76612-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="76612-110">_ulFlags_</span></span>
  
> <span data-ttu-id="76612-111">возврата Битовая маска флагов, которые управляют временем операции ограничения.</span><span class="sxs-lookup"><span data-stu-id="76612-111">[in] Bitmask of flags that controls the timing of the restriction operation.</span></span> <span data-ttu-id="76612-112">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="76612-112">The following flags can be set:</span></span>
    
<span data-ttu-id="76612-113">ТБЛ_АСИНК</span><span class="sxs-lookup"><span data-stu-id="76612-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="76612-114">Асинхронно запускает операцию и возвращает результат до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="76612-114">Starts the operation asynchronously and returns before the operation completes.</span></span>
    
<span data-ttu-id="76612-115">ТБЛ_БАТЧ</span><span class="sxs-lookup"><span data-stu-id="76612-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="76612-116">ОтКладывает оценку фильтра до тех пор, пока данные в таблице не будут обязательными.</span><span class="sxs-lookup"><span data-stu-id="76612-116">Defers evaluation of the filter until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="76612-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="76612-117">Return value</span></span>

<span data-ttu-id="76612-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="76612-118">S_OK</span></span> 
  
> <span data-ttu-id="76612-119">Фильтр успешно применен.</span><span class="sxs-lookup"><span data-stu-id="76612-119">The filter was successfully applied.</span></span>
    
<span data-ttu-id="76612-120">МАПИ_Е_БУСИ</span><span class="sxs-lookup"><span data-stu-id="76612-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="76612-121">Выполняется другая операция, которая не позволяет запустить операцию ограничения.</span><span class="sxs-lookup"><span data-stu-id="76612-121">Another operation is in progress that prevents the restriction operation from starting.</span></span> <span data-ttu-id="76612-122">Выполнение выполняемой операции должно быть разрешено или остановлено.</span><span class="sxs-lookup"><span data-stu-id="76612-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="76612-123">МАПИ_Е_ТУ_КОМПЛЕКС</span><span class="sxs-lookup"><span data-stu-id="76612-123">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="76612-124">Таблице не удается выполнить операцию, так как определенный фильтр, на который указывает параметр _лпрестриктион_ , слишком сложный.</span><span class="sxs-lookup"><span data-stu-id="76612-124">The table cannot perform the operation because the particular filter pointed to by the  _lpRestriction_ parameter is too complicated.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="76612-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="76612-125">Remarks</span></span>

<span data-ttu-id="76612-126">Метод **IMAPITable:: restrict** устанавливает ограничение или фильтр для таблицы.</span><span class="sxs-lookup"><span data-stu-id="76612-126">The **IMAPITable::Restrict** method establishes a restriction, or filter, on a table.</span></span> <span data-ttu-id="76612-127">Если имеется предыдущее ограничение, оно отбрасывается и применяется новый.</span><span class="sxs-lookup"><span data-stu-id="76612-127">If there is a previous restriction, it is discarded and the new one applied.</span></span> <span data-ttu-id="76612-128">Применение ограничения не влияет на базовые данные таблицы; Он просто изменяет представление, ограничивая строки, которые могут быть извлечены в строки, содержащие данные, удовлетворяющие ограничению.</span><span class="sxs-lookup"><span data-stu-id="76612-128">Applying a restriction has no affect on the underlying data of a table; it simply alters the view by limiting the rows that can be retrieved to rows containing data that satisfy the restriction.</span></span> 
  
<span data-ttu-id="76612-129">Существует несколько различных типов ограничений, каждая из которых описана в разных структурах.</span><span class="sxs-lookup"><span data-stu-id="76612-129">There are several different types of restrictions, each described with a different structure.</span></span> <span data-ttu-id="76612-130">Структура [срестриктион](srestriction.md) содержит два члена: значение, которое указывает тип ограничения и конкретную структуру, подходящую для этого типа.</span><span class="sxs-lookup"><span data-stu-id="76612-130">The [SRestriction](srestriction.md) structure contains two members: a value that indicates the type of restriction and the specific structure applicable for that type.</span></span> 
  
<span data-ttu-id="76612-131">Уведомления для строк таблицы, которые скрыты от представлений по вызовам **ограничения** , никогда не создаются.</span><span class="sxs-lookup"><span data-stu-id="76612-131">Notifications for table rows that are hidden from view by calls to **Restrict** are never generated.</span></span> 
  
<span data-ttu-id="76612-132">Ограничение свойства для многозначного свойства работает как ограничение на свойство с одним значением.</span><span class="sxs-lookup"><span data-stu-id="76612-132">A property restriction on a multivalued property works like a restriction on a single-valued property.</span></span> <span data-ttu-id="76612-133">Для многозначного свойства, используемого в ограничении свойств, должен быть установлен флаг МВИ_ФЛАГ.</span><span class="sxs-lookup"><span data-stu-id="76612-133">A multivalued property to be used in a property restriction must have the MVI_FLAG flag set.</span></span> <span data-ttu-id="76612-134">Если этот флаг не установлен, он рассматривается как полностью упорядоченный кортеж.</span><span class="sxs-lookup"><span data-stu-id="76612-134">If it doesn't have this flag set, it is treated as a totally ordered tuple.</span></span> <span data-ttu-id="76612-135">Сравнение двух многозначных столбцов сравнивает элементы столбцов по порядку, сообщая о связи столбцов по первому неравенству.</span><span class="sxs-lookup"><span data-stu-id="76612-135">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality.</span></span> <span data-ttu-id="76612-136">Равенство возвращается только в том случае, если сравниваемые столбцы содержат одни и те же значения в одном и том же порядке.</span><span class="sxs-lookup"><span data-stu-id="76612-136">Equality is returned only if the columns compared contain the same values in the same order.</span></span> <span data-ttu-id="76612-137">Если один столбец содержит меньше значений, чем другой, то полученное отношение имеет значение NULL для другого значения.</span><span class="sxs-lookup"><span data-stu-id="76612-137">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
<span data-ttu-id="76612-138">Более подробную информацию об ограничениях можно узнать в статье [ограничения](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="76612-138">For more information about restrictions, see [About Restrictions](about-restrictions.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="76612-139">Если вы создаете динамические запросы для поиска данных на сервере, используйте метод **FindRow** , вместо того чтобы использовать метод **restrict** и метод **QueryRows** вместе.</span><span class="sxs-lookup"><span data-stu-id="76612-139">If you create dynamic queries to search for data on the server, use the **FindRow** method instead of using the **Restrict** method and the **QueryRows** method together.</span></span> <span data-ttu-id="76612-140">Метод **restrict** создает кэшированное представление, используемое для оценки всех сообщений, добавляемых в базовую папку или измененных в ней.</span><span class="sxs-lookup"><span data-stu-id="76612-140">The **Restrict** method creates a cached view that is used to evaluate all messages added to or modified in the base folder.</span></span> <span data-ttu-id="76612-141">Если клиентское приложение использует метод **restrict** для каждого динамического запроса, для каждого запроса будет создано кэшированное представление.</span><span class="sxs-lookup"><span data-stu-id="76612-141">If a client application uses the **Restrict** method for each dynamic query, a cached view will be created for each query.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="76612-142">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="76612-142">Notes to callers</span></span>

<span data-ttu-id="76612-143">Чтобы отменить текущее ограничение без создания нового, передайте значение NULL в _лпрестриктион_.</span><span class="sxs-lookup"><span data-stu-id="76612-143">To discard the current restriction without creating a new one, pass NULL in  _lpRestriction_.</span></span>
  
<span data-ttu-id="76612-144">Если выполняется другой асинхронный вызов таблицы, что приводит \*\*\*\* к возврату мапи_е_буси, вы можете вызвать метод [IMAPITable:: Abort](imapitable-abort.md) для остановки вызова.</span><span class="sxs-lookup"><span data-stu-id="76612-144">If another asynchronous table call is in progress, causing **Restrict** to return MAPI_E_BUSY, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the call.</span></span> 
  
 <span data-ttu-id="76612-145">Если вы не задаете один из флагов, то **Ограничьте** работу синхронно.</span><span class="sxs-lookup"><span data-stu-id="76612-145">**Restrict** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="76612-146">Если установлен флаг ТБЛ_БАТЧ, **ограничение** откладывает оценку ограничения, если вы не запрашиваете данные.</span><span class="sxs-lookup"><span data-stu-id="76612-146">If you set the TBL_BATCH flag, **Restrict** postpones the evaluation of the restriction unless you request the data.</span></span> <span data-ttu-id="76612-147">Если установлен флаг ТБЛ_АСИНК, **ограничение**действует асинхронно, потенциально возвращая до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="76612-147">If the TBL_ASYNC flag is set, **Restrict**operates asynchronously, potentially returning before the completion of the operation.</span></span>
  
<span data-ttu-id="76612-148">Все закладки для таблицы отбрасываются при выполнении вызова reStricted \*\*\*\* , а букмарк_куррент текущее положение курсора задается в начале таблицы.</span><span class="sxs-lookup"><span data-stu-id="76612-148">All bookmarks for a table are discarded when a call to **Restrict** is made, and BOOKMARK_CURRENT, the current cursor position, is set to the beginning of the table.</span></span> 
  
<span data-ttu-id="76612-149">Если вы попытаетесь применить ограничение свойства к свойству, которое не входит в набор столбцов таблицы, результаты будут неопределенными.</span><span class="sxs-lookup"><span data-stu-id="76612-149">If you attempt to impose a property restriction on a property that is not in the table's column set, the results are undefined.</span></span> <span data-ttu-id="76612-150">Если вы не уверены в том, что свойство поддерживается в таблице, объедините ограничение свойства с ограничением EXISTS.</span><span class="sxs-lookup"><span data-stu-id="76612-150">Whenever you are unsure as to whether a property is supported in a table, combine the property restriction with an exists restriction.</span></span> <span data-ttu-id="76612-151">Ограничение Exists проверяет наличие свойства перед попыткой применить ограничение свойства.</span><span class="sxs-lookup"><span data-stu-id="76612-151">The exists restriction checks for the existence of the property before attempting to impose the property restriction.</span></span> 
  
<span data-ttu-id="76612-152">Не ожидается получение уведомления таблицы для строки, которая была отфильтрована из таблицы из-за ограничения.</span><span class="sxs-lookup"><span data-stu-id="76612-152">Do not expect to receive a table notification on a row that has been filtered from a table due to a restriction.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="76612-153">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="76612-153">MFCMAPI reference</span></span>

<span data-ttu-id="76612-154">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="76612-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="76612-155">**Файл**</span><span class="sxs-lookup"><span data-stu-id="76612-155">**File**</span></span>|<span data-ttu-id="76612-156">**Функция**</span><span class="sxs-lookup"><span data-stu-id="76612-156">**Function**</span></span>|<span data-ttu-id="76612-157">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="76612-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="76612-158">Контентстаблелистктрл. cpp</span><span class="sxs-lookup"><span data-stu-id="76612-158">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="76612-159">Кконтентстаблелистктрл:: Апплирестриктион</span><span class="sxs-lookup"><span data-stu-id="76612-159">CContentsTableListCtrl::ApplyRestriction</span></span>  <br/> |<span data-ttu-id="76612-160">MFCMAPI использует метод **IMAPITable:: restrict** , чтобы задать ограничение для таблицы.</span><span class="sxs-lookup"><span data-stu-id="76612-160">MFCMAPI uses the **IMAPITable::Restrict** method to set a restriction on a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="76612-161">См. также</span><span class="sxs-lookup"><span data-stu-id="76612-161">See also</span></span>



[<span data-ttu-id="76612-162">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="76612-162">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="76612-163">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="76612-163">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="76612-164">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="76612-164">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="76612-165">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="76612-165">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="76612-166">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="76612-166">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="76612-167">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="76612-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="76612-168">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="76612-168">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

