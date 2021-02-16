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
ms.openlocfilehash: d6a13799da4ef9315f9c23317fa18853d71c72f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420117"
---
# <a name="imapitable--iunknown"></a><span data-ttu-id="1fbf8-103">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1fbf8-103">IMAPITable : IUnknown</span></span>

  
  
<span data-ttu-id="1fbf8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1fbf8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1fbf8-105">Предоставляет представление таблицы только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-105">Provides a read-only view of a table.</span></span> <span data-ttu-id="1fbf8-106">**IMAPITable** используется клиентами и поставщиками услуг для управления тем, как отображается таблица.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-106">**IMAPITable** is used by clients and service providers to manipulate the way a table appears.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1fbf8-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="1fbf8-107">Header file:</span></span>  <br/> |<span data-ttu-id="1fbf8-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1fbf8-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="1fbf8-109">Выставим:</span><span class="sxs-lookup"><span data-stu-id="1fbf8-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="1fbf8-110">Объекты table</span><span class="sxs-lookup"><span data-stu-id="1fbf8-110">Table objects</span></span>  <br/> |
|<span data-ttu-id="1fbf8-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="1fbf8-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="1fbf8-112">Поставщики услуг и MAPI</span><span class="sxs-lookup"><span data-stu-id="1fbf8-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="1fbf8-113">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="1fbf8-113">Called by:</span></span>  <br/> |<span data-ttu-id="1fbf8-114">Клиентские приложения, поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="1fbf8-114">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="1fbf8-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="1fbf8-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="1fbf8-116">IID_IMAPITable</span><span class="sxs-lookup"><span data-stu-id="1fbf8-116">IID_IMAPITable</span></span>  <br/> |
|<span data-ttu-id="1fbf8-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="1fbf8-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="1fbf8-118">LPMAPITABLE</span><span class="sxs-lookup"><span data-stu-id="1fbf8-118">LPMAPITABLE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="1fbf8-119">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="1fbf8-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="1fbf8-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="1fbf8-120">GetLastError</span></span>](imapitable-getlasterror.md) <br/> |<span data-ttu-id="1fbf8-121">Возвращает структуру [MAPIERROR, содержащую](mapierror.md) сведения о предыдущей ошибке в таблице.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-121">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span>  <br/> |
|[<span data-ttu-id="1fbf8-122">Консультация</span><span class="sxs-lookup"><span data-stu-id="1fbf8-122">Advise</span></span>](imapitable-advise.md) <br/> |<span data-ttu-id="1fbf8-123">Регистрируется для получения уведомлений об указанных событиях, влияющих на таблицу.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-123">Registers to receive notification of specified events affecting the table.</span></span>  <br/> |
|[<span data-ttu-id="1fbf8-124">Unadvise</span><span class="sxs-lookup"><span data-stu-id="1fbf8-124">Unadvise</span></span>](imapitable-unadvise.md) <br/> |<span data-ttu-id="1fbf8-125">Отменяет отправку уведомлений, которые ранее были настроены с помощью вызова метода **IMAPITable::Advise.**</span><span class="sxs-lookup"><span data-stu-id="1fbf8-125">Cancels the sending of notifications previously set up with a call to the **IMAPITable::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="1fbf8-126">GetStatus</span><span class="sxs-lookup"><span data-stu-id="1fbf8-126">GetStatus</span></span>](imapitable-getstatus.md) <br/> |<span data-ttu-id="1fbf8-127">Возвращает состояние и тип таблицы.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-127">Returns the table's status and type.</span></span>  <br/> |
|[<span data-ttu-id="1fbf8-128">SetColumns</span><span class="sxs-lookup"><span data-stu-id="1fbf8-128">SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="1fbf8-129">Определяет конкретные свойства и порядок их появления в качестве столбцов в таблице.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-129">Defines the particular properties and order of properties to appear as columns in the table.</span></span>  <br/> |
|[<span data-ttu-id="1fbf8-130">QueryColumns</span><span class="sxs-lookup"><span data-stu-id="1fbf8-130">QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="1fbf8-131">Возвращает список столбцов для таблицы.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-131">Returns a list of columns for the table.</span></span>  <br/> |
|[<span data-ttu-id="1fbf8-132">GetRowCount</span><span class="sxs-lookup"><span data-stu-id="1fbf8-132">GetRowCount</span></span>](imapitable-getrowcount.md) <br/> |<span data-ttu-id="1fbf8-133">Возвращает общее число строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-133">Returns the total number of rows in the table.</span></span>  <br/> |
|[<span data-ttu-id="1fbf8-134">SeekRow</span><span class="sxs-lookup"><span data-stu-id="1fbf8-134">SeekRow</span></span>](imapitable-seekrow.md) <br/> |<span data-ttu-id="1fbf8-135">Перемещает курсор на определенную позицию в таблице.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-135">Moves the cursor to a specific position in the table.</span></span>  <br/> |
|[<span data-ttu-id="1fbf8-136">SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="1fbf8-136">SeekRowApprox</span></span>](imapitable-seekrowapprox.md) <br/> |<span data-ttu-id="1fbf8-137">Перемещает курсор в приблизительное дробное положение в таблице.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-137">Moves the cursor to an approximate fractional position in the table.</span></span>  <br/> |
|[<span data-ttu-id="1fbf8-138">QueryPosition</span><span class="sxs-lookup"><span data-stu-id="1fbf8-138">QueryPosition</span></span>](imapitable-queryposition.md) <br/> |<span data-ttu-id="1fbf8-139">Извлекает текущую позицию строки таблицы курсора на основе дробного значения.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-139">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>  <br/> |
|[<span data-ttu-id="1fbf8-140">FindRow</span><span class="sxs-lookup"><span data-stu-id="1fbf8-140">FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="1fbf8-141">Находит следующую строку в таблице, которая соответствует определенным условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-141">Finds the next row in a table that matches specific search criteria.</span></span>  <br/> |
|[<span data-ttu-id="1fbf8-142">Restrict</span><span class="sxs-lookup"><span data-stu-id="1fbf8-142">Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="1fbf8-143">Применяет фильтр к таблице, уменьшая набор строк только теми строками, которые соответствуют указанным условиям.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-143">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="1fbf8-144">CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="1fbf8-144">CreateBookmark</span></span>](imapitable-createbookmark.md) <br/> |<span data-ttu-id="1fbf8-145">Пометка текущего положения таблицы.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-145">Marks the table's current position.</span></span>  <br/> |
|[<span data-ttu-id="1fbf8-146">FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="1fbf8-146">FreeBookmark</span></span>](imapitable-freebookmark.md) <br/> |<span data-ttu-id="1fbf8-147">Освобождает память, связанную с закладкой.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-147">Releases the memory associated with a bookmark.</span></span>  <br/> |
|[<span data-ttu-id="1fbf8-148">SortTable</span><span class="sxs-lookup"><span data-stu-id="1fbf8-148">SortTable</span></span>](imapitable-sorttable.md) <br/> |<span data-ttu-id="1fbf8-149">Заказ строк таблицы на основе критериев сортировки.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-149">Orders the rows of the table based on sort criteria.</span></span>  <br/> |
|[<span data-ttu-id="1fbf8-150">QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="1fbf8-150">QuerySortOrder</span></span>](imapitable-querysortorder.md) <br/> |<span data-ttu-id="1fbf8-151">Извлекает текущий порядок сортировки для таблицы.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-151">Retrieves the current sort order for a table.</span></span>  <br/> |
|[<span data-ttu-id="1fbf8-152">QueryRows</span><span class="sxs-lookup"><span data-stu-id="1fbf8-152">QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="1fbf8-153">Возвращает одну или несколько строк из таблицы, начиная с текущего положения курсора.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-153">Returns one or more rows from a table, beginning at the current cursor position.</span></span>  <br/> |
|[<span data-ttu-id="1fbf8-154">Прервать</span><span class="sxs-lookup"><span data-stu-id="1fbf8-154">Abort</span></span>](imapitable-abort.md) <br/> |<span data-ttu-id="1fbf8-155">Останавливает все асинхронные операции, которые в настоящее время проводятся для таблицы.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-155">Stops any asynchronous operations currently in progress for the table.</span></span>  <br/> |
|[<span data-ttu-id="1fbf8-156">ExpandRow</span><span class="sxs-lookup"><span data-stu-id="1fbf8-156">ExpandRow</span></span>](imapitable-expandrow.md) <br/> |<span data-ttu-id="1fbf8-157">Расширяет категорию свернутой таблицы, добавляя строки, принадлежащие этой категории, в представление таблицы.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-157">Expands a collapsed table category, adding the leaf rows belonging to the category to the table view.</span></span>  <br/> |
|[<span data-ttu-id="1fbf8-158">CollapseRow</span><span class="sxs-lookup"><span data-stu-id="1fbf8-158">CollapseRow</span></span>](imapitable-collapserow.md) <br/> |<span data-ttu-id="1fbf8-159">Свернет расширенную категорию таблицы, удалив строки, принадлежащие этой категории, из представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-159">Collapses an expanded table category, removing the leaf rows belonging to the category from the table view.</span></span>  <br/> |
|[<span data-ttu-id="1fbf8-160">WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="1fbf8-160">WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |<span data-ttu-id="1fbf8-161">Приостанавливать обработку до завершения одной или более асинхронных операций в таблице.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-161">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>  <br/> |
|[<span data-ttu-id="1fbf8-162">GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="1fbf8-162">GetCollapseState</span></span>](imapitable-getcollapsestate.md) <br/> |<span data-ttu-id="1fbf8-163">Возвращает данные, необходимые для перестроения текущего свернутого или расширенного состояния классизированной таблицы.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-163">Returns the data necessary to rebuild the current collapsed or expanded state of a categorized table.</span></span>  <br/> |
|[<span data-ttu-id="1fbf8-164">SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="1fbf8-164">SetCollapseState</span></span>](imapitable-setcollapsestate.md) <br/> |<span data-ttu-id="1fbf8-165">Перестраивать текущее расширенное или свернутое состояние классизированной таблицы с помощью данных, сохраненных при предыдущем вызове метода **IMAPITable::GetCollapseState.**</span><span class="sxs-lookup"><span data-stu-id="1fbf8-165">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the **IMAPITable::GetCollapseState** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1fbf8-166">См. также</span><span class="sxs-lookup"><span data-stu-id="1fbf8-166">See also</span></span>



[<span data-ttu-id="1fbf8-167">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="1fbf8-167">MAPI Interfaces</span></span>](mapi-interfaces.md)

