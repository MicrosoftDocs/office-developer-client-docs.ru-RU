---
title: Имапитаблесетколумнс
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328821"
---
# <a name="imapitablesetcolumns"></a><span data-ttu-id="73ced-103">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="73ced-103">IMAPITable::SetColumns</span></span>

  
  
<span data-ttu-id="73ced-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73ced-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73ced-105">Определяет определенные свойства и порядок их отображения в виде столбцов в таблице.</span><span class="sxs-lookup"><span data-stu-id="73ced-105">Defines the particular properties and order of properties to appear as columns in the table.</span></span>
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="73ced-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="73ced-106">Parameters</span></span>

 <span data-ttu-id="73ced-107">_Лппроптагаррай_</span><span class="sxs-lookup"><span data-stu-id="73ced-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="73ced-108">возврата Указатель на массив тегов свойств, определяющий свойства, которые необходимо включить в качестве столбцов в таблице.</span><span class="sxs-lookup"><span data-stu-id="73ced-108">[in] Pointer to an array of property tags identifying properties to be included as columns in the table.</span></span> <span data-ttu-id="73ced-109">Для части типа свойства каждого тега можно задать допустимый тип или **пр_нулл** для резервного места для последующих дополнений.</span><span class="sxs-lookup"><span data-stu-id="73ced-109">The property type portion of each tag can be set to a valid type or to **PR_NULL** to reserve space for subsequent additions.</span></span> <span data-ttu-id="73ced-110">Параметр _лппроптагаррай_ не может иметь значение null; у каждой таблицы должен быть по крайней мере один столбец.</span><span class="sxs-lookup"><span data-stu-id="73ced-110">The  _lpPropTagArray_ parameter cannot be set to NULL; every table must have at least one column.</span></span> 
    
 <span data-ttu-id="73ced-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="73ced-111">_ulFlags_</span></span>
  
> <span data-ttu-id="73ced-112">возврата Битовая маска флагов, которые управляют возвратом асинхронного вызова в **метода SetColumns**, например, когда **метода SetColumns** используется в уведомлении.</span><span class="sxs-lookup"><span data-stu-id="73ced-112">[in] Bitmask of flags that controls the return of an asynchronous call to **SetColumns**, for example when **SetColumns** is used in notification.</span></span> <span data-ttu-id="73ced-113">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="73ced-113">The following flags can be set:</span></span> 
    
<span data-ttu-id="73ced-114">ТБЛ_АСИНК</span><span class="sxs-lookup"><span data-stu-id="73ced-114">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="73ced-115">ЗаПрашивает, чтобы операция установки столбца выполнялась асинхронно, вызывая потенциальное возвращение **метода SetColumns** до полного завершения операции.</span><span class="sxs-lookup"><span data-stu-id="73ced-115">Requests that the column setting operation be performed asynchronously causing **SetColumns** to potentially return before the operation has fully completed.</span></span> 
    
<span data-ttu-id="73ced-116">ТБЛ_БАТЧ</span><span class="sxs-lookup"><span data-stu-id="73ced-116">TBL_BATCH</span></span> 
  
> <span data-ttu-id="73ced-117">Разрешает таблице откладывать операцию установки столбца, пока данные не будут действительно необходимы.</span><span class="sxs-lookup"><span data-stu-id="73ced-117">Permits the table to postpone the column setting operation until the data is actually required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="73ced-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73ced-118">Return value</span></span>

<span data-ttu-id="73ced-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="73ced-119">S_OK</span></span> 
  
> <span data-ttu-id="73ced-120">Операция настройки столбца выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="73ced-120">The column setting operation was successful.</span></span>
    
<span data-ttu-id="73ced-121">МАПИ_Е_БУСИ</span><span class="sxs-lookup"><span data-stu-id="73ced-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="73ced-122">Выполняется другая операция, которая не позволяет запустить операцию настройки столбца.</span><span class="sxs-lookup"><span data-stu-id="73ced-122">Another operation is in progress that prevents the column setting operation from starting.</span></span> <span data-ttu-id="73ced-123">Выполнение выполняемой операции должно быть разрешено или остановлено.</span><span class="sxs-lookup"><span data-stu-id="73ced-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="73ced-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73ced-124">Remarks</span></span>

<span data-ttu-id="73ced-125">Набор столбцов таблицы — это группа свойств, которые составляют столбцы для строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="73ced-125">The column set of a table is the group of properties that make up the columns for the rows in the table.</span></span> <span data-ttu-id="73ced-126">Для каждого типа таблицы существует набор столбцов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="73ced-126">There is a default column set for each type of table.</span></span> <span data-ttu-id="73ced-127">Набор столбцов по умолчанию состоит из свойств, автоматически включаемых средством реализации таблиц.</span><span class="sxs-lookup"><span data-stu-id="73ced-127">The default column set is made up of the properties that the table implementer automatically includes.</span></span> <span data-ttu-id="73ced-128">Пользователи таблицы могут изменить этот набор по умолчанию, вызвав метод **IMAPITable:: метода SetColumns** .</span><span class="sxs-lookup"><span data-stu-id="73ced-128">Table users can alter this default set by calling the **IMAPITable::SetColumns** method.</span></span> <span data-ttu-id="73ced-129">Они могут запросить Добавление других столбцов в набор по умолчанию, если средство реализации таблиц поддерживает их удаление или изменение порядка столбцов.</span><span class="sxs-lookup"><span data-stu-id="73ced-129">They can request that other columns be added to the default set if the table implementer supports them that columns be removed, or that the order of columns be changed.</span></span> <span data-ttu-id="73ced-130">**Метода SetColumns** указывает столбцы, возвращаемые с каждой строкой, и порядок этих столбцов в строке.</span><span class="sxs-lookup"><span data-stu-id="73ced-130">**SetColumns** specifies the columns that are returned with each row and the order of these columns within the row.</span></span> 
  
<span data-ttu-id="73ced-131">Успешное выполнение операции **метода SetColumns** очевидно только после выполнения следующего вызова для получения данных таблицы.</span><span class="sxs-lookup"><span data-stu-id="73ced-131">The success of the **SetColumns** operation is apparent only after a subsequent call has been made to retrieve the data of the table.</span></span> <span data-ttu-id="73ced-132">Затем сообщается о сообщениях об ошибках.</span><span class="sxs-lookup"><span data-stu-id="73ced-132">It is then that any errors are reported.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="73ced-133">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="73ced-133">Notes to implementers</span></span>

<span data-ttu-id="73ced-134">Некоторые поставщики допускают вызов **метода SetColumns** для заказа только тех столбцов таблицы, которые являются частью доступных столбцов для представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="73ced-134">Some providers allow a **SetColumns** call to order only table columns that are part of the available columns for a table view.</span></span> <span data-ttu-id="73ced-135">Другие поставщики допускают вызов **метода SetColumns** для упорядочения всех столбцов таблицы, включая те, которые содержат свойства, не приходящие к исходному набору столбцов.</span><span class="sxs-lookup"><span data-stu-id="73ced-135">Other providers allow a **SetColumns** call to order all table columns, including those containing properties not in the original column set.</span></span> 
  
<span data-ttu-id="73ced-136">Если для асинхронных операций задан ТБЛ_БАТЧ, поставщики должны возвращать тип свойства ПТ_ЕРРОР и значение свойства NULL для неподдерживаемых столбцов.</span><span class="sxs-lookup"><span data-stu-id="73ced-136">When TBL_BATCH is set for asynchronous operations, providers should return a property type of PT_ERROR and a property value of NULL for columns that are not supported.</span></span>
  
<span data-ttu-id="73ced-137">Вам не нужно отвечать на флаг ТБЛ_АСИНК, запрашивающий выполнение операции асинхронно.</span><span class="sxs-lookup"><span data-stu-id="73ced-137">You do not need to respond to the TBL_ASYNC flag requesting that the operation be asynchronous.</span></span> <span data-ttu-id="73ced-138">Если вы не поддерживаете определение набора асинхронных столбцов, выполните операцию в синхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="73ced-138">If you do not support asynchronous column set definition, perform the operation synchronously.</span></span> <span data-ttu-id="73ced-139">Если вы можете поддерживать флаг ТБЛ_АСИНК и еще выполняется другая асинхронная операция, возвратите МАПИ_Е_БУСИ.</span><span class="sxs-lookup"><span data-stu-id="73ced-139">If you can support the TBL_ASYNC flag and another asynchronous operation is still in progress, return MAPI_E_BUSY.</span></span> <span data-ttu-id="73ced-140">В противном случае возвращается значение S_OK независимо от того, поддерживаются ли все свойства, включенные в массив тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="73ced-140">Otherwise, return S_OK regardless of whether or not you support all of the properties included in the property tag array.</span></span> <span data-ttu-id="73ced-141">Ошибки, вызванные неподдерживаемыми свойствами, возвращаются из методов **IMAPITable** , которые получают данные, например **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="73ced-141">Errors resulting from unsupported properties should be returned from **IMAPITable** methods that retrieve data, such as **QueryRows**.</span></span> 
  
<span data-ttu-id="73ced-142">Не создавайте уведомления для строк таблицы, которые скрыты от представления вызовами для **ограничения**.</span><span class="sxs-lookup"><span data-stu-id="73ced-142">Do not generate notifications for table rows that are hidden from view by calls to **Restrict**.</span></span> 
  
<span data-ttu-id="73ced-143">При отправке уведомлений таблицы порядок следования свойств в элементе **Row** структуры [табле_нотификатион](table_notification.md) и порядке, указанНому последним вызовом **метода SetColumns** , должен совпадать со временем запроса уведомления. Отправлено.</span><span class="sxs-lookup"><span data-stu-id="73ced-143">When sending table notifications, the order of the properties in the **row** member of the [TABLE_NOTIFICATION](table_notification.md) structure and the order specified by the most recent **SetColumns** call must be the same as of the time that the notification request was sent.</span></span> 
  
<span data-ttu-id="73ced-144">Другой флаг, ТБЛ_БАТЧ, позволяет звонящим указать, что средство реализации таблиц может отложить оценку результатов операции до следующего момента.</span><span class="sxs-lookup"><span data-stu-id="73ced-144">Another flag, TBL_BATCH, allows callers to specify that the table implementer can defer evaluating the results of the operation until a later time.</span></span> <span data-ttu-id="73ced-145">Когда это возможно, абонентам следует устанавливать этот флаг, так как пакетная операция повышает производительность.</span><span class="sxs-lookup"><span data-stu-id="73ced-145">Whenever possible, callers should set this flag because batched operation improves performance.</span></span>
  
<span data-ttu-id="73ced-146">Часто вызывающим абонентам часто удобно зарезервировать некоторые столбцы в извлеченных строках для значений, которые будут добавлены позже.</span><span class="sxs-lookup"><span data-stu-id="73ced-146">It is often convenient for callers to reserve some columns in the retrieved row set for values to be added later.</span></span> <span data-ttu-id="73ced-147">Вызывающие объекты выполняют эту задачу, размещая **пр_нулл** ([PidTagNull](pidtagnull-canonical-property.md)) в нужных позициях в массиве тегов свойств, переданном в **метода SetColumns**; После этого таблица передается **пр_нулл** в этих положениях во всех строках, полученных с помощью **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="73ced-147">Callers do this by placing **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) at the desired positions in the property tag array passed to **SetColumns**; the table will then pass back **PR_NULL** at those positions in all rows retrieved with **QueryRows**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="73ced-148">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="73ced-148">Notes to callers</span></span>

<span data-ttu-id="73ced-149">При создании массива тегов свойств для параметра _лппроптагаррай_ упорядочивайте теги в том порядке, в котором должны отображаться столбцы в представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="73ced-149">When building the property tag array for the  _lpPropTagArray_ parameter, order the tags in the order that you want the columns to appear in the table view.</span></span> 
  
<span data-ttu-id="73ced-150">Можно указать многозначные свойства, включаемые в набор столбцов, применяя флаг многозначного экземпляра или константу МВИ_ФЛАГ к тегу свойства.</span><span class="sxs-lookup"><span data-stu-id="73ced-150">You can specify multivalued properties to be included in the column set by applying the multivalued instance flag, or MVI_FLAG constant, to the property tag.</span></span> <span data-ttu-id="73ced-151">Установите этот флаг, передав тег свойства для однозначной версии свойства в качестве параметра для макроса МВИ_ПРОП следующим образом:</span><span class="sxs-lookup"><span data-stu-id="73ced-151">Set this flag by passing the property tag for the single-valued version of the property as a parameter to the MVI_PROP macro as follows:</span></span>
  
```
MVI_PROP(ulPropTag)

```

<span data-ttu-id="73ced-152">Макрос МВИ_ПРОП задает МВИ_ФЛАГ для свойства, преобразуя тег в многозначный тег.</span><span class="sxs-lookup"><span data-stu-id="73ced-152">The MVI_PROP macro will set MVI_FLAG for the property, turning the tag into a multivalued tag.</span></span> <span data-ttu-id="73ced-153">Если вы ошибочно попытаетесь вызвать МВИ_ПРОП для свойства с одним значением, MAPI проигнорирует вызов и оставит неизменным тег свойства.</span><span class="sxs-lookup"><span data-stu-id="73ced-153">If you erroneously try to call MVI_PROP on a single-valued property, MAPI will ignore the call and leave the property tag unchanged.</span></span> 
  
<span data-ttu-id="73ced-154">Можно включить теги свойств в **пр_нулл** в массиве тегов свойств, чтобы зарезервировать пространство в наборе столбцов.</span><span class="sxs-lookup"><span data-stu-id="73ced-154">You can include property tags set to **PR_NULL** in the property tag array to reserve space in the column set.</span></span> <span data-ttu-id="73ced-155">Резервирование пространства позволяет добавить в набор столбцов, не выполняя выделение нового массива тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="73ced-155">Reserving space allows you to add to a column set without having to allocate a new property tag array.</span></span> 
  
<span data-ttu-id="73ced-156">Если при вызове **метода SetColumns** происходит изменение порядка столбцов таблицы и один или несколько этих столбцов представляют многозначное свойство, можно увеличить количество строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="73ced-156">When your call to **SetColumns** causes a change to the order of a table's columns and one or more of these columns represent a multivalued property, it is possible for the number of rows in the table to increase.</span></span> <span data-ttu-id="73ced-157">В таком случае все закладки для таблицы отбрасываются.</span><span class="sxs-lookup"><span data-stu-id="73ced-157">If this occurs, all of the bookmarks for the table are discarded.</span></span> <span data-ttu-id="73ced-158">Дополнительные сведения о том, как Многозначные столбцы влияют на таблицы, можно посмотреть [в разделе Работа с](working-with-multivalued-columns.md)многоЗначными столбцами.</span><span class="sxs-lookup"><span data-stu-id="73ced-158">For more information about how multivalued columns affect tables, see [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
<span data-ttu-id="73ced-159">Параметр columns по умолчанию является синхронной операцией.</span><span class="sxs-lookup"><span data-stu-id="73ced-159">Setting columns is by default a synchronous operation.</span></span> <span data-ttu-id="73ced-160">Тем не менее, можно разрешить таблице отложить операцию до тех пор, пока данные не понадобятся, установив флаг ТБЛ_БАТЧ.</span><span class="sxs-lookup"><span data-stu-id="73ced-160">However, you can allow the table to postpone the operation until such time as the data is needed by setting the TBL_BATCH flag.</span></span> <span data-ttu-id="73ced-161">Установка этого флага может увеличить производительность.</span><span class="sxs-lookup"><span data-stu-id="73ced-161">Setting this flag can improve performance.</span></span> <span data-ttu-id="73ced-162">Другой флаг, ТБЛ_АСИНК, делает операцию асинхронной, позволяя **метода SetColumns** возвращаться до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="73ced-162">Another flag, TBL_ASYNC, makes the operation asynchronous, allowing **SetColumns** to return before the operation is complete.</span></span> <span data-ttu-id="73ced-163">Чтобы определить, когда выполняется завершение, вызовите метод [IMAPITable::.](imapitable-getstatus.md)</span><span class="sxs-lookup"><span data-stu-id="73ced-163">To determine when completion occurs, call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span>
  
<span data-ttu-id="73ced-164">Если при вызове **метода SetColumns** возвращается мапи_е_буси, указывающий на то, что другая операция препятствует запуску, можно вызвать команду [IMAPITable:: Abort](imapitable-abort.md) , чтобы остановить выполняемую операцию.</span><span class="sxs-lookup"><span data-stu-id="73ced-164">If a call to **SetColumns** returns MAPI_E_BUSY, indicating that another operation is preventing your operation from starting, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the operation in progress.</span></span> 
  
<span data-ttu-id="73ced-165">Вы также можете вызвать [храддколумнсекс](hraddcolumnsex.md) , чтобы изменить набор столбцов.</span><span class="sxs-lookup"><span data-stu-id="73ced-165">You can also call [HrAddColumnsEx](hraddcolumnsex.md) to change a column set.</span></span> <span data-ttu-id="73ced-166">Разница между **храддколумнсекс** и **IMAPITable:: метода SetColumns** заключается в том, что **храддколумнсекс** является менее гибким; Он может только добавлять столбцы.</span><span class="sxs-lookup"><span data-stu-id="73ced-166">The difference between **HrAddColumnsEx** and **IMAPITable::SetColumns** is that **HrAddColumnsEx** is less flexible; it can only add columns.</span></span> <span data-ttu-id="73ced-167">Дополнительные столбцы помещаются в начало набора столбцов; После этих столбцов отображаются все существующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="73ced-167">The additional columns are placed at the beginning of the column set; all existing columns appear following these columns.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="73ced-168">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="73ced-168">MFCMAPI reference</span></span>

<span data-ttu-id="73ced-169">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="73ced-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="73ced-170">**Файл**</span><span class="sxs-lookup"><span data-stu-id="73ced-170">**File**</span></span>|<span data-ttu-id="73ced-171">**Функция**</span><span class="sxs-lookup"><span data-stu-id="73ced-171">**Function**</span></span>|<span data-ttu-id="73ced-172">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="73ced-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="73ced-173">Контентстаблелистктрл. cpp</span><span class="sxs-lookup"><span data-stu-id="73ced-173">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="73ced-174">Кконтентстаблелистктрл::D Осетколумнс</span><span class="sxs-lookup"><span data-stu-id="73ced-174">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="73ced-175">MFCMAPI использует метод **IMAPITable:: метода SetColumns** , чтобы задать нужные столбцы для таблицы.</span><span class="sxs-lookup"><span data-stu-id="73ced-175">MFCMAPI uses the **IMAPITable::SetColumns** method to set the desired columns for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="73ced-176">См. также</span><span class="sxs-lookup"><span data-stu-id="73ced-176">See also</span></span>



[<span data-ttu-id="73ced-177">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="73ced-177">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="73ced-178">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="73ced-178">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="73ced-179">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="73ced-179">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="73ced-180">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="73ced-180">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="73ced-181">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="73ced-181">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="73ced-182">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="73ced-182">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="73ced-183">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="73ced-183">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="73ced-184">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="73ced-184">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="73ced-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="73ced-185">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="73ced-186">SRowSet</span><span class="sxs-lookup"><span data-stu-id="73ced-186">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="73ced-187">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="73ced-187">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="73ced-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="73ced-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="73ced-189">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="73ced-189">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

