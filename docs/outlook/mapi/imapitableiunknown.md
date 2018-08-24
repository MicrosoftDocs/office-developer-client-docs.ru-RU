---
title: IMAPITable IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable
api_type:
- COM
ms.assetid: f25be2b1-0f94-4a0c-b29d-d2201dc70ab7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a5504711bdeac4ef94cbe47395ceb8163b60ad68
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584333"
---
# <a name="imapitable--iunknown"></a><span data-ttu-id="dfc63-103">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dfc63-103">IMAPITable : IUnknown</span></span>

  
  
<span data-ttu-id="dfc63-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dfc63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dfc63-105">Содержит сведения о таблицы только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dfc63-105">Provides a read-only view of a table.</span></span> <span data-ttu-id="dfc63-106">**IMAPITable** используется клиентами и поставщиков услуг для работы с внешний вид таблицы.</span><span class="sxs-lookup"><span data-stu-id="dfc63-106">**IMAPITable** is used by clients and service providers to manipulate the way a table appears.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dfc63-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="dfc63-107">Header file:</span></span>  <br/> |<span data-ttu-id="dfc63-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dfc63-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="dfc63-109">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="dfc63-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="dfc63-110">Список таблиц</span><span class="sxs-lookup"><span data-stu-id="dfc63-110">Table objects</span></span>  <br/> |
|<span data-ttu-id="dfc63-111">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="dfc63-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="dfc63-112">Поставщиков услуг и MAPI</span><span class="sxs-lookup"><span data-stu-id="dfc63-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="dfc63-113">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="dfc63-113">Called by:</span></span>  <br/> |<span data-ttu-id="dfc63-114">Клиентские приложения, поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="dfc63-114">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="dfc63-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="dfc63-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="dfc63-116">IID_IMAPITable</span><span class="sxs-lookup"><span data-stu-id="dfc63-116">IID_IMAPITable</span></span>  <br/> |
|<span data-ttu-id="dfc63-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="dfc63-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="dfc63-118">LPMAPITABLE</span><span class="sxs-lookup"><span data-stu-id="dfc63-118">LPMAPITABLE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="dfc63-119">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="dfc63-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="dfc63-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="dfc63-120">GetLastError</span></span>](imapitable-getlasterror.md) <br/> |<span data-ttu-id="dfc63-121">Возвращает структуру [MAPIERROR](mapierror.md) , содержащий сведения о предыдущем ошибки в таблице.</span><span class="sxs-lookup"><span data-stu-id="dfc63-121">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span>  <br/> |
|[<span data-ttu-id="dfc63-122">Уведомить</span><span class="sxs-lookup"><span data-stu-id="dfc63-122">Advise</span></span>](imapitable-advise.md) <br/> |<span data-ttu-id="dfc63-123">Регистрация для получения уведомлений о влияния на таблице указанных событий.</span><span class="sxs-lookup"><span data-stu-id="dfc63-123">Registers to receive notification of specified events affecting the table.</span></span>  <br/> |
|[<span data-ttu-id="dfc63-124">Unadvise</span><span class="sxs-lookup"><span data-stu-id="dfc63-124">Unadvise</span></span>](imapitable-unadvise.md) <br/> |<span data-ttu-id="dfc63-125">Показано, как отменить отправку уведомлений, ранее настройка с помощью вызова метода **IMAPITable::Advise** .</span><span class="sxs-lookup"><span data-stu-id="dfc63-125">Cancels the sending of notifications previously set up with a call to the **IMAPITable::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="dfc63-126">GetStatus</span><span class="sxs-lookup"><span data-stu-id="dfc63-126">GetStatus</span></span>](imapitable-getstatus.md) <br/> |<span data-ttu-id="dfc63-127">Возвращает состояние в таблице и тип.</span><span class="sxs-lookup"><span data-stu-id="dfc63-127">Returns the table's status and type.</span></span>  <br/> |
|[<span data-ttu-id="dfc63-128">Метода SetColumns</span><span class="sxs-lookup"><span data-stu-id="dfc63-128">SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="dfc63-129">Определяет конкретного свойства и порядок свойств в виде столбцов в таблице.</span><span class="sxs-lookup"><span data-stu-id="dfc63-129">Defines the particular properties and order of properties to appear as columns in the table.</span></span>  <br/> |
|[<span data-ttu-id="dfc63-130">QueryColumns</span><span class="sxs-lookup"><span data-stu-id="dfc63-130">QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="dfc63-131">Возвращает список столбцов для таблицы.</span><span class="sxs-lookup"><span data-stu-id="dfc63-131">Returns a list of columns for the table.</span></span>  <br/> |
|[<span data-ttu-id="dfc63-132">GetRowCount</span><span class="sxs-lookup"><span data-stu-id="dfc63-132">GetRowCount</span></span>](imapitable-getrowcount.md) <br/> |<span data-ttu-id="dfc63-133">Возвращает общее число строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="dfc63-133">Returns the total number of rows in the table.</span></span>  <br/> |
|[<span data-ttu-id="dfc63-134">SeekRow</span><span class="sxs-lookup"><span data-stu-id="dfc63-134">SeekRow</span></span>](imapitable-seekrow.md) <br/> |<span data-ttu-id="dfc63-135">Перемещение курсора в определенное место в таблице.</span><span class="sxs-lookup"><span data-stu-id="dfc63-135">Moves the cursor to a specific position in the table.</span></span>  <br/> |
|[<span data-ttu-id="dfc63-136">SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="dfc63-136">SeekRowApprox</span></span>](imapitable-seekrowapprox.md) <br/> |<span data-ttu-id="dfc63-137">Перемещение курсора в приблизительно, например дробная позицию в таблице.</span><span class="sxs-lookup"><span data-stu-id="dfc63-137">Moves the cursor to an approximate fractional position in the table.</span></span>  <br/> |
|[<span data-ttu-id="dfc63-138">QueryPosition</span><span class="sxs-lookup"><span data-stu-id="dfc63-138">QueryPosition</span></span>](imapitable-queryposition.md) <br/> |<span data-ttu-id="dfc63-139">Получает текущую позицию строки в таблице курсора на основании дробное значение.</span><span class="sxs-lookup"><span data-stu-id="dfc63-139">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>  <br/> |
|[<span data-ttu-id="dfc63-140">FindRow</span><span class="sxs-lookup"><span data-stu-id="dfc63-140">FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="dfc63-141">Находит следующую строку в таблице, которая соответствует определенным условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="dfc63-141">Finds the next row in a table that matches specific search criteria.</span></span>  <br/> |
|[<span data-ttu-id="dfc63-142">Ограничить</span><span class="sxs-lookup"><span data-stu-id="dfc63-142">Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="dfc63-143">Применение фильтра к таблице, уменьшение строки, задайте значение только строк, соответствующих определенным условиям.</span><span class="sxs-lookup"><span data-stu-id="dfc63-143">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="dfc63-144">CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="dfc63-144">CreateBookmark</span></span>](imapitable-createbookmark.md) <br/> |<span data-ttu-id="dfc63-145">Помечает текущую позицию в таблице.</span><span class="sxs-lookup"><span data-stu-id="dfc63-145">Marks the table's current position.</span></span>  <br/> |
|[<span data-ttu-id="dfc63-146">FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="dfc63-146">FreeBookmark</span></span>](imapitable-freebookmark.md) <br/> |<span data-ttu-id="dfc63-147">Освобождает память, связанную с закладку.</span><span class="sxs-lookup"><span data-stu-id="dfc63-147">Releases the memory associated with a bookmark.</span></span>  <br/> |
|[<span data-ttu-id="dfc63-148">SortTable</span><span class="sxs-lookup"><span data-stu-id="dfc63-148">SortTable</span></span>](imapitable-sorttable.md) <br/> |<span data-ttu-id="dfc63-149">Упорядочивает строки в таблице, на основе критерия сортировки.</span><span class="sxs-lookup"><span data-stu-id="dfc63-149">Orders the rows of the table based on sort criteria.</span></span>  <br/> |
|[<span data-ttu-id="dfc63-150">QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="dfc63-150">QuerySortOrder</span></span>](imapitable-querysortorder.md) <br/> |<span data-ttu-id="dfc63-151">Получает текущий порядок сортировки для таблицы.</span><span class="sxs-lookup"><span data-stu-id="dfc63-151">Retrieves the current sort order for a table.</span></span>  <br/> |
|[<span data-ttu-id="dfc63-152">QueryRows</span><span class="sxs-lookup"><span data-stu-id="dfc63-152">QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="dfc63-153">Возвращает один или несколько строк из таблицы, начиная с текущей позиции курсора.</span><span class="sxs-lookup"><span data-stu-id="dfc63-153">Returns one or more rows from a table, beginning at the current cursor position.</span></span>  <br/> |
|[<span data-ttu-id="dfc63-154">Прервать</span><span class="sxs-lookup"><span data-stu-id="dfc63-154">Abort</span></span>](imapitable-abort.md) <br/> |<span data-ttu-id="dfc63-155">Останавливает асинхронной операции в данный момент для таблицы.</span><span class="sxs-lookup"><span data-stu-id="dfc63-155">Stops any asynchronous operations currently in progress for the table.</span></span>  <br/> |
|[<span data-ttu-id="dfc63-156">ExpandRow</span><span class="sxs-lookup"><span data-stu-id="dfc63-156">ExpandRow</span></span>](imapitable-expandrow.md) <br/> |<span data-ttu-id="dfc63-157">При развертывании категории свернутые таблицы, добавление конечные строки, относящегося к категории, которую требуется в табличном представлении.</span><span class="sxs-lookup"><span data-stu-id="dfc63-157">Expands a collapsed table category, adding the leaf rows belonging to the category to the table view.</span></span>  <br/> |
|[<span data-ttu-id="dfc63-158">CollapseRow</span><span class="sxs-lookup"><span data-stu-id="dfc63-158">CollapseRow</span></span>](imapitable-collapserow.md) <br/> |<span data-ttu-id="dfc63-159">Сворачивание категорию расширенной таблицы, удаление конечные строки, относящегося к категории из в табличном представлении.</span><span class="sxs-lookup"><span data-stu-id="dfc63-159">Collapses an expanded table category, removing the leaf rows belonging to the category from the table view.</span></span>  <br/> |
|[<span data-ttu-id="dfc63-160">WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="dfc63-160">WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |<span data-ttu-id="dfc63-161">Приостанавливает работу до завершения одного или нескольких асинхронной операции выполняется в таблице.</span><span class="sxs-lookup"><span data-stu-id="dfc63-161">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>  <br/> |
|[<span data-ttu-id="dfc63-162">GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="dfc63-162">GetCollapseState</span></span>](imapitable-getcollapsestate.md) <br/> |<span data-ttu-id="dfc63-163">Возвращает данные, необходимые для перестроения текущего свернут или развернут состояние форматирование таблицы.</span><span class="sxs-lookup"><span data-stu-id="dfc63-163">Returns the data necessary to rebuild the current collapsed or expanded state of a categorized table.</span></span>  <br/> |
|[<span data-ttu-id="dfc63-164">SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="dfc63-164">SetCollapseState</span></span>](imapitable-setcollapsestate.md) <br/> |<span data-ttu-id="dfc63-165">Заново создает текущее развернутое или свернутое состояние форматирование таблицы с использованием данных, сохраненный во время предыдущего вызова метода **IMAPITable::GetCollapseState** .</span><span class="sxs-lookup"><span data-stu-id="dfc63-165">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the **IMAPITable::GetCollapseState** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dfc63-166">См. также</span><span class="sxs-lookup"><span data-stu-id="dfc63-166">See also</span></span>



[<span data-ttu-id="dfc63-167">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="dfc63-167">MAPI Interfaces</span></span>](mapi-interfaces.md)

